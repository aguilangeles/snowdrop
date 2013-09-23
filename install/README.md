Snowdrop Installer
==================

Purpose
--------

To enable ease of installation of the snowdrop module in the standalone version of EAP.

What-it-does
------------

It copies the necessary snowdrop and spring jars in their proper location within ${JBOSS_HOME}/modules.

It also modifies the standalone.xml and registers the snowdrop extension and subsystem, removing the need for manual installation.

How-to-use
-----------

_NOTE: Make sure to pass in -DJBOSS_HOME=/path/to/EAP installation_

_NOTE: If you are installing a non released version, be sure to mvn clean install on the top level._

_NOTE: If you are installing on Windows you will need to reverse the slashes._

Simply, run:

		mvn package -DJBOSS_HOME=/path/to/jboss_home

By default snowdrop version 3.0.1.Final and spring 3.2.4.RELEASE will be installed. To change this simply execute:

		mvn package -P${desired-spring-version} -DJBOSS_HOME=/path/to/jboss_home -Dversion.snowdrop=${desired-snowdrop-version}

There are four possible spring version profiles: spring-2.5, spring-3, spring-3.1, and spring-3.2 (the default).
