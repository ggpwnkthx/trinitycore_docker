# build
```
-repo "git://..."
	default: "github.com/TrinityCore/TrinityCore.git"
-branch "master" or "3.3.5"
	default: "master"
```	
This script will clone (or update/pull) the TrinityCore source and build it. The repository can be changed, but for most people, the only argument you'll want to change is the branch. For BfA, use "master". For WotLK, use "3.3.5". 
 
# add_project
```
-project "Name of Project"
	default: "untitled"
-version "8.2.0" or "3.3.5"
	default: "8.2.0"
-realms "Trinity,Scarlet,Molten"
	default: "Trinity"
-development $false
	default: $false
```	
This script will create a project folder and copy the necessary files for an authentication server and any specified (comma delimited) realms. 
	
# start_project
```
-project "Name of Project"
	default: "untitled"
-version "8.2.0" or "3.3.5"
	default: "8.2.0"
-realms "Trinity,Scarlet,Molten"
	default ""
```	
This script will start up all the containers necessary for a given project. If realms argument is not set all realms for that project will be started.

# REQUIREMENTS
Clients must be in the "clients" folder. Put the contents of the WotLK folder into "clients/3.3.5". Put the contents of the BfA folder into "clients/8.2.0".
For WotLK, the folder structure should look like:
```
clients
    3.3.5
        Data
		Interface
		{other files}
```
For BfA, the folder structure should look like:
```
clients
    8.2.0
	    _classic_
		_retail_
        Data
		{other files}
```