
## what is para-virtualization

Para-virtualization is a virtualization technique that presents a software interface to virtual machines (VMs) that is slightly different from the underlying hardware. Unlike full virtualization, where the guest operating system operates without any modification, para-virtualization requires the guest OS to be modified to interact with the hypervisor (the software layer that manages VMs) more efficiently. 

In para-virtualization, the hypervisor provides a virtual environment that can be more efficient, as it allows the guest OS to directly interact with the hypervisor for certain operations. This approach can improve performance, as it reduces the overhead associated with emulating hardware.

Key points about para-virtualization:
1. **Modified OS:** The guest OS needs to be aware of the virtualization and modified to work with the hypervisor.
2. **Efficiency:** It can offer better performance compared to full virtualization due to reduced overhead.
3. **Hypervisor:** Manages the virtual machines and provides the para-virtualized environment.

It's like providing a tailored suit for the OS, allowing it to work more seamlessly with the virtualized hardware.

---

## compare and contrast virtualization and para-virtualization

