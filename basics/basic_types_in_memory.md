# Basic Types in Memory

The following are basic types in Java:

- `boolean` (true/false)
- `byte` (-128..127)
- `short` (-32768 to 32767)
- `int` (-2147483648 to 2147483647)
- `long` (-9223372036854775808 to 9223372036854775807)
- `float` (single-precision 32-bit format IEEE 754)
- `double` (double-precision 64-bit format IEEE 754)
- `char` ('\u0000' to '\uffff')
- `String` (special object containing int length & `char` array)

The [Java Language Specification](http://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.2) says how each of these primitive types should behave.

In memory, you can think of an isolated primitive variable as taking a machine word of memory.  There are exceptions to this:

- if multiple primitives are together as instance fields
- if there are arrays of primitives

In those cases, you can think of the primitives as taking the following amount of space in memory:

- `boolean` (1 byte)
- `byte` (1 byte)
- `short` (2 bytes)
- `int` (4 bytes)
- `long` (8 bytes)
- `float` (4 bytes)
- `double` (8 bytes)
- `char` (2 bytes)
- `String` (4 bytes for length, plus array of 2 byte `char`)

See [this stack overflow question](http://stackoverflow.com/questions/229886/size-of-a-byte-in-memory-java) for more details.

---

Memory size quiz

How much space is required for a boolean array of size 100?
- [x] implementation dependent
- [ ] guess: 400 bytes
- [x] guess: 100 bytes
- [ ] guess: 800 bytes

> How big is a boolean?  In a field?  In an array?

How much space is required for a single boolean field?
- [ ] guess: one byte
- [x] implementation dependent
- [x] guess: one machine word

> Is the field packed?  Is it word aligned?

---
