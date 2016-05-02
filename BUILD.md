# Building the Linked Data Studio
This document describes the steps to build the Linked Data Studio.
## Prerequisites
You should have build the [Linked Data Theatre](https://github.com/architolk/Linked-Data-Theatre).

## Dependancy on open source components
The Linked Data Studio depends on a couple of open source components:

1. The Linked Data Theatre, and its open source depedencies;
2. MorphRDB.

## Build proces
The Linked Data Studio consists of three components:

1. The original Linked Data Theatre
2. Java source code, for custom Orbeon processors
3. Orbeon app (mainly XPL and XSL source code), as an extension of the LDT.

### Install the Linked Data Theatre dependency
The LDS is configured to have a dependency with the LDT, so you need to install the LDT in your local maven repository, by performing the following steps:

1. Got to your local copy of the linked data theatre;
2. Execute: `mvn install`.

Please notice that your version of the LDT should correspond with the depedency in the pom.xml file of the LDS!

### Build the java source code
To build the java source code perform the following steps (only ones):

1.	Go to \morphrdb and execute: `mvn package`
2.	Go to \processors and execute `maven-install-morphrdb.bat` following by `mvn clean install`

### Orbeon app
You should only perform this step after all other steps!
To build the full orbeon app (including the orbeon code):

1.	Go to the root directory of the Linked Data Studio.
2.	Execute: `mvn clean package`. 
