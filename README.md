# IBM-icm-CPE-Maven-Install
This is a Maven POM project which takes a directory location and installs the CPE JARs into a Maven repository
# Usage
* Open the POM file and change the property value for "filenet.cpe.install.path" to the install path of your Content Engine
* Run 'mvn install' (local Maven) or 'mvn deploy' (remote Maven)
* Now you can make use of the CPE JARs available in your Maven repository

# Deployed JARs
In groupId 'com.ibm.filenet.cpe'
* Jace.jar
* javaapi.jar
* listener.jar
* log4j.jar
* p8cjares.jar
* pe.jar
* peResources.jar
* pe3pt.jar
* client-download.jar
* stax-api.jar
* xlxpScanner.jar
* xlxpScannerUtils.jar