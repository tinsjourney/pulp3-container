# Playbook to install pulp3 has multiprocess single image.

Playbook pulp3 will install and configure pulp3 to run as a [multiprocess single image](https://github.com/pulp/pulp-oci-images/blob/latest/docs/multi-process-images.md).

Container will be run as a standard user.

Pre-requisite:

- Directory /pulp exist and standard user is owner of this directory
- Standard user as sudo right
- Host has access to docker.io
- firewalld is installed and running

Tested with :

- podman >= 4.1.1
- ansible-core 2.12.2


## Example playbook

create_spp_content.yaml is an example playbook to create HPE SPP rpm repository for :

- HPE PROLIANT GEN11 for RHEL9
- HPE PROLIANT GEN10 for RHEL9
- HPE PROLIANT GEN10 for RHEL8
