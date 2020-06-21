### Day 3

- Create a role that configures an Apache vhost on the managed hosts in the group "lamp"
- Have it include a template to create a minimal vhost configuration file in which all references to the hostname are replaced with Ansible facts
>  Готово. См. репозиторий.

- Use an ad-hoc commands to test working of the vhost
> Проверить работоспособность vhost-ов можно, например, следующей командой:
```
ansible -i inventory lamp -m shell -a 'curl -s  http://$(hostname -f)'
```
> Ее вывод:
```
node1.snetesa.club | CHANGED | rc=0 >>
Welcome to node1.europe-north1-a.c.modified-legacy-279621.internal!
node2.snetesa.club | CHANGED | rc=0 >>
Welcome to node2.europe-north1-a.c.modified-legacy-279621.internal!
```