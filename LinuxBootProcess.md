## Linux Boot Process


- When first pressed power button, a program called BIOS (Basic Input Output System) is executed. BIOS is a firmware, which is a software that is embedded in a hardware. BIOS is responsible for initializing the hardware and starting the boot process. 

- There is UEFI (Unified Extensible Firmware Interface) which is a newer firmware that replaces BIOS. UEFI is more advanced than BIOS. UEFI provides secure & faster boot.

- Next, BIOS or UEFI runs POST (Power-On Self Test). POST checks the hardware to ensure that everything is working properly. If POST fails, the computer will not boot. POST also checks the CMOS (Complementary Metal-Oxide-Semiconductor) settings. CMOS settings are stored in a battery-powered chip. CMOS settings include date, time, and boot order.

- After that BIOS or UEFI loads the boot loader. The boot loader is a small program that loads the operating system. The boot loader is stored in the MBR (Master Boot Record) or GPT (GUID Partition Table). MBR is an older standard and GPT is a newer standard. MBR has a limit of 2TB and GPT has a limit of 9.4ZB.

- The key jobs of the boot loader are to detect the operating system and load the kernel. The kernel is the core of the operating system. The kernel is responsible for managing the hardware and software resources. The kernel is loaded into the memory.

- There are mainly two boot loaders: 
    1. GRUB (Grand Unified Bootloader): It is the most popular boot loader for Linux. It is highly configurable. It can boot multiple operating systems. It is stored in the MBR or GPT.
    2. LILO (Linux Loader): It is an older boot loader for Linux. It is less configurable. It can boot only Linux. It is stored in the MBR.

- After loading the kernel, the kernel initializes the hardware and starts the init process. The init process is the first process that is started by the kernel.

- The init process is responsible for starting the system services. The system services are the background services that are required for the system to function properly. The system services include network services, file services, and printing services.
