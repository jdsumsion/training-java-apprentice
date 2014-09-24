# StringBuffer vs StringBuilder

This one is easy.

`StringBuffer` is a legacy type that should not be used any more.

`StringBuilder` is the replacement.

The difference is that `StringBuilder` doesn't have `synchronized` methods, and therefore, it's faster and lighter-weight.
