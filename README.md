安装注意事项
========

把这套代码放到装有ansible(最好2.3版本以上)系统的一个文件夹下即可，例如setup-infrastructure文件夹

注意:一定要先安装pre_install和setup_ceph，然后再部署setup-infrastructure


第一步: 安装前准备
--------------

* inventory: 修改openstack_hosts文件要部署的主机变量
* 变量: 修改group_vars/all里面的变量，这个必须要修改
* 修改所有的hostname和ip地址等变量

第二步: 安装执行
--------------

* 执行代码: ansible-playbook -i openstack_hosts setup-infrastructure.yml 


第三步: 检测
--------------

* 安装后检测: mysql -h virtula_ip -uroot -p密码，看看是否可以进去
* 需要删除: myslq -e "drop user 'root'@'b-ops-126-1';" ，这里的b-ops-*-*根据实际需求添加 

备注
--------------

*rsyslog_install模块还没写完，暂时不要部署 
