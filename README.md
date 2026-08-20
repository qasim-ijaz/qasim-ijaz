```
[    7.921183] NET: Registered PF_PACKET protocol family                                                                                       
[    7.926409] 8021q: 802.1Q VLAN Support v1.8                                                                                                 
[    7.930721] Key type dns_resolver registered                                                                                                
[    7.975219] registered taskstats version 1                                                                                                  
[    7.979466] Loading compiled-in X.509 certificates                                                                                          
[    8.055768] adi-dwmac 31040000.ethernet eth0: Register MEM_TYPE_PAGE_POOL RxQ-0                                                             
[    8.071150] adi-dwmac 31040000.ethernet eth0: PHY [stmmac-0:00] driver [Generic PHY] (irq=POLL)                                             
[    8.081101] adi-dwmac 31040000.ethernet eth0: No Safety Features support found                                                              
[    8.090180] adi-dwmac 31040000.ethernet eth0: IEEE 1588-2008 Advanced Timestamp supported                                                   
[    8.098370] adi-dwmac 31040000.ethernet eth0: configuring for phy/rgmii-id link mode                                                        
[    8.112503] 8021q: adding VLAN 0 to HW filter on device eth0                                                                                
[   12.199690] adi-dwmac 31040000.ethernet eth0: Link is Up - 1Gbps/Full - flow control off                                                    
[   12.222732] IP-Config: Guessing netmask 255.0.0.0                                                                                           
[   12.227352] IP-Config: Complete:                                                                                                            
[   12.230514]      device=eth0, hwaddr=02:80:ad:20:31:e8, ipaddr=10.42.0.2, mask=255.0.0.0, gw=255.255.255.255                                
[   12.240444]      host=sc846, domain=, nis-domain=(none)                                                                                     
[   12.245592]      bootserver=10.42.0.1, rootserver=10.42.0.1, rootpath=                                                                      
[   12.246342] clk: Disabling unused clocks                                                                                                                                                                                                   
[   12.412817] Freeing unused kernel memory: 2816K                                                                                             
[   12.417691] Run /init as init process                                                                                                       
[   12.636122]                                                                                                                                 
[   12.636122]          Analog Initial Ram Filesystem                                                                                          
[   12.636122]                 www.analog.com                                                                                                  
[   12.636122]               www.yoctoproject.org                                                                                              
[   12.636122]                                                                                                                                 
[   12.636122] Analog [Initramfs]: Preparing Operating System....                                                                              
[   12.636122] Analog [Initramfs]: Mounting Root File System...                                                                                
[   12.761609] Analog [Initramfs]: Switching RFS to NFS mount (tcp,nfsvers=3,10.42.0.1:/romfs)...                                              
                                                                                                                   
```


