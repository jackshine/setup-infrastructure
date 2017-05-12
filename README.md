安装注意事项
========

把这套代码放到装有ansible(最好2.3版本以上)系统的一个文件夹下即可，例如setup-infrastructure文件夹

注意:一定要先安装pre_install和setup_ceph，然后再部署setup-infrastructure


第一步: 安装前准备
--------------

* inventory: 修改openstack_hosts文件要部署的IP地址
* 变量: 修改group_vars/all里面的变量，这个必须要修改

第二步: 安装执行
--------------

* 执行代码: ansible-playbook -i openstack_hosts setup-infrastructure.yml 

备注
--------------

*rsyslog_install模块还没写完，暂时不要部署 
