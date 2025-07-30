Emulates the functionality of physical computer
- One can install different operating systems inside the virtual machine 
- Has the functionality of a normal computer
- **VM are isolated from the Host** 
- <span style="color:#ffff00">Boots its own kernel </span>
## Host and Guest 
- physical computer is the host and the VM are the Guests


---
### Virtual Machine Disk
- Is a large file stored in the host SSD, that the virtual machine uses as *if it were its own SSD*
- in this file, all the dependencies of the operating system (including it) are installed 
- **VMDK are used by VMware products**
Virtual Machines allocate their own portion of the SSD and the RAM of the Host.

---

### Functionality 
- **Allows the host to isolate it's own hardware into independent machines**
