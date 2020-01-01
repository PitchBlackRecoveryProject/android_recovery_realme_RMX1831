 TWRP Device Tree for Realme U1
===========================================

The Realme U1 (codenames _"RMX1831"_ and _"RMX1833"_) is a mid-range smartphone from Realme, announced in November 2018.	
 
## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
OS	| Android 8.1 (Oreo), upgradable to Android 9.0 (Pie)	
CPU     | Octa-core (4x2.1 GHz Cortex-A73 & 4x2.0 GHz Cortex-A53)
Chipset | Mediatek Helio P70
GPU     | Mali-G72 MP3
Memory  | 3GB/4GB RAM
Storage | 32GB/64GB
MicroSD | up to 256 GB (dedicated slot)
Battery | Non-removable Li-Ion 3500 mAh battery
Resolution | 1080 x 2340 pixels, 19.5:9 ratio (~409 ppi density)
Camera (Rear)  | (Dual) 13 MP, f/2.2, AF. 2 MP, f/2.4, depth sensor
Rear Camera Features | LED flash, HDR, panorama
Video	| 1080p@30fps, 720p@90fps
Camera (Front)  | 25 MP, f/2.0, 1/2.8", 0.9µm
Features| Fingerprint (rear-mounted), accelerometer, proximity, compass	

## Device picture

![Realme U1](https://images-na.ssl-images-amazon.com/images/I/71G%2BlExqsrL._AC_SX679_.jpg "Realme U1")



## Getting Started ##
---------------

To get started with OMNI sources to build TWRP, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

# repo init

To initialize your local repository using the OMNIROM trees to build TWRP, use a command like this:

    repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0

To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0

# repo sync

If you are a first time builder then do check Imp_for_first_time_builders.txt file.
 Then to sync up:

    repo sync -j(nproc) -c

## To Build ##
---------------

Build the TWRP recovery using below command.

    cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_RMX1831-eng; mka recoveryimage
