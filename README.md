# Weblogic-install-12.2.3


1. Download the Oracle WebLogic Server installation jar file from the Oracle website.

2. Create a response file for the installation. A response file is a text file that contains all the information needed to complete the installation. You 3. can create a response file using a text editor, such as vi or nano. Here is an example of a response file:




4. Modify the response file to include the appropriate values for your environment, such as ORACLE_HOME, MW_HOME, and NODEMGR_PORT.

5. Run the installation command with the -silent flag and the path to the response file:


java -jar fmw_12.2.1.3.0_wls.jar -silent -responseFile /path/to/response/file.rsp


6. After the installation is complete, you can create a WebLogic domain in silent mode using the Configuration Wizard. Create a new response file with the following contents:

domain_file.rsp

7. Modify the response file to include the appropriate values for your domain name, domain home, applications home, WL_HOME, and admin password.

8. Run the Configuration Wizard with the -silent flag and the path to the response file:

/u01/oracle/Middleware/Oracle_Home/wlserver/common/bin/config.sh -silent -responseFile /path/to/response/domain_file.rsp

9. After the domain is created, you can start the Administration Server using the startWebLogic.sh script:

