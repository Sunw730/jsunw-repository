# jsunw-repository
My personal maven repository.

## Usage
pom.xml:
```xml
    <repositories>
        <repository>
            <id>jsunw-repository-snapshot</id>
            <name>jsunw-repository-snapshot</name>
            <url>https://github.com/Sunw730/jsunw-repository/snapshot</url>
        </repository>
        <repository>
            <id>jsunw-repository-release</id>
            <name>jsunw-repository-release</name>
            <url>https://github.com/Sunw730/jsunw-repository/release</url>
        </repository>
    </repositories>
```
```xml
    <dependency>
        <groupId>com.sunw</groupId>
        <artifactId>sunw-simple-search</artifactId>
        <version>1.0-SNAPSHOT</version>
    </dependency>
```
