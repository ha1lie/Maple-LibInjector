# Maple-LibInjector
---

A sub-utility combined with the [Maple](https://github.com/ha1lie/Maple) suite used to customize your Mac via Runtime Injection. This script is responsible for loading Dynamic Libraries when a specific application or daemon is launched.

This program utilizes the [EndpointSecurity](https://developer.apple.com/documentation/endpointsecurity) framework by Apple. As originally implemented, this framework was developed to help limit malware. In our case, we're using it to bypass exactly that.

#### Not what you were looking for?

[Check out Maple](https://github.com/ha1lie/Maple) 
[Check out MapleKit](https://www.google.com)
[Check out my whole GitHub](https://github.com/ha1lie)

## Credits
---

The original script was created by [@kabiroberai](https://github.com/kabiroberai). I credit basically this entire project, including the entirety of [Maple](https://github.com/ha1lie/Maple) to him, as without his work on both LibInjector and Orion, the project will not exist. 

I simply transformed this script to be able to listen for more than one binary, and control which Dynamic Library is injected. 

## Usage
---

`./Maple-LibInjector <maple-listen-file>`

- Allows the listener to look for up to 100 bundle IDs 

## Maple Listen File Format
---

Ex: `listen.txt`, which injects `libTestLib.dylib` into com.apple.MobileSMS(The Messages App) and `newCalcColor.dylib` into com.apple.calculator(The Mac's Calculator App)

    com.apple.MobileSMS ./libTestLib.dylib
    com.apple.calculator ./newCalcColor.dylib

## Limitations 
---

As of currently, this listener cannot watch for more than 100 BIDs. If this behavior is desired, we will have to adapt this script for more. 
*I am not a C++ developer. This script is possibly not secure as of this time. I will look into this at some point in the future. For now, it works*

---

Based on [repo by @kabiroberai](https://github.com/kabiroberai/LibraryInjector/), who's README contents is below 👇

Load a library into newly spawned processes using EndpointSecurity.

Based on [this gist](https://gist.github.com/saagarjha/a70d44951cb72f82efee3317d80ac07f) by Saagar Jha.
