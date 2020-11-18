

##Method Detail
___
###getBuildDate

Get the build date for the service.

Parameters:
`username`
`password`

Returns:
The build date of the service
___
###getBuildNumber

Get the build number for the service.

Parameters:
`username`
`password`

Returns:
The build number of the service
___
###getVersion

Get the version of the service

Parameters:
`username`
`password`

Returns:
The service version number
___
###addXmlMessageEx

Add an Xml message to the pneuron server's internal message queue

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`sourceNeuron` - The neuron which is sending the message
`targetNeuron` - The neuron who is to receive the message
`message` - The message

Returns:
Status
___
###fireNeurons

Fire all neurons sent as parameters

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`xmlNeuronNames` - XML containing neurons name

Returns:
Status
___
###fireNeuronsWithDebug

Fire all neurons sent as parameters, with a message set as DEBUG

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`xmlNeuronNames` - XML containing neurons name


Returns:
Status
___
###addXmlMessage

Add an Xml message to the pneuron server's internal message queue

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`targetNeuron` - The neuron who is to receive the message
message - The message

Returns:
Status
___
###clearMessages

Clear a given pneuron server's message queue

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`name` - Name of the queue

Returns:
Status
___
###getXmlMessage

Get a message from a pneuron server's queue

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`name` - Name of the queue

Returns:
First message in the queue
___
###getTransactionStatus

Parameters:
`username`
`password`
`transactionId`

Returns:
xml - status of transaction
___
###searchTransaction

Check if transaction is still running

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`name` - Transaction Name search criteria
`fPropogate` -


Returns:
Transaction Details List
___
###quitTransaction

Check if transaction is still running

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`name` - Transaction Name search criteria
`messageId`
`transactionId`
`clusterfPropogate`

Returns:
Status
___
###searchDurableMessages

Get all durable messages associated

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`neuornName`
`startDate`
`endDate`
`topResults` -

Returns:
Status
___
###removeDurableMessages

Removes durable messages for a Pneuron

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`xmlIdList`

Returns:
Status
___
###getDurableMessage

Get all durable messages associated with a pneuron

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`messageId`

Returns:
Xml of all durable messages.
___
###searchDurableTransferMessages

Get all durable messages associated with a pneuron

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`startDate`
`endDate`
`neuronNameFrom`
`neuronNameTo`
`neuronHostFrom`
`neuronHostTo`
`withinLastSeconds`
`topResults`

Returns:
Xml of all found durable messages.
___
###removeDurableTransferMessages

Removes durable transfer messages for a Pneuron

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`xmlIdList`

Returns:
Status
___
###getDurableTransferMessage

Parameters:
`username` - The username the message is sent from
`password` - The password for the username
`messageId`

Returns:
Xml of all durable transfer messages.
___
###removeAllDurableMessages

Delete all durable messages.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
Status
___
###removeAllDurableTransferMessages

Delete all durable transfer messages.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
Status
___
###countRecordsForDurableTransferMessages

Delete all durable transfer messages.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
Count of records
___
###countRecordsForDurableMessages

Delete all durable messages.

Parameters:
`username` - The username the message is sent from
`password` - The password for the username

Returns:
Count of records
