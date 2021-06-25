# harvester-inventory
the  ansible dynamic inventory to pull hosts(nodes and virtualmachines) from Harvester.

## Example

### all (nodes+virtualmachines)
```bash
ansible -m ping -i ./harvester-inventory all
```


### nodes
```bash
ansible -m ping -i ./harvester-inventory nodes
```

### virtualmachines in default namespace
```bash
ansible -m ping -i ./harvester-inventory vms
```


### virtualmachines in other namespace
```bash
NAMESPACE=other ansible -m ping -i ./harvester-inventory vms
```

### master node
```bash
ansible -m ping -i ./harvester-inventory node_label_node_role_kubernetes_io_control_plane_true
```
