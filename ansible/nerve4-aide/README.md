nerve4-aide
===========

An Ansible role that installs AIDE to CENTOS 7/8.


Requirements
------------

Make sure, you made your vars file with valid path to custom template or you can use Default vars.


Prerequisites
--------------

You need ansible 2.9.9 to run this module


Role Variables
--------------

Available variables are listed below, along with default values.
- aide_cron_day - Day of the week that the job should run ( 0-6 for Sunday-Saturday, *, etc )
- aide_cron_min - minute, that the job should run (0 - 59)
- aide_cron_hour - hour, that the job should run (0 - 23)


Tasks descriptions
------------

- main.yml - Run the OS check and run the relevant playbook
- install_el7.yml - Install aide on Centos 7.x
- install_el8.yml - Install aide on Centos 8.x


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servergroup
      become: true
      become_user: lee
    
      vars_files:
        - vars/main.yml
        
      roles:
        - nerve4-aide


Author Information
------------------
Lee P. | 2020


## License

This project is licensed under the MIT License

