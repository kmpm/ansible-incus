


```shell
python3 -m venv venv
pip install ansible
mkdir -p ~/.ansible/plugins/modules
mkdir -p ~/.ansible/plugins/module_utils

ln -s $(pwd)/plugins/modules/incus_instance.py ~/.ansible/plugins/modules/


ansible-doc -t module incus_instance

ansible-playbook -i inventory.ini playbook.yml
```