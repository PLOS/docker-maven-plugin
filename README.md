Docker Maven Plugin
===================

This Maven plugin attaches a shutdown hook to the jvm which stops and removes
the Docker instance used in NED's build process (neddb).

Build/Deploy (Local Maven Repo)
-------------------------------

    mvn clean install

Deploy (Ambra Maven Repo)
-------------------------

    mvn deploy

Here the url to browse [Ambra repo](http://maven.ambraproject.org/maven2/release/)

To use the Docker Maven Plugin artifact in the Ambra Maven repository in a
project, add these dependency and repository sections to pom.xml.

  <dependency>
    <groupId>org.plos.maven</groupId>
    <artifactId>docker-maven-plugin</artifactId>
    <version>1.0.0</version>
  </dependency>
  ...
  <repositories>
    <repository>
      <id>ambra</id>
      <name>Maven 2 Release Repository for Ambra</name>
      <url>http://maven.ambraproject.org/maven2/release/</url>
      <releases>
        <enabled>true</enabled>
      </releases>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
    </repository>
  </repositories>

Testing
-------

You can test the shutdown hook by running the docker mojo tester script. You'll
need to update the CLASSPATH - see script for details.

    ./docker-mojo-tester.sh
