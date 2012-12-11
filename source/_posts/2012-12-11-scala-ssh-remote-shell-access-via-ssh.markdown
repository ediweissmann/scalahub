---
layout: post
title: "scala-ssh - Remote shell access via SSH"
date: 2012-12-11 21:34
comments: true
categories: [ssh]
gitHubUrl: https://github.com/sirthias/scala-ssh
---

[scala-ssh](https://github.com/sirthias/scala-ssh) provides remote shell access via SSH for your Scala applications.

Besides remote execution of shell commands, you get access to `stdin`, `stdout` and `stderr`, private key authentication and host configuration via code or from resource file.

Here's a simple example of how to use the API:

``` scala
SSH("repl.scalahub.com") { client =>
  client.exec("scala --version").right.map { res =>
    println("And the scala version is... [drums]... \n" + res.stdOutAsString())
  }
}
```
[scala-ssh](https://github.com/sirthias/scala-ssh) is written by [Mathias](https://github.com/sirthias) from [Spray.io](http://spray.io).
