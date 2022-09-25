# distributed-group-membership

## How to run the project

### Pre-requisites

This project uses maven as the build system, and for handling dependencies. Make sure you have maven 1.8 and JDK installed on the system.

### Commands

To build & package:
```
$ mvn clean
$ mvn install
$ mvn dependency:copy-dependencies
$ mvn package
```

To run the membership protocol at each node: 
```
$ java -cp "target/group-membership-1.0-SNAPSHOT.jar:target/*" com.mp2.membership.Node
```

To run the introducer: 
```
$ java -cp introducer-1.0-SNAPSHOT.jar com.mp2.introducer.Introducer
```

To kill socket: 
```
$ lsof -i:<PORT NUM>; kill -9 <PID>
```