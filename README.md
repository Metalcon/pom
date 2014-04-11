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
        <version>0.0.2</version>
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

### Plugins & Extensions

The versions for plugins, extensions and dependencies are tried to be set to the latest one. Nevertheless you can overwrite them by settings the respective variable.

| Type      | Artifact              | Version | Variable |
| --------- | --------------------- | ------- | -------- |
| Plugin    | maven-compiler-plugin | 3.1     | java.compiler-plugin.version |
| Plugin    | exec-maven-plugin     | 1.2.1   | java.exec.version |
| Plugin    | maven-javadoc-plugin  | 2.9.1   | java.javaDoc-plugin.version |
| Extension | wagon-ssh             | 2.6     | maven.ssh-extension.version |

#### Java execution configuration

Set `java.exec.launcherClass` to specify the class containing the `main`-method you want to execute.  
If you need to pass arguments you have to add the plugin yourself and use its configuration fields.

### Dependencies

#### Testing

| Artifact | Version | Variable |
| -------- | ------- | -------- |
| junit    | 4.9     | junit.version |

#### Metalcon dependencies

| Artifact | Version | Variable |
| -------- | ------- | -------- |
| db-helper | 0.1.1  | metalcon.dbHelper.version |
| RequestDispatcher | 1.3.0 | metalcon.dispatcher.version |
| exceptions | 0.1.1 | metalcon.exceptions.version |
| json-pretty-printer | 0.0.1 | metalcon.jsonPrettyPrinter.version |
| muid     | 0.3.2   | metalcon.muid.version |
| testing | 0.0.2 | metalcon.testing.version |
| zmq-worker-helper | 0.4.0 | metalcon.zmqWorkerHelper.version |
| API |---|---|
| backend-api | 0.1.2 | metalcon.backendApi.version |
| image-gallery-server-api | 0.0.1 | metalcon.imageGalleryServer.api.version |
| like-server-api | 0.2.0 | metalcon.likeServer.api.version |
| music-streaming-server-api      | 0.1.0 | metalcon.musicStreamingServer.api.version |
| static-data-delivery-server-api | 0.1.3 | metalcon.staticDataDeliveryServer.api.version |
| url-mapping-server-api          | 0.4.0 | metalcon.urlMappingServer.api.version |
| Backend components |---|---|
| image-storage-server | 0.1.0 | metalcon.imageStorageServer.version |
| like-server | 0.3.0 | metalcon.likeServer.version |
| music-storage-server | 0.1.0 | metalcon.musicStorageServer.version |
