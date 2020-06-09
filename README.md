# C++ Requests Example

Example project that uses [C++ Requests](https://github.com/whoshuu/cpr), a
simple wrapper around [libcurl](http://curl.haxx.se/libcurl) inspired by the
excellent [Python Requests](https://github.com/kennethreitz/requests) project.

## Building

This project requires CMake 3.11 or greater. Build in the usual CMake fashion:

```
mkdir build
cd build
cmake ..
make
```

If you have libcurl installed, you can speed up the build by adding
`-DUSE_SYSTEM_CURL=ON` to the CMake command. Additionally, you can skip
building dependency tests with `-DBUILD_CPR_TESTS=OFF` to shave off even more
time.

This should produce a binary in the `build/src` directory called `example`. Run
it! If you get a response in the form of some json object, then everything
worked as expected! The program you just ran is a sweet 3 liner you'll find
[here](example.cpp).

## Documentation

You can get the latest documentation for C++ Requests
[here](https://whoshuu.github.io/cpr). It's a work in progress, but it should
give you a better idea of how to use the library than the
[tests](https://github.com/whoshuu/cpr/tree/master/test) currently do.

## Requirements

The only explicit requirement is a C++11 compatible compiler such as clang or
gcc. The minimum required version of gcc is unknown, so if anyone has trouble
building this library with a specific version of gcc, do let me know.

## Contributing

Please fork the parent repository and contribute back using
[pull requests](https://github.com/whoshuu/cpr/pulls). Features can be requested
using [issues](https://github.com/whoshuu/cpr/issues). All code, comments, and
critiques are greatly appreciated.

For direct contributions to the example project, you can open
[pull requests](https://github.com/whoshuu/cpr-example/pulls) or
[issues](https://github.com/whoshuu/cpr-example/issues).
