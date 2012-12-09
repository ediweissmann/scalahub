---
layout: post
title: "Goose - Article extractor"
date: 2012-12-09 22:15
comments: true
categories: [github, article extraction]
gitHubUrl: https://github.com/jiminoc/goose
projectHomepage:
---

In a nutshell, point [Goose](https://github.com/jiminoc/goose) to an url and it will extract the **plain text** of the article, along with the **main image**,  embedded **movies** and **meta information** that it finds (tags, publish date). Awesome stuff, right?

Checkout [the live demo page](http://jimplush.com/blog/goose) where you can play with parsing an url of your choice.

``` scala
val goose = new Goose(new Configuration)
val article = goose.extractContent(url)
println(article.cleanedArticleText)
println(article.title)
println(article.tags)
```

[Goose](https://github.com/jiminoc/goose) is created by [Jim Plush](http://jimplush.com/) from [Gravity.com](http://gravity.com) Maven dependency is available.


