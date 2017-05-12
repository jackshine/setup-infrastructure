# 功能

部署pacemaker集群，并添加集群相应资源。

# 配置项

必填：
- virtual_ip: 虚ip，在网络中此ip应没有被占用，由于virtual_ip为支持整体HA方案，所以此变量请在all的group var中设置。
- bindnetaddr: 网络地址，比如：本地ip为192.168.5.92，子网掩码为255.255.255.0，bindnetaddr应该设置为192.168.5.0; 本地ip为192.168.5.92，子网掩码255.255.255.192, bindnetaddr应设置为192.168.5.64。
- hacluster_password: pacemaker创建集群用户hacluster的用户密码

选填：
- expected_votes: 期望投票数，默认3
- group_name: pacemaker集群中将所有资源归为一组，指定组名，默认为common

以上选项都可以在group_vars/pacemaker_all中指定，指定后将覆盖role中var/main.yml中的变量。
