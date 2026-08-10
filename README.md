```
> run nfsboot 
##################################################
Packets received 6488, Transfer Successful
Bytes transferred = 9388570 (8f421a hex)
## Loading kernel (any) from FIT Image at 90000000 ...
   Using 'conf-1' configuration
   Verifying Hash Integrity ... OK
   Trying 'kernel-1' kernel subimage
     Description:  Linux kernel
     Type:         Kernel Image
     Compression:  gzip compressed
     Data Start:   0x900000e0
     Data Size:    6505928 Bytes = 6.2 MiB
     Architecture: AArch64
     OS:           Linux
     Load Address: 0x9a200000
     Entry Point:  0x9a200000
     Hash algo:    sha1
     Hash value:   f1410104d43205da68da7e85f38ec0c895c341d7
     Sign algo:    sha1,rsa2048:
     Sign value:   unavailable
   Verifying Hash Integrity ... sha1+ sha1,rsa2048:- OK
## Loading ramdisk (any) from FIT Image at 90000000 ...
   Using 'conf-1' configuration
   Verifying Hash Integrity ... OK
   Trying 'ramdisk-3' ramdisk subimage
     Description:  Initial Ram File System
     Type:         RAMDisk Image
     Compression:  uncompressed
     Data Start:   0x9063a730
     Data Size:    2856193 Bytes = 2.7 MiB
     Architecture: AArch64
     OS:           Linux
     Load Address: 0x9c000000
     Entry Point:  0x9c000000
     Hash algo:    sha1
     Hash value:   6141c365ec6e58ba6e7ce48e35ba161dcf8a294a
     Sign algo:    sha1,rsa2048:
     Sign value:   unavailable
   Verifying Hash Integrity ... sha1+ sha1,rsa2048:- OK
   Loading ramdisk from 0x9063a730 to 0x9c000000
## Loading fdt (any) from FIT Image at 90000000 ...
   Using 'conf-1' configuration
   Verifying Hash Integrity ... OK
   Trying 'fdt-2' fdt subimage
     Description:  Flattened Device Tree Blob
     Type:         Flat Device Tree
     Compression:  uncompressed
     Data Start:   0x906347e0
     Data Size:    24124 Bytes = 23.6 KiB
     Architecture: AArch64
     Load Address: 0x99000000
     Hash algo:    sha1
     Hash value:   e6d070dfbe8e759f9111a3da32a4d358a76758d6
     Sign algo:    sha1,rsa2048:
     Sign value:   unavailable
   Verifying Hash Integrity ... sha1+ sha1,rsa2048:- OK
   Loading fdt from 0x906347e0 to 0x99000000
   Booting using the fdt blob at 0x99000000
Working FDT set to 99000000
   Uncompressing Kernel Image to 9a200000
   Loading Device Tree to 00000000beeb9000, end 00000000beec1e3b ... OK
Working FDT set to beeb9000

Starting kernel ...

[    0.000000] Booting Linux on physical CPU 0x0000000000 [0x412fd050]
[    0.000000] Linux version 6.18.31-yocto-standard-00206-gf16fdb1a2745-dirty (oe-user@oe-host) (aarch64-adi_glibc-linux-gcc (GCC) 13.4.0, GNU ld (GNU Binutils) 2.42.0.20240723) #1 SMP PREEMPT Fri Aug  7 10:16:31 UTC 2026
[    0.000000] Machine model: ADI 64-bit SC84X
[    0.000000] earlycon: adi_uart0 at MMIO 0x0000000031003000 (options '')
[    0.000000] printk: legacy bootconsole [adi_uart0] enabled
[    0.000000] efi: UEFI not found.
[    0.000000] OF: reserved mem: 0x0000000020000000..0x00000000200003ff (1 KiB) nomap non-reusable rsc_tbl0@20000000
[    0.000000] OF: reserved mem: 0x0000000020000400..0x00000000200007ff (1 KiB) nomap non-reusable rsc_tbl0@20000400
[    0.000000] OF: reserved mem: 0x0000000020005000..0x0000000020024fff (128 KiB) nomap non-reusable sharc_internal_icc@20005000
[    0.000000] OF: reserved mem: 0x0000000020040000..0x000000002007ffff (256 KiB) map non-reusable sram1-reserved@20040000
[    0.000000] OF: reserved mem: 0x0000000020080000..0x0000000020083fff (16 KiB) nomap non-reusable vdev0vring0@20080000
[    0.000000] Reserved memory: created DMA memory pool at 0x0000000020084000, size 0 MiB
[    0.000000] OF: reserved mem: initialized node vdev0buffer@20084000, compatible id shared-dma-pool
[    0.000000] OF: reserved mem: 0x0000000020084000..0x00000000200a3fff (128 KiB) nomap non-reusable vdev0buffer@20084000
[    0.000000] OF: reserved mem: 0x00000000200a4000..0x00000000200a7fff (16 KiB) nomap non-reusable vdev0vring0@200A4000
[    0.000000] Reserved memory: created DMA memory pool at 0x00000000200a8000, size 0 MiB
[    0.000000] OF: reserved mem: initialized node vdev0buffer@200A8000, compatible id shared-dma-pool
[    0.000000] OF: reserved mem: 0x00000000200a8000..0x00000000200c7fff (128 KiB) nomap non-reusable vdev0buffer@200A8000
[    0.000000] Zone ranges:
[    0.000000]   DMA      [mem 0x0000000020040000-0x00000000bfffffff]
[    0.000000]   DMA32    empty
[    0.000000]   Normal   empty
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x0000000020040000-0x000000002007ffff]
[    0.000000]   node   0: [mem 0x0000000080000000-0x00000000bfffffff]
[    0.000000] Initmem setup node 0 [mem 0x0000000020040000-0x00000000bfffffff]
[    0.000000] On node 0, zone DMA: 64 pages in unavailable ranges
[    0.000000] On node 0, zone DMA: 32640 pages in unavailable ranges
[    0.000000] percpu: Embedded 29 pages/cpu s78744 r8192 d31848 u118784
[    0.000000] Detected VIPT I-cache on CPU0
[    0.000000] CPU features: detected: GICv3 CPU interface
[    0.000000] CPU features: detected: Virtualization Host Extensions
[    0.000000] CPU features: detected: ARM errata 1165522, 1319367, or 1530923
[    0.000000] alternatives: applying boot alternatives
[    0.000000] Kernel command line: root=/dev/nfs rw nfsroot=10.42.0.1:/romfs,tcp,nfsvers=3 earlycon=adi_uart,0x31003000 console=ttySC0,115200 vmalloc=512M cma=64M coherent_pool=32M clk_ignore_unused ip=10.42.0.2:10.42.0.1:0.0.0.0:255.255.255.0:sc846:eth0:off
[    0.000000] Unknown kernel command line parameters "vmalloc=512M cma=64M", will be passed to user space.
[    0.000000] printk: log_buf_len individual max cpu contribution: 4096 bytes
[    0.000000] printk: log_buf_len total cpu_extra contributions: 4096 bytes
[    0.000000] printk: log_buf_len min size: 4096 bytes
[    0.000000] printk: log buffer data + meta data: 8192 + 28672 = 36864 bytes
[    0.000000] printk: early log buf free: 760(18%)
[    0.000000] Dentry cache hash table entries: 131072 (order: 8, 1048576 bytes, linear)
[    0.000000] Inode-cache hash table entries: 65536 (order: 7, 524288 bytes, linear)
[    0.000000] software IO TLB: SWIOTLB bounce buffer size adjusted to 1MB
[    0.000000] software IO TLB: area num 2.
[    0.000000] software IO TLB: SWIOTLB bounce buffer size roundup to 2MB
[    0.000000] software IO TLB: mapped [mem 0x00000000bfa04000-0x00000000bfc04000] (2MB)
[    0.000000] Built 1 zonelists, mobility grouping on.  Total pages: 262208
[    0.000000] mem auto-init: stack:all(zero), heap alloc:off, heap free:off
[    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=2, Nodes=1
[    0.000000] rcu: Preemptible hierarchical RCU implementation.
[    0.000000] rcu:     RCU restricting CPUs from NR_CPUS=512 to nr_cpu_ids=2.
[    0.000000]  Trampoline variant of Tasks RCU enabled.
[    0.000000]  Tracing variant of Tasks RCU enabled.
[    0.000000] rcu: RCU calculated value of scheduler-enlistment delay is 25 jiffies.
[    0.000000] rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=2
[    0.000000] RCU Tasks: Setting shift to 1 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=2.
[    0.000000] RCU Tasks Trace: Setting shift to 1 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=2.
[    0.000000] NR_IRQS: 64, nr_irqs: 64, preallocated irqs: 0
[    0.000000] GICv3: GIC: Using split EOI/Deactivate mode
[    0.000000] GICv3: 448 SPIs implemented
[    0.000000] GICv3: 0 Extended SPIs implemented
[    0.000000] Root IRQ handler: gic_handle_irq
[    0.000000] GICv3: GICv3 features: 16 PPIs
[    0.000000] GICv3: GICD_CTLR.DS=0, SCR_EL3.FIQ=0
[    0.000000] GICv3: CPU0: found redistributor 0 region 0:0x0000000031240000
[    0.000000] rcu: srcu_init: Setting srcu_struct sizes based on contention.
[    0.000000] arch_timer: cp15 timer running at 31.25MHz (phys).
[    0.000000] clocksource: arch_sys_counter: mask: 0xffffffffffffff max_cycles: 0xe6a171046, max_idle_ns: 881590405314 ns
[    0.000002] sched_clock: 56 bits at 31MHz, resolution 32ns, wraps every 4398046511088ns
[    0.009019] Console: colour dummy device 80x25
[    0.013482] Calibrating delay loop (skipped), value calculated using timer frequency.. 62.50 BogoMIPS (lpj=125000)
[    0.023781] pid_max: default: 32768 minimum: 301
[    0.028827] LSM: initializing lsm=capability
[    0.033495] Mount-cache hash table entries: 2048 (order: 2, 16384 bytes, linear)
[    0.040841] Mountpoint-cache hash table entries: 2048 (order: 2, 16384 bytes, linear)
[    0.052203] cacheinfo: Unable to detect cache hierarchy for CPU 0
[    0.063352] rcu: Hierarchical SRCU implementation.
[    0.068071] rcu:     Max phase no-delay instances is 1000.
[    0.074409] Timer migration: 1 hierarchy levels; 8 children per group; 1 crossnode level
[    0.083901] EFI services will not be available.
[    0.089031] smp: Bringing up secondary CPUs ...
[    0.093511] smp: Brought up 1 node, 1 CPU
[    0.097433] SMP: Total of 1 processors activated.
[    0.102225] CPU: All CPU(s) started at EL2
[    0.106337] CPU features: detected: 32-bit EL0 Support
[    0.111415] CPU features: detected: Data cache clean to the PoU not required for I/D coherence
[    0.120013] CPU features: detected: CRC32 instructions
[    0.125162] CPU features: detected: RCpc load-acquire (LDAPR)
[    0.130891] CPU features: detected: LSE atomic instructions
[    0.136459] CPU features: detected: Privileged Access Never
[    0.142029] CPU features: detected: PMUv3
[    0.146054] CPU features: detected: Speculative Store Bypassing Safe (SSBS)
[    0.153078] alternatives: applying system-wide alternatives
[    0.162873] Memory: 1000236K/1048832K available (9088K kernel code, 1414K rwdata, 2996K rodata, 2816K init, 393K bss, 44556K reserved, 0K cma-reserved)
[    0.177683] devtmpfs: initialized
[    0.207706] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645041785100000 ns
[    0.217454] posixtimers hash table entries: 1024 (order: 2, 16384 bytes, linear)
[    0.224848] futex hash table entries: 512 (32768 bytes on 1 NUMA nodes, total 32 KiB, linear).
[    0.233612] 28544 pages in range for non-PLT usage
[    0.233642] 520064 pages in range for PLT usage
[    0.238856] pinctrl core: initialized pinctrl subsystem
[    0.249484] DMI not present or invalid.
[    0.254844] NET: Registered PF_NETLINK/PF_ROUTE protocol family
[    0.264816] DMA: preallocated 4096 KiB GFP_KERNEL pool for atomic allocations
[    0.273824] DMA: preallocated 4096 KiB GFP_KERNEL|GFP_DMA pool for atomic allocations
[    0.283523] DMA: preallocated 4096 KiB GFP_KERNEL|GFP_DMA32 pool for atomic allocations
[    0.291564] audit: initializing netlink subsys (disabled)
[    0.297394] audit: type=2000 audit(0.192:1): state=initialized audit_enabled=0 res=1
[    0.307644] hw-breakpoint: found 6 breakpoint and 4 watchpoint registers.
[    0.314496] ASID allocator initialised with 65536 entries
[    0.320639] Serial: AMBA PL011 UART driver
[    0.391144] HugeTLB: registered 1.00 GiB page size, pre-allocated 0 pages
[    0.405960] HugeTLB: 0 KiB vmemmap can be freed for a 1.00 GiB page
[    0.416200] HugeTLB: registered 32.0 MiB page size, pre-allocated 0 pages
[    0.430971] HugeTLB: 0 KiB vmemmap can be freed for a 32.0 MiB page
[    0.445237] HugeTLB: registered 2.00 MiB page size, pre-allocated 0 pages
[    0.455982] HugeTLB: 0 KiB vmemmap can be freed for a 2.00 MiB page
[    0.470246] HugeTLB: registered 64.0 KiB page size, pre-allocated 0 pages
[    0.485015] HugeTLB: 0 KiB vmemmap can be freed for a 64.0 KiB page
[    0.505714] iommu: Default domain type: Translated
[    0.518515] iommu: DMA domain TLB invalidation policy: strict mode
[    0.530049] SCSI subsystem initialized
[    0.538740] usbcore: registered new interface driver usbfs
[    0.552393] usbcore: registered new interface driver hub
[    0.561827] usbcore: registered new device driver usb
[    0.577341] i2c-adi-twi 31001600.twi: ADI on-chip I2C TWI Controller, regs_base@(____ptrval____)
[    0.595696] i2c-adi-twi 31001200.twi: ADI on-chip I2C TWI Controller, regs_base@(____ptrval____)
[    0.628705] clocksource: Switched to clocksource arch_sys_counter
[    6.270286] VFS: Disk quotas dquot_6.6.0
[    6.275717] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
[    6.319218] NET: Registered PF_INET protocol family
[    6.324562] IP idents hash table entries: 16384 (order: 5, 131072 bytes, linear)
[    6.337797] tcp_listen_portaddr_hash hash table entries: 512 (order: 1, 8192 bytes, linear)
[    6.346154] Table-perturb hash table entries: 65536 (order: 6, 262144 bytes, linear)
[    6.353923] TCP established hash table entries: 8192 (order: 4, 65536 bytes, linear)
[    6.361860] TCP bind hash table entries: 8192 (order: 6, 262144 bytes, linear)
[    6.369636] TCP: Hash tables configured (established 8192 bind 8192)
[    6.376143] UDP hash table entries: 512 (order: 3, 32768 bytes, linear)
[    6.382820] UDP-Lite hash table entries: 512 (order: 3, 32768 bytes, linear)
[    6.390307] NET: Registered PF_UNIX/PF_LOCAL protocol family
[    6.397397] RPC: Registered named UNIX socket transport module.
[    6.403257] RPC: Registered udp transport module.
[    6.407942] RPC: Registered tcp transport module.
[    6.412640] RPC: Registered tcp-with-tls transport module.
[    6.418122] RPC: Registered tcp NFSv4.1 backchannel transport module.
[    6.425295] Unpacking initramfs...
[    6.433164] Initialise system trusted keyrings
[    6.448015] workingset: timestamp_bits=46 max_order=18 bucket_order=0
[    6.463516] NFS: Registering the id_resolver key type
[    6.475123] Key type id_resolver registered
[    6.483055] Key type id_legacy registered
[    6.491110] nfs4filelayout_init: NFSv4 File Layout Driver Registering...
[    6.507058] nfs4flexfilelayout_init: NFSv4 Flexfile Layout Driver Registering...
[    6.519218] jffs2: version 2.2. (NAND) © 2001-2006 Red Hat, Inc.
[    7.004765] Key type asymmetric registered
[    7.015171] Asymmetric key parser 'x509' registered
[    7.023319] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 247)
[    7.039062] io scheduler mq-deadline registered
[    7.047073] io scheduler kyber registered
[    7.055209] io scheduler bfq registered
[    7.071121] ledtrig-cpu: registered to indicate activity on CPUs
[    7.084693] adi-dma 31022000.dma: Creating new peripheral DMA controller instance
[    7.106888] adi-dma 31023000.dma: Creating new peripheral DMA controller instance
[    7.130856] adi-dma 3102d000.dma: Creating new peripheral DMA controller instance
[    7.174427] adi-dma 310a7000.dma: Creating new peripheral DMA controller instance
[    7.204595] genirq: Flags mismatch irq 27. 00000004 (dma controller error irq) vs. 00000004 (dma controller error irq)
[    7.227205] adi-dma 310a7000.dma: error -EBUSY: request_irq(27) adi_dma_error_handler adi_dma_thread_handler dma controller error irq
[    7.251098] adi-dma 310a7000.dma: Failed to request IRQ -16
[    7.263102] adi-dma 310a7000.dma: probe with driver adi-dma failed with error -16
[    7.280573] adi-dma 31026000.dma: Creating new peripheral DMA controller instance
[    7.319714] adi-dma 3109a000.dma: Creating new MDMA controller instance
[    7.369762] Serial: 8250/16550 driver, 4 ports, IRQ sharing enabled
[    7.399762] ADI serial driver
[    7.407116] adi-uart4 31003000.uart: Serial probe
[    7.416340] 31003000.uart: ttySC0 at MMIO 0x0 (irq = 0, base_baud = 7812500) is a ADI-UART4
[    7.435146] printk: legacy console [ttySC0] enabled
[    7.435146] printk: legacy console [ttySC0] enabled
[    7.455051] printk: legacy bootconsole [adi_uart0] disabled
[    7.455051] printk: legacy bootconsole [adi_uart0] disabled
[    7.497657] adi-spi3 3102f000.spi: EARLY rate=125000000 enabled=1 enable_count=0
[    7.515894] adi-spi3 3102f000.spi: A rate=125000000 enabled=1
[    7.527228] adi-spi3 3102f000.spi: B rate=125000000 enabled=1
[    7.680853] Freeing initrd memory: 2788K
[    7.700327] 4 fixed-partitions partitions found on MTD device spi1.0
[    7.706765] Creating 4 MTD partitions on "spi1.0":
[    7.711586] 0x000000000000-0x000000040000 : "u-boot spl"
[    7.736192] 0x000000040000-0x000000100000 : "u-boot proper"
[    7.748109] 0x000000210000-0x000001210000 : "kernel"
[    7.764099] 0x000001210000-0x000010000000 : "rootfs"
[    7.780333] adi-spi3 3102f000.spi: registered ADI SPI controller spi1
[    7.791516] adi-dwmac 31040000.ethernet: IRQ eth_wake_irq not found
[    7.797753] adi-dwmac 31040000.ethernet: IRQ sfty not found
[    7.803504] OF: /scb/ethernet@31040000: Read of boolean property 'snps,tso' with a value.
[    7.811780] adi-dwmac 31040000.ethernet: PTP uses main clock
[    7.817968] adi-dwmac 31040000.ethernet: User ID: 0x10, Synopsys ID: 0x53
[    7.824700] adi-dwmac 31040000.ethernet:     DWMAC4/5
[    7.829458] adi-dwmac 31040000.ethernet: DMA HW capability register supported
[    7.836570] adi-dwmac 31040000.ethernet: RX Checksum Offload Engine supported
[    7.843686] adi-dwmac 31040000.ethernet: TX Checksum insertion supported
[    7.850369] adi-dwmac 31040000.ethernet: Wake-Up On Lan supported
[    7.856452] adi-dwmac 31040000.ethernet: TSO supported
[    7.861568] adi-dwmac 31040000.ethernet: Enable RX Mitigation via HW Watchdog Timer
[    7.869220] adi-dwmac 31040000.ethernet: Enabled L3L4 Flow TC (entries=8)
[    7.875998] adi-dwmac 31040000.ethernet: Enabled RFS Flow TC (entries=10)
[    7.882749] adi-dwmac 31040000.ethernet: TSO feature enabled
[    7.888388] adi-dwmac 31040000.ethernet: SPH feature enabled
[    7.894031] adi-dwmac 31040000.ethernet: Using 32/32 bits DMA host/device width
[    7.927989] usbcore: registered new interface driver usb-storage
[    7.937898] i2c_dev: i2c /dev entries driver
[    7.944352] adi_wdt: initialized: timeout=30 sec (nowayout=0)
[    7.952697] sdhci: Secure Digital Host Controller Interface driver
[    7.958898] sdhci: Copyright(c) Pierre Ossman
[    7.963244] Synopsys Designware Multimedia Card Interface Driver
[    7.969540] sdhci-pltfm: SDHCI platform and OF driver helper
[    7.978169] hw perfevents: enabled with armv8_pmuv3 PMU driver, 7 (0,8000003f) counters available
[    7.989506] NET: Registered PF_PACKET protocol family
[    7.994721] 8021q: 802.1Q VLAN Support v1.8
[    7.999167] Key type dns_resolver registered
[    8.043663] registered taskstats version 1
[    8.048022] Loading compiled-in X.509 certificates
[    8.124412] adi-dwmac 31040000.ethernet eth0: Register MEM_TYPE_PAGE_POOL RxQ-0
[    8.141739] adi-dwmac 31040000.ethernet eth0: PHY [stmmac-0:00] driver [Generic PHY] (irq=POLL)
[    8.151743] adi-dwmac 31040000.ethernet eth0: No Safety Features support found
[    8.160960] adi-dwmac 31040000.ethernet eth0: IEEE 1588-2008 Advanced Timestamp supported
[    8.169170] adi-dwmac 31040000.ethernet eth0: configuring for phy/rgmii-id link mode
[    8.183951] 8021q: adding VLAN 0 to HW filter on device eth0
[   12.264041] adi-dwmac 31040000.ethernet eth0: Link is Up - 1Gbps/Full - flow control off
[   12.287077] IP-Config: Complete:
[   12.290162]      device=eth0, hwaddr=02:80:ad:20:31:e8, ipaddr=10.42.0.2, mask=255.255.255.0, gw=255.255.255.255
[   12.300459]      host=sc846, domain=, nis-domain=(none)
[   12.305594]      bootserver=10.42.0.1, rootserver=10.42.0.1, rootpath=
[   12.306681] clk: Not disabling unused clocks
[   12.322365] Freeing unused kernel memory: 2816K
[   12.327343] Run /init as init process
[   12.545770]  
[   12.545770]          Analog Initial Ram Filesystem
[   12.545770]                 www.analog.com
[   12.545770]               www.yoctoproject.org
[   12.545770] 
[   12.545770] Analog [Initramfs]: Preparing Operating System....
[   12.545770] Analog [Initramfs]: Mounting Root File System...
[   12.672086] Analog [Initramfs]: Switching RFS to NFS mount (tcp,nfsvers=3,10.42.0.1:/romfs)...
[   13.025736] 
[   13.027553] ====================================
[   13.032384] REACHED REAL NFS ROOTFS /sbin/init
[   13.036937] ====================================
[   13.041563] 
sh: cannot set terminal process group (-1): Inappropriate ioctl for device
sh: no job control in this shell
sh-5.2# 

```

