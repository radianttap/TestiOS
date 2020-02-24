## Xcode 11.4 b2

Error shown is:

> cdtool hash unarchiving error: The data isn’t in the correct format.

Raw output:

```
DataModelCompile /Users/aleck/Library/Developer/Xcode/DerivedData/TestiOS-bebrxokyqhikmuajbrznmrwqpmsq/Build/Products/Debug-watchsimulator/TestwatchOS\ Extension.appex/ /Users/aleck/dev/local/TestiOS/TestModel.xcdatamodeld (in target 'TestwatchOS Extension' from project 'TestiOS')
cd /Users/aleck/dev/local/TestiOS
/Applications/Xcode-beta.app/Contents/Developer/usr/bin/momc --sdkroot /Applications/Xcode-beta.app/Contents/Developer/Platforms/WatchSimulator.platform/Developer/SDKs/WatchSimulator6.2.sdk --watchsimulator-deployment-target 6.1 --module TestwatchOS_Extension /Users/aleck/dev/local/TestiOS/TestModel.xcdatamodeld /Users/aleck/Library/Developer/Xcode/DerivedData/TestiOS-bebrxokyqhikmuajbrznmrwqpmsq/Build/Products/Debug-watchsimulator/TestwatchOS\ Extension.appex/

cdtool hash unarchiving error: The data isn’t in the correct format.
/Users/aleck/dev/local/TestiOS/TestModel.xcdatamodeld/TestModel.xcdatamodel:: error: cdtool cannot compile [0]
```

## Xcode 11.3

Error shown is:

> Command DataModelCompile failed with a nonzero exit code

(It's the same error on Xcode 10.3)

Raw output:

```
DataModelCompile /Users/aleck/Library/Developer/Xcode/DerivedData/TestiOS-bebrxokyqhikmuajbrznmrwqpmsq/Build/Products/Debug-watchsimulator/TestwatchOS\ Extension.appex/ /Users/aleck/dev/local/TestiOS/TestModel.xcdatamodeld (in target 'TestwatchOS Extension' from project 'TestiOS')
cd /Users/aleck/dev/local/TestiOS
/Applications/Xcode-beta.app/Contents/Developer/usr/bin/momc --sdkroot /Applications/Xcode-beta.app/Contents/Developer/Platforms/WatchSimulator.platform/Developer/SDKs/WatchSimulator6.2.sdk --watchsimulator-deployment-target 6.1 --module TestwatchOS_Extension /Users/aleck/dev/local/TestiOS/TestModel.xcdatamodeld /Users/aleck/Library/Developer/Xcode/DerivedData/TestiOS-bebrxokyqhikmuajbrznmrwqpmsq/Build/Products/Debug-watchsimulator/TestwatchOS\ Extension.appex/

Command DataModelCompile failed with a nonzero exit code
```

The mentioned exit code is `13` (this is shown when using legacy build system)


