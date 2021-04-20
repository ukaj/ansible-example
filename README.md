## Ansible example with included kubespray roles

PoC of ansible repo with included kubespray roles as git submodules.
Based on instructions from https://github.com/kubernetes-sigs/kubespray/blob/master/docs/integration.md 

## Prepare enviroment
```sh
git submodule sync
git submodule update --init
python3 -m venv venv
. venv/bin/activate
pip3 install -r requirements.txt
```

Setup ip addresses ($EXT_IP, $INTIP) in hosts.yaml

## Run

There are two approeches of including kubespray in your project

### Include roles
Script based on kubespray/cluster.yml
```sh
ansible-playbook include_roles.yml -b
```
### Include playbook
This doesn't work :rotating_light:

```sh
ansible-playbook include_playbook.yml -b
````
