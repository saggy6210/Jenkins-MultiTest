1. To Run Powershll Script with jenkins job
2. To Run Pipeline through Jenkinsfile with powershell script.

Prerequisite:
Install following plugins into Jenkins master.
Git Plugin 
pipeline Plugin
Powershell Plugin

1. Steps to follow:
 Create New Freestyle Job in jenkins -> Build Option -> Select Windows Powershell -> Add Powershell command/Script -> Save & Apply -> Build
 
2. Steps to follow:
Create pipeline job in jenkins -> Pipeline Option -> Select Pipeline script form SCM -> choose SCM as Git -> Add repository URL -> 
Update Branch name & Script path - >Apply and Save -> Build. 
