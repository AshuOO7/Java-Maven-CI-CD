# Java-Maven-CI-CD

Here is a starter project for the ArcGIS Runtime SDK for Java with Maven.

The project includes the Maven wrapper, so there is no need to install Maven to run the app.

The app launches a window displaying a map.

![screenshot](screenshot.png)

## Instructions

### IntelliJ IDEA

1. Open IntelliJ IDEA and select _File > Open..._.
2. Choose the java-maven-starter-project directory and click _OK_.
3. Select _File > Project Structure..._ and ensure that the Project SDK and language level are set to use Java 11.
4. Open the Maven view with _View > Tool Windows > Maven_.
5. In the Maven view, under _Plugins > dependency_, double-click the `dependency:unpack` goal. This will unpack the native libraries into $USER_HOME/.arcgis.
6. In the Maven view, run the `compile` phase under _Lifecycle_ and then the `exec:java` goal to run the app.

### Eclipse

1. Open Eclipse and select _File > Import_.
2. In the import wizard, choose _Maven > Existing Maven Projects_, then click _Next_.
3. Select the java-maven-starter-project as the project root directory.
4. Click _Finish_ to complete the import.
5. Select _Project > Properties_ . In _Java Build Path_, ensure that under the Libraries tab, _Modulepath_ is set to JRE System Library (JavaSE-11). In _Java Compiler_, ensure that the _Use compliance from execution environment 'JavaSE-11' on the 'Java Build Path'_ checkbox is selected.
6. Right-click the project in the Project Explorer or Package Explorer and choose _Run As > Maven Build..._. In the _Edit Configuration_ dialog, create a new configuration with name `unpack`. In the _Goals_ field, enter `dependency:unpack`. Click _Run_ to run the goal. This will unpack the native libraries into $USER_HOME/.arcgis.
7. Again, create a new run configuration with name `run`. In the _Goals_ field, enter `compile exec:java`. Click _Run_ to run the goal. The app should compile and launch the JavaFX window.

### Command Line

1. `cd` into the project's root directory.
2. Run `./mvnw dependency:unpack` on Linux/Mac or `mvnw.cmd dependency:unpack` on Windows to unpack the native libraries to $USER_HOME/.arcgis.
3. Run `./mvnw compile exec:java` on Linux/Mac or `mvnw.cmd compile exec:java` on Windows to run the app.

## Requirements

See the Runtime SDK's [system requirements](https://developers.arcgis.com/java/reference/system-requirements/).

## Resources

* [ArcGIS Runtime SDK for Java](https://developers.arcgis.com/java/)  
* [ArcGIS Blog](https://blogs.esri.com/esri/arcgis/)  
* [Esri Twitter](https://twitter.com/esri)  
