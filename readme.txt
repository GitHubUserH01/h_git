https://support.huawei.com/enterprise/zh/doc/EDOC1100023543?section=j01d
https://support.huawei.com/enterprise/zh/doc/EDOC1100168647


VPN = VRF 目的是解决不同企业私网地址段相同，为了防止冲突，采用将相同私网地址放到不同的VRF表中
VRF = RD + RT RD用来区分本地VRF(对应EVPN实例，EVPN实例通过VBDIF绑定并获取)，该属性仅本地有效，给某VRF里面的路由打上标签，进而实现地址的复用而不产生冲突；RT用来指明是BGP路由导出还是导入，ERT（Export RT）和IRT (Import RT)相同时，路由才能更新
二层vni只是代表了广播域，三层vni才是代表了租户，三层vni和vrf、vpn 1:1绑定
EVPN是Ethernet二层互联vpn，负责控制vtep间导入导出EVPN路由
一般vtep ip是loopback地址，环回地址不属于网卡，只属于主机
