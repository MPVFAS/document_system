# # Deplay Requirements:

# Go Version 1.16 or later

# Installation:
$ go get -u github.com/uadmin/uadmin/
$ go install github.com/uadmin/uadmin/cmd/uadmin@latest

# Test Installation:
$ uadmin
Usage: uadmin COMMAND [--src]
This tools helps you prepare a folder for a new project or update static files and templates

Commands:
 -- prepare         Generates folders and prepares static and templates
 -- version         Shows the version of uAdmin

Arguments:
  --src           If you want to copy static files and templates from src folder

Get full documentation online:
https://uadmin-docs.readthedocs.io/en/latest/

# Build your first app Document_System list. First, we will create a folder for your project and prepare it :

$ mkdir -p ~/go/src/github.com/your_name/document_system
$ cd ~/go/src/github.com/your_name/document_system
$ uadmin prepare

[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/models
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/api
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/views
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/media
[  INFO  ]   Copying static/templates from: /Users/abdullah/go/pkg/mod/github.com/uadmin/uadmin@v0.6.0
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/static
[   OK   ]   Created: /Users/abdullah/go/src/github.com/twistedhardware/test/templates

# Prepare Modules :

$ go mod init
go: creating new go.mod: module github.com/document_system
go: to add module requirements and sums:

$ go mod tidy
go: finding module for package github.com/uadmin/uadmin
go: found github.com/uadmin/uadmin in github.com/uadmin/uadmin v0.6.0

# Run Apps :

$ go build; ./document_system
[   OK   ]   Initializing DB: [14/14]
[   OK   ]   Initializing Languages: [185/185]
[  INFO  ]   Auto generated admin user. Username:admin, Password:admin.
[   OK   ]   Synching System Settings: [49/49]
[   OK   ]   Server Started: http://0.0.0.0:8080
         ___       __          _
  __  __/   | ____/ /___ ___  (_)___
 / / / / /| |/ __  / __ '__ \/ / __ \
/ /_/ / ___ / /_/ / / / / / / / / / /
\__,_/_/  |_\__,_/_/ /_/ /_/_/_/ /_/
