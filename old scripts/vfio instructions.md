**ONLY TESTED WITH AND ARCH**


```
/etc/default/grub: 
intel_iommu=on (or) amd_iommu=on 
rd.driver.pre=vfio-pc 
kvm.ignore_msrs=on

Add this to /etc/mkinitcpio.conf:
Modules="vfio_pci vfio vfio_iommu_type1 vfio_virqfd"
Files="/usr/bin/vfio-pci-override.sh"
Hooks="... vfio ...."
```
