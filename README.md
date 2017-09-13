Docker Maven Plugin
===================

This Maven plugin attaches a shutdown hook to the jvm which stops and removes
the Docker instance used in the testing phase of the Maven lifecycle.

Building
--------

    mvn clean package

Deploying
---------

To install plugin in local Maven repo.

    mvn install

To install plugin in Ambra Maven repo - only versioned artifacts (ie, not snapshots)
can be deployed to this repo.

    mvn deploy

Here is the url to browse [Ambra repo](http://maven.ambraproject.org/maven2/release/)

Testing
-------

You can test the shutdown hook by running the docker mojo tester script. You'll
need to update the CLASSPATH - see script for details.

    ./docker-mojo-tester.sh
