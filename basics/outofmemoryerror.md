# OutOfMemoryError

Write an application to find out how many total characters can be held in a list of strings before you run out of memory.

Here is an example of how some people start writing this application:

``` java
import java.util.ArrayList;
import java.util.List;

public class MemoryMeter {

  public static void main(String[] args) {
    // 50 chars
    String s = "01234567890123456789012345678901234567890123456789";
    List<String> list = new ArrayList<>();
    long items = 0;
    try {
      while (true) {
        items++;
        list.add(s);
      }
    }
    // NOTE: you should NEVER catch OutOfMemoryError in a real app
    // unless you call System.exit(1) right after
    // running out of memory leaves the JVM in an UNSTABLE state, even if you catch it
    catch (OutOfMemoryError e) {
      System.out.println("items added: " + items);
    }
  }
}
```

Here is an example of how to run the program:
``` bash
# -Xmx is for shrinking the heap to 10MB - runs faster
$ java -Xmx10m MemoryMeter
```

What is wrong with the program above?  Why isn't it giving you the correct answer?  How many distinct `char[]` values are being pointed to?

How are you going to fix it?

---

OutOfMemoryError quiz

Is the number of characters the same as the number of bytes?
- [ ] yes
- [x] no

> How many bytes does a character take up in memory?  How does that affect the amount of memory used?

How can you create a `String` that contains a copy of another `String` with a different `char[]`?
- [ ] `new String(str)`
- [x] `new StringBuilder(str).toString()`
- [ ] `str.clone()`
- [x] `new String(s.getBytes("UTF-8"), "UTF-8")`

> Attach the [JDK source code](http://stackoverflow.com/a/16182330/1667497) in your IDE.  Look at the various options.  Which ones reuse the `char[]` and which ones create a new `char[]`?

---
