#Metalcon POM

parental POM for Metalcon projects including

* organization Metalcon
* license
* Java 1.7 compiler plugin
* Metalcon deployment repository
* SSH extension to deploy via SCP

## Use in projects

You can inherit from the parental pom by adding

    <project ...>
      <parent>
        <groupId>de.metalcon</groupId>
        <artifactId>pom</artifactId>
        <version>0.0.1</version>
      </parent>
      
      ...
    </project>

to the head of your pom file.

To use the parental pom you have to add the Metalcon repository:

    <project ...>
      ...
      <repositories>
        <!-- Metalcon repository to resolve dependencies from -->
        <repository>
          <id>metalcon-depend</id>
          <url>http://metalcon2.physik.uni-mainz.de:8080/mvn/</url>
        </repository>
      </repositories>
      ...
    </project>

See https://github.com/renepickhardt/metalcon/wiki/technologyMaven for more information about the usage of Maven and deployment in particular.

## Versions

The versions for plugins and extensions are tried to be set to the latest one. Nevertheless you can overwrite them by settings the respective variable.

| Type      | Artifact              | Version | Variable |
| --------- | --------------------- | ------- | -------- |
| Plugin    | maven-compiler-plugin | 3.1     | java.compiler-plugin.version |
| Plugin    | maven-javadoc-plugin  | 2.9.1   | java.javaDoc-plugin.version |
| Extension | wagon-ssh             | 2.6     | maven.ssh-extension.version |