# Before
```
                                 enable  prepare  protect                                duty  hardware                            connection                                                          
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id                                                          
---------------------------------------------------------------------------------------------------------------------------------------------                                                          
 dummy                               2       2        0        0           0          0     50000      Y   deviceless                      no_connection_id                                            
    arm1_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id                                         
       arm1                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id                                      
    arm0_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id                                         
       arm0                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id                                      
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   deviceless                      no_connection_id                                            
 sys_clkin0                          1       1        0        25000000    0          0     50000      Y   clock-controller@3108d000       sys_clkin0                                                  
                                                                                                           deviceless                      no_connection_id                                            
    cgu1_df                          0       0        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                         
       cgu1_vco                      0       0        0        3600000000  0          0     50000      Y         deviceless                      no_connection_id                                      
          cgu1_pllclk                0       0        0        1800000000  0          0     50000      Y            deviceless                      no_connection_id                                   
             cgu1_pllclk_half        0       0        0        900000000   0          0     50000      Y               deviceless                      no_connection_id                                
                dclk1_1              0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                cclk2_1              0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                cgu1_s1selexdiv      0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   cgu1_sclk1sel     0       0        0        180000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      sclk1_1        0       0        0        180000000   0          0     50000      Y                        deviceless                      no_connection_id                       
                         xspi1_sel   0       0        0        180000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            xspi1    0       0        0        180000000   0          0     50000      Y                              deviceless                      no_connection_id                 
                cgu1_s0selexdiv      0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   cgu1_sclk0sel     0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      sclk0_1        0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id                       
                cgu1_odiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   oclk_1            0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id                          
                cgu1_ddiv            0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   dclk_1            0       0        0        300000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      lp_sel         0       0        0        300000000   0          0     50000      Y                        deviceless                      no_connection_id                       
                         lp          0       0        0        300000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                sysclk_1             0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   cgu1_s1seldiv     0       0        0        90000000    0          0     50000      Y                     deviceless                      no_connection_id                          
                   cgu1_s0seldiv     0       0        0        45000000    0          0     50000      Y                     deviceless                      no_connection_id                          
                cgu1_cdiv            0       0        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   cclk0_1           0       0        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id                          
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id                                         
       cgu0_vco                      1       1        0        4000000000  0          0     50000      Y         deviceless                      no_connection_id                                      
          cgu0_pllclk                1       1        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id                                   
             cgu0_pllclk_half        2       2        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id                                
                dclk1_0              0       0        0        200000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                cclk2_0              0       0        0        333333333   0          0     50000      Y                  deviceless                      no_connection_id                             
                cgu0_s1selexdiv      0       0        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id                             
                   cgu0_sclk1sel     0       0        0        333333334   0          0     50000      Y                     deviceless                      no_connection_id                          
                      sclk1_0        0       0        0        333333334   0          0     50000      Y                        deviceless                      no_connection_id                       
                         spdif_sel   0       0        0        333333334   0          0     50000      Y                           deviceless                      no_connection_id                    
                            spdif    0       0        0        333333334   0          0     50000      Y                              deviceless                      no_connection_id                 
                cgu0_odiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   oclk_0            0       0        0        100000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      can_sel        0       0        0        100000000   0          0     50000      Y                        deviceless                      no_connection_id                       
                         can         0       0        0        100000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                cgu0_ddiv            0       0        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   dclk_0            0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      ddr_sel        0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id                       
                         cdu_ddr     0       0        0        500000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                sysclk_0             1       1        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id                             
                   pwm_sel           0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      pwm            0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id                       
                   cgu0_s1seldiv     0       0        0        250000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                   cgu0_s0seldiv     1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id                          
                      sclk0_0        5       5        0        125000000   0          0     50000      Y                        31008000.watchdog               sclk0                                  
                                                                                                                                31003000.serial                 sclk0                                  
                                                                                                                                31001200.i2c                    sclk0                                  
                                                                                                                                31001600.i2c                    sclk0                                  
                                                                                                                                deviceless                      no_connection_id                       
                         mshc_sel    0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            mshc     0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id                 
                         trace_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            trace    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id                 
                         xspi0_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            xspi0    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id                 
                         gige_sel    1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            gige     1       1        0        125000000   0          0     50000      Y                              31040000.ethernet               stmmaceth                        
                                                                                                                                      deviceless                      no_connection_id                 
                         spi_sel     1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id                    
                            spi      1       1        0        125000000   0          0     50000      Y                              3102f000.spi                    spi                              
                                                                                                                                      deviceless                      no_connection_id                 
                cgu0_cdiv            1       1        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id                             
                   cclk0_0           1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id                          
                      sharc0_sel     1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id                       
                         sharc0      1       1        0        1000000000  0          0     50000      Y                           deviceless                      no_connection_id                    
```
# After:
```
```


```
---
 drivers/usb/musb-new/musb_uboot.c | 5 +++++
 1 file changed, 5 insertions(+)

diff --git a/drivers/usb/musb-new/musb_uboot.c b/drivers/usb/musb-new/musb_uboot.c
--- a/drivers/usb/musb-new/musb_uboot.c
+++ b/drivers/usb/musb-new/musb_uboot.c
@@ -238,6 +238,11 @@ int musb_lowlevel_init(struct musb_host_data *host)
 		return -ENODEV;
 	}
 
+	/*
+	 * Allow the USB device/PHY to settle before the initial root-port reset.
+	 */
+	mdelay(500);
 	_musb_reset_root_port(host, NULL);
 	host->host->is_active = 1;
 	host->hcd.hcd_priv = host->host;
-- 
2.43.0
```

