---
layout: post
title: "scalaj-time - A Scala Wrapper For Joda Time"
date: 2012-12-22 12:52
comments: true
categories: [date, time]
gitHubUrl: https://github.com/scalaj/scalaj-time
---
![Alarm clock](http://farm5.staticflickr.com/4017/4469802928_3a9405be0d_n.jpg)

[scalaj-time](https://github.com/jorgeortiz85/scala-time) is a scala **convenience wrapper** around the [Joda time](http://joda-time.sourceforge.net/) libraries.

It provides more **pleasant syntax** like operators addition, subtraction and comparison, and also, fields are now available in the Scala convention, without the "get" prefix.

Here's some example usage:

``` scala
import org.scala_tools.time.Imports._

DateTime.now // returns org.joda.time.DateTime

DateTime.now + 2.months // two months from now

DateTime.nextMonth < DateTime.now + 2.months // true

DateTime.now to DateTime.tomorrow // returns an org.joda.time.Interval

(1.hours + 25.minutes + 15.seconds).millis // returns org.joda.time.Duration

9.months + 3.days // returns org.joda.time.Period
```

[scalaj-time](https://github.com/jorgeortiz85/scala-time) is created by [Jorge Ortiz](https://github.com/jorgeortiz85) from [scalaj](https://github.com/scalaj).
