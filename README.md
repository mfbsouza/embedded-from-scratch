# Building a minimal embedded linux system from Scratch

What you are looking at right now is a collection of instructions on how to
bootstrap a tiny linux system for a embedded board (by the course of this
guide we will use a Beaglebone Black as exemple).

We will bootstrap the system by building our own cross compiler toolchain
and then using it to cross compile everything we need for a working Linux
based OS.

In contrast to similar guides, I try to explain why we are doing the things
the way we are doing them, instead of just throwing a bunch of copy-paste
command lines around (I'm looking at you, LFS).

This guide is divided into the following parts:

* [Basic Setup](scripts/setup.md). Lists some tools that you should have
  installed and walks through the steps of setting up the directory tree that
  we work in, as well as a few handy environment variables.
* [Building a cross compiler toolchain](scripts/crosscc.md).
* [Cross compiling a statically linked BusyBox and the kernel](scripts/kernel.md).
  The BusyBox is packaged into a small initramfs. We will make it boot on the
  Rapsberry Pi and explore some parts of the Linux boot process.
* [Building a simple userland](scripts/basic_usr.md). Mostly a
  Linux-From-Scratch-Style walkthrough to building some packages for a simple
  GNU userland. The userland is packed into a SquashFS image. The BusyBox
  based initrd is modified to mount it and switch into it.

## Thanks to

- AgentD for creating a great guide that this one is built on top off
