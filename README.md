# blog_source

Source files for personal blog. 


## Adding posts

### New draft posts

New drafts can be created in the [draft directory][drafts-directory]. The [draft template][draft template] contains all the necessary front-matter metadata and should be used when creating new draft posts.


### Publishing drafts

When a draft post is ready to be published, update the front-matter in the draft from `draft: true` to `draft: false`, and move it to the [published posts][published-posts-directory].


## Deploying site

The site is automatically redeployed via the [publish GitHub action][publish-gh-action]. Each merge to the `main` branch will result in this action being triggered and the site being redeployed.


## 


[drafts-directory]: ./content/drafts
[draft template]: ./content/drafts/_template.md
[published-posts-directory]: ./content/published
[publish-gh-action]: ./.github/workflows/publish-site.yml