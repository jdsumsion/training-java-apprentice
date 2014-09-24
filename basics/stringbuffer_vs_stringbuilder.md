# StringBuffer vs StringBuilder

This one is easy.

`StringBuffer` is a legacy type that should not be used any more.

`StringBuilder` is the replacement.

The difference is that initially `StringBuffer` had synchronized methods.  This was an early choice in Java's history that didn't need to be that way, because any multi-threaded string buffer access can be synchronized outside `StringBuffer` without making the common single-threaded case be as expensive.

On the other hand, `StringBuilder` doesn't have `synchronized` methods, and therefore, it's faster and lighter-weight.  They both do about the same thing, and are optimized and tuned to the same level.

---

Quiz for string buffers

Which one is faster?
- [x] `StringBuilder`
- [ ] `StringBuffer`

> Which ones is a legacy type again?

Why is it faster?
- [ ] because it is highly tuned
- [ ] because it uses an optimized representation of a string
- [x] because it doesn't have `synchronized` methods
- [ ] because it doesn't need to do UTF-8 conversions

> What's the difference between them again?

---
