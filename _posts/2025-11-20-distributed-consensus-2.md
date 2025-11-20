---
layout: post
title: "Distributed consensus 2/2"
---

Last time we made some basic observations:
- We defined a database which one can write to and read from.
- We observed that in a large volume where many machines are involved, setup consistency is a challenge.

Google Spanner, which is a technology I wanted to recall when attempting to write this provides a very attractive solution to the problem.
Let's consider a simplified data scenario where we care about maintaining only one piece of state.
Our way of interacting with this simple database will be to either read or write that one piece of data completely.

In order to make such a database reliable and consistent we need to resolve a problem of achieving **consensus**.

(to be continued)