```
root@adsp-sc598-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                                                     
                                 enable  prepare  protect                                duty  hardware                            connection                                                                          
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                                                          
---------------------------------------------------------------------------------------------------------------------------------------------                                                                          
 emac1_clkin                         0       0        0        50000000    0          0     50000      Y   deviceless                      no_connection_id                                                            
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                                                            
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                                                  
                                                                                                           deviceless                      no_connection_id                                                            
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                                                  
                                                                                                           deviceless                      no_connection_id                                                            
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                                         
       cgu0_vco                      1       1        0        4000000000  0          0     50000      Y         deviceless                      no_connection_id                                                      
          cclk2_0                    0       0        0        1333333333  0          0     50000      Y            deviceless                      no_connection_id                                                   
          cgu0_pllclk                3       3        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id                                                   
             cgu0_s1selexdiv         1       1        0        333333334   0          0     50000      Y               deviceless                      no_connection_id                                                
                cgu0_sclk1sel        1       1        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   sclk1_0           1       1        0        333333334   0          0     50000      Y                     31002400.i2s                    sclk                                                      
                                                                                                                             deviceless                      no_connection_id                                          
                      spdif_sel      0       0        0        333333334   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         spdif       0       0        0        333333334   0          0     50000      N                           deviceless                      no_connection_id                                    
             cgu0_odiv               0       0        0        250000000   0          0     50000      Y               deviceless                      no_connection_id                                                
                oclk_0               0       0        0        250000000   0          0     50000      N                  deviceless                      no_connection_id                                             
                   lp_ddr_sel        0       0        0        250000000   0          0     50000      Y                     deviceless                      no_connection_id                                          
                      lp_ddr         0       0        0        250000000   0          0     50000      N                        deviceless                      no_connection_id                                       
             cgu0_ddiv               0       0        0        666666667   0          0     50000      Y               deviceless                                                                                      
     no_connection_id                                                                                                                                                                                                  
                dclk_0               0       0        0        666666667   0          0     50000      N                  deviceless                      no_connection_id                                             
                   cdu_ddr_sel       0       0        0        666666667   0          0     50000      Y                     deviceless                      no_connection_id                                          
                      cdu_ddr        0       0        0        666666667   0          0     50000      N                        deviceless                      no_connection_id                                       
                   dclk_0_half       0       0        0        333333333   0          0     50000      Y                     deviceless                      no_connection_id                                          
             sysclk_0                1       1        0        500000000   0          0     50000      Y               deviceless                      no_connection_id                                                
                ospi_refclk_sel      0       0        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   ospi_refclk       0       0        0        500000000   0          0     50000      N                     deviceless                      no_connection_id                                          
                cgu0_s1seldiv        0       0        0        250000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                cgu0_s0seldiv        1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   sclk0_0           6       6        0        125000000   0          0     50000      Y                     31008000.watchdog               adi-watchdog                                              
                                                                                                                             31003000.uart                   sclk0                                                     
                                                                                                                             31001600.twi                    sclk0                                                     
                                                                                                                             31001400.twi                    sclk0                                                     
                                                                                                                             gptimers@31018000               no_connection_id                                          
                                                                                                                             deviceless                      no_connection_id                                          
                      trace_sel      0       0        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         trace       0       0        0        125000000   0          0     50000      N                           deviceless                      no_connection_id                                    
                      lp_sel         0       0        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         lp          0       0        0        125000000   0          0     50000      N                           deviceless                      no_connection_id                                    
                      gige_sel       1       1        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         gige        1       1        0        125000000   0          0     50000      Y                           31040000.ethernet               stmmaceth                                           
                                                                                                                                   deviceless                      no_connection_id                                    
                                                                                                                                                                                                                       
                      spi_sel        1       1        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         spi         1       1        0        125000000   0          0     50000      Y                           31030000.spi                    spi                                                 
                                                                                                                                   deviceless                      no_connection_id                                    
             cgu0_cdiv               1       1        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                                                
                cclk0_0              2       2        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id                                             
                   sharc1_sel        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                                          
                      sharc1         1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id                                       
                   sharc0_sel        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                                          
                      sharc0         1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id                                       
    cgu1_in_sel                      2       2        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                                         
       3pll_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                                                      
          3pll_vco                   1       1        0        3200000000  0          0     50000      Y            deviceless                      no_connection_id                                                   
             3pll_pllclk             1       1        0        1600000000  0          0     50000      Y               deviceless                      no_connection_id                                                
                3pll_ddiv            1       1        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   ddr               1       1        0        800000000   0          0     50000      Y                     deviceless                      no_connection_id                                          
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                                                      
          cgu1_vco                   2       2        0        3600000000  0          0     50000      Y            deviceless                      no_connection_id                                                   
             cclk2_1                 1       1        0        1200000000  0          0     50000      Y               deviceless                      no_connection_id                                                
                arm_sel              1       1        0        1200000000  0          0     50000      Y                  deviceless                      no_connection_id                                             
                   arm               1       1        0        1200000000  0          0     50000      Y                     deviceless                      no_connection_id                                          
             cgu1_pllclk             1       1        0        1800000000  0          0     50000      Y               deviceless                      no_connection_id                                                
                cgu1_s1selexdiv      0       0        0        20000000    0          0     50000      Y                  deviceless                      no_connection_id                                             
                   cgu1_sclk1sel     0       0        0        20000000    0          0     50000      Y                                                                                                               
     deviceless                      no_connection_id                                                                                                                                                                  
                      sclk1_1        0       0        0        20000000    0          0     50000      N                        deviceless                      no_connection_id                                       
                         sclk1_1_half 0       0        0        10000000    0          0     50000      Y                           deviceless                      no_connection_id                                   
                            emmc_timer_qmc_sel 0       0        0        10000000    0          0     50000      Y                              deviceless                      no_connection_id                       
                               emmc_timer_qmc 0       0        0        10000000    0          0     50000      N                                 deviceless                      no_connection_id                     
                cgu1_s0selexdiv      1       1        0        50000000    0          0     50000      Y                  deviceless                      no_connection_id                                             
                   cgu1_sclk0sel     1       1        0        50000000    0          0     50000      Y                     deviceless                      no_connection_id                                          
                      sclk0_1        1       1        0        50000000    0          0     50000      Y                        deviceless                      no_connection_id                                       
                         emmc_sel    1       1        0        50000000    0          0     50000      Y                           deviceless                      no_connection_id                                    
                            emmc     1       1        0        50000000    0          0     50000      Y                              310c7000.mmc                    core                                             
                                                                                                                                      deviceless                      no_connection_id                                 
                cgu1_odiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   oclk_1            0       0        0        112500000   0          0     50000      N                     deviceless                      no_connection_id                                          
                      can_sel        0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id                                       
                         can         0       0        0        112500000   0          0     50000      N                           deviceless                      no_connection_id                                    
                cgu1_ddiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   dclk_1            0       0        0        100000000   0          0     50000      N                     deviceless                      no_connection_id                                          
                      dclk_1_half    0       0        0        50000000    0          0     50000      Y                        deviceless                      no_connection_id                                       
                sysclk_1             0       0        0        225000000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   cgu1_s1seldiv     0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id                                          
                   cgu1_s0seldiv     0       0        0        56250000    0          0     50000      Y                     deviceless                      no_connection_id                                          
                cgu1_cdiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                                             
                   cclk0_1           0       0        0        112500000   0          0     50                                                                                                                         
000      N                     deviceless                      no_connection_id                                                                                                                                        
root@adsp-sc598-som-ezkit:~#
```


