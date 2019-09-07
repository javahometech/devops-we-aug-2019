# Install Maven on Linux
Java is a dependency for maven

### Install Java

Note: JDK is mandatory to run maven commands

```
  sudo yum install java-1.8.0-openjdk-devel -y
```
Verify JDK installation

```
  java -version
  javac -version
```

### Install Apache Maven.

```
  sudo yum install maven -y
```

Verify maven installation

```
  mvn --version
```

### Install Git to clone source code from GIT

```
  sudo yum install git -y
```

### Package Java App using Maven

```
  git clone https://github.com/javahometech/my-app
  cd myapp
  mvn package
```

