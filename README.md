# Patent
# Cloud controller providing architecture-based installations
In some examples, a method can include detecting, with a cloud controller, a Central Processing Unit (CPU) architecture for a bare metal server; selecting, based on the detected CPU architecture, a specific bootloader, specific Operating System (“OS”) and specific Virtual Machine (“VM”) for the bare metal server; and installing the selected bootloader, OS, and VM on the bare metal server.What is claimed is:
1. A method comprising:
detecting, with a cloud controller, a Central Processing Unit (CPU) architecture for a bare metal server;
selecting, based on the detected CPU architecture, a specific bootloader, specific Operating System (“OS”) and specific Virtual Machine (“VM”) for the bare metal server; and
installing the selected bootloader, OS, and VM on the bare metal server.
2. The method of claim 1, wherein detecting the CPU architecture is based on a received Dynamic Host Configuration Protocol (“DHCP”) packet broadcasted by the bare metal server during a Pre-boot eXecution Environment (“PXE”) boot.
3. The method of claim 1, wherein detecting the CPU architecture is based on a packet broadcasted by the bare metal server in the form of a DHCPDISCOVERY packet including a DHCP option 93 specified by RFC 4578.
4. The method of claim 1, wherein the bare metal server is a host server.
5. The method of claim 1, wherein the VM is a guest VM.
6. The method of claim 1, further comprising:
registering information about a hypervisor of the bare metal server via a Representational State Transfer (“REST”) call.
7. The method of claim 1, wherein the information about a hypervisor includes one or more of Media Access Control (“MAC”) Address, Architecture Type, amount of Random Access Memory (“RAM”), and CPU size.
8. The method of claim 1, wherein the cloud controller is to install a hypervisor on the bare metal server.
9. The method of claim 1, wherein the cloud controller is to install a first OS on a hypervisor having a first architecture and the cloud controller is to install a second OS on a hypervisor having a second architecture, wherein the first and second OS's are different OS's and the first and second architectures are different architectures.
10. The method of claim 1, wherein a single cloud controller is to handle the respective installation of bootloaders, OS's, and VM's on multiple bare metal servers with different CPU architectures.
11. The method of claim 1, wherein the cloud controller provides an option for a manual override of the selected bootloader, OS, or VM.
12. A non-transitory machine readable storage medium having stored thereon machine readable instructions to cause a computer processor to:
receive, with a cloud controller, a request for the creation of a guest Virtual Machine (“VM”) on equipment controlled by the cloud controller;
detect a pre-boot architecture for the controlled equipment;
load a bootloader on the controlled equipment based on the detected pre-boot architecture; and
automatically install, on the controlled equipment, an Operating System (“OS”) and a guest VM on a hypervisor.
13. The medium of claim 12, wherein the instructions are to cause the computer processor to:
in response to a DHCP trigger, execute an automation script on the cloud controller.
14. The medium of claim 12, wherein detecting a pre-boot architecture for the controlled equipment includes extracting such information from a DHCP broadcasted packet.
15. The medium of claim 12, wherein the cloud controller is configured with automation scripts and kickstart files for OS installation on the controlled equipment.
16. The medium of claim 15, wherein the automation script directs the cloud controller to a specific bootloader to be loaded on the controlled equipment.
17. A cloud controller comprising:
a processing resource; and
a memory resource storing machine readable instructions to cause the processing resource to:
extract information about the architecture of a first bare metal server from a broadcasted packet;
select, for the first bare metal server and based on the extracted architecture information, a first Operating System (“OS”) from a set of multiple OS's;
extract information about the architecture of a second bare metal server from a broadcasted packet; and
select, for the second bare metal server and based on the extracted architecture information, a second Operating System (“OS”) from a set of multiple OS's.
18. The cloud controller of claim 17, wherein the memory resource stores machine readable instructions to cause the processing resource to:
install the first OS on the first bare metal server; and
install the second OS on the second bare metal server.
19. The cloud controller of claim 17, wherein the memory resource stores machine readable instructions to cause the processing resource to:
select, for the first bare metal server and based on the extracted architecture information, a first bootloader from a set of multiple bootloaders;
select, for the second bare metal server and based on the extracted architecture information, a second bootloader from a set of multiple bootloaders.
20. The cloud controller of claim 19, wherein the memory resource stores machine readable instructions to cause the processing resource to:
install the first bootloader on the first bare metal server; and
install the second bootloader on the second bare metal server.

