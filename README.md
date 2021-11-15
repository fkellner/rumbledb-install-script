# RumbleDB Install Script

The (probably) fastest way to try out [RumbleDB](https://github.com/RumbleDB/rumble) on your Linux machine. Downloads all JARs into a folder, exposes REPL and file input as
bash commands, and includes an uninstaller that cleans everything up
if needed.

## How to use it

```bash
# Download
wget https://raw.githubusercontent.com/fkellner/rumbledb-install-script/main/install-rumbledb.sh

# Make executable
chmod +x install-rumbledb.sh

# Check if everything is setup okay
./install-rumbledb.sh --help

# Run
./install-rumbledb.sh
```

## What it does

- Downloads Apache Spark and RumbleDB
- If run on a debian-based system (with `apt-get` available), it also installs Java 8 JRE from OpenJDK if no Java version is present
- Creates a RumbleDB REPL script `rumble-repl` and a RumbleDB File execution script `rumble-file`
- Scripts are added to PATH via an edit to ~/.bashrc
- Everything, including an uninstaller, will be stored in `$HOME/RumbleDB`
- Versions of Apache Spark, Hadoop and RumbleDB as well as the Install Path are variables that can be edited

## What it does not do

- This script was generated to help students to get RumbleDB up and running quickly for some simple queries as homework for a course. I do not know if this setup works for any professional use case.
- Files are not moved to POSIX-compliant locations. I'm happy about any input on that. However, this was never intended to serve as professional packaging like a `.deb`-Package.
- Automatically install Java 8 if there is another version of Java present. **RumbleDB recommends versions 8 or 11!**

## Contributing

I am happy about any feedback, be it an issue or pull request.
