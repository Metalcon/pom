#Metalcon POM

parental POM for Metalcon projects including

* organization Metalcon
* license
* Java 1.7 compiler plugin
* Metalcon deployment repository
* SSH extension to deploy via SCP

## Use in projects

You can inherit from the parental pom by adding

    <parent>
      <groupId>de.metalcon</groupId>
      <artifactId>pom</artifactId>
      <version>0.0.1</version>
    </parent>

to the head of your pom file.

To use the parental pom you have to add the Metalcon repository:

    <!-- Metalcon repository to resolve dependencies from -->
    <repository>
      <id>metalcon-depend</id>
      <url>http://metalcon2.physik.uni-mainz.de:8080/mvn/</url>
    </repository>

See https://github.com/renepickhardt/metalcon/wiki/technologyMaven for more information about the usage of Maven and deployment in particular.
