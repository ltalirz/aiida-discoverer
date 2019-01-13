# aiida-discoverer

Ansible scripts for setting up the server used during the AiiDA molsim tutorial 2019.

Includes:

 * AiiDA
 * REST API system service
 * EXPLORE docker container
 * bokeh-aiida-visualizer system service
 * plotly-file-upload apache site

### Prerequisites

- A virtual machine running Ubuntu 16.04
- passwordless ssh access to the VM via ssh key
- [python](https://www.python.org/)

```
pip install -r requirements.txt
ansible-galaxy install -r requirements.yml
```

### Set up Virtual Machine

1. put IP address of your server in `./hosts` file
1. adapt path to your ssh key in corresponding `./host_vars/*.yml` file
1. run `ansible-playbook playbook.yml`

 * add deploy-standalone and conf to keys folder
 * open ports 5000-5002 on target machine for ingoing traffic

### Comments

In order to speed up things, everything is set up for the ubuntu user.

## Acknowledgements

This work is supported by the [MARVEL National Centre for Competency in
Research](http://nccr-marvel.ch) and the [MaX European centre of
excellence](http://www.max-centre.eu/)