```
root@adsp-sc589-mini:/sys/kernel/debug/clk# cat clk_summary                                                                                                                               
                                 enable  prepare  protect                                duty  hardware                            connection                                             
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                             
---------------------------------------------------------------------------------------------------------------------------------------------                                             
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                               
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                     
                                                                                                           deviceless                      no_connection_id                               
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                     
                                                                                                           deviceless                      no_connection_id                               
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu0_vco                      1       1        0        450000000   0          0     50000      Y         deviceless                      no_connection_id                         
          cgu0_pllclk                4       4        0        450000000   0          0     50000      Y            deviceless                      no_connection_id                      
             cgu0_odiv               1       1        0        150000000   0          0     50000      Y               deviceless                      no_connection_id                   
                oclk_0               1       1        0        150000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   spdif_sel         0       0        0        150000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      spdif          0       0        0        150000000   0          0     50000      N                        deviceless                      no_connection_id          
                   can_sel           0       0        0        150000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      can            0       0        0        150000000   0          0     50000      N                        deviceless                      no_connection_id          
                   oclk_0_half       1       1        0        75000000    0          0     50000      Y                     deviceless                      no_connection_id             
                      sdio_sel       1       1        0        75000000    0          0     50000      Y                        deviceless                      no_connection_id          
                         sdio        1       1        0        75000000    0          0     50000      Y                           31010000.mmc                    ciu                    
                                                                                                                                   deviceless                      no_connection_id       
             cgu0_ddiv               1       1        0        450000000   0          0     50000      Y               deviceless                      no_connection_id                   
                dclk_0               1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   cdu_ddr_sel       1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      cdu_ddr        1       1        0        450000000   0          0     50000      Y                        deviceless                      no_connection_id          
             sysclk_0                2       2        0        225000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cgu0_s1seldiv        1       1        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk1_0           2       2        0        112500000   0          0     50000      Y                     31002000.i2s-sport0             sclk                         
                                                                                                                             31042000.spi                    spi                          
                                                                                                                             deviceless                      no_connection_id             
                cgu0_s0seldiv        1       1        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk0_0           7       7        0        112500000   0          0     50000      Y                     31010000.mmc                    biu                          
                                                                                                                             31008000.watchdog               adi-watchdog                 
                                                                                                                             31044000.spi                    spi                          
                                                                                                                             31003000.uart                   sclk0                        
                                                                                                                             31001600.twi                    sclk0                        
                                                                                                                             31001500.twi                    sclk0                        
                                                                                                                             31001400.twi                    sclk0                        
                                                                                                                             gptimers@31001000               no_connection_id             
                                                                                                                             deviceless                      no_connection_id             
                      lp_sel         0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id          
                         lp          0       0        0        112500000   0          0     50000      N                           deviceless                      no_connection_id       
                      reserved_sel   0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id          
                         reserved    0       0        0        112500000   0          0     50000      N                           deviceless                      no_connection_id       
             cgu0_cdiv               2       2        0        450000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cclk1_0              1       1        0        450000000   0          0     50000      N                  deviceless                      no_connection_id                
                   arm_sel           1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      arm            1       1        0        450000000   0          0     50000      Y                        deviceless                      no_connection_id          
                cclk0_0              2       2        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   sharc1_sel        1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      sharc1         1       1        0        450000000   0          0     50000      Y                        deviceless                      no_connection_id          
                   sharc0_sel        1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      sharc0         1       1        0        450000000   0          0     50000      Y                        deviceless                      no_connection_id          
    cgu1_in_sel                      1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                         
          cgu1_vco                   1       1        0        125000000   0          0     50000      Y            deviceless                      no_connection_id                      
             cgu1_pllclk             1       1        0        125000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cgu1_odiv            0       0        0        41666667    0          0     50000      Y                  deviceless                      no_connection_id                
                   oclk_1            0       0        0        41666667    0          0     50000      N                     deviceless                      no_connection_id             
                cgu1_ddiv            0       0        0        62500000    0          0     50000      Y                  deviceless                      no_connection_id                
                   dclk_1            0       0        0        62500000    0          0     50000      N                     deviceless                      no_connection_id             
                sysclk_1             0       0        0        62500000    0          0     50000      Y                  deviceless                      no_connection_id                
                   cgu1_s1seldiv     0       0        0        31250000    0          0     50000      Y                     deviceless                      no_connection_id             
                      sclk1_1        0       0        0        31250000    0          0     50000      N                        deviceless                      no_connection_id          
                   cgu1_s0seldiv     0       0        0        31250000    0          0     50000      Y                     deviceless                      no_connection_id             
                      sclk0_1        0       0        0        31250000    0          0     50000      N                        deviceless                      no_connection_id          
                cgu1_cdiv            1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   cclk1_1           0       0        0        125000000   0          0     50000      N                     deviceless                      no_connection_id             
                      cclk1_1_half   0       0        0        62500000    0          0     50000      Y                        deviceless                      no_connection_id          
                   cclk0_1           1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      gige_sel       1       1        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         gige        1       1        0        125000000   0          0     50000      Y                           3100c000.ethernet               stmmaceth              
                                                                                                                                   deviceless                      no_connection_id       
root@adsp-sc589-mini:/sys/kernel/debug/clk#                                                                                                                                               
```

