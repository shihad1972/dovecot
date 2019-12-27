install.yml

    Install Dovecot packages (list of packages defined in role)
    Enable to dovecot service (controlled via enable_dovecot_service variable)

configure.yml
 
    Enable SASL Authentication for postfix (controlled via do_postfix variable)
    Copy over non ldap authentication configuration (controlled via do_ldap variable)
    Template the mail location configuration (homebasedir variable provides home directory location)

ssl.yml

    Create SSL key directory
    Create SSL certificate directory
    Copy over private key
    Copy over certificate file / public key
    Template SSL configuration file
        - dovecot_conf: main configuration directory for dovecot
        - dovecot_conf_d: conf.d directory for dovecot, under {{ dovecot_conf }}
        - dovecot_crtdir: certificate directory
        - dovecot_keydir: private key directory
        - dovecot_fqdn: FQDN of dovecot server / service

users.yml

    Create base directory for home directories
    Create user home directories (ldap_users variable provides list of users)

ldap.yml

    Create 3 ldap configuration files
        - LDAP Authentication configuration
        - Dovecot user and password database
        - Detail configuration for binding to ldap directory
