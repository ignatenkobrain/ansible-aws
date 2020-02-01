# ansible-aws

Manage AWS thingies with Ansible.

## Prerequisites

* `ansible` >= 2.9
* `python3-boto3`
* `python3-boto`
* `awscli`

## Configuration

1. Create Access key in AWS IAM
2. Configure a profile using `awscli` (e.g. `awscli configure --profile gdc-test`)

## Running

Using configured AWS profile, set the environment variable and run playbook.

```sh
env AWS_PROFILE=gdc-test ansible-playbook -i testing vpc.yml
```

## Testing inventory’s sanity

```sh
ansible-playbook -i testing playbooks/check-inventory.yml
```
