# TestiOS

A sample to show watchOS appp with CoreData issue on [AMD-based Hackintoshes](https://github.com/radianttap/EFI-ASRock-X570-ITX-iMacPro1-1) (`cdtool` crashes). 

See `issues.md` for example of the crash or simply build the test targets and look for cdtool crashes in Console.app

**Update**: tested this same project on BigSur beta 5, using Xcode 12 beta 6 and it compiles just fine. Even tried a *much* larger project with iOS / watchOS targets both using Core Data and that also compiled properly. Xcode 11.7 on that same Big Sur throws same cdtool error, thus it seems this is some obscure issue in watchOS 6.x SDKs.
