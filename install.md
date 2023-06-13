# Install a java sdk on your machine

Java is a popular programming language that allows you run programs on many platforms, including Fedora. If you want to create Java programs, you need to install a JDK (Java Development Kit).

There are 2 main sdk for java

OpenJDK — an open-source implementation of the Java Platform, Standard Edition. This version is preferred, and included in Fedora.

Oracle Java SE — a free JDK from Oracle. This version is not open-source and we recommend that it only be used if OpenJDK is not sufficient.

To install OpenJDK from the Fedora repository run the following command to list available versions:

```bash
dnf search openjdk
```

But since doing this is too boring, just type the following command to install OpenJDK :

```bash
sudo dnf install java-17-openjdk-devel.x86_64
```

Wait for the installation to finish and... There we go! Now we're ready to program in Java!
