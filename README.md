[![Docker Stars](https://img.shields.io/docker/stars/yogihardi/alpine-oraclejdk7.svg?style=flat-square)](https://hub.docker.com/r/yogihardi/alpine-oraclejdk7/)
[![Docker Pulls](https://img.shields.io/docker/pulls/yogihardi/alpine-oraclejdk7.svg?style=flat-square)](https://hub.docker.com/r/yogihardi/alpine-oraclejdk7/)


OracleJDK 7 Docker image
========================

This image is based on Alpine Linux image, which is only a 5MB image, and contains
[OracleJDK 7](http://www.oracle.com/technetwork/java/javase/overview/index.html).


Consider using `develar/java` image (~120MB) if you only need JRE (you can run
java applications, but cannot build/compile them).


Usage Example
-------------

```bash
$ echo 'public class Main { public static void main(String[] args) { System.out.println("Hello World"); } }' > Main.java
$ docker run --rm -v "$(pwd)":/mnt --workdir /mnt yogihardi/alpine-oraclejdk7 sh -c "javac Main.java && java Main"
```

Once you have run this command you will get printed 'Hello World' from Java!
