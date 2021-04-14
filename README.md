# openshift
openshift 记录

## 添加新节点在集群
https://docs.openshift.com/container-platform/3.11/install_config/adding_hosts_to_existing_cluster.html

## 手动更新master 证书
https://access.redhat.com/solutions/5140431

```
- name: Get common IP facts when necessary
  hosts: nodes:!masters
  roles:
  - openshift_facts
  tasks:
  - name: Gather Cluster facts
    openshift_facts:
      role: common
      system_facts: "{{ vars_openshift_facts_system_facts }}"
```

## osd 添加失败
https://bugzilla.redhat.com/show_bug.cgi?id=1886534


## k8s 如何利用terminationGracePeriodSeconds 优雅地关闭你的服务？
https://www.jianshu.com/p/1f54ad627cb7
