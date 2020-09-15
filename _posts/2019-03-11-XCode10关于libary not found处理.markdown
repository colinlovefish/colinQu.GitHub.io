---
layout: post
title:  "XCode10关于library not found for -lstdc++.6.0.9 处理"
date:   20190311 15:30:51 +0800
categories: yinghu update
---


请将将以下命令中 Xcode9xxxx.app 改成你Xcode9的自定义名字
真机
```
sudo cp /Applications/Xcode9xxxx.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/lib/libstdc++.6.0.9.tbd /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/lib/libstdc++.6.0.9.tbd
```

模拟器

```
sudo cp /Applications/Xcode9xxxx.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator.sdk/usr/lib/libstdc++.* /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator.sdk/usr/lib/
```

替换完成后,替换完成后在模拟器iOS10.0以上运行会出现一个错误：

```
Reason: no suitable image found.  Did find:
/usr/lib/libstdc++.6.dylib: mach-o, butnotbuiltforiOS simulator
```

执行以下命令,拷贝进去之后将名字改成libstdc++.6.dylib
```
sudo cp /Applications/Xcode9xxxx.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/CoreSimulator/Profiles/Runtimes/iOS.simruntime/Contents/Resources/RuntimeRoot/usr/lib/libstdc++.6.0.9.dylib /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/CoreSimulator/Profiles/Runtimes/iOS.simruntime/Contents/Resources/RuntimeRoot/usr/lib
```


