# Embedded Linux System from Scratch

What you are looking at right now is a collection of instructions on how to
bootstrap a tiny linux system for a embedded board.

We will bootstrap the system by building our own cross compiler toolchain
and then using it to cross compile everything we need for a working Linux
based OS.

In contrast to similar guides, I try to explain why we are doing the things
the way we are doing them, instead of just throwing a bunch of copy-paste
command lines around (I'm looking at you, LFS).

## Content

This guide is divided into the following parts:

* [host machine setup](docs/setup.md). 
	* Tools that you should have installed and steps to setup the 
	directory tree that we work in.
* [Building a cross-toolchain](docs/crosscc.md).
	* Steps to compile a cross compiler toolchain and creating a sysroot 
	directory

## Thanks to

- AgentD for creating a great guide that this one is built on top of
