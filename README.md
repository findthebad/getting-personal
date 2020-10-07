# Find the Bad: Getting Personal
This lab continues to build on the previous two exercises [Model 3](https://github.com/findthebad/model-3) and [Powerfall Convo](https://github.com/findthebad/powerfall-convo).  It should only require the installation of Docker and Docker Compose. 

## Disclaimer
This lab is based on real data containing actual malicious indicators.  If you attempt to do things such as find and run files, or visit network entities that occur in these logs, you do so at your own risk.

## Setup
1) Download and install [Docker](https://www.docker.com/get-started).
2) Download and install [Docker Compose](https://docs.docker.com/compose/install/) (On Windows Docker Compose should be bundled with the Docker installer, so this step shouldn't be required).
3) Download or clone this repository.
4) Open up a command prompt, make your way to this repository folder on your local machine and run `docker-compose up`.
5) When `docker-compose up` is finished bringing the containers up, open a browser and navigate to `http://localhost:5601` to access the Kibana instance.

## The Lab
This lab continues with the use of Kibana for identifying and investigating signs of a compromise.  The `VT Hunting` dashboard should provide you the information you need to get started.  If you're struggling or things aren't clear, make sure to look at the previous two labs in this introductory series.

### Questions
1) What is the name of the malicious file that has executed?
2) What did the associated process do?  Were there any other malicious indicators?
3) What was the parent process that launched the malicious image?  What does this tell you?  Are there other indicators that confirm that?
4) What process created the ddpp file?  Did it create or delete any other files?
5) What appears to be process that started all of this activity, when did it occur, on what computer and by what user? 

Bonus:
What advanced persistent threat (APT) has been discussed as being the group behind these indicators?

### Useful Links
- [VirusTotal](https://www.virustotal.com/gui/home/upload)
- [Sysmon Events List](https://docs.microsoft.com/en-ca/sysinternals/downloads/sysmon#events)
- [Sysmon Event ID 23](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-23-filedelete-a-file-delete-was-detected)
- [Kibana Query Language](https://www.elastic.co/guide/en/kibana/current/kuery-query.html)
- [MITRE - ATT&CK](https://attack.mitre.org/)
- [MITRE - ATT&CK - Scheduled Task/Job](https://attack.mitre.org/techniques/T1053/)

### Solution
Available [here](https://findthebad.com/getting-personal/).