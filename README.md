# MBP-2010-GPU-Panic-fix
MBP 2010 GPU Panic fix to MacBook Pro 15" mid 2010


My macrumores.com user is fabioroberto.
I found a solution with MacBook Pro 6,2 GPU Panic problem. 
I discovered that this problem happens every time that g-state change between 2 to 0.

G-States go from 0 to 3, are related to the thresholds inside AppleGraphicsPowerManagement.kext.
G-state 0 (maximum speed) and G-state 3 (lowest speed).

I solved the problem keeping it always at G-State 3 and 2 (medium speed). 
	
About the performance after the fix? 
Exemple: Cinebench, default (G-state 0) i've about 15fps, with g-state 2 (medium speed): 10fps. Not bad.	
	
More info:
https://forums.macrumors.com/threads/gpu-kernel-panic-in-mid-2010-whats-the-best-fix.1890097/#post-23312990


# How to use:

1 - Make sure these .kext are original (unmodified), and loaded (About this Mac -> System Report -> Software -> Extensions):
	ACPI_SMC_PlatformPlugin.kext (IOPlatformPluginFamily.kext)
	AppleGraphicsPowerManagement.kext

2 - Disable SIP (boot into recovery mode, terminal: csrutil disable)
Avaliable only in OS X El Capitan or later.

3 - Download MBP 2010 GPU Panic fix and run. Here: https://github.com/fabioiop/MBP-2010-GPU-Panic-fix/releases


4 - Choose option: run the fix or remove the previous fix.
