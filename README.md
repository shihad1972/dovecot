Dovecot
=========

Install and configure a dovecot installation

Requirements
------------

There are no pre-requisites for this role, save if you wish to have SSL configuration. Then you
 must have an SSL key pair. These files should be located in the files/ directory in the same
 directory as your playbooks.

Role Variables
--------------

  - enable_dovecot_service: Enable the dovecot service on boot. Defaults to true
  - my_fqdn: FQDN of the dovecot server / service. Set this to the CN of your SSL certificate.
  - do_ssl: Boolean. Enable SSL configuration. Requires SSL cert and key files. Defaults to true
  - do_ldap: Boolean. Enable ldap configuration
    - ldap_host_name: Hostname of the ldap server.
    - do_ldap_users: Create home directories for ldap users
    - dovecot_anonymous_bind: Set to true if you directory allows anonymous binds.
        Set the below variables if your directory does not accept anonymous binds.
    - dovecot_bind_dn: Full DN of the dovecot user
    - dovecot_bind_pass: Password for the dovecot user.
  - do_postfix: Boolean. Enable postfix SASL authentication
  - homebase: Base home directory for users. Defaults to /home

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: dovecot, my_fqdn: my.host.name.com }

License
-------

GPL

Author Information
------------------

Iain M Conochie <iain@thargoid.co.uk>