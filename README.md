# boardcad-java

Setup for Windows
=================

Install JDK:

http://www.oracle.com/technetwork/java/javase/downloads/index.html

Build

Compile trunk:

```
javac -encoding ISO-8859-1 -classpath ".;j3dcore.jar;j3dutils.jar;vecmath.jar;jogl-all.jar;gluegen-rt.jar" cadcore/*.java board/*.java board/readers/*.java board/writers/*.java boardcad/*.java boardcad/i18n/*.java boardcad/export/*.java boardcad/gui/jdk/plugin/*.java boardcad/gui/jdk/*.java boardcad/print/*.java boardcad/settings/*.java boardcam/*.java boardcam/cutters/*.java boardcam/holdingsystems/*.java boardcam/toolpathgenerators/*.java boardcam/readers/*.java boardcam/writers/*.java
```

Execute:

```
java -classpath ".;j3dcore.jar;j3dutils.jar;vecmath.jar;jogl-all.jar;gluegen-rt.jar;jython.jar;Lib.jar;jythonconsole.jar" boardcad.gui.jdk.BoardCAD
```

Deploy

Create jar file:

```
jar cvmf mymanifest BoardCAD.jar cadcore/*.class board/*.class board/readers/*.class board/writers/*.class boardcad/*.class boardcad/i18n/* boardcad/icons/* boardcad/export/*.class boardcad/gui/jdk/plugin/*.class boardcad/gui/jdk/*.class boardcad/print/*.class boardcad/settings/*.class boardcam/*.class boardcam/cutters/*.class boardcam/holdingsystems/*.class boardcam/toolpathgenerators/*.class boardcam/readers/*.class boardcam/writers/*.class
```

Signing jar file:

```
jarsigner -keystore newkey BoardCAD.jar boardcad
```

Password=boardcad

Execute jar file:

```
java -jar BoardCAD.jar
```

Setup for Ubuntu
================

Install JDK:

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java7-installer
```

Build

Compile trunk:

```
javac -encoding ISO-8859-1 -classpath ".:j3dcore.jar:j3dutils.jar:vecmath.jar:jogl-all.jar:gluegen-rt.jar" cadcore/*.java board/*.java board/readers/*.java board/writers/*.java boardcad/*.java boardcad/i18n/*.java boardcad/export/*.java boardcad/gui/jdk/plugin/*.java boardcad/gui/jdk/*.java boardcad/print/*.java boardcad/settings/*.java boardcam/*.java boardcam/cutters/*.java boardcam/holdingsystems/*.java boardcam/toolpathgenerators/*.java boardcam/readers/*.java boardcam/writers/*.java
```

Execute:

```
java -classpath ".:gluegen-rt.jar:j3dcore.jar:j3dutils.jar:jogl-all.jar:vecmath.jar:jython.jar:Lib.jar:jythonconsole.jar" boardcad.gui.jdk.BoardCAD
```

Deploy

Create jar file:

```
jar cvmf mymanifest BoardCAD.jar cadcore/*.class board/*.class board/readers/*.class board/writers/*.class boardcad/*.class boardcad/i18n/* boardcad/icons/* boardcad/export/*.class boardcad/gui/jdk/plugin/*.class boardcad/gui/jdk/*.class boardcad/print/*.class boardcad/settings/*.class boardcam/*.class boardcam/cutters/*.class boardcam/holdingsystems/*.class boardcam/toolpathgenerators/*.class boardcam/readers/*.class boardcam/writers/*.class
```

Execute jar file:

```
java -jar BoardCAD.jar
```
