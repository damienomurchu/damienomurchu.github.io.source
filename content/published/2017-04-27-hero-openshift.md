---
draft: false
layout: post
date: 2017-04-27
title: "OpenShift in 30 mins"
subtitle: "Geting started with OpenShift"
description: ""
author: "@damienomurchu"
image: ""
tags:
  - OpenShift
  - Containers
  - Dev Ops
  - Node.js
URL: "/blog/2017/04/27/openshift-in-30-mins/"
categories: [Articles]
---

# Openshift in 30 mins with a Node.JS application  
  
## Prerequisites  

These steps presume you already have Docker installed. If you don't, look at this quickstart docker guide, or install Docker from [here](https://docs.docker.com/engine/installation/). Before you proceed any further confirm you can run docker process commands by trying `docker ps`


## Installing Openshift  
  
### Installing the oc cli tool  

Download the Linux [oc binary](https://github.com/openshift/origin/releases) and place it in your path.


## Bring your cluster up  

Bring up your cluster for the first time by running:

* `oc cluster up --public-hostname=127.0.0.1 --host-data-dir=$HOME/os/data-dir --host-config-dir=$HOME/os/config-dir`

If successful you should see output like the following:

![clusterup-terminal-output][image-clusterup]

To bring up your cluster subsequently pass in the `--use-existing-config` flag to your `oc cluster up` command:

* `oc cluster up --public-hostname=127.0.0.1 --host-data-dir=$HOME/os/data-dir --host-config-dir=$HOME/os/config-dir --use-existing-config`


### Troubleshooting  

If you encounter any errors the error messages are generally helpful enough to diagnose and resolve the issue. 
Before delving too deeply, be sure to double-check your version of Docker, and that it is compatible with the version of OpenShift you are using.

Some issues that were encountered included:

* the docker service daemon/ service was not running or needed to be restarted


### OpenShift console  

Once you have successfully brought your cluster up you should be able to access the OpenShift console through the url specified at the end of your `oc cluster up` log. 

![openshift-mainconsole][image-mainconsole]  

![openshift-consoledashboard][image-dashboard]


## Deploy your app to OpenShift  

Deploy your app by executing:

* `oc new-app <dockerhub-username>/<dockerhub-image-name>`

If you don't have an app, you can use the nodejs-hello example from google to test a deployment:

* * `oc new-app google/nodejs-hello`

In the OpenShift console you should see your app spinning up in its pod. 

To access your app, you will need to create an external-facing route to it. Do this through the cli with:

* `oc expose service/<name> --hostname=<www.example.com>`

Or if you are using the nodejs-hello example from google:

* `oc expose service/nodejs-hello --hostname=nodejs-hello.127.0.0.1.nip.io:8080`

You can also set up a route through the openshift console:

![openshift-selectroute][image-selectreoutes]  

![openshift-createroute][image-createroute]  

Congratulations! You have now deployed your app on OpenShift and should be able to access your deployed app through the route you specified.


## Bringing down your cluster  

To bring down your cluster `oc cluster down` will take down your cluster.


## Summary & further reading  

Through the above steps you should have:

* Installed OpenShift locally
* Installed the OC CLI to interact with your OpenShift cluster
* Brought up your local cluster and deployed a Node.JS app from a Docker container image
* Created a route/ url to access your app

As seen above, Containerised apps can be deployed quite easily to an OpenShift cluster. [Docker Hub](https://hub.docker.com/) can facilitate this process by providing a place to host your container images, and you may wish to create an account there (some steps to do so can be found [here](/hero-docker/)).

OpenShift also supports building and deploying your directly from source code, which may be covered in a subsequent document. 

For further reading, check out the below links & also feel free to reach out to feedhenry-dev at redhat.com or the #feedhenry IRC channel if you need help.

* [A summary of the oc cluster up options](https://www.mankier.com/1/oc-cluster-up)
* [A summary/ set of man pages for the various oc client command options](https://www.mankier.com/package/origin-clients)
* [Documentation for OpenShift cluster management](https://github.com/openshift/origin/blob/master/docs/cluster_up_down.md)
* [The OpenShift Developer guide](https://docs.openshift.com/enterprise/3.1/dev_guide/index.html)


[image-clusterup]: /assets/images/hero-openshift/oc-cluster-up.png  
[image-mainconsole]: /assets/images/hero-openshift/openshift-opening-screen.png  
[image-dashboard]: /assets/images/hero-openshift/openshift-dashboard.png  
[image-selectreoutes]: /assets/images/hero-openshift/select-routes.png  
[image-createroute]: /assets/images/hero-openshift/create-route.png  
