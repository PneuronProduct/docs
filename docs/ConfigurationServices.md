#Configuration WEB Service
The neuron configuration service allows for the addition, deletion and modification of pneurons and aliases. All connections between neurons are also managed via this service.

##Methods
___
###getBuildDate

Get the build date for the service.

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
The build date of the service
___
###getBuildNumber

Get the build number for the service.

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
The build number of the service.
___
###getVersion

Get the build version for the service.

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
The build version of the service
___
###isCacheProjects

Check if project caching is enabled or not

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
true - Project caching is enabled. 
false - Project caching is disabled.
___
###addCategory

Add new category

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`configurationXML` - XML to be used to describe the new category

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addDashletOption

Add a dashlet option to a dashlet.

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` -  XML of new option

Returns:
Status
___
###addHost

Add a new host definition

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`name` - The name of the new host
`system_defined` - Is the new host system defined

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addNeuron

Add a new pneuron to a project

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`fPropagate` - Should the addition be propagated to remote servers
`configurationXML` - XML to be used to describe the new pneuron 
 
<xml>

   <name>foo</name>
   <class>com.pneuron.foo</class>
   <host>localhost</host>
   <image>foo.png</image>
   <X>10</X>
   <Y>10</Y>
   <project>default</project>
 </xml>
            
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addNeuronType

Adds Pneuron Type

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`name` - type name
`className` - java class
`image` - image address

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addPredefinedQuery

Add Predefined Query allowing DataSource and Project Entry

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`id` - query id
`name` - query name
`query` - actual query string
`projectID` - associated project id
`dataSourceID` - associated data source id

Returns:
Status
___
###updatePredefinedQuery

Update Predefined Query allowing DataSource and Project Entry

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`id` - query id
`name` - query name
`query` - actual query string
`projectID` - associated project id
`dataSourceID` - associated data source id

Returns:
Status
___
###addPredefinedSqlDetails

Add a new predefined sql detail

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - Describes the new predefined sql detail 
 
<xml>

<predefined_sql_id>00000001_12F76AA82CE_C0A801DD_FABE</predefined_sql_id>
   <tableName>dda_cust_yr_mth_anlys</tableName>
   <condition>d.avail_bal_amt <= 10000</condition>
   <alias>'0-$10,000'</alias>
 </xml>
 Returns:
Status
___     
###addPrivilege
Add a new privilege to the pneuron environment

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`name` - Name of the new privilege
`system_defined` - Is the new privilege system defined

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addProject

Add a new project to the environment

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - Describes the new project 
 
<xml>

   <name>foo</name>
   <description>This is the foo project</description>
 </xml>
             
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addRole

Add a new role to the environment

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`name` - Name for the new role
`system_defined` - System_defined tells us if the record is system defined

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addSubProject

Add a subject project to the environment

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - Describes the new project 
 
<xml>

   <parent_id>1</parent_id>
   <src_neuronid>100</src_neuronid>
   <dst_neuronid>20</dst_neuronid>
   <child_id>110</child_id>
   <X>100</X>
   <Y>100</Y>
   <image>get_users.png</image>
 </xml>
            
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addEditTab

Add a new tab or Edit a tab

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - Describes the tab 
            
Returns:
The id of the new created tab or -1 if the name of tab exists
___
###resetPassword

Reset password

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`resetpassword` - new password

Returns:
String containing one of the following values: "error","success", "Password already used"
___
###saveUser

Add a new user to the pneuron system

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - fooNameTest fooPassword firstNameTest lastNameTest departmentTest 12345 emailAddressTest 0yes 03-13-2012 12:02:10 yes yes

Returns:
String containing one of the following values: "error","success", "Password already used"
___
###saveGroup

Add a new group to the pneuron system

Parameters:
`name` - Name of the group
`description` - Description of the group fooName fooDescription 

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###saveInformationsAccess

Add a new information access to the pneuron system

Parameters:
`name` - Name of the information fooResourceID fooUserID fooGroupID fooAccessCode 

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###addUserVar

Add a new user variable

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - Describes the new project 
 
<xml>

   <name>var1</name>
   <src_neuronid>100</src_neuronid>
   <type>integer_value</type>
   <value>110</value>
   <project>1000</project>
 </xml>
 
Returns:
Status
___            
###authenticateUser

Check the authentication of a username and password pair

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
An XML document containing the user details if success, an empty string if not
___
###copyProject

Make a copy for each project

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
stopNeurons - true if the new copied will be stoped
projectsXML - XML containing the names of the projects to copy 
  
<projects>
<project>
 			
<newName>Project1</newName>
 			<oldName>New Project1</oldName>
 			<host>localhost:8888</host>
 		</project>
 		<project>
 			<newName>Project2</newName>
 			<oldName>New Project2</oldName>
 			<host>localhost:8888</host>
 		</project>
 	</projects>
  
            
Returns:
a XML string containing the list of all projects names with name conflict problem
___
###dashboardExists

Verify if a dashboard already exists and if it does if it can be overwritten (if it belongs to a user with the same roles as the authenticated user)

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`dashboardName` - The name of the dashboard to be verified

Returns:
XML Name The name of the dashboard if it already exists, and if it cam be overwritten.
___
###deleteCategory

Delete a category instance from the configuration

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`id` - ID of the categories to delete
`newCategoryId` - ID of the category where all the neurons from deleted categories will be moved

Returns:
Status
___
###getSelectedTabForUserId
Get the last selected dashboard id and last selected tab id for an user.

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server

Returns:
: a String array result[0] = last selected dashboard id, result[1] = last selected tab id If the dashboard or the tab do not exist the srray will be empty
___
###addUpdateLastSelectedDashboardForUser

Set the last dashboard visited by the user

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`tabID` - Last selected tab id

Returns:
Status
___
###setDefaultTabForDashboard

Set the default tab for a dashboard

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`isDefaultTab` - If a tab is set as default
`tabID` - Tab sets as default

Returns:
Status
___
###deleteDashboards
Delete a dashboard

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`dashboardID` - ID of the dashboard to delete

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###deleteDashletOptions

Delete a dashlet option

Parameters:
`username` - Username to be used to authenticate with the server
`password` - Password to be used to authenticate with the server
`xml` - xml containing the ids list of the dashlets options to delete

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###deleteDashletOptionsForDatasourceName

Delete dashlet options for a certain dashlet, options associated to a datasource.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
datasourceName - Name of the datasource
dashletID - ID of the dashlet
allProperties - if all properties for that datasource should be removed or only the RowColor group properties

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###deleteDashlets

Delete a dashlet

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashletID - xml ids list of the dashlets to delete

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###deleteProject

Delete a project from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the deletion be propogated to all effect servers
name - Id of the projects to delete

Returns:
Status
___
###deleteProperty

Delete a property

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - The value of the field name

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###deleteTab

Delete a tab

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
tabID - ID of the tab to delete

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateCreationTimeForTabs

Updates time of creation for tabs

Parameters:
Username
Password
xml

Returns:
Status
___
###deleteUserVar
Delete a user vairable

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the variable

Returns:
Status
___
###projectUvDependencies

Searches if the projects with ids = listProjId have dependencies

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
listProjId - Ids of the projects

Returns:
Status
___
###userVarsDependencies

Searches if the userVar is used by other resources

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
lstUvNames - Names of the variables
listProjId - Ids of the projects
shouldCheckInsideOfTheProject - Check dependecies inside of the project or not

Returns:
userVars used by other resources.
___
###getTemplateDependencies

Searches if the template is used by other resources

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
templateName - Names of the template

Returns:
Template dependencies
___
###getAnalayticXmlForTemplate

Gets XML template for analytic editor.

Parameters:
Username
Password
Id
Returns:
Template in XML format 
___
###saveAnalayticXmlForTemplate

Saves XML template in analytic editor

Parameters:
Username
Password
Id
analyticXml

Returns:
Status
___
###definedQueriesDependencies

Searches if the definedQuery is used by other resources

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
lstDqNames - Names of the variables
listProjId - Ids of the projects

Returns:
Status
___
###delHost

Delete a host from the system configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Host name

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###findProjectsAndNeuronsContainingText

Find projects and neurons whose name contain certain text.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
textToFind - The text to be contained

Returns:
XML 00000003_1373605772B_C0A80115_072E a1 00000019_13736082228_C0A80115_072E aaaaaa2 com.pneuron.neurons.PrintNeuron  print.png 5 1 localhost:8888 
___
###getAllNeuronNames

Gets all Pneuron names

Parameters:
Username
Password

Returns: XML of all Pneuron names
___
###findDashboardsTabsAndWidgetsContainingText

Finds dashboards or tabs containing the given text.

Parameters
Username
Password
TextToFind

Returns:
Status
___
###delNeuron

Delete a neuron instance from the configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the deletion be propogated to all effected servers
id - The ID of the neuron

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delNeuronByName

Delete a neuron instance from the configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the deletion be propogated to all effect servers
id - The ID of the neuron
neuronName - The name of the neuron

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delNeuronType

Delete Pneuron Type

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - type id

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delPredefinedQuery

Delete a predefined query fromt the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the query
projectID - Project assocaited with the query

Returns:
Status
___
###delPredefinedQueryForAdmin

Delete Predefined Query By Id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - query id

Returns:
Status
___
###delPrivilege

Delete a privilege from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the privilege

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delRole

Delete a given role from the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the role

Returns:
true if delete a given role from the environment false if the given role wasn't deleted
___
###getRoleDependencies

Get if exists users with role name associated

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the role

Returns:
true if exists users with role name associated and false if the role is not associated
___
###delSubProject

Delete a subproject from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - The ID of the project

Returns:
Status
___
###delSubProjectConnection

Delete a subproject connection

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
srcId - Source neuron ID
dstId - Destination neuron ID
action - Action to be taken (project or neuron)

Returns:
Status
___
###delUser

Delete a user from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - User name to be deleted

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delGroup

Delete a group from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - User name to be deleted

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###delInformationAccess

Delete an information from the system

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - User id to be deleted

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###getAllDatasources

Get all data sources

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
showAll - showAll to be used to get all datasources if true, if false to get datasources only for the user's logged roles

Returns:
XML document describing all data sources
___
###getAllHosts

Get all configured hosts

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all of the known hosts
___
###getAllHostsAndNeuronsHosts

Get all configured hosts and neurons hosts

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all of the known hosts
___
###getAllHostsForCluster

Get all configured hosts for Pmonit Application

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all of the known hosts
___
###getPneuronPropertyByName

Get configured property by property name

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name to be used to find the configured property

Returns:
An XML document describing the configured property
___
###getAllNeurons

Get all know neuron instances

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectName - Name of the project to search

Returns:
An array of names
___
###getAllNeuronTypes

Get All Pneuron Types For Admin Application

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Xml describing the neuron types.
___
###getAllPredefinedQueries

Get all pre-defined queries

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
showAll - showAll to be used to get all predefined_sql if true, if false to get predefined_sql only for the user's logged roles

Returns:
An XML document descibing the predefined queries
___
###getAllPrivileges

Get all of the system privilages

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document descibing the privialges
___
###getSelectedProjects

Get the selected projects

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
appName - Name of the calling application
projectsXml - String xml containing the project names

Returns:
An XML document describing the projects
___
###getAllProjects

Get all of the known pojects

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
showAll - Show all projects be returned

Returns:
An XML document describing the projects
___
###getAllProperties

Get all configured properties

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all of the known properties
___
###getAllRoles

Get all roles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all roles
___
###getAllUserNames

Get all usernames

Parameters:
username
password

Returns:
XML of usernames
___
###getAllUsers

Get all users

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all users
___
###lockUsers

Lock all users

Parameters:
Username
Password
maxFailedAttempts

Returns:
Status
___
###getInformationsAccess

Get All Informations Access

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Xml describing the groups.
___
###getCountsInformationsAccess

get count of information access

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlSectionNames
searchText

Returns:
Xml containing counts.	
___
###getAllGroups

Get All Groups

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Xml describing the groups.
___
###getAllUserVars

Get all user variables

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all user variables
___
###getCategory

Get the neurons from a category

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectName - Name of the category

Returns:
An XML document which describes the project
___
###getDashboardById

Get dashboard name and id.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardID - The id of the dashboard

Returns:
xml 4CB8CAF7-23C1-49DA-98B6-F8B51EF800BD Dashboard1 
___
###getDashboardsForUser

Get all dashboards for a certain user

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all dashboards for that user
___
###getDashboardsAndTabsForUser

Get all dashboards and associated tabs for a certain user

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all dashboards and tabs for that user
___
###getDashletOptionsForDashlet

Get all dashlet options for a certain dashlet

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashletID - ID of the dashlet

Returns:
XML describing all dashlet options for that dashlet
___
###getDashletsForDashboard

Get all dashlets for a certain dashboard

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
tabID - ID of the tab

Returns:
XML describing all dashlets for that dashboard
___
###getDataSourcebyName

Get all of the data sources

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the data sources

Returns:
XML describing all data sources
___
###getErrorText

Map an error code to text

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
errorCode - Error code to map

Returns:
The error string
___
###getExistingDatasources

Gets existing datasources and queries

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - the xml describing a dasboard

Returns:
XML containing all datsource names and queries
___
###getHosts

Get all the hosts Map an error code to text

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document which contains the host information
___
###getMonitoredStatistics

Get Statistics for Monitoring

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Monitoring Stats
___
###getNeuronConfiguration

Get a neuron instance configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the neuron

Returns:
An XML document which contains the neuron information
___
###getProjectForNeuron

Get the project name and id for a neuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name of the neuron

Returns:
An XML document which contains the project name and id
___
###getNeuronMessageStatus

Get the status of a neuron instance

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document which contains the neuron status
___
###getParentsForDashlet
Get the parent dashlet option for a dashlet.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashletID - The id of the dashlet

Returns:
95DD64DC-4AF3-4582-A75D-0ADBF6935431 SelectParent cont cont_x 0 
___
###getParentsPredefinedQueryDetails

Get predefined query details for more parents ids

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
queryId - XML of query ids

Returns:
The query details
___
###getPneuronProperties
Get a list with Corda and Host properties of Pneuron, from softwarerx.properties
Returns:
The list with required properties of Pneuron
___
###getPredefinedQueryById

Get a predefined query by ID

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
queryId - Queue ID

Returns:
An XML document describing the query
___
###getPredefinedQueryDetails

Get a predefined query details

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
queryId - Query ID

Returns:
The query details
___
###getProjects
Get the description of the projects

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectNamesXML - XML containig the names of the projects and the users ids that are selected for notes ( at the save action) Name1 Name2 Name3 1234.... 1234.... 
complexLoad - 0 - get specific data 1 - get all data
String - [] userWithNotes [user1, user2, user3]..... users that have the notes on neurons in the projects

Returns:
An XML document which describes the projects
___
###getProjectDetailsForECM

Get project details for ECM (neurons and user vars for projectId)

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId - Project id

Returns:
An XML document which describes the project details(neurons and user vars for a specified projectId)
___
###getProjectId

Get project id

Parameters:
Username - 
Password -
Dashn – project name

Returns:
Project id
___
###getQueriesByDataSource

Get all of the queries associated with a data source

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dataSourceId - Data source ID

Returns:
An XML document which describes the roles
___
###getQueryIdForQuery

Get the id of the query with a certain data source id and query name.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
datasourceId - ID of the data source for the query
queryName - the name of the query

Returns:
id for that query
___
###getRolePrivileges

Get all of the privileges associated with a role

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
roleId - Role ID

Returns:
An XML document which describes the privileges
___
###getUserPrivileges

Get all of the privileged associated with a role

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
roleId - Role ID

Returns:
An XML document which describes the privileges
___
###getSubProject

Get a given subproject

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - Project ID

Returns:
An XML document which describes the project
___
###getSubProjects

Get all of the subprojects for a project

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
parent_id - Parent project ID

Returns:
An XML document which describes the projects
___
###getSubProjectsMap

Get a map of the subprojects

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document which describes the map
___
###getSpecialConnections

Get Special Connections between pneurons and projects

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronId - Neuron Id gets all the connections for this pneuron
projectId - Project Id gets all the connections for this project

Returns:
An XML document which describes the connections
___
###getTabsForDashboard

Gets all tabs for a dashboard

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardID - ID of the dashboard

Returns:
XML describing all tabs for that dashboard
___
###getUserRoles

Get a user's roles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
userId - The ID of the user

Returns:
An XML document which describes a user's roles
___
###getUserVar

Get a user variable

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - The variable ID

Returns:
An XML document which describes the user variable
___
###getProjectForUserVar

Get the project for an user variable

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - The variable ID

Returns:
An XML document which describes the user variable
___
###getWhatIfResult

Get What If Result information

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - ID of the What If Result

Returns:
XML describing what if result
___
###loadDashboard

Load a new dashboard from XML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - XML created during an export call

Returns:
name of the loaded dashboard
___
###loadNeuron

Load a neuron instance

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
pneuron - Neuron name

Returns:
Status
___
###loadProjects

Load a one or more projects from XML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should this project be propagated
projectXML - XML created during an export call

Reurns:
Status
___
###getDatasourcesForOtherRoles

Get datasources that belong to users with other roles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectXML - The xml for the project

Returns:
The list of datasources that are created by another user
___
###getAliasWithRoles

Gets alias with roles

Parameters
Username
Password

Returns:
XML describing alias and roles
___
###moveNeurons
Move a list of neurons to another cateory

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - An XML document which describes the id of category where neurons will be moved and the ids of neurons

Returns:
Status
___
###moveNeuronsFromCategory

When a category is deleted the neurons are transfered to another cateory

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
oldParentId - The id of the deleted category
newParentId - The id of the new parent category
projectExists
Checks if the project name exists
Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlProjects - XML containing names and ids of the projects 
 
<projects> 
<project>

<name>Project1</name>
<id>0000001B_1373C4A9315_C0A80110_C73F </id>
</project>
<project>
<name>Project2</name>
<id>00000005_1374AB0D35F_C0A80110_E7AA</id>
</project>
<needRights>false</needRights>
</projects>
  
Returns:
  
<projects>

<name hasRights="1">Project1</name>
<name hasRights="1">Project2</name>
</projects>
           
hasRights: 1 if the project name exists and the user has the roles to override it, 0 if the project name does not exist, -1 if the project name exists and the user does not have the roles to override it, 2 if the project was renamed
___
###getExisitingNeurons

Check if neurons allready existin the database

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neurons - fooNeuron1 fooNeuron2 

Returns:
a string containing the duplicate names
___
###reloadNeuron
Reload a give neuron instance

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the reload be propagated to other servers
name - XML containing the names of the neurons to reload

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###reloadPNeuron

Reload a give neuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Names of the neuron to reload

Returns:
Status
___
###reloadNeurons

Reload all neuron instances

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the reload be propagated to other servers

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###reloadNeuronConfig

Reload configuration for all neuron instances

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###extractMessageTags

Returns message tags

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Configuration Xml message with neuron data

Returns:
Message tags separated by ;
___
###reloadProject
Reload the neurons from a given project

Parameters:
userName - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId - The id of the projects to reload

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###reloadTagSystem

Reload Tag System

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
___
###reloadTagHost

Reload Tag System

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateNeuronNotificationEvent

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId - The neurons project id
value - Value to be updated all the neurons EnableNotificationEvents field

Returns:
Status
___
###saveDashboard
Save (add/update) a dashboard to the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Describes the dashboard 
 
<dashboard>

<id/>

<name>NewDashboard</name>
</dashboard>
If node has no value it will do an insert, otherwise it will update for the that is specified.

Returns:
ID of the added/updated dashboard
___
###saveEcmSessionData
Save ECM session data of a certain dashboard

Parameters
Username
Password
dashboardID
content
isDelete

Returns:
Status
___
###updateEcmSessionData
Updates ECM session of a certain dashboard

Parameters:
Username
Password
dashboardId
content

Returns
Status
___
###saveDashlets
Save (add/update) a dashlets to the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Describes the dashlet 
 
<dashboard>

<id>00000016_13040B356EF_C0A8010D_154D</id>
<dashlets>
<dashlet>
<id>E9D68B1D-97C6-4E2C-A171-23E1486F55D7</id>
<widget_left>198</widget_left>
<widget_top>128</widget_top>
<widget_width>400</widget_width>
<widget_height>300</widget_height>
<name>DonutChart_1</name>
<widget_class>com.pneuron.dashboards.gwt.client.domain.designer.widget.DonutChart</widget_class>
<stack_order>0</stack_order>
<version>0</version>
<dashlet_options>
<dashlet_option>
<id>4CB8CAF7-23C1-49DA-98B6-F8B51EF800BD</id>
<group_name>Dashlet</group_name>
<property_name>Title</property_name>
<long_value>null</long_value>
<string_value>DonutChart_1</string_value>
<version>0</version>
</dashlet_option>
<dashlet_option>
<id>BE900F4E-3349-4D84-80B4-82A77A9722BB</id>
<group_name>Chart</group_name>
<property_name>Height</property_name>
<long_value>300</long_value>
<string_value>null</string_value>
<version>0</version>
</dashlet_option>
<dashlet_option><id>94901356-38CC-430A-89A6-849DF7DCC605</id>
<group_name>DataSource</group_name>
<property_name>default</property_name>
<long_value>null</long_value>
<string_value>DataSource@#@DataSourceNameInHere@#@00000003_12CA667FBCD_C0A80259_0B8C@#@f83e8933-00e0-41ad-9eb4-d20e25e11111</string_value>
<version>0</version>
</dashlet_option>
<dashlet_option>
<id>7189FF07-07F3-4809-95C5-672950932D8B</id>
<group_name>UserVar</group_name>
<property_name>UserVariableNameInHere</property_name>
<long_value>null</long_value>
<string_value>UserVar@#@00000016_13040C71997_C0A8010D_1EC1@#@uservar@#@0&#64;#@100&#64;#@@#@00176A09_12B9BF1353B_0ACAC790_A2A5@#@GetDataFromECM@#@</string_value>
<version>0</version></dashlet_option>
<dashlet_option><id>59D0D376-7981-4904-84D6-652886A80A87</id>
<group_name>ToggleNetwork</group_name>
<property_name>ToogleNetworkNameInHere</property_name>
<long_value>null</long_value>
<string_value>ToggleNetwork@#@00000029_1301D3E33B4_C0A8010D_B805@#@NeuronDB@#@</string_value>
<version>0</version> </dashlet_option> </dashlet_options> </dashlet>
</dashlets> </dashboard> 
           
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###saveProperty
Save a property (add or update)

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - The value of the field name
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
saveWhatIfResult
Save (add/update) a What If Result to the environment
Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Describes the What If Result Information 

<what_if>
<id/>
<test_result>Awaiting Test Results.....</test_result>
<version>0</version>
</what_if>
            
If node has no value it will do an insert, otherwise it will update for the that is specified

Returns:
ID of the added/updated What If Result
___
###unloadNeuron

Unload a give neuron instance

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
pneuron - Name of the neuron to reload

Returns:
Status
___
###updateCategory
Update an existing category from the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name for the category
id - ID of the category that we want to update
X - X coordinate of the category that we want to update
Y - Y coordinate of the category that we want to update

Returns:
STATUS_SUCCESS, STATUS_FAILURE
___
###updateHost
Updates host

Parameters
Username
Password
Name
Id
isLoadBalancing
Returns:
Status
___
###getNeuronsForId
Get Pneurons from given list of Ids

Parameters
Username
Password
Ids

Returns:
Pneurons and description
___
###updateNeuron
Update an existing pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should this project be propagated
configurationXML - 
            
<xml>

<id>000000A0_125500DE574_7F000001_4E2D</id>
<X>117</X>
<Y>337</Y>
<properties>
<PersistMessage type="string">FALSE</PersistMessage>
<DbQueryInterval type="integer">0</DbQueryInterval>
<Query type="string">[Change Me]</Query>
<DbSource type="string">[Change Me]</DbSource>
</properties>
<connections>
<connection action="add" condition="">Print</connection>
<connection action="delete">Print2</connection>
</connections>
</xml>
 
Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateMultipleNodePositions
Update the coordinates of one or multiple nodes

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should this project be propagated
configurationXML - 
            
<nodes>
<node>
<id>00000011_1374B61351A_C0A80110_E7AA</id>
<name>projectA</name>
<x>12</x>
<y>-2</y>
<type>neuron</type>
</node>
</nodes>
 
Returns:
empty string if success, names of projects that could not be updated or "ERROR" for error in connection
___
###updateNeuronTypes
Update Pneuron Type

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - type id
name - type name
className - java class
image - image address

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updatePrivilege
Update an existing privs from the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name for the role
id - The id of the privilege to be updated

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateProject
Update an existing project from the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name for the project
id - ID of the project that we want to update
X - X coordinate of the project that we want to update
Y - Y coordinate of the project that we want to update

Returns:
STATUS_SUCCESS, STATUS_FAILURE
___
###updateRole
Update an existing role from the environment

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name for the privs
id - ID of the privs that we want to update

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateRolePrivileges
Update a roles privileges

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - XML description of the role's privileges 
            
<xml>

<id>0000000A_12AC8E02EDA_0A000093_9331</id><name>User Role</name>
<privileges>
<privilege>
<id>00000005_12AC8E02ED3_0A000093_9331</id><name>Designer Privilege</name>
</privilege>
</privileges>
</xml>

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateUserPrivileges
Updates user privileges

Parameters
Username
Password
Xml - xml list of privileges you want updated

Returns
Status
___
###updateUserRoles
Update user roles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - XML description of the user's roles

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###updateUserVar
Update user variable

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
applicationName - Application from where the request is made
xml - XML description of the user variable update

Returns:
Status
___
###validateSASFile
Validates the SAS and XML files and if correct creates a JAR file

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
sasFileContent - Content of the SAS file
xmlFileContent - Content of the XML file

Returns:
The name of the namespace if conversion was correct, the error if the conversion failed
___
###generateServiceLibrary
Generates Jar Library using wsdl shell batch execution

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
url - webservice url address
neuronId - Current Neuron Id

Returns:
Jar library file name to be used within the neuron properties
___
###getPneuronPropertiesList
Get properties values from softwarerx.properties

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
propertyNames - XML with properties and their values . . . Xml of property names for which we want to obtain the value Name1 Name2 Name3 

Returns:
values for the specified properties
___
###getAllFiringPneurons
Provides a list of Pneurons that can fire the network for the current user

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all pneurons with firing properties
___
###getAllFiringPneuronsForCurrentHost
Provides a list of current host's Pneurons that can fire the network for the current user

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing all pneurons with firing properties
___
###getAllDebuggingPneurons
Provides a list of Pneurons that are in debug mode for the current user
Parameters:
userName - 
password - 
projectId - 
pneuronName - 
pneuronHost - 
pneuronClass - 

Returns:
XML of all pneurons in debug mode
___
###getAllDebuggingPneuronsForCurrentHost

Provides a list of current host's Pneurons from the current host that are in debug mode for the current user

Parameters:
userName - 
password - 
Returns:
XML of all pneurons in debug mode for host
___
###getLibraryClasses

Get library class

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
jarLibraryFileName - Jar File Name

Returns:
XML describing all classes available within the Jar Library
___
###getLibraryClassMethods

Get library class methods

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
jarLibraryFileName - Jar File Name
classPath - Full Class Path, Namespace and Class Name

Returns:
XML describing all methods available within the specified Class
___
###getWrapperLibraries
Gets all wrapper libraries

Parameters:
Username
Password

Returns:
XML of wrapper libraries
___
###getLibrariesForType
Get libraries for given type

Parameters:
Username
Password
Types

Returns:
XML describing libraries of given type
___
###validatePaths
Validate paths

Parameters:
username
password
paths

Returns:
Success or fail or invalid login
___
###cloneDmAlias
Copy an alias environment

Parameters:
aliasName - Alias name
srcAliasEnvironment - Source environment
dstAliasEnvironment - Destination environment

Returns:
Status

___
###cloneDmEnvironment
Copy an alias environment
Parameters:
aliasName - Alias name
srcAliasEnvironment - Source environment
dstAliasEnvironment - Destination environment

Returns:
Status
___
###getInfoAccessAvailablePrivileges

Checks what privileges from InfoAccess can be enabled for an user.

Parameters:
username - Username to be checked
password - Password to be checked

Returns:
An XML document containing the InfoAccess privileges available for user
___
###getUserVarsByIds

Get user variable by Id.

Parameters:
Username
Password
uvId

Returns:
XML doc of user variables
___
###checkIfClassExists

Checks if class exists

Parameters:
Username
Password
classFullPath
Returns:
Status
___
###saveNeuronNote

Method adds or updates an existing note associated by an user to a pneuron

Parameters:
username - Username to be used to authenticate with the server and to add the note to a pneuron
password - Password to be used to authenticate with the server and to add the note to a pneuron
noteId - Note Identifier to be used if a note needs to be updated, leave blank if you need to add and not update
pneuronId - Pneuron reference (identifier)
note - Note body

Returns:
Status
___
###deleteNeuronNote

Method deletes an existing note using the note identifier

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
noteId - Note Identifier used to identify note in order to delete

Returns:
Status
___
###getNeuronNotes

Method gets all the notes associated with a pneuron instance < >Created: Cristian Blaga

Parameters:
username - Username to be used to authenticate with the server and to add the note to a pneuron
password - Password to be used to authenticate with the server and to add the note to a pneuron
noteId - Note Identifier to be used if a note needs to be updated, leave blank if you need to add and not update
pneuronId - Pneuron reference (identifier)
note - Note body

Returns:
returns all notes for pneuron
___
###getFromInformationForDebug

Get all projects and the corresponding from_pneurons which send debugging messages

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing the projects and pneurons
___
###getToInformationForDebug

Get all projects and the corresponding to_pneurons which receive debugging messages from

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fromPneuron - Pneuron name - source of messaging

Returns:
An XML document describing the projects and pneurons
___
###getFieldsNameForDebug

Get all unique fields from messages_values between

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fromPneuron - Pneuron name - source of messaging
toPneuron - Pneuron name - destination of messaging

Returns:
An XML document describing the projects and pneurons
___
###getMessagesInformationForDebugBySearchingCriteria

Get informations about the debugging messages between

Parameters:
fromPneuron - and
toPneuron - taking in consideration searching criteria
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fromPneuron - Pneuron name - source of messaging
toPneuron - Pneuron name - destination of messaging
fieldsList - List of fields from messages_values
searchedValue - Pneuron name - destination of messaging
orderByTicksSent - type of ordering the results: asc or desc
limit - Number of results that will be returned

Returns:
An XML document describing the projects and pneurons
___
###cleanDebugForProject

Cleans all the debug information associated with the network/project idendified using

Parameters:
projectName - or
projectId - 
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectName - Project name - Network Name
projectId - Project Id - Project Unique Identifier

Returns:
Execution Status Login Failure/Success/Failure
___
###getDebugConfigurationForProject
Gets all the pneuron debug settings for a provided project, identified using

Parameters:
projectName - or
projectId - 
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectName - Project name - Network Name
projectId - Project Id - Project Unique Identifier

Returns:
Project Debug Settings for all pneurons.
___
###saveDebugConfigurationForProject
Saves debug settings for provided pneurons, identified using

Parameters:
xml - 
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Xml - stream contains pneuron id, debug state, and hops

Returns:
Execution Status Login Failure/Success/Failure
___
###extractAnalyticTags
Extract all the generated tags/store variables defined within

Parameters:
analyticInstructionBody - instruction body list
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
analyticInstructionBody - Instruction Xml String

Returns:
Generated Tags as Xml/String
___
###saveProjectInPanel
Creates new panel or add to existing panel the list of projects specified

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
panelId - Panel Id - existing panel id
projectIdList - Project List separated by ;
isGlobalPanel - If the destination panel is global

Returns:
Execution Status Success/Failure/Invalid Login
___
###removeProjectFromPanel
Removes from panel the list of projects specified

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
panelId - Panel Identifier
projectIdList - Project List separated by ;

Returns:
Execution Status Success/Failure/Invalid Login
___
###removeProjectsFromAllPanels
Removes the list of projects from all panels (global and local)

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectIdList - Project List separated by ;

Returns:
Execution Status Success/Failure/Invalid Login
___
###removePanel
Removes panel

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
panelId - Panel Identifier

Returns:
Execution Status Success/Failure/Invalid Login
___
###getPanelsForUser
Get Panels for User - get panel list

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
xml message (as string) containing all the panels declared by user
___
###getProjectsInPanel
Get Projects in Panel

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
xml message (as string) containing all the projects from panel, with their privileges
___
###renamePanel
Removes panel

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
panelId - Panel Identifier

Returns:
Execution Status Success/Failure/Invalid Login
___
###setPanelsOrder
Set order of panels

Parameters:
username
password
ids

Returns:
Status
___
###getCacheBatchSize
Gets batch file size

Parameters:
username
password

Returns:
Batch cache record size
___
###getPaletteOrderForUser

Get Palette order for User

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
xml message (as string) containing the palette order declared by user

<xml>

<category id= "ID"> 
<name> all </name> 
<neuron_order> Order of all the neurons icons separed by ";" </neuron_order> 
</category> 
<category id= "foo"> 
<name> analytics </name> 
<neuron_order>Pneuron Project;Custom Neuron;com.pneuron.neurons.matching.MatchingAnalyticNeuron;com.pneuron.neurons.analytic.AnalyticNeuron;com.pneuron.neurons.predictive.SasNeuron; </neuron_order> 
</category> 
</xml> 
___
###savePaletteOrderForUser
Saves palette order for user, idendified using

Parameters:
xml - 
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - Xml - stream contains name of the category and the neuron order

Returns:
Execution Status Login Failure/Success/Failure
___
###delDmAlias
Delete an alias

Parameters:
aliasName - Alias name

Returns:
Status
___
###addEnvironment
Add new environment

Parameters:
username
password
name
comment

Returns:
Status
___
###deleteEnvironment
Delete environment

Parameters:
username
password
name

Returns:
Status
___
###getAllEnvironments
Gets all environments

Parameters:
username
password
searchText

Returns:
XML doc containing all environments and details
___
###updateEnvironment
Updates environment

Parameters:
username
password
oldName
newname
comment
getAliasTypes
get all alias types
parameters
username
password

Returns:
XML doc containg all available alias types
___
###deleteAlias
Deletes an alias by name

Parameters:
username
password
aliasName

Returns:
Status
___
###updateAlias
Updates alias

Parameters
username
password
oldName
newName

Returns:
Status
___
###checkIfAliasExist
Checks if alias exists

Parameters:
username
password
alias – alias name

Returns:
True or false
___
###addAlias
Add a new alias

Parameters:
username
password
name
typeId

Returns:
Status
___
###findAlias
Find a certain alias

Parameters:
username
password
filterName
filterType
env
envStatus
applicationName

Returns:
XML doc of all found aliases
___
###getEnvironmentForAlias
Get environment for a given alias name

Parameters:
username
password
aliasName

Returns:
XML doc describing evironment
___
###getAliasDriverXML
Gets alias driver XML template

Parameters:
username
password
aliasType
environmentName

Returns
XML template of alias
___
###saveAliasAttributes
Save alias attributes

Parameters:
username
password
attributesXML
alias
environment

Returns:
Status
___
###addAliasWithAttributes
Add alias with attributes

Parameters:
username
password
name
typeId
attribXml

Returns:
Status
___
###testAliasDriver

Runs test command for given alias driver

Parameters:
username
password
alias
environment

Returns:
Status
___
###getAttributesForAliasType
Notifies Deployment Manager to reload

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns
Attributes for alias types
___
###getHostsHealth
Get Health for all Hosts within the platform

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Xml as String with all the hosts and their status
___
###resetHostsHealt
Reset the status for all the Hosts

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Xml as String with all the hosts and their status
___
###copyPneuron
Copy a list of neurons

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server 
neuronsXML - XML containing original neuron Id, copy name, host

Returns:
Status
___
###validateDriverAttributes
Validate Attributes for Driver Alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
driverType - Driver Class Name
xmlAttributes - Driver attributes - defined as XML containing name and value

Returns:
validation status as XML
___
###testAliasDriverWithAttributes
Test connection for DBSourceAlias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
driverType - Driver Class Name
xmlAttributes - Driver attributes - defined as XML containing name and value

Returns:
error message or "success"
___
###getDirectoryStructure
Gets Directory Structure

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
path - Directory File Path on local machine

Returns:
directory entries (files, sub-directories and link file) as XML
___
###getDetailDirectoryStructure

Gets Detailed Directory Structure

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
path - Directory File Path on local machine

Returns:
directory entries (files, sub-directories and link file) as XML
___
###removeResource
Remove Resource - Directory/File Entry

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
path - Directory/File Path on local machine
fileName - File Name on local machine to be removed/deleted

Returns:
Status
___
###indexSearch
Search Index Directory

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
indexAliasId - Index Alias Identifier

Result:
Status
___
###indexCheck
Check if Index Directory exists

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
indexAliasId - Index Alias Identifier

Returns
True/False
___
###updateIndex
Start Update Index Process

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
indexAliasId - Index Directory Path

Returns:
Status
___
###saveTemplate
Update or add a new template.If the id from xml is null then the template is added otherwise is updated.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
id of the templated
___
###getTemplateByName
Get template by name.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - Name to be used to find the template

Returns:
An XML document describing the templates properties. 
___
###getAllTemplatesDetails
Get all templates details.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing the templates properties. 
___
###getAllTemplates
Get all templates.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document containing all templates with their properties. 
___
###updateTemplate
Update an existing templateName

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
oldName - Old Name for the templates
newName - New name for the templates

Returns:
Status
___
###deleteTemplateById
Delete Template by id.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - The template id to be deleted

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE

___
###copyTemplate
Copy an template

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
templateId - The original template id
templateTab - The original template tab
copyTemplateName - New name for the template copy

Returns:
Status
___
###saveMapEntityXML
Save the group map entity and its association to directory aliases.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
id of the map entity.
___
###deleteMapGroupById
Delete index map group by id.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - The index map group id to be deleted

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###getAllMapGroupsXML

Get all map group entities.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document containing all map group entities with their id and name. 
___
###getAliasesForGroup
Get all directory aliases for the group map

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - Id of the group map

Returns:
An XML document containing all the directory aliases associated to the group map 
___
###getAllStoreProceduresFromAlias
Gets all stored procedures from data source alias

Parameters:
username
password
aliasName

Returns:
XML doc of stored procedure names
___
###getAllParamsFromStoreProcedures
Get all parameters from a stored procedure in a data source alias

Parameters:
username
password
aliasName
procedureName
schemaName

Returns:
XML doc of all parameters in stored procedure
___
###getAllExecutionSchedule
Get all configured directory schedules

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all of the known directory schedules
___
###saveExecutionScheduleEntityXML
Save execution schedule
Parameters:
username
password
xml – XML descriving execution schedule

Return:
Status
___
###resetIndexSchedule
Resets index schedule

Parameters:
username
password
type

Returns:
Status
___
###deleteExecutionScheduleById
Deletes execution schedule using given Id.

Parameters:
username
password
id

Return:
Status
___
###getDataFormat
Get data format by type or description

Parameters:
username
password
searchType
searchDescription

Result:
XML doc of all data formats found from search
___
###saveDataFormat
Save a data format

Parameters:
username
password
id
type
format

Returns:
Status
___
###deleteDataFormat
Delete a certain data format by id

Parameters:
username
password
id

Returns:
Status
___
###getExistingTemplatesFromXML
Get all template names that exist in the database and in the templatesXML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
templatesXML - An XML document describing template names to check if they exist in the database

Returns:
An XML document describing template names
___
###checkExistingNameForWidget
Check if a dashlet name is already taken in the specified dashboard

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name - The Name that need to be verified
dashboardId - The id of the dashboard where the names will be checked
dashletId - The id of the dashlet which will be checked

Returns:
returns true for an existing name, false otherwise
___
###getDashletNotes
Gets all notes associated with a dashlet Id.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashletId

Results:
XML doc containing notes for dashlet
___
###deleteDashletNote
Deletes dashlet note given its id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
noteId

Returns
Status
___
###saveDashletNote
Save a note to a dashlet

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
noteId
dashletId
note

Returns:
Status
___
###resetStatisticsForProject
Reset statistic for a project

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectXML
fPropogate

Returns:
Status
___
###resetStatisticsForPneuron
Reset statistics for a Pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuoronsXML
shouldFire
fPropogate

Returns:
Status
___
###connectGenericErrorBranch
Create a generic error branch connection.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId
neuronId
alwaysUse

Returns:
Status
___
###disconnectGenericErrorBranch
Disconnect a generic error branch connection

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId
neuronId

Returns:
Status
___
###resetGenericErrorBranchConfiguration
Resets configuration for generic error branch

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate

Returns:
Status
___
###getGenericErrorConfiguration
Get configuration of a generic error by project Id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId

Returns:
XML doc of generic error configuration
___
###saveGenericErrorConfiguration
Save configuration of generic error

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId
configXML

Returns:
Status
___
###updateNodesImage
Update the image of a node

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
nodesId
image
isNormalSize
isBold
isProject

Returns:
Status
___
###getCaseNeuronConfiguration
Get XML config of Case Pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronId

Returns:
XML of Case pneuron configuration
___
###getCaseNeuronForbiddenDestinations
Get XML of forbidden destinations of Case Pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronId

Returns:
XML of Case pneuron forbidden destination
___
###saveCaseNeuronConfiguration
Save configuration of Case Pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronId
branchXML

Returns:
Status
___
###containsNeurons
Does a certain project contain Pneurons

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectIds -

Returns:
XML of project names and whether they contain Pneurons or not.
___
###copyDashboard
Copy a dashboard

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
srcDashboardId
dstDashboardName

Returns:
Status
___
###copyDashboardTab
Copies a dashboard tab

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
doc

Returns:
Status
___
###getAllProjectsOrDashbords
Get all of the known projects o dashboards

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document descibing the projects
___
###checkNeuronNameIfExists
Checks if there is already defined a pneuron with the provided name

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronName - Neuron Name to be checked

Returns:
True - neuron name already used; False - neuron name not used
___
###getWidgetsOrderForUser
Get widgets order for User for ECM

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
xml message (as string) containing the widgets order declared by user
___
###saveWidgetsOrderForUser
Saves widgets order for user, idendified using

Parameters:
xml - 
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
stackName - Stack name: Basic or Extendet
stackName - Contains the names of the widgets in order

Returns:
Execution Status Login Failure/Success/Failure
___
###getCategoriesForProjects
Get the categories for selected projects

Parameters:
username - 
password - 
projectIds - the list od projects ids

Returns:
XML of categories.
___
###getUsersWithNotesForProjectsIds
Get all Users with notes for projects ids = listProjId have dependencies

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
listProjId - Ids of the projects

Returns:
Users with notes
___
###getUsersWithNotesForDashletsIds
Get a list of all users with notes given dashlet ids.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlDashletIds

Returns:
XML of users with notes for given dashlet
___
###getDashboardXmlWithNotes
Get dashboard description and notes

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardID - ID of the dashboard
userNamesXML - XML with user ids for the export of notes; null if the user doesn't have ADMIN role

Returns:
XML describing dashboard
___
###getAliasUsage
Get the resources name which use the alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName - Name of the alias

Returns:
In case of success returns an xml containing the list of neurons and queries which use the alias OR empty string in case that the alias is not used.In case of error returns null
___
###copyWidgets
Copy widgets

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName - Name of the alias

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###getDashboardsAndWidgetscopyWidgets
Returns the xml containing the dashboards and all widget names from the dashboards

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardIds - Dashboard id's list

Returns:
The xml containing the dashboards and all widget names from the dashboards
___
###moveWidgets
Move widgets

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName - Name of the alias

Returns:
STATUS_INVALID_LOGIN, STATUS_SUCCESS, STATUS_FAILURE
___
###getAllDistinctHostsForProjectIds
Returns the xml containing the distinct hosts used in the projectsIds

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectsIds - Projects ids

Returns:
The xml containing the distinct hosts used for the projectsIds given
___
###getNotificationAliasSource
Get notifications from a source alias

Parameters:
username - Username to be used to authenticate with the server.
password - Password to be used to authenticate with the server.

Returns:
XML of notifications of alias
___
###getNotificationConfigurationSource
Get notification configuration source

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName - Name of the alias

Returns:
XML of notifications of configuration
___
###getRunningEnvironment
Get running environment details

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML description of running environment
___
###getCloudIdentifier
Get cloud identifier

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Cloud identifier
___
###getProjectsForNeuronNames
Get all the known projects for the selected Pneuron names

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
neuronNames - List of neuron names

Returns:
An XML document describing the projects
___
###virtualizationKill
Kill Virtualization

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate - 

Returns:
Status
___
###virtualizationReloadAll
Reload virtualization

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate - 

Returns:
Status
___
###virtualizationLoadProject
Kill virtualization

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectId
fPropogate - 

Returns:
Status
___
###virtualizationUnloadProject
Unload a project

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate 
projectId - 

Returns:
Status
___
###virtualizationReloadProject
Reload a project

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate - 

Returns:
Status
___
###virtualizationLoadPneuron
Load a pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name
fPropogate - 

Returns:
Status
___
###virtualizationUnloadPneuron
Unload a pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name
fPropogate - 

Returns:
Status
___
###virtualizationReloadPneuron
Reload a pneuron

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name
fPropogate - 

Returns:
Status
___
###virtualClusterLoad
Load a cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterName
fPropogate - 

Returns:
Status
___
###virtualClusterReload
Reload a cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterName
fPropogate - 

Returns:
Status
___
###virtualClusterStart
Load a cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterName
fPropogate - 

Returns:
Status
___
###virtualClusterKill
Kill a cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterName
fPropogate - 

Returns:
Status
___
###virtualClusterKillAll
Kill all clusters

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropogate - 

Returns:
Status
___
###getAllNotificationTags
Get all notification tags

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name
parentName
systemDef
isActive

Returns:
XML containing all tags
___
###saveNotificationTag
Save a notification tag

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###deleteNotificationTag
Delete notification tag

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - 

Returns:
Status
___
###getAllNotification
Get all notifications

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlFilter - 

Returns:
XML containing all notification tags
___
###saveNotification
Save a notification

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###deleteNotification
Save a notification

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - 

Returns:
Status
___
###getTagsAssociatedToNotification
Get tags that are associated with a notification

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
notificationId - 

Returns:
XML containing tags.
___
###saveTagsAssociatedToNotification
Save a tags associated with a notification

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###getAllNotificationBodys
Get all notification bodies

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlFilter - 

Returns:
XML containing all notification bodies
___
###saveNotificationBody
Save a notification body

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###deleteNotificationBody
Delete a notification

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - 

Returns:
Status
___
###getAllNotificationDrivers
Get all notification dirvers

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
bodyId - 

Returns:
XML containing all notification driver descriptions
___
###saveNotificationDriver
Save a notification driver

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###deleteNotificationDriver
Delete a notification driver

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
notificationDriverId - 

Returns:
Status
___
###getNotificationDetails
Get notification details

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
notifiactionID - 

Returns:
XML containing details of the notification.
___
###updateActiveStateForNotifications
Update active state for notifications

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xmlFilter
activate - 

Returns:
Status
___
###updateActiveStateForAllErrors
Update active state for all errors

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
activate - 
Returns:
Status

Returns:
Status
___
###addCluster
Add cluster object definitions

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###deleteCluster
Delete cluster object definitions by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###updateCluster
Update cluster object definitions

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###activateCluster
Activate cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###getAllClusterDefinitions
Get all cluster object definitions

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###getClusterNamesForProjectId
Get cluster name for project id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
the cluster name
___
###getAllClusterProblemsByClusterId
Get cluster name for project id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId 

Returns:
XML contain all issues with cluster
___
###getClusterPriorityAlgorithmsById
Get Cluster Priority Algorithms By Id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###getAllClusterPriorityAlgorithms
Get All Cluster Priority Algorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###addClusterPriorityAlgorithms
Add cluster PriorityAlgorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###deleteClusterPriorityAlgorithms
Delete cluster Priority Algorithms by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateClusterPriorityAlgorithms
Update cluster PriorityAlgorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###getAllClusterDispatchAlgorithms
Get All Cluster DispatchAlgorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###addClusterDispatchAlgorithms
Add cluster Dispatch Algorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###deleteClusterDispatchAlgorithms
Delete cluster Dispatch Algorithms by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateClusterDispatchAlgorithms
Update cluster PriorityAlgorithms

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###getClusterDispatchAlgorithmsById
Get Cluster Dispatch Algorithms By Id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###getAllClusterHostType
Get All Cluster Host Type

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###addClusterHostType
Add cluster Host Type

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###deleteClusterHostType
Delete cluster Host Type by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateClusterHostType
Update cluster object definitions

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###getClusterHostTypeById
Get Cluster Host Type By Id get

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###getAllClusterHostsByClusterId
Get All Cluster Hosts By Cluster Id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all know cluster definitions
___
###addClusterProblem
Add cluster problem

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###deleteClusterProblem
Delete cluster problem by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateClusterProblem
Update cluster problems

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###activateClusterProblem
Activate cluster problems

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###getAllNeuronsForProjectId
Get neurons for projects id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
An XML document describing all neurons for project id
___
###getAllClusterHostProblemsById
Get all cluster host problems by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
problemId -

Returns:
An XML document describing all cluster host problems
___
###addClusterHostProblem
Add cluster host problem

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###deleteClusterHostProblem
Delete cluster host problem by id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###updateClusterHostProblem
Update cluster problems

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###addClusterHost
Add Cluster Host

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###deleteClusterHost
Delete cluster Host

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###updateClusterHost
Update cluster host

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Results:
Status
___
###activateClusterHost
Activate cluster host

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId
id
hostStatus

Results:
Status
completeClusterWork
Complete cluster work

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
problemId - Problem id
messageId - Message id
transactionId - Transaction id
host – Host string

Results:
Status
___
###virtualClusterKillTransaction
Virtual killing of cluster transaction

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
problemId - Problem id
transactionId - Transaction id
fPropogate – 

Results:
Status
___
###virtualClusterStartHost
Virtual cluster start host.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
hostname -  Host string
fPropogate - 

Results:
Status
___
###virtualClusterStopHost
Virtual stop of cluster host.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
hostname -  Host string
fPropogate - 

Results:
Status
___
###virtualClusterQuiesceHost
Virtual quiesce host of cluster.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
hostname -  Host string
fPropogate - 

Results:
Status
___
###virtualClusterResumeHost
Virtual resume host of cluster.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
hostname -  Host string
fPropogate - 

Results:
Status
___
###virtualClusterRefreshFriendlyName
Virtual refresh of friendly names.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
fPropogate - 

Results:
Status
___
###virtualClusterCheckProject
Virtual check cluster project.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId - Cluster id
hostname -  Host string
fPropogate - 

Results:
Status
___
###virtualClusterGetInflight
Get inflight messages of cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterName -  Host string
fPropogate - 

Results:
XML of inflight messages
___
###databasePropertiesGetForId
Get database properties for cluster

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - Cluster id

Results:
XML describing database properties.
___
###aliasNameExists
Does alias exist.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName
aliasId - Cluster id

Results:
True/false
___
###saveDataToFile
Write Data To a file

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fileType - Type of file (csv, xml, xls etc.)
fileName - Name of the file
path - Path of the file
relativePath - Relative path of the file
additionalInfo - For example for excel it contains the sheet name
columnNames - For example for csv is the first row
content - A matrix that contains the content

Returns:
Status
___
###removeConnections
Removes connections

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
connectionsXML - XML containing a list of connections to remove

Returns:
Status
___
###changeConnectionTypes
Change connection types

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
connectionsXML - XML containing a list of connections and the new type

Returns:
Statsus
___
###getUsersReport
Get all users reports

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML of user report
___
###getMailConfigurations
Get mail configuration map (id and name)

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML of mail configurations
___
###updateGlobalProperties
Update global properties

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - An xml containing names and values of the properties

Returns
Status
___
###activateAccounts
Activates accounts

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###inactivateAccounts
Inactivate accounts

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML containing inactive accounts
___
###markAccountsAsDeleted
Marks accounts as deleted

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###notifyInactiveAccounts
Sends an email with the accounts that will become inactive

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
Status
___
###updateSecurityPolicies
Updates all security policies from the db

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fPropagate - Should the addition be propagated to remote servers

Returns:
Status
___
###getAllMailConfigurations
Gets all mail configuration from db

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML containing all mail configurations
___
###insertMailConfiguration
Inserts mail configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
mailConfigurationXML - XML containing mail configuration attributes

Returns:
one of the following strings "error", "name_exists", "success"
___
###updateMailConfiguration
Updates mail configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
mailConfigurationXML - XML containing mail configuration attributes

Returns:
Status
___
###deleteMailConfiguration
Deletes mail configuration

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
mailConfigurationName - mail configuration name

Returns:
1 for success, 0 failure
___
###getGlobalProperties
Get global properties by names

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
an XML document containing all the values from @propNamesList
___
###saveLibraryData
Save library data.

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
fileAddress
parameters - 

Results:
Status

___
###getLibraryDetails
Get details of a library given id

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id - id

Results:
XML describing details of library.
___
###getLicenseServerDateTime
Gets the date time of the license server

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
an XML document containing server time and time zone
___
###getUserVarsWithRoles
Get all uservars names that exist in the database and in the queriesXML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectXML - An XML document describing the project to upload
projectNames - list of project names

Returns:
An XML document describing uservars names
___
###getQueriesWithRoles
Get all queries names that exist in the database and in the queriesXML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
projectXML - An XML document describing the project to upload
projectNames - list of project names

Returns:
An XML document describing query names
___
###findGlobalPanelsForUser
Get Panels for User - get panel list

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
xml message (as string) containing all the panels declared by user
___
###addPanel
Add Design Studio panels

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
panelName - Panel Name - new or existing panel name

Returns:
Execution Status Success/Failure/Invalid Login
___
###findWidgetsUsingQuery
Return an xml containing information about widgets (dashboard, tab, widget name) that use a query (excepting the widget with the given widgetId)

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
queryName - Name of the query to be checked
widgetId - Id of widget not to be included in the search

Returns:
Execution Status Success/Failure/Invalid Login
___
###getProjectIAMs
Get project IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getAliasIAMs
Get alias IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getUserVariableIAMs
Get user variable IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getDefinedQueryIAMs
Get define query IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getDashboardIAMs
Get dashboard IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getWidgetIAMs
Get widget IAMs

Parameters:
Argument – argument used to get IAMs

Returns:
XML describing IAM
___
###getAllDashboards
Get all dashboards

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing each dashboard
___
###getAllDashlets
Get all dashlets

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML describing each dashlet
___
###saveProjectIAMs
Save project IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###saveAliasIAMs
Save alias IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###saveUserVariableIAMs
Save user variable IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###saveDefinedQueryIAMs
Save defined query IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###saveDashboardIAMs
Save dashboard IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###saveWidgetIAMs
Save widget IAMs

Parameters:
filterInfo – info used for filtering
saveInfo – Info you want saved

Returns:
Status
___
###getSingleDashboardIAMs
Get a dashboard IAMs

Parameters:
filterInfo – Info used for filtering

Returns:
Status
___
###updateAdditionalAttribute
Update additional alias attribute

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id
name
value
isSecured

Returns:
Status
___
###deleteAdditionalAttribute
Delete additional alias attribute

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id

Returns:
Status
___
###getAdditionalAttributes
Get addition alias attribute

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id
aliasXml

Returns:
Status
___
###exportAlias
Export alias 

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasName
envName

Returns:
XML containing alias details. Capable of being imported.
___
###importAlias
Import alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasXml
override

Returns:
Status
___
###decryptAliasValue
Decrypts an alias value

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
value

Returns:
Status
___
###directoryAliasCreateFolder
Creates a folder in a given directory alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasId
path

Returns:
Status
___
###directoryAliasDeleteFolder

Delete folder in directory alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasId
path

Returns:
Status
___
###saveDashletsOptions
Updates dashlet options

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml - 

Returns:
Status
___
###checkDirectoryAliasDiskSpace
Gets disk space of directory alias

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasId

Returns:
Disk space
___
###directoryAliasRenameFile
Get addition alias attribute

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
aliasId
filePath
newFilePath
option

Returns:
Status
___
###addNewDashboard
Add a new dashboard

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardName

Returns:
Status
___
###savePossibleValue
Save a possible value

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
oldName
dashboardId
possibleValueXML

Returns:
Status
___
###getPossibleValues
Get possible values

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId

Returns:
Status
___
###deletePossibleValue
Delete possible values

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId

Returns:
Status
___
###saveECMSessionValuesAndFormControls
Save ECM values and form controls

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId
sessionValuesXML
forControlXML

Returns:
Status
___
###getDashboardsFormControlsAndPossibleValues
Get ECM dashboard values and form controls

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardIds

Returns:
XML of dashboards values and form controls
___
###copyFormControlsAndPossibleValuesToDashboards
Copy ECM values and form controls

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml

Returns:
Status
___
###getClusterScaling
Get cluster scaling

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
clusterId

Returns:
Cluster scaling description
___
###saveClusterScaling
Copy ECM values and form controls

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id
clusterId
hypervisorId
scaleUp
scaleDown

Returns:
Status
___
###saveHypervisor
Save Hypervisor

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id
friendlyName
classPath
parameters
state

Returns:
Status
___
###setHypervisorState
Set hypervisor State

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
id
state

Returns:
Status
___
###searchHypervisor
Search hypervisor State

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
name
classPath

Returns:
Any found hypervisors
___
###scalingParameterDefinitionToXml
Add scaling definition to XML

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server

Returns:
XML of scaling definition
___
###saveDashboardFormControlBindings
Save dashboard from control bindingd

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
xml
metadataXml

Returns:
Status
___
###getDashboardFormControlBindings
Get dashboard forn control bindings

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId

Returns:
XML of dashboard control bindings
___
###saveDashboardFormControlToggles
Save dashboard form control toggles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId
metadataXml

Returns:
Status
___
###getDashboardFormControlToggles
Get dashboard form control toggles

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardToggleId

Returns:
Status
___
###deleteDashboardFormControlToggles
Delete dashboard form control toggle

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardToggleId

Returns:
Status
___
###saveDefaultDashboardFormControlToggle
Save dashboard form control toggle

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId
neuornId

Returns:
Status
___
###getDashboardTogglesMetadata
Save dashboard form control toggle

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardToggleIds

Returns:
Status
___
###noSQLTest
Test NoSQL query

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
noSQLAlias
query

Returns:
Response of NoSQL Query
___
###noSQLHelp
Save dashboard form control toggle

Parameters:
username - Username to be used to authenticate with the server
password - Password to be used to authenticate with the server
dashboardId
neuornId

Returns:
XML containing NoSQL help dialog
___