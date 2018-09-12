# paytm
basic integration ptm 


for adding ptm  
1.  got paytm side and download the java paytm kit api and put any specif floader and extract that folder and choose any version 
of paytm jdk jar file find the groupid and artificat id inside jar file
2. example
go to the checksume_2.0 inside after target.maven-archive in these folder inside we will get one file pom.properties
(we will get version, groupid and artifactid )
version=1.0
groupId=com.paytm.pg
artifactId=pg-checksum

3. after that open terminal and go to project home inside path and give the following command based on your system checksum jar file location(add jar inside maven repository)

 mvn install:install-file -Dfile=/Users/jagasan/Downloads/checksum_2.0.0.jar -DgroupId=com.paytm.pg -DartifactId=pg-checksum -Dversion=1.0 -Dpackaging=jar -DgeneratePom=true
 
 4. add the following dependency in pom.xml 
 
      <dependency>
	<groupId>com.paytm.pg</groupId>
	<artifactId>pg-checksum</artifactId>
      <version>1.0</version>
  </dependency>
    
    now your pytm jar is availale to use in spring boot project
 
 
 
 
 


