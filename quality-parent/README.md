## How To Get Started

Add the quality-parent as parent to your project:

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<artifactId>your-project</artifactId>
	<version>0.0.1</version>

	<parent>
		<groupId>nl.jam</groupId>
		<artifactId>quality-parent</artifactId>
		<version>{latest.version}</version>
	</parent>
</project>
```

## How Does It Work

Everytime you start a maven build your project will be checked:

* Ensure the build is started with jdk 1.8
* Ensure all (transitive) dependencies are compatible with ${project.compile.jdk}
* Check for java compile warnings and errors
* Correct use of dependencies and there scopes
* Run all unit and integration tests
* Check style (based on the Build tools project)
* Check for PMD warnings (based on the Build tools project)
* Check for FindBugs warnings (based on the Build tools project)
* Check code coverage

## How Do I Skip It

Run maven without the quality profile, add -P!quality to your command.
