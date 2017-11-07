# F5 SSL Orchestrator and Juniper vSRX solution
SSL visibility and service chaining for advanced threat Analysis and Prevention

1.	Set up the virtual F5 BIG-IP LTM on VMware fusion. For more information, refer (https://devcentral.f5.com/articles/f5-developer-edition-installing-big-ip-on-vmware-fusion-8)
2.	Set up vSRX on VMware fusion. For more information, refer (https://github.com/saimkhan92/F5-SSL-Orchestrator-and-Juniper-vSRX-solution/blob/master/vSRX_vmware_fusion_setup.pdf)
3.	Set up Ubuntu virtual machine for testing the solution. For more information, refer (https://www.askdavetaylor.com/install-ubuntu-linux-vmware-fusion/)
4.	Service chain the three VMs using Fusion bridges. Consider VMware fusion bridge, a layer 2 switch. If two network adapters are connected to the same bridge, the traffic starts flowing. In my setup, I created five custom VMware bridges for the purpose of service chaining. The following was the bridge configuration that I used:

![Alt text](https://github.com/saimkhan92/F5-SSL-Orchestrator-and-Juniper-vSRX-solution/blob/master/fusion_block_diagram.png "Optional title")

All the bridges were custom VMware fusion bridges. The fifth bridge, vmnet12, was connected to the host mac for management network setup. The bridge, vmnet13, was a NAT bridge and provided internet connectivity using the mac's internet connection.

5.	Set up F5 SSL orchestrator. For more information, refer (https://f5.com/Portals/1/PDF/security/F5_BIG-IP_Platform_Palo_Alto_Networks_Next-Gen_Firewall_Solution.pdf)
6.	Set up IPS on vSRX to analyze the decrypted traffic. Refer (https://www.juniper.net/documentation/en_US/junos/topics/task/configuration/security-ips-configuration-cli.html)
