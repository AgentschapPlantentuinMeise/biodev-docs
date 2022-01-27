# biodev-docs
 Documentation and system managment of the biodev01 development server


For more information contact Pieter (@PietrH): pieter.huybrechts@meisebotanicgarden.be 

## Where to find the server?
Server IP: 10.10.0.54

You need to be inside the gardens network to access the server, so if you are offsite you'll need the VPN. 

Please contact Pieter+Niko for login credentials if you think you need some. 

## Scope

You can use this server to run pretty much everything, as long as it doesn't need to be exposed to the outside world. This is not a production server. Let's try to be mindful of creep towards production services, if you feel something that is running on the server is becoming too important to loose, bring it up and we'll find a solution.

This server is a great place to store data you need to run your scripts (that you surely have stored in the cloud/github). Things like a wikidata/gbif dump belong here, but not data that you can't replicate (use cladonia/discuss with Niko if large).

The server is not a place to store vital data. It's not backed up, if you need something stored here that needs to be included in the backup, please discuss it with Niko and Pieter. 

Of course you can store data here, but just keep in mind that it may be lost if the server loses a drive, or if it needs to be whiped for any reason. bio-dev01 is a development environement, which means we have more freedom to experiment, but you may loose your stuff if you store it here. 

## Overview of installed libraries

For a complete overview please consult: [installed-packages](./installed-packages)

- pip3 18.1 
- Python 3.7.3 
- 7za 16.02
- MySQL 8.0.27-debian10
- aws-cli/2.4.14 Python/3.8.8
- curl 7.64.0 
- gdebi-core
- R version 4.1.2 (2021-11-01) -- "Bird Hippie"
- RStudio Server v2021.09.2+382
- libxml2-dev
- git 2.20.1

### MySQL

See https://github.com/AgentschapPlantentuinMeise/BGBASEtoMySQL for more information

## Installing new packages

**DO NOT RUN apt-upgrade**

Please contact Pieter if you want to install a new package so we can check for dependency problems. Perhaps using something like a conda environement is an alternative (miniconda, not Anaconda).

You can request a full VM to be created if you want to run something that might break things for others. 

