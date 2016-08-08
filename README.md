# jsunw-repository
My personal maven repository.

## Usage
setting.xml:
```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
              xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">   
    	<profiles>   
    		<profile>
    			<id>jsunw</id>
    			<repositories>
                    <repository>
                        <id>jsunw-repository-snapshot</id>
                        <name>jsunw-repository-snapshot</name>
                        <url>https://github.com/Sunw730/jsunw-repository/tree/snapshot</url>
                    </repository>
                    <repository>
                        <id>jsunw-repository-release</id>
                        <name>jsunw-repository-release</name>
                        <url>https://github.com/Sunw730/jsunw-repository/tree/release</url>
                    </repository>
                </repositories>	
    		</profile>
    	</profiles>
    	<activeProfiles>
    		<activeProfile>jsunw</activeProfile>
    	</activeProfiles>
    </settings>
```
或者 pom.xml:
```xml
    <repositories>
        <repository>
            <id>jsunw-repository-snapshot</id>
            <name>jsunw-repository-snapshot</name>
            <url>https://github.com/Sunw730/jsunw-repository/tree/snapshot</url>
        </repository>
        <repository>
            <id>jsunw-repository-release</id>
            <name>jsunw-repository-release</name>
            <url>https://github.com/Sunw730/jsunw-repository/tree/release</url>
        </repository>
    </repositories>
```
```xml
    <dependency>
        <groupId>com.jsunw</groupId>
        <artifactId>jsunw-simple-search</artifactId>
        <version>1.0-SNAPSHOT</version>
    </dependency>
```
