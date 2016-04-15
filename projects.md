---
layout: page
permalink: projects
---

This is a small subset of some of the interesting projects I've done.

# Software projects

## [Zed](https://github.com/archimedespi/zed) - a programming language
I read a bunch of "Compilers: Principles, Techniques and Tools", and thought it would be fun to implement a very simple compiler. I started out trying to do it in one week, but missed the deadline (big surprise). I continued working on it though, and now it's fully functional and can compile a "Hello World" program.
Zed is written in C, *flex*, and *bison*. It generates C as IR, which can then be compiled using `clang` or `gcc`. The syntax is inspired by Javascript and Groovy.
Here's an example of me writing a basic hello world program in Zed:

![gif of terminal, writing hello world in zed](http://i.imgur.com/KGKv3au.gif)

## [Lossy](https://github.com/archimedespi/lossy)
Lossy is my perpetually-changing OS in Rust. Right now it can sort of allocate memory, I'm currently working on a keyboard driver.

## [NSA Away](https://hackaday.io/project/1569-nsa-away)
I collaborated with a number of other hackerspace members at Sector67 to design and implement a semi-hardware-based one-time-pad encryption tool. A hardware CSRNG device we designed was used to generate OTP keys, which were then used by a custom Android application for encrypting a plaintext, which were then sent over email from a computer and entered using custom keyboard-emulating USB OTG hardware to insulate the phone from the computer. Received cyphertext was entered into the phone using OCR, to provide an airgap between the receiving machine and the decryption and keys.
A bog-standard XOR OTP stream cipher was used to perform encryption.

# Hardware projects

## Rapid prototyping a laboratory-equipment repair
A chromatography instrument company I work with had a critical part fail by snapping in half:

![broken sampler bracket](https://i.imgur.com/7B7ldH6.jpg)

I quickly CADed and 3d-printed a replacement bracket in Solidworks, which works beautifully:

<iframe id="ytplayer" type="text/html" width="640" height="390"
  src="http://www.youtube.com/embed/pvNaDUpizJo"
  frameborder="0"/>

