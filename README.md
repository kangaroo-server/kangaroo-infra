# kangaroo-infra

This project contains the ansible scripts necessary for kangaroo's build infrastructure. At this
time, it is restricted to building our jenkins-slave AMI, which is used by the jenkins master
to provision build slaves.

### Developer quickstart

This project is - at this time - not intended for multi-developer use. Contributions to permit
this kind of collaboration are encouraged.

Tools required:
- Ansible
- An AWS account with exported AWS environment parameters.
- An AWS SSH key named "ansible" that permits password-less ssh into your instances.
- A VPC with the ID hardcoded into our scripts.

To build an publish a new AMI, run the following command.

```bash
make ami
```