Pre clock changes Uboot
```
=> clk dump
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
 1000000000           1        |   |       |-- cgu0_pllclk
 1000000000           0        |   |       |   |-- cgu0_cdiv
 1000000000           0        |   |       |   |   `-- cclk0_0
 1000000000           0        |   |       |   |       `-- sharc_sel
 1000000000           0        |   |       |   |           `-- sharc
 500000000            1        |   |       |   |-- sysclk_0
 125000000            1        |   |       |   |   |-- cgu0_s0seldiv
 125000000            1        |   |       |   |   |   `-- sclk0_0
 125000000            0        |   |       |   |   |       |-- spi_sel
 125000000            0        |   |       |   |   |       |   `-- spi
 125000000            0        |   |       |   |   |       |-- gige_sel
 125000000            0        |   |       |   |   |       |   `-- gige
 125000000            0        |   |       |   |   |       |-- xspi_sel
 125000000            0        |   |       |   |   |       |   `-- xspi
 125000000            0        |   |       |   |   |       |-- trace_sel
 125000000            0        |   |       |   |   |       |   `-- trace
 125000000            0        |   |       |   |   |       `-- mshc_sel
 125000000            0        |   |       |   |   |           `-- mshc
 250000000            0        |   |       |   |   |-- cgu0_s1seldiv
 500000000            0        |   |       |   |   `-- pwm_sel
 500000000            0        |   |       |   |       `-- pwm
 500000000            0        |   |       |   |-- cgu0_ddiv
 500000000            0        |   |       |   |   `-- dclk_0
 500000000            0        |   |       |   |       `-- cdu_ddr_sel
 500000000            0        |   |       |   |           `-- cdu_ddr
 100000000            0        |   |       |   |-- cgu0_odiv
 100000000            0        |   |       |   |   `-- oclk_0
 100000000            0        |   |       |   |       `-- can_sel
 100000000            0        |   |       |   |           `-- can
 333333334            0        |   |       |   `-- cgu0_s1selexdiv
 333333334            0        |   |       |       `-- cgu0_sclk1sel
 333333334            0        |   |       |           `-- sclk1_0
 333333334            0        |   |       |               `-- spdif_sel
 333333334            0        |   |       |                   `-- spdif
 1333333333           0        |   |       |-- cclk2_0
 1333333333           0        |   |       |-- cclk2_1
 800000000            0        |   |       `-- dclk1_0
 25000000             0        |   `-- cgu1_df
 3600000000           0        |       `-- cgu1_vco
 900000000            0        |           |-- cgu1_pllclk
 450000000            0        |           |   |-- cgu1_cdiv
 450000000            0        |           |   |   `-- cclk0_1
 180000000            0        |           |   |-- sysclk_1
 45000000             0        |           |   |   |-- cgu1_s0seldiv
 90000000             0        |           |   |   `-- cgu1_s1seldiv
 300000000            0        |           |   |-- cgu1_ddiv
 300000000            0        |           |   |   `-- dclk_1
 300000000            0        |           |   |       `-- lp_sel
 300000000            0        |           |   |           `-- lp
 112500000            0        |           |   |-- cgu1_odiv
 112500000            0        |           |   |   `-- oclk_1
 112500000            0        |           |   |-- cgu1_s0selexdiv
 112500000            0        |           |   |   `-- cgu1_sclk0sel
 112500000            0        |           |   |       `-- sclk0_1
 180000000            0        |           |   `-- cgu1_s1selexdiv
 180000000            0        |           |       `-- cgu1_sclk1sel
 180000000            0        |           |           `-- sclk1_1
 180000000            0        |           |               `-- xspi2_sel
 180000000            0        |           |                   `-- xspi2
 1200000000           0        |           `-- cclk2_1
 25000000             0        |-- sys_clkin1
```
Pre clock changes Linux:
```
root@adsp-sc846-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary 
                                 enable  prepare  protect                                duty  hardware                            connection
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id
---------------------------------------------------------------------------------------------------------------------------------------------
 dummy                               2       2        0        0           0          0     50000      Y   deviceless                      no_connection_id         
    arm1_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id         
       arm1                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id         
    arm0_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id         
       arm0                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id         
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   deviceless                      no_connection_id         
 sys_clkin0                          1       1        0        25000000    0          0     50000      Y   clock-controller@3108d000       sys_clkin0               
                                                                                                           deviceless                      no_connection_id         
    cgu1_df                          0       0        0        25000000    0          0     50000      Y      deviceless                      no_connection_id         
       cgu1_vco                      0       0        0        3600000000  0          0     50000      Y         deviceless                      no_connection_id         
          cgu1_pllclk                0       0        0        1800000000  0          0     50000      Y            deviceless                      no_connection_id         
             cgu1_pllclk_half        0       0        0        900000000   0          0     50000      Y               deviceless                      no_connection_id         
                dclk1_1              0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cclk2_1              0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cgu1_s1selexdiv      0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_sclk1sel     0       0        0        180000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk1_1        0       0        0        180000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         xspi1_sel   0       0        0        180000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            xspi1    0       0        0        180000000   0          0     50000      Y                              deviceless                      no_connection_id         
                cgu1_s0selexdiv      0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_sclk0sel     0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk0_1        0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id         
                cgu1_odiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id         
                   oclk_1            0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id         
                cgu1_ddiv            0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   dclk_1            0       0        0        300000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      lp_sel         0       0        0        300000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         lp          0       0        0        300000000   0          0     50000      Y                           deviceless                      no_connection_id         
                sysclk_1             0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_s1seldiv     0       0        0        90000000    0          0     50000      Y                     deviceless                      no_connection_id         
                   cgu1_s0seldiv     0       0        0        45000000    0          0     50000      Y                     deviceless                      no_connection_id         
                cgu1_cdiv            0       0        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cclk0_1           0       0        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id         
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id         
       cgu0_vco                      1       1        0        4000000000  0          0     50000      Y         deviceless                      no_connection_id         
          cgu0_pllclk                1       1        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id         
             cgu0_pllclk_half        2       2        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id         
                dclk1_0              0       0        0        200000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cclk2_0              0       0        0        333333333   0          0     50000      Y                  deviceless                      no_connection_id         
                cgu0_s1selexdiv      0       0        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu0_sclk1sel     0       0        0        333333334   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk1_0        0       0        0        333333334   0          0     50000      Y                        deviceless                      no_connection_id         
                         spdif_sel   0       0        0        333333334   0          0     50000      Y                           deviceless                      no_connection_id         
                            spdif    0       0        0        333333334   0          0     50000      Y                              deviceless                      no_connection_id         
                cgu0_odiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   oclk_0            0       0        0        100000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      can_sel        0       0        0        100000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         can         0       0        0        100000000   0          0     50000      Y                           deviceless                      no_connection_id         
                cgu0_ddiv            0       0        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   dclk_0            0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      ddr_sel        0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         cdu_ddr     0       0        0        500000000   0          0     50000      Y                           deviceless                      no_connection_id         
                sysclk_0             1       1        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   pwm_sel           0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      pwm            0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id         
                   cgu0_s1seldiv     0       0        0        250000000   0          0     50000      Y                     deviceless                      no_connection_id         
                   cgu0_s0seldiv     1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk0_0        5       5        0        125000000   0          0     50000      Y                        31008000.watchdog               sclk0                    
                                                                                                                                31003000.serial                 sclk0                    
                                                                                                                                31001200.i2c                    sclk0                    
                                                                                                                                31001600.i2c                    sclk0                    
                                                                                                                                deviceless                      no_connection_id         
                         mshc_sel    0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            mshc     0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         trace_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            trace    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         xspi0_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            xspi0    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         gige_sel    1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            gige     1       1        0        125000000   0          0     50000      Y                              31040000.ethernet               stmmaceth                
                                                                                                                                      deviceless                      no_connection_id         
                         spi_sel     1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            spi      1       1        0        125000000   0          0     50000      Y                              3102f000.spi                    spi                      
                                                                                                                                      deviceless                      no_connection_id         
                cgu0_cdiv            1       1        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id         
                   cclk0_0           1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id         
                      sharc0_sel     1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id         
                         sharc0      1       1        0        1000000000  0          0     50000      Y                           deviceless                      no_connection_id       
```

