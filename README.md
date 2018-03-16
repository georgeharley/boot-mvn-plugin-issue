# boot-mvn-plugin-issue

Using Spring Boot version 1.5.10.RELEASE...


1) Package the Spring Boot Jar supplying an override for the final Jar name
```
$> ./mvnw -Djar.finalName=foo clean package
```

2) List the contents of the `target` folder and note that the new "thin" Jar has been named according to the Maven property value but the Spring Boot "fat" Jar has ignored it. 
```
$> ls target/*.jar
target/foo.jar    target/myapp-0.0.1-SNAPSHOT.jar
```

