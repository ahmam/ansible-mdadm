mrlesmithjr.mdadm
=================

An [Ansible] role to install and manage [mdadm] raid arrays.

Requirements
------------

- Available unpartitioned disk devices

Role Variables
--------------

```
---
# defaults file for ansible-mdadm
#
# Define Raid Arrays to manage
#
# Example RAID1:
# mdadm_arrays:
#   # Define array name
# - name: 'md0'
#   # Define disk devices to assign to array
#   devices:
#     - '/dev/sdb'
#     - '/dev/sdc'
#   # Define filesystem to partition array with
#   filesystem: 'ext4'
#   # Define the array raid level
#   # 0|1|4|5|6|10
#   level: '1'
#   # Define mountpoint for array device
#   mountpoint: '/mnt/md0'
#   # Define if array should be present or absent
#   state: 'present'
#   # Set mount options (optional)
#   opts: 'noatime'
#
# Example RAID5:
# mdadm_arrays:
# - name: 'md0'
#   devices:
#     - '/dev/sdb'
#     - '/dev/sdc'
#     - '/dev/sdd'
#   filesystem: 'ext4'
#   level: '5'
#   mountpoint: '/mnt/md0'
#   state: 'present'
mdadm_arrays: []
```

Dependencies
------------

None

Example Playbook
----------------

```
- hosts: all
  become: true
  vars:
  roles:
    - role: ansible-mdadm
  tasks:
```

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- [@mrlesmithjr]
- [EverythingShouldBeVirtual]
- mrlesmithjr [at] gmail.com

[@mrlesmithjr]: <https://www.twitter.com/mrlesmithjr>
[EverythingShouldBeVirtual]: <http://www.everythingshouldbevirtual.com>

[mdadm]: <https://linux.die.net/man/8/mdadm>
[Ansible]: <https://www.ansible.com>
