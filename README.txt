site: https://sites.google.com/site/beigesoftware

Part of Apache Tomcat and JSTL to precompile JSP/JSTL for A-Jetty (Jetty 9.2 adapted for Android).

Version 1.0.5:
Added JAR signing.
Fixed crossplatform file.separator.


All you need to precompile JSP/JSTL for A-Jetty is:
1. assemble A-Tomcate:
  *install a-javabeans and a-tomcat-all with Apache Maven
  *create folder a-apache-tomcat
  *copy a-tomcat-all/a-apache-jspc/target/a-apache-jspc-jar-with-dependencies.jar into folder a-apache-tomcat
  *copy a-tomcat-all/a-apache-jspc/src/main/resources/catalina-tasks.xml into folder a-apache-tomcat
  *add path a-apache-tomcat to environment variables as TOMCATA_HOME
2. Use standard way (ANT task, Apache Ant should be installed) to precompile your JSP/JSTL:
  *Copy a-jetty-all/webapp-test/build.xml into your Maven web-app project then run there:
    $ANT_HOME/bin/ant -Dtomcat.home=$TOMCATA_HOME -Dwebapp.path=target/[your-project-name]/

See https://github.com/demidenko05/beige-software beige-accounting-ajetty for example

Licenses:

The Apache Software License, Version 2.0
http://www.apache.org/licenses/LICENSE-2.0.txt

3-d party:

Eclipse JDT
The Eclipse Public License, Version 1.0
http://www.eclipse.org/legal/epl-v10.html

Oracle JEE (Servlet API...)
CDDL + GPLv2 with classpath exception
https://javaee.github.io/glassfish/LICENSE

https://github.com/demidenko05/a-javabeans8 - adapted OpenJDK8 javabeans for Android:
GNU General Public License, version 2, with the Classpath Exception
http://openjdk.java.net/legal/gplv2+ce.html

