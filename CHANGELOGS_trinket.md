# Biofrost | Realme 5 Series (trinket/r5x) Specific Changes
##  02/05/2022 | trinket
Mainline:
- Compiled with latest Azure Clang 15.0
- Added Various Useful BACKPORTS
- Power Efficient Workqueues
- Silenced a lot more loggings/tracing crap
- Switch to Energy-Model

General:
- sched/fair: tuning
- mm: some changes
- lib/string: optimizations
- iommu: msm: improved performance
- msm: kgsl: some fixes
- scripts/kallsyms: make it more effective
- Switch to capacity based Energy Model
- Added some more modifications to the Energy Model
- qcacld: minor fixes/optimizations
- sched/fair: optimizations
- cpuidle: tweaks
- kprofiles: some changes
- file system: various improvements
- Removed Qcom's PM_QoS Implementation
- Some more minor improvements
- Treewide: fixes and improvements underhood
- Tuned for Performance and Battery Backup
- Many other more!

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
