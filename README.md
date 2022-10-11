# biodev-docs
 Documentation and system managment of the biodev01 development server


For more information contact Pieter (@PietrH): pieter.huybrechts@meisebotanicgarden.be 

## Where to find the server?
Server IP: 10.10.0.54

You need to be inside the gardens network to access the server, so if you are offsite you'll need the VPN. 

Please contact Pieter+Niko for login credentials if you think you need some. 

### Ports in use

OpenRefine: http://10.10.0.54:3333/

RStudio: http://10.10.0.54:8787/

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
- poppler-utils
- Spark 3.0.1
- Hadoop 3.2
- openjdk version "11.0.14" 2022-01-18
- libarrow
- github cli 2.5.2
- jpeginfo v1.6.0
- pigz 2.4
- OpenRefine 3.5.2
- tesseract 4.0.0
- leptonica-1.76.0
- libgif 5.1.4 : libjpeg 6b (libjpeg-turbo 1.5.2) : libpng 1.6.36 : libtiff 4.1.0 : zlib 1.2.11 : libwebp 0.6.1 : libopenjp2 2.3.0
- tesseract-ocr-eng
- tesseract-ocr-fra
- ocrmypdf 8.0.1+dfsg
- libmariadb-dev


### OpenRefine
We are running Version 3.5.2 on OpenJDK Runtime Environment 11.0.14+9-post-Debian-1deb10u1. To start the service run: `start openrefine.service` with elevated user rights. Restarting the service is similar with `restart`. I have no objections to updating to the most recent version, but I'll hold off until I get a request.

If you need more RAM to be allocated to OpenRefine (increase the JAVA heap size) by looking in this book which has other interesting things in it: https://subscription.packtpub.com/book/big-data-and-business-intelligence/9781783289080/1/ch01lvl1sec15/recipe-7-going-for-more-memory, do keep in mind that OpenRefine/JAVA will keep this RAM reserved, so it will not be availalbe to other services such as Python/MySQL/R.

### MySQL

See https://github.com/AgentschapPlantentuinMeise/BGBASEtoMySQL for more information

## Installing new packages

**DO NOT RUN apt-upgrade**

Please contact Pieter if you want to install a new package so we can check for dependency problems. Perhaps using something like a conda environement is an alternative (miniconda, not Anaconda).

You can request a full VM to be created if you want to run something that might break things for others. 

