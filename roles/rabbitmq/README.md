说明：
```
1》定义的主机组一定不能改变
主机组中可以是IP或者主机名，但不能加其他的变量

2》>./inventory/hosts 中的变量

[rabbitmq:vars]
user=openstack     #添加的用户
password=123456  #用户密码
cluster_join_node1=rabbit1  #加入的节点名称

3》rabbitmq的标签有3个
  -- rabbitmq  是首次执行的操作，就是不管disc或者ram节点都执行
  -- rabbitmq_disc 只执行与disc相关操作
  -- rabbitmq_ram  只执行与ram相关操作

4》执行首次安装
ansible-playbook site.yml --tags rabbitmq

5》disc和ram重置重新添加
ansible-playbook site.yml --tags rabbitmq_disc
ansible-playbook site.yml --tags rabbitmq_ram
```

