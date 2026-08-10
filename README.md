```
[    7.797804] adi-dwmac 31040000.ethernet: IRQ sfty not found
[    7.803553] OF: /scb/ethernet@31040000: Read of boolean property 'snps,tso' with a value.
[    7.811828] adi-dwmac 31040000.ethernet: PTP uses main clock
[    7.818018] adi-dwmac 31040000.ethernet: User ID: 0x10, Synopsys ID: 0x53
[    7.824750] adi-dwmac 31040000.ethernet:     DWMAC4/5
[    7.829509] adi-dwmac 31040000.ethernet: DMA HW capability register supported
[    7.836620] adi-dwmac 31040000.ethernet: RX Checksum Offload Engine supported
[    7.843735] adi-dwmac 31040000.ethernet: TX Checksum insertion supported
[    7.850418] adi-dwmac 31040000.ethernet: Wake-Up On Lan supported
[    7.856503] adi-dwmac 31040000.ethernet: TSO supported
[    7.861617] adi-dwmac 31040000.ethernet: Enable RX Mitigation via HW Watchdog Timer
[    7.869270] adi-dwmac 31040000.ethernet: Enabled L3L4 Flow TC (entries=8)
[    7.876048] adi-dwmac 31040000.ethernet: Enabled RFS Flow TC (entries=10)
[    7.882798] adi-dwmac 31040000.ethernet: TSO feature enabled
[    7.888436] adi-dwmac 31040000.ethernet: SPH feature enabled
[    7.894080] adi-dwmac 31040000.ethernet: Using 32/32 bits DMA host/device width
[    7.928048] usbcore: registered new interface driver usb-storage
[    7.937950] i2c_dev: i2c /dev entries driver
[    7.944414] adi_wdt: initialized: timeout=30 sec (nowayout=0)
[    7.952727] sdhci: Secure Digital Host Controller Interface driver
[    7.958927] sdhci: Copyright(c) Pierre Ossman
[    7.963273] Synopsys Designware Multimedia Card Interface Driver
[    7.969572] sdhci-pltfm: SDHCI platform and OF driver helper
[    7.978188] hw perfevents: enabled with armv8_pmuv3 PMU driver, 7 (0,8000003f) counters available
[    7.989525] NET: Registered PF_PACKET protocol family
[    7.994740] 8021q: 802.1Q VLAN Support v1.8
[    7.999128] Key type dns_resolver registered
[    8.044037] registered taskstats version 1
[    8.048384] Loading compiled-in X.509 certificates
[    8.124566] adi-dwmac 31040000.ethernet eth0: Register MEM_TYPE_PAGE_POOL RxQ-0
[    8.141902] adi-dwmac 31040000.ethernet eth0: PHY [stmmac-0:00] driver [Generic PHY] (irq=POLL)
[    8.151930] adi-dwmac 31040000.ethernet eth0: No Safety Features support found
[    8.161019] adi-dwmac 31040000.ethernet eth0: IEEE 1588-2008 Advanced Timestamp supported
[    8.169209] adi-dwmac 31040000.ethernet eth0: configuring for phy/rgmii-id link mode
[    8.183994] 8021q: adding VLAN 0 to HW filter on device eth0
[   12.264083] adi-dwmac 31040000.ethernet eth0: Link is Up - 1Gbps/Full - flow control off
[   12.287118] IP-Config: Complete:
[   12.290203]      device=eth0, hwaddr=02:80:ad:20:31:e8, ipaddr=10.42.0.2, mask=255.255.255.0, gw=255.255.255.255
[   12.300500]      host=sc846, domain=, nis-domain=(none)
[   12.305634]      bootserver=10.42.0.1, rootserver=10.42.0.1, rootpath=
[   12.306720] clk: Not disabling unused clocks
[   12.322406] Freeing unused kernel memory: 2816K
[   12.327386] Run /init as init process
[   12.545587]  
[   12.545587]          Analog Initial Ram Filesystem
[   12.545587]                 www.analog.com
[   12.545587]               www.yoctoproject.org
[   12.545587] 
[   12.545587] Analog [Initramfs]: Preparing Operating System....
[   12.545587] Analog [Initramfs]: Mounting Root File System...
[   12.671914] Analog [Initramfs]: Switching RFS to NFS mount (tcp,nfsvers=3,10.42.0.1:/romfs)...

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


