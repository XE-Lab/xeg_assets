# Biofrost | Realme 5 Series (trinket/r5x) Specific Changes
##  02/13/2022 | trinket
Mainline:
- Bump to rev1.4
- Linux upstream 'v4.14.265', 'v4.14.266'
- Imported WireGuard 'v1.0.20211208'
- Introduced and Enabled: CPU_INPUT_BOOST
- Introduced and Enabled UCLAMP
- Introduce GPU Input-boost feature
- Introduced and Enabled Adreno Idler
- Implement UCLAMP Assist
- ZRAM Improvements and Optimizations
- Optimized energy model
- Improved cpuidle
- Improved Scheduler
- Network Tweaks

General:
- cpu_input_boost: tuned freqs accordingly
- cpufreq: Optimizations
- uclamp: BACKPORTS
- uclamp: Optimizations
- uclamp: tuning
- adrenoboost: tuning
- adrenoboost: added conservative governor
- adrenoboost: added conservative governor v2
- adrenoboost: cut sum low freq bump 
- adreno_idler: switch to count based instead of time based
- adreno_idler: remove frequency bump
- adreno_idler: fix-up type definitions
- adreno_idler: fix-up some comments
- adreno_idler: fix typos 
- adreno idler: Ramp down more agressively
- ZRAM: Optimizations, Improvements
- cpuidle: some optimizations and improvements
- Set ZRAM's Default Compression Algorithm to LZ4
- Enabled: ZRAM Writeback
- Increased ZRAM's size to 1.4GB
- zsmalloc: Optimizations
- thermal: Optimizations
- Do not migrate if the prev_cpu is idle
- arm/arm64: dts: Some improvements/fixes
- mm: Optimizations
- ext4: Optimizations
- rcu: Fixes and Improvements
- block: cfq-iosched: Micro Optimize
- printk: few additions
- net: sched: Optimizations
- fq-codel: Improvements
- BACKPORT: ipv6: Implement draft-ietf-6man-rfc4941bis
- TCP_bbr: Improvements and optimizations
- NET-tcp: Some tweaks
-  Disabled a lot of tracing, logging, and debugging
- Tons of backports for General Improvements
- Many more under-the-hood improvements treewide
- Many other more from latest Tags (.255/.256)

##  02/05/2022 | trinket
Mainline:
- Compiled with latest Azure Clang 15.0
- Added Various Useful BACKPORTS
- Power Efficient Workqueues
- Silenced a lot more loggings/tracing crap
- Switch to capacity based Energy-Model
- treewide: fixes and improvements

General:
- sched/fair: tuning
- mm: some changes
- lib/string: optimizations
- ashmem: improve performance
- iommu: msm: improve performance
- msm: kgsl: lots of changes/optimizations 
- scripts/kallsyms: make it more effective
- qcacld: minor fixes/optimizations
- sched/fair: optimizations
- cpuidle: tweaks
- kprofiles: some changes
- cpu-boost: various fixes/optimizations
- file system: various improvements
- Added some more modifications to the Energy Model
- Removed Qcom's PM_QoS Implementation
- Some more minor improvements
- Tuned for Performance and Battery Backup
- Many other more! (i guess)

## 01/31/2022 | trinket
Mainline:
- Linux upstream 'v4.14.264'
- Compiled with Proton 13.0 Clang
- Disabled/Nuked a lot of Loggings
- Power efficient work queues

General:
- Force suspend when cable out
- Disable MSM_PERFORMANCE
- Fingerprint Optimizations
- Silenced some more logs/debugs
- Trimmed some codes
- Relax CPU latency requirements to save power 
- Shittons of Optimizations
- Some Minor Fixes
- Remove magisk support (you can flash even unrooted)
- Improved deep sleep
- Added some tweaks for performance / battery
- many more ^^

NOTE: Even though i've tuned some stuffs for battery-efficiency, i didn't forget about gaming/performance.

## 01/29/2022 | trinket
Mainline:
- Switch back to Proton 13.0 Clang
- Linux upstream 'v4.14.263'

General:
- Improved RAM Management
- Change TCP from Cubic to BBR
- Logging Cleanup
- Introduced Kprofiles 
  - kprofiles: hardcode battery mode as default
  - bump kprofiles to v2 and v3 
- Reduce TCP Performance Spikes
- Force applications to use TCP_NODELAY
- Disabled Some More Loggings
- Added Fast Charge Support
- Make iowait boost more energy efficient 
- Many other more (i'm lazy to include)
