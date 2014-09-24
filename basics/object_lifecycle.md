# Object Lifecycle

What is the lifecycle of an Object in Java?

Java is two things:
* a language
* a virtual machine

The language allows programmers to create object instances and use them.  It also specifies a memory model that includes garbage collection.

## Garbage Collector

Instead of having to manage memory manually, the Java Virtual Machine (JVM) keeps track of whether an object is still in use.  When an object is no longer in use, its space in RAM is reclaimed.  This is called "garbage collection".

The "garbage collector" is a module inside the JVM that determines "object liveness" and takes care of memory management.

There are [4 garbage collector implementations](http://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html) in modern JVMs:
1. Serial collector
2. Parallel collector
3. Concurrent Mark Sweep collector (CMS)
4. G1 collector

The CMS collector is the default, but G1 is going to replace it post Java 7.


---

Garbage collection quiz

When is an object a candidate for garbage collection?
- [ ] programmer calls `finalize()`
- [x] object is no longer referenced anywhere
- [ ] `System.gc()` is called on a system thread
- [ ] programmer calls `free()`

> Try again - how does garbage collection work?

What is the default garbage collector in Java 7?
- [ ] Parallel collector
- [ ] G1 collector
- [ ] Serial collector
- [x] Concurrent Mark Sweep collector (CMS)

> Try again - what is current, and what is the new default?

---
