# clang-format
node.js module which wraps the native clang-format executable.

## From the command-line:

    $ npm install -g clang-format
    $ clang-format -help

If your platform isn't yet supported, you can create the native binary from
the latest upstream clang sources, make sure it is stripped and optimized
(should be about 1.4MB as of mid-2015) and send a pull request to add it.

## Compiling clang-format

For Linux, compile a statically linked MinSizeRel build:

    cmake -G Ninja -DCMAKE_BUILD_TYPE=MinSizeRel -DLLVM_BUILD_STATIC=true ..
    ninja clang-format

For Mac OS X, static linking is not required.

## Windows

Windows snapshot builds to include in the release can be found at the
[LLVM website](http://llvm.org/builds/).
