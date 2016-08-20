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
    			
    			<!-- 指定jdk版本 -->
                <activation>
                    <jdk>1.8</jdk>
                </activation>
    			
    			<repositories>
    			
    			    <!-- 公共仓库 -->
    			    <repository>
                        <id>apache repo</id>
                        <name>apache repo</name>
                        <url>http://repo.maven.apache.org/maven2/</url>
                        <layout>default</layout>
                        <releases>
                            <enabled>true</enabled>
                            <updatePolicy>never</updatePolicy>
                            <checksumPolicy>warn</checksumPolicy>
                        </releases>
                        <snapshots>
                            <enabled>false</enabled>
                        </snapshots>
                    </repository>
                    <repository>
                        <id>mvnrepository</id>
                        <name>mvnrepository</name>
                        <url>https://mvnrepository.com/</url>
                        <layout>default</layout>
                        <snapshots>
                            <enabled>false</enabled>
                        </snapshots>
                        <releases>
                            <enabled>true</enabled>
                            <updatePolicy>never</updatePolicy>
                            <checksumPolicy>warn</checksumPolicy>
                        </releases>
                    </repository>
    			
    			    <!-- jsunw 仓库 -->
                    <repository>
                        <id>jsunw-repository-snapshot</id>
                        <name>jsunw-repository-snapshot</name>
                        <url>https://github.com/Sunw730/jsunw-repository/tree/snapshot</url>
                        <releases>
    						<enabled>false</enabled>
    					</releases>
    					<snapshots>    
    						<enabled>true</enabled>  
    						<updatePolicy>always</updatePolicy>  
    						<checksumPolicy>warn</checksumPolicy>    
    					</snapshots>  
                    </repository>
                </repositories>	
    		</profile>
    	</profiles>
    	
    	<!-- 使用profile配置 -->
    	<activeProfiles>
    		<activeProfile>jsunw</activeProfile>
    	</activeProfiles>
    </settings>
```
```xml
    <!-- 引入jsunw的jar包，例如 -->
    <dependency>
        <groupId>com.jsunw</groupId>
        <artifactId>jsunw-simple-search</artifactId>
        <version>1.0-SNAPSHOT</version>
    </dependency>
```
