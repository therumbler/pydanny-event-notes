=========
PyPy talk
=========

by Alex Gaynor

* Student at RPI
* Core Python Dev

    * cpython
    * PyPy

* Core Django Dev
* Interned at Quora and got them on PyPY
* Dressed very classy.

Two things go faster than C
==============================

* neutrinos
* PyPy

Story of PyPy
================

* psyco was JIT python

    * Managing it was hard
    * hardcoded for 32 bit CPUs and we are on 64 bit
    * Any changes to core Python killed pysco
    
* Years ago created a Python interpreter inside of Python

    * 2000x slower than cpython
    * ran on restricted Python (**r-python**)
    * Wrote a great compiler: now 10x slower than cpython
    * Added better garbage collection: now 4x slower than cpython
    
* New JIT for Python

    * Writing a JIT for Python sucks
    * Writing a generator for making JITs for any language is easier
    * **Alex Statement**: "PyPy is the only project I know of that uses SVN branches. That's the most impressive part"
    * Doing it this way made it faster? How? Wizard Magic?

* Now PyPY is going fast:

    * Crazy that it runs so much faster than cpython
    * Hard to believe
    * Python using a JIT generator to create a JIT library?
    * Faster than cpython
    * http://speed.pypy.org/

Why you should use PyPy
=======================

Science!
---------

* Fast and scientist friendly
* Now works with numpy!

    * Not complete
    
Tools
-----

* jitviewer

    * Finding slow spots in existing code
    * Looks at Python, byte code, assembler, et al
    
**Fast!!!**
-------------------

* Faster than cpython
* They now metric it's speed against C, not Python
* Compatibilities

    * Much work with third-party integration
    * lots of people are using Python instead of C extensions
    * PEP in place so that new stdlib stuff has to be pure python
    
* Quora is much more snappy
    
Python 3
--------

* PyPy is beginning the move to Python 3
* JIT generator to the rescue!


JIT generator means...
------------------------

* They can branch the Python 2.7 PyPy stuff to Python 3
    * Make the Python 3 version work
    * And since the JIT generator makes the code, both versions **will just work**
    
* Can do a GIL version for single CPU or non-GIL for multicore

    * JIT generated so...
    * **Both versions just work!!!**

The Future
============

* Lets make Python faster!
* Give us problem children to fix!

