#Release Notes

##Upcoming Features

> ###Database Autodeployment
Allows for the autodeployment of the pneuron_config database either locally or to a remote host. 

> ###Database Caching
> Allows option for users to cache files in the pneuron_config database by using a new option in the Adapter Pneuron. 

> ###Pneuron Microservices
> Allows users to programmatically call pneurons through the rest API and receive a response 

##October 2020 (Kratos)

> ###Parser Pneuron
> Removed EDI Pneuron and replaces with parser pneuron. Includes SWIFT, HL7, and EDI parsing capabilities.

> ###Pneuron Rest API
> Updated Pneuron API by removing SOAP services and replacing with REST architecture.

> ###Converted to Binary Message Stream
> Converted the Pneuron message stream to binary from XML. Displays messages in JSON format in console window. Increased performance anywhere from 2 to 6 times using preexisting Pneuron networks.

> ###Spark Pneuron
> Added the Spark Pneuron that allows for submission of Jar and PySpark applications to existing Spark clusters.

> ###Kafka Pneuron
> Added the Kafka Publisher and Listener Pneurons that allow for publishing and recieveing messages from Kafka streams.

##June 2020 (Heracles)

> ###Zulu JDK Support
> Adds Pneuron support for the Zulu JDK.

> ###UTF-8 Support for Non-English Characters
> Added support for Chinese and Spanish characters.

> ###New Matching Algorithms
> Added a wider selection of matching algorithms for Matching Pro Pneuron.

> ###Hadoop Action Pneuron
> Added the Hadoop Action Pneuron that allows the user to perform actions on files in the HDFS like deleting and moving files. 

> ###HTTP Pneuron Update
> Adds new options and functionality to the HTTP Pneuron like storing the response in memory.

> ###Couch DB Support
> Adds Couch DB support to the NoSQL Pneuron.

##March 2020 (Hermes)

> ###Event Hub Pneurons
> Added the Event HUb Publisher and Listener Pneurons that allow users to add an receive messages from Azure Event Hubs.

> ###Database Migration Pneuron
> Added the Database Migration Pneuron which is a faster way of moving large amounts of data from one database to another. 

> ###Multi-Host / Multi-Port Setup on Single Server. 
> Added capability to have many hosts and ports on a single server. 

> ###Auto Retry/Reconnect/Clean-Up for Database Aliases
> Allows retry, reconnect, and clean-up functionality for destination and source database connectivity issues. 

##December 2019 (Athena)

> ###Qubz Pneuron
> Adds the Qubz Pneuron which allows for various actions to be performed on cubes and jobs in Qubz.

> ###Hive DB Alias
> Adds support for Hive database in data source alias. 

> ###File Action Update
> Adds updated functionality for the File Action Pneuron such as using file reference and renaming files.

> ###Hadoop Reader Pneuron
> Adds the Hadoop Reader Pneuorn that allows for reading files from HDFS.

> ###Hadoop Writer Pneuron
> Adds the Hadoop Writer Pneuorn that allows for writing to the HDFS.

##September 2019 (Apollo)

> ###JSON Parsing Support
> Added JSON parsing support for the File Pneuron.

> ###Cloud Enabled/Docker Support
> Pneuron can now be deployed on the cloud via Docker.

> ###New Dashboard Functionality and UX Enhancments
> Updated UX and added more dashboard functionalities.

##March 2019 (Ares)

> ###Removed Third Party Dependencies
> We removed a few third party dependency libraries that bogged down deployment and client

> ###NoSQL Pneuron
> Added the NoSQL Pneuron that allows users to query NoSQL Databases. 

> ###ETL Pneuron
> Added supply chain management support through the new ETL Pneuron.

> ###SFTP Support
> Added the SFTP option for the FTP Pneuron

> ###AES 256 Encryption
> Security change fro DES to AES encryption. 
