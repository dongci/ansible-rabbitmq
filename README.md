English:
------------------------------------------------------
## ansible-rabbitmq ##

Edit the ./inventory/hosts configuration file

###
[rabbitmq_disc]
10.0.0.101
10.0.0.103

[rabbitmq_ram]
10.0.0.102

[rabbitmq: children]
rabbitmq_disc
rabbitmq_ram

[rabbitmq: vars]
user = openstack
password = 123456
cluster_join_node1 = rabbit1
###

1> Install rabbitmq cluster
```
ansible-playbook site.yml --tags rabbitmq
```

2> Update rabbitmq disc node
```
ansible-playbook site.yml --tags rabbitmq_disc
```

3> Update rabbitmq ram node
```
ansible-playbook site.yml --tags rabbitmq_ram
```

------------------------------------------------------
