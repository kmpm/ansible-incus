


```shell
python3 -m venv venv
pip install ansible
ln -s $(pwd)/plugins/modules/incus_instance.py ~/.ansible/plugins/modules/


ansible-doc -t module incus_instance
```