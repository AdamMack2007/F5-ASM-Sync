# F5 ASM Policy Sync

Ansible role that synchronizes F5 ASM policies across separate clusters.

## Usage

This role will export ASM policies to .xml files on the Ansible server and then import them into the F5s specified in destination_f5 var.

## Required Vars

* **policy_dir**: Directory to store xml files temporarily, files will be deleted after import.
* **source_f5**: This is the primary device that the policies will be pulled from
* **destination_f5**: This is the list of devices that the policies will be imported into.

## Example playbook

```
- name: Sync F5 ASM Policies
  hosts: all
  gather_facts: no

  roles:
    - f5_asm_sync
 ```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
