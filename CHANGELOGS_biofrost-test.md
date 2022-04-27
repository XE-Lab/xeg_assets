|==========| Biofrost - Test |=========|

Device: Realme 5 series (r5x)
Kernel Version: v4.14.276
Compiler: Dora Clang 15.0.0
Linker: GNU Binutils (ld.bfd)
By: mcdofrenchfreis

========================================

Date: 28/04/22

- Compiled with Cortex-A73.Cortex-A53+Crypto + 03 + POLLY (optimizations)
- Upstream to v4.14.277
- Reduced some more logspams/loggers
- Blk-mq fixes
- MSM_BUS fixes
- Sched optimizations
- Core.c optimizations
- Add node tampering blacklist function
- Update blocking blacklist
- Increase thermal trip points to 16
- Increase throttling limit
- Don't qualify thermal polling as high priority
- Schedutil optimizations
- Initialize governors earlier
- Introduce: Process Reclaim Low Memory Killer [PRLMK]
- Tweak PRLMK's tuning a little bit (free file limit/free swap limit)
- biofrost_defconfig: Set PELT half-life to 16
- many more optimizations (that i'm lazy to include here)
- misc.

========================================

Date: 24/04/22

Changelog:
- Dropped 230422 sched ricing, Picked a much better one (can't list 1 by 1, it's 2 page on git)
- schedutil: reduce frequencies slower
- schedutil: make iowait boost more energy efficient
- schedutil: add up/down frequency transition rate limits
- schedutil: enable iowait boost by default
- schedutil: enforce realtime priority
- kprofiles: set to balanced mode by default
- [EXP]: biofrost_defconfig: switch to 300Hz tickrate
- power on display asynchronously as early as possible
- mark display-wake kthread as performance critical
- remove duplicate pm_qos object used for unblanking
- don't add event timer for unused autorefresh feature

========================================

Date: 23/04/22

Changelog:
- ION Fixes and Improvements
- Picked some ricing from sultan
- Speed up mremap by 20x on large regions 
- jump_label backports
- Scheduler ricings (for overall improvements)
- Bump CPU Input Boost wake duration
- misc changes / under-the-hood improvements
