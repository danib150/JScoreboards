# JScoreboards
Welcome to the JScoreboards Spigot library page.

If you find bugs- report them as a GitHub issue. Thanks!

If you'd like a video tutorial on how this API works, I have a [YouTube video](https://youtube.com/watch?v=SoPWdEMNFAM) you can watch.
Otherwise, you can take a look at the [wiki](https://github.com/JordanOsterberg/JScoreboards/wiki).
 
## Maven Repository
Please note- as of version 2.0.3 the Maven repository has changed. Update your pom.xml accordingly:

**Repository**:
```xml
<repository>
    <id>jordanosterberg-repo</id>
    <url>https://nexus-repo.jordanosterberg.com/repository/maven-releases/</url>
</repository>
```

**Dependency**
```xml
<dependency>
    <groupId>dev.jcsoftware</groupId>
    <artifactId>JScoreboards</artifactId>
    <version>2.1.2-RELEASE</version>
</dependency>
```

Make sure to specify your Java build version (e.x. Minecraft 1.8 requires Java 8, whereas 1.17 requires Java 16) in your `pom.xml`, as well as shade it into your jar file. The API will not work otherwise:
```xml
<build>
    <pluginManagement>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>JAVA_VERSION_HERE</source>
                    <target>JAVA_VERSION_HERE</target>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-shade-plugin</artifactId>
                <version>3.2.4</version>
                <executions>
                    <execution>
                        <phase>package</phase>
                        <goals>
                            <goal>shade</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </pluginManagement>
</build>
```

If you're having trouble, please submit a GitHub issue. The self hosted Maven repo gig is new to me :]

See [LICENSE.md](LICENSE.md) for license information.

That being said, the only *tested* versions are as follows:
- 1.8
- 1.16
- 1.17