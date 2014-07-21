node-ios-devices
================

A JSON object mapping iOS device model codes (e.g. iPad2,1) to their respectively marketing names (e.g. iPad 2).

The data is mainly sourced from the Wikipedia page [List of iOS devices](https://en.wikipedia.org/wiki/List_of_iOS_devices).

The following C code prints the device model code:
```c
#include <sys/sysctl.h>
size_t size;
sysctlbyname("hw.machine", NULL, &size, NULL, 0);
char result[size];
sysctlbyname("hw.machine", result, &size, NULL, 0);
printf("%s\n", result);

// result is a typical C string that can be passed to [NSString stringWithUTF8String:result];
```

## License
Do what you want, this is all available on the aforementioned Wiki page. Copyright 2014 Josh Oldenburg, released under the MIT license.
