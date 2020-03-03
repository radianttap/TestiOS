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

This generates crash report, which can be seen in Console app, here's one:

```
Process:               cdtool [11877]
Path:                  /Applications/Xcode-beta.app/Contents/Developer/Platforms/WatchSimulator.platform/Developer/Library/Xcode/Agents/cdtool
Identifier:            cdtool
Version:               ???
Code Type:             X86 (Native)
Parent Process:        momc [11869]
Responsible:           Xcode [11834]
User ID:               501

Date/Time:             2020-03-03 20:25:44.124 +0100
OS Version:            Mac OS X 10.15.4 (19E242d)
Report Version:        12
Anonymous UUID:        F8EB5E4B-A1AF-89D7-864D-FD95B5D04987


Time Awake Since Boot: 86000 seconds

System Integrity Protection: enabled

Crashed Thread:        Unknown

Exception Type:        EXC_BAD_INSTRUCTION (SIGILL)
Exception Codes:       0x0000000000000001, 0x0000000000000000
Exception Note:        EXC_CORPSE_NOTIFY

Termination Signal:    Illegal instruction: 4
Termination Reason:    Namespace SIGNAL, Code 0x4
Terminating Process:   exc handler [11877]

Backtrace not available

Unknown thread crashed with X86 Thread State (32-bit):
eax: 0x000800b1  ebx: 0x0009d001  ecx: 0xbff876ac  edx: 0x000f63c6
edi: 0x0009e087  esi: 0x000f4bea  ebp: 0xbff876d8  esp: 0xbff876ac
ss: 0x00000023  efl: 0x00010296  eip: 0x000f6a8b   cs: 0x0000001b
ds: 0x00000023   es: 0x00000023   fs: 0x00000000   gs: 0x00000000
cr2: 0x000f63bc

Logical CPU:     6
Error Code:      0x00000000
Trap Number:     6


Binary images description not available


External Modification Summary:
Calls made by other processes targeting this process:
task_for_pid: 0
thread_create: 0
thread_set_state: 0
Calls made by this process:
task_for_pid: 0
thread_create: 0
thread_set_state: 0
Calls made by all processes on this machine:
task_for_pid: 45888
thread_create: 0
thread_set_state: 0
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


