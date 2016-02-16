# IBM-FileNet-CPE-Maven-Install
This is a Maven POM project which takes a directory location and installs the CPE JARs into a Maven repository
# Usage
* Open the POM file and change the property value for "filenet.cpe.install.path" to the install path of your Content Engine
* Run 'mvn install' (local Maven) or 'mvn deploy' (remote Maven)
* Now you can make use of the CPE JARs available in your Maven repository