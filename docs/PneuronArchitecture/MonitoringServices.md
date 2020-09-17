#Monitoring Web Services
The monitor services allows remote systems to manage monitor statistics on the server.
##Methods
___
###getBuildDate

Get the build date for the service.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
The build date of the service
___
###getBuildNumber

Get the build number for the service.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
The build number of the service
___
###getVersion

Get the build version for the service.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
The build version of the service
___
###getInFlightMessageIds

Get the inflight message IDs

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dispatcherTopic - The dispatcher's JMS topic

Returns:
An XML document which describes all of the in flight messages
___
###getServerStats

Get all of the server statistics

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
An XML document which describes all of the server statistics