```
                                                                                                                                                                                          
root@adsp-sc594-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                        
                                 enable  prepare  protect                                duty  hardware                            connection                                             
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                             
---------------------------------------------------------------------------------------------------------------------------------------------                                             
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                               
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                     
                                                                                                           deviceless                      no_connection_id                               
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                     
                                                                                                           deviceless                      no_connection_id                               
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu0_vco                      1       1        0        2000000000  0          0     50000      Y         deviceless                      no_connection_id                         
          cgu0_pllclk                2       2        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id                      
             cgu0_s1selexdiv         0       0        0        333333334   0          0     50000      Y               deviceless                      no_connection_id                   
                cgu0_sclk1sel        0       0        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk1_0           0       0        0        333333334   0          0     50000      N                     deviceless                      no_connection_id             
                      spdif_sel      0       0        0        333333334   0          0     50000      Y                        deviceless                      no_connection_id          
                         spdif       0       0        0        333333334   0          0     50000      N                           deviceless                      no_connection_id       
             cgu0_odiv               0       0        0        125000000   0          0     50000      Y               deviceless                      no_connection_id                   
                oclk_0               0       0        0        125000000   0          0     50000      N                  deviceless                      no_connection_id                
                   lpddr_sel         0       0        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      lpddr          0       0        0        125000000   0          0     50000      N                        deviceless                      no_connection_id          
             cgu0_ddiv               0       0        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                   
                dclk_0               0       0        0        1000000000  0          0     50000      N                  deviceless                      no_connection_id                
             sysclk_0                1       1        0        500000000   0          0     50000      Y               deviceless                      no_connection_id                   
                ospi_sel             0       0        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   ospi              0       0        0        500000000   0          0     50000      N                     deviceless                      no_connection_id             
                cgu0_s1seldiv        0       0        0        250000000   0          0     50000      Y                  deviceless                      no_connection_id                
                cgu0_s0seldiv        1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk0_0           6       6        0        125000000   0          0     50000      Y                     31002400.i2s                    sclk                         
                                                                                                                             31008000.watchdog               adi-watchdog                 
                                                                                                                             31003000.uart                   sclk0                        
                                                                                                                             31001600.twi                    sclk0                        
                                                                                                                             gptimers@31018000               no_connection_id             
                                                                                                                             deviceless                      no_connection_id             
                      trace_sel      0       0        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         trace       0       0        0        125000000   0          0     50000      N                           deviceless                      no_connection_id       
                      lp_sel         0       0        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         lp          0       0        0        125000000   0          0     50000      N                           deviceless                      no_connection_id       
                      gige_sel       1       1        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         gige        1       1        0        125000000   0          0     50000      Y                           31040000.ethernet               stmmaceth              
                                                                                                                                   deviceless                      no_connection_id       
                      spi_sel        1       1        0        125000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         spi         1       1        0        125000000   0          0     50000      Y                           31030000.spi                    spi                    
                                                                                                                                   deviceless                      no_connection_id       
             cgu0_cdiv               2       2        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                   
                cclk1_0              1       1        0        1000000000  0          0     50000      N                  deviceless                      no_connection_id                
                   arm_sel           1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id             
                      arm            1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id          
                cclk0_0              2       2        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id                
                   sharc1_sel        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id             
                      sharc1         1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id          
                   sharc0_sel        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id             
                      sharc0         1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id          
    cgu1_in_sel                      1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                         
          cgu1_vco                   1       1        0        1600000000  0          0     50000      Y            deviceless                      no_connection_id                      
             cgu1_pllclk             1       1        0        1600000000  0          0     50000      Y               deviceless                      no_connection_id                   
                cgu1_s1selexdiv      0       0        0        50000000    0          0     50000      Y                  deviceless                      no_connection_id                
                cgu1_odiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   oclk_1            0       0        0        100000000   0          0     50000      N                     deviceless                      no_connection_id             
                      can_sel        0       0        0        100000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         can         0       0        0        100000000   0          0     50000      N                           deviceless                      no_connection_id       
                cgu1_ddiv            1       1        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   dclk_1            1       1        0        800000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      cdu_ddr_sel    1       1        0        800000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         cdu_ddr     1       1        0        800000000   0          0     50000      Y                           deviceless                      no_connection_id       
                sysclk_1             0       0        0        400000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   cgu1_s1seldiv     0       0        0        200000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      cgu1_sclk1sel  0       0        0        200000000   0          0     50000      Y                        deviceless                      no_connection_id          
                         sclk1_1     0       0        0        200000000   0          0     50000      N                           deviceless                      no_connection_id       
                   cgu1_s0seldiv     0       0        0        100000000   0          0     50000      Y                     deviceless                      no_connection_id             
                      sclk0_1        0       0        0        100000000   0          0     50000      N                        deviceless                      no_connection_id          
                cgu1_cdiv            0       0        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                
                   cclk1_1           0       0        0        800000000   0          0     50000      N                     deviceless                      no_connection_id             
                   cclk0_1           0       0        0        800000000   0          0     50000      N                     deviceless                      no_connection_id             
root@adsp-sc594-som-ezkit:~#                                                                                                                                                              
                                                                                                                                                                                          
```
```
root@adsp-sc573-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                         
                                 enable  prepare  protect                                duty  hardware                            connection                                          
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                          
---------------------------------------------------------------------------------------------------------------------------------------------                                          
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                            
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@0x3108d000               sys_clkin1                                  
                                                                                                           deviceless                      no_connection_id                            
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@0x3108d000               sys_clkin0                                  
                                                                                                           deviceless                      no_connection_id                            
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                         
       cgu0_pllclk                   4       4        0        450000000   0          0     50000      Y         deviceless                      no_connection_id                      
          cgu0_odiv                  1       1        0        150000000   0          0     50000      Y            deviceless                      no_connection_id                   
             oclk_0                  1       1        0        150000000   0          0     50000      Y               deviceless                      no_connection_id                
                spdif_sel            0       0        0        150000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   spdif             0       0        0        150000000   0          0     50000      N                     deviceless                      no_connection_id          
                can_sel              0       0        0        150000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   can               0       0        0        150000000   0          0     50000      N                     deviceless                      no_connection_id          
                oclk_0_half          1       1        0        75000000    0          0     50000      Y                  deviceless                      no_connection_id             
                   sdio_sel          1       1        0        75000000    0          0     50000      Y                     deviceless                      no_connection_id          
                      sdio           1       1        0        75000000    0          0     50000      Y                        31010000.mmc                    ciu                    
                                                                                                                                deviceless                      no_connection_id       
          cgu0_ddiv                  1       1        0        225000000   0          0     50000      Y            deviceless                      no_connection_id                   
             dclk_0                  1       1        0        225000000   0          0     50000      Y               deviceless                      no_connection_id                
                cdu_ddr_sel          1       1        0        225000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   cdu_ddr           1       1        0        225000000   0          0     50000      Y                     deviceless                                                
                 no_connection_id                                                                                                                                                      
          sysclk_0                   2       2        0        225000000   0          0     50000      Y            deviceless                      no_connection_id                   
             cgu0_s1seldiv           1       1        0        112500000   0          0     50000      Y               deviceless                      no_connection_id                
                sclk1_0              2       2        0        112500000   0          0     50000      Y                  31044000.spi                    spi                          
                                                                                                                          3102e000.spi                    spi                          
                                                                                                                          deviceless                      no_connection_id             
             cgu0_s0seldiv           1       1        0        112500000   0          0     50000      Y               deviceless                      no_connection_id                
                sclk0_0              7       7        0        112500000   0          0     50000      Y                  31002000.i2s                    sclk                         
                                                                                                                          31010000.mmc                    biu                          
                                                                                                                          31008000.watchdog               adi-watchdog                 
                                                                                                                          31003000.uart                   sclk0                        
                                                                                                                          31001600.twi                    sclk0                        
                                                                                                                          31001500.twi                    sclk0                        
                                                                                                                          31001400.twi                    sclk0                        
                                                                                                                          gptimers@0x31018000             no_connection_id             
                                                                                                                          deviceless                      no_connection_id             
          cgu0_cdiv                  2       2        0        450000000   0          0     50000      Y            deviceless                      no_connection_id                   
             cclk1_0                 1       1        0        450000000   0          0     50000      N               deviceless                      no_connection_id                
                arm_sel              1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   arm               1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id          
             cclk0_0                 2       2        0        450000000   0          0     50000      Y               deviceless                      no_connection_id                
                sharc1_sel           1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   sharc1            1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id          
                sharc0_sel           1       1        0        450000000   0          0                                                                                                
    50000      Y                  deviceless                      no_connection_id                                                                                                     
                   sharc0            1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id          
    cgu1_in_sel                      1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                         
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                      
          cgu1_pllclk                1       1        0        125000000   0          0     50000      Y            deviceless                      no_connection_id                   
             cgu1_odiv               0       0        0        41666667    0          0     50000      Y               deviceless                      no_connection_id                
                oclk_1               0       0        0        41666667    0          0     50000      N                  deviceless                      no_connection_id             
             cgu1_ddiv               0       0        0        62500000    0          0     50000      Y               deviceless                      no_connection_id                
                dclk_1               0       0        0        62500000    0          0     50000      N                  deviceless                      no_connection_id             
             sysclk_1                0       0        0        62500000    0          0     50000      Y               deviceless                      no_connection_id                
                cgu1_s1seldiv        0       0        0        31250000    0          0     50000      Y                  deviceless                      no_connection_id             
                   sclk1_1           0       0        0        31250000    0          0     50000      N                     deviceless                      no_connection_id          
                cgu1_s0seldiv        0       0        0        31250000    0          0     50000      Y                  deviceless                      no_connection_id             
                   sclk0_1           0       0        0        31250000    0          0     50000      N                     deviceless                      no_connection_id          
             cgu1_cdiv               1       1        0        125000000   0          0     50000      Y               deviceless                      no_connection_id                
                cclk1_1              0       0        0        125000000   0          0     50000      N                  deviceless                      no_connection_id             
                   cclk1_1_half      0       0        0        62500000    0          0     50000      Y                     deviceless                      no_connection_id          
                cclk0_1              1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id             
                   gige_sel          1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id          
                      gige           1       1        0        125000000   0          0     50000      Y                        3100c000.ethernet               stmmaceth              
                                                                                                                                deviceless                      no_connection_id       
                                                                                                                                                                                       
root@adsp-sc573-ezkit:~#                                                                                                                                                               
root@adsp-sc573-ezkit:~#                                                                                                                                                               
```

# POST

```
root@adsp-sc594-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                               
                                 enable  prepare  protect                                duty  hardware                            connection                                                    
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                                    
---------------------------------------------------------------------------------------------------------------------------------------------                                                    
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                                      
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                            
                                                                                                           deviceless                      no_connection_id                                      
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                            
                                                                                                           deviceless                      no_connection_id                                      
    cdu_clkinsel                     1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                   
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                                
          cgu1_vco                   1       1        0        1600000000  0          0     50000      Y            deviceless                      no_connection_id                             
             cgu1_pllclk             1       1        0        1600000000  0          0     50000      Y               deviceless                      no_connection_id                          
                cgu1_s1selexdiv      0       0        0        50000000    0          0     50000      Y                  deviceless                      no_connection_id                       
                cgu1_odiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                   oclk_1            0       0        0        100000000   0          0     50000      N                     deviceless                      no_connection_id                    
                      cdu_can        0       0        0        100000000   0          0     50000      N                        deviceless                      no_connection_id                 
                cgu1_ddiv            1       1        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                   dclk_1            1       1        0        800000000   0          0     50000      Y                     deviceless                      no_connection_id                    
                      cdu_ddr        1       1        0        800000000   0          0     50000      Y                        deviceless                      no_connection_id                 
                sysclk_1             0       0        0        400000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                   cgu1_s1seldiv     0       0        0        200000000   0          0     50000      Y                     deviceless                      no_connection_id                    
                      cgu1_sclk1sel  0       0        0        200000000   0          0     50000      Y                        deviceless                      no_connection_id                 
                         sclk1_1     0       0        0        200000000   0          0     50000      N                           deviceless                      no_connection_id              
                   cgu1_s0seldiv     0       0        0        100000000   0          0     50000      Y                                                                                         
         deviceless                      no_connection_id                                                                                                                                        
                      sclk0_1        0       0        0        100000000   0          0     50000      N                        deviceless                      no_connection_id                 
                cgu1_cdiv            0       0        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                   cclk1_1           0       0        0        800000000   0          0     50000      N                     deviceless                      no_connection_id                    
                   cclk0_1           0       0        0        800000000   0          0     50000      N                     deviceless                      no_connection_id                    
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                   
       cgu0_vco                      1       1        0        2000000000  0          0     50000      Y         deviceless                      no_connection_id                                
          cgu0_pllclk                2       2        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id                             
             cgu0_s1selexdiv         0       0        0        333333334   0          0     50000      Y               deviceless                      no_connection_id                          
                cgu0_sclk1sel        0       0        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id                       
                   sclk1_0           0       0        0        333333334   0          0     50000      N                     deviceless                      no_connection_id                    
                      cdu_spdif      0       0        0        333333334   0          0     50000      N                        deviceless                      no_connection_id                 
             cgu0_odiv               0       0        0        125000000   0          0     50000      Y               deviceless                      no_connection_id                          
                oclk_0               0       0        0        125000000   0          0     50000      N                  deviceless                      no_connection_id                       
                   cdu_lpddr         0       0        0        125000000   0          0     50000      N                     deviceless                      no_connection_id                    
             cgu0_ddiv               0       0        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                          
                dclk_0               0       0        0        1000000000  0          0     50000      N                  deviceless                      no_connection_id                       
             sysclk_0                1       1        0        500000000   0          0     50000      Y               deviceless                      no_connection_id                          
                cdu_ospi_refclk      0       0        0        500000000   0          0     50000      N                  deviceless                      no_connection_id                       
                cgu0_s1seldiv        0       0        0        250000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                cgu0_s0seldiv        1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id                       
                   sclk0_0           6       6        0        125000000   0          0     50000      Y                     31002400.i2s                    sclk                                
                                                                                                                             31008000.watchdog               sclk0                               
                                                                                                                                                                                                 
                                                                      31003000.uart                   sclk0                                                                                      
                                                                                                                             31001600.twi                    sclk0                               
                                                                                                                             gptimers@31018000               no_connection_id                    
                                                                                                                             deviceless                      no_connection_id                    
                      cdu_trace      0       0        0        125000000   0          0     50000      N                        deviceless                      no_connection_id                 
                      cdu_lp         0       0        0        125000000   0          0     50000      N                        deviceless                      no_connection_id                 
                      cdu_spi        1       1        0        125000000   0          0     50000      Y                        31030000.spi                    spi                              
                                                                                                                                deviceless                      no_connection_id                 
                      cdu_gige       1       1        0        125000000   0          0     50000      Y                        31040000.ethernet               stmmaceth                        
                                                                                                                                deviceless                      no_connection_id                 
             cgu0_cdiv               2       2        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                          
                cclk1_0              1       1        0        1000000000  0          0     50000      N                  deviceless                      no_connection_id                       
                   cdu_arm           1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                    
                cclk0_0              2       2        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id                       
                   cdu_sharc1        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                    
                   cdu_sharc0        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                    
                                                                                                                                                                                                 
root@adsp-sc594-som-ezkit:~#                                                                                                                                                                                                                                                                                                                         
```
```
root@adsp-sc598-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                                          
                                 enable  prepare  protect                                duty  hardware                            connection                                                               
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                                               
---------------------------------------------------------------------------------------------------------------------------------------------                                                               
 emac1_clkin                         0       0        0        50000000    0          0     50000      Y   deviceless                      no_connection_id                                                 
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                                                 
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                                       
                                                                                                           deviceless                      no_connection_id                                                 
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                                       
                                                                                                           deviceless                      no_connection_id                                                 
    cdu_clkinsel                     2       2        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                              
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                                           
          cgu1_vco                   2       2        0        3600000000  0          0     50000      Y            deviceless                      no_connection_id                                        
             cclk2_1                 1       1        0        1200000000  0          0     50000      Y               deviceless                      no_connection_id                                     
                cdu_arm              1       1        0        1200000000  0          0     50000      Y                  deviceless                      no_connection_id                                  
             cgu1_pllclk             1       1        0        1800000000  0          0     50000      Y               deviceless                      no_connection_id                                     
                cgu1_s1selexdiv      0       0        0        20000000    0          0     50000      Y                  deviceless                      no_connection_id                                  
                   cgu1_sclk1sel     0       0        0        20000000    0          0     50000      Y                     deviceless                      no_connection_id                               
                      sclk1_1        0       0        0        20000000    0          0     50000      N                        deviceless                      no_connection_id                            
                         sclk1_1_half 0       0        0        10000000    0          0     50000      Y                           deviceless                      no_connection_id                        
                            cdu_emmc_timer 0       0        0        10000000    0          0     50000      N                              deviceless                      no_connection_id                
                cgu1_s0selexdiv      1       1        0        50000000    0          0     50000      Y                  deviceless                      no_connection_id                                  
                   cgu1_sclk0sel     1       1        0        50000000    0          0     50000      Y                     deviceless                      no_connection_id                               
                      sclk0_1        1       1        0        50000000    0          0     50000      Y                        deviceless                      no_connection_id                            
                         cdu_emmc    1       1        0        50000000    0          0     50000      Y                           310c7000.mmc                    core                                     
                                                                                                                                   deviceless                      no_connection_id                         
                cgu1_odiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   oclk_1            0       0        0        112500000   0          0     50000      N                     deviceless                      no_connection_id                               
                      cdu_can        0       0        0        112500000   0          0     50000      N                        deviceless                      no_connection_id                            
                cgu1_ddiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   dclk_1            0       0        0        100000000   0          0     50000      N                     deviceless                      no_connection_id                               
                      dclk_1_half    0       0        0        50000000    0          0     50000      Y                        deviceless                      no_connection_id                            
                sysclk_1             0       0        0        225000000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   cgu1_s1seldiv     0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id                               
                   cgu1_s0seldiv     0       0        0        56250000    0          0     50000      Y                     deviceless                      no_connection_id                               
                cgu1_cdiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   cclk0_1           0       0        0        112500000   0          0     50000      N                     deviceless                      no_connection_id                               
       3pll_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                                           
          3pll_vco                   1       1        0        3200000000  0          0     50000      Y            deviceless                      no_connection_id                                        
             3pll_pllclk             1       1        0        1600000000  0          0     50000      Y               deviceless                      no_connection_id                                     
                3pll_ddiv            1       1        0        800000000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   ddr               1       1        0        800000000   0          0     50000      Y                     deviceless                      no_connection_id                               
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                              
       cgu0_vco                      1       1        0        4000000000  0          0     50000      Y         deviceless                      no_connection_id                                           
          cclk2_0                    0       0        0        1333333333  0          0     50000      Y            deviceless                      no_connection_id                                        
          cgu0_pllclk                3       3        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id                                        
             cgu0_s1selexdiv         1       1        0        333333334   0          0     50000      Y               deviceless                      no_connection_id                                     
                cgu0_sclk1sel        1       1        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   sclk1_0           1       1        0        333333334   0          0     50000      Y                     31002400.i2s                    sclk                                           
                                                                                                                             deviceless                      no_connection_id                               
                      cdu_spdif      0       0        0        333333334   0          0     50000      N                        deviceless                      no_connection_id                            
             cgu0_odiv               0       0        0        250000000   0          0     50000      Y               deviceless                      no_connection_id                                     
                oclk_0               0       0        0        250000000   0          0     50000      N                  deviceless                      no_connection_id                                  
                   cdu_lpddr         0       0        0        250000000   0          0     50000      N                     deviceless                      no_connection_id                               
             cgu0_ddiv               0       0        0        666666667   0          0     50000      Y               deviceless                      no_connection_id                                     
                dclk_0               0       0        0        666666667   0          0     50000      N                  deviceless                      no_connection_id                                  
                   cdu_ddr           0       0        0        666666667   0          0     50000      N                     deviceless                      no_connection_id                               
                   dclk_0_half       0       0        0        333333333   0          0     50000      Y                     deviceless                      no_connection_id                               
             sysclk_0                1       1        0        500000000   0          0     50000      Y               deviceless                      no_connection_id                                     
                cdu_ospi_refclk      0       0        0        500000000   0          0     50000      N                  deviceless                      no_connection_id                                  
                cgu0_s1seldiv        0       0        0        250000000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                cgu0_s0seldiv        1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id                                  
                   sclk0_0           6       6        0        125000000   0          0     50000      Y                     31008000.watchdog               sclk0                                          
                                                                                                                             31003000.uart                   sclk0                                          
                                                                                                                             31001600.twi                    sclk0                                          
                                                                                                                             31001400.twi                    sclk0                                          
                                                                                                                             gptimers@31018000               no_connection_id                               
                                                                                                                             deviceless                      no_connection_id                               
                      cdu_trace      0       0        0        125000000   0          0     50000      N                        deviceless                      no_connection_id                            
                      cdu_lp         0       0        0        125000000   0          0     50000      N                        deviceless                      no_connection_id                            
                      cdu_spi        1       1        0        125000000   0          0     50000      Y                        31030000.spi                    spi                                         
                                                                                                                                deviceless                      no_connection_id                            
                      cdu_gige       1       1        0        125000000   0          0     50000      Y                        31040000.ethernet               stmmaceth                                   
                                                                                                                                deviceless                      no_connection_id                            
             cgu0_cdiv               1       1        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                                     
                cclk0_0              2       2        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id                                  
                   cdu_sharc1        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                               
                   cdu_sharc0        1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                               
                                                                                                                                                                                                            
root@adsp-sc598-som-ezkit:~#                                                                                                                                                                 
```
reserved sel parents in original is wrong, mine fixes:
```
root@adsp-sc589-mini:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                     
                                 enable  prepare  protect                                duty  hardware                            connection                                     
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                     
---------------------------------------------------------------------------------------------------------------------------------------------                                     
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                       
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                             
                                                                                                           deviceless                      no_connection_id                       
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                             
                                                                                                           deviceless                      no_connection_id                       
    cdu_clkinsel                     1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                    
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                 
          cgu1_vco                   1       1        0        125000000   0          0     50000      Y            deviceless                      no_connection_id              
             cgu1_pllclk             1       1        0        125000000   0          0     50000      Y               deviceless                      no_connection_id           
                cgu1_odiv            0       0        0        41666667    0          0     50000      Y                  deviceless                      no_connection_id        
                   oclk_1            0       0        0        41666667    0          0     50000      N                     deviceless                      no_connection_id     
                cgu1_ddiv            0       0        0        62500000    0          0     50000      Y                  deviceless                      no_connection_id        
                   dclk_1            0       0        0        62500000    0          0     50000      N                     deviceless                      no_connection_id     
                sysclk_1             0       0        0        62500000    0          0     50000      Y                  deviceless                      no_connection_id        
                   cgu1_s1seldiv     0       0        0        31250000    0          0     50000      Y                     deviceless                      no_connection_id     
                      sclk1_1        0       0        0        31250000    0          0     50000      N                        deviceless                      no_connection_id  
                   cgu1_s0seldiv     0       0        0        31250000    0          0     50000      Y                     deviceless                      no_connection_id     
                      sclk0_1        0       0        0        31250000    0          0     50000      N                        deviceless                      no_connection_id  
                cgu1_cdiv            1       1        0        125000000   0          0     50000      Y                  deviceless                      no_connection_id        
                   cclk1_1           0       0        0        125000000   0          0     50000      N                     deviceless                      no_connection_id     
                      cclk1_1_half   0       0        0        62500000    0          0     50000      Y                        deviceless                      no_connection_id  
                   cclk0_1           1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id     
                      cdu_gige       1       1        0        125000000   0          0     50000      Y                        3100c000.ethernet               stmmaceth         
                                                                                                                                deviceless                      no_connection_id  
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                    
       cgu0_vco                      1       1        0        450000000   0          0     50000      Y         deviceless                      no_connection_id                 
          cgu0_pllclk                4       4        0        450000000   0          0     50000      Y            deviceless                      no_connection_id              
             cgu0_odiv               1       1        0        150000000   0          0     50000      Y               deviceless                      no_connection_id           
                oclk_0               1       1        0        150000000   0          0     50000      Y                  deviceless                      no_connection_id        
                   cdu_reserved      0       0        0        150000000   0          0     50000      N                     deviceless                      no_connection_id     
                   cdu_spdif         0       0        0        150000000   0          0     50000      N                     deviceless                      no_connection_id     
                   cdu_can           0       0        0        150000000   0          0     50000      N                     deviceless                      no_connection_id     
                   oclk_0_half       1       1        0        75000000    0          0     50000      Y                     deviceless                      no_connection_id     
                      cdu_sdio       1       1        0        75000000    0          0     50000      Y                        31010000.mmc                    ciu               
                                                                                                                                deviceless                      no_connection_id  
             cgu0_ddiv               1       1        0        450000000   0          0     50000      Y               deviceless                      no_connection_id           
                dclk_0               1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id        
                   cdu_ddr           1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id     
             sysclk_0                2       2        0        225000000   0          0     50000      Y               deviceless                      no_connection_id           
                cgu0_s1seldiv        1       1        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id        
                   sclk1_0           2       2        0        112500000   0          0     50000      Y                     31002000.i2s-sport0             sclk                 
                                                                                                                             31042000.spi                    spi                  
                                                                                                                             deviceless                      no_connection_id     
                cgu0_s0seldiv        1       1        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id        
                   sclk0_0           7       7        0        112500000   0          0     50000      Y                     31010000.mmc                    biu                  
                                                                                                                             31008000.watchdog               sclk0                
                                                                                                                             31044000.spi                    spi                  
                                                                                                                             31003000.uart                   sclk0                
                                                                                                                             31001600.twi                    sclk0                
                                                                                                                             31001500.twi                    sclk0                
                                                                                                                             31001400.twi                    sclk0                
                                                                                                                             gptimers@31001000               no_connection_id     
                                                                                                                             deviceless                      no_connection_id     
                      cdu_lp         0       0        0        112500000   0          0     50000      N                        deviceless                      no_connection_id  
             cgu0_cdiv               2       2        0        450000000   0          0     50000      Y               deviceless                      no_connection_id           
                cclk1_0              1       1        0        450000000   0          0     50000      N                  deviceless                      no_connection_id        
                   cdu_arm           1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id     
                cclk0_0              2       2        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id        
                   cdu_sharc1        1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id     
                   cdu_sharc0        1       1        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id     
root@adsp-sc589-mini:~#                                                                                                                                                           
```
```
root@adsp-sc573-ezkit:~# cat /sys/kernel/debug/clk/clk_summary                                                                                                                            
                                 enable  prepare  protect                                duty  hardware                            connection                                             
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                             
---------------------------------------------------------------------------------------------------------------------------------------------                                             
 dummy                               0       0        0        0           0          0     50000      Y   deviceless                      no_connection_id                               
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin1                                     
                                                                                                           deviceless                      no_connection_id                               
 sys_clkin0                          2       2        0        25000000    0          0     50000      Y   clocks@3108d000                 sys_clkin0                                     
                                                                                                           deviceless                      no_connection_id                               
    cdu_clkinsel                     1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu1_df                       1       1        0        25000000    0          0     50000      Y         deviceless                      no_connection_id                         
          cgu1_pllclk                1       1        0        125000000   0          0     50000      Y            deviceless                      no_connection_id                      
             cgu1_odiv               0       0        0        41666667    0          0     50000      Y               deviceless                      no_connection_id                   
                oclk_1               0       0        0        41666667    0          0     50000      N                  deviceless                      no_connection_id                
             cgu1_ddiv               0       0        0        62500000    0          0     50000      Y               deviceless                      no_connection_id                   
                dclk_1               0       0        0        62500000    0          0     50000      N                  deviceless                      no_connection_id                
             sysclk_1                0       0        0        62500000    0          0     50000      Y               deviceless                      no_connection_id                   
                cgu1_s1seldiv        0       0        0        31250000    0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk1_1           0       0        0        31250000    0          0     50000      N                     deviceless                      no_connection_id             
                cgu1_s0seldiv        0       0        0        31250000    0          0     50000      Y                  deviceless                      no_connection_id                
                   sclk0_1           0       0        0        31250000    0          0     50000      N                     deviceless                      no_connection_id             
             cgu1_cdiv               1       1        0        125000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cclk1_1              0       0        0        125000000   0          0     50000      N                  deviceless                      no_connection_id                
                   cclk1_1_half      0       0        0        62500000    0          0     50000      Y                     deviceless                      no_connection_id             
                cclk0_1              1       1        0        125000000   0          0     50000      Y                  deviceless                                                      
  no_connection_id                                                                                                                                                                        
                   cdu_gige          1       1        0        125000000   0          0     50000      Y                     3100c000.ethernet               stmmaceth                    
                                                                                                                             deviceless                      no_connection_id             
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                            
       cgu0_pllclk                   4       4        0        450000000   0          0     50000      Y         deviceless                      no_connection_id                         
          cgu0_odiv                  1       1        0        150000000   0          0     50000      Y            deviceless                      no_connection_id                      
             oclk_0                  1       1        0        150000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cdu_spdif            0       0        0        150000000   0          0     50000      N                  deviceless                      no_connection_id                
                cdu_can              0       0        0        150000000   0          0     50000      N                  deviceless                      no_connection_id                
                oclk_0_half          1       1        0        75000000    0          0     50000      Y                  deviceless                      no_connection_id                
                   cdu_sdio          1       1        0        75000000    0          0     50000      Y                     31010000.mmc                    ciu                          
                                                                                                                             deviceless                      no_connection_id             
          cgu0_ddiv                  1       1        0        225000000   0          0     50000      Y            deviceless                      no_connection_id                      
             dclk_0                  1       1        0        225000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cdu_ddr              1       1        0        225000000   0          0     50000      Y                  deviceless                      no_connection_id                
          sysclk_0                   2       2        0        225000000   0          0     50000      Y            deviceless                      no_connection_id                      
             cgu0_s1seldiv           1       1        0        112500000   0          0     50000      Y               deviceless                      no_connection_id                   
                sclk1_0              2       2        0        112500000   0          0     50000      Y                  31044000.spi                    spi                             
                                                                                                                          3102e000.spi                    spi                             
                                                                                                                          deviceless                      no_connection_id                
             cgu0_s0seldiv           1       1        0        112500000   0          0     50000      Y               deviceless                      no_connection_id                   
                sclk0_0              7       7        0        112500000   0          0     50000      Y                  31002000.i2s                    sclk                            
                                                                                                                          31010000.mmc                    biu                             
                                                                                                                          31                                                              
008000.watchdog               sclk0                                                                                                                                                       
                                                                                                                          31003000.uart                   sclk0                           
                                                                                                                          31001600.twi                    sclk0                           
                                                                                                                          31001500.twi                    sclk0                           
                                                                                                                          31001400.twi                    sclk0                           
                                                                                                                          gptimers@31018000               no_connection_id                
                                                                                                                          deviceless                      no_connection_id                
          cgu0_cdiv                  2       2        0        450000000   0          0     50000      Y            deviceless                      no_connection_id                      
             cclk1_0                 1       1        0        450000000   0          0     50000      N               deviceless                      no_connection_id                   
                cdu_arm              1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                
             cclk0_0                 2       2        0        450000000   0          0     50000      Y               deviceless                      no_connection_id                   
                cdu_sharc1           1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                
                cdu_sharc0           1       1        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                
                                                                                                                                                                                          
```


