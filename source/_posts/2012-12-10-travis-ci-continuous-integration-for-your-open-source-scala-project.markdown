---
layout: post
title: "Travis CI - Continuous integration for your open source scala project"
date: 2012-12-10 20:32
comments: true
categories: 
gitHubUser: travis-ci
gitHubProject: travis-ci
projectHomepage: http://travis-ci.org/
---

![Travis CI logo](/images/travis-ci.jpeg)

Do you have an open source project written in Scala? (Well done!) [Travis CI](http://travis-ci.org) offers a hosted continuous integration for the open source community, and [they support Scala projects](http://about.travis-ci.org/docs/user/languages/scala/).

Setting up continuous integration with [GitHub](http://github.com/) is super-easy. Simply add a `.travis.yml` file to your project, telling Travis that it's written in Scala, and optionally defining the Scala version to use. That's it! Travis is pretty smart and will figure out by itself if you chose SBT or Maven :)

``` scala
language: scala
scala:
   - 2.8.2
   - 2.9.2
```

Then, simply log in to [travis-ci.org](http://travis-ci.org) with your GitHub account and enable continuous integration for your project [from the Travis profile page](https://travis-ci.org/profile). 

Once authorized to your GitHub account, Travis will add a commit hook that builds your project each time you commit code.
A nice touch is adding the Travis CI build status to your README file [by using the build status images](http://about.travis-ci.org/docs/user/status-images/), like the one below.

![Travis build status](https://secure.travis-ci.org/ediweissmann/metrics-statsmix.png?branch=master)



