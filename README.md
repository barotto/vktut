Shabi's Vulkan Tutorials
========================

This is a repository of tutorials on Vulkan.  It starts with the basics,
enumerating your GPUs, allocating memory and getting computation done.  It then
moves on to actually displaying things and using shaders.  Along the way, some
of the optional Vulkan layers are explored.

Each tutorial may use functions implemented in a previous tutorial.  The
functions are thus named as `tutX_*()` so that it would be immediately obvious
which tutorial you should refer to, if you don't remember what that function
does.

These tutorials were developed in Linux, and I have no intention of trying them
on Windows.  Feel free to send a pull request if they needed tweaks to run on
that.  You would need the following external libraries:

- Vulkan, of course
- SDL2
- X11-xcb

The tutorials are source code themselves, with enough comments in them to
explain how things are done and/or why.  I strongly recommend reading the
Vulkan specifications alongside the tutorials.  It is well-written and easy to
grasp.  Also note that Vulkan is not for the faint of heart.  I expect you are
not struggling with reading C code and have some understanding of computer
graphics and operating systems.

The `main.c` of each tutorial glues together the functionalities implemented in
the `tut*.c` files, and may include uninteresting things like printing out
information.  The important stuff is usually in `tut*.c` files.

Build and Execution
-------------------

This project uses autotools.  If you have received the project as a release
tarball, you can go through the usual procedure:

```
mkdir build && cd build
../configure
make
```

If you are building from source, you would need autotools installed and do the
following step beforehand:

```
autoreconf -i
```

Each tutorial will have an executable in its own directory that you can run.

---

**Disclaimer:** I am writing these tutorials as I am learning Vulkan myself.  I
am in no way an expert in computer graphics and my own knowledge of OpenGL
barely passes 1.2.  Please do not consider these tutorials as "best practices"
in Vulkan.  They are intended to merely ease you in Vulkan, getting you
familiar with the API.  How to _best_ utilize the API is beyond me at this
point.
