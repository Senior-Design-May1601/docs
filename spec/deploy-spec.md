### Intro

This document aims to specify the set of tasks that take a device from a
vanilla Raspbian install up to a fully functioning (TODO: what's the actual
device name?) honeypot device.

These tasks are grouped into 4 major phases:

   * The Bootstrap Phase
   * The Package Install Phase
   * The Service Startup Phase
   * The Testing Phase

#### Bootstrap Phase

The bootstrap phase configures initial system administrative-type stuff,
such as setting up initial user accounts, uploading SSH keys, basic
hardening, etc.

The bootstrap phase requires the following tasks (in rough, but not final,
order):

   * Change root password (read from shared config file XXX is it ok for root
     password to be shared across devices? I think so but am open to change)
   * Add deploy user with password (XXX shared passwd again?)
   * Upload deploy user SSH public key
   * Remove default Rasbpian user
   * Disable root login over SSH
   * Disable password login
   * Move SSH to new port (for SPA/disguised login)
   * Other SSH hardening (e.g. disable X forwarding TODO: specifiy this
     completely)
   * Upload IPTables ruleset
   * Configure IPTables to come up on boot
   * Bring up IPTables


TODO:

   * Justify security rationale for shared passwords.
   * Specify more hardening steps.

#### Package Install Phase

TODO

#### Service Startup Phase

TODO

#### Testing Phase

TODO
