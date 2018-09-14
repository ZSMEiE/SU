# jekyll-theme-new

[![Build Status](https://travis-ci.org/vllur/jekyll-theme-new.svg?branch=master)](https://travis-ci.org/vllur/jekyll-theme-new)

Jekyll-theme-new is a Jekyll theme template which provides many out-of-the-box features (like, for example, complex Travis CI testing), to help you build your new, awesome (and Github Pages compatible) Jekyll theme.

## Features
- full Github Pages compatibility
- custom baseurl support
  - (whole site can live on domain subdirectory, e.g. on Github project page)
- posts tags
- seo tags
- Google Analytics
- complex Travis CI testing with [htmlproofer](https://github.com/gjtorikian/html-proofer) 
  - (by [jekyll-test](https://github.com/Floppy/jekyll-test) gem)
- post pinning 
  - (with automatic hiding oldest pinned posts)

See [wiki](https://github.com/vllur/jekyll-theme-new/wiki) to learn more about every feature.

## Dependencies
see [Gemfile](https://github.com/vllur/jekyll-theme-new/blob/master/Gemfile)

Make sure to install all necessary gems with Bundler:
 - ```bundle install```
 - ```bundle exec jekyll build```

## Usage
Quick how-to guide on creating a new theme with ```jekyll-theme-new```:
- Make sure that you have right environment
  - you will need Ruby and Bundler installed on your local machine
- Clone the repo
  - you can either start working on files just from there, or use ```jekyll new-theme``` (if you want e.g make a theme gem) and then overwrite generated files
- Install necessary gems
  - ```bundle install```
  - ```bundle exec jekyll build```
- Test your environment
  - run ```bundle exec jekyll serve```
  - your test site will be accessible at ```localhost:4000/baseurl```
- Customize ```_config.yml```
  - make sure that you have replaced all info, and there isn't any blank variables (besides scope-path which needs to be blank, and google-analytics, which can be blank)
  - leave ```baseurl``` with ```/``` if you want to publish your site from root of a domain (e.g. Github Pages user site), or with ```/repository``` if you want to publish it from regular repository
- Create repository and upload all files
  - if your repo is named ```yourusername.github.io``` it will be accesible at that address
  - if not, it will be at ```yourusername.github.io/reponame```, but you will need to publish it from master branch in repo settings
- Set up Travis CI
  - you just need to activate your repostitory at ```travis-ci.org```
  - you will see your newest build after every push
- Delete README.md
  - you can set up your read-me file, e.g. with Travis badge
- And finally - start working on your theme!

You can create new CSS files in ```_sass``` directory, and then link them in ```css/main.css```. Parts of HTML can be found in ```_includes```, and layouts are in ```_layouts```. If you want to read more about / remove a feature, head up to the [wiki](https://github.com/vllur/jekyll-theme-new/wiki).

## Contributing
Feel free to post an issue to report a bug or to ask a question. If you want contribute to the code of this project, please first post an issue in which you can describe proposed changes. Thanks!
