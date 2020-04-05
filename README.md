# Source code for georgeluong.com

## Testing Builds Locally
1. Ensure that all gem dependencies are met:
```bash
bundle install --path vendor/bundle
```
1. Compile and host the site locally
```bash
bundle exec jekyll server -H 127.0.0.1
```

## Compiling and building the site
1. This should happen once the changes are merged to `master` in Github
1. Jekyll builds the site, and we're using S3 to host the static assets.
