Matrix SDK example with Google Analytics Pod
--------------------------------------------

This trivial project demonstrates a compiler error when using the MatrixSDK with
the Google Analytics pod. This is technically a swift project, however the same
error would occur in an Obj-C project if the `use_frameworks!` setting is
enabled in the project's podfile. (Obj-C projects support both Frameworks and
Libraries. Swift projects **only** support Frameworks)

1. `pod install`
2. attempt to build the project
3. Error:

```
Undefined symbols for architecture x86_64:
  "_OBJC_CLASS_$_GAIDictionaryBuilder", referenced from:
      objc-class-ref in MXSession-1B51A8C9071014D8.o
  "_OBJC_CLASS_$_GAI", referenced from:
      objc-class-ref in MXSession-1B51A8C9071014D8.o
ld: symbol(s) not found for architecture x86_64
clang: error: linker command failed with exit code 1 (use -v to see invocation)
```
