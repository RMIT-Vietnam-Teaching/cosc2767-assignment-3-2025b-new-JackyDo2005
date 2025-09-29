/*
  RMIT University Vietnam
  Course: COSC2767|COSC2805 Systems Deployment and Operations
  Semester: 2025B 
  Assessment: Assignment 3
  Author: Do Duy Hung
  ID: S3991053
  Created  date: 22/9/2025
  Last modified: 22/9/2025
  Acknowledgement: Acknowledge the resources that you use here. 
*/

# ---- Base Tomcat ----
FROM tomcat:10.1-jdk17

# (optional) clean default apps
RUN rm -rf /usr/local/tomcat/webapps/*

# ---- Copy your WAR built by Maven ----
# Ensure this file exists before building: JackyWebApp/target/JackyWebApp-1.0-SNAPSHOT.war
COPY ./JackyWebApp/target/JackyWebApp-1.0-SNAPSHOT.war /usr/local/tomcat/webapps/ROOT.war

# ---- Network & start ----
EXPOSE 8080
CMD ["catalina.sh","run"]
