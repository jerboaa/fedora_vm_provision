# Provision a Fedora VM

This is an ansible playbook to quickly provision a Fedora virtual machine image
with the following setup:

- Configures the VM to run in FIPS mode
- Configures the VM for OpenJDK cgroups v2 testing
- Configures the VM for basic Mandrel testing

# Pre-requisites

```
$ sudo dnf install -y ansible-core
```

# Usage

```
$ git clone https://github.com/jerboaa/fedora_vm_provision.git
$ cd fedora_vm_provision
$ ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -e 'ansible_user=root' -e 'user_p=<user-p>' -e 'root_p=<root-p>' -e 'vm=F39-01' -K kvm_provision_cgroupsv2_fips.yaml
```
