### Intro

This document aims to specify the set of tasks that take a device from a
vanilla Raspbian install up to a fully functioning (TODO: what's the actual
device name?) honeypot device.

These tasks are grouped into 4 major phases:

   1. The Bootstrap Phase
   2. The Package Install Phase
   3. The Service Startup Phase
   4. The Testing Phase

#### Bootstrap Phase

The bootstrap phase configures initial system administrative-type stuff,
such as setting up initial user accounts, uploading SSH keys, basic
hardening, etc.

The bootstrap phase requires the following tasks (in rough, but not final,
order):

   1. Change root password (read from shared config file XXX is it ok for root
     password to be shared across devices? I think so but am open to change)
   2. Add deploy user with password (XXX shared passwd again?)
   3. Upload deploy user SSH public key
   4. Remove default Rasbpian user
   5. Disable root login over SSH
   6. Disable password login
   7. Move SSH to new port (for SPA/disguised login)
   8. Other SSH hardening (e.g. disable X forwarding TODO: specifiy this
     completely)
   9. Upload IPTables ruleset
   10. Configure IPTables to come up on boot
   11. Bring up IPTables


TODO:

   * Justify security rationale for shared passwords.
   * Specify more hardening steps.

#### Package Install Phase

TODO

#### Service Startup Phase

TODO

#### Testing Phase

TODO
