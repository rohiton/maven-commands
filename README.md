# maven-commands

## mvn clean 
It deletes the target folder from your project that contains all the bytecodes of your source code, test files and jar/war files.

## mvn eclipse:clean 
This will only delete the .settings directory and .project & .classpath file from your project and will not delete the target folder.

## mvn compiler:comple 
This will compile all the source code(src/main/java	) and will place the resultant bytecode into target/classes directory (It will not build the jar/war file).

## mvn compiler:testCompile 
This will compile all the test classes(src/test/java) and will place the result bytecode into target/test-classes directory (first generate the bytecodes of your source files to compile your test classes).

## mvn package
This is one of the important command as it builds your project into respective jar/war file but note that before the package goal, maven will first compile your source code, compile your test source code and also perform the test cases before actually building the jar/war file. It will only build the project but will not install in local repo.

## mvn install 
To place the jar/war files and dependencies related to your project into the local repository such that next time maven will look into your local repository instead of central repository when building your project. It will also build the jar/war/pom and also performs test cases.

## mvn validate
To validate your project and check its correctness.

## mvn dependency:tree
This will generate the dependency tree.

## mvn dependency:analyze
This will find the unused and undeclared dependencies.

## mvn archetype:generate
This will create a maven project and will ask for groupId, artifactId, package, version and will generate a project for you at the end.

## mvn site:site
This will generate a static website that contains information about your project and its dependencies and will place into target folder.

## mvn test
This is used to run all the test cases and make sure that you've compiled your test classes first.

## mvn compile
This will compile your source code into bytecode and will place into target folder.

## mvn -f /opt/projects/demo/pom.xml package
To build project from a different location.

## mvn -o package
To run in offline mode when you're sure that all the required dependencies are available and you don't want maven to look for depedencies from central repo.

## mvn -DskipTests package
It compiles the tests but skip running them followed by building the project jar/war file.

## mvn -DskipTests=true package
It will skip compiling the tests and running them followed by building the project jar/war file.
