# salesforce-ant
Salesforce Ant Migration Tool

This a Salesforce simple fetch and deploy using ant migration tool

build.xml - file defines the configuration
build.properties -
package.xml file - defines the metadata to retrieve
src folder - the output for the retrieved metadata
src/package.xml - the output package.xml for the src folder
environments folder - contains the credentials for target org
environments/<org>.properties file - org defines the environment


Fetch Build
	ant -Denvironment=sandbox -buildfile build.xml fetchMetadata

Deploy Build
	ant -Denvironment=prod -buildfile build.xml deployMetadata

Undeploy Build
	ant -Denvironment=prod -buildfile build.xml undeployCode	

Validate Build
	ant -Dsandbox=prod -buildfile build.xml deployEmptyCheckOnly


To create an executable bat file. Open notepad and paste the ant command and save the file as a .bat. Eg. fetchSandbox.bat. Call the fetchSandbox from the command prompt.
