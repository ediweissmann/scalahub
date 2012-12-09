---
layout: post
title: "Goose - Article extractor"
date: 2012-12-09 22:15
comments: true
categories: [github, article extraction]
gitHubUrl: https://github.com/jiminoc/goose
projectHomepage:
---

[Goose](https://github.com/jiminoc/goose) is an article extractor written in Scala. Point it to an url and it will extract the **plain text** of the article, along with the **main image**,  embedded **movies** and **meta information** that it finds (tags, publish date). Awesome stuff, right?

Here's an example of how to use it (It's this simple!):

``` scala
val goose = new Goose(new Configuration)
val article = goose.extractContent(url)

println(article.cleanedArticleText)
println(article.title)
println(article.tags)
```

Checkout [the live demo page](http://jimplush.com/blog/goose) where you can play with parsing an url of your choice.

[Goose](https://github.com/jiminoc/goose) is created by [Jim Plush](http://jimplush.com/) from [Gravity.com](http://gravity.com) Maven/SBT dependency is available for quick use in your project.


