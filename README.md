# Spring for Android

[Spring for Android] is an extension of the [Spring Framework] that aims to simplify the development of native [Android] applications.


## Downloading artifacts

The [Android Maven Plugin] makes it possible to build Android applications utilizing the power of Maven dependency management. See [downloading Spring artifacts] for Maven repository information. Unable to use Maven or other transitive dependency management tools? See [building a distribution with dependencies].


### Dependencies

Spring for Android consists of three modules: Core, Rest Template, and Auth.

```xml
<dependency>
    <groupId>org.springframework.android</groupId>
    <artifactId>spring-android-core</artifactId>
    <version>${org.springframework.android-version}</version>
</dependency>

<dependency>
    <groupId>org.springframework.android</groupId>
    <artifactId>spring-android-rest-template</artifactId>
    <version>${org.springframework.android-version}</version>
</dependency>

<dependency>
    <groupId>org.springframework.android</groupId>
    <artifactId>spring-android-auth</artifactId>
    <version>${org.springframework.android-version}</version>
</dependency>
```

### Repositories

```xml
<repository>
	<id>spring-repo</id>
	<name>Spring Repository</name>
	<url>http://repo.springsource.org/release</url>
</repository>	
	
<repository>
	<id>spring-milestone</id>
	<name>Spring Milestone Repository</name>
	<url>http://repo.springsource.org/milestone</url>
</repository>

<repository>
	<id>spring-snapshot</id>
	<name>Spring Snapshot Repository</name>
	<url>http://repo.springsource.org/snapshot</url>
</repository>
```

## Documentation

See the current [Javadoc] and [reference docs].


## Sample Applications

Several example projects are available in the [samples repository].


## Issue Tracking

Report issues via the [Spring Android JIRA]. While JIRA is preferred, [GitHub issues] are also welcome. Understand our issue management process by reading about [the lifecycle of an issue].


## Build from Source

1. Clone the repository from GitHub:

		$ git clone git://github.com/SpringSource/spring-android.git

2. Navigate into the cloned repository directory:

		$ cd spring-android

3. The project uses [Gradle] to build:

		$ ./gradlew build
		
4. Install jars into your local Maven cache (optional)

		$ ./gradlew install


## Import Source into your IDE

### Eclipse

1. To generate Eclipse metadata (.classpath and .project files):

		$ ./gradlew eclipse

2. Once complete, you may then import the projects into Eclipse as usual:

		File -> Import -> Existing projects into workspace

	_Note: [SpringSource Tool Suite] has built in support for [Gradle], and you can simply import as Gradle projects._

### IDEA

Generate IDEA metadata (.iml and .ipr files):

	$ ./gradlew idea


## Tests

There are three Android Test Projects located in the "test" folder of the repository that correspond to the three Spring for Android Modules (Core, Rest Template, and Auth). These projects are executed separately from the Gradle build process. To run the suite of tests, perform the following steps. The parent POM located in the root of the "test" folder will execute each test project on all attached devices and emulators.

1. Build Spring for Android JARs and install them to the local Maven repository:

		$ ./gradlew build install

2. The tests are run using the [Android Maven Plugin]:

		$ mvn -f ./test/pom.xml clean install

	_Note: Each test project can also be executed individually, by running the previous command from within the respective test project's directory._


## Contributing

[Pull requests] are welcome. See the [contributor guidelines] for details.


## License

Spring Mobile is released under version 2.0 of the [Apache License](http://www.apache.org/licenses/LICENSE-2.0).


[Spring for Android]: http://www.springsource.org/spring-android
[Spring Framework]: http://www.springsource.org/spring-framework
[Android]: http://developer.android.com/index.html
[Android Maven Plugin]: http://code.google.com/p/maven-android-plugin
[downloading Spring artifacts]: https://github.com/SpringSource/spring-framework/wiki/Downloading-Spring-artifacts
[building a distribution with dependencies]: https://github.com/SpringSource/spring-framework/wiki/Building-a-distribution-with-dependencies
[Javadoc]: http://static.springsource.org/spring-android/docs/1.0.x/api/
[reference docs]: http://static.springsource.org/spring-android/docs/1.0.x/reference/html/
[samples repository]: https://github.com/SpringSource/spring-android-samples
[Spring Android JIRA]: http://jira.springsource.org/browse/ANDROID
[GitHub issues]: https://github.com/SpringSource/spring-android/issues?direction=desc&sort=created&state=open
[the lifecycle of an issue]: https://github.com/cbeams/spring-framework/wiki/The-Lifecycle-of-an-Issue
[Gradle]: http://gradle.org
[SpringSource Tool Suite]: http://www.springsource.com/developer/sts
[Pull requests]: http://help.github.com/send-pull-requests
[contributor guidelines]: https://github.com/SpringSource/spring-android/wiki/Contributor-Guidelines



