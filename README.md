# Source code for georgeluong.com

## Testing Builds Locally
*_NOTE_*: Post headers must include the following:
```bash
layout: post
title: <Your title>
catagories: blog|fiction
tags:
  - <tag>
image:
  path: images/filename.jpg # this is optional
last_modified_at: YYYY-MM-DDTHH:MM:SS-8:00
(for example    : 2020-01-01T21:13:00-8:00)
```

1. Ensure that all gem dependencies are met:
```bash
bundle install --path vendor/bundle
```

2. Testing htmlproofer and favicons
```bash
bundle exec htmlproofer ./_site --allow-hash-href --check-favicon --check-html --disable-external
```

3. Compile and host the site locally
```bash
bundle exec jekyll server -H 127.0.0.1
```

## Compiling and building the site
1. This should happen once the changes are merged to `master` in Github
1. Jekyll builds the site, and we're using S3 to host the static assets.
1. We use Octopress to deploy the site (configs stored in `_deploy.yml` -- this is in gitignore so we don't leak credentials)
```bash
bundle exec octopress deploy
```
