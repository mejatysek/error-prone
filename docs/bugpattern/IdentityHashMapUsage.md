`java.util.IdentityHashMap` uses reference-equality when comparing keys which
isn't what a reader would expect if the type of the variable is `java.util.Map`.
Due to this special nature of `IdentityHashMap`, we recommend preserving the
type of the variable. This means that we shouldn't type upcast `IdentityHashMap`
to its super classes and always use the default type. This is to make sure that
reader/maintainer of the code is aware about it and takes special consideration
when invoking any method on them.
