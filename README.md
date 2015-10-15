node-ios-devices
================

A JSON object mapping iOS device model codes (e.g. iPad2,1) to their respectively marketing names (e.g. iPad 2).

The data is mainly sourced from [here](https://www.innerfence.com/howto/apple-ios-devices-dates-versions-instruction-sets).

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

Thanks to [vijaymadhavan](https://github.com/vijaymadhavan) for adding more detail to each row. (See pull request #2)

## License
This is released into the public domain under the [Unlicense](http://unlicense.org/). This information is publicly available.
