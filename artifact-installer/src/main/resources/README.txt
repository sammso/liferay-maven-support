This ant script uses existing Liferay Tomcat bundle and source to create and
install  Liferay maven artifacts including source and javadoc to either a local
maven repository or remote maven repository.

Download the Liferay tomcat bundle and source code and extract them to a directory.
Then edit installer.<username>.properties to set the path to you tomcat directory, liferay version and custom groupId
Liferay portal source directory and Liferay version number. This installer is 
compatible with any Liferay 5.x release including EE. 

run "ant install-liferay-artifacts" to install artifacts to local maven repository.

run "ant deploy-liferay-artifacts" to install artifacts to a remote maven repository.

run "and prepare-poms" changes pom structure from maven-plugin to match your version defined in installer.<username>.properties with groupId and version.

If you need to provide credentials to your repository add them into 
<USER_HOME>/.m2/settings.xml

Below is a sample settings.xml

<?xml version="1.0" encoding="UTF-8"?>
<settings>
    <servers>
        <server>
            <id>liferay</id>
            <username>admin</username>
            <password>admin123</password>
        </server>
    </servers>
</settings>
