# Install kubernetes (Master & Node) on Centos (7,8) or debian (9,10) with Ansible 2.7+ and above

you can use on the multidistribution linux for the master or the nodes with Ansible

##  Prerequisites

- Nodes or Master: CentOS/RHEL (7.x,8.x) or Debian (9.x,10.x) and above

- Ansible 2.7+ and above 

- change your Address IP and the hostname in the `hosts.yml`

 +   master:
      ansible_host: `Address IP Master`
      vars:
        ansible_hostname: `Hostname Master`
 +   workers-1:                             you can make many nodes (workers-1,workers-2,....workers-n)
      ansible_host: `Address IP Master`
      vars:
        ansible_hostname: `Hostname Master`

- change the `node_ip` and `master_server` in the  `group_vars\all`

  + node_ip: `Address IP Master`
  + master_server: `Hostname Master`

- change your default user in the `site.yml`
   + remote_user: `your_user`

## Install and Deployment 

when the master and the nodes are ready,you can make the command:

```
 ansible-playbook -i hosts.yml site.yml
```

## Author Information
* `Dialy Burleigh` in 2020