﻿# Using PKI Express on Java

This articles describes how to use [PKI Express](../index.md) on Java

## Samples project

The samples project shows the usage of PKI Express together with the [Web PKI](../../web-pki/index.md) browser component
on a **Java 7+** web application (including 8 and 9) using the [Spring MVC](http://spring.io/) framework. It is hosted on GitHub:

https://github.com/LacunaSoftware/PkiSuiteSamples/tree/master/java/springmvc

> [!NOTE]
> If you are using a previous version of Java, please [contact us](https://www.lacunasoftware.com/en/home/purchase).

### Running the project

To run the project, it's necessary to have the Java Development Kit installed. You can use the following tools:

**Using Gradle**

1. [Install PKI Express](../setup/index.md)

1. [Download the project](https://github.com/LacunaSoftware/PkiSuiteSamples/archive/master.zip) or clone the [repository](https://github.com/LacunaSoftware/PkiSuiteSamples.git)

1. In a command prompt, navigate to the folder `Java` and run the command `gradlew bootRun` (on Linux `./gradlew bootRun`).
   If you are using Windows, you can alternatively double-click the file `Run-Sample.bat`

1. Once you see the message "Started Application in x.xxx seconds" (the on-screen percentage
   will *not* reach 100%), open a web browser and go the URL http://localhost:60695/

> [!NOTE]
> If you are on Linux, you may have to add the execution permission to *gradlew* file by executing the command `chmod +x gradlew`.

**Using Maven**

1. [Install PKI Express](../setup/index.md)

1. [Download the project](https://github.com/LacunaSoftware/PkiSuiteSamples/archive/master.zip) or clone the [repository](https://github.com/LacunaSoftware/PkiSuiteSamples.git)

1. In a command prompt, navigate to the folder `Java` and run the command `mvn spring-boot:run`. To run the command, it's 
necessary to have the Apache Maven installed.

1. Once you see the message "Started Application in x.xxx seconds" (the on-screen percentage
   will *not* reach 100%), open a web browser and go the URL http://localhost:60695/

## Maven package

In order to use PKI Express on Java you must include the Maven package [pki-express](https://search.maven.org/artifact/com.lacunasoftware.pkiexpress/pki-express)

If your project uses **Maven**, add this to your `pom.xml`:

[!include[pom.xml](../../../../includes/pki-express/java/maven.md)]

If your project uses **Gradle**, add this to your `build.gradle`:

[!include[build.gradle](../../../../includes/pki-express/java/gradle.md)]

The package is open-source, hosted on [GitHub](https://github.com/LacunaSoftware/PkiExpressJava). Feel free to fork it if you need to make any customizations, and even submit and *pull request*.

## See also

* [Signature sample explained](how-it-works.md)
