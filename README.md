# Jetson-Nano-Hashcat
Hashcat benchmarks on the Jetson Nano.
Nothing fancy, just hashcat -b

Fresh make install from github successfully used the Cuda API on default nano image.

SD Benchmark - 256 GB Sandisk Extreme Pro - A2-3
Compile hashcat from source - no pre-compiled binaries available and need hashcat's newer cuda-api functionality anyways


SSD Benchmarks:

1TB Samsung 850 EVO via .5" USB3<->SATA cable
    Used initrd method to make SSD "bootable":  https://www.jetsonhacks.com/2019/09/17/jetson-nano-run-from-usb-drive/
    Compile hashcat from source - no pre-compiled binaries available and need hashcats newer cuda-api functionality anyways.
    Some mild performance gains were made over the SD benchmarks, but nothing of significance.
    Additional mild gains were made running with workload set to insane (-w4)
    No additional heat was observed on the processor for any workloads.
        Need to collect data for further comparison on heat.
    *Noted that 1 cpu core is always bound when tests are being performed.  It switches cpu core with each hash type.
    
    
512GB Samasung 860 Pro (NAND) via .5" USB3<->SATA cable
    Used initrd method to make SSD "bootable":  https://www.jetsonhacks.com/2019/09/17/jetson-nano-run-from-usb-drive/
    Compile hashcat from source - no pre-compiled binaries available and need hashcats newer cuda-api functionality anyways
