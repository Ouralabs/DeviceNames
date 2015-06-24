# Device Names
A list of iOS and Android devices seen from our logging service which has managed > 10mm devices globally. The values are mapped by what is reported by the OS of each platform. See below for each platform.

## Android
The values are mapped by:
```java
Build.MODEL
```

Append Build.MANUFACTURER to get the full device model.

## iOS
The values are mapped by:
```objc
+ (NSString *)model {
    struct utsname systemInfo;
    uname(&systemInfo);
    
    return [NSString stringWithCString:systemInfo.machine encoding:NSUTF8StringEncoding];
}
```
