# mvn-java-version-fix

When I install Java then Maven, I realised that Java version in maven was different. 


`mvn -v` 

`Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)
Maven home: /usr/local/Cellar/maven/3.6.3_1/libexec
Java version: 13.0.2, vendor: N/A, runtime: /usr/local/Cellar/openjdk/13.0.2+8_2/libexec/openjdk.jdk/Contents/Home
Default locale: en_GB, platform encoding: UTF-8
OS name: "mac os x", version: "10.15.2", arch: "x86_64", family: "mac"`


`java -version `

`java version "1.8.0_201"`


To fix this you need to change maven config file.
 
`vi /usr/local/Cellar/maven/3.6.3_1/bin/mvn` --> version can be different. 


Inside this file change JAVA_HOME part to 

`JAVA_HOME="${JAVA_HOME:-$(/usr/libexec/java_home)}"`
