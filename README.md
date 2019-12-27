Dovecot
=========

Install and configure a dovecot installation

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

  - enable_dovecot_service: Enable the dovecot service on boot. Defaults to true
  - dovecot_fqdn: FQDN of the dovecot server / service. Set this to the CN of your SSL certificate.
  - do_ldap: Boolean. Enable ldap configuration
  - do_postfix: Boolean. Enable postfix SASL authentication

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPL

Author Information
------------------

Iain M Conochie <iain@thargoid.co.uk>