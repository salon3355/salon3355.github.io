# Salon3355

## Quickstart

```bash
PROJECT="salon3355"
JEKYLL_VERSION="4.2.2"

# Install the required gems
sudo docker run --rm \
    --name "$PROJECT-bundle-install" \
    --env BUNDLE_PATH="vendor/bundle" \
    --volume "$PWD:/srv/jekyll" \
    "jekyll/jekyll:$JEKYLL_VERSION" \
    bundle install

# Run the development environment on port 4000
sudo docker run --rm --tty --interactive \
    --name "$PROJECT-jekyll-serve" \
    --env BUNDLE_PATH="vendor/bundle" \
    --volume "$PWD:/srv/jekyll" \
    --publish "127.0.0.1:4000:4000" \
    "jekyll/jekyll:$JEKYLL_VERSION" \
    bundle exec jekyll serve --host 0.0.0.0

# Clear temporary files
sudo rm -rfv vendor _site
```

## Links

* https://docs.github.com/en/pages/quickstart
* https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll
* https://stackoverflow.com/questions/6317980/you-have-already-activated-x-but-your-gemfile-requires-y
* https://github.com/orgs/community/discussions/22795
* https://pixabay.com/photos/nail-art-manicure-nails-nail-polish-5653459/
* https://pixabay.com/photos/eyelash-eyeball-eyebrow-mascara-3300338/
* https://pixabay.com/photos/woman-girl-makeup-lashes-female-1677558/
