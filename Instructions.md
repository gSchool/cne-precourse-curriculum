# Instructions

## Installation

**Git**

Ensure that you have installed Git.  See https://help.github.com/articles/set-up-git/ for help.

To check if git is installed correctly run `git version`.  It should print something like:

```
git version 2.10.1
```

If you are on a Mac, consider using [Homebrew](http://brew.sh/) and running `brew install git`.

**Java**

Ensure that you have Java 8 JDK.  See https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html for help.

To check if Java 8 is installed correctly, run `java -version`.  It should print something like:

```
java version "1.8.0_05"
Java(TM) SE Runtime Environment (build 1.8.0_05-b13)
Java HotSpot(TM) 64-Bit Server VM (build 25.5-b02, mixed mode)
```

## Commit #1

Fork and Clone https://github.com/gschool/cnt-precourse-drills.  See this article for help on Forking projects https://help.github.com/articles/fork-a-repo/.

Once you have cloned the repo, `cd` into the `cnt-precourse-drills` directory, then run the following:

```
./gradlew clean build
java -jar build/libs/cnt-precourse-drills.jar
```

The output should look like this (but longer):

```json
{
  "java.runtime.name": "Java(TM) SE Runtime Environment",
  "sun.boot.library.path": "/Library/Java/JavaVirtualMachines/jdk1.8.0_05.jdk/Contents/Home/jre/lib",
  "java.vm.version": "25.5-b02",
  "gopherProxySet": "false",
  "ftp.nonProxyHosts": "local|*.local|169.254/16|*.169.254/16",
  "sun.cpu.isalist": ""
}
```

Create a new file, and copy and paste the output into a new file called `system-properties.json`.  Your file structure should now look like this:

```
.
├── README.md
├── build
├── build.gradle
├── gradle
├── gradlew
├── gradlew.bat
├── settings.gradle
├── src
└── system-properties.json
```

Add, commit and push your changes in Git.  See https://help.github.com/articles/adding-a-file-to-a-repository-using-the-command-line/ for help on how to do that.


## Commit #2
