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

Get the build version for the service.

Parameters:
		`username`
		`password`

Returns:
The build version of the service
___
###relock

Re-lock a lock object

Parameters:
`username`
`password`
`lockId` - The Id of the lock object
`id` - The Id associated with the caller

Returns:
true - Successfully locked
false - Failure to lock
___
###unlockMultipleObjects

Unlocks multiple lock objects

Parameters:
`username`
`password`
`lockIds` - The id of the objects separated by ;
`id` - The Id associated with the caller
___
###unlockAllObjectsForUser

Unlocks all lock objects

Parameters:
`username`
`password`
~id` - The Id associated with the caller
___
###lockMultipleObjects

Locks multiple lock objects

Parameters:
`username`
`password`
`lockIds` - The id of the objects separated by ;
`id` - The Id associated with the caller

Returns:
true - Successfully locked
id of the projects that could not be locked separated by ;
___
###lock

Lock a lock object

Parameters:
`username`
`password`
`lockId` - The Id of the lock object
`id` - The Id associated with the caller
Returns:
true - Successfully locked
false - Failure to lock
___
###unlock

Unlock a lock object

Parameters:
`username`
`password`
`lockId` - The Id of the lock object
`id` - The Id associated with the caller
`propogate`

Returns:
true - Successfully locked
false - Failure to lock
___
###isProjectLocked

Checks if the object is locked by another user

Parameters:
`username`
`password`
`lockId` - The Id of the lock object
`id` - The Id associated with the caller

Returns:
true - object is locked by another user
false - object is released
___
###getAllLockedProjects

Gets all the projects that are locked by another user

Parameters:
`username`
`password`
`userId` - The Id associated with the caller
`propogate`

Returns:
xml

<projects>
<project>projectId</project>
</projects>
___
###setLockStatus

Sets the locking status for all projects that are locked by the user

Parameters:
`username`
`password`
`userId` - The Id associated with the caller
`isLock` - true - projects are locked false - projects are released
`propogate`

Returns:
Status
___
###getAllLockedProjectsOrDashboards

Gets all the projects or dashboards that are locked

Parameters:
`username`
`password`
`userId` - The Id associated with the caller
`propogate`

Returns:
xml

<projects>
<project>projectId</project>
</projects>
___
###unlockedProjectsOrDashboards

Unlock projects or dashboards

Parameters:
`username` - 
`password` - 
`xml` - 

Returns:
Status
