Creates three environments (cicd, dev and test) as well as a generic pipeline that should work with most templates. It expects that the pipeline is available on a URL so it is not setup to use one of the OpenShift internal templates.

To provision the environments and pipeline, follow these steps:

* Switch to the ansible directory
* Update the inventory and add a group_vars for your host with the required details for master, username, password, etc
* Modify the host in install.yml to reflect the gour_var you added
* Update the variables in vars/vars/yml to reflect the playbook you will be using
* Run the installer:

```ansible-playbook -i inventory install.yml```
