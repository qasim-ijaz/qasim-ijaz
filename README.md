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
