# buildscripts for homeean

[**homeean**](https://himpler.com/homeean) is a web based buildtool, which generates an individual buildscript (Bash-Script) for user selected Smart Home Tools to be installed on a Raspberry Pi running on Raspbian. 

These tools are mainly provided for the use with the Smart Home Gateway [**homee**](https://hom.ee) in order to extend its functionality and provide interfaces to other tools & standards. 

Target group for homeean are users with limited knowledge of Linux system administration.

The name "homeean" has been chosen as a tribute to [**Debian**](https://www.debian.org) (forefather of [**Raspbian**](https://www.raspian.org)) and homee.

homeean is intentionally always written in lower case (as is homee), even at the beginning of a sentence ;-) 

## contributing
Contributions are welcome, wether you provide a new script or update a existing one. Please push only tested packages to the master branch, since every commit is pulled frequently by the web based build tool.

### folders and filenames
The files are organized in folders. The foldernames are in **kebab case**, i.e. `harmony-api`. Each folder contains at least two files
- **commands.sh**  with the bash commands to install the package (without dependencies to other packages)
- **description.md** with a short description of the package

### dependencies
To ensure that every package is only installed once, homeean includes a dependency manager. To add dependencies create a `dependencies.json` with an array of package names in your folder. The packages must be already included in homeean.

```
// dependencies.json example

[
    "node-js",
    "git",
    "harmony-api"
]
```
