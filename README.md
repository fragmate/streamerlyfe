# README

# Installation
This is assuming the machine already has Ruby installed.

`cd path/to/repo`
`gem install bundler`
`bundle install`

# Development
`jekyll serve --watch`

# Deployment
`JEKYLL_ENV=production bundle exec jekyll build`
`git commit -am 'prod build'`
`git subtree push --prefix _site origin gh-pages`