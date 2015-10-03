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

## Devices
![iPhone/iPod touch models](https://cloud.githubusercontent.com/assets/291371/3639182/e89de91a-1070-11e4-862e-fa46161e3db7.png)

![iPad/iPad Mini models](https://cloud.githubusercontent.com/assets/291371/3639183/ec126d50-1070-11e4-876f-e3cd692756ac.png)

These images were created by using the Chrome developer tools to remove all the rows except these on the Wiki page, and then screenshotting it.

## License
This is released into the public domain under the [Unlicense](http://unlicense.org/). This information is publicly available.
