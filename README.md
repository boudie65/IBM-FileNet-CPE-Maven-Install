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

# Motivation
Have you ever used Maven in combination with FileNet development? Then you also are aware that adding the FileNet JARs to your local or remote repository is quite some work. The best thing that could happen is that IBM would offer the JARs on the IBM Maven Repository. Unfortunately, it is not there (yet). So I am urging IBM ECM to get there act together and provide us with a repository. The nice colleagues from WAS know how to do it, looking at [this location](http://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/maven/repository)

And I also found this interesting bit there, a POM to install all WAS JARs into your local repository. You can find it here for [WAS 8.5.5](http://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/maven/repository/com/ibm/tools/target/was.installer/8.5.5/was.installer-8.5.5.pom)

Reusing the FileNet version information.
Since I am lazy, I wanted to reuse the information from the ce_version.txt file to be able to add the JARs under that version number. This means I can simply add the JARs after performing an Interim Fix or Fix Pack installation. I use the Groovy Maven plugin to grab hold of the file and search for the version number.

Now you can install the FileNet JARs in your local repository.

`mvn install`

By adding the following parameters you can also deploy them to a remote (Nexus) repository for instance:

`-Durl=http://<remote repo>:8081/nexus/content/repositories/thirdparty/ -DrepositoryId=nexus`
#### Note
Please note, it is working for my currently installed version, you are free to make changes and improve the script
