ESXi Base file used: VMware-ESXi-6.7U3v-24514018-x86_64.iso (this is the latest patch as of 2026, 202503001).

Added following .vib:

net55-r8168-8.045a-napi.x86_64.vib (realtek 8168 drivers)

net-igb-5.3.2-99.x86_64.vib (intel lan drivers)

net-r8125-9.011.00-10.vib (realtek 8125 2.5gbe drivers)

VMW_bootbank_nvme-community_1.0.1.0-1vmw.670.0.0.8169922.vib (nvme drivers)

VMW_bootbank_vmkusb-nic-fling_2.1-6vmw.670.2.48.39203948.vib (usb nic drivers)

Special: replaced original esx-ui-1.43.10.vib (with bug in WebHost Console that breaks attaching disks to VMs: https://community.broadcom.com/vmware-cloud-foundation/discussion/esx-ui-211-impossible-add-existing-vmdk)
         with esx-ui-1.33.7.vib, to restore functionality
