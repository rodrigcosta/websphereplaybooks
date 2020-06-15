# Ansible HCLauncher
------------
Author: Marcelo F. Oliveira ( moliv@br.ibm.com ).

## Introduction
------------
This set of playbooks intent to:
 - Download and copy HCLauncher tool 
 - Install the binary on the {{remoteInstallDir}}
 - Download and copy the Unix, Sudo and SSH policies 
 - Copy the reports from the hosts to the {{ReportServer}} on {{ReportServerFolder}}


## Requirements
------------
Those playbooks were create to run on AIX, RedHat and SuSE operational systems, as such you need to provide the following extra-vars:
 - remoteInstallDir:
 - remote_user
 - remote_group
 - ReportServer
 - ReportServerFolder


## Example Command Line Use
------------------------
### - Install HCLauncher
cmd `ansible-playbook Install_HCLauncher.yml -e remoteInstallDir=/soibm -e remote_user=ansible -e remote_group=ansible`

### - Run HCLauncher
cmd `ansible-playbook Run_HCLauncher.yml -e remote_user=ansible -e remote_group=ansible -e remoteInstallDir=/soibm -e ReportServer=b01lvi21539180.ahe.pok.ibm.com -e ReportServerFolder=/repo/ansibleReports `


## License
-------

IBM Proprietary