# Uboot

U-Boot clock tree after changes:
```
 Rate               Usecnt      Name
------------------------------------------
 0                    0        |-- dummy
 0                    0        |   |-- arm0_sel
 0                    0        |   |   `-- arm0
 0                    0        |   `-- arm1_sel
 0                    0        |       `-- arm1
 25000000             0        |-- sys_clkin0
 25000000             1        |   |-- cgu0_df
 4000000000           1        |   |   `-- cgu0_vco
 2000000000           1        |   |       |-- cgu0_pllclk
 1000000000           1        |   |       |   `-- cgu0_pllclk_half
 1000000000           0        |   |       |       |-- cgu0_cdiv
 1000000000           0        |   |       |       |   `-- cclk0_0
 1000000000           0        |   |       |       |       `-- sharc_sel
 1000000000           0        |   |       |       |           `-- sharc
 500000000            1        |   |       |       |-- sysclk_0
 125000000            1        |   |       |       |   |-- cgu0_s0seldiv
 125000000            1        |   |       |       |   |   `-- sclk0_0
 125000000            0        |   |       |       |   |       |-- spi_sel
 125000000            0        |   |       |       |   |       |   `-- spi
 125000000            0        |   |       |       |   |       |-- gige_sel
 125000000            0        |   |       |       |   |       |   `-- gige
 125000000            0        |   |       |       |   |       |-- xspi_sel
 125000000            0        |   |       |       |   |       |   `-- xspi
 125000000            0        |   |       |       |   |       |-- trace_sel
 125000000            0        |   |       |       |   |       |   `-- trace
 125000000            0        |   |       |       |   |       `-- mshc_sel
 125000000            0        |   |       |       |   |           `-- mshc
 250000000            0        |   |       |       |   |-- cgu0_s1seldiv
 500000000            0        |   |       |       |   `-- pwm_sel
 500000000            0        |   |       |       |       `-- pwm
 500000000            0        |   |       |       |-- cgu0_ddiv
 500000000            0        |   |       |       |   `-- dclk_0
 500000000            0        |   |       |       |       `-- cdu_ddr_sel
 500000000            0        |   |       |       |           `-- cdu_ddr
 100000000            0        |   |       |       |-- cgu0_odiv
 100000000            0        |   |       |       |   `-- oclk_0
 100000000            0        |   |       |       |       `-- can_sel
 100000000            0        |   |       |       |           `-- can
 333333334            0        |   |       |       `-- cgu0_s1selexdiv
 333333334            0        |   |       |           `-- cgu0_sclk1sel
 333333334            0        |   |       |               `-- sclk1_0
 333333334            0        |   |       |                   `-- spdif_sel
 333333334            0        |   |       |                       `-- spdif
 1333333333           0        |   |       |-- cclk2_0
 800000000            0        |   |       `-- dclk1_0
 25000000             0        |   `-- cgu1_df
 3600000000           0        |       `-- cgu1_vco
 1800000000           0        |           |-- cgu1_pllclk
 900000000            0        |           |   `-- cgu1_pllclk_half
 450000000            0        |           |       |-- cgu1_cdiv
 450000000            0        |           |       |   `-- cclk0_1
 180000000            0        |           |       |-- sysclk_1
 45000000             0        |           |       |   |-- cgu1_s0seldiv
 90000000             0        |           |       |   `-- cgu1_s1seldiv
 300000000            0        |           |       |-- cgu1_ddiv
 300000000            0        |           |       |   `-- dclk_1
 300000000            0        |           |       |       `-- lp_sel
 300000000            0        |           |       |           `-- lp
 112500000            0        |           |       |-- cgu1_odiv
 112500000            0        |           |       |   `-- oclk_1
 112500000            0        |           |       |-- cgu1_s0selexdiv
 112500000            0        |           |       |   `-- cgu1_sclk0sel
 112500000            0        |           |       |       `-- sclk0_1
 180000000            0        |           |       `-- cgu1_s1selexdiv
 180000000            0        |           |           `-- cgu1_sclk1sel
 180000000            0        |           |               `-- sclk1_1
 180000000            0        |           |                   `-- xspi2_sel
 180000000            0        |           |                       `-- xspi2
 1200000000           0        |           |-- cclk2_1
 720000000            0        |           `-- dclk1_1
 25000000             0        |-- sys_clkin1
```


