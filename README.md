#  Maple-LibInjector

An executable listener designed for code-injection. Eventually going to listen for multiple Bundle IDs to inject variable dylibs into.

## Usage
`./Maple-LibInjector <maple-listen-file>`

- Allows the listener to look for up to 100 bundle IDs 

## Maple Listen File Format
Ex: `example-listen.txt`, which injects libTestLib.dylib(stored in the same folder as `Maple-LibInjector` into Messages and Calculator apps)
`
<bundle-id> <dylib-path-from-source-folder>
<bundle-id> <dylib-path-rom-source-folder>
...
...
` 

## Limitations 

As of currently, this listener cannot watch for more than 100 BIDs. If this behavior is desired, we will have to adapt this script for more. 
*I am not a C++ developer. This script is possibly not secure as of this time. I will look into this at some point in the future. For now, it works*

Based on [repo by @kabiroberai](https://http://github.com/kabiroberai/LibraryInjector/), who's README contents is below 👇

Load a library into newly spawned processes using EndpointSecurity.

Based on [this gist](https://gist.github.com/saagarjha/a70d44951cb72f82efee3317d80ac07f) by Saagar Jha.
