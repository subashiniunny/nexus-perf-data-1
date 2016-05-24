# Nexus Performance Test Suite data

This build produces data packages for Nexus Performance Test Suite.

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.takari.nexus.perf.data/parent/badge.svg?subject=io.takari.nexus.perf.data:parent)](https://maven-badges.herokuapp.com/maven-central/io.takari.nexus.perf.data/parent)

Excercised formats:
* [Apache Maven](maven/)
* [npm](npm/)

## Consuming deployed tarballs

Steps:
* Get Nexus up up running.
* Download latest `jar-with-dependencies.jar` from [![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.takari.nexus/nexus-perf/badge.svg?subject=Nexus%20Performance%20Suite)](https://maven-badges.herokuapp.com/maven-central/io.takari.nexus/nexus-perf)
* Download the required data package tarball (or the "all" one having all scenarios).
* Untar the "data" tarball, it will create a sub-directory from current working directory, example:
  ```
  $ tar xfvz nexus-perf-1.0.1-standard-data.tar.gz
  ```
* IF: your Nexus uses other baseUrl and/or port than default `http://localhost:8081/nexus`, you have to edit the "data" properties file and set `nexus.baseUrl` property accordingly:
  ```
  $ edit nexus-perf-1.0.1/perf.properties
  ```
* Run the perf suite JAR and point it at the "data" directory:
  ```
  $ java -jar nexus-perf-1.0.1-jar-with-dependencies.jar nexus-perf-1.0.1/
  ```
* The performance suite should run

