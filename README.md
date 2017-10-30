English:
------------------------------------------------------
``# ansible-rabbitmq``

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
