---
layout: page
permalink: projects
---

I've done many, many projects in my life. This is a small subset of some of the interesting ones.

# Software projects

## [Zed](https://github.com/archimedespi/zed) - a programming language
I read a bunch of "Compilers: Principles, Techniques and Tools", and thought it would be fun to implement a very simple compiler. I started out trying to do it in one week, but missed the deadline (big suprise). I continued working on it though, and now it's fully functional and can compile a "Hello World" program.
Zed is written in C, *flex*, and *bison*. It generates C as IR, which can then be compiled using `clang` or `gcc`. The syntax is inspired by Javascript and Groovy.
Here's an example of me writing a basic hello world program in Zed:

![gif of terminal, writing hello world in zed](http://i.imgur.com/KGKv3au.gif)

# Hardware projects

## Rapid prototyping a laboratory-equipment repair
A chromatography instrument company I work with had a critical part fail by snapping in half:

![broken sampler bracket](https://i.imgur.com/7B7ldH6.jpg)

I quickly CADed and 3d-printed a replacement bracket in Solidworks, which works beautifully:

<iframe id="ytplayer" type="text/html" width="640" height="390"
  src="http://www.youtube.com/embed/pvNaDUpizJo"
  frameborder="0"/>