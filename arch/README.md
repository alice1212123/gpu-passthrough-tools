# Performance optimizations
```
    <hyperv>
      <vpindex state="on"/>
      <runtime state="on"/>
      <synic state="on"/>
      <stimer state="on">
      <direct state="on"/>
      </stimer>
      <reset state="on"/>
      <frequencies state="on"/>
      <reenlightenment state="on"/>

```
```
    <feature policy="require" name="invtsc"/>
```
_______________________________________________________________
# CPU core pinning
```
  <vcpu placement="static">8</vcpu>
  <iothreads>1</iothreads>
  <cputune>
    <vcpupin vcpu="0" cpuset="0"/>
    <vcpupin vcpu="1" cpuset="1"/>
    <vcpupin vcpu="2" cpuset="2"/>
    <vcpupin vcpu="3" cpuset="3"/>
    <vcpupin vcpu="4" cpuset="4"/>
    <vcpupin vcpu="5" cpuset="5"/>
    <vcpupin vcpu="6" cpuset="6"/>
    <vcpupin vcpu="7" cpuset="7"/>
    <emulatorpin cpuset="8-9"/>
    <iothreadpin iothread="1" cpuset="10"/>
  </cputune>

  
```
__________________________________________________________________
# AMD GPU hypervisor detection
```
  <hyperv>
    
    <vendor_id state='on' value='notavm'/>
    
  </hyperv>
_______________________________________________________________
```
  
# Sources
* https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF#Using_identical_guest_and_host_GPUs
