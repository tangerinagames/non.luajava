# non.luajava #
[![Build Status](https://travis-ci.org/non2d/non.luajava.svg?branch=master)](https://travis-ci.org/non2d/non.luajava)

  * [Supported platforms](#supported-platforms)
  * [About LuaJava](#about-luajava)
  * [Building](#building)
    * [Building natives](#building-natives)
    * [Building library](#building-library)
  * [Credits](#credits)

## Supported platforms ##

  * Windows
  * Linux
  * Mac OS X
  * Android (and Ouya)
  * iOS

## About LuaJava ##
LuaJava is a scripting tool for Java. The goal of this tool is to allow scripts written in Lua to manipulate components developed in Java.

It allows Java components to be accessed from Lua using the same syntax that is used for accessing Lua`s native objects, without any need for declarations or any kind of preprocessing. LuaJava also allows Java to implement an interface using Lua. This way any interface can be implemented in Lua and passed as parameter to any method, and when called, the equivalent function will be called in Lua, and it's result passed back to Java.

## Building ##

To compile and pack both natives and library, execute:

```shell
ant
```

This will create `libs/` directory with build results.

### Building natives ###

To compile and pack natives for all platforms:

```shell
ant natives
```

To only compile natives:

```shell
ant compile-natives
```

To only pack natives:

```shell
ant pack-natives
```

To clean natives

```shell
ant clean-natives
```

To compile or pack natives only for specified platform (for example for Linux), run specified ant target:

```shell
ant compile-linux
ant pack-linux
```

targets can be:

* linux
* windows
* macosx
* ios
* android

### Building library ###

To compile and pack java library:

```shell
ant library
```

To only compile java library:

```shell
ant compile-library
```

To only pack java library:

```shell
ant pack-library
```

To clean library

```shell
ant clean-library
```

## Credits ##

 * [LuaJava](https://github.com/jasonsantos/luajava)
 * [LibGDX](https://github.com/libgdx/libgdx)
 
This is mostly wrapper for LuaJava for cross-platform compatibility using also LibGDX SharedLibraryLoader for loading natives in cross-platform way.