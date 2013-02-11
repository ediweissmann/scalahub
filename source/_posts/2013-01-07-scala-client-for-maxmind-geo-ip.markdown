---
layout: post
title: "Scala client for MaxMind Geo-IP"
date: 2013-01-07 22:47
comments: true
categories: 
gitHubUser: snowplow
gitHubProject: scala-maxmind-geoip
---
![You are here](http://farm1.staticflickr.com/51/138297060_de2979e042.jpg)

[scala-maxmind-geoip](https://github.com/snowplow/scala-maxmind-geoip) is a Scala wrapper for the [MaxMind](http://dev.maxmind.com/geoip/) Java Geo-IP library. 

Besides the friendly **Scala syntax**, you get **configurable LRU caching** out of the box. And if you are using `SBT` there's built-in **automagical update** to the latest MaxMind `GeoLiteCity.dat` and Java client library version.

Quick usage example:

``` scala
val geoDbFile = new java.io.File(getClass.getResource("/maxmind/GeoLiteCity.dat").toURI())
val ipGeo = new IpGeo(dbFile = geoDbFile, lruCache = 100, memCache = false)

for (loc <- ipGeo.getLocation("204.232.175.78")) {
  println(loc.countryCode)   // US
  println(loc.countryName)   // United States
}
```

[scala-maxmind-geoip](https://github.com/snowplow/scala-maxmind-geoip) is written by [Alexander Dean](https://github.com/alexanderdean) from [SnowPlow Analytics](http://snowplowanalytics.com). 