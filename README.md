# Ansible Incus
This is a small project for developing [Incus](https://linuxcontainers.org) plugins for [Ansible](https://ansible.com).

__NOTE!!!__: All development here is halted and moved to https://github.com/kmpm/ansible-collection-incus

These are based/forked from work in the module 
[lxd_container](https://github.com/ansible-collections/community.general/blob/main/plugins/modules/lxd_container.py),
[Issue 7853](https://github.com/ansible-collections/community.generalissues/7853) 
and [PR 7980](https://github.com/ansible-collections/community.general/pull/7980) specificaly.

For the moment only `lxd_container` is changed to `incus_instance`.
The module util `lxd` is change into `incus`.
All licenses and copyrights are kept for now.

## Testing
Since the supplied `ansible.cfg` changes `home` to `./` it should be possible to run with the following.

```shell
# install and activate a virtual environment if you want/need
python3 -m venv venv
. venv/bin/activate

# install ansible if not already done
pip install ansible

# test that ansible can find the module
ansible-doc -t module incus_instance

# run a short example
ansible-playbook -i inventory.ini playbook.yml
```