Post clock changes Uboot
```
=> clk dump
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
Post clock changes linux
```
root@adsp-sc846-som-ezkit:~# cat /sys/kernel/debug/clk/clk_summary 
                                 enable  prepare  protect                                duty  hardware                            connection
   clock                          count    count    count        rate   accuracy phase  cycle    enable   consumer                         id
---------------------------------------------------------------------------------------------------------------------------------------------
 dummy                               2       2        0        0           0          0     50000      Y   deviceless                      no_connection_id         
    arm1_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id         
       arm1                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id         
    arm0_sel                         1       1        0        0           0          0     50000      Y      deviceless                      no_connection_id         
       arm0                          1       1        0        0           0          0     50000      Y         deviceless                      no_connection_id         
 sys_clkin1                          0       0        0        25000000    0          0     50000      Y   deviceless                      no_connection_id         
 sys_clkin0                          1       1        0        25000000    0          0     50000      Y   clock-controller@3108d000       sys_clkin0               
                                                                                                           deviceless                      no_connection_id         
    cgu1_df                          0       0        0        25000000    0          0     50000      Y      deviceless                      no_connection_id         
       cgu1_vco                      0       0        0        3600000000  0          0     50000      Y         deviceless                      no_connection_id         
          cgu1_pllclk                0       0        0        1800000000  0          0     50000      Y            deviceless                      no_connection_id         
             cgu1_pllclk_half        0       0        0        900000000   0          0     50000      Y               deviceless                      no_connection_id         
                dclk1_1              0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cclk2_1              0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cgu1_s1selexdiv      0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_sclk1sel     0       0        0        180000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk1_1        0       0        0        180000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         xspi1_sel   0       0        0        180000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            xspi1    0       0        0        180000000   0          0     50000      Y                              deviceless                      no_connection_id         
                cgu1_s0selexdiv      0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_sclk0sel     0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk0_1        0       0        0        112500000   0          0     50000      Y                        deviceless                      no_connection_id         
                cgu1_odiv            0       0        0        112500000   0          0     50000      Y                  deviceless                      no_connection_id         
                   oclk_1            0       0        0        112500000   0          0     50000      Y                     deviceless                      no_connection_id         
                cgu1_ddiv            0       0        0        300000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   dclk_1            0       0        0        300000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      lp_sel         0       0        0        300000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         lp          0       0        0        300000000   0          0     50000      Y                           deviceless                      no_connection_id         
                sysclk_1             0       0        0        180000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu1_s1seldiv     0       0        0        90000000    0          0     50000      Y                     deviceless                      no_connection_id         
                   cgu1_s0seldiv     0       0        0        45000000    0          0     50000      Y                     deviceless                      no_connection_id         
                cgu1_cdiv            0       0        0        450000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   cclk0_1           0       0        0        450000000   0          0     50000      Y                     deviceless                      no_connection_id         
    cgu0_df                          1       1        0        25000000    0          0     50000      Y      deviceless                      no_connection_id         
       cgu0_vco                      1       1        0        4000000000  0          0     50000      Y         deviceless                      no_connection_id         
          cgu0_pllclk                1       1        0        2000000000  0          0     50000      Y            deviceless                      no_connection_id         
             cgu0_pllclk_half        2       2        0        1000000000  0          0     50000      Y               deviceless                      no_connection_id         
                dclk1_0              0       0        0        200000000   0          0     50000      Y                  deviceless                      no_connection_id         
                cclk2_0              0       0        0        333333333   0          0     50000      Y                  deviceless                      no_connection_id         
                cgu0_s1selexdiv      0       0        0        333333334   0          0     50000      Y                  deviceless                      no_connection_id         
                   cgu0_sclk1sel     0       0        0        333333334   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk1_0        0       0        0        333333334   0          0     50000      Y                        deviceless                      no_connection_id         
                         spdif_sel   0       0        0        333333334   0          0     50000      Y                           deviceless                      no_connection_id         
                            spdif    0       0        0        333333334   0          0     50000      Y                              deviceless                      no_connection_id         
                cgu0_odiv            0       0        0        100000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   oclk_0            0       0        0        100000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      can_sel        0       0        0        100000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         can         0       0        0        100000000   0          0     50000      Y                           deviceless                      no_connection_id         
                cgu0_ddiv            0       0        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   dclk_0            0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      ddr_sel        0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id         
                         cdu_ddr     0       0        0        500000000   0          0     50000      Y                           deviceless                      no_connection_id         
                sysclk_0             1       1        0        500000000   0          0     50000      Y                  deviceless                      no_connection_id         
                   pwm_sel           0       0        0        500000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      pwm            0       0        0        500000000   0          0     50000      Y                        deviceless                      no_connection_id         
                   cgu0_s1seldiv     0       0        0        250000000   0          0     50000      Y                     deviceless                      no_connection_id         
                   cgu0_s0seldiv     1       1        0        125000000   0          0     50000      Y                     deviceless                      no_connection_id         
                      sclk0_0        5       5        0        125000000   0          0     50000      Y                        31008000.watchdog               sclk0                    
                                                                                                                                31003000.serial                 sclk0                    
                                                                                                                                31001200.i2c                    sclk0                    
                                                                                                                                31001600.i2c                    sclk0                    
                                                                                                                                deviceless                      no_connection_id         
                         mshc_sel    0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            mshc     0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         trace_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            trace    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         xspi0_sel   0       0        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            xspi0    0       0        0        125000000   0          0     50000      Y                              deviceless                      no_connection_id         
                         gige_sel    1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            gige     1       1        0        125000000   0          0     50000      Y                              31040000.ethernet               stmmaceth                
                                                                                                                                      deviceless                      no_connection_id         
                         spi_sel     1       1        0        125000000   0          0     50000      Y                           deviceless                      no_connection_id         
                            spi      1       1        0        125000000   0          0     50000      Y                              3102f000.spi                    spi                      
                                                                                                                                      deviceless                      no_connection_id         
                cgu0_cdiv            1       1        0        1000000000  0          0     50000      Y                  deviceless                      no_connection_id         
                   cclk0_0           1       1        0        1000000000  0          0     50000      Y                     deviceless                      no_connection_id         
                      sharc0_sel     1       1        0        1000000000  0          0     50000      Y                        deviceless                      no_connection_id         
                         sharc0      1       1        0        1000000000  0          0     50000      Y                           deviceless                      no_connection_id     
```
