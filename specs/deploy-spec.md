## Intro

This document aims to specify the set of tasks that take a device from a
vanilla Raspbian install up to a fully functioning (TODO: what's the actual
device name?) honeypot device.

These tasks are grouped into 5 major phases:

   1. The Bootstrap Phase (TODO: this is maybe a bad name)
   2. The Package Install Phase
   3. The Build Phase
   4. The Service Startup Phase
   5. The Testing Phase

### Bootstrap Phase

The bootstrap phase configures initial system administrative-type stuff,
such as setting up initial user accounts, uploading SSH keys, basic
hardening, etc.


##### Role: config-root-user


Tasks:

   1. Hash root password using `mkpasswd` (read from ansible-vault)
   2. Change the root password


##### Role: config-deploy-user


Tasks:

   1. Hash deploy password using `mkpasswd` (read from ansible-vault)
   2. Create deploy user with password
   3. Add deploy user authorized SSH key


##### Role: unprivileged-user


Tasks:

   1. Create unprivileged user to run services


Run for:

   * webauth


##### Role: lockdown-ssh


Tasks:

   1. Disable root login
   2. Disable password login
   3. Set authentication to publickey
   4. Set privilege separation to sandbox
   5. Disable X11 forwarding
   6. Only allow deploy user to use ssh
   7. Set modern ciphers
   8. Set modern MACs
   9. Restart ssh


##### Role: iptables

Tasks:

   1. Install iptables-persistent
   2. Copy iptables file
   3. Reload iptables


### Package Install Phase


The package install phase installs/upgrades all packages required for
(TODO: what's the project name?) the system.


##### Role: golang


Tasks:

   1. Install golang with apt


TODO: set GOPATH?


##### Role: git

   
Tasks:

   1. Install git with apt


##### Role: clone


Tasks:

   1. Create src directory
   2. Clone a git repo


Run for:

    * webauth


#### Build Phase


The build phase builds all necessary packages, at this point mainly our
go services.


##### Role: build-go


Tasks:

   1. Create bin directory.
   2. Build package.
   3. Copy executable to bin.


Run for:

   * webauth


##### Role: config-webauth


Tasks:

   1. Copy webauth config to (TODO: name?) device


TODO: we should abstract this out to a reuseable role.


### Service Startup Phase


The service startup phase brings up all honeypot services.


##### Role: start-service


Tasks:

   1. Copy service config file to (TODO: name?) device
   2. Enable service to start at boot.
   3. Start service


Run for:

   * webauth


#### Testing Phase

TODO
