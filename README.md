# wlr8100

cal extraction:

dd if=/dev/mtd6ro of=cal-pci-0000:01:00.0.bin bs=1 skip=24576 count=2116
dd if=/dev/mtd7ro of=cal-pci-0000:01:00.0.bin bs=1 skip=348160 count=2116

one seems to be the backup ?

works partly:

```
[   13.270455] PCI: Enabling device 0000:01:00.0 (0000 -> 0002)
[   13.276387] ath10k_pci 0000:01:00.0: pci irq legacy oper_irq_mode 1 
irq_mode 0 reset_mode 0
[   13.511330] ath10k_pci 0000:01:00.0: Direct firmware load for 
ath10k/pre-cal-pci-0000:01:00.0.bin failed with error -2
[   13.522230] ath10k_pci 0000:01:00.0: Falling back to user helper
[   13.597125] firmware ath10k!pre-cal-pci-0000:01:00.0.bin: 
firmware_loading_store: map pages failed
[   14.004113] ath10k_pci 0000:01:00.0: qca988x hw2.0 target 0x4100016c 
chip_id 0x043202ff sub 0000:0000
[   14.013475] ath10k_pci 0000:01:00.0: kconfig debug 1 debugfs 1 
tracing 0 dfs 1 testmode 1
[   14.026567] ath10k_pci 0000:01:00.0: firmware ver 10.2.4.97 api 5 
features no-p2p crc32 f91e34f2
[   14.075690] ath10k_pci 0000:01:00.0: Direct firmware load for 
ath10k/QCA988X/hw2.0/board-2.bin failed with error -2
[   14.086295] ath10k_pci 0000:01:00.0: Falling back to user helper
[   14.161184] firmware ath10k!QCA988X!hw2.0!board-2.bin: 
firmware_loading_store: map pages failed
[   14.170439] ath10k_pci 0000:01:00.0: board_file api 1 bmi_id N/A 
crc32 bebc7c08
[   15.286070] ath10k_pci 0000:01:00.0: htt-ver 2.1 wmi-op 5 htt-op 2 
cal file max-sta 128 raw 0 hwcrypto 1
```

issue: (bmi_id: N/A)
