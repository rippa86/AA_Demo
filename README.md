# Compliance Automation Demo 
If you're using this God Speed :). Ansible Demo on how we can use OpenScap to perform compliance Automation for RHEL. 

**'So, whats it do?**
1. Run Openscap on a a couple of instances. From there it will compile a report on the http site (template here: https://github.com/rippa86/compliance_reports).
2. Creates a INC ticket in SNOW and Updates Slack. if more than 4 defects are found or if compliance is under 90%. To force one of your RHEL hosts under 90% run cook_host.yml
3. Runs a Self Healing playbook to resove issues

## Requirements
- AAP cluster
- 2 x RHEL instances
- 1 x HTTPD Server ( I'm using the AAP host as the httpd service)
- ServiceNow Dev Instance integrated into AAP
- Slack channel 

Role Variables
slack : boolean 

#### Rippa to update!

Dependencies
[Compliance Reports](https://github.com/rippa86/compliance_reports) 
[OpenScap Role](https://github.com/rippa86/compliance_reports)

- Run Set_up.yml to install:
- rhel: 
  - openscap
- http
  - httpd
  - openscap

Example Playbook
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: servers
  roles:
     - { role: username.rolename, x: 42 }
License
BSD

Author Information
Developed by Rippa. 
