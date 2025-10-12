# healthcareproject

This is the Healthcare demo Spring Boot project.

Key changes applied by automation:
- Upgraded project Java target to Java 21
- Configured maven-compiler-plugin to use release 21
- Fixed duplicate Lombok dependency and explicit Lombok version 1.18.30

How to build & test locally (Windows PowerShell):

```powershell
# Ensure JDK 21 is used (adjust path to your JDK 21 installation)
$env:JAVA_HOME='C:\Program Files\Java\jdk-21'
$env:Path = "$env:JAVA_HOME\bin;" + $env:Path

# Build and run tests
.\mvnw.cmd clean test

# Package without running tests
.\mvnw.cmd -DskipTests clean package
```

Notes:
- The project uses Spring Boot 3.5.5 and requires Java 21.
- If your CI or IDE uses a different JDK, set JAVA_HOME accordingly before building.

How to publish to GitHub (one-time steps shown below): see the instructions in this repo's root or use the commands provided after commit.