|==========| Biofrost - Test |=========|

Device: Realme 5 series (r5x)
Kernel Version: v4.14.277
Compiler: Proton Clang 13.0.0 (20210522)
Linker: GNU Binutils (ld.bfd)
By: mcdofrenchfreis

========================================

Date: 04/05/2022

* biofrost_defconfig: Enable PSTORE
* biofrost_defconfig: Disable PAN Emulation
* biofrost_defconfig: Reduce VBSWAP Disksize to 3GB
* biofrost_defconfig: Bump devfreq_boost frequency
* biofrost_defconfig: Disable CPUSS Dumping
* biofrost_defconfig: Disable SLUB per CPU partial cache
* biofrost_defconfig: Enable CONFIG_NET_SCH_FQ
* biofrost_defconfig: Disable Profiling
* biofrost_defconfig: Lower Input/Max Boost Frequency for Perf Cluster (CIB)
* binder: Reserve cache for small, high frequency memory allocations
* set binder_debug_mask=0 to suppress logging
* disable watchdog during suspend
* don't needlessly calculate diff time for cpuidle enter_state
* Do not allow any wakelocks to be held at qcacld-3.0
* include/linux/cgroup.h: export cgroup mutex
* Guard debugfs_real_fops usage
* some more mm commits for better quality of life
* fix ridiculous strnlen usage at ipa_v3
* fs: Reduce cache pressure
* silence some more useless system logspams
* trinket: use 67us latency for cdsp
* qg-soc: don't drop SOC if still charging 
* Minimize wakeup time
* Make zlib compression optional for pstore
* ion: Use a freezable unbound workqueue for the memory prefetch work items
* kgsl: use DMA APIs for memory pool cache maintenance
* binder: use pr_debug() instead of pr_*
* BACKPORTS: locking/rwsem, locking/mutex, locking/qrwlock
* fs: improve eventpoll logging to stop indicting timerfd
* smp2p: add proper retrigger detection
* smp2p: don't check for null before ipc_log_string()
* smp2p: Add memory barrier for irq_pending
* msm_venc: changes to improve quality
* drivers/char: adsprpc: remove PM_QoS implementation

========================================

Date: 02/05/22

* Drop Process Reclaim Low Memory Killer (PRLMK)
* Introduce and Enable Multi-generation LRU
* Enable LMKD
* Enable PSI
* Some tweaks for process reclaim 
* Some more optimizations for Memory Management
* Switch to fq_codel queue discipline
* Retune devfreq boost (drop it's boost input/wake duration + frequency)
* Avoid devfreq competing with low-priority tasks
* Compiled vDSO at -O3 Optimization level
* Add NEON accelerated XOR impelementation
* some more misc changes
* Introduce and Enable adrenoboost (GPU Boost)
* adrenoboost: finetuning algorithm - scale it a bit down
* adrenoboost: make each level with different debount limits for frequency change
* adrenoboost: add divider of the boosting for high frequency levels
* adrenoboost: control aggressivity for very high frequencies
* adrenoboost: damp down the aggressiveness in lowest frequency dividers
* adrenoboost: tune adrenoboost (tweak)
* adrenoboost: set to medium by default
* adreno_tz, binder: reduce logspam
* gpu: msm: reset the throttling limit (to avoid overheating on prolonged usage)
* qcom: Do not re-enable the interrupt after hardirq handler
* qcom: Relax wakeup source on failing to register IRQ
* sched: Utilize more higher capacity cpus in asymmetric systems
* sched: remove a duplicate trace print
* sched: always panic when scheduling in atomic context
* drop some MM commits for MGLRU's compatibility.
* fsync: optimize double-fysnc a bunch
* block, cfq: disable logging if trace is not enabled
* blk: disable IO_STAT completely
* kernel/cpuset: tweak top-app and foreground (uclamp)
* biofrost_defconfig: re-adjust cib tuning
* adrenoboost: set to low by default
* sched: ideally use 10ms scheduling periods
* binder_alloc: avoid page memory allocation in high memory
* update LZ4 decompressor module
* lz4: fix kernel decompression speed
* lz4: explicitly support in-place decompression
* lz4: declare LZ4_decompress_Safe_withPrefix64k static
* lz4: document deliberate use of `&'
* biofrost_defconfig: switch to LZ4 as default compress/decompress algorithm
* treewide: Remove VLA usage (for more free memory + memory allocation nodes)
* Switch to improved strnlen from glibc
* Improve 3x faster integer sqrt
* Implement the improved reciprocal_div algorithm
* lib/brtree/string/csum: fixes and improvements
* Move frequently used functions to headers and inline
* Remove explicit barriers from mmio ops where unneeded
* biofrost_defconfig: reduce log buffer to 4KB
* biofrost_defconfig: Enable ramdisk/ramfs compression using LZ4
* biofrost_defconfig: re-adjust CIB tuning
* biofrost_defconfig: Enable Garbage Collector for userspace wakelocks
* biofrost_defconfig: remove CPUFreq times driver
* biofrost_defconfig: remove MSM event timer
* biofrost_defconfig: disable syncookies
* mm: don't hog the cpu and zone lock in rmqueue_bulk()
* pdc: don't overwrite irq domain name on init
* npu_dev: initialize mutex_lock earlier
* pinctrl: don't lock around irq_set_irq_wake()
* don't allow s2idle to be used
* don't needlessly calculate diff time
* remove unneeded time profiling from ringbuffer submision
* disable adreno snapshot, coresight, and trace
* mailbox: remove debug cruft
* sync_file: speed up ioctl by omitting debug names
* kgsl: increase worker thread priority
* change default SCHED_RR timeslice from 100 ms to 1 jiffy
* kallsyms: lower alignment on ARM
* oppo_charger: enable fast charging
* misc: implement usb fast charging mode

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
