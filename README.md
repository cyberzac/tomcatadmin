tomcatadmin
===========

Bash script to simplify the usage of the Tomcat manager web app.
Basically it creates Tomcat manager text api urls and executes them with curl. 
Enjoy.


A wrapper around Tomcats manager webapp, see http://tomcat.apache.org/tomcat-7.0-doc/manager-howto.html#Supported_Manager_Commands 
Usage /Users/zac/bin/tomcatadmin [-h --host] command [parameter...]

Where command is one of:
  list                  - List all webapps
  serverinfo            - Lists information about Tomcat, OS and the JVM
  resources [type=XXX]  - Lists global JNDI resources
  status path           - returns -1 for not running, or if running, the number of sessions
  start path            - Starts the webapp on context path path
  stop path             - Stops  the webapp on context path path
  reload path           - Reloads the webapp on context path path
  deploy args           - Deploys a webapp, exampels of args is path=/foo war=file:/tmp/foo.war, see the link above
  undeploy path         - Undeploys the webapp at the given path

Flags:

-h host                Use host instead of localhost
-p port                Use port instead of 8080
-u user[:password]     Use user insterad of admin:admin
 
