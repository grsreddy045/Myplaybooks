# Purpose
This role will configure a machine as a Spring Boot app machine

It works with either Amazon Linux only, currently.
# Required Variables

## Vars in group_vars
The following are required or optional variables in the group_vars directory at the same level as the playbook file:

### Required vars
* project: This is to indicate the project name, as defined when onboarding with TechOps

### Optional vars
* linux_install_dir: The directory the app is installed in.  Defaults to: "/var/lib/project/{{ project }}"
* service_port: The port the application listens on.  Be sure your AWS infrastructure was also created using this port before changing.  Defaults to: 8080

## Vars in extra_vars
These variables MUST be specified when calling the ansible-playbook command using the -e parameter:
* service_name: The actual service name within the project
