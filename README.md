# # Deploy Requirements:

# Go Version 1.16 or later

# Installation:
$ go get -u github.com/uadmin/uadmin/
<br>
or
<br>
$ go install github.com/uadmin/uadmin/cmd/uadmin@latest
<br>

## Test Installation:
$ uadmin
<br>
Usage: uadmin COMMAND [--src]
<br>
This tools helps you prepare a folder for a new project or update static files and templates
<br>
# Commands:
 -- prepare         Generates folders and prepares static and templates
 -- version         Shows the version of uAdmin

Arguments:
  --src           If you want to copy static files and templates from src folder

Get full documentation online:
https://uadmin-docs.readthedocs.io/en/latest/

## Build your first app Document System list. First, we will create a folder for your project and prepare it :
$ mkdir -p ~/go/src/github.com/your_name/document_system
<br>
$ cd ~/go/src/github.com/your_name/document_system
#
$ uadmin prepare
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/models
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/api
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/views
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/media
<br>
[  INFO  ]   Copying static/templates from: /Users/abdullah/go/pkg/mod/github.com/uadmin/uadmin@v0.6.0
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/static
<br>
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/templates
<br>

# Prepare Modules :
#
$ go mod init
<br>
go: creating new go.mod: module github.com/document_system

go: to add module requirements and sums:
#
$ go mod tidy
<br>
go: finding module for package github.com/uadmin/uadmin

go: found github.com/uadmin/uadmin in github.com/uadmin/uadmin v0.6.0
#
## Run Apps :
<br>
$ go build; ./document_system
<br>
<br>
[   OK   ]   Initializing DB: [14/14]
<br>
[   OK   ]   Initializing Languages: [185/185]
<br>
[  INFO  ]   Auto generated admin user. Username:admin, Password:admin.
<br>
[   OK   ]   Synching System Settings: [49/49]
<br>
[   OK   ]   Server Started: http://0.0.0.0:8080
<br>
##
         ___       __          _
  __  __/   | ____/ /___ ___  (_)___
 / / / / /| |/ __  / __ '__ \/ / __ \
/ /_/ / ___ / /_/ / / / / / / / / / /
\__,_/_/  |_\__,_/_/ /_/ /_/_/_/ /_/

##
