                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.3.1 #8804 (Aug  6 2013) (Linux)
                                      4 ; This file was generated Mon Aug 25 04:16:58 2014
                                      5 ;--------------------------------------------------------
                                      6 	.module contiki_main
                                      7 	.optsdcc -mmcs51 --model-huge
                                      8 	
                                      9 ;--------------------------------------------------------
                                     10 ; Public variables in this module
                                     11 ;--------------------------------------------------------
                                     12 	.globl _main
                                     13 	.globl _random_init
                                     14 	.globl _puthex
                                     15 	.globl _putstring
                                     16 	.globl _putchar
                                     17 	.globl _netstack_init
                                     18 	.globl _queuebuf_init
                                     19 	.globl _packetbuf_set_datalen
                                     20 	.globl _packetbuf_dataptr
                                     21 	.globl _packetbuf_clear
                                     22 	.globl _cc2530_rf_set_addr
                                     23 	.globl _uart0_set_input
                                     24 	.globl _uart0_init
                                     25 	.globl _leds_off
                                     26 	.globl _leds_on
                                     27 	.globl _leds_init
                                     28 	.globl _serial_line_init
                                     29 	.globl _serial_line_input_byte
                                     30 	.globl _soc_init
                                     31 	.globl _energest_init
                                     32 	.globl _rtimer_init
                                     33 	.globl _ctimer_init
                                     34 	.globl _etimer_next_expiration_time
                                     35 	.globl _etimer_pending
                                     36 	.globl _etimer_request_poll
                                     37 	.globl _clock_time
                                     38 	.globl _clock_init
                                     39 	.globl _autostart_start
                                     40 	.globl _process_run
                                     41 	.globl _process_init
                                     42 	.globl _process_start
                                     43 	.globl _memcpy
                                     44 	.globl _watchdog_periodic
                                     45 	.globl _watchdog_start
                                     46 	.globl _watchdog_init
                                     47 	.globl _ACTIVE
                                     48 	.globl _TX_BYTE
                                     49 	.globl _RX_BYTE
                                     50 	.globl _ERR
                                     51 	.globl _FE
                                     52 	.globl _SLAVE
                                     53 	.globl _RE
                                     54 	.globl _MODE
                                     55 	.globl _T3OVFIF
                                     56 	.globl _T3CH0IF
                                     57 	.globl _T3CH1IF
                                     58 	.globl _T4OVFIF
                                     59 	.globl _T4CH0IF
                                     60 	.globl _T4CH1IF
                                     61 	.globl _OVFIM
                                     62 	.globl _B_0
                                     63 	.globl _B_1
                                     64 	.globl _B_2
                                     65 	.globl _B_3
                                     66 	.globl _B_4
                                     67 	.globl _B_5
                                     68 	.globl _B_6
                                     69 	.globl _B_7
                                     70 	.globl _P2IF
                                     71 	.globl _UTX0IF
                                     72 	.globl _UTX1IF
                                     73 	.globl _P1IF
                                     74 	.globl _WDTIF
                                     75 	.globl _ACC_0
                                     76 	.globl _ACC_1
                                     77 	.globl _ACC_2
                                     78 	.globl _ACC_3
                                     79 	.globl _ACC_4
                                     80 	.globl _ACC_5
                                     81 	.globl _ACC_6
                                     82 	.globl _ACC_7
                                     83 	.globl _P
                                     84 	.globl _F1
                                     85 	.globl _OV
                                     86 	.globl _RS0
                                     87 	.globl _RS1
                                     88 	.globl _F0
                                     89 	.globl _AC
                                     90 	.globl _CY
                                     91 	.globl _DMAIF
                                     92 	.globl _T1IF
                                     93 	.globl _T2IF
                                     94 	.globl _T3IF
                                     95 	.globl _T4IF
                                     96 	.globl _P0IF
                                     97 	.globl _STIF
                                     98 	.globl _DMAIE
                                     99 	.globl _T1IE
                                    100 	.globl _T2IE
                                    101 	.globl _T3IE
                                    102 	.globl _T4IE
                                    103 	.globl _P0IE
                                    104 	.globl _RFERRIE
                                    105 	.globl _ADCIE
                                    106 	.globl _URX0IE
                                    107 	.globl _URX1IE
                                    108 	.globl _ENCIE
                                    109 	.globl _STIE
                                    110 	.globl _EA
                                    111 	.globl _P2_0
                                    112 	.globl _P2_1
                                    113 	.globl _P2_2
                                    114 	.globl _P2_3
                                    115 	.globl _P2_4
                                    116 	.globl _P2_5
                                    117 	.globl _P2_6
                                    118 	.globl _P2_7
                                    119 	.globl _ENCIF_0
                                    120 	.globl _ENCIF_1
                                    121 	.globl _P1_0
                                    122 	.globl _P1_1
                                    123 	.globl _P1_2
                                    124 	.globl _P1_3
                                    125 	.globl _P1_4
                                    126 	.globl _P1_5
                                    127 	.globl _P1_6
                                    128 	.globl _P1_7
                                    129 	.globl _IT0
                                    130 	.globl _RFERRIF
                                    131 	.globl _IT1
                                    132 	.globl _URX0IF
                                    133 	.globl _ADCIF
                                    134 	.globl _URX1IF
                                    135 	.globl _P0_0
                                    136 	.globl _P0_1
                                    137 	.globl _P0_2
                                    138 	.globl _P0_3
                                    139 	.globl _P0_4
                                    140 	.globl _P0_5
                                    141 	.globl _P0_6
                                    142 	.globl _P0_7
                                    143 	.globl _WDCTL
                                    144 	.globl _U1GCR
                                    145 	.globl _U1UCR
                                    146 	.globl _U1BAUD
                                    147 	.globl _U1DBUF
                                    148 	.globl _U1CSR
                                    149 	.globl _U0GCR
                                    150 	.globl _U0UCR
                                    151 	.globl _U0BAUD
                                    152 	.globl _U0DBUF
                                    153 	.globl _U0CSR
                                    154 	.globl _TIMIF
                                    155 	.globl _T4CC1
                                    156 	.globl _T4CCTL1
                                    157 	.globl _T4CC0
                                    158 	.globl _T4CCTL0
                                    159 	.globl _T4CTL
                                    160 	.globl _T4CNT
                                    161 	.globl _T3CC1
                                    162 	.globl _T3CCTL1
                                    163 	.globl _T3CC0
                                    164 	.globl _T3CCTL0
                                    165 	.globl _T3CTL
                                    166 	.globl _T3CNT
                                    167 	.globl _T2MSEL
                                    168 	.globl _T2IRQM
                                    169 	.globl _T2MOVF2
                                    170 	.globl _T2MOVF1
                                    171 	.globl _T2MOVF0
                                    172 	.globl _T2M1
                                    173 	.globl _T2M0
                                    174 	.globl _T2IRQF
                                    175 	.globl _T2EVTCFG
                                    176 	.globl _T2CTRL
                                    177 	.globl _T1STAT
                                    178 	.globl _T1CCTL2
                                    179 	.globl _T1CCTL1
                                    180 	.globl _T1CCTL0
                                    181 	.globl _T1CTL
                                    182 	.globl _T1CNTH
                                    183 	.globl _T1CNTL
                                    184 	.globl _T1CC2H
                                    185 	.globl _T1CC2L
                                    186 	.globl _T1CC1H
                                    187 	.globl _T1CC1L
                                    188 	.globl _T1CC0H
                                    189 	.globl _T1CC0L
                                    190 	.globl _CLKCONSTA
                                    191 	.globl _CLKCONCMD
                                    192 	.globl _SLEEPSTA
                                    193 	.globl _SLEEPCMD
                                    194 	.globl _STLOAD
                                    195 	.globl _ST2
                                    196 	.globl _ST1
                                    197 	.globl _ST0
                                    198 	.globl _RFERRF
                                    199 	.globl _RFIRQF0
                                    200 	.globl _RFST
                                    201 	.globl _RFD
                                    202 	.globl _RFIRQF1
                                    203 	.globl _PSBANK
                                    204 	.globl _FMAP
                                    205 	.globl _MEMCTR
                                    206 	.globl __XPAGE
                                    207 	.globl _MPAGE
                                    208 	.globl _PMUX
                                    209 	.globl _P2DIR
                                    210 	.globl _P1DIR
                                    211 	.globl _P0DIR
                                    212 	.globl _P2INP
                                    213 	.globl _P1INP
                                    214 	.globl _P2SEL
                                    215 	.globl _P1SEL
                                    216 	.globl _P0SEL
                                    217 	.globl _APCFG
                                    218 	.globl _PERCFG
                                    219 	.globl _P0INP
                                    220 	.globl _P2IEN
                                    221 	.globl _P1IEN
                                    222 	.globl _P0IEN
                                    223 	.globl _PICTL
                                    224 	.globl _P2IFG
                                    225 	.globl _P1IFG
                                    226 	.globl _P0IFG
                                    227 	.globl _DMAREQ
                                    228 	.globl _DMAARM
                                    229 	.globl _DMA0CFGH
                                    230 	.globl _DMA0CFGL
                                    231 	.globl _DMA1CFGH
                                    232 	.globl _DMA1CFGL
                                    233 	.globl _DMAIRQ
                                    234 	.globl _ENCCS
                                    235 	.globl _ENCDO
                                    236 	.globl _ENCDI
                                    237 	.globl _RNDH
                                    238 	.globl _RNDL
                                    239 	.globl _ADCH
                                    240 	.globl _ADCL
                                    241 	.globl _ADCCON3
                                    242 	.globl _ADCCON2
                                    243 	.globl _ADCCON1
                                    244 	.globl _B
                                    245 	.globl _IRCON2
                                    246 	.globl _ACC
                                    247 	.globl _PSW
                                    248 	.globl _IRCON
                                    249 	.globl _IP1
                                    250 	.globl _IEN1
                                    251 	.globl _IP0
                                    252 	.globl _IEN0
                                    253 	.globl _P2
                                    254 	.globl _S1CON
                                    255 	.globl _IEN2
                                    256 	.globl _S0CON
                                    257 	.globl _DPS
                                    258 	.globl _P1
                                    259 	.globl _TCON
                                    260 	.globl _PCON
                                    261 	.globl _DPH1
                                    262 	.globl _DPL1
                                    263 	.globl _DPH0
                                    264 	.globl _DPL0
                                    265 	.globl _SP
                                    266 	.globl _P0
                                    267 	.globl _X_IEEE_ADDR
                                    268 	.globl _X_INFOPAGE
                                    269 	.globl _X_P2DIR
                                    270 	.globl _X_P1DIR
                                    271 	.globl _X_P0DIR
                                    272 	.globl _X_U1GCR
                                    273 	.globl _X_U1UCR
                                    274 	.globl _X_U1BAUD
                                    275 	.globl _X_U1DBUF
                                    276 	.globl _X_U1CSR
                                    277 	.globl _X_P2INP
                                    278 	.globl _X_P1INP
                                    279 	.globl _X_P2SEL
                                    280 	.globl _X_P1SEL
                                    281 	.globl _X_P0SEL
                                    282 	.globl _X_APCFG
                                    283 	.globl _X_PERCFG
                                    284 	.globl _X_T4CC1
                                    285 	.globl _X_T4CCTL1
                                    286 	.globl _X_T4CC0
                                    287 	.globl _X_T4CCTL0
                                    288 	.globl _X_T4CTL
                                    289 	.globl _X_T4CNT
                                    290 	.globl _X_RFIRQF0
                                    291 	.globl _X_T1CCTL2
                                    292 	.globl _X_T1CCTL1
                                    293 	.globl _X_T1CCTL0
                                    294 	.globl _X_T1CTL
                                    295 	.globl _X_T1CNTH
                                    296 	.globl _X_T1CNTL
                                    297 	.globl _X_RFST
                                    298 	.globl _X_T1CC2H
                                    299 	.globl _X_T1CC2L
                                    300 	.globl _X_T1CC1H
                                    301 	.globl _X_T1CC1L
                                    302 	.globl _X_T1CC0H
                                    303 	.globl _X_T1CC0L
                                    304 	.globl _X_RFD
                                    305 	.globl _X_TIMIF
                                    306 	.globl _X_DMAREQ
                                    307 	.globl _X_DMAARM
                                    308 	.globl _X_DMA0CFGH
                                    309 	.globl _X_DMA0CFGL
                                    310 	.globl _X_DMA1CFGH
                                    311 	.globl _X_DMA1CFGL
                                    312 	.globl _X_DMAIRQ
                                    313 	.globl _X_T3CC1
                                    314 	.globl _X_T3CCTL1
                                    315 	.globl _X_T3CC0
                                    316 	.globl _X_T3CCTL0
                                    317 	.globl _X_T3CTL
                                    318 	.globl _X_T3CNT
                                    319 	.globl _X_WDCTL
                                    320 	.globl _X_MEMCTR
                                    321 	.globl _X_CLKCONCMD
                                    322 	.globl _X_U0GCR
                                    323 	.globl _X_U0UCR
                                    324 	.globl _X_T2MSEL
                                    325 	.globl _X_U0BAUD
                                    326 	.globl _X_U0DBUF
                                    327 	.globl _X_RFERRF
                                    328 	.globl _X_SLEEPCMD
                                    329 	.globl _X_RNDH
                                    330 	.globl _X_RNDL
                                    331 	.globl _X_ADCH
                                    332 	.globl _X_ADCL
                                    333 	.globl _X_ADCCON3
                                    334 	.globl _X_ADCCON2
                                    335 	.globl _X_ADCCON1
                                    336 	.globl _X_ENCCS
                                    337 	.globl _X_ENCDO
                                    338 	.globl _X_ENCDI
                                    339 	.globl _X_T1STAT
                                    340 	.globl _X_PMUX
                                    341 	.globl _X_STLOAD
                                    342 	.globl _X_P2IEN
                                    343 	.globl _X_P0IEN
                                    344 	.globl _X_T2IRQM
                                    345 	.globl _X_T2MOVF2
                                    346 	.globl _X_T2MOVF1
                                    347 	.globl _X_T2MOVF0
                                    348 	.globl _X_T2M1
                                    349 	.globl _X_T2M0
                                    350 	.globl _X_T2IRQF
                                    351 	.globl _X_P2
                                    352 	.globl _X_PSBANK
                                    353 	.globl _X_FMAP
                                    354 	.globl _X_CLKCONSTA
                                    355 	.globl _X_SLEEPSTA
                                    356 	.globl _X_T2EVTCFG
                                    357 	.globl _X_ST2
                                    358 	.globl _X_ST1
                                    359 	.globl _X_ST0
                                    360 	.globl _X_T2CTRL
                                    361 	.globl _X__XPAGE
                                    362 	.globl _X_MPAGE
                                    363 	.globl _X_RFIRQF1
                                    364 	.globl _X_P1
                                    365 	.globl _X_P0INP
                                    366 	.globl _X_P1IEN
                                    367 	.globl _X_PICTL
                                    368 	.globl _X_P2IFG
                                    369 	.globl _X_P1IFG
                                    370 	.globl _X_P0IFG
                                    371 	.globl _X_U0CSR
                                    372 	.globl _X_P0
                                    373 	.globl _USBF5
                                    374 	.globl _USBF4
                                    375 	.globl _USBF3
                                    376 	.globl _USBF2
                                    377 	.globl _USBF1
                                    378 	.globl _USBF0
                                    379 	.globl _USBCNTH
                                    380 	.globl _USBCNTL
                                    381 	.globl _USBCNT0
                                    382 	.globl _USBCSOH
                                    383 	.globl _USBCSOL
                                    384 	.globl _USBMAXO
                                    385 	.globl _USBCSIH
                                    386 	.globl _USBCSIL
                                    387 	.globl _USBCS0
                                    388 	.globl _USBMAXI
                                    389 	.globl _USBCTRL
                                    390 	.globl _USBINDEX
                                    391 	.globl _USBFRMH
                                    392 	.globl _USBFRML
                                    393 	.globl _USBCIE
                                    394 	.globl _USBOIE
                                    395 	.globl _USBIIE
                                    396 	.globl _USBCIF
                                    397 	.globl _USBOIF
                                    398 	.globl _USBIIF
                                    399 	.globl _USBPOW
                                    400 	.globl _USBADDR
                                    401 	.globl _CSPT
                                    402 	.globl _CSPZ
                                    403 	.globl _CSPY
                                    404 	.globl _CSPX
                                    405 	.globl _CSPSTAT
                                    406 	.globl _CSPCTRL
                                    407 	.globl _CSPPROG23
                                    408 	.globl _CSPPROG22
                                    409 	.globl _CSPPROG21
                                    410 	.globl _CSPPROG20
                                    411 	.globl _CSPPROG19
                                    412 	.globl _CSPPROG18
                                    413 	.globl _CSPPROG17
                                    414 	.globl _CSPPROG16
                                    415 	.globl _CSPPROG15
                                    416 	.globl _CSPPROG14
                                    417 	.globl _CSPPROG13
                                    418 	.globl _CSPPROG12
                                    419 	.globl _CSPPROG11
                                    420 	.globl _CSPPROG10
                                    421 	.globl _CSPPROG9
                                    422 	.globl _CSPPROG8
                                    423 	.globl _CSPPROG7
                                    424 	.globl _CSPPROG6
                                    425 	.globl _CSPPROG5
                                    426 	.globl _CSPPROG4
                                    427 	.globl _CSPPROG3
                                    428 	.globl _CSPPROG2
                                    429 	.globl _CSPPROG1
                                    430 	.globl _CSPPROG0
                                    431 	.globl _RFC_OBS_CTRL2
                                    432 	.globl _RFC_OBS_CTRL1
                                    433 	.globl _RFC_OBS_CTRL0
                                    434 	.globl _TXFILTCFG
                                    435 	.globl _PTEST1
                                    436 	.globl _PTEST0
                                    437 	.globl _ATEST
                                    438 	.globl _DACTEST2
                                    439 	.globl _DACTEST1
                                    440 	.globl _DACTEST0
                                    441 	.globl _MDMTEST1
                                    442 	.globl _MDMTEST0
                                    443 	.globl _ADCTEST2
                                    444 	.globl _ADCTEST1
                                    445 	.globl _ADCTEST0
                                    446 	.globl _AGCCTRL3
                                    447 	.globl _AGCCTRL2
                                    448 	.globl _AGCCTRL1
                                    449 	.globl _AGCCTRL0
                                    450 	.globl _FSCAL3
                                    451 	.globl _FSCAL2
                                    452 	.globl _FSCAL1
                                    453 	.globl _FSCAL0
                                    454 	.globl _FSCTRL
                                    455 	.globl _RXCTRL
                                    456 	.globl _FREQEST
                                    457 	.globl _MDMCTRL1
                                    458 	.globl _MDMCTRL0
                                    459 	.globl _RFRND
                                    460 	.globl _RFERRM
                                    461 	.globl _RFIRQM1
                                    462 	.globl _RFIRQM0
                                    463 	.globl _TXLAST_PTR
                                    464 	.globl _TXFIRST_PTR
                                    465 	.globl _RXP1_PTR
                                    466 	.globl _RXLAST_PTR
                                    467 	.globl _RXFIRST_PTR
                                    468 	.globl _TXFIFOCNT
                                    469 	.globl _RXFIFOCNT
                                    470 	.globl _RXFIRST
                                    471 	.globl _RSSISTAT
                                    472 	.globl _RSSI
                                    473 	.globl _CCACTRL1
                                    474 	.globl _CCACTRL0
                                    475 	.globl _FSMCTRL
                                    476 	.globl _FIFOPCTRL
                                    477 	.globl _FSMSTAT1
                                    478 	.globl _FSMSTAT0
                                    479 	.globl _TXCTRL
                                    480 	.globl _TXPOWER
                                    481 	.globl _FREQCTRL
                                    482 	.globl _FREQTUNE
                                    483 	.globl _RXMASKCLR
                                    484 	.globl _RXMASKSET
                                    485 	.globl _RXENABLE
                                    486 	.globl _FRMCTRL1
                                    487 	.globl _FRMCTRL0
                                    488 	.globl _SRCEXTEN2
                                    489 	.globl _SRCEXTEN1
                                    490 	.globl _SRCEXTEN0
                                    491 	.globl _SRCSHORTEN2
                                    492 	.globl _SRCSHORTEN1
                                    493 	.globl _SRCSHORTEN0
                                    494 	.globl _SRCMATCH
                                    495 	.globl _FRMFILT1
                                    496 	.globl _FRMFILT0
                                    497 	.globl _SHORT_ADDR1
                                    498 	.globl _SHORT_ADDR0
                                    499 	.globl _PAN_ID1
                                    500 	.globl _PAN_ID0
                                    501 	.globl _EXT_ADDR7
                                    502 	.globl _EXT_ADDR6
                                    503 	.globl _EXT_ADDR5
                                    504 	.globl _EXT_ADDR4
                                    505 	.globl _EXT_ADDR3
                                    506 	.globl _EXT_ADDR2
                                    507 	.globl _EXT_ADDR1
                                    508 	.globl _EXT_ADDR0
                                    509 	.globl _SRCSHORTPENDEN2
                                    510 	.globl _SRCSHORTPENDEN1
                                    511 	.globl _SRCSHORTPENDEN0
                                    512 	.globl _SRCEXTPENDEN2
                                    513 	.globl _SRCEXTPENDEN1
                                    514 	.globl _SRCEXTPENDEN0
                                    515 	.globl _SRCRESINDEX
                                    516 	.globl _SRCRESMASK2
                                    517 	.globl _SRCRESMASK1
                                    518 	.globl _SRCRESMASK0
                                    519 	.globl _SRC_ADDR_TABLE
                                    520 	.globl _TXFIFO
                                    521 	.globl _RXFIFO
                                    522 	.globl _RFCORE_RAM
                                    523 	.globl _CMPCTL
                                    524 	.globl _OPAMPS
                                    525 	.globl _OPAMPC
                                    526 	.globl _STCV2
                                    527 	.globl _STCV1
                                    528 	.globl _STCV0
                                    529 	.globl _STCS
                                    530 	.globl _STCC
                                    531 	.globl _T1CC4H
                                    532 	.globl _T1CC4L
                                    533 	.globl _T1CC3H
                                    534 	.globl _T1CC3L
                                    535 	.globl _XX_T1CC2H
                                    536 	.globl _XX_T1CC2L
                                    537 	.globl _XX_T1CC1H
                                    538 	.globl _XX_T1CC1L
                                    539 	.globl _XX_T1CC0H
                                    540 	.globl _XX_T1CC0L
                                    541 	.globl _T1CCTL4
                                    542 	.globl _T1CCTL3
                                    543 	.globl _XX_T1CCTL2
                                    544 	.globl _XX_T1CCTL1
                                    545 	.globl _XX_T1CCTL0
                                    546 	.globl _CLD
                                    547 	.globl _IRCTL
                                    548 	.globl _CHIPINFO1
                                    549 	.globl _CHIPINFO0
                                    550 	.globl _FWDATA
                                    551 	.globl _FADDRH
                                    552 	.globl _FADDRL
                                    553 	.globl _FCTL
                                    554 	.globl _IVCTRL
                                    555 	.globl _BATTMON
                                    556 	.globl _SRCRC
                                    557 	.globl _DBGDATA
                                    558 	.globl _TESTREG0
                                    559 	.globl _CHIPID
                                    560 	.globl _CHVER
                                    561 	.globl _OBSSEL5
                                    562 	.globl _OBSSEL4
                                    563 	.globl _OBSSEL3
                                    564 	.globl _OBSSEL2
                                    565 	.globl _OBSSEL1
                                    566 	.globl _OBSSEL0
                                    567 	.globl _I2CIO
                                    568 	.globl _I2CWC
                                    569 	.globl _I2CADDR
                                    570 	.globl _I2CDATA
                                    571 	.globl _I2CSTAT
                                    572 	.globl _I2CCFG
                                    573 	.globl _OPAMPMC
                                    574 	.globl _MONMUX
                                    575 ;--------------------------------------------------------
                                    576 ; special function registers
                                    577 ;--------------------------------------------------------
                                    578 	.area RSEG    (ABS,DATA)
      000000                        579 	.org 0x0000
                           000080   580 _P0	=	0x0080
                           000081   581 _SP	=	0x0081
                           000082   582 _DPL0	=	0x0082
                           000083   583 _DPH0	=	0x0083
                           000084   584 _DPL1	=	0x0084
                           000085   585 _DPH1	=	0x0085
                           000087   586 _PCON	=	0x0087
                           000088   587 _TCON	=	0x0088
                           000090   588 _P1	=	0x0090
                           000092   589 _DPS	=	0x0092
                           000098   590 _S0CON	=	0x0098
                           00009A   591 _IEN2	=	0x009a
                           00009B   592 _S1CON	=	0x009b
                           0000A0   593 _P2	=	0x00a0
                           0000A8   594 _IEN0	=	0x00a8
                           0000A9   595 _IP0	=	0x00a9
                           0000B8   596 _IEN1	=	0x00b8
                           0000B9   597 _IP1	=	0x00b9
                           0000C0   598 _IRCON	=	0x00c0
                           0000D0   599 _PSW	=	0x00d0
                           0000E0   600 _ACC	=	0x00e0
                           0000E8   601 _IRCON2	=	0x00e8
                           0000F0   602 _B	=	0x00f0
                           0000B4   603 _ADCCON1	=	0x00b4
                           0000B5   604 _ADCCON2	=	0x00b5
                           0000B6   605 _ADCCON3	=	0x00b6
                           0000BA   606 _ADCL	=	0x00ba
                           0000BB   607 _ADCH	=	0x00bb
                           0000BC   608 _RNDL	=	0x00bc
                           0000BD   609 _RNDH	=	0x00bd
                           0000B1   610 _ENCDI	=	0x00b1
                           0000B2   611 _ENCDO	=	0x00b2
                           0000B3   612 _ENCCS	=	0x00b3
                           0000D1   613 _DMAIRQ	=	0x00d1
                           0000D2   614 _DMA1CFGL	=	0x00d2
                           0000D3   615 _DMA1CFGH	=	0x00d3
                           0000D4   616 _DMA0CFGL	=	0x00d4
                           0000D5   617 _DMA0CFGH	=	0x00d5
                           0000D6   618 _DMAARM	=	0x00d6
                           0000D7   619 _DMAREQ	=	0x00d7
                           000089   620 _P0IFG	=	0x0089
                           00008A   621 _P1IFG	=	0x008a
                           00008B   622 _P2IFG	=	0x008b
                           00008C   623 _PICTL	=	0x008c
                           0000AB   624 _P0IEN	=	0x00ab
                           00008D   625 _P1IEN	=	0x008d
                           0000AC   626 _P2IEN	=	0x00ac
                           00008F   627 _P0INP	=	0x008f
                           0000F1   628 _PERCFG	=	0x00f1
                           0000F2   629 _APCFG	=	0x00f2
                           0000F3   630 _P0SEL	=	0x00f3
                           0000F4   631 _P1SEL	=	0x00f4
                           0000F5   632 _P2SEL	=	0x00f5
                           0000F6   633 _P1INP	=	0x00f6
                           0000F7   634 _P2INP	=	0x00f7
                           0000FD   635 _P0DIR	=	0x00fd
                           0000FE   636 _P1DIR	=	0x00fe
                           0000FF   637 _P2DIR	=	0x00ff
                           0000AE   638 _PMUX	=	0x00ae
                           000093   639 _MPAGE	=	0x0093
                           000093   640 __XPAGE	=	0x0093
                           0000C7   641 _MEMCTR	=	0x00c7
                           00009F   642 _FMAP	=	0x009f
                           00009F   643 _PSBANK	=	0x009f
                           000091   644 _RFIRQF1	=	0x0091
                           0000D9   645 _RFD	=	0x00d9
                           0000E1   646 _RFST	=	0x00e1
                           0000E9   647 _RFIRQF0	=	0x00e9
                           0000BF   648 _RFERRF	=	0x00bf
                           000095   649 _ST0	=	0x0095
                           000096   650 _ST1	=	0x0096
                           000097   651 _ST2	=	0x0097
                           0000AD   652 _STLOAD	=	0x00ad
                           0000BE   653 _SLEEPCMD	=	0x00be
                           00009D   654 _SLEEPSTA	=	0x009d
                           0000C6   655 _CLKCONCMD	=	0x00c6
                           00009E   656 _CLKCONSTA	=	0x009e
                           0000DA   657 _T1CC0L	=	0x00da
                           0000DB   658 _T1CC0H	=	0x00db
                           0000DC   659 _T1CC1L	=	0x00dc
                           0000DD   660 _T1CC1H	=	0x00dd
                           0000DE   661 _T1CC2L	=	0x00de
                           0000DF   662 _T1CC2H	=	0x00df
                           0000E2   663 _T1CNTL	=	0x00e2
                           0000E3   664 _T1CNTH	=	0x00e3
                           0000E4   665 _T1CTL	=	0x00e4
                           0000E5   666 _T1CCTL0	=	0x00e5
                           0000E6   667 _T1CCTL1	=	0x00e6
                           0000E7   668 _T1CCTL2	=	0x00e7
                           0000AF   669 _T1STAT	=	0x00af
                           000094   670 _T2CTRL	=	0x0094
                           00009C   671 _T2EVTCFG	=	0x009c
                           0000A1   672 _T2IRQF	=	0x00a1
                           0000A2   673 _T2M0	=	0x00a2
                           0000A3   674 _T2M1	=	0x00a3
                           0000A4   675 _T2MOVF0	=	0x00a4
                           0000A5   676 _T2MOVF1	=	0x00a5
                           0000A6   677 _T2MOVF2	=	0x00a6
                           0000A7   678 _T2IRQM	=	0x00a7
                           0000C3   679 _T2MSEL	=	0x00c3
                           0000CA   680 _T3CNT	=	0x00ca
                           0000CB   681 _T3CTL	=	0x00cb
                           0000CC   682 _T3CCTL0	=	0x00cc
                           0000CD   683 _T3CC0	=	0x00cd
                           0000CE   684 _T3CCTL1	=	0x00ce
                           0000CF   685 _T3CC1	=	0x00cf
                           0000EA   686 _T4CNT	=	0x00ea
                           0000EB   687 _T4CTL	=	0x00eb
                           0000EC   688 _T4CCTL0	=	0x00ec
                           0000ED   689 _T4CC0	=	0x00ed
                           0000EE   690 _T4CCTL1	=	0x00ee
                           0000EF   691 _T4CC1	=	0x00ef
                           0000D8   692 _TIMIF	=	0x00d8
                           000086   693 _U0CSR	=	0x0086
                           0000C1   694 _U0DBUF	=	0x00c1
                           0000C2   695 _U0BAUD	=	0x00c2
                           0000C4   696 _U0UCR	=	0x00c4
                           0000C5   697 _U0GCR	=	0x00c5
                           0000F8   698 _U1CSR	=	0x00f8
                           0000F9   699 _U1DBUF	=	0x00f9
                           0000FA   700 _U1BAUD	=	0x00fa
                           0000FB   701 _U1UCR	=	0x00fb
                           0000FC   702 _U1GCR	=	0x00fc
                           0000C9   703 _WDCTL	=	0x00c9
                                    704 ;--------------------------------------------------------
                                    705 ; special function bits
                                    706 ;--------------------------------------------------------
                                    707 	.area RSEG    (ABS,DATA)
      000000                        708 	.org 0x0000
                           000087   709 _P0_7	=	0x0087
                           000086   710 _P0_6	=	0x0086
                           000085   711 _P0_5	=	0x0085
                           000084   712 _P0_4	=	0x0084
                           000083   713 _P0_3	=	0x0083
                           000082   714 _P0_2	=	0x0082
                           000081   715 _P0_1	=	0x0081
                           000080   716 _P0_0	=	0x0080
                           00008F   717 _URX1IF	=	0x008f
                           00008D   718 _ADCIF	=	0x008d
                           00008B   719 _URX0IF	=	0x008b
                           00008A   720 _IT1	=	0x008a
                           000089   721 _RFERRIF	=	0x0089
                           000088   722 _IT0	=	0x0088
                           000097   723 _P1_7	=	0x0097
                           000096   724 _P1_6	=	0x0096
                           000095   725 _P1_5	=	0x0095
                           000094   726 _P1_4	=	0x0094
                           000093   727 _P1_3	=	0x0093
                           000092   728 _P1_2	=	0x0092
                           000091   729 _P1_1	=	0x0091
                           000090   730 _P1_0	=	0x0090
                           000099   731 _ENCIF_1	=	0x0099
                           000098   732 _ENCIF_0	=	0x0098
                           0000A7   733 _P2_7	=	0x00a7
                           0000A6   734 _P2_6	=	0x00a6
                           0000A5   735 _P2_5	=	0x00a5
                           0000A4   736 _P2_4	=	0x00a4
                           0000A3   737 _P2_3	=	0x00a3
                           0000A2   738 _P2_2	=	0x00a2
                           0000A1   739 _P2_1	=	0x00a1
                           0000A0   740 _P2_0	=	0x00a0
                           0000AF   741 _EA	=	0x00af
                           0000AD   742 _STIE	=	0x00ad
                           0000AC   743 _ENCIE	=	0x00ac
                           0000AB   744 _URX1IE	=	0x00ab
                           0000AA   745 _URX0IE	=	0x00aa
                           0000A9   746 _ADCIE	=	0x00a9
                           0000A8   747 _RFERRIE	=	0x00a8
                           0000BD   748 _P0IE	=	0x00bd
                           0000BC   749 _T4IE	=	0x00bc
                           0000BB   750 _T3IE	=	0x00bb
                           0000BA   751 _T2IE	=	0x00ba
                           0000B9   752 _T1IE	=	0x00b9
                           0000B8   753 _DMAIE	=	0x00b8
                           0000C7   754 _STIF	=	0x00c7
                           0000C5   755 _P0IF	=	0x00c5
                           0000C4   756 _T4IF	=	0x00c4
                           0000C3   757 _T3IF	=	0x00c3
                           0000C2   758 _T2IF	=	0x00c2
                           0000C1   759 _T1IF	=	0x00c1
                           0000C0   760 _DMAIF	=	0x00c0
                           0000D7   761 _CY	=	0x00d7
                           0000D6   762 _AC	=	0x00d6
                           0000D5   763 _F0	=	0x00d5
                           0000D4   764 _RS1	=	0x00d4
                           0000D3   765 _RS0	=	0x00d3
                           0000D2   766 _OV	=	0x00d2
                           0000D1   767 _F1	=	0x00d1
                           0000D0   768 _P	=	0x00d0
                           0000E7   769 _ACC_7	=	0x00e7
                           0000E6   770 _ACC_6	=	0x00e6
                           0000E5   771 _ACC_5	=	0x00e5
                           0000E4   772 _ACC_4	=	0x00e4
                           0000E3   773 _ACC_3	=	0x00e3
                           0000E2   774 _ACC_2	=	0x00e2
                           0000E1   775 _ACC_1	=	0x00e1
                           0000E0   776 _ACC_0	=	0x00e0
                           0000EC   777 _WDTIF	=	0x00ec
                           0000EB   778 _P1IF	=	0x00eb
                           0000EA   779 _UTX1IF	=	0x00ea
                           0000E9   780 _UTX0IF	=	0x00e9
                           0000E8   781 _P2IF	=	0x00e8
                           0000F7   782 _B_7	=	0x00f7
                           0000F6   783 _B_6	=	0x00f6
                           0000F5   784 _B_5	=	0x00f5
                           0000F4   785 _B_4	=	0x00f4
                           0000F3   786 _B_3	=	0x00f3
                           0000F2   787 _B_2	=	0x00f2
                           0000F1   788 _B_1	=	0x00f1
                           0000F0   789 _B_0	=	0x00f0
                           0000DE   790 _OVFIM	=	0x00de
                           0000DD   791 _T4CH1IF	=	0x00dd
                           0000DC   792 _T4CH0IF	=	0x00dc
                           0000DB   793 _T4OVFIF	=	0x00db
                           0000DA   794 _T3CH1IF	=	0x00da
                           0000D9   795 _T3CH0IF	=	0x00d9
                           0000D8   796 _T3OVFIF	=	0x00d8
                           0000FF   797 _MODE	=	0x00ff
                           0000FE   798 _RE	=	0x00fe
                           0000FD   799 _SLAVE	=	0x00fd
                           0000FC   800 _FE	=	0x00fc
                           0000FB   801 _ERR	=	0x00fb
                           0000FA   802 _RX_BYTE	=	0x00fa
                           0000F9   803 _TX_BYTE	=	0x00f9
                           0000F8   804 _ACTIVE	=	0x00f8
                                    805 ;--------------------------------------------------------
                                    806 ; overlayable register banks
                                    807 ;--------------------------------------------------------
                                    808 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        809 	.ds 8
                                    810 ;--------------------------------------------------------
                                    811 ; internal ram data
                                    812 ;--------------------------------------------------------
                                    813 	.area DSEG    (DATA)
      000008                        814 _len:
      000008                        815 	.ds 2
                                    816 ;--------------------------------------------------------
                                    817 ; overlayable items in internal ram 
                                    818 ;--------------------------------------------------------
                                    819 ;--------------------------------------------------------
                                    820 ; Stack segment in internal ram 
                                    821 ;--------------------------------------------------------
                                    822 	.area	SSEG
      000021                        823 __start__stack:
      000021                        824 	.ds	1
                                    825 
                                    826 ;--------------------------------------------------------
                                    827 ; indirectly addressable internal ram data
                                    828 ;--------------------------------------------------------
                                    829 	.area ISEG    (DATA)
                                    830 ;--------------------------------------------------------
                                    831 ; absolute internal ram data
                                    832 ;--------------------------------------------------------
                                    833 	.area IABS    (ABS,DATA)
                                    834 	.area IABS    (ABS,DATA)
                                    835 ;--------------------------------------------------------
                                    836 ; bit data
                                    837 ;--------------------------------------------------------
                                    838 	.area BSEG    (BIT)
                                    839 ;--------------------------------------------------------
                                    840 ; paged external ram data
                                    841 ;--------------------------------------------------------
                                    842 	.area PSEG    (PAG,XDATA)
                                    843 ;--------------------------------------------------------
                                    844 ; external ram data
                                    845 ;--------------------------------------------------------
                                    846 	.area XSEG    (XDATA)
                           0061A6   847 _MONMUX	=	0x61a6
                           0061A6   848 _OPAMPMC	=	0x61a6
                           006230   849 _I2CCFG	=	0x6230
                           006231   850 _I2CSTAT	=	0x6231
                           006232   851 _I2CDATA	=	0x6232
                           006233   852 _I2CADDR	=	0x6233
                           006234   853 _I2CWC	=	0x6234
                           006235   854 _I2CIO	=	0x6235
                           006243   855 _OBSSEL0	=	0x6243
                           006244   856 _OBSSEL1	=	0x6244
                           006245   857 _OBSSEL2	=	0x6245
                           006246   858 _OBSSEL3	=	0x6246
                           006247   859 _OBSSEL4	=	0x6247
                           006248   860 _OBSSEL5	=	0x6248
                           006249   861 _CHVER	=	0x6249
                           00624A   862 _CHIPID	=	0x624a
                           00624B   863 _TESTREG0	=	0x624b
                           006260   864 _DBGDATA	=	0x6260
                           006262   865 _SRCRC	=	0x6262
                           006264   866 _BATTMON	=	0x6264
                           006265   867 _IVCTRL	=	0x6265
                           006270   868 _FCTL	=	0x6270
                           006271   869 _FADDRL	=	0x6271
                           006272   870 _FADDRH	=	0x6272
                           006273   871 _FWDATA	=	0x6273
                           006276   872 _CHIPINFO0	=	0x6276
                           006277   873 _CHIPINFO1	=	0x6277
                           006281   874 _IRCTL	=	0x6281
                           006290   875 _CLD	=	0x6290
                           0062A0   876 _XX_T1CCTL0	=	0x62a0
                           0062A1   877 _XX_T1CCTL1	=	0x62a1
                           0062A2   878 _XX_T1CCTL2	=	0x62a2
                           0062A3   879 _T1CCTL3	=	0x62a3
                           0062A4   880 _T1CCTL4	=	0x62a4
                           0062A6   881 _XX_T1CC0L	=	0x62a6
                           0062A7   882 _XX_T1CC0H	=	0x62a7
                           0062A8   883 _XX_T1CC1L	=	0x62a8
                           0062A9   884 _XX_T1CC1H	=	0x62a9
                           0062AA   885 _XX_T1CC2L	=	0x62aa
                           0062AB   886 _XX_T1CC2H	=	0x62ab
                           0062AC   887 _T1CC3L	=	0x62ac
                           0062AD   888 _T1CC3H	=	0x62ad
                           0062AE   889 _T1CC4L	=	0x62ae
                           0062AF   890 _T1CC4H	=	0x62af
                           0062B0   891 _STCC	=	0x62b0
                           0062B1   892 _STCS	=	0x62b1
                           0062B2   893 _STCV0	=	0x62b2
                           0062B3   894 _STCV1	=	0x62b3
                           0062B4   895 _STCV2	=	0x62b4
                           0062C0   896 _OPAMPC	=	0x62c0
                           0062C1   897 _OPAMPS	=	0x62c1
                           0062D0   898 _CMPCTL	=	0x62d0
                           006000   899 _RFCORE_RAM	=	0x6000
                           006000   900 _RXFIFO	=	0x6000
                           006080   901 _TXFIFO	=	0x6080
                           006100   902 _SRC_ADDR_TABLE	=	0x6100
                           006160   903 _SRCRESMASK0	=	0x6160
                           006161   904 _SRCRESMASK1	=	0x6161
                           006162   905 _SRCRESMASK2	=	0x6162
                           006163   906 _SRCRESINDEX	=	0x6163
                           006164   907 _SRCEXTPENDEN0	=	0x6164
                           006165   908 _SRCEXTPENDEN1	=	0x6165
                           006166   909 _SRCEXTPENDEN2	=	0x6166
                           006167   910 _SRCSHORTPENDEN0	=	0x6167
                           006168   911 _SRCSHORTPENDEN1	=	0x6168
                           006169   912 _SRCSHORTPENDEN2	=	0x6169
                           00616A   913 _EXT_ADDR0	=	0x616a
                           00616B   914 _EXT_ADDR1	=	0x616b
                           00616C   915 _EXT_ADDR2	=	0x616c
                           00616D   916 _EXT_ADDR3	=	0x616d
                           00616E   917 _EXT_ADDR4	=	0x616e
                           00616F   918 _EXT_ADDR5	=	0x616f
                           006170   919 _EXT_ADDR6	=	0x6170
                           006171   920 _EXT_ADDR7	=	0x6171
                           006172   921 _PAN_ID0	=	0x6172
                           006173   922 _PAN_ID1	=	0x6173
                           006174   923 _SHORT_ADDR0	=	0x6174
                           006175   924 _SHORT_ADDR1	=	0x6175
                           006180   925 _FRMFILT0	=	0x6180
                           006181   926 _FRMFILT1	=	0x6181
                           006182   927 _SRCMATCH	=	0x6182
                           006183   928 _SRCSHORTEN0	=	0x6183
                           006184   929 _SRCSHORTEN1	=	0x6184
                           006185   930 _SRCSHORTEN2	=	0x6185
                           006186   931 _SRCEXTEN0	=	0x6186
                           006187   932 _SRCEXTEN1	=	0x6187
                           006188   933 _SRCEXTEN2	=	0x6188
                           006189   934 _FRMCTRL0	=	0x6189
                           00618A   935 _FRMCTRL1	=	0x618a
                           00618B   936 _RXENABLE	=	0x618b
                           00618C   937 _RXMASKSET	=	0x618c
                           00618D   938 _RXMASKCLR	=	0x618d
                           00618E   939 _FREQTUNE	=	0x618e
                           00618F   940 _FREQCTRL	=	0x618f
                           006190   941 _TXPOWER	=	0x6190
                           006191   942 _TXCTRL	=	0x6191
                           006192   943 _FSMSTAT0	=	0x6192
                           006193   944 _FSMSTAT1	=	0x6193
                           006194   945 _FIFOPCTRL	=	0x6194
                           006195   946 _FSMCTRL	=	0x6195
                           006196   947 _CCACTRL0	=	0x6196
                           006197   948 _CCACTRL1	=	0x6197
                           006198   949 _RSSI	=	0x6198
                           006199   950 _RSSISTAT	=	0x6199
                           00619A   951 _RXFIRST	=	0x619a
                           00619B   952 _RXFIFOCNT	=	0x619b
                           00619C   953 _TXFIFOCNT	=	0x619c
                           00619D   954 _RXFIRST_PTR	=	0x619d
                           00619E   955 _RXLAST_PTR	=	0x619e
                           00619F   956 _RXP1_PTR	=	0x619f
                           0061A1   957 _TXFIRST_PTR	=	0x61a1
                           0061A2   958 _TXLAST_PTR	=	0x61a2
                           0061A3   959 _RFIRQM0	=	0x61a3
                           0061A4   960 _RFIRQM1	=	0x61a4
                           0061A5   961 _RFERRM	=	0x61a5
                           0061A7   962 _RFRND	=	0x61a7
                           0061A8   963 _MDMCTRL0	=	0x61a8
                           0061A9   964 _MDMCTRL1	=	0x61a9
                           0061AA   965 _FREQEST	=	0x61aa
                           0061AB   966 _RXCTRL	=	0x61ab
                           0061AC   967 _FSCTRL	=	0x61ac
                           0061AD   968 _FSCAL0	=	0x61ad
                           0061AE   969 _FSCAL1	=	0x61ae
                           0061AF   970 _FSCAL2	=	0x61af
                           0061B0   971 _FSCAL3	=	0x61b0
                           0061B1   972 _AGCCTRL0	=	0x61b1
                           0061B2   973 _AGCCTRL1	=	0x61b2
                           0061B3   974 _AGCCTRL2	=	0x61b3
                           0061B4   975 _AGCCTRL3	=	0x61b4
                           0061B5   976 _ADCTEST0	=	0x61b5
                           0061B6   977 _ADCTEST1	=	0x61b6
                           0061B7   978 _ADCTEST2	=	0x61b7
                           0061B8   979 _MDMTEST0	=	0x61b8
                           0061B9   980 _MDMTEST1	=	0x61b9
                           0061BA   981 _DACTEST0	=	0x61ba
                           0061BB   982 _DACTEST1	=	0x61bb
                           0061BC   983 _DACTEST2	=	0x61bc
                           0061BD   984 _ATEST	=	0x61bd
                           0061BE   985 _PTEST0	=	0x61be
                           0061BF   986 _PTEST1	=	0x61bf
                           0061FA   987 _TXFILTCFG	=	0x61fa
                           0061EB   988 _RFC_OBS_CTRL0	=	0x61eb
                           0061EC   989 _RFC_OBS_CTRL1	=	0x61ec
                           0061ED   990 _RFC_OBS_CTRL2	=	0x61ed
                           0061C0   991 _CSPPROG0	=	0x61c0
                           0061C1   992 _CSPPROG1	=	0x61c1
                           0061C2   993 _CSPPROG2	=	0x61c2
                           0061C3   994 _CSPPROG3	=	0x61c3
                           0061C4   995 _CSPPROG4	=	0x61c4
                           0061C5   996 _CSPPROG5	=	0x61c5
                           0061C6   997 _CSPPROG6	=	0x61c6
                           0061C7   998 _CSPPROG7	=	0x61c7
                           0061C8   999 _CSPPROG8	=	0x61c8
                           0061C9  1000 _CSPPROG9	=	0x61c9
                           0061CA  1001 _CSPPROG10	=	0x61ca
                           0061CB  1002 _CSPPROG11	=	0x61cb
                           0061CC  1003 _CSPPROG12	=	0x61cc
                           0061CD  1004 _CSPPROG13	=	0x61cd
                           0061CE  1005 _CSPPROG14	=	0x61ce
                           0061CF  1006 _CSPPROG15	=	0x61cf
                           0061D0  1007 _CSPPROG16	=	0x61d0
                           0061D1  1008 _CSPPROG17	=	0x61d1
                           0061D2  1009 _CSPPROG18	=	0x61d2
                           0061D3  1010 _CSPPROG19	=	0x61d3
                           0061D4  1011 _CSPPROG20	=	0x61d4
                           0061D5  1012 _CSPPROG21	=	0x61d5
                           0061D6  1013 _CSPPROG22	=	0x61d6
                           0061D7  1014 _CSPPROG23	=	0x61d7
                           0061E0  1015 _CSPCTRL	=	0x61e0
                           0061E1  1016 _CSPSTAT	=	0x61e1
                           0061E2  1017 _CSPX	=	0x61e2
                           0061E3  1018 _CSPY	=	0x61e3
                           0061E4  1019 _CSPZ	=	0x61e4
                           0061E5  1020 _CSPT	=	0x61e5
                           006200  1021 _USBADDR	=	0x6200
                           006201  1022 _USBPOW	=	0x6201
                           006202  1023 _USBIIF	=	0x6202
                           006204  1024 _USBOIF	=	0x6204
                           006206  1025 _USBCIF	=	0x6206
                           006207  1026 _USBIIE	=	0x6207
                           006209  1027 _USBOIE	=	0x6209
                           00620B  1028 _USBCIE	=	0x620b
                           00620C  1029 _USBFRML	=	0x620c
                           00620D  1030 _USBFRMH	=	0x620d
                           00620E  1031 _USBINDEX	=	0x620e
                           00620F  1032 _USBCTRL	=	0x620f
                           006210  1033 _USBMAXI	=	0x6210
                           006211  1034 _USBCS0	=	0x6211
                           006211  1035 _USBCSIL	=	0x6211
                           006212  1036 _USBCSIH	=	0x6212
                           006213  1037 _USBMAXO	=	0x6213
                           006214  1038 _USBCSOL	=	0x6214
                           006215  1039 _USBCSOH	=	0x6215
                           006216  1040 _USBCNT0	=	0x6216
                           006216  1041 _USBCNTL	=	0x6216
                           006217  1042 _USBCNTH	=	0x6217
                           006220  1043 _USBF0	=	0x6220
                           006222  1044 _USBF1	=	0x6222
                           006224  1045 _USBF2	=	0x6224
                           006226  1046 _USBF3	=	0x6226
                           006228  1047 _USBF4	=	0x6228
                           00622A  1048 _USBF5	=	0x622a
                           007080  1049 _X_P0	=	0x7080
                           007086  1050 _X_U0CSR	=	0x7086
                           007089  1051 _X_P0IFG	=	0x7089
                           00708A  1052 _X_P1IFG	=	0x708a
                           00708B  1053 _X_P2IFG	=	0x708b
                           00708C  1054 _X_PICTL	=	0x708c
                           00708D  1055 _X_P1IEN	=	0x708d
                           00708F  1056 _X_P0INP	=	0x708f
                           007090  1057 _X_P1	=	0x7090
                           007091  1058 _X_RFIRQF1	=	0x7091
                           007093  1059 _X_MPAGE	=	0x7093
                           007093  1060 _X__XPAGE	=	0x7093
                           007094  1061 _X_T2CTRL	=	0x7094
                           007095  1062 _X_ST0	=	0x7095
                           007096  1063 _X_ST1	=	0x7096
                           007097  1064 _X_ST2	=	0x7097
                           00709C  1065 _X_T2EVTCFG	=	0x709c
                           00709D  1066 _X_SLEEPSTA	=	0x709d
                           00709E  1067 _X_CLKCONSTA	=	0x709e
                           00709F  1068 _X_FMAP	=	0x709f
                           00709F  1069 _X_PSBANK	=	0x709f
                           0070A0  1070 _X_P2	=	0x70a0
                           0070A1  1071 _X_T2IRQF	=	0x70a1
                           0070A2  1072 _X_T2M0	=	0x70a2
                           0070A3  1073 _X_T2M1	=	0x70a3
                           0070A4  1074 _X_T2MOVF0	=	0x70a4
                           0070A5  1075 _X_T2MOVF1	=	0x70a5
                           0070A6  1076 _X_T2MOVF2	=	0x70a6
                           0070A7  1077 _X_T2IRQM	=	0x70a7
                           0070AB  1078 _X_P0IEN	=	0x70ab
                           0070AC  1079 _X_P2IEN	=	0x70ac
                           0070AD  1080 _X_STLOAD	=	0x70ad
                           0070AE  1081 _X_PMUX	=	0x70ae
                           0070AF  1082 _X_T1STAT	=	0x70af
                           0070B1  1083 _X_ENCDI	=	0x70b1
                           0070B2  1084 _X_ENCDO	=	0x70b2
                           0070B3  1085 _X_ENCCS	=	0x70b3
                           0070B4  1086 _X_ADCCON1	=	0x70b4
                           0070B5  1087 _X_ADCCON2	=	0x70b5
                           0070B6  1088 _X_ADCCON3	=	0x70b6
                           0070BA  1089 _X_ADCL	=	0x70ba
                           0070BB  1090 _X_ADCH	=	0x70bb
                           0070BC  1091 _X_RNDL	=	0x70bc
                           0070BD  1092 _X_RNDH	=	0x70bd
                           0070BE  1093 _X_SLEEPCMD	=	0x70be
                           0070BF  1094 _X_RFERRF	=	0x70bf
                           0070C1  1095 _X_U0DBUF	=	0x70c1
                           0070C2  1096 _X_U0BAUD	=	0x70c2
                           0070C3  1097 _X_T2MSEL	=	0x70c3
                           0070C4  1098 _X_U0UCR	=	0x70c4
                           0070C5  1099 _X_U0GCR	=	0x70c5
                           0070C6  1100 _X_CLKCONCMD	=	0x70c6
                           0070C7  1101 _X_MEMCTR	=	0x70c7
                           0070C9  1102 _X_WDCTL	=	0x70c9
                           0070CA  1103 _X_T3CNT	=	0x70ca
                           0070CB  1104 _X_T3CTL	=	0x70cb
                           0070CC  1105 _X_T3CCTL0	=	0x70cc
                           0070CD  1106 _X_T3CC0	=	0x70cd
                           0070CE  1107 _X_T3CCTL1	=	0x70ce
                           0070CF  1108 _X_T3CC1	=	0x70cf
                           0070D1  1109 _X_DMAIRQ	=	0x70d1
                           0070D2  1110 _X_DMA1CFGL	=	0x70d2
                           0070D3  1111 _X_DMA1CFGH	=	0x70d3
                           0070D4  1112 _X_DMA0CFGL	=	0x70d4
                           0070D5  1113 _X_DMA0CFGH	=	0x70d5
                           0070D6  1114 _X_DMAARM	=	0x70d6
                           0070D7  1115 _X_DMAREQ	=	0x70d7
                           0070D8  1116 _X_TIMIF	=	0x70d8
                           0070D9  1117 _X_RFD	=	0x70d9
                           0070DA  1118 _X_T1CC0L	=	0x70da
                           0070DB  1119 _X_T1CC0H	=	0x70db
                           0070DC  1120 _X_T1CC1L	=	0x70dc
                           0070DD  1121 _X_T1CC1H	=	0x70dd
                           0070DE  1122 _X_T1CC2L	=	0x70de
                           0070DF  1123 _X_T1CC2H	=	0x70df
                           0070E1  1124 _X_RFST	=	0x70e1
                           0070E2  1125 _X_T1CNTL	=	0x70e2
                           0070E3  1126 _X_T1CNTH	=	0x70e3
                           0070E4  1127 _X_T1CTL	=	0x70e4
                           0070E5  1128 _X_T1CCTL0	=	0x70e5
                           0070E6  1129 _X_T1CCTL1	=	0x70e6
                           0070E7  1130 _X_T1CCTL2	=	0x70e7
                           0070E9  1131 _X_RFIRQF0	=	0x70e9
                           0070EA  1132 _X_T4CNT	=	0x70ea
                           0070EB  1133 _X_T4CTL	=	0x70eb
                           0070EC  1134 _X_T4CCTL0	=	0x70ec
                           0070ED  1135 _X_T4CC0	=	0x70ed
                           0070EE  1136 _X_T4CCTL1	=	0x70ee
                           0070EF  1137 _X_T4CC1	=	0x70ef
                           0070F1  1138 _X_PERCFG	=	0x70f1
                           0070F2  1139 _X_APCFG	=	0x70f2
                           0070F3  1140 _X_P0SEL	=	0x70f3
                           0070F4  1141 _X_P1SEL	=	0x70f4
                           0070F5  1142 _X_P2SEL	=	0x70f5
                           0070F6  1143 _X_P1INP	=	0x70f6
                           0070F7  1144 _X_P2INP	=	0x70f7
                           0070F8  1145 _X_U1CSR	=	0x70f8
                           0070F9  1146 _X_U1DBUF	=	0x70f9
                           0070FA  1147 _X_U1BAUD	=	0x70fa
                           0070FB  1148 _X_U1UCR	=	0x70fb
                           0070FC  1149 _X_U1GCR	=	0x70fc
                           0070FD  1150 _X_P0DIR	=	0x70fd
                           0070FE  1151 _X_P1DIR	=	0x70fe
                           0070FF  1152 _X_P2DIR	=	0x70ff
                           007800  1153 _X_INFOPAGE	=	0x7800
                           00780C  1154 _X_IEEE_ADDR	=	0x780c
                                   1155 ;--------------------------------------------------------
                                   1156 ; absolute external ram data
                                   1157 ;--------------------------------------------------------
                                   1158 	.area XABS    (ABS,XDATA)
                                   1159 ;--------------------------------------------------------
                                   1160 ; external initialized ram data
                                   1161 ;--------------------------------------------------------
                                   1162 	.area XISEG   (XDATA)
                                   1163 	.area HOME    (CODE)
                                   1164 	.area GSINIT0 (CODE)
                                   1165 	.area GSINIT1 (CODE)
                                   1166 	.area GSINIT2 (CODE)
                                   1167 	.area GSINIT3 (CODE)
                                   1168 	.area GSINIT4 (CODE)
                                   1169 	.area GSINIT5 (CODE)
                                   1170 	.area GSINIT  (CODE)
                                   1171 	.area GSFINAL (CODE)
                                   1172 	.area CSEG    (CODE)
                                   1173 ;--------------------------------------------------------
                                   1174 ; interrupt vector 
                                   1175 ;--------------------------------------------------------
                                   1176 	.area HOME    (CODE)
      000000                       1177 __interrupt_vect:
      000000 02 71 81         [24] 1178 	ljmp	__sdcc_gsinit_startup
      000003 32               [24] 1179 	reti
      000004                       1180 	.ds	7
      00000B 32               [24] 1181 	reti
      00000C                       1182 	.ds	7
      000013 32               [24] 1183 	reti
      000014                       1184 	.ds	7
      00001B 32               [24] 1185 	reti
      00001C                       1186 	.ds	7
      000023 32               [24] 1187 	reti
      000024                       1188 	.ds	7
      00002B 02 6C CE         [24] 1189 	ljmp	_clock_isr
      00002E                       1190 	.ds	5
      000033 02 88 FE         [24] 1191 	ljmp	_port_2_isr
      000036                       1192 	.ds	5
      00003B 32               [24] 1193 	reti
      00003C                       1194 	.ds	7
      000043 32               [24] 1195 	reti
      000044                       1196 	.ds	7
      00004B 02 6E 0A         [24] 1197 	ljmp	_rtimer_isr
                                   1198 ;--------------------------------------------------------
                                   1199 ; global & static initialisations
                                   1200 ;--------------------------------------------------------
                                   1201 	.area HOME    (CODE)
                                   1202 	.area GSINIT  (CODE)
                                   1203 	.area GSFINAL (CODE)
                                   1204 	.area GSINIT  (CODE)
                                   1205 	.globl __sdcc_gsinit_startup
                                   1206 	.globl __sdcc_program_startup
                                   1207 	.globl __start__stack
                                   1208 	.globl __mcs51_genXINIT
                                   1209 	.globl __mcs51_genXRAMCLEAR
                                   1210 	.globl __mcs51_genRAMCLEAR
                                   1211 	.area GSFINAL (CODE)
      007202 02 00 4E         [24] 1212 	ljmp	__sdcc_program_startup
                                   1213 ;--------------------------------------------------------
                                   1214 ; Home
                                   1215 ;--------------------------------------------------------
                                   1216 	.area HOME    (CODE)
                                   1217 	.area HOME    (CODE)
      00004E                       1218 __sdcc_program_startup:
      00004E 02 02 2E         [24] 1219 	ljmp	_main
                                   1220 ;	return from main will return to caller
                                   1221 ;--------------------------------------------------------
                                   1222 ; code
                                   1223 ;--------------------------------------------------------
                                   1224 	.area HOME    (CODE)
                                   1225 ;------------------------------------------------------------
                                   1226 ;Allocation info for local variables in function 'fade'
                                   1227 ;------------------------------------------------------------
                                   1228 ;l                         Allocated to stack - sp -5
                                   1229 ;i                         Allocated to stack - sp -3
                                   1230 ;a                         Allocated to stack - sp -1
                                   1231 ;k                         Allocated to registers r4 r5 
                                   1232 ;j                         Allocated to registers r2 r3 
                                   1233 ;------------------------------------------------------------
                                   1234 ;	../../../../platform/cc2530eb/./contiki-main.c:64: fade(int l) CC_NON_BANKED
                                   1235 ;	-----------------------------------------
                                   1236 ;	 function fade
                                   1237 ;	-----------------------------------------
      000051                       1238 _fade:
                           000007  1239 	ar7 = 0x07
                           000006  1240 	ar6 = 0x06
                           000005  1241 	ar5 = 0x05
                           000004  1242 	ar4 = 0x04
                           000003  1243 	ar3 = 0x03
                           000002  1244 	ar2 = 0x02
                           000001  1245 	ar1 = 0x01
                           000000  1246 	ar0 = 0x00
      000051 C0 82            [24] 1247 	push	dpl
      000053 C0 83            [24] 1248 	push	dph
      000055 E5 81            [12] 1249 	mov	a,sp
      000057 24 04            [12] 1250 	add	a,#0x04
      000059 F5 81            [12] 1251 	mov	sp,a
                                   1252 ;	../../../../platform/cc2530eb/./contiki-main.c:68: for(k = 0; k < 400; ++k) {
      00005B 7C 00            [12] 1253 	mov	r4,#0x00
      00005D 7D 00            [12] 1254 	mov	r5,#0x00
      00005F                       1255 00110$:
                                   1256 ;	../../../../platform/cc2530eb/./contiki-main.c:69: j = k > 200 ? 400 - k : k;
      00005F C3               [12] 1257 	clr	c
      000060 74 C8            [12] 1258 	mov	a,#0xC8
      000062 9C               [12] 1259 	subb	a,r4
      000063 E4               [12] 1260 	clr	a
      000064 64 80            [12] 1261 	xrl	a,#0x80
      000066 8D F0            [24] 1262 	mov	b,r5
      000068 63 F0 80         [24] 1263 	xrl	b,#0x80
      00006B 95 F0            [12] 1264 	subb	a,b
      00006D 50 0B            [24] 1265 	jnc	00114$
      00006F 74 90            [12] 1266 	mov	a,#0x90
      000071 C3               [12] 1267 	clr	c
      000072 9C               [12] 1268 	subb	a,r4
      000073 FA               [12] 1269 	mov	r2,a
      000074 74 01            [12] 1270 	mov	a,#0x01
      000076 9D               [12] 1271 	subb	a,r5
      000077 FB               [12] 1272 	mov	r3,a
      000078 80 04            [24] 1273 	sjmp	00115$
      00007A                       1274 00114$:
      00007A 8C 02            [24] 1275 	mov	ar2,r4
      00007C 8D 03            [24] 1276 	mov	ar3,r5
      00007E                       1277 00115$:
                                   1278 ;	../../../../platform/cc2530eb/./contiki-main.c:71: leds_on(l);
      00007E E5 81            [12] 1279 	mov	a,sp
      000080 24 FB            [12] 1280 	add	a,#0xfb
      000082 F8               [12] 1281 	mov	r0,a
      000083 86 07            [24] 1282 	mov	ar7,@r0
      000085 8F 82            [24] 1283 	mov	dpl,r7
      000087 C0 07            [24] 1284 	push	ar7
      000089 C0 05            [24] 1285 	push	ar5
      00008B C0 04            [24] 1286 	push	ar4
      00008D C0 03            [24] 1287 	push	ar3
      00008F C0 02            [24] 1288 	push	ar2
      000091 78 51            [12] 1289 	mov	r0,#_leds_on
      000093 79 83            [12] 1290 	mov	r1,#(_leds_on >> 8)
      000095 7A 04            [12] 1291 	mov	r2,#(_leds_on >> 16)
      000097 12 07 25         [24] 1292 	lcall	__sdcc_banked_call
      00009A D0 02            [24] 1293 	pop	ar2
      00009C D0 03            [24] 1294 	pop	ar3
      00009E D0 04            [24] 1295 	pop	ar4
      0000A0 D0 05            [24] 1296 	pop	ar5
      0000A2 D0 07            [24] 1297 	pop	ar7
                                   1298 ;	../../../../platform/cc2530eb/./contiki-main.c:72: for(i = 0; i < j; ++i) {
      0000A4 E5 81            [12] 1299 	mov	a,sp
      0000A6 24 FD            [12] 1300 	add	a,#0xfd
      0000A8 F8               [12] 1301 	mov	r0,a
      0000A9 E4               [12] 1302 	clr	a
      0000AA F6               [12] 1303 	mov	@r0,a
      0000AB 08               [12] 1304 	inc	r0
      0000AC F6               [12] 1305 	mov	@r0,a
      0000AD                       1306 00105$:
      0000AD E5 81            [12] 1307 	mov	a,sp
      0000AF 24 FD            [12] 1308 	add	a,#0xfd
      0000B1 F8               [12] 1309 	mov	r0,a
      0000B2 C3               [12] 1310 	clr	c
      0000B3 E6               [12] 1311 	mov	a,@r0
      0000B4 9A               [12] 1312 	subb	a,r2
      0000B5 08               [12] 1313 	inc	r0
      0000B6 E6               [12] 1314 	mov	a,@r0
      0000B7 64 80            [12] 1315 	xrl	a,#0x80
      0000B9 8B F0            [24] 1316 	mov	b,r3
      0000BB 63 F0 80         [24] 1317 	xrl	b,#0x80
      0000BE 95 F0            [12] 1318 	subb	a,b
      0000C0 50 1D            [24] 1319 	jnc	00101$
                                   1320 ;	../../../../platform/cc2530eb/./contiki-main.c:73: a = i;
      0000C2 E5 81            [12] 1321 	mov	a,sp
      0000C4 24 FD            [12] 1322 	add	a,#0xfd
      0000C6 F8               [12] 1323 	mov	r0,a
      0000C7 A9 81            [24] 1324 	mov	r1,sp
      0000C9 19               [12] 1325 	dec	r1
      0000CA E6               [12] 1326 	mov	a,@r0
      0000CB F7               [12] 1327 	mov	@r1,a
      0000CC 08               [12] 1328 	inc	r0
      0000CD 09               [12] 1329 	inc	r1
      0000CE E6               [12] 1330 	mov	a,@r0
      0000CF F7               [12] 1331 	mov	@r1,a
                                   1332 ;	../../../../platform/cc2530eb/./contiki-main.c:72: for(i = 0; i < j; ++i) {
      0000D0 E5 81            [12] 1333 	mov	a,sp
      0000D2 24 FD            [12] 1334 	add	a,#0xfd
      0000D4 F8               [12] 1335 	mov	r0,a
      0000D5 74 01            [12] 1336 	mov	a,#0x01
      0000D7 26               [12] 1337 	add	a,@r0
      0000D8 F6               [12] 1338 	mov	@r0,a
      0000D9 E4               [12] 1339 	clr	a
      0000DA 08               [12] 1340 	inc	r0
      0000DB 36               [12] 1341 	addc	a,@r0
      0000DC F6               [12] 1342 	mov	@r0,a
      0000DD 80 CE            [24] 1343 	sjmp	00105$
      0000DF                       1344 00101$:
                                   1345 ;	../../../../platform/cc2530eb/./contiki-main.c:75: leds_off(l);
      0000DF 8F 82            [24] 1346 	mov	dpl,r7
      0000E1 C0 05            [24] 1347 	push	ar5
      0000E3 C0 04            [24] 1348 	push	ar4
      0000E5 C0 03            [24] 1349 	push	ar3
      0000E7 C0 02            [24] 1350 	push	ar2
      0000E9 78 71            [12] 1351 	mov	r0,#_leds_off
      0000EB 79 83            [12] 1352 	mov	r1,#(_leds_off >> 8)
      0000ED 7A 04            [12] 1353 	mov	r2,#(_leds_off >> 16)
      0000EF 12 07 25         [24] 1354 	lcall	__sdcc_banked_call
      0000F2 D0 02            [24] 1355 	pop	ar2
      0000F4 D0 03            [24] 1356 	pop	ar3
      0000F6 D0 04            [24] 1357 	pop	ar4
      0000F8 D0 05            [24] 1358 	pop	ar5
                                   1359 ;	../../../../platform/cc2530eb/./contiki-main.c:76: for(i = 0; i < 200 - j; ++i) {
      0000FA E5 81            [12] 1360 	mov	a,sp
      0000FC 24 FD            [12] 1361 	add	a,#0xfd
      0000FE F8               [12] 1362 	mov	r0,a
      0000FF E4               [12] 1363 	clr	a
      000100 F6               [12] 1364 	mov	@r0,a
      000101 08               [12] 1365 	inc	r0
      000102 F6               [12] 1366 	mov	@r0,a
      000103 74 C8            [12] 1367 	mov	a,#0xC8
      000105 C3               [12] 1368 	clr	c
      000106 9A               [12] 1369 	subb	a,r2
      000107 FE               [12] 1370 	mov	r6,a
      000108 E4               [12] 1371 	clr	a
      000109 9B               [12] 1372 	subb	a,r3
      00010A FF               [12] 1373 	mov	r7,a
      00010B                       1374 00108$:
      00010B E5 81            [12] 1375 	mov	a,sp
      00010D 24 FD            [12] 1376 	add	a,#0xfd
      00010F F8               [12] 1377 	mov	r0,a
      000110 C3               [12] 1378 	clr	c
      000111 E6               [12] 1379 	mov	a,@r0
      000112 9E               [12] 1380 	subb	a,r6
      000113 08               [12] 1381 	inc	r0
      000114 E6               [12] 1382 	mov	a,@r0
      000115 64 80            [12] 1383 	xrl	a,#0x80
      000117 8F F0            [24] 1384 	mov	b,r7
      000119 63 F0 80         [24] 1385 	xrl	b,#0x80
      00011C 95 F0            [12] 1386 	subb	a,b
      00011E 50 1D            [24] 1387 	jnc	00111$
                                   1388 ;	../../../../platform/cc2530eb/./contiki-main.c:77: a = i;
      000120 E5 81            [12] 1389 	mov	a,sp
      000122 24 FD            [12] 1390 	add	a,#0xfd
      000124 F8               [12] 1391 	mov	r0,a
      000125 A9 81            [24] 1392 	mov	r1,sp
      000127 19               [12] 1393 	dec	r1
      000128 E6               [12] 1394 	mov	a,@r0
      000129 F7               [12] 1395 	mov	@r1,a
      00012A 08               [12] 1396 	inc	r0
      00012B 09               [12] 1397 	inc	r1
      00012C E6               [12] 1398 	mov	a,@r0
      00012D F7               [12] 1399 	mov	@r1,a
                                   1400 ;	../../../../platform/cc2530eb/./contiki-main.c:76: for(i = 0; i < 200 - j; ++i) {
      00012E E5 81            [12] 1401 	mov	a,sp
      000130 24 FD            [12] 1402 	add	a,#0xfd
      000132 F8               [12] 1403 	mov	r0,a
      000133 74 01            [12] 1404 	mov	a,#0x01
      000135 26               [12] 1405 	add	a,@r0
      000136 F6               [12] 1406 	mov	@r0,a
      000137 E4               [12] 1407 	clr	a
      000138 08               [12] 1408 	inc	r0
      000139 36               [12] 1409 	addc	a,@r0
      00013A F6               [12] 1410 	mov	@r0,a
      00013B 80 CE            [24] 1411 	sjmp	00108$
      00013D                       1412 00111$:
                                   1413 ;	../../../../platform/cc2530eb/./contiki-main.c:68: for(k = 0; k < 400; ++k) {
      00013D 0C               [12] 1414 	inc	r4
      00013E BC 00 01         [24] 1415 	cjne	r4,#0x00,00138$
      000141 0D               [12] 1416 	inc	r5
      000142                       1417 00138$:
      000142 C3               [12] 1418 	clr	c
      000143 EC               [12] 1419 	mov	a,r4
      000144 94 90            [12] 1420 	subb	a,#0x90
      000146 ED               [12] 1421 	mov	a,r5
      000147 64 80            [12] 1422 	xrl	a,#0x80
      000149 94 81            [12] 1423 	subb	a,#0x81
      00014B 50 03            [24] 1424 	jnc	00139$
      00014D 02 00 5F         [24] 1425 	ljmp	00110$
      000150                       1426 00139$:
      000150 E5 81            [12] 1427 	mov	a,sp
      000152 24 FA            [12] 1428 	add	a,#0xFA
      000154 F5 81            [12] 1429 	mov	sp,a
      000156 22               [24] 1430 	ret
                                   1431 ;------------------------------------------------------------
                                   1432 ;Allocation info for local variables in function 'set_rime_addr'
                                   1433 ;------------------------------------------------------------
                                   1434 ;i                         Allocated to registers r5 
                                   1435 ;macp                      Allocated to registers 
                                   1436 ;------------------------------------------------------------
                                   1437 ;	../../../../platform/cc2530eb/./contiki-main.c:83: set_rime_addr(void) CC_NON_BANKED
                                   1438 ;	-----------------------------------------
                                   1439 ;	 function set_rime_addr
                                   1440 ;	-----------------------------------------
      000157                       1441 _set_rime_addr:
                                   1442 ;	../../../../platform/cc2530eb/./contiki-main.c:88: __xdata unsigned char *macp = &X_IEEE_ADDR;
                                   1443 ;	../../../../platform/cc2530eb/./contiki-main.c:93: PUTSTRING("Rime is 0x");
      000157 90 7C CF         [24] 1444 	mov	dptr,#__str_0
      00015A 75 F0 80         [24] 1445 	mov	b,#0x80
      00015D 78 8E            [12] 1446 	mov	r0,#_putstring
      00015F 79 89            [12] 1447 	mov	r1,#(_putstring >> 8)
      000161 7A 04            [12] 1448 	mov	r2,#(_putstring >> 16)
      000163 12 07 25         [24] 1449 	lcall	__sdcc_banked_call
                                   1450 ;	../../../../platform/cc2530eb/./contiki-main.c:94: PUTHEX(sizeof(rimeaddr_t));
      000166 75 82 08         [24] 1451 	mov	dpl,#0x08
      000169 78 C1            [12] 1452 	mov	r0,#_puthex
      00016B 79 89            [12] 1453 	mov	r1,#(_puthex >> 8)
      00016D 7A 04            [12] 1454 	mov	r2,#(_puthex >> 16)
      00016F 12 07 25         [24] 1455 	lcall	__sdcc_banked_call
                                   1456 ;	../../../../platform/cc2530eb/./contiki-main.c:95: PUTSTRING(" bytes long\n\r");
      000172 90 7C DA         [24] 1457 	mov	dptr,#__str_1
      000175 75 F0 80         [24] 1458 	mov	b,#0x80
      000178 78 8E            [12] 1459 	mov	r0,#_putstring
      00017A 79 89            [12] 1460 	mov	r1,#(_putstring >> 8)
      00017C 7A 04            [12] 1461 	mov	r2,#(_putstring >> 16)
      00017E 12 07 25         [24] 1462 	lcall	__sdcc_banked_call
                                   1463 ;	../../../../platform/cc2530eb/./contiki-main.c:98: PUTSTRING("Reading MAC from Info Page\n\r");
      000181 90 7C E8         [24] 1464 	mov	dptr,#__str_2
      000184 75 F0 80         [24] 1465 	mov	b,#0x80
      000187 78 8E            [12] 1466 	mov	r0,#_putstring
      000189 79 89            [12] 1467 	mov	r1,#(_putstring >> 8)
      00018B 7A 04            [12] 1468 	mov	r2,#(_putstring >> 16)
      00018D 12 07 25         [24] 1469 	lcall	__sdcc_banked_call
                                   1470 ;	../../../../platform/cc2530eb/./contiki-main.c:118: for(i = (RIMEADDR_SIZE - 1); i >= 0; --i) {
      000190 7E 0C            [12] 1471 	mov	r6,#_X_IEEE_ADDR
      000192 7F 78            [12] 1472 	mov	r7,#(_X_IEEE_ADDR >> 8)
      000194 7D 07            [12] 1473 	mov	r5,#0x07
      000196                       1474 00103$:
                                   1475 ;	../../../../platform/cc2530eb/./contiki-main.c:119: rimeaddr_node_addr.u8[i] = *macp;
      000196 ED               [12] 1476 	mov	a,r5
      000197 24 78            [12] 1477 	add	a,#_rimeaddr_node_addr
      000199 FB               [12] 1478 	mov	r3,a
      00019A E4               [12] 1479 	clr	a
      00019B 34 16            [12] 1480 	addc	a,#(_rimeaddr_node_addr >> 8)
      00019D FC               [12] 1481 	mov	r4,a
      00019E 8E 82            [24] 1482 	mov	dpl,r6
      0001A0 8F 83            [24] 1483 	mov	dph,r7
      0001A2 E0               [24] 1484 	movx	a,@dptr
      0001A3 FA               [12] 1485 	mov	r2,a
      0001A4 A3               [24] 1486 	inc	dptr
      0001A5 AE 82            [24] 1487 	mov	r6,dpl
      0001A7 AF 83            [24] 1488 	mov	r7,dph
      0001A9 8B 82            [24] 1489 	mov	dpl,r3
      0001AB 8C 83            [24] 1490 	mov	dph,r4
      0001AD EA               [12] 1491 	mov	a,r2
      0001AE F0               [24] 1492 	movx	@dptr,a
                                   1493 ;	../../../../platform/cc2530eb/./contiki-main.c:120: macp++;
                                   1494 ;	../../../../platform/cc2530eb/./contiki-main.c:118: for(i = (RIMEADDR_SIZE - 1); i >= 0; --i) {
      0001AF 1D               [12] 1495 	dec	r5
      0001B0 ED               [12] 1496 	mov	a,r5
      0001B1 30 E7 E2         [24] 1497 	jnb	acc.7,00103$
                                   1498 ;	../../../../platform/cc2530eb/./contiki-main.c:131: PUTSTRING("Rime configured with address ");
      0001B4 90 7D 05         [24] 1499 	mov	dptr,#__str_3
      0001B7 75 F0 80         [24] 1500 	mov	b,#0x80
      0001BA 78 8E            [12] 1501 	mov	r0,#_putstring
      0001BC 79 89            [12] 1502 	mov	r1,#(_putstring >> 8)
      0001BE 7A 04            [12] 1503 	mov	r2,#(_putstring >> 16)
      0001C0 12 07 25         [24] 1504 	lcall	__sdcc_banked_call
                                   1505 ;	../../../../platform/cc2530eb/./contiki-main.c:132: for(i = 0; i < RIMEADDR_SIZE - 1; i++) {
      0001C3 7F 00            [12] 1506 	mov	r7,#0x00
      0001C5                       1507 00105$:
                                   1508 ;	../../../../platform/cc2530eb/./contiki-main.c:133: PUTHEX(rimeaddr_node_addr.u8[i]);
      0001C5 EF               [12] 1509 	mov	a,r7
      0001C6 24 78            [12] 1510 	add	a,#_rimeaddr_node_addr
      0001C8 F5 82            [12] 1511 	mov	dpl,a
      0001CA E4               [12] 1512 	clr	a
      0001CB 34 16            [12] 1513 	addc	a,#(_rimeaddr_node_addr >> 8)
      0001CD F5 83            [12] 1514 	mov	dph,a
      0001CF E0               [24] 1515 	movx	a,@dptr
      0001D0 F5 82            [12] 1516 	mov	dpl,a
      0001D2 C0 07            [24] 1517 	push	ar7
      0001D4 78 C1            [12] 1518 	mov	r0,#_puthex
      0001D6 79 89            [12] 1519 	mov	r1,#(_puthex >> 8)
      0001D8 7A 04            [12] 1520 	mov	r2,#(_puthex >> 16)
      0001DA 12 07 25         [24] 1521 	lcall	__sdcc_banked_call
                                   1522 ;	../../../../platform/cc2530eb/./contiki-main.c:134: PUTCHAR(':');
      0001DD 75 82 3A         [24] 1523 	mov	dpl,#0x3A
      0001E0 78 76            [12] 1524 	mov	r0,#_putchar
      0001E2 79 6B            [12] 1525 	mov	r1,#(_putchar >> 8)
      0001E4 7A 00            [12] 1526 	mov	r2,#(_putchar >> 16)
      0001E6 12 07 25         [24] 1527 	lcall	__sdcc_banked_call
      0001E9 D0 07            [24] 1528 	pop	ar7
                                   1529 ;	../../../../platform/cc2530eb/./contiki-main.c:132: for(i = 0; i < RIMEADDR_SIZE - 1; i++) {
      0001EB 0F               [12] 1530 	inc	r7
      0001EC C3               [12] 1531 	clr	c
      0001ED EF               [12] 1532 	mov	a,r7
      0001EE 64 80            [12] 1533 	xrl	a,#0x80
      0001F0 94 87            [12] 1534 	subb	a,#0x87
      0001F2 40 D1            [24] 1535 	jc	00105$
                                   1536 ;	../../../../platform/cc2530eb/./contiki-main.c:136: PUTHEX(rimeaddr_node_addr.u8[i]);
      0001F4 EF               [12] 1537 	mov	a,r7
      0001F5 24 78            [12] 1538 	add	a,#_rimeaddr_node_addr
      0001F7 F5 82            [12] 1539 	mov	dpl,a
      0001F9 E4               [12] 1540 	clr	a
      0001FA 34 16            [12] 1541 	addc	a,#(_rimeaddr_node_addr >> 8)
      0001FC F5 83            [12] 1542 	mov	dph,a
      0001FE E0               [24] 1543 	movx	a,@dptr
      0001FF F5 82            [12] 1544 	mov	dpl,a
      000201 78 C1            [12] 1545 	mov	r0,#_puthex
      000203 79 89            [12] 1546 	mov	r1,#(_puthex >> 8)
      000205 7A 04            [12] 1547 	mov	r2,#(_puthex >> 16)
      000207 12 07 25         [24] 1548 	lcall	__sdcc_banked_call
                                   1549 ;	../../../../platform/cc2530eb/./contiki-main.c:137: PUTCHAR('\n');
      00020A 75 82 0A         [24] 1550 	mov	dpl,#0x0A
      00020D 78 76            [12] 1551 	mov	r0,#_putchar
      00020F 79 6B            [12] 1552 	mov	r1,#(_putchar >> 8)
      000211 7A 00            [12] 1553 	mov	r2,#(_putchar >> 16)
      000213 12 07 25         [24] 1554 	lcall	__sdcc_banked_call
                                   1555 ;	../../../../platform/cc2530eb/./contiki-main.c:138: PUTCHAR('\r');
      000216 75 82 0D         [24] 1556 	mov	dpl,#0x0D
      000219 78 76            [12] 1557 	mov	r0,#_putchar
      00021B 79 6B            [12] 1558 	mov	r1,#(_putchar >> 8)
      00021D 7A 00            [12] 1559 	mov	r2,#(_putchar >> 16)
      00021F 12 07 25         [24] 1560 	lcall	__sdcc_banked_call
                                   1561 ;	../../../../platform/cc2530eb/./contiki-main.c:141: cc2530_rf_set_addr(IEEE802154_PANID);
      000222 90 54 49         [24] 1562 	mov	dptr,#0x5449
      000225 78 9F            [12] 1563 	mov	r0,#_cc2530_rf_set_addr
      000227 79 A9            [12] 1564 	mov	r1,#(_cc2530_rf_set_addr >> 8)
      000229 7A 03            [12] 1565 	mov	r2,#(_cc2530_rf_set_addr >> 16)
                                   1566 ;	../../../../platform/cc2530eb/./contiki-main.c:142: return;
      00022B 02 07 25         [24] 1567 	ljmp	__sdcc_banked_call
                                   1568 ;------------------------------------------------------------
                                   1569 ;Allocation info for local variables in function 'main'
                                   1570 ;------------------------------------------------------------
                                   1571 ;r                         Allocated to registers r6 
                                   1572 ;------------------------------------------------------------
                                   1573 ;	../../../../platform/cc2530eb/./contiki-main.c:146: main(void) CC_NON_BANKED
                                   1574 ;	-----------------------------------------
                                   1575 ;	 function main
                                   1576 ;	-----------------------------------------
      00022E                       1577 _main:
                                   1578 ;	../../../../platform/cc2530eb/./contiki-main.c:149: clock_init();
      00022E 78 FF            [12] 1579 	mov	r0,#_clock_init
      000230 79 6B            [12] 1580 	mov	r1,#(_clock_init >> 8)
      000232 7A 00            [12] 1581 	mov	r2,#(_clock_init >> 16)
      000234 12 07 25         [24] 1582 	lcall	__sdcc_banked_call
                                   1583 ;	../../../../platform/cc2530eb/./contiki-main.c:150: soc_init();
      000237 78 70            [12] 1584 	mov	r0,#_soc_init
      000239 79 EE            [12] 1585 	mov	r1,#(_soc_init >> 8)
      00023B 7A 02            [12] 1586 	mov	r2,#(_soc_init >> 16)
      00023D 12 07 25         [24] 1587 	lcall	__sdcc_banked_call
                                   1588 ;	../../../../platform/cc2530eb/./contiki-main.c:151: rtimer_init();
      000240 78 DF            [12] 1589 	mov	r0,#_rtimer_init
      000242 79 83            [12] 1590 	mov	r1,#(_rtimer_init >> 8)
      000244 7A 04            [12] 1591 	mov	r2,#(_rtimer_init >> 16)
      000246 12 07 25         [24] 1592 	lcall	__sdcc_banked_call
                                   1593 ;	../../../../platform/cc2530eb/./contiki-main.c:156: leds_init();
      000249 78 F7            [12] 1594 	mov	r0,#_leds_init
      00024B 79 82            [12] 1595 	mov	r1,#(_leds_init >> 8)
      00024D 7A 04            [12] 1596 	mov	r2,#(_leds_init >> 16)
      00024F 12 07 25         [24] 1597 	lcall	__sdcc_banked_call
                                   1598 ;	../../../../platform/cc2530eb/./contiki-main.c:157: leds_off(LEDS_ALL);
      000252 75 82 0F         [24] 1599 	mov	dpl,#0x0F
      000255 78 71            [12] 1600 	mov	r0,#_leds_off
      000257 79 83            [12] 1601 	mov	r1,#(_leds_off >> 8)
      000259 7A 04            [12] 1602 	mov	r2,#(_leds_off >> 16)
      00025B 12 07 25         [24] 1603 	lcall	__sdcc_banked_call
                                   1604 ;	../../../../platform/cc2530eb/./contiki-main.c:158: fade(LEDS_GREEN);
      00025E 90 00 01         [24] 1605 	mov	dptr,#0x0001
      000261 12 00 51         [24] 1606 	lcall	_fade
                                   1607 ;	../../../../platform/cc2530eb/./contiki-main.c:161: process_init();
      000264 78 47            [12] 1608 	mov	r0,#_process_init
      000266 79 86            [12] 1609 	mov	r1,#(_process_init >> 8)
      000268 7A 03            [12] 1610 	mov	r2,#(_process_init >> 16)
      00026A 12 07 25         [24] 1611 	lcall	__sdcc_banked_call
                                   1612 ;	../../../../platform/cc2530eb/./contiki-main.c:167: io_arch_init();
      00026D 78 AB            [12] 1613 	mov	r0,#_uart0_init
      00026F 79 AB            [12] 1614 	mov	r1,#(_uart0_init >> 8)
      000271 7A 02            [12] 1615 	mov	r2,#(_uart0_init >> 16)
      000273 12 07 25         [24] 1616 	lcall	__sdcc_banked_call
                                   1617 ;	../../../../platform/cc2530eb/./contiki-main.c:172: io_arch_set_input(serial_line_input_byte);
      000276 90 85 7F         [24] 1618 	mov	dptr,#_serial_line_input_byte
      000279 75 F0 04         [24] 1619 	mov	b,#(_serial_line_input_byte >> 16)
      00027C 78 12            [12] 1620 	mov	r0,#_uart0_set_input
      00027E 79 07            [12] 1621 	mov	r1,#(_uart0_set_input >> 8)
      000280 7A 00            [12] 1622 	mov	r2,#(_uart0_set_input >> 16)
      000282 12 07 25         [24] 1623 	lcall	__sdcc_banked_call
                                   1624 ;	../../../../platform/cc2530eb/./contiki-main.c:173: serial_line_init();
      000285 78 B4            [12] 1625 	mov	r0,#_serial_line_init
      000287 79 87            [12] 1626 	mov	r1,#(_serial_line_init >> 8)
      000289 7A 04            [12] 1627 	mov	r2,#(_serial_line_init >> 16)
      00028B 12 07 25         [24] 1628 	lcall	__sdcc_banked_call
                                   1629 ;	../../../../platform/cc2530eb/./contiki-main.c:175: fade(LEDS_RED);
      00028E 90 00 02         [24] 1630 	mov	dptr,#0x0002
      000291 12 00 51         [24] 1631 	lcall	_fade
                                   1632 ;	../../../../platform/cc2530eb/./contiki-main.c:177: PUTSTRING("##########################################\n\r");
      000294 90 7D 23         [24] 1633 	mov	dptr,#__str_4
      000297 75 F0 80         [24] 1634 	mov	b,#0x80
      00029A 78 8E            [12] 1635 	mov	r0,#_putstring
      00029C 79 89            [12] 1636 	mov	r1,#(_putstring >> 8)
      00029E 7A 04            [12] 1637 	mov	r2,#(_putstring >> 16)
      0002A0 12 07 25         [24] 1638 	lcall	__sdcc_banked_call
                                   1639 ;	../../../../platform/cc2530eb/./contiki-main.c:178: putstring(CONTIKI_VERSION_STRING "\n\r");
      0002A3 90 7D 50         [24] 1640 	mov	dptr,#__str_5
      0002A6 75 F0 80         [24] 1641 	mov	b,#0x80
      0002A9 78 8E            [12] 1642 	mov	r0,#_putstring
      0002AB 79 89            [12] 1643 	mov	r1,#(_putstring >> 8)
      0002AD 7A 04            [12] 1644 	mov	r2,#(_putstring >> 16)
      0002AF 12 07 25         [24] 1645 	lcall	__sdcc_banked_call
                                   1646 ;	../../../../platform/cc2530eb/./contiki-main.c:179: putstring(MODEL_STRING);
      0002B2 90 7D 5E         [24] 1647 	mov	dptr,#__str_6
      0002B5 75 F0 80         [24] 1648 	mov	b,#0x80
      0002B8 78 8E            [12] 1649 	mov	r0,#_putstring
      0002BA 79 89            [12] 1650 	mov	r1,#(_putstring >> 8)
      0002BC 7A 04            [12] 1651 	mov	r2,#(_putstring >> 16)
      0002BE 12 07 25         [24] 1652 	lcall	__sdcc_banked_call
                                   1653 ;	../../../../platform/cc2530eb/./contiki-main.c:180: switch(CHIPID) {
      0002C1 90 62 4A         [24] 1654 	mov	dptr,#_CHIPID
      0002C4 E0               [24] 1655 	movx	a,@dptr
      0002C5 FF               [12] 1656 	mov	r7,a
      0002C6 BF 8D 02         [24] 1657 	cjne	r7,#0x8D,00158$
      0002C9 80 42            [24] 1658 	sjmp	00104$
      0002CB                       1659 00158$:
      0002CB BF 95 02         [24] 1660 	cjne	r7,#0x95,00159$
      0002CE 80 2C            [24] 1661 	sjmp	00103$
      0002D0                       1662 00159$:
      0002D0 BF A5 02         [24] 1663 	cjne	r7,#0xA5,00160$
      0002D3 80 05            [24] 1664 	sjmp	00101$
      0002D5                       1665 00160$:
                                   1666 ;	../../../../platform/cc2530eb/./contiki-main.c:181: case 0xA5:
      0002D5 BF B5 44         [24] 1667 	cjne	r7,#0xB5,00105$
      0002D8 80 11            [24] 1668 	sjmp	00102$
      0002DA                       1669 00101$:
                                   1670 ;	../../../../platform/cc2530eb/./contiki-main.c:182: putstring("cc2530");
      0002DA 90 7D 70         [24] 1671 	mov	dptr,#__str_7
      0002DD 75 F0 80         [24] 1672 	mov	b,#0x80
      0002E0 78 8E            [12] 1673 	mov	r0,#_putstring
      0002E2 79 89            [12] 1674 	mov	r1,#(_putstring >> 8)
      0002E4 7A 04            [12] 1675 	mov	r2,#(_putstring >> 16)
      0002E6 12 07 25         [24] 1676 	lcall	__sdcc_banked_call
                                   1677 ;	../../../../platform/cc2530eb/./contiki-main.c:183: break;
                                   1678 ;	../../../../platform/cc2530eb/./contiki-main.c:184: case 0xB5:
      0002E9 80 31            [24] 1679 	sjmp	00105$
      0002EB                       1680 00102$:
                                   1681 ;	../../../../platform/cc2530eb/./contiki-main.c:185: putstring("cc2531");
      0002EB 90 7D 77         [24] 1682 	mov	dptr,#__str_8
      0002EE 75 F0 80         [24] 1683 	mov	b,#0x80
      0002F1 78 8E            [12] 1684 	mov	r0,#_putstring
      0002F3 79 89            [12] 1685 	mov	r1,#(_putstring >> 8)
      0002F5 7A 04            [12] 1686 	mov	r2,#(_putstring >> 16)
      0002F7 12 07 25         [24] 1687 	lcall	__sdcc_banked_call
                                   1688 ;	../../../../platform/cc2530eb/./contiki-main.c:186: break;
                                   1689 ;	../../../../platform/cc2530eb/./contiki-main.c:187: case 0x95:
      0002FA 80 20            [24] 1690 	sjmp	00105$
      0002FC                       1691 00103$:
                                   1692 ;	../../../../platform/cc2530eb/./contiki-main.c:188: putstring("cc2533");
      0002FC 90 7D 7E         [24] 1693 	mov	dptr,#__str_9
      0002FF 75 F0 80         [24] 1694 	mov	b,#0x80
      000302 78 8E            [12] 1695 	mov	r0,#_putstring
      000304 79 89            [12] 1696 	mov	r1,#(_putstring >> 8)
      000306 7A 04            [12] 1697 	mov	r2,#(_putstring >> 16)
      000308 12 07 25         [24] 1698 	lcall	__sdcc_banked_call
                                   1699 ;	../../../../platform/cc2530eb/./contiki-main.c:189: break;
                                   1700 ;	../../../../platform/cc2530eb/./contiki-main.c:190: case 0x8D:
      00030B 80 0F            [24] 1701 	sjmp	00105$
      00030D                       1702 00104$:
                                   1703 ;	../../../../platform/cc2530eb/./contiki-main.c:191: putstring("cc2540");
      00030D 90 7D 85         [24] 1704 	mov	dptr,#__str_10
      000310 75 F0 80         [24] 1705 	mov	b,#0x80
      000313 78 8E            [12] 1706 	mov	r0,#_putstring
      000315 79 89            [12] 1707 	mov	r1,#(_putstring >> 8)
      000317 7A 04            [12] 1708 	mov	r2,#(_putstring >> 16)
      000319 12 07 25         [24] 1709 	lcall	__sdcc_banked_call
                                   1710 ;	../../../../platform/cc2530eb/./contiki-main.c:193: }
      00031C                       1711 00105$:
                                   1712 ;	../../../../platform/cc2530eb/./contiki-main.c:195: putstring("-" CC2530_FLAVOR_STRING ", ");
      00031C 90 7D 8C         [24] 1713 	mov	dptr,#__str_11
      00031F 75 F0 80         [24] 1714 	mov	b,#0x80
      000322 78 8E            [12] 1715 	mov	r0,#_putstring
      000324 79 89            [12] 1716 	mov	r1,#(_putstring >> 8)
      000326 7A 04            [12] 1717 	mov	r2,#(_putstring >> 16)
      000328 12 07 25         [24] 1718 	lcall	__sdcc_banked_call
                                   1719 ;	../../../../platform/cc2530eb/./contiki-main.c:196: puthex(CHIPINFO1 + 1);
      00032B 90 62 77         [24] 1720 	mov	dptr,#_CHIPINFO1
      00032E E0               [24] 1721 	movx	a,@dptr
      00032F FF               [12] 1722 	mov	r7,a
      000330 0F               [12] 1723 	inc	r7
      000331 8F 82            [24] 1724 	mov	dpl,r7
      000333 78 C1            [12] 1725 	mov	r0,#_puthex
      000335 79 89            [12] 1726 	mov	r1,#(_puthex >> 8)
      000337 7A 04            [12] 1727 	mov	r2,#(_puthex >> 16)
      000339 12 07 25         [24] 1728 	lcall	__sdcc_banked_call
                                   1729 ;	../../../../platform/cc2530eb/./contiki-main.c:197: putstring("KB SRAM\n\r");
      00033C 90 7D 94         [24] 1730 	mov	dptr,#__str_12
      00033F 75 F0 80         [24] 1731 	mov	b,#0x80
      000342 78 8E            [12] 1732 	mov	r0,#_putstring
      000344 79 89            [12] 1733 	mov	r1,#(_putstring >> 8)
      000346 7A 04            [12] 1734 	mov	r2,#(_putstring >> 16)
      000348 12 07 25         [24] 1735 	lcall	__sdcc_banked_call
                                   1736 ;	../../../../platform/cc2530eb/./contiki-main.c:199: PUTSTRING("\nSDCC Build:\n\r");
      00034B 90 7D 9E         [24] 1737 	mov	dptr,#__str_13
      00034E 75 F0 80         [24] 1738 	mov	b,#0x80
      000351 78 8E            [12] 1739 	mov	r0,#_putstring
      000353 79 89            [12] 1740 	mov	r1,#(_putstring >> 8)
      000355 7A 04            [12] 1741 	mov	r2,#(_putstring >> 16)
      000357 12 07 25         [24] 1742 	lcall	__sdcc_banked_call
                                   1743 ;	../../../../platform/cc2530eb/./contiki-main.c:202: PUTSTRING("  With Banking.\n\r");
      00035A 90 7D AD         [24] 1744 	mov	dptr,#__str_14
      00035D 75 F0 80         [24] 1745 	mov	b,#0x80
      000360 78 8E            [12] 1746 	mov	r0,#_putstring
      000362 79 89            [12] 1747 	mov	r1,#(_putstring >> 8)
      000364 7A 04            [12] 1748 	mov	r2,#(_putstring >> 16)
      000366 12 07 25         [24] 1749 	lcall	__sdcc_banked_call
                                   1750 ;	../../../../platform/cc2530eb/./contiki-main.c:214: PUTCHAR('\n');
      000369 75 82 0A         [24] 1751 	mov	dpl,#0x0A
      00036C 78 76            [12] 1752 	mov	r0,#_putchar
      00036E 79 6B            [12] 1753 	mov	r1,#(_putchar >> 8)
      000370 7A 00            [12] 1754 	mov	r2,#(_putchar >> 16)
      000372 12 07 25         [24] 1755 	lcall	__sdcc_banked_call
                                   1756 ;	../../../../platform/cc2530eb/./contiki-main.c:215: PUTCHAR('\r');
      000375 75 82 0D         [24] 1757 	mov	dpl,#0x0D
      000378 78 76            [12] 1758 	mov	r0,#_putchar
      00037A 79 6B            [12] 1759 	mov	r1,#(_putchar >> 8)
      00037C 7A 00            [12] 1760 	mov	r2,#(_putchar >> 16)
      00037E 12 07 25         [24] 1761 	lcall	__sdcc_banked_call
                                   1762 ;	../../../../platform/cc2530eb/./contiki-main.c:217: PUTSTRING(" Net: ");
      000381 90 7D BF         [24] 1763 	mov	dptr,#__str_15
      000384 75 F0 80         [24] 1764 	mov	b,#0x80
      000387 78 8E            [12] 1765 	mov	r0,#_putstring
      000389 79 89            [12] 1766 	mov	r1,#(_putstring >> 8)
      00038B 7A 04            [12] 1767 	mov	r2,#(_putstring >> 16)
      00038D 12 07 25         [24] 1768 	lcall	__sdcc_banked_call
                                   1769 ;	../../../../platform/cc2530eb/./contiki-main.c:218: PUTSTRING(NETSTACK_NETWORK.name);
      000390 90 7E 2F         [24] 1770 	mov	dptr,#_sicslowpan_driver
      000393 E4               [12] 1771 	clr	a
      000394 93               [24] 1772 	movc	a,@a+dptr
      000395 FD               [12] 1773 	mov	r5,a
      000396 A3               [24] 1774 	inc	dptr
      000397 E4               [12] 1775 	clr	a
      000398 93               [24] 1776 	movc	a,@a+dptr
      000399 FE               [12] 1777 	mov	r6,a
      00039A A3               [24] 1778 	inc	dptr
      00039B E4               [12] 1779 	clr	a
      00039C 93               [24] 1780 	movc	a,@a+dptr
      00039D FF               [12] 1781 	mov	r7,a
      00039E 8D 82            [24] 1782 	mov	dpl,r5
      0003A0 8E 83            [24] 1783 	mov	dph,r6
      0003A2 8F F0            [24] 1784 	mov	b,r7
      0003A4 78 8E            [12] 1785 	mov	r0,#_putstring
      0003A6 79 89            [12] 1786 	mov	r1,#(_putstring >> 8)
      0003A8 7A 04            [12] 1787 	mov	r2,#(_putstring >> 16)
      0003AA 12 07 25         [24] 1788 	lcall	__sdcc_banked_call
                                   1789 ;	../../../../platform/cc2530eb/./contiki-main.c:219: PUTCHAR('\n');
      0003AD 75 82 0A         [24] 1790 	mov	dpl,#0x0A
      0003B0 78 76            [12] 1791 	mov	r0,#_putchar
      0003B2 79 6B            [12] 1792 	mov	r1,#(_putchar >> 8)
      0003B4 7A 00            [12] 1793 	mov	r2,#(_putchar >> 16)
      0003B6 12 07 25         [24] 1794 	lcall	__sdcc_banked_call
                                   1795 ;	../../../../platform/cc2530eb/./contiki-main.c:220: PUTCHAR('\r');
      0003B9 75 82 0D         [24] 1796 	mov	dpl,#0x0D
      0003BC 78 76            [12] 1797 	mov	r0,#_putchar
      0003BE 79 6B            [12] 1798 	mov	r1,#(_putchar >> 8)
      0003C0 7A 00            [12] 1799 	mov	r2,#(_putchar >> 16)
      0003C2 12 07 25         [24] 1800 	lcall	__sdcc_banked_call
                                   1801 ;	../../../../platform/cc2530eb/./contiki-main.c:221: PUTSTRING(" MAC: ");
      0003C5 90 7D C6         [24] 1802 	mov	dptr,#__str_16
      0003C8 75 F0 80         [24] 1803 	mov	b,#0x80
      0003CB 78 8E            [12] 1804 	mov	r0,#_putstring
      0003CD 79 89            [12] 1805 	mov	r1,#(_putstring >> 8)
      0003CF 7A 04            [12] 1806 	mov	r2,#(_putstring >> 16)
      0003D1 12 07 25         [24] 1807 	lcall	__sdcc_banked_call
                                   1808 ;	../../../../platform/cc2530eb/./contiki-main.c:222: PUTSTRING(NETSTACK_MAC.name);
      0003D4 90 7E 62         [24] 1809 	mov	dptr,#_csma_driver
      0003D7 E4               [12] 1810 	clr	a
      0003D8 93               [24] 1811 	movc	a,@a+dptr
      0003D9 FD               [12] 1812 	mov	r5,a
      0003DA A3               [24] 1813 	inc	dptr
      0003DB E4               [12] 1814 	clr	a
      0003DC 93               [24] 1815 	movc	a,@a+dptr
      0003DD FE               [12] 1816 	mov	r6,a
      0003DE A3               [24] 1817 	inc	dptr
      0003DF E4               [12] 1818 	clr	a
      0003E0 93               [24] 1819 	movc	a,@a+dptr
      0003E1 FF               [12] 1820 	mov	r7,a
      0003E2 8D 82            [24] 1821 	mov	dpl,r5
      0003E4 8E 83            [24] 1822 	mov	dph,r6
      0003E6 8F F0            [24] 1823 	mov	b,r7
      0003E8 78 8E            [12] 1824 	mov	r0,#_putstring
      0003EA 79 89            [12] 1825 	mov	r1,#(_putstring >> 8)
      0003EC 7A 04            [12] 1826 	mov	r2,#(_putstring >> 16)
      0003EE 12 07 25         [24] 1827 	lcall	__sdcc_banked_call
                                   1828 ;	../../../../platform/cc2530eb/./contiki-main.c:223: PUTCHAR('\n');
      0003F1 75 82 0A         [24] 1829 	mov	dpl,#0x0A
      0003F4 78 76            [12] 1830 	mov	r0,#_putchar
      0003F6 79 6B            [12] 1831 	mov	r1,#(_putchar >> 8)
      0003F8 7A 00            [12] 1832 	mov	r2,#(_putchar >> 16)
      0003FA 12 07 25         [24] 1833 	lcall	__sdcc_banked_call
                                   1834 ;	../../../../platform/cc2530eb/./contiki-main.c:224: PUTCHAR('\r');
      0003FD 75 82 0D         [24] 1835 	mov	dpl,#0x0D
      000400 78 76            [12] 1836 	mov	r0,#_putchar
      000402 79 6B            [12] 1837 	mov	r1,#(_putchar >> 8)
      000404 7A 00            [12] 1838 	mov	r2,#(_putchar >> 16)
      000406 12 07 25         [24] 1839 	lcall	__sdcc_banked_call
                                   1840 ;	../../../../platform/cc2530eb/./contiki-main.c:225: PUTSTRING(" RDC: ");
      000409 90 7D CD         [24] 1841 	mov	dptr,#__str_17
      00040C 75 F0 80         [24] 1842 	mov	b,#0x80
      00040F 78 8E            [12] 1843 	mov	r0,#_putstring
      000411 79 89            [12] 1844 	mov	r1,#(_putstring >> 8)
      000413 7A 04            [12] 1845 	mov	r2,#(_putstring >> 16)
      000415 12 07 25         [24] 1846 	lcall	__sdcc_banked_call
                                   1847 ;	../../../../platform/cc2530eb/./contiki-main.c:226: PUTSTRING(NETSTACK_RDC.name);
      000418 90 7E 7C         [24] 1848 	mov	dptr,#_nullrdc_driver
      00041B E4               [12] 1849 	clr	a
      00041C 93               [24] 1850 	movc	a,@a+dptr
      00041D FD               [12] 1851 	mov	r5,a
      00041E A3               [24] 1852 	inc	dptr
      00041F E4               [12] 1853 	clr	a
      000420 93               [24] 1854 	movc	a,@a+dptr
      000421 FE               [12] 1855 	mov	r6,a
      000422 A3               [24] 1856 	inc	dptr
      000423 E4               [12] 1857 	clr	a
      000424 93               [24] 1858 	movc	a,@a+dptr
      000425 FF               [12] 1859 	mov	r7,a
      000426 8D 82            [24] 1860 	mov	dpl,r5
      000428 8E 83            [24] 1861 	mov	dph,r6
      00042A 8F F0            [24] 1862 	mov	b,r7
      00042C 78 8E            [12] 1863 	mov	r0,#_putstring
      00042E 79 89            [12] 1864 	mov	r1,#(_putstring >> 8)
      000430 7A 04            [12] 1865 	mov	r2,#(_putstring >> 16)
      000432 12 07 25         [24] 1866 	lcall	__sdcc_banked_call
                                   1867 ;	../../../../platform/cc2530eb/./contiki-main.c:227: PUTCHAR('\n');
      000435 75 82 0A         [24] 1868 	mov	dpl,#0x0A
      000438 78 76            [12] 1869 	mov	r0,#_putchar
      00043A 79 6B            [12] 1870 	mov	r1,#(_putchar >> 8)
      00043C 7A 00            [12] 1871 	mov	r2,#(_putchar >> 16)
      00043E 12 07 25         [24] 1872 	lcall	__sdcc_banked_call
                                   1873 ;	../../../../platform/cc2530eb/./contiki-main.c:228: PUTCHAR('\r');
      000441 75 82 0D         [24] 1874 	mov	dpl,#0x0D
      000444 78 76            [12] 1875 	mov	r0,#_putchar
      000446 79 6B            [12] 1876 	mov	r1,#(_putchar >> 8)
      000448 7A 00            [12] 1877 	mov	r2,#(_putchar >> 16)
      00044A 12 07 25         [24] 1878 	lcall	__sdcc_banked_call
                                   1879 ;	../../../../platform/cc2530eb/./contiki-main.c:230: PUTSTRING("##########################################\n\r");
      00044D 90 7D 23         [24] 1880 	mov	dptr,#__str_4
      000450 75 F0 80         [24] 1881 	mov	b,#0x80
      000453 78 8E            [12] 1882 	mov	r0,#_putstring
      000455 79 89            [12] 1883 	mov	r1,#(_putstring >> 8)
      000457 7A 04            [12] 1884 	mov	r2,#(_putstring >> 16)
      000459 12 07 25         [24] 1885 	lcall	__sdcc_banked_call
                                   1886 ;	../../../../platform/cc2530eb/./contiki-main.c:233: watchdog_init();
      00045C 78 B2            [12] 1887 	mov	r0,#_watchdog_init
      00045E 79 83            [12] 1888 	mov	r1,#(_watchdog_init >> 8)
      000460 7A 04            [12] 1889 	mov	r2,#(_watchdog_init >> 16)
      000462 12 07 25         [24] 1890 	lcall	__sdcc_banked_call
                                   1891 ;	../../../../platform/cc2530eb/./contiki-main.c:236: random_init(0);
      000465 90 00 00         [24] 1892 	mov	dptr,#0x0000
      000468 78 9D            [12] 1893 	mov	r0,#_random_init
      00046A 79 91            [12] 1894 	mov	r1,#(_random_init >> 8)
      00046C 7A 04            [12] 1895 	mov	r2,#(_random_init >> 16)
      00046E 12 07 25         [24] 1896 	lcall	__sdcc_banked_call
                                   1897 ;	../../../../platform/cc2530eb/./contiki-main.c:239: process_start(&etimer_process, NULL);
      000471 E4               [12] 1898 	clr	a
      000472 C0 E0            [24] 1899 	push	acc
      000474 C0 E0            [24] 1900 	push	acc
      000476 C0 E0            [24] 1901 	push	acc
      000478 90 18 C9         [24] 1902 	mov	dptr,#_etimer_process
      00047B 75 F0 00         [24] 1903 	mov	b,#0x00
      00047E 78 0F            [12] 1904 	mov	r0,#_process_start
      000480 79 80            [12] 1905 	mov	r1,#(_process_start >> 8)
      000482 7A 03            [12] 1906 	mov	r2,#(_process_start >> 16)
      000484 12 07 25         [24] 1907 	lcall	__sdcc_banked_call
      000487 15 81            [12] 1908 	dec	sp
      000489 15 81            [12] 1909 	dec	sp
      00048B 15 81            [12] 1910 	dec	sp
                                   1911 ;	../../../../platform/cc2530eb/./contiki-main.c:240: ctimer_init();
      00048D 78 13            [12] 1912 	mov	r0,#_ctimer_init
      00048F 79 E3            [12] 1913 	mov	r1,#(_ctimer_init >> 8)
      000491 7A 03            [12] 1914 	mov	r2,#(_ctimer_init >> 16)
      000493 12 07 25         [24] 1915 	lcall	__sdcc_banked_call
                                   1916 ;	../../../../platform/cc2530eb/./contiki-main.c:243: netstack_init();
      000496 78 3A            [12] 1917 	mov	r0,#_netstack_init
      000498 79 07            [12] 1918 	mov	r1,#(_netstack_init >> 8)
      00049A 7A 00            [12] 1919 	mov	r2,#(_netstack_init >> 16)
      00049C 12 07 25         [24] 1920 	lcall	__sdcc_banked_call
                                   1921 ;	../../../../platform/cc2530eb/./contiki-main.c:244: set_rime_addr();
      00049F 12 01 57         [24] 1922 	lcall	_set_rime_addr
                                   1923 ;	../../../../platform/cc2530eb/./contiki-main.c:247: process_start(&sensors_process, NULL);
      0004A2 E4               [12] 1924 	clr	a
      0004A3 C0 E0            [24] 1925 	push	acc
      0004A5 C0 E0            [24] 1926 	push	acc
      0004A7 C0 E0            [24] 1927 	push	acc
      0004A9 90 19 03         [24] 1928 	mov	dptr,#_sensors_process
      0004AC 75 F0 00         [24] 1929 	mov	b,#0x00
      0004AF 78 0F            [12] 1930 	mov	r0,#_process_start
      0004B1 79 80            [12] 1931 	mov	r1,#(_process_start >> 8)
      0004B3 7A 03            [12] 1932 	mov	r2,#(_process_start >> 16)
      0004B5 12 07 25         [24] 1933 	lcall	__sdcc_banked_call
      0004B8 15 81            [12] 1934 	dec	sp
      0004BA 15 81            [12] 1935 	dec	sp
      0004BC 15 81            [12] 1936 	dec	sp
                                   1937 ;	../../../../platform/cc2530eb/./contiki-main.c:248: ADC_SENSOR_ACTIVATE();
      0004BE 90 7D E0         [24] 1938 	mov	dptr,#(_adc_sensor + 0x0006)
      0004C1 E4               [12] 1939 	clr	a
      0004C2 93               [24] 1940 	movc	a,@a+dptr
      0004C3 FD               [12] 1941 	mov	r5,a
      0004C4 A3               [24] 1942 	inc	dptr
      0004C5 E4               [12] 1943 	clr	a
      0004C6 93               [24] 1944 	movc	a,@a+dptr
      0004C7 FE               [12] 1945 	mov	r6,a
      0004C8 A3               [24] 1946 	inc	dptr
      0004C9 E4               [12] 1947 	clr	a
      0004CA 93               [24] 1948 	movc	a,@a+dptr
      0004CB FF               [12] 1949 	mov	r7,a
      0004CC C0 07            [24] 1950 	push	ar7
      0004CE C0 06            [24] 1951 	push	ar6
      0004D0 C0 05            [24] 1952 	push	ar5
      0004D2 74 01            [12] 1953 	mov	a,#0x01
      0004D4 C0 E0            [24] 1954 	push	acc
      0004D6 E4               [12] 1955 	clr	a
      0004D7 C0 E0            [24] 1956 	push	acc
      0004D9 C0 05            [24] 1957 	push	ar5
      0004DB C0 06            [24] 1958 	push	ar6
      0004DD C0 07            [24] 1959 	push	ar7
      0004DF 90 00 81         [24] 1960 	mov	dptr,#0x0081
      0004E2 D0 02            [24] 1961 	pop	ar2
      0004E4 D0 01            [24] 1962 	pop	ar1
      0004E6 D0 00            [24] 1963 	pop	ar0
      0004E8 12 07 25         [24] 1964 	lcall	__sdcc_banked_call
      0004EB 15 81            [12] 1965 	dec	sp
      0004ED 15 81            [12] 1966 	dec	sp
      0004EF D0 05            [24] 1967 	pop	ar5
      0004F1 D0 06            [24] 1968 	pop	ar6
      0004F3 D0 07            [24] 1969 	pop	ar7
                                   1970 ;	../../../../platform/cc2530eb/./contiki-main.c:253: JOYSTICK_SENSOR_ACTIVATE();
      0004F5 90 7D F0         [24] 1971 	mov	dptr,#(_joystick_sensor + 0x0006)
      0004F8 E4               [12] 1972 	clr	a
      0004F9 93               [24] 1973 	movc	a,@a+dptr
      0004FA FD               [12] 1974 	mov	r5,a
      0004FB A3               [24] 1975 	inc	dptr
      0004FC E4               [12] 1976 	clr	a
      0004FD 93               [24] 1977 	movc	a,@a+dptr
      0004FE FE               [12] 1978 	mov	r6,a
      0004FF A3               [24] 1979 	inc	dptr
      000500 E4               [12] 1980 	clr	a
      000501 93               [24] 1981 	movc	a,@a+dptr
      000502 FF               [12] 1982 	mov	r7,a
      000503 C0 07            [24] 1983 	push	ar7
      000505 C0 06            [24] 1984 	push	ar6
      000507 C0 05            [24] 1985 	push	ar5
      000509 74 01            [12] 1986 	mov	a,#0x01
      00050B C0 E0            [24] 1987 	push	acc
      00050D E4               [12] 1988 	clr	a
      00050E C0 E0            [24] 1989 	push	acc
      000510 C0 05            [24] 1990 	push	ar5
      000512 C0 06            [24] 1991 	push	ar6
      000514 C0 07            [24] 1992 	push	ar7
      000516 90 00 81         [24] 1993 	mov	dptr,#0x0081
      000519 D0 02            [24] 1994 	pop	ar2
      00051B D0 01            [24] 1995 	pop	ar1
      00051D D0 00            [24] 1996 	pop	ar0
      00051F 12 07 25         [24] 1997 	lcall	__sdcc_banked_call
      000522 15 81            [12] 1998 	dec	sp
      000524 15 81            [12] 1999 	dec	sp
      000526 D0 05            [24] 2000 	pop	ar5
      000528 D0 06            [24] 2001 	pop	ar6
      00052A D0 07            [24] 2002 	pop	ar7
                                   2003 ;	../../../../platform/cc2530eb/./contiki-main.c:258: memcpy(&uip_lladdr.addr, &rimeaddr_node_addr, sizeof(uip_lladdr.addr));
      00052C 74 08            [12] 2004 	mov	a,#0x08
      00052E C0 E0            [24] 2005 	push	acc
      000530 E4               [12] 2006 	clr	a
      000531 C0 E0            [24] 2007 	push	acc
      000533 74 78            [12] 2008 	mov	a,#_rimeaddr_node_addr
      000535 C0 E0            [24] 2009 	push	acc
      000537 74 16            [12] 2010 	mov	a,#(_rimeaddr_node_addr >> 8)
      000539 C0 E0            [24] 2011 	push	acc
      00053B E4               [12] 2012 	clr	a
      00053C C0 E0            [24] 2013 	push	acc
      00053E 90 06 04         [24] 2014 	mov	dptr,#_uip_lladdr
      000541 75 F0 00         [24] 2015 	mov	b,#0x00
      000544 78 F2            [12] 2016 	mov	r0,#_memcpy
      000546 79 77            [12] 2017 	mov	r1,#(_memcpy >> 8)
      000548 7A 00            [12] 2018 	mov	r2,#(_memcpy >> 16)
      00054A 12 07 25         [24] 2019 	lcall	__sdcc_banked_call
      00054D E5 81            [12] 2020 	mov	a,sp
      00054F 24 FB            [12] 2021 	add	a,#0xfb
      000551 F5 81            [12] 2022 	mov	sp,a
                                   2023 ;	../../../../platform/cc2530eb/./contiki-main.c:259: queuebuf_init();
      000553 78 54            [12] 2024 	mov	r0,#_queuebuf_init
      000555 79 BC            [12] 2025 	mov	r1,#(_queuebuf_init >> 8)
      000557 7A 03            [12] 2026 	mov	r2,#(_queuebuf_init >> 16)
      000559 12 07 25         [24] 2027 	lcall	__sdcc_banked_call
                                   2028 ;	../../../../platform/cc2530eb/./contiki-main.c:260: process_start(&tcpip_process, NULL);
      00055C E4               [12] 2029 	clr	a
      00055D C0 E0            [24] 2030 	push	acc
      00055F C0 E0            [24] 2031 	push	acc
      000561 C0 E0            [24] 2032 	push	acc
      000563 90 18 B9         [24] 2033 	mov	dptr,#_tcpip_process
      000566 75 F0 00         [24] 2034 	mov	b,#0x00
      000569 78 0F            [12] 2035 	mov	r0,#_process_start
      00056B 79 80            [12] 2036 	mov	r1,#(_process_start >> 8)
      00056D 7A 03            [12] 2037 	mov	r2,#(_process_start >> 16)
      00056F 12 07 25         [24] 2038 	lcall	__sdcc_banked_call
      000572 15 81            [12] 2039 	dec	sp
      000574 15 81            [12] 2040 	dec	sp
      000576 15 81            [12] 2041 	dec	sp
                                   2042 ;	../../../../platform/cc2530eb/./contiki-main.c:264: process_start(&viztool_process, NULL);
      000578 E4               [12] 2043 	clr	a
      000579 C0 E0            [24] 2044 	push	acc
      00057B C0 E0            [24] 2045 	push	acc
      00057D C0 E0            [24] 2046 	push	acc
      00057F 90 19 34         [24] 2047 	mov	dptr,#_viztool_process
      000582 75 F0 00         [24] 2048 	mov	b,#0x00
      000585 78 0F            [12] 2049 	mov	r0,#_process_start
      000587 79 80            [12] 2050 	mov	r1,#(_process_start >> 8)
      000589 7A 03            [12] 2051 	mov	r2,#(_process_start >> 16)
      00058B 12 07 25         [24] 2052 	lcall	__sdcc_banked_call
      00058E 15 81            [12] 2053 	dec	sp
      000590 15 81            [12] 2054 	dec	sp
      000592 15 81            [12] 2055 	dec	sp
                                   2056 ;	../../../../platform/cc2530eb/./contiki-main.c:267: energest_init();
      000594 78 E6            [12] 2057 	mov	r0,#_energest_init
      000596 79 FF            [12] 2058 	mov	r1,#(_energest_init >> 8)
      000598 7A 01            [12] 2059 	mov	r2,#(_energest_init >> 16)
      00059A 12 07 25         [24] 2060 	lcall	__sdcc_banked_call
                                   2061 ;	../../../../platform/cc2530eb/./contiki-main.c:270: autostart_start(autostart_processes);
      00059D 90 7D D4         [24] 2062 	mov	dptr,#_autostart_processes
      0005A0 75 F0 80         [24] 2063 	mov	b,#0x80
      0005A3 78 65            [12] 2064 	mov	r0,#_autostart_start
      0005A5 79 8A            [12] 2065 	mov	r1,#(_autostart_start >> 8)
      0005A7 7A 04            [12] 2066 	mov	r2,#(_autostart_start >> 16)
      0005A9 12 07 25         [24] 2067 	lcall	__sdcc_banked_call
                                   2068 ;	../../../../platform/cc2530eb/./contiki-main.c:272: watchdog_start();
      0005AC 78 B8            [12] 2069 	mov	r0,#_watchdog_start
      0005AE 79 83            [12] 2070 	mov	r1,#(_watchdog_start >> 8)
      0005B0 7A 04            [12] 2071 	mov	r2,#(_watchdog_start >> 16)
      0005B2 12 07 25         [24] 2072 	lcall	__sdcc_banked_call
                                   2073 ;	../../../../platform/cc2530eb/./contiki-main.c:274: fade(LEDS_YELLOW);
      0005B5 90 00 04         [24] 2074 	mov	dptr,#0x0004
      0005B8 12 00 51         [24] 2075 	lcall	_fade
                                   2076 ;	../../../../platform/cc2530eb/./contiki-main.c:278: do {
      0005BB                       2077 00113$:
                                   2078 ;	../../../../platform/cc2530eb/./contiki-main.c:280: watchdog_periodic();
      0005BB 78 BE            [12] 2079 	mov	r0,#_watchdog_periodic
      0005BD 79 83            [12] 2080 	mov	r1,#(_watchdog_periodic >> 8)
      0005BF 7A 04            [12] 2081 	mov	r2,#(_watchdog_periodic >> 16)
      0005C1 12 07 25         [24] 2082 	lcall	__sdcc_banked_call
                                   2083 ;	../../../../platform/cc2530eb/./contiki-main.c:283: if(sleep_flag) {
      0005C4 90 14 6E         [24] 2084 	mov	dptr,#_sleep_flag
      0005C7 E0               [24] 2085 	movx	a,@dptr
      0005C8 FF               [12] 2086 	mov	r7,a
      0005C9 60 57            [24] 2087 	jz	00112$
                                   2088 ;	../../../../platform/cc2530eb/./contiki-main.c:284: if(etimer_pending() &&
      0005CB 78 05            [12] 2089 	mov	r0,#_etimer_pending
      0005CD 79 93            [12] 2090 	mov	r1,#(_etimer_pending >> 8)
      0005CF 7A 03            [12] 2091 	mov	r2,#(_etimer_pending >> 16)
      0005D1 12 07 25         [24] 2092 	lcall	__sdcc_banked_call
      0005D4 E5 82            [12] 2093 	mov	a,dpl
      0005D6 85 83 F0         [24] 2094 	mov	b,dph
      0005D9 45 F0            [12] 2095 	orl	a,b
      0005DB 60 40            [24] 2096 	jz	00109$
                                   2097 ;	../../../../platform/cc2530eb/./contiki-main.c:285: (etimer_next_expiration_time() - clock_time() - 1) > MAX_TICKS) {
      0005DD 78 41            [12] 2098 	mov	r0,#_etimer_next_expiration_time
      0005DF 79 93            [12] 2099 	mov	r1,#(_etimer_next_expiration_time >> 8)
      0005E1 7A 03            [12] 2100 	mov	r2,#(_etimer_next_expiration_time >> 16)
      0005E3 12 07 25         [24] 2101 	lcall	__sdcc_banked_call
      0005E6 AE 82            [24] 2102 	mov	r6,dpl
      0005E8 AF 83            [24] 2103 	mov	r7,dph
      0005EA C0 07            [24] 2104 	push	ar7
      0005EC C0 06            [24] 2105 	push	ar6
      0005EE 78 E4            [12] 2106 	mov	r0,#_clock_time
      0005F0 79 6B            [12] 2107 	mov	r1,#(_clock_time >> 8)
      0005F2 7A 00            [12] 2108 	mov	r2,#(_clock_time >> 16)
      0005F4 12 07 25         [24] 2109 	lcall	__sdcc_banked_call
      0005F7 AC 82            [24] 2110 	mov	r4,dpl
      0005F9 AD 83            [24] 2111 	mov	r5,dph
      0005FB D0 06            [24] 2112 	pop	ar6
      0005FD D0 07            [24] 2113 	pop	ar7
      0005FF EE               [12] 2114 	mov	a,r6
      000600 C3               [12] 2115 	clr	c
      000601 9C               [12] 2116 	subb	a,r4
      000602 FE               [12] 2117 	mov	r6,a
      000603 EF               [12] 2118 	mov	a,r7
      000604 9D               [12] 2119 	subb	a,r5
      000605 FF               [12] 2120 	mov	r7,a
      000606 1E               [12] 2121 	dec	r6
      000607 BE FF 01         [24] 2122 	cjne	r6,#0xFF,00164$
      00060A 1F               [12] 2123 	dec	r7
      00060B                       2124 00164$:
      00060B C3               [12] 2125 	clr	c
      00060C 74 FF            [12] 2126 	mov	a,#0xFF
      00060E 9E               [12] 2127 	subb	a,r6
      00060F 74 7F            [12] 2128 	mov	a,#0x7F
      000611 9F               [12] 2129 	subb	a,r7
      000612 50 09            [24] 2130 	jnc	00109$
                                   2131 ;	../../../../platform/cc2530eb/./contiki-main.c:286: etimer_request_poll();
      000614 78 50            [12] 2132 	mov	r0,#_etimer_request_poll
      000616 79 90            [12] 2133 	mov	r1,#(_etimer_request_poll >> 8)
      000618 7A 03            [12] 2134 	mov	r2,#(_etimer_request_poll >> 16)
      00061A 12 07 25         [24] 2135 	lcall	__sdcc_banked_call
      00061D                       2136 00109$:
                                   2137 ;	../../../../platform/cc2530eb/./contiki-main.c:288: sleep_flag = 0;
      00061D 90 14 6E         [24] 2138 	mov	dptr,#_sleep_flag
      000620 E4               [12] 2139 	clr	a
      000621 F0               [24] 2140 	movx	@dptr,a
      000622                       2141 00112$:
                                   2142 ;	../../../../platform/cc2530eb/./contiki-main.c:291: r = process_run();
      000622 78 C1            [12] 2143 	mov	r0,#_process_run
      000624 79 88            [12] 2144 	mov	r1,#(_process_run >> 8)
      000626 7A 03            [12] 2145 	mov	r2,#(_process_run >> 16)
      000628 12 07 25         [24] 2146 	lcall	__sdcc_banked_call
      00062B AE 82            [24] 2147 	mov	r6,dpl
      00062D AF 83            [24] 2148 	mov	r7,dph
                                   2149 ;	../../../../platform/cc2530eb/./contiki-main.c:292: } while(r > 0);
      00062F EE               [12] 2150 	mov	a,r6
      000630 70 89            [24] 2151 	jnz	00113$
                                   2152 ;	../../../../platform/cc2530eb/./contiki-main.c:293: len = NETSTACK_RADIO.pending_packet();
      000632 90 7E 14         [24] 2153 	mov	dptr,#(_cc2530_rf_driver + 0x0015)
      000635 E4               [12] 2154 	clr	a
      000636 93               [24] 2155 	movc	a,@a+dptr
      000637 FD               [12] 2156 	mov	r5,a
      000638 A3               [24] 2157 	inc	dptr
      000639 E4               [12] 2158 	clr	a
      00063A 93               [24] 2159 	movc	a,@a+dptr
      00063B FE               [12] 2160 	mov	r6,a
      00063C A3               [24] 2161 	inc	dptr
      00063D E4               [12] 2162 	clr	a
      00063E 93               [24] 2163 	movc	a,@a+dptr
      00063F FF               [12] 2164 	mov	r7,a
      000640 C0 07            [24] 2165 	push	ar7
      000642 C0 06            [24] 2166 	push	ar6
      000644 C0 05            [24] 2167 	push	ar5
      000646 C0 05            [24] 2168 	push	ar5
      000648 C0 06            [24] 2169 	push	ar6
      00064A C0 07            [24] 2170 	push	ar7
      00064C D0 02            [24] 2171 	pop	ar2
      00064E D0 01            [24] 2172 	pop	ar1
      000650 D0 00            [24] 2173 	pop	ar0
      000652 12 07 25         [24] 2174 	lcall	__sdcc_banked_call
      000655 85 82 08         [24] 2175 	mov	_len,dpl
      000658 85 83 09         [24] 2176 	mov	(_len + 1),dph
      00065B D0 05            [24] 2177 	pop	ar5
      00065D D0 06            [24] 2178 	pop	ar6
      00065F D0 07            [24] 2179 	pop	ar7
                                   2180 ;	../../../../platform/cc2530eb/./contiki-main.c:294: if(len) {
      000661 E5 08            [12] 2181 	mov	a,_len
      000663 45 09            [12] 2182 	orl	a,(_len + 1)
      000665 70 03            [24] 2183 	jnz	00167$
      000667 02 05 BB         [24] 2184 	ljmp	00113$
      00066A                       2185 00167$:
                                   2186 ;	../../../../platform/cc2530eb/./contiki-main.c:295: packetbuf_clear();
      00066A 78 78            [12] 2187 	mov	r0,#_packetbuf_clear
      00066C 79 AE            [12] 2188 	mov	r1,#(_packetbuf_clear >> 8)
      00066E 7A 03            [12] 2189 	mov	r2,#(_packetbuf_clear >> 16)
      000670 12 07 25         [24] 2190 	lcall	__sdcc_banked_call
                                   2191 ;	../../../../platform/cc2530eb/./contiki-main.c:296: len = NETSTACK_RADIO.read(packetbuf_dataptr(), PACKETBUF_SIZE);
      000673 90 7E 0B         [24] 2192 	mov	dptr,#(_cc2530_rf_driver + 0x000c)
      000676 E4               [12] 2193 	clr	a
      000677 93               [24] 2194 	movc	a,@a+dptr
      000678 FD               [12] 2195 	mov	r5,a
      000679 A3               [24] 2196 	inc	dptr
      00067A E4               [12] 2197 	clr	a
      00067B 93               [24] 2198 	movc	a,@a+dptr
      00067C FE               [12] 2199 	mov	r6,a
      00067D A3               [24] 2200 	inc	dptr
      00067E E4               [12] 2201 	clr	a
      00067F 93               [24] 2202 	movc	a,@a+dptr
      000680 FF               [12] 2203 	mov	r7,a
      000681 C0 07            [24] 2204 	push	ar7
      000683 C0 06            [24] 2205 	push	ar6
      000685 C0 05            [24] 2206 	push	ar5
      000687 78 C8            [12] 2207 	mov	r0,#_packetbuf_dataptr
      000689 79 B2            [12] 2208 	mov	r1,#(_packetbuf_dataptr >> 8)
      00068B 7A 03            [12] 2209 	mov	r2,#(_packetbuf_dataptr >> 16)
      00068D 12 07 25         [24] 2210 	lcall	__sdcc_banked_call
      000690 AA 82            [24] 2211 	mov	r2,dpl
      000692 AB 83            [24] 2212 	mov	r3,dph
      000694 AC F0            [24] 2213 	mov	r4,b
      000696 D0 05            [24] 2214 	pop	ar5
      000698 D0 06            [24] 2215 	pop	ar6
      00069A D0 07            [24] 2216 	pop	ar7
      00069C C0 07            [24] 2217 	push	ar7
      00069E C0 06            [24] 2218 	push	ar6
      0006A0 C0 05            [24] 2219 	push	ar5
      0006A2 74 80            [12] 2220 	mov	a,#0x80
      0006A4 C0 E0            [24] 2221 	push	acc
      0006A6 E4               [12] 2222 	clr	a
      0006A7 C0 E0            [24] 2223 	push	acc
      0006A9 C0 05            [24] 2224 	push	ar5
      0006AB C0 06            [24] 2225 	push	ar6
      0006AD C0 07            [24] 2226 	push	ar7
      0006AF 8A 82            [24] 2227 	mov	dpl,r2
      0006B1 8B 83            [24] 2228 	mov	dph,r3
      0006B3 8C F0            [24] 2229 	mov	b,r4
      0006B5 D0 02            [24] 2230 	pop	ar2
      0006B7 D0 01            [24] 2231 	pop	ar1
      0006B9 D0 00            [24] 2232 	pop	ar0
      0006BB 12 07 25         [24] 2233 	lcall	__sdcc_banked_call
      0006BE 85 82 08         [24] 2234 	mov	_len,dpl
      0006C1 85 83 09         [24] 2235 	mov	(_len + 1),dph
      0006C4 15 81            [12] 2236 	dec	sp
      0006C6 15 81            [12] 2237 	dec	sp
      0006C8 D0 05            [24] 2238 	pop	ar5
      0006CA D0 06            [24] 2239 	pop	ar6
      0006CC D0 07            [24] 2240 	pop	ar7
                                   2241 ;	../../../../platform/cc2530eb/./contiki-main.c:297: if(len > 0) {
      0006CE E5 08            [12] 2242 	mov	a,_len
      0006D0 45 09            [12] 2243 	orl	a,(_len + 1)
      0006D2 70 03            [24] 2244 	jnz	00168$
      0006D4 02 05 BB         [24] 2245 	ljmp	00113$
      0006D7                       2246 00168$:
                                   2247 ;	../../../../platform/cc2530eb/./contiki-main.c:298: packetbuf_set_datalen(len);
      0006D7 85 08 82         [24] 2248 	mov	dpl,_len
      0006DA 85 09 83         [24] 2249 	mov	dph,(_len + 1)
      0006DD 78 BA            [12] 2250 	mov	r0,#_packetbuf_set_datalen
      0006DF 79 B2            [12] 2251 	mov	r1,#(_packetbuf_set_datalen >> 8)
      0006E1 7A 03            [12] 2252 	mov	r2,#(_packetbuf_set_datalen >> 16)
      0006E3 12 07 25         [24] 2253 	lcall	__sdcc_banked_call
                                   2254 ;	../../../../platform/cc2530eb/./contiki-main.c:299: NETSTACK_RDC.input();
      0006E6 90 7E 88         [24] 2255 	mov	dptr,#(_nullrdc_driver + 0x000c)
      0006E9 E4               [12] 2256 	clr	a
      0006EA 93               [24] 2257 	movc	a,@a+dptr
      0006EB FD               [12] 2258 	mov	r5,a
      0006EC A3               [24] 2259 	inc	dptr
      0006ED E4               [12] 2260 	clr	a
      0006EE 93               [24] 2261 	movc	a,@a+dptr
      0006EF FE               [12] 2262 	mov	r6,a
      0006F0 A3               [24] 2263 	inc	dptr
      0006F1 E4               [12] 2264 	clr	a
      0006F2 93               [24] 2265 	movc	a,@a+dptr
      0006F3 FF               [12] 2266 	mov	r7,a
      0006F4 C0 07            [24] 2267 	push	ar7
      0006F6 C0 06            [24] 2268 	push	ar6
      0006F8 C0 05            [24] 2269 	push	ar5
      0006FA C0 05            [24] 2270 	push	ar5
      0006FC C0 06            [24] 2271 	push	ar6
      0006FE C0 07            [24] 2272 	push	ar7
      000700 D0 02            [24] 2273 	pop	ar2
      000702 D0 01            [24] 2274 	pop	ar1
      000704 D0 00            [24] 2275 	pop	ar0
      000706 12 07 25         [24] 2276 	lcall	__sdcc_banked_call
      000709 D0 05            [24] 2277 	pop	ar5
      00070B D0 06            [24] 2278 	pop	ar6
      00070D D0 07            [24] 2279 	pop	ar7
      00070F 02 05 BB         [24] 2280 	ljmp	00113$
                                   2281 	.area CSEG    (CODE)
                                   2282 	.area CONST   (CODE)
      007CCF                       2283 __str_0:
      007CCF 52 69 6D 65 20 69 73  2284 	.ascii "Rime is 0x"
             20 30 78
      007CD9 00                    2285 	.db 0x00
      007CDA                       2286 __str_1:
      007CDA 20 62 79 74 65 73 20  2287 	.ascii " bytes long"
             6C 6F 6E 67
      007CE5 0A                    2288 	.db 0x0A
      007CE6 0D                    2289 	.db 0x0D
      007CE7 00                    2290 	.db 0x00
      007CE8                       2291 __str_2:
      007CE8 52 65 61 64 69 6E 67  2292 	.ascii "Reading MAC from Info Page"
             20 4D 41 43 20 66 72
             6F 6D 20 49 6E 66 6F
             20 50 61 67 65
      007D02 0A                    2293 	.db 0x0A
      007D03 0D                    2294 	.db 0x0D
      007D04 00                    2295 	.db 0x00
      007D05                       2296 __str_3:
      007D05 52 69 6D 65 20 63 6F  2297 	.ascii "Rime configured with address "
             6E 66 69 67 75 72 65
             64 20 77 69 74 68 20
             61 64 64 72 65 73 73
             20
      007D22 00                    2298 	.db 0x00
      007D23                       2299 __str_4:
      007D23 23 23 23 23 23 23 23  2300 	.ascii "##########################################"
             23 23 23 23 23 23 23
             23 23 23 23 23 23 23
             23 23 23 23 23 23 23
             23 23 23 23 23 23 23
             23 23 23 23 23 23 23
      007D4D 0A                    2301 	.db 0x0A
      007D4E 0D                    2302 	.db 0x0D
      007D4F 00                    2303 	.db 0x00
      007D50                       2304 __str_5:
      007D50 43 6F 6E 74 69 6B 69  2305 	.ascii "Contiki 2.6"
             20 32 2E 36
      007D5B 0A                    2306 	.db 0x0A
      007D5C 0D                    2307 	.db 0x0D
      007D5D 00                    2308 	.db 0x00
      007D5E                       2309 __str_6:
      007D5E 54 49 20 53 6D 61 72  2310 	.ascii "TI SmartRF05 EB"
             74 52 46 30 35 20 45
             42
      007D6D 0A                    2311 	.db 0x0A
      007D6E 0D                    2312 	.db 0x0D
      007D6F 00                    2313 	.db 0x00
      007D70                       2314 __str_7:
      007D70 63 63 32 35 33 30     2315 	.ascii "cc2530"
      007D76 00                    2316 	.db 0x00
      007D77                       2317 __str_8:
      007D77 63 63 32 35 33 31     2318 	.ascii "cc2531"
      007D7D 00                    2319 	.db 0x00
      007D7E                       2320 __str_9:
      007D7E 63 63 32 35 33 33     2321 	.ascii "cc2533"
      007D84 00                    2322 	.db 0x00
      007D85                       2323 __str_10:
      007D85 63 63 32 35 34 30     2324 	.ascii "cc2540"
      007D8B 00                    2325 	.db 0x00
      007D8C                       2326 __str_11:
      007D8C 2D 46 32 35 36 2C 20  2327 	.ascii "-F256, "
      007D93 00                    2328 	.db 0x00
      007D94                       2329 __str_12:
      007D94 4B 42 20 53 52 41 4D  2330 	.ascii "KB SRAM"
      007D9B 0A                    2331 	.db 0x0A
      007D9C 0D                    2332 	.db 0x0D
      007D9D 00                    2333 	.db 0x00
      007D9E                       2334 __str_13:
      007D9E 0A                    2335 	.db 0x0A
      007D9F 53 44 43 43 20 42 75  2336 	.ascii "SDCC Build:"
             69 6C 64 3A
      007DAA 0A                    2337 	.db 0x0A
      007DAB 0D                    2338 	.db 0x0D
      007DAC 00                    2339 	.db 0x00
      007DAD                       2340 __str_14:
      007DAD 20 20 57 69 74 68 20  2341 	.ascii "  With Banking."
             42 61 6E 6B 69 6E 67
             2E
      007DBC 0A                    2342 	.db 0x0A
      007DBD 0D                    2343 	.db 0x0D
      007DBE 00                    2344 	.db 0x00
      007DBF                       2345 __str_15:
      007DBF 20 4E 65 74 3A 20     2346 	.ascii " Net: "
      007DC5 00                    2347 	.db 0x00
      007DC6                       2348 __str_16:
      007DC6 20 4D 41 43 3A 20     2349 	.ascii " MAC: "
      007DCC 00                    2350 	.db 0x00
      007DCD                       2351 __str_17:
      007DCD 20 52 44 43 3A 20     2352 	.ascii " RDC: "
      007DD3 00                    2353 	.db 0x00
                                   2354 	.area XINIT   (CODE)
                                   2355 	.area CABS    (ABS,CODE)
