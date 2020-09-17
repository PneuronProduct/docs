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
###getLicense

Allocate a unit of the license to the ID

Parameters:
Parameters:
`username`
`password`
`name` - Name product license
`id` - Identifier of the caller (normally host name)

Returns:
true if successfully obtained, false on failure
___
###getLicenseThrottle

        public static boolean getLicenseThrottle(java.lang.String username,
                                                 java.lang.String password,
                                                 java.lang.String name,
                                                 int throttle,
                                                 java.lang.String id)

        Allocate a unit of the license to the ID

		Parameters:
Parameters:
`username`
`password`
`name` - Name product license
`id` - Identifier of the caller (normally host name)
`throttle`

Returns:
true if successfully obtained, false on failure
___
###releaseLicense

		Parameters:
Parameters:
`username`
`password`
`name` - Name product license
`id` - Identifier of the caller (normally host name)
`throttle`

Returns:
Status
___
###checkLicenses

Check to see if we can allocate licenses for neurons (binary license)

Parameters:
`username`
`password`
`xmlLicenseNames` - XML of license names Name1 Name2 Name3 
        
Returns:
XML of neurons if the licensed could have been acquired
___
###getLicenseDetails

Get information about the client license
`username`
`password`

Returns:
XML of the licenses with the License name, License number of units and License number of days left
___
###getAllLicenseDetails

Get information about the all client license


Parameters:
`username`
`password`

Returns:
XML of the licenses with the License name, License number of units and License number of days left Feature: #5297 Author: Augustin Galea Date: 11-08-2013 Description: Keeps information about the method GetAllLicenseDetailsRpc
___
###releaseLicensesManagement

Release licenses for license_name and allowed_by Feature: #5297 Author: Augustin Galea Date: 11-08-2013

Parameters:
`usernames` - 
`password` - 
`xml` - 

Returns:
Status
___
###reloadLicense

Reload the new license

Parameters:
`usernames` - 
`password` - 
`licenseFileName` - Name of the file that was uploaded
Returns:
Success or The error that might have occurred while trying to upload the license
___
###     checkLicenseConsumerVersion

Check changes to license state

Parameters:
`usernames` - 
`password` - 
`sessionID` - Session Identifier
`knownVersion` - Current Version Known by Client
Returns:
Version Status - true - current, false - old
___
###getLicenseLocksState        

Get License Locks and Version - Current State

Parameters:
`usernames` - 
`password` - 
`licenseFileName` - Name of the file that was uploaded
Returns:
Success or The error that might have occurred while trying to upload the license
___
   ###getVersion
   
Get the version of the service

Parameters:
`usernames` - 
`password` - 

Returns:
The service version number

