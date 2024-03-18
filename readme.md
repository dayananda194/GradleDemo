SET UP OF BASIC GRADLE USING COMMAND LINE INTERFACE :

--step1 
	gradle init --use-defaults --type java-application

The above command will set up a basic gradle project .

--step2 
	./gradlew build 

 The above command will build our java project 


To run a jar file , after creating , we need to set up the manifest property (the property which 
tells  the starting point of our java application to the build tool ) . 

The manifest property have to set in 'build.gradle' file . It will identify the main class 
to execute . 


---------------manifest property contents in build.gradle file ----------
jar {
    manifest {
        attributes 'Main-Class': 'org.example.Main'
    }
}
------------------------------------------------------------------------

--step3 
	./gradlew jar 

The above command will create a new jar file in build/libs folder .

--step4 
	java -jar /build/libs/jar_file_name.jar

The above command will run our java project . 

 


