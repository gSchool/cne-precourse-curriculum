# Step 2: Git and Java

Fork and Clone https://github.com/gSchool/cne-precourse-drills

> REFERENCE: https://help.github.com/articles/fork-a-repo/

Once you have cloned the repo, `cd` into the `cne-precourse-drills` directory, then run the following:

```
./gradlew assemble
java -jar build/libs/cne-precourse-drills.jar
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

Create a new file, and copy and paste the output into a new file called `system-properties.json`.  

Your file structure should now look like this:

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

Add, commit and push your changes in Git.  

> REFERENCE: https://help.github.com/articles/adding-a-file-to-a-repository-using-the-command-line/
