---
layout: post
comments: true
---

It's always a bit difficult choosing how to start writing about a new project. Here goes.

I thought it would be fun to try and experiment with getting a small RC car to drive around a track by itself. This would be an exercise in embedded programming, computer vision and system dynamics as well as an exploration into machine learning. I know little of machine learning (having only studied Andrew Ng's Coursera course), but I think a project like this would be a good platform to theoretically and empirically study the various machine learning techniques and compare them to classical control methods.

I *believe* this is a realistic project. I am of course going to be hitting dead ends and many bumps along the way and if anyone reading this has any suggestions, then please throw them my way (*if* anyone is reading this, heh),

## Goals

1. Install hardware on chosen platform and write rudimentary code to control the RC car.
2. Develop a self-driving algorithm using classical computer vision and system control techniques.
3. Develop a self-driving algorithm using machine learning.

Since this is just a hobby, I'm not going to impose deadline, use scrum, draw out a Gantt chart or practice extensive project management procedures. Let's leave that for 9-5 and just use simple GTD.

## Tools

I haven't quite decided whether I'll be coding in C++ or Python (OpenCV comes in both flavours). Python would be more adventageous for a quicker development process but then again there's C++, because who wouldn't like to tough it out. Most machine learning libraries tend to be implemented in C++ but also offer a Python API over it. Google's TensorFlow supports both but they say their Python API is the most complete and the easiet to use. Caffe, which is supposedly an implementation of MATLAB's convnets in C++ (Yay MATLAB!) also offer a Python API. The barebones code (control of the car and the basic computer vision) would be quite easily transferred between the two language anyway.

I'll cover the actual hardware and the equipment I'll be using in the following blog post. I'll also try and keep a track of the expenses so that if any of you aspire to build the same thing then you'll know how much it'll cost you.

## Namesake

It's probably well known that Apple is developing an electric car, which is most likely going to be self-driving, the codename of which is Project Titan. Titan is Saturn's *largest* moon and since I'll be working on a very small car, compared to Apple's sedan (how weird does that sound), I thought it would be fun to call it Project Mimas, after Saturn's *smallest* moon. It was a bit of a face slap moment when I found out that they were inspired by Greek mythology and not astronomy, but Project Mimas still sounds cool, right guys?



Since this is May the 4th, happy Star Wars day!

![May the Fourth be with you.](/images/maytheforce.gif)