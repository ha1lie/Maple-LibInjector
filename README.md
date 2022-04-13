#  Maple-LibInjector

An executable listener designed for code-injection. Eventually going to listen for multiple Bundle IDs to inject variable dylibs into.

## Usage

*Current usage*: `./Maple-LibInjector <bundle-id> <injectable.dylib>`
Desired usage: `./Maple-LibInjector <maple-listen-file>`

- This would allow the listener to inject into one process using one centralized listener, opposed to a multitude of the same process running on a target machine  

## Maple Listen File Format

`
<bundle-id> <dylib-path>
<bundle-id> <dylib-path>
...
...
` 

Based on [repo by @kabiroberai](https://http://github.com/kabiroberai/LibraryInjector/), who's README contents is below 👇

Load a library into newly spawned processes using EndpointSecurity.

Based on [this gist](https://gist.github.com/saagarjha/a70d44951cb72f82efee3317d80ac07f) by Saagar Jha.
