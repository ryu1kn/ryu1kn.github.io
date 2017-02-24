---
layout: post
title:  Golang way
date:   2017-02-06 21:57:58 +1100
categories: blog
---

* I want to convert a list of type T1 to a list of type T2. Do I convert its element one-by-one?
  * Yes, simply iterate over the whole list. cf. [Type converting slices of interfaces in go](http://stackoverflow.com/questions/12753805/type-converting-slices-of-interfaces-in-go)
* Does a Go project needs to be under `GOPATH`? I wrote a tool in Go and want to check it into an exising repository, but don't want to put the repo under `GOPATH` as it's mostly written in non-Go languages
  * Add an appropriate place to `GOPATH` every time you run go commands. cf. [`GOPATH` for a project written in several languages (for example Go and Python)?](https://groups.google.com/forum/#!topic/golang-nuts/6orXabMNivE)
* [AWS SDK for Go](http://docs.aws.amazon.com/sdk-for-go/api/) exposes `struct`s but not many `interface`s hence hard to mock in unit tests.
  * Define interfaces as you need and use AWS SDK through them. cf. [Discussion: How should you unit test code which uses the aws-sdk-go](https://github.com/aws/aws-sdk-go/issues/88)
* Where is list manipulation functions like `filter`, `map`, `reduce`, ...?
  * Use `for` loop. cf. [Map, reduce and filter in Go?, Writing type parametric functions in Go](http://blog.burntsushi.net/type-parametric-functions-golang/)
* Dereferencing a `nil` pointer doesn't cause an error??
  * No. There was a discussion: [Why can I call methods on nil pointers?](https://groups.google.com/forum/#!topic/golang-nuts/wcrZ3P1zeAk)
* Go's `struct` doesn't have a constructor. How can I make sure my objects are instantiated consistently?
  * Write a factory method to instantiate an object. cf. [Constructors - Go Language Patterns](http://www.golangpatterns.info/object-oriented/constructors)
* Is it appropriate to use channel here? [Go channels are bad and you should feel bad](http://www.jtolds.com/writing/2016/03/go-channels-are-bad-and-you-should-feel-bad/)
