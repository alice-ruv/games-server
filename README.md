Board Game Server
=================

##Battleship game display:
![image](https://user-images.githubusercontent.com/124344785/224997886-c0e521d2-24e4-4e38-a5f4-53e7da429e8c.png)
![image](https://user-images.githubusercontent.com/124344785/224998117-66f9753f-0967-41c8-9bda-0535541fd330.png)

##Connect 4 game display:
![image](https://user-images.githubusercontent.com/124344785/224998274-3a6c7fb9-9583-4383-ac97-8da1cf3ec635.png)
![image](https://user-images.githubusercontent.com/124344785/224998377-01db05f6-edca-4ebb-b34c-a0f72043fefe.png)

******************************************************************************************************************************************

Installation Requirements:
--------------------------
1) JDK 1.8 (Version 8.0.202 is used for this application) <br />https://www.oracle.com/il-en/java/technologies/javase/javase8-archive-downloads.html

2) Glassfish 5.0.0 <br />http://download.oracle.com/glassfish/5.0.1/release/java_ee_sdk-8u1.zip	

3) PostgreSQL 14 <br />https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

4) JDBC Driver (Postgresql JDBC 42.4.0) <br />https://jdbc.postgresql.org/download/

5)  InteliJ ultimate <br />https://www.jetbrains.com/idea/download/#section=windows

6) Launch4j - used for creating exe file to run the client, not from IntelliJ <br />https://sourceforge.net/projects/launch4j/files/launch4j-3/3.14/

►This application was tested in 1920×1080 display resolution in windows. 



Installing Instructions:
------------------------
1) Install Postgres
	- set password to “password”
	- keep port to default (5432)

2) Unpack Glassfish to c drive

3) Copy JDBC driver jar file to c:\glassfish5\glassfish\domains\domain1\lib\

4) Overwrite domains.xml to c:\glassfish5\glassfish\domains\domain1\config\
   The file exists in final_project\domain.xml

5) Import project in InteliJ and build it.
   If you have an error "Application Server 'GlassFish 5.0.1' is not configured" in run/debug configurations: 
   press configure and then add your GlassFish Home directory.


6) Deploy server:
	- Deploy server from InteliJ by running “ServerApp” run configuration
	- Deploy server from cmd (only after it was deployed at least once by IntelliJ): 
		- Run “asadmin start-domain” in cmd from C:\glassfish5\glassfish\bin
		- Go to localhost:4848 in web browser, select Applications and then on BoardGamesServer-v1 row select Launch.

7) Deploy client:
	- Deploy client from InteliJ by running “ClientApp” run configuration
	- Deploy client from cmd: 
		- Build artifact clientJavaFXApp
		- You can use Launch4j to create exe file to run the client:
			1. Define Output file and Jar 
			2. Define Min and Max JRE version 
			3. Select the setting icon for creating the exe 
