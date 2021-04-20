## Ansible example with included kubespray roles

PoC of ansible repo with included kubespray roles as git submodules
Based on instructions from https://github.com/kubernetes-sigs/kubespray/blob/master/docs/integration.md 

## Prepare enviroment
```sh
git submodule sync
git submodule update --init
python3 -m venv venv
. venv/bin/acticate
pip3 install -r requirements.txt
```

Set ip addresses (EXT_IP, INTIP) in hosts.yaml

## Run

# Include roles
Script based on kubespray/cluster.yml
```sh
ansible-playbook include_role.yml -b
```
# Include playbook
!!! This doesn't work

```sh
ansible-playbook include_playbook.yml -b
````
