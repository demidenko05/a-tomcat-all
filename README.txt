Part of Apache Tomcat and JSTL to precompile JSP/JSTL for A-Jetty (Jetty 9.2 adapted for Android).

All you need to precompile JSP/JSTL for A-Jetty is:
1. assemble A-Tomcate:
  *install a-javabeans, a-tomcat-all, create folder a-apache-tomcat
  *copy a-tomcat-all/a-apache-jspc/target/a-apache-jspc-jar-with-dependencies.jar into folder a-apache-tomcat
  *copy a-tomcat-all/a-apache-jspc/src/main/resources/catalina-tasks.xml into folder a-apache-tomcat
  *add path a-apache-tomcat to environment variables as TOMCATA_HOME
2. Use standard way (ANT task) to precompile your JSP/JSTL:
  *Copy a-jetty-all/webapp-test/build.xml into your Maven web-app project then run there "$ANT_HOME/bin/ant -Dtomcat.home=$TOMCATA_HOME -Dwebapp.path=target/[your-project-name]/".

See https://github.com/demidenko05/beige-software beige-accounting-ajetty for example
