Installing roles
Roles can be pulled and installed in multiple ways by using the CLI. The easiest and most straightforward way of doing it is to use the ansible-galaxy website:

ansible-galaxy install username.rolename
The location where roles are downloaded can be configured in your ansible.cfg file as the roles_path.

Using roles with public and private git repositories
A not so much advertised feature of ansible galaxy CLI is the ability to download roles from private git repositories. This is something very useful in corporate environments where code can’t be open sourced and automation is a must.

A new YAML format to define the role requirements file was introduced since version 1.8. This new feature adds the possibility to specify remote repositories from where to download roles.

                #command to install roles from a requirements file
		ansible-galaxy install -r requirements.yml
The new YAML format offers a great degree of freedom and configuration to specify role dependencies. Below I will go through a simple setup for two roles:

