# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-03-16 00:34:43

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 348
- **总 Thread 数**: 34
- **大型 Thread** (>20封): 5 个

### 分类分布

- **PATCH**: 26 threads (275 邮件)
- **RFC**: 4 threads (61 邮件)
- **Question**: 1 threads (2 邮件)
- **GIT PULL**: 2 threads (7 邮件)
- **Other**: 1 threads (3 邮件)

---

## 📌 PATCH

共 26 个 thread

---

### Thread 1: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 41 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 13 Mar 2026 14:45:37 +0000

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 ARM MPAM（内存分区和监控）在 KVM/arm64 和 resctrl 中的集成，涉及多个补丁的提交和讨论。

1. **原始补丁内容**：本系列补丁的核心是将 MPAM 功能集成到 resctrl 中，使其能够在用户空间可用。补丁包括对 MPAM 控制和监控功能的支持，特别是对 L2/L3 缓存的 CPOR 控制和内存带宽最大值控制（MBW_MAX）的实现。

2. **历史讨论要点**：之前的讨论主要集中在如何简化代码以支持 MPAM 的不同功能，并处理与 resctrl 的集成问题。开发者们讨论了 MPAM 的特性如何映射到 resctrl 的资源，确保在不同硬件平台上保持一致性。

3. **本周的新讨论与进展**：本周的讨论主要围绕补丁的具体实现和测试，包括：
   - 对 MPAM 相关寄存器的初始化和上下文切换支持。
   - 处理特定硬件的缺陷（如 T241 的多个补丁），确保在不同情况下的稳定性。
   - 增加了对 CSU（缓存存储使用）计数器的支持，以及如何在 resctrl 中实现监控功能。
   - 引入了一个新的补丁框架，以便根据 MPAMF_IIDR 值启用特定的硬件工作区。
   - 最后，补丁还添加了初步的 MPAM 文档，以帮助用户理解可用的功能。

总体而言，这一系列补丁旨在增强 ARM 架构下的内存管理和监控能力，确保在虚拟化和资源控制方面的有效性。

#### 📝 邮件列表

1. **[03-13 14:45]** [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
2. **[03-13 14:45]** [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after applying configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
3. **[03-13 14:45]** [PATCH v6 02/40] arm_mpam: Reset when feature configuration bit unset
   - 发件人: Ben Horgan <ben.horgan@arm.com>
4. **[03-13 14:45]** [PATCH v6 03/40] arm64/sysreg: Add MPAMSM_EL1 register
   - 发件人: Ben Horgan <ben.horgan@arm.com>
5. **[03-13 14:45]** [PATCH v6 04/40] KVM: arm64: Preserve host MPAM configuration when changing traps
   - 发件人: Ben Horgan <ben.horgan@arm.com>
6. **[03-13 14:45]** [PATCH v6 05/40] KVM: arm64: Make MPAMSM_EL1 accesses UNDEF
   - 发件人: Ben Horgan <ben.horgan@arm.com>
7. **[03-13 14:45]** [PATCH v6 06/40] arm64: mpam: Context switch the MPAM registers
   - 发件人: Ben Horgan <ben.horgan@arm.com>
8. **[03-13 14:45]** [PATCH v6 07/40] arm64: mpam: Re-initialise MPAM regs when CPU comes online
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[03-13 14:45]** [PATCH v6 08/40] arm64: mpam: Drop the CONFIG_EXPERT restriction
   - 发件人: Ben Horgan <ben.horgan@arm.com>
10. **[03-13 14:45]** [PATCH v6 09/40] arm64: mpam: Advertise the CPUs MPAM limits to the driver
   - 发件人: Ben Horgan <ben.horgan@arm.com>
11. **[03-13 14:45]** [PATCH v6 10/40] arm64: mpam: Add cpu_pm notifier to restore MPAM sysregs
   - 发件人: Ben Horgan <ben.horgan@arm.com>
12. **[03-13 14:45]** [PATCH v6 11/40] arm64: mpam: Initialise and context switch the MPAMSM_EL1 register
   - 发件人: Ben Horgan <ben.horgan@arm.com>
13. **[03-13 14:45]** [PATCH v6 12/40] arm64: mpam: Add helpers to change a task or cpu's MPAM PARTID/PMG values
   - 发件人: Ben Horgan <ben.horgan@arm.com>
14. **[03-13 14:45]** [PATCH v6 13/40] KVM: arm64: Force guest EL1 to use user-space's partid configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
15. **[03-13 14:45]** [PATCH v6 14/40] arm_mpam: resctrl: Add boilerplate cpuhp and domain allocation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
16. **[03-13 14:45]** [PATCH v6 15/40] arm_mpam: resctrl: Pick the caches we will use as resctrl resources
   - 发件人: Ben Horgan <ben.horgan@arm.com>
17. **[03-13 14:45]** [PATCH v6 16/40] arm_mpam: resctrl: Implement resctrl_arch_reset_all_ctrls()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
18. **[03-13 14:45]** [PATCH v6 17/40] arm_mpam: resctrl: Add resctrl_arch_get_config()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
19. **[03-13 14:45]** [PATCH v6 18/40] arm_mpam: resctrl: Implement helpers to update configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
20. **[03-13 14:45]** [PATCH v6 19/40] arm_mpam: resctrl: Add plumbing against arm64 task and cpu hooks
   - 发件人: Ben Horgan <ben.horgan@arm.com>
21. **[03-13 14:45]** [PATCH v6 20/40] arm_mpam: resctrl: Add CDP emulation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
22. **[03-13 14:45]** [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind CONFIG_EXPERT
   - 发件人: Ben Horgan <ben.horgan@arm.com>
23. **[03-13 14:45]** [PATCH v6 22/40] arm_mpam: resctrl: Convert to/from MPAMs fixed-point formats
   - 发件人: Ben Horgan <ben.horgan@arm.com>
24. **[03-13 14:46]** [PATCH v6 23/40] arm_mpam: resctrl: Add rmid index helpers
   - 发件人: Ben Horgan <ben.horgan@arm.com>
25. **[03-13 14:46]** [PATCH v6 24/40] arm_mpam: resctrl: Wait for cacheinfo to be ready
   - 发件人: Ben Horgan <ben.horgan@arm.com>
26. **[03-13 14:46]** [PATCH v6 25/40] arm_mpam: resctrl: Add support for 'MB' resource
   - 发件人: Ben Horgan <ben.horgan@arm.com>
27. **[03-13 14:46]** [PATCH v6 26/40] arm_mpam: resctrl: Add kunit test for control format conversions
   - 发件人: Ben Horgan <ben.horgan@arm.com>
28. **[03-13 14:46]** [PATCH v6 27/40] arm_mpam: resctrl: Add monitor initialisation and domain boilerplate
   - 发件人: Ben Horgan <ben.horgan@arm.com>
29. **[03-13 14:46]** [PATCH v6 28/40] arm_mpam: resctrl: Add support for csu counters
   - 发件人: Ben Horgan <ben.horgan@arm.com>
30. **[03-13 14:46]** [PATCH v6 29/40] arm_mpam: resctrl: Allow resctrl to allocate monitors
   - 发件人: Ben Horgan <ben.horgan@arm.com>
31. **[03-13 14:46]** [PATCH v6 30/40] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
32. **[03-13 14:46]** [PATCH v6 31/40] arm_mpam: resctrl: Update the rmid reallocation limit
   - 发件人: Ben Horgan <ben.horgan@arm.com>
33. **[03-13 14:46]** [PATCH v6 32/40] arm_mpam: resctrl: Add empty definitions for assorted resctrl functions
   - 发件人: Ben Horgan <ben.horgan@arm.com>
34. **[03-13 14:46]** [PATCH v6 33/40] arm64: mpam: Select ARCH_HAS_CPU_RESCTRL
   - 发件人: Ben Horgan <ben.horgan@arm.com>
35. **[03-13 14:46]** [PATCH v6 34/40] arm_mpam: resctrl: Call resctrl_init() on platforms that can support resctrl
   - 发件人: Ben Horgan <ben.horgan@arm.com>
36. **[03-13 14:46]** [PATCH v6 35/40] arm_mpam: Add quirk framework
   - 发件人: Ben Horgan <ben.horgan@arm.com>
37. **[03-13 14:46]** [PATCH v6 36/40] arm_mpam: Add workaround for T241-MPAM-1
   - 发件人: Ben Horgan <ben.horgan@arm.com>
38. **[03-13 14:46]** [PATCH v6 37/40] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Ben Horgan <ben.horgan@arm.com>
39. **[03-13 14:46]** [PATCH v6 38/40] arm_mpam: Add workaround for T241-MPAM-6
   - 发件人: Ben Horgan <ben.horgan@arm.com>
40. **[03-13 14:46]** [PATCH v6 39/40] arm_mpam: Quirk CMN-650's CSU NRDY behaviour
   - 发件人: Ben Horgan <ben.horgan@arm.com>
41. **[03-13 14:46]** [PATCH v6 40/40] arm64: mpam: Add initial MPAM documentation
   - 发件人: Ben Horgan <ben.horgan@arm.com>

---

### Thread 2: [PATCH v14 00/30] Tracefs support for pKVM

**📧 邮件数**: 38 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  9 Mar 2026 16:24:46 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 pKVM 的 Tracefs 支持的补丁系列（PATCH v14 00/30），主要涉及如何在虚拟化环境中实现高效的事件跟踪和调试。

1. **原始补丁内容**：该补丁系列旨在为 pKVM 超级虚拟机提供 Tracefs 支持，允许在保护模式下使用 Tracefs 进行调试和性能分析。补丁引入了新的接口和数据结构，以便在内核和超虚拟机之间共享跟踪事件。

2. **历史讨论要点**：之前的讨论集中在如何设计和实现一个简单的环形缓冲区，以便超虚拟机能够写入事件，同时内核能够读取这些事件。补丁还讨论了如何处理环形缓冲区的元数据和事件格式。

3. **本周新讨论和进展**：
   - **补丁进展**：本周的讨论涉及多个补丁的提交，包括对环形缓冲区的改进、事件支持的添加以及 Tracefs 目录的创建。补丁中还增加了对 nVHE/pKVM 超级虚拟机的跟踪能力，允许记录进入和退出事件（hyp_enter/hyp_exit）。
   - **自测试支持**：引入了用于测试 Tracefs 接口的自测试事件，确保在不同情况下的功能正常。
   - **社区反馈**：参与者对补丁进行了审查和反馈，Steven Rostedt 和 Marc Zyngier 等人表示已将相关补丁合并到他们的代码库中，推动了该功能的进一步开发。

总体而言，本周的讨论和进展表明，Tracefs 支持 pKVM 的实现正在稳步推进，社区对该功能的兴趣和支持也在增加。

#### 📝 邮件列表

1. **[03-09 16:24]** [PATCH v14 00/30] Tracefs support for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-09 16:24]** [PATCH v14 01/30] ring-buffer: Add page statistics to the meta-page
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-09 16:24]** [PATCH v14 02/30] ring-buffer: Store bpage pointers into subbuf_ids
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[03-09 16:24]** [PATCH v14 03/30] ring-buffer: Introduce ring-buffer remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[03-09 16:24]** [PATCH v14 04/30] ring-buffer: Add non-consuming read for ring-buffer remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[03-09 16:24]** [PATCH v14 05/30] tracing: Introduce trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[03-09 16:24]** [PATCH v14 06/30] tracing: Add reset to trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[03-09 16:24]** [PATCH v14 07/30] tracing: Add non-consuming read to trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[03-09 16:24]** [PATCH v14 08/30] tracing: Add init callback to trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[03-09 16:24]** [PATCH v14 09/30] tracing: Add events to trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[03-09 16:24]** [PATCH v14 10/30] tracing: Add events/ root files to trace remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[03-09 16:24]** [PATCH v14 11/30] tracing: Add helpers to create trace remote events
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[03-09 16:24]** [PATCH v14 12/30] ring-buffer: Export buffer_data_page and macros
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[03-09 16:24]** [PATCH v14 13/30] tracing: Introduce simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[03-09 16:25]** [PATCH v14 14/30] tracing: Add a trace remote module for testing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[03-09 16:25]** [PATCH v14 15/30] tracing: selftests: Add trace remote tests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[03-09 16:25]** [PATCH v14 16/30] Documentation: tracing: Add tracing remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[03-09 16:25]** [PATCH v14 17/30] tracing: load/unload page callbacks for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[03-09 16:25]** [PATCH v14 18/30] tracing: Check for undefined symbols in simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
20. **[03-09 16:25]** [PATCH v14 19/30] KVM: arm64: Add PKVM_DISABLE_STAGE2_ON_PANIC
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
21. **[03-09 16:25]** [PATCH v14 20/30] KVM: arm64: Add clock support to nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
22. **[03-09 16:25]** [PATCH v14 21/30] KVM: arm64: Initialise hyp_nr_cpus for nVHE hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
23. **[03-09 16:25]** [PATCH v14 22/30] KVM: arm64: Support unaligned fixmap in the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
24. **[03-09 16:25]** [PATCH v14 23/30] KVM: arm64: Add tracing capability for the
 nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
25. **[03-09 16:25]** [PATCH v14 24/30] KVM: arm64: Add trace remote for the nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
26. **[03-09 16:25]** [PATCH v14 25/30] KVM: arm64: Sync boot clock with the nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
27. **[03-09 16:25]** [PATCH v14 26/30] KVM: arm64: Add trace reset to the nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
28. **[03-09 16:25]** [PATCH v14 27/30] KVM: arm64: Add event support to the nVHE/pKVM hyp
 and trace remote
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
29. **[03-09 16:25]** [PATCH v14 28/30] KVM: arm64: Add hyp_enter/hyp_exit events to
 nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
30. **[03-09 16:25]** [PATCH v14 29/30] KVM: arm64: Add selftest event support to nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
31. **[03-09 16:25]** [PATCH v14 30/30] tracing: selftests: Add hypervisor trace remote tests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
32. **[03-10 10:43]** Re: [PATCH v14 00/30] Tracefs support for pKVM
   - 发件人: Steven Rostedt <rostedt@goodmis.org>
33. **[03-11 08:58]** Re: (subset) [PATCH v14 00/30] Tracefs support for pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
34. **[03-11 09:02]** Re: [PATCH v14 00/30] Tracefs support for pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
35. **[03-11 15:18]** Re: [PATCH v14 18/30] tracing: Check for undefined symbols in
 simple_ring_buffer
   - 发件人: Nathan Chancellor <nathan@kernel.org>
36. **[03-12 08:55]** Re: [PATCH v14 18/30] tracing: Check for undefined symbols in
 simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
37. **[03-12 14:07]** Re: [PATCH v14 18/30] tracing: Check for undefined symbols in
 simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
38. **[03-12 13:40]** Re: [PATCH v14 18/30] tracing: Check for undefined symbols in
 simple_ring_buffer
   - 发件人: Nathan Chancellor <nathan@kernel.org>

---

### Thread 3: [PATCH v3 00/36] KVM: arm64: Add support for protected guest memory with pKVM

**📧 邮件数**: 34 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  5 Mar 2026 14:43:13 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上支持受保护来宾内存的补丁系列（PATCH v3 00/36）。该补丁旨在通过 pKVM（Protected Kernel Virtual Machine）实现对受保护虚拟机的支持，主要包括对异常处理、内存管理和特性限制的改进。

在历史讨论中，Will Deacon 提出了多个补丁，涵盖了从处理阶段-2 页表的初始化失败到支持受保护虚拟机的内存分配等多个方面的改动。补丁中包括了对异常注入逻辑的重构、对不支持特性的隐藏、以及对受保护虚拟机的内存操作限制等。

在本周的新讨论中，Fuad Tabba 对多个补丁进行了测试和审核，确认了其有效性并给予了“Reviewed-by”的反馈。这些补丁包括了对页表映射的错误处理、异常处理逻辑的重构、以及允许用户空间创建受保护虚拟机的功能等。整体来看，本周的讨论主要集中在对补丁的确认和审核上，表明这些改动正在逐步得到认可并准备合并。

#### 📝 邮件列表

1. **[03-05 14:43]** [PATCH v3 00/36] KVM: arm64: Add support for protected guest memory with pKVM
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-05 14:43]** [PATCH v3 01/36] KVM: arm64: Don't leak stage-2 page-table if VM fails to init under pKVM
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-05 14:43]** [PATCH v3 02/36] KVM: arm64: Move handle check into pkvm_pgtable_stage2_destroy_range()
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-05 14:43]** [PATCH v3 03/36] KVM: arm64: Rename __pkvm_pgtable_stage2_unmap()
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-05 14:43]** [PATCH v3 04/36] KVM: arm64: Don't advertise unsupported features for protected guests
   - 发件人: Will Deacon <will@kernel.org>
6. **[03-05 14:43]** [PATCH v3 06/36] KVM: arm64: Remove is_protected_kvm_enabled() checks from hypercalls
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-05 14:43]** [PATCH v3 07/36] KVM: arm64: Ignore MMU notifier callbacks for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-05 14:43]** [PATCH v3 08/36] KVM: arm64: Prevent unsupported memslot operations on protected VMs
   - 发件人: Will Deacon <will@kernel.org>
9. **[03-05 14:43]** [PATCH v3 09/36] KVM: arm64: Ignore -EAGAIN when mapping in pages for the pKVM host
   - 发件人: Will Deacon <will@kernel.org>
10. **[03-05 14:43]** [PATCH v3 10/36] KVM: arm64: Split teardown hypercall into two phases
   - 发件人: Will Deacon <will@kernel.org>
11. **[03-05 14:43]** [PATCH v3 13/36] KVM: arm64: Handle aborts from protected VMs
   - 发件人: Will Deacon <will@kernel.org>
12. **[03-05 14:43]** [PATCH v3 16/36] KVM: arm64: Factor out pKVM host exception injection logic
   - 发件人: Will Deacon <will@kernel.org>
13. **[03-05 14:43]** [PATCH v3 17/36] KVM: arm64: Support translation faults in inject_host_exception()
   - 发件人: Will Deacon <will@kernel.org>
14. **[03-05 14:43]** [PATCH v3 18/36] KVM: arm64: Inject SIGSEGV on illegal accesses
   - 发件人: Will Deacon <will@kernel.org>
15. **[03-05 14:43]** [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Will Deacon <will@kernel.org>
16. **[03-05 14:43]** [PATCH v3 31/36] KVM: arm64: Add some initial documentation for pKVM
   - 发件人: Will Deacon <will@kernel.org>
17. **[03-05 14:43]** [PATCH v3 36/36] KVM: arm64: Rename PKVM_PAGE_STATE_MASK
   - 发件人: Will Deacon <will@kernel.org>
18. **[03-11 10:07]** Re: [PATCH v3 00/36] KVM: arm64: Add support for protected guest
 memory with pKVM
   - 发件人: Fuad Tabba <tabba@google.com>
19. **[03-11 10:10]** Re: [PATCH v3 09/36] KVM: arm64: Ignore -EAGAIN when mapping in pages
 for the pKVM host
   - 发件人: Fuad Tabba <tabba@google.com>
20. **[03-11 10:12]** Re: [PATCH v3 16/36] KVM: arm64: Factor out pKVM host exception
 injection logic
   - 发件人: Fuad Tabba <tabba@google.com>
21. **[03-11 10:12]** Re: [PATCH v3 17/36] KVM: arm64: Support translation faults in inject_host_exception()
   - 发件人: Fuad Tabba <tabba@google.com>
22. **[03-11 10:13]** Re: [PATCH v3 18/36] KVM: arm64: Inject SIGSEGV on illegal accesses
   - 发件人: Fuad Tabba <tabba@google.com>
23. **[03-11 10:15]** Re: [PATCH v3 02/36] KVM: arm64: Move handle check into pkvm_pgtable_stage2_destroy_range()
   - 发件人: Fuad Tabba <tabba@google.com>
24. **[03-11 10:15]** Re: [PATCH v3 04/36] KVM: arm64: Don't advertise unsupported features
 for protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
25. **[03-11 10:16]** Re: [PATCH v3 06/36] KVM: arm64: Remove is_protected_kvm_enabled()
 checks from hypercalls
   - 发件人: Fuad Tabba <tabba@google.com>
26. **[03-11 10:16]** Re: [PATCH v3 08/36] KVM: arm64: Prevent unsupported memslot
 operations on protected VMs
   - 发件人: Fuad Tabba <tabba@google.com>
27. **[03-11 10:22]** Re: [PATCH v3 10/36] KVM: arm64: Split teardown hypercall into two phases
   - 发件人: Fuad Tabba <tabba@google.com>
28. **[03-11 10:22]** Re: [PATCH v3 13/36] KVM: arm64: Handle aborts from protected VMs
   - 发件人: Fuad Tabba <tabba@google.com>
29. **[03-11 10:25]** Re: [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected
 VMs when pKVM is enabled
   - 发件人: Fuad Tabba <tabba@google.com>
30. **[03-11 10:25]** Re: [PATCH v3 31/36] KVM: arm64: Add some initial documentation for pKVM
   - 发件人: Fuad Tabba <tabba@google.com>
31. **[03-11 10:26]** Re: [PATCH v3 36/36] KVM: arm64: Rename PKVM_PAGE_STATE_MASK
   - 发件人: Fuad Tabba <tabba@google.com>
32. **[03-11 12:48]** Re: [PATCH v3 01/36] KVM: arm64: Don't leak stage-2 page-table if VM
 fails to init under pKVM
   - 发件人: Fuad Tabba <tabba@google.com>
33. **[03-11 12:49]** Re: [PATCH v3 03/36] KVM: arm64: Rename __pkvm_pgtable_stage2_unmap()
   - 发件人: Fuad Tabba <tabba@google.com>
34. **[03-11 12:50]** Re: [PATCH v3 07/36] KVM: arm64: Ignore MMU notifier callbacks for
 protected VMs
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 4: [PATCH v5 00/41] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 25 | **👥 参与者**: 5 | **📅 开始时间**: Tue, 24 Feb 2026 17:56:39 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 ARM MPAM（内存带宽分配管理）在 KVM/arm64 和 resctrl 中的集成，主要集中在一系列补丁的提交与审查。

1. **原始补丁内容**：Ben Horgan 提出的补丁系列（PATCH v5 00/41）旨在添加 KVM/arm64 和 resctrl 的集成代码，更新 CDP（控制数据路径）仿真以匹配 resctrl 接口，允许 L2 和 L3 资源单独启用 CDP，并进行了一些重构和小改动。

2. **之前讨论要点**：历史讨论中，参与者对补丁进行了审查和测试，确认了补丁的有效性，并提出了一些改进意见。例如，Marc Zyngier 对于 KVM 中的 PARTID 配置提出了质疑，认为应避免主机配置影响 pKVM 的行为。

3. **本周的新讨论与进展**：本周的讨论主要集中在补丁的审查和一些潜在问题的解决方案上。Gavin Shan 和 Zeng Heng 对多个补丁进行了确认和审查，特别是关于 CDP 启用时的 limbo 状态问题，提出了短期解决方案，即将 CDP 隐藏在 CONFIG_EXPERT 后以避免用户意外触发错误。此外，Ben Horgan 决定放弃某个补丁，以简化代码和避免不必要的复杂性。

总体而言，邮件线程展示了开发者们在 ARM MPAM 集成过程中的积极协作与问题解决。

#### 📝 邮件列表

1. **[02-24 17:56]** [PATCH v5 00/41] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
2. **[02-24 17:56]** [PATCH v5 06/41] arm64: mpam: Drop the CONFIG_EXPERT restriction
   - 发件人: Ben Horgan <ben.horgan@arm.com>
3. **[02-24 17:56]** [PATCH v5 07/41] arm64: mpam: Advertise the CPUs MPAM limits to the driver
   - 发件人: Ben Horgan <ben.horgan@arm.com>
4. **[02-24 17:56]** [PATCH v5 10/41] arm64: mpam: Add helpers to change a task or cpu's MPAM PARTID/PMG values
   - 发件人: Ben Horgan <ben.horgan@arm.com>
5. **[02-24 17:56]** [PATCH v5 11/41] KVM: arm64: Force guest EL1 to use user-space's partid configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
6. **[02-24 17:56]** [PATCH v5 12/41] KVM: arm64: Use kernel-space partid configuration for hypercalls
   - 发件人: Ben Horgan <ben.horgan@arm.com>
7. **[02-24 17:56]** [PATCH v5 13/41] arm_mpam: resctrl: Add boilerplate cpuhp and domain allocation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
8. **[02-24 17:57]** [PATCH v5 31/41] arm_mpam: resctrl: Add resctrl_arch_rmid_read() and resctrl_arch_reset_rmid()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[02-24 17:57]** [PATCH v5 38/41] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Ben Horgan <ben.horgan@arm.com>
10. **[03-01 09:28]** Re: [PATCH v5 38/41] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Fenghua Yu <fenghuay@nvidia.com>
11. **[03-02 17:11]** Re: [PATCH v5 38/41] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Ben Horgan <ben.horgan@arm.com>
12. **[03-02 18:15]** Re: [PATCH v5 12/41] KVM: arm64: Use kernel-space partid configuration for hypercalls
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[03-03 16:33]** Re: [PATCH v5 12/41] KVM: arm64: Use kernel-space partid
 configuration for hypercalls
   - 发件人: Ben Horgan <ben.horgan@arm.com>
14. **[03-07 17:29]** Re: [PATCH v5 31/41] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
 and resctrl_arch_reset_rmid()
   - 发件人: Zeng Heng <zengheng4@huawei.com>
15. **[03-09 16:42]** Re: [PATCH v5 06/41] arm64: mpam: Drop the CONFIG_EXPERT restriction
   - 发件人: Gavin Shan <gshan@redhat.com>
16. **[03-09 16:43]** Re: [PATCH v5 07/41] arm64: mpam: Advertise the CPUs MPAM limits to
 the driver
   - 发件人: Gavin Shan <gshan@redhat.com>
17. **[03-09 16:44]** Re: [PATCH v5 10/41] arm64: mpam: Add helpers to change a task or
 cpu's MPAM PARTID/PMG values
   - 发件人: Gavin Shan <gshan@redhat.com>
18. **[03-09 16:45]** Re: [PATCH v5 11/41] KVM: arm64: Force guest EL1 to use user-space's
 partid configuration
   - 发件人: Gavin Shan <gshan@redhat.com>
19. **[03-09 16:30]** Re: [PATCH v5 31/41] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
 and resctrl_arch_reset_rmid()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
20. **[03-09 10:39]** Re: [PATCH v5 38/41] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Fenghua Yu <fenghuay@nvidia.com>
21. **[03-10 11:23]** Re: [PATCH v5 31/41] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
 and resctrl_arch_reset_rmid()
   - 发件人: Zeng Heng <zengheng4@huawei.com>
22. **[03-10 16:17]** Re: [PATCH v5 13/41] arm_mpam: resctrl: Add boilerplate cpuhp and
 domain allocation
   - 发件人: Gavin Shan <gshan@redhat.com>
23. **[03-10 10:34]** Re: [PATCH v5 13/41] arm_mpam: resctrl: Add boilerplate cpuhp and
 domain allocation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
24. **[03-10 11:26]** Re: [PATCH v5 38/41] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Ben Horgan <ben.horgan@arm.com>
25. **[03-13 09:43]** Re: [PATCH v5 12/41] KVM: arm64: Use kernel-space partid
 configuration for hypercalls
   - 发件人: Ben Horgan <ben.horgan@arm.com>

---

### Thread 5: [PATCH 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)

**📧 邮件数**: 19 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  2 Mar 2026 16:57:53 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 Arm C1-Pro 处理器的一个已知缺陷（erratum 4193714，CVE-2026-0995）的补丁方案。该缺陷可能导致在执行 TLBI+DSB 序列时，未能确保所有 SME（可扩展矩阵扩展）内存访问的完成，从而可能在内存访问未完成时重用页面。

历史讨论中，Catalin Marinas 提出了四个补丁，旨在通过在 TLB 失效后对所有受影响的 CPU 执行本地 DSB 操作来解决该问题。补丁的主要内容包括：为内核 TLB 维护添加新的同步函数、传递相应的 mm 结构以限制特定任务的修复、以及针对早期 CME DVMSync 确认的工作方案。

在本周的新讨论中，参与者们对补丁的细节进行了深入探讨。Vladimir Murzin 提出了对 SME 支持的理解，Mark Rutland 和 Will Deacon 则讨论了补丁在不同情况下的有效性和潜在问题。Will 还提到，可能需要在特定情况下主动执行 DSB，以确保在执行 TLB 刷新时的内存一致性。整体来看，讨论集中在如何确保补丁在实际应用中的可靠性和性能优化上。

#### 📝 邮件列表

1. **[03-02 16:57]** [PATCH 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[03-02 16:57]** [PATCH 1/4] arm64: tlb: Use __tlbi_sync_s1ish_kernel() for kernel TLB maintenance
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[03-02 16:57]** [PATCH 2/4] arm64: tlb: Pass the corresponding mm to __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
4. **[03-02 16:57]** [PATCH 3/4] arm64: errata: Work around early CME DVMSync acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-03 13:12]** Re: [PATCH 1/4] arm64: tlb: Use __tlbi_sync_s1ish_kernel() for
 kernel TLB maintenance
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[03-05 11:27]** Re: [PATCH 1/4] arm64: tlb: Use __tlbi_sync_s1ish_kernel() for
 kernel TLB maintenance
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
7. **[03-05 14:32]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-05 14:33]** Re: [PATCH 2/4] arm64: tlb: Pass the corresponding mm to
 __tlbi_sync_s1ish()
   - 发件人: Will Deacon <will@kernel.org>
9. **[03-05 19:19]** Re: [PATCH 2/4] arm64: tlb: Pass the corresponding mm to
 __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
10. **[03-06 11:15]** Re: [PATCH 2/4] arm64: tlb: Pass the corresponding mm to
 __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
11. **[03-06 12:00]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
12. **[03-09 10:13]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
13. **[03-09 12:12]** Re: [PATCH 1/4] arm64: tlb: Use __tlbi_sync_s1ish_kernel() for
 kernel TLB maintenance
   - 发件人: Mark Rutland <mark.rutland@arm.com>
14. **[03-10 15:35]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
15. **[03-12 14:55]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
16. **[03-12 15:00]** Re: [PATCH 2/4] arm64: tlb: Pass the corresponding mm to
 __tlbi_sync_s1ish()
   - 发件人: Will Deacon <will@kernel.org>
17. **[03-13 15:48]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
18. **[03-13 15:58]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
19. **[03-13 16:27]** Re: [PATCH 2/4] arm64: tlb: Pass the corresponding mm to
 __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 6: [PATCH v15 0/8] support FEAT_LSUI

**📧 邮件数**: 16 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 27 Feb 2026 15:16:57 +0000

#### 🤖 AI 总结

本邮件线程讨论了支持 Arm 架构新特性 FEAT_LSUI 的补丁集（PATCH v15 0/8）。该特性允许在特权级别下访问用户内存，而无需清除 PSTATE.PAN 位，主要应用于 futex 原子操作等。

在历史讨论中，Yeoreum Yun 提出了该补丁集，重点在于重构 futex 原子操作，以便利用 FEAT_LSUI 进行更高效的用户内存访问。补丁集的更新包括修正了之前版本中的一些问题，并对代码进行了清理。

在本周的新讨论中，Catalin Marinas 对补丁集中的具体实现提出了一些建议和问题，包括对代码中不必要的头文件引用的移除、使用命名操作数的建议，以及对 futex 操作中循环和错误处理的讨论。Yeoreum Yun 对这些反馈表示感谢，并确认将根据讨论结果进行相应的修改。此外，Yeoreum 还提到将更新补丁版本以反映这些更改。

总体来看，本周的讨论主要集中在代码细节的优化和逻辑的清晰性上，参与者之间的互动积极，推动了补丁集的进一步完善。

#### 📝 邮件列表

1. **[02-27 15:16]** [PATCH v15 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[02-27 15:17]** [PATCH v15 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[02-27 15:17]** [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[02-27 15:17]** [PATCH v15 7/8] KVM: arm64: use CAST instruction for swapping guest descriptor
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[03-12 14:41]** Re: [PATCH v15 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
6. **[03-12 14:53]** Re: [PATCH v15 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[03-12 14:54]** Re: [PATCH v15 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
8. **[03-12 14:57]** Re: [PATCH v15 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[03-12 18:17]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
10. **[03-13 09:23]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
11. **[03-13 09:56]** Re: [PATCH v15 7/8] KVM: arm64: use CAST instruction for swapping
 guest descriptor
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
12. **[03-13 09:59]** Re: [PATCH v15 7/8] KVM: arm64: use CAST instruction for swapping
 guest descriptor
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
13. **[03-13 14:42]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
14. **[03-13 14:56]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
15. **[03-13 16:43]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
16. **[03-13 16:51]** Re: [PATCH v15 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 7: [PATCH v17 0/8] support FEAT_LSUI

**📧 邮件数**: 9 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 14 Mar 2026 17:51:25 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于支持 Arm 架构中的 FEAT_LSUI 特性的补丁集（PATCH v17 0/8）。FEAT_LSUI 是自 Armv9.6 起引入的特性，允许特权级代码在不清除 PSTATE.PAN 位的情况下访问用户内存。该补丁集主要应用于 futex 原子操作等功能。

在历史讨论中，补丁经历了多个版本的迭代，从 v1 到 v17，主要修改包括移除不必要的循环、重构代码、添加 LSUI 配置检查等。每个版本都在逐步完善对 FEAT_LSUI 的支持，确保其在不同情况下的兼容性。

本周的新讨论中，Yeoreum Yun 提交了补丁的具体实现，主要包括：
1. **补丁内容**：添加对 FEAT_LSUI 的 CPU 特性检测，支持 futex 原子操作，使用 CAST 指令来交换虚拟机描述符，并在 Kconfig 中添加 LSUI 的支持选项。
2. **进展**：补丁得到了 Marc Zyngier 和 Catalin Marinas 的认可，表明其在代码审查中获得了积极反馈。

总的来说，本周的讨论集中在实现和完善对 FEAT_LSUI 的支持上，旨在提升 Arm 架构下内核的性能和安全性。

#### 📝 邮件列表

1. **[03-14 17:51]** [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[03-14 17:51]** [PATCH v17 1/8] arm64: cpufeature: add FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[03-14 17:51]** [PATCH v17 2/8] KVM: arm64: expose FEAT_LSUI to guest
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[03-14 17:51]** [PATCH v17 3/8] KVM: arm64: kselftest: set_id_regs: add test for FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[03-14 17:51]** [PATCH v17 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[03-14 17:51]** [PATCH v17 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[03-14 17:51]** [PATCH v17 6/8] arm64: armv8_deprecated: disable swp emulation when FEAT_LSUI present
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[03-14 17:51]** [PATCH v17 7/8] KVM: arm64: use CAST instruction for swapping guest descriptor
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[03-14 17:51]** [PATCH v17 8/8] arm64: Kconfig: add support for LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 8: [PATCH RESEND 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs

**📧 邮件数**: 9 | **👥 参与者**: 4 | **📅 开始时间**: Sun,  8 Mar 2026 23:18:27 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，目的是在 debugfs 中暴露影子页表，以提高调试和测试的能力。补丁的核心内容是创建一个名为 "nested" 的目录，针对每个有效的 s2 MMU，提供可读的影子页表文件，文件名格式为 0x<vttbr>-0x<vtcr>-s2-{en,dis}abled。

在历史讨论中，Wei-Lin Chang 提出了这个补丁，并解释了其设计意图及实现方式。补丁的实现依赖于 CONFIG_PTDUMP_STAGE2_DEBUGFS 配置选项，以确保调试信息的可控性。

在本周的新讨论中，参与者们对补丁进行了进一步的审查和讨论。Joey Gouly 建议将新目录的创建也纳入 CONFIG_PTDUMP_STAGE2_DEBUGFS 的保护范围，Wei-Lin Chang 最终同意了这一建议。此外，Sebastian Ene 提出了使用宏来隐藏某些定义的大小，以提高代码的可读性和安全性。整体来看，讨论氛围积极，补丁得到了认可，并在细节上进行了优化。

#### 📝 邮件列表

1. **[03-08 23:18]** [PATCH RESEND 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-08 23:18]** [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[03-10 15:26]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Joey Gouly <joey.gouly@arm.com>
4. **[03-10 16:17]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[03-10 16:50]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-10 17:41]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[03-11 15:41]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[03-13 22:28]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[03-14 09:39]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 9: [PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition
 the PMU

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 11 Mar 2026 11:59:31 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为“[PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition the PMU”的补丁，该补丁旨在引入一种方法来对性能监控单元（PMU）进行分区。

在历史讨论中，补丁的主要目的是优化ARM架构下的PMU使用，特别是在虚拟化环境中如何有效管理计数器。参与者们讨论了如何处理不同计数器的可用性及其在宿主机和虚拟机之间的分配。

本周的新讨论中，主要参与者James Clark和Colton Lewis进行了多次互动，提出了一些技术细节和改进建议。Clark指出了补丁中的几个小问题，例如错误返回值未被调用者使用，以及计数器的全局定义可能导致误解。他还提到了一些自测未能捕捉到的错误，建议增加对非零计数值的检查。此外，Clark强调了在处理特定计数器时需要特别注意的情况，特别是ARMV8架构下的周期计数器。

Lewis对Clark的反馈表示感谢，并承诺将根据讨论结果进行补丁的修改，包括删除不必要的功能和修正错误。总体来看，本周的讨论集中在补丁的细节完善和潜在问题的解决上，显示出开发者们对提高代码质量的重视。

#### 📝 邮件列表

1. **[03-11 11:59]** Re: [PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition
 the PMU
   - 发件人: James Clark <james.clark@linaro.org>
2. **[03-11 12:00]** Re: [PATCH v6 06/19] perf: arm_pmuv3: Keep out of guest counter
 partition
   - 发件人: James Clark <james.clark@linaro.org>
3. **[03-11 12:01]** Re: [PATCH v6 11/19] KVM: arm64: Context swap Partitioned PMU guest
 registers
   - 发件人: James Clark <james.clark@linaro.org>
4. **[03-11 17:45]** Re: [PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition
 the PMU
   - 发件人: James Clark <james.clark@linaro.org>
5. **[03-12 22:13]** Re: [PATCH v6 16/19] KVM: arm64: Add vCPU device attr to partition
 the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[03-12 22:37]** Re: [PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition
 the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[03-12 22:37]** Re: [PATCH v6 04/19] perf: arm_pmuv3: Introduce method to partition
 the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[03-12 22:39]** Re: [PATCH v6 06/19] perf: arm_pmuv3: Keep out of guest counter partition
   - 发件人: Colton Lewis <coltonlewis@google.com>
9. **[03-12 22:39]** Re: [PATCH v6 11/19] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 10: [PATCH v16 0/8] support FEAT_LSUI

**📧 邮件数**: 9 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 12 Mar 2026 17:52:35 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于支持 Armv9.6 的 FEAT_LSUI 特性的补丁集（PATCH v16 0/8）。FEAT_LSUI 允许特权级代码在不清除 PSTATE.PAN 位的情况下访问用户内存，主要应用于 futex 原子操作等。

在历史讨论中，补丁集经历了多个版本的迭代，逐步完善了对 FEAT_LSUI 的支持，包括添加 CPU 特性检测、重构 futex 原子操作、以及在 KVM 中暴露该特性给虚拟机等。补丁的主要变化包括移除不必要的操作、简化代码结构以及增加测试覆盖。

本周的新讨论中，Yeoreum Yun 提交了补丁的最终版本，详细介绍了每个补丁的功能和实现细节。具体进展包括：
1. 添加了对 FEAT_LSUI 的 Kconfig 支持。
2. 在 KVM 中使用 CAST 指令进行交换操作，避免了清除 PAN 位的需要。
3. 对 futex 原子操作进行了重构，以利用 FEAT_LSUI 提供的指令。
4. 讨论了禁用 SWP 指令的仿真，以消除 PAN 切换的需求。

整体来看，该补丁集旨在提升 Arm64 架构在处理用户内存时的效率和安全性。

#### 📝 邮件列表

1. **[03-12 17:52]** [PATCH v16 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[03-12 17:52]** [PATCH v16 1/8] arm64: cpufeature: add FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[03-12 17:52]** [PATCH v16 2/8] KVM: arm64: expose FEAT_LSUI to guest
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[03-12 17:52]** [PATCH v16 3/8] KVM: arm64: kselftest: set_id_regs: add test for FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[03-12 17:52]** [PATCH v16 4/8] arm64: futex: refactor futex atomic operation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[03-12 17:52]** [PATCH v16 5/8] arm64: futex: support futex with FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[03-12 17:52]** [PATCH v16 6/8] arm64: armv8_deprecated: disable swp emulation when FEAT_LSUI present
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[03-12 17:52]** [PATCH v16 7/8] KVM: arm64: use CAST instruction for swapping guest descriptor
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[03-12 17:52]** [PATCH v16 8/8] arm64: Kconfig: add support for LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 11: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 25 Feb 2026 12:04:16 +0800

#### 🤖 AI 总结

本邮件线程讨论了针对 Armv9.5 架构引入的硬件脏页状态跟踪结构（HDBSS）功能的支持，主要集中在相关的补丁（PATCH v3 0/5）及其实现细节。

**原始补丁内容**：该补丁系列旨在通过硬件支持来增强对翻译表描述符脏状态的跟踪，以减少脏页扫描的开销。HDBSS 功能在迁移开始时通过用户空间的 ioctl 启用，仅在 VHE 模式下支持。

**之前讨论要点**：在历史讨论中，参与者探讨了如何有效地保存和恢复与 HDBSS 相关的寄存器状态。Leonardo Bras 提出了一些建议，认为可以简化寄存器的保存方式，以避免在 vcpu_put/get 中进行复杂的掩码操作。Tian Zheng 则强调了保持状态结构清晰的重要性，并与 Oliver Upton 进行了深入讨论。

**本周新讨论进展**：本周的讨论中，Tian Zheng 和 Leonardo Bras 确认了在 vcpu_put 时的处理方式，并讨论了在 kvm_arch_vcpu_ioctl_run() 和 kvm_sched_out() 中进行 HDBSS 刷新的必要性。双方一致认为，HDBSS 不适用于嵌套或其他复杂情况，因此只需在上述两个函数中执行刷新。Leonardo Bras 表示将根据讨论更新代码并进行测试，以确保没有遗漏任何边缘情况。

总体来看，讨论围绕 HDBSS 的实现细节展开，参与者积极提出建议并达成共识，推动了补丁的完善。

#### 📝 邮件列表

1. **[02-25 12:04]** [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
2. **[02-25 12:04]** [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[03-04 15:40]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[03-06 17:27]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
5. **[03-06 15:01]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[03-12 14:17]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
7. **[03-12 12:06]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[03-12 21:13]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
9. **[03-12 14:58]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 12: [PATCH v3 0/3] Enforce host page-size alignment for shared buffers

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  9 Mar 2026 15:56:22 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于在共享缓冲区中强制执行主机页面大小对齐的补丁系列（[PATCH v3 0/3]），主要由Aneesh Kumar K.V提出。该补丁的目的是解决在私有内存虚拟机中，主机和虚拟机之间共享缓冲区的对齐要求。由于这些共享缓冲区需要与主机内核对齐，因此必须符合主机的页面大小。

在历史讨论中，补丁的背景主要涉及到虚拟机内核在分配与超管共享的缓冲区时，必须施加额外的约束。错误的内存访问可能导致内核崩溃，因此引入了新的辅助函数`mem_decrypt_granule_size()`和`mem_decrypt_align()`来确保缓冲区的对齐和大小。

本周的新讨论中，Aneesh Kumar K.V 提出了三个补丁的具体实现，分别涉及到swiotlb的内存分配、DMA直接分配以及引入Realm Host Interface。补丁的更新包括修复了之前版本中的一些问题，并引入了新的内存对齐机制，以确保在共享内存的情况下，缓冲区的大小和对齐符合主机的要求。

此外，Suzuki K Poulose 提出了对补丁的细微建议，讨论了在主机未实现对齐时的处理方式。邮件中还提到了一些构建错误，提示开发者需要修复这些问题以确保补丁的有效性。整体来看，本周的讨论集中在补丁的实现细节和潜在问题的解决上。

#### 📝 邮件列表

1. **[03-09 15:56]** [PATCH v3 0/3] Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[03-09 15:56]** [PATCH v3 1/3] dma-direct: swiotlb: handle swiotlb alloc/free outside __dma_direct_alloc_pages
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[03-09 15:56]** [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[03-09 15:56]** [PATCH v3 3/3] coco: guest: arm64: Add Realm Host Interface and hostconf RHI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[03-09 10:50]** Re: [PATCH v3 3/3] coco: guest: arm64: Add Realm Host Interface and
 hostconf RHI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[03-09 14:54]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: kernel test robot <lkp@intel.com>
7. **[03-09 15:55]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: kernel test robot <lkp@intel.com>
8. **[03-09 23:44]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: kernel test robot <lkp@intel.com>
9. **[03-09 23:55]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: kernel test robot <lkp@intel.com>

---

### Thread 13: [PATCH 1/3] KVM: arm64: fix include path for ring buffer implementation

**📧 邮件数**: 6 | **👥 参与者**: 4 | **📅 开始时间**: Thu, 12 Mar 2026 13:35:42 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的两个补丁，主要集中在修复环形缓冲区的包含路径和添加 ftrace 依赖。

**原始补丁内容**：
第一个补丁（PATCH 1/3）旨在修复 `simple_ring_buffer.c` 文件的包含路径问题。由于该文件位于源树中而非构建时生成，导致在使用分离对象树时出现找不到文件的错误。补丁通过修改 Makefile 中的包含路径来解决此问题。

**之前讨论要点**：
在历史讨论中并没有相关的背景信息，但补丁的提出是为了修复之前的代码更改（提交 ID：680a04c333fa），该更改添加了 nVHE/pKVM hyp 的跟踪能力。

**本周新讨论及进展**：
本周的讨论中，Arnd Bergmann 提出了两个补丁，分别为修复包含路径和添加 ftrace 依赖。Vincent Donnefort 对第一个补丁表示已被 Marc Zyngier 接受并应用，第二个补丁也获得了审核通过。Marc Zyngier 确认这两个补丁已被合并到下一个版本中。Nathan Chancellor 提到补丁中删除了 `kernel/trace/Makefile` 的 SPDX 标识行，需注意这一点。

总体来看，本周的讨论进展顺利，补丁得到了积极的反馈并已被应用。

#### 📝 邮件列表

1. **[03-12 13:35]** [PATCH 1/3] KVM: arm64: fix include path for ring buffer implementation
   - 发件人: Arnd Bergmann <arnd@kernel.org>
2. **[03-12 13:35]** [PATCH 3/3] KVM: arm64: tracing: add ftrace dependency
   - 发件人: Arnd Bergmann <arnd@kernel.org>
3. **[03-12 13:35]** Re: [PATCH 1/3] KVM: arm64: fix include path for ring buffer
 implementation
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[03-12 13:52]** Re: [PATCH 3/3] KVM: arm64: tracing: add ftrace dependency
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[03-12 15:45]** Re: (subset) [PATCH 1/3] KVM: arm64: fix include path for ring buffer implementation
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-12 15:08]** Re: (subset) [PATCH 1/3] KVM: arm64: fix include path for ring
 buffer implementation
   - 发件人: Nathan Chancellor <nathan@kernel.org>

---

### Thread 14: [PATCH v12 06/46] arm64: RMI: Define the user ABI

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 02 Mar 2026 14:25:37 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构下的 RMI（Resource Management Interface）用户 ABI（应用二进制接口）的定义，属于 Linux 内核的补丁系列（PATCH v12 06/46）。

在历史讨论中，Marc Zyngier 和 Steven Price 讨论了如何处理 PSCI（Power State Coordination Interface）在虚拟机监控器（VMM）中的应用，提出将 PSCI 的处理方式强制化可能会简化实现。Steven 还提到，当前的补丁中包含了对 PSCI 的更改，并讨论了将功能推向用户空间的必要性。

在本周的新讨论中，Marc Zyngier 提出了使用 `splice(2)` 函数来实现异步操作的建议，并认为这可能是处理 CCA（Confidential Computing Architecture）的一种更优雅的方式。然而，Suzuki K Poulose 指出，使用 `splice` 时无法有效传达数据的测量标志（measured vs unmeasured），这在 CCA 和其他技术中是一个重要问题。Marc 进一步讨论了数据测量的属性应与内存区域相关，而不是仅仅依赖于复制方式。最终，Steven Price 对 `splice(2)` 的适用性表示怀疑，认为其对管道的要求可能不适用于当前的设计需求。

总体来看，本周讨论集中在如何优化 RMI 用户 ABI 的实现细节，特别是在数据处理和内存管理方面的挑战。

#### 📝 邮件列表

1. **[03-02 14:25]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-02 15:23]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
3. **[03-11 19:10]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-12 09:28]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[03-12 09:39]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-12 10:45]** Re: [PATCH v12 06/46] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 15: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on CPU hotplug

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 10 Mar 2026 08:54:33 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在解决 CPU 热插拔时对 ICH_VTR_EL2.TDS 的重新探测问题。原始补丁由 Marc Zyngier 提出，指出在 pKVM（保护模式下的 KVM）环境中，热插拔 CPU 时会因无法访问 EL2 stub helper 而导致 CPU 无法正常启动。补丁通过检测保护模式的早期状态，避免了不必要的重新探测，从而确保系统的稳定性。

在之前的讨论中，参与者们关注补丁的实现细节，Suzuki K Poulose 提出是否需要添加注释以解释为何在热插拔情况下返回能力的系统状态。Vincent Donnefort 则表示已对补丁进行了测试，确认其有效性。

本周的讨论中，Marc Zyngier 和 Suzuki K Poulose 对补丁进行了进一步的完善，增加了注释以解释 pKVM 如何影响 CPU 状态的稳定性。最终，Marc Zyngier 确认补丁已被应用到修复列表中，标志着这一问题的解决。

#### 📝 邮件列表

1. **[03-10 08:54]** [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on CPU hotplug
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-10 09:17]** Re: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on
 CPU hotplug
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[03-10 09:27]** Re: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on
 CPU hotplug
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[03-10 09:43]** Re: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on CPU hotplug
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-10 10:13]** Re: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on
 CPU hotplug
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[03-10 10:17]** Re: [PATCH] KVM: arm64: pkvm: Don't reprobe for ICH_VTR_EL2.TDS on CPU hotplug
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 16: [PATCH] KVM: arm64: Discard PC update state on vcpu reset

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 12 Mar 2026 14:08:50 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的一个补丁，旨在解决在虚拟 CPU（vcpu）重置时未正确处理程序计数器（PC）更新状态的问题。

**原始补丁内容**：
补丁的核心是修复在 vcpu 重置过程中，未能清除与 PC 更新相关的状态，导致在执行恢复时可能跳过重要指令，从而影响 CPU 的启动或恢复过程。补丁通过在重置时清除所有影响 PC 的状态，确保系统能够正常启动。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 提出了该问题的背景，指出了当前实现的缺陷，并强调了 PC 更新与异常处理之间的耦合问题。该问题可能导致 CPU 热插拔失败，并影响系统的稳定性。

**本周的新讨论与进展**：
本周的讨论中，参与者对补丁进行了积极的反馈，Joey Gouly 和 Suzuki K Poulose 都表示赞同并进行了审核。Marc Zyngier 在最后一封邮件中确认补丁已被应用到修复分支，并感谢大家的贡献。这表明该补丁得到了认可，并将有助于提升 KVM 的稳定性和可靠性。

#### 📝 邮件列表

1. **[03-12 14:08]** [PATCH] KVM: arm64: Discard PC update state on vcpu reset
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-13 14:30]** Re: [PATCH] KVM: arm64: Discard PC update state on vcpu reset
   - 发件人: Joey Gouly <joey.gouly@arm.com>
3. **[03-13 16:16]** Re: [PATCH] KVM: arm64: Discard PC update state on vcpu reset
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[03-15 15:08]** Re: [PATCH] KVM: arm64: Discard PC update state on vcpu reset
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-15 15:11]** Re: [PATCH] KVM: arm64: Discard PC update state on vcpu reset
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 17: [PATCH v13 00/32] Tracefs support for pKVM

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Fri,  6 Mar 2026 14:35:04 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 pKVM 的 Tracefs 支持的补丁（PATCH v13 00/32）。该补丁旨在为保护模式下的虚拟化提供调试和分析工具，Tracefs 被认为是理想的选择，因为它易于使用并且与多种工具兼容。此外，补丁还引入了环形缓冲区的远程功能，使得外部实体（如固件或虚拟机监控器）能够以与 Tracefs 环形缓冲区相同的格式写入事件。

在历史讨论中，Vincent Donnefort 提出了补丁的初步版本，并详细说明了环形缓冲区的设置和所需的回调函数。Markus Elfring 也参与了讨论，提出了关于锁保护的建议。

在本周的新讨论中，Steven Rostedt 指出该补丁在 7.0-rc3 版本上无法干净应用，要求 Vincent 进行重新基于（rebase）。Vincent 随后回应，表示他已根据 Markus 的建议进行了修改，并准备了新版本的补丁。这表明讨论仍在继续，开发者们积极响应反馈并推进补丁的完善。

#### 📝 邮件列表

1. **[03-06 14:35]** [PATCH v13 00/32] Tracefs support for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-06 14:35]** [PATCH v13 03/32] ring-buffer: Introduce ring-buffer remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-06 17:37]** Re: [PATCH v13 03/32] ring-buffer: Introduce ring-buffer remotes
   - 发件人: Markus Elfring <Markus.Elfring@web.de>
4. **[03-08 21:45]** Re: [PATCH v13 00/32] Tracefs support for pKVM
   - 发件人: Steven Rostedt <rostedt@goodmis.org>
5. **[03-11 15:23]** Re: [PATCH v13 03/32] ring-buffer: Introduce ring-buffer remotes
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 18: [PATCH] tracing: Generate undef symbols allowlist for simple_ring_buffer

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 12 Mar 2026 18:20:10 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），旨在为 `simple_ring_buffer` 生成未定义符号的允许列表。该补丁由 Vincent Donnefort 提出，主要目的是通过自动检测符号来增强允许列表的鲁棒性，替代原先的硬编码列表。这一机制生成一个 C 函数，用于触发常见的编译器插入符号。

在之前的讨论中，参与者们关注了补丁的实现细节，特别是如何更有效地生成 C 文件。Steven Rostedt 提出了将生成 C 文件的命令合并为一个单一命令的建议，以提高效率。Nathan Chancellor 则指出，应该使用 `filechk` 来避免每次构建都重新生成 `undefsyms_base.c` 文件，从而减少不必要的重建。

在本周的新讨论中，Vincent Donnefort 对参与者的反馈表示感谢，并计划根据建议进行补丁的更新（v2版本）。Nathan 还提到了一些未定义符号的问题，并建议在补丁中添加更多的头文件引用，以确保符号的正确处理。

总结来说，邮件讨论围绕如何改进 `simple_ring_buffer` 的未定义符号处理展开，参与者们提出了多项建设性意见，促进了补丁的进一步完善。

#### 📝 邮件列表

1. **[03-12 18:20]** [PATCH] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-12 14:43]** Re: [PATCH] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Steven Rostedt <rostedt@goodmis.org>
3. **[03-12 16:51]** Re: [PATCH] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Nathan Chancellor <nathan@kernel.org>
4. **[03-13 10:23]** Re: [PATCH] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 19: [PATCH] KVM: arm64: Fix ICV_DIR_EL1 trapping detection for pKVM

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  9 Mar 2026 16:04:50 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 pKVM（Protected KVM）环境中 ICV_DIR_EL1 触发检测的问题。原始的补丁（patch）由 Vincent Donnefort 提出，主要是因为在非 VHE（Virtualization Host Extensions）模式下，can_trap_icv_dir_el1() 函数依赖于 hyp-stub HVC 来读取 ICH_VTR_EL2 寄存器，这与启用 pKVM 的设备不兼容，导致在热插拔 CPU 时出现能力冲突，进而阻止 CPU 上线。

在之前的讨论中，Marc Zyngier 指出原补丁的复杂性，并建议直接返回当前属性值，因为在 pKVM 环境下，CPU 的状态不会在热插拔过程中发生变化。他提供了一种简化的解决方案，建议在系统能力最终确定且启用 pKVM 时，直接检查 CPU 是否具备相关能力。

本周的讨论中，Vincent Donnefort 对 Marc 的建议进行了测试，确认其有效性，并表示可以基于此方案生成新的补丁。最终，Vincent 提到已将修改后的代码发送，期待测试反馈。整体来看，讨论围绕如何简化 ICV_DIR_EL1 的触发检测逻辑展开，并取得了积极进展。

#### 📝 邮件列表

1. **[03-09 16:04]** [PATCH] KVM: arm64: Fix ICV_DIR_EL1 trapping detection for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-09 17:33]** Re: [PATCH] KVM: arm64: Fix ICV_DIR_EL1 trapping detection for pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-09 18:07]** Re: [PATCH] KVM: arm64: Fix ICV_DIR_EL1 trapping detection for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[03-10 08:56]** Re: [PATCH] KVM: arm64: Fix ICV_DIR_EL1 trapping detection for pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 20: [PATCH] tracing: Update undefined symbols allow list for simple_ring_buffer

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 12 Mar 2026 11:35:35 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于更新 `simple_ring_buffer` 的未定义符号允许列表的补丁（patch）。该补丁由 Vincent Donnefort 提出，目的是解决在编译 `simple_ring_buffer.c` 时，某些编译器生成的符号未被包含在允许列表中，从而导致编译失败。

在历史讨论中，补丁的背景是由于之前的提交（a717943d8ecc）引入了对未定义符号的检查，但未能涵盖所有必要的符号，导致编译过程中出现问题。Vincent 提到需要更新允许列表，以包含缺失的符号。

在本周的新讨论中，Vincent 提交了补丁，并在邮件中提到需要确认该补丁是通过 ARM 树还是其他途径提交。Steven Rostedt 表示对补丁的支持，并确认可以通过 ARM 树提交。Marc Zyngier 则表示已经将补丁应用到下一个版本中，确认了补丁的成功整合。

总结来说，本周的讨论主要集中在补丁的确认和提交流程上，补丁已被接受并应用，解决了之前未定义符号的问题。

#### 📝 邮件列表

1. **[03-12 11:35]** [PATCH] tracing: Update undefined symbols allow list for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-12 09:33]** Re: [PATCH] tracing: Update undefined symbols allow list for
 simple_ring_buffer
   - 发件人: Steven Rostedt <rostedt@goodmis.org>
3. **[03-12 15:44]** Re: [PATCH] tracing: Update undefined symbols allow list for simple_ring_buffer
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 21: [PATCH v2] tracing: Generate undef symbols allowlist for simple_ring_buffer

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 10:58:29 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 Linux 内核的补丁（PATCH v2），旨在为 `simple_ring_buffer` 生成未定义符号的允许列表。该补丁的主要目的是通过自动检测符号来增强允许列表的鲁棒性，而不是使用硬编码的符号列表。这一机制生成一个 C 函数，用于触发常见的编译器插入符号。

在之前的讨论中，补丁的初始版本提出了使用 `filechk` 来替代过时的 `extra-y`，并将 `simple_ring_buffer` 添加到允许列表中。此外，还增加了 `memcpy()` 以生成更多符号，并引入了 `__sancov`。

在本周的新讨论中，参与者 Vincent Donnefort 提到补丁在 RISC-V 架构上的表现，指出在某些情况下，`undefsyms_base.o` 由于未链接到 `vmlinux`，未自动启用 KASAN，从而导致出现意外的符号。为了解决这个问题，补丁中增加了确保 KASAN 被启用的逻辑。Nathan Chancellor 对此表示认可，并确认这一修改对其测试是有效的。

总体而言，本周的讨论集中在补丁的细节调整和特定架构的兼容性上，确保了补丁在不同环境下的有效性。

#### 📝 邮件列表

1. **[03-13 10:58]** [PATCH v2] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-13 09:37]** Re: [PATCH v2] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Nathan Chancellor <nathan@kernel.org>

---

### Thread 22: [PATCH] KVM: arm64: avoid unused-variable warning

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 10:49:16 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在避免未使用变量的警告。

1. **原始 patch/问题的内容**：补丁由 Arnd Bergmann 提出，主要解决在 `arch/arm64/kvm/hyp_trace.c` 文件中，`cpu` 变量在某些条件下未被使用而导致的编译警告。补丁通过将 `#ifdef` 条件替换为 `IS_ENABLED()` 检查，来确保在编译时仅在相关配置启用时才使用该变量，从而避免警告。

2. **之前的讨论要点**：本邮件线程没有提供历史讨论的内容，所有讨论均集中在本周的新进展上。

3. **本周的新讨论、进展或结论**：在本周的讨论中，Arnd Bergmann 提出了补丁，Vincent Donnefort 对该补丁进行了审核并表示支持，标记为“Reviewed-by”。这表明补丁得到了认可，可能会在后续版本中合并。

总的来说，此次讨论集中在修复未使用变量警告的补丁上，参与者之间的互动表明该补丁得到了积极的反馈。

#### 📝 邮件列表

1. **[03-13 10:49]** [PATCH] KVM: arm64: avoid unused-variable warning
   - 发件人: Arnd Bergmann <arnd@kernel.org>
2. **[03-13 11:07]** Re: [PATCH] KVM: arm64: avoid unused-variable warning
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 23: [PATCH] KVM: arm64: Fix out-of-tree build for nVHE/pKVM tracing

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 11 Mar 2026 16:49:56 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复 nVHE/pKVM 跟踪的外部构建问题。补丁的核心内容是修正 `simple_ring_buffer.c` 的包含路径，使其指向源代码树而非对象树。

在历史讨论中，虽然没有具体的邮件记录，但可以推测出该问题的背景是与 KVM 的构建过程相关，特别是在处理外部构建时出现的路径问题。

在本周的新讨论中，Vincent Donnefort 提出了该补丁，明确指出了需要修改的 Makefile 中的路径。Marc Zyngier 随后回复确认已将该补丁应用到下一个版本中，并表示感谢。这表明该补丁得到了认可并将被纳入后续的开发中。整体来看，此次讨论顺利推进了 KVM 的构建过程优化。

#### 📝 邮件列表

1. **[03-11 16:49]** [PATCH] KVM: arm64: Fix out-of-tree build for nVHE/pKVM tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-11 17:24]** Re: [PATCH] KVM: arm64: Fix out-of-tree build for nVHE/pKVM tracing
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 24: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 13 Mar 2026 15:31:30 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构上添加对受保护来宾内存的支持，特别是与 pKVM（Protected Kernel Virtual Machine）相关的补丁。

在历史讨论中，虽然没有具体的补丁内容被提及，但可以推测该补丁旨在增强 KVM 的安全性，使其能够支持受保护的虚拟机内存，提升虚拟化环境的安全性。

本周的新讨论中，参与者 Mostafa Saleh 分享了他在 Lenovo ideacenter Mini X Gen 10 Snapdragon 设备上测试该补丁的结果。他提到在使用 nvhe（Non-virtual Hypervisor Execution）时能够成功启动受保护和非受保护的虚拟机，尽管在 hvhe（Hypervisor Execution）上遇到了一些问题。Mostafa 还提供了他使用的配置和运行命令，并确认了补丁的有效性，标记为“Tested-by”。

综上所述，本周的讨论表明该补丁在特定硬件上的测试取得了积极进展，为后续的开发和优化提供了基础。

#### 📝 邮件列表

1. **[03-13 15:31]** Re: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 25: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 12 Mar 2026 21:44:07 +0000

#### 🤖 AI 总结

本邮件主题为“[PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned”，涉及对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的性能监控单元版本（PMUVer）读取方式的修改。该补丁的目的是将 PMUVer 作为无符号数进行读取，以提高数据处理的准确性和一致性。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁的提出是基于对现有 PMUVer 读取方式的不足之处的认识，可能存在数据类型不匹配或处理不当的问题。

在本周的新讨论中，参与者 Colton Lewis 对该补丁进行了测试，并表示感谢 James Clark 的工作，确认了补丁的有效性，并给予了“Reviewed-by”的标记。这表明该补丁得到了积极的反馈，可能会在后续版本中被采纳。

总结而言，本周的讨论主要集中在对补丁的认可与测试结果上，显示出社区对改进 KVM 在 arm64 架构下性能监控的积极态度。

#### 📝 邮件列表

1. **[03-12 21:44]** Re: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 26: [PATCH v2 14/35] KVM: arm64: Handle aborts from protected VMs

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 11 Mar 2026 10:24:30 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（内核虚拟机）在 arm64 架构下处理来自受保护虚拟机的中止（aborts）情况的补丁（patch）。该补丁的目的是增强 KVM 在处理受保护虚拟机时的稳定性和安全性。

在历史讨论中，并没有提供具体的背景信息或之前的讨论内容，可能是因为该邮件线程中只有本周的新讨论。

本周的讨论中，参与者 Fuad Tabba 对该补丁进行了审查，并表示已通过（Reviewed-by），这表明补丁在技术上得到了认可，准备进入下一步的处理流程。这是该补丁在本周的主要进展，显示出社区对该补丁的支持和认可。

#### 📝 邮件列表

1. **[03-11 10:24]** Re: [PATCH v2 14/35] KVM: arm64: Handle aborts from protected VMs
   - 发件人: Fuad Tabba <tabba@google.com>

---

## 📌 RFC

共 4 个 thread

---

### Thread 1: [RFC PATCH 00/14] KVM: ITS hardening for pKVM

**📧 邮件数**: 25 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 10 Mar 2026 12:49:19 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于KVM（Kernel-based Virtual Machine）中ITS（Interrupt Translation Service）硬化的RFC补丁系列，主要针对pKVM（Protected KVM）环境的安全性进行增强。

**原始补丁内容**：
该补丁系列旨在通过对设备访问进行陷阱和仿真，增强pKVM环境下GIC/ITS控制器的安全性，以防止攻击者通过该设备篡改虚拟机监控器（hypervisor）保护的内存。补丁包括对ITS命令队列的共享、保护和仿真机制的实现。

**之前讨论要点**：
在历史讨论中，参与者们对补丁的设计和实现进行了深入探讨，包括如何处理MMIO（内存映射输入输出）区域的捐赠、如何追踪未映射的MMIO区域，以及如何在虚拟化环境中有效地管理ITS的状态。讨论中还提到了一些术语的使用，如“shadow”状态的替换为“hypervisor state”。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现细节上，包括对ITS命令的解析、对虚拟待处理表（VPT）和设备表的管理、以及对ITS寄存器的访问限制。参与者们提出了对补丁的优化建议，如改进内存分配的方式、确保缓存一致性，以及在处理命令时的错误检查。此外，Mostafa和Fuad报告了在测试过程中遇到的内核挂起问题，表明补丁在某些硬件上可能存在兼容性问题。

总之，本邮件线程展示了KVM ITS硬化补丁的设计、实现及其在pKVM环境下的挑战，参与者们积极交流以改进补丁的质量和稳定性。

#### 📝 邮件列表

1. **[03-10 12:49]** [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-10 12:49]** [PATCH 01/14] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[03-10 12:49]** [PATCH 02/14] KVM: arm64: Track host-unmapped MMIO regions in a
 static array
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[03-10 12:49]** [PATCH 03/14] KVM: arm64: Support host MMIO trap handlers for
 unmapped devices
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[03-10 12:49]** [PATCH 04/14] KVM: arm64: Mediate host access to GIC/ITS MMIO via unmapping
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[03-10 12:49]** [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for KVM
 host deprivilege
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[03-10 12:49]** [PATCH 06/14] KVM: arm64: Add infrastructure for ITS emulation setup
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[03-10 12:49]** [PATCH 07/14] KVM: arm64: Restrict host access to the ITS tables
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[03-10 12:49]** [PATCH 08/14] KVM: arm64: Trap & emulate the ITS MAPD command
   - 发件人: Sebastian Ene <sebastianene@google.com>
10. **[03-10 12:49]** [PATCH 09/14] KVM: arm64: Trap & emulate the ITS VMAPP command
   - 发件人: Sebastian Ene <sebastianene@google.com>
11. **[03-10 12:49]** [PATCH 10/14] KVM: arm64: Trap & emulate the ITS MAPC command
   - 发件人: Sebastian Ene <sebastianene@google.com>
12. **[03-10 12:49]** [PATCH 11/14] KVM: arm64: Restrict host updates to GITS_CTLR
   - 发件人: Sebastian Ene <sebastianene@google.com>
13. **[03-10 12:49]** [PATCH 12/14] KVM: arm64: Restrict host updates to GITS_CBASER
   - 发件人: Sebastian Ene <sebastianene@google.com>
14. **[03-10 12:49]** [PATCH 13/14] KVM: arm64: Restrict host updates to GITS_BASER
   - 发件人: Sebastian Ene <sebastianene@google.com>
15. **[03-10 12:49]** [PATCH 14/14] KVM: arm64: Implement HVC interface for ITS emulation setup
   - 发件人: Sebastian Ene <sebastianene@google.com>
16. **[03-12 17:56]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Fuad Tabba <tabba@google.com>
17. **[03-12 17:57]** Re: [PATCH 01/14] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Fuad Tabba <tabba@google.com>
18. **[03-12 19:05]** Re: [PATCH 02/14] KVM: arm64: Track host-unmapped MMIO regions in a
 static array
   - 发件人: Fuad Tabba <tabba@google.com>
19. **[03-13 09:31]** Re: [PATCH 03/14] KVM: arm64: Support host MMIO trap handlers for
 unmapped devices
   - 发件人: Fuad Tabba <tabba@google.com>
20. **[03-13 09:58]** Re: [PATCH 04/14] KVM: arm64: Mediate host access to GIC/ITS MMIO via unmapping
   - 发件人: Fuad Tabba <tabba@google.com>
21. **[03-13 10:40]** Re: [PATCH 01/14] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[03-13 11:26]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Fuad Tabba <tabba@google.com>
23. **[03-13 13:10]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Fuad Tabba <tabba@google.com>
24. **[03-13 15:18]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>
25. **[03-15 13:24]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 2: [RFC PATCH v3 00/12] coco/TSM: Implement host-side support for Arm CCA TDISP setup

**📧 邮件数**: 13 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 12 Mar 2026 13:37:31 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于在 Arm CCA 中实现主机端支持的补丁系列，主题为「[RFC PATCH v3 00/12] coco/TSM: 实现 Arm CCA TDISP 设置的主机端支持」。该补丁系列主要涉及 Realm vdev 对象的创建与管理、设备认证请求的服务以及 KVM/RMM 流程的实现。

历史讨论中，Aneesh Kumar K.V 提到该补丁系列基于 RMM ALP17 和 RHI v1.0 BET1 规范，主要添加了主机端 vdev 通信与生命周期管理、RHI DA 对象的处理、KVM 对 vdev 请求的处理等功能。补丁还解决了之前的审查反馈，并进行了代码重构。

本周的新讨论中，补丁逐步完善，涉及多个功能的实现，包括：
1. 添加了对虚拟设备通信的支持。
2. 实现了 RMM vdev 对象的创建与管理。
3. 增加了处理 RHI DA 对象读取的功能。
4. 引入了用于获取和更新接口报告及设备测量的辅助函数。
5. 实现了 vdev 状态转换到 TDISP RUN 状态的功能。
6. 最后，补丁还启用了在创建 Realm 时的设备认证（DA）功能。

整体上，该补丁系列旨在增强 Arm CCA 的主机端支持，推动设备虚拟化和安全性的发展。

#### 📝 邮件列表

1. **[03-12 13:37]** [RFC PATCH v3 00/12] coco/TSM: Implement host-side support for Arm CCA TDISP setup
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[03-12 13:37]** [RFC PATCH v3 01/12] coco: host: arm64: Add support for virtual device communication
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[03-12 13:37]** [RFC PATCH v3 02/12] coco: host: arm64: Add support for RMM vdev objects
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[03-12 13:37]** [RFC PATCH v3 03/12] coco: host: arm64: Add helpers to unlock and destroy RMM vdev
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[03-12 13:37]** [RFC PATCH v3 04/12] coco: host: arm64: Add support for da object read RHI handling
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[03-12 13:37]** [RFC PATCH v3 05/12] coco: host: arm64: Add helper for cached object fetches
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[03-12 13:37]** [RFC PATCH v3 06/12] coco: host: arm64: Fetch interface report via RMI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[03-12 13:37]** [RFC PATCH v3 07/12] coco: host: arm64: Fetch device measurements via RMI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[03-12 13:37]** [RFC PATCH v3 08/12] coco: host: KVM: arm64: Handle vdev request exits and completion
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[03-12 13:37]** [RFC PATCH v3 09/12] coco: host: KVM: arm64: Handle vdev map/validation exits
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[03-12 13:37]** [RFC PATCH v3 10/12] KVM: arm64: Unmap device mappings when a private granule is destroyed
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[03-12 13:37]** [RFC PATCH v3 11/12] coco: host: arm64: Transition vdevs to TDISP RUN state
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
13. **[03-12 13:37]** [RFC PATCH v3 12/12] KVM: arm64: CCA: enable DA in realm create parameters
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

### Thread 3: [RFC PATCH v3 00/11] coco/TSM: Arm CCA guest TDISP lock/accept flow with verification and DMA enable

**📧 邮件数**: 12 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 12 Mar 2026 13:34:31 +0530

#### 🤖 AI 总结

本邮件讨论的主题是关于 Arm CCA 客户端的 TDISP 锁定/接受流程的实现，涉及到多个补丁的更新和讨论。

1. **原始补丁内容**：该补丁系列实现了 TDISP 设置所需的 TSM ->lock()、->unlock() 和 ->accept() 回调，确保设备在 TDI LOCK 和 RUN 状态之间的转换，并在成功验证后启用 DMA。

2. **之前讨论要点**：之前的讨论主要集中在如何实现设备状态转换、验证主机提供的证据与 RMM 提供的摘要之间的一致性，以及如何在锁定和解锁过程中处理接口报告的缓存。

3. **本周的新讨论和进展**：
   - 本周的讨论中，Aneesh Kumar K.V 提出了多个补丁，增加了对设备锁定、解锁和接受的支持，确保在设备接受后启用 DMA。
   - 具体补丁包括实现了接口报告和测量的刷新、设备证据的验证、以及 DMA 行为的更新，确保接受的设备只能访问私有内存。
   - 还引入了新的 SMC 调用以支持 DMA 启用，并在设备接受路径中进行调用，确保在通过验证后才能启用 DMA。
   - 讨论中还提到未来可能需要扩展 DMA 接口以支持共享内存的分配。

整体来看，本周的讨论进一步完善了 Arm CCA 客户端的安全性和功能性，确保了设备在虚拟化环境中的安全操作。

#### 📝 邮件列表

1. **[03-12 13:34]** [RFC PATCH v3 00/11] coco/TSM: Arm CCA guest TDISP lock/accept flow with verification and DMA enable
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[03-12 13:34]** [RFC PATCH v3 01/11] coco: guest: arm64: Guest TSM callback and realm device lock support
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[03-12 13:34]** [RFC PATCH v3 02/11] coco: guest: arm64: Fix a typo in the ARM_CCA_GUEST Kconfig help string ("and" -> "an").
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[03-12 13:34]** [RFC PATCH v3 03/11] coco: guest: arm64: Add Realm Host Interface and guest DA helper
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[03-12 13:34]** [RFC PATCH v3 04/11] coco: guest: arm64: Support guest-initiated TDI lock/unlock transitions
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[03-12 13:34]** [RFC PATCH v3 05/11] coco: guest: arm64: Refresh interface-report cache during device lock
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[03-12 13:34]** [RFC PATCH v3 06/11] coco: guest: arm64: Add measurement refresh via RHI_DA_VDEV_GET_MEASUREMENTS
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[03-12 13:34]** [RFC PATCH v3 07/11] coco: guest: arm64: Add guest APIs to read host-cached DA objects
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[03-12 13:34]** [RFC PATCH v3 08/11] coco: guest: arm64: Verify DA evidence with RSI_VDEV_GET_INFO digests
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[03-12 13:34]** [RFC PATCH v3 09/11] coco: guest: arm64: Hook TSM accept to Realm TDISP RUN transition
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[03-12 13:34]** [RFC PATCH v3 10/11] coco: arm64: dma: Update force_dma_unencrypted for accepted devices
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[03-12 13:34]** [RFC PATCH v3 11/11] coco: guest: arm64: Enable vdev DMA after attestation
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

### Thread 4: [RFC PATCH v3 00/10] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks

**📧 邮件数**: 11 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 12 Mar 2026 13:31:19 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于 ARM CCA IDE 设置的补丁系列，主要通过连接/断开回调实现主机端的支持。

1. **原始补丁内容**：
   该补丁系列实现了 TSM 的 `connect()` 和 `disconnect()` 回调，以支持根据 RMM ALP17 规范进行 ARM CCA IDE 设置。补丁包括特性检测、TSM 回调连接、IDE 流分配、RMM 设备描述符的创建与注册等功能。

2. **之前讨论要点**：
   之前的讨论主要集中在补丁的版本更新和对代码的审查反馈上。补丁经过多次迭代，逐步完善了对 RMM 设备通信的支持，并解决了在设备连接过程中可能出现的问题。

3. **本周的新讨论与进展**：
   本周的讨论中，补丁的多个子项被逐一提交，包括：
   - 添加了 RMM 设备通信的辅助函数。
   - 实现了 RMM pdev 的创建和销毁功能。
   - 增强了对公钥的处理，支持从证书链中提取公钥并注册到 RMM。
   - 讨论了 X.509 证书解析的改进，以支持新的安全协议。

整体来看，本周的讨论和补丁提交显示出对 ARM CCA IDE 设置的持续关注，旨在通过增强的设备通信和安全性支持，推动 ARM 平台的虚拟化进展。

#### 📝 邮件列表

1. **[03-12 13:31]** [RFC PATCH v3 00/10] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[03-12 13:31]** [RFC PATCH v3 01/10] KVM: arm64: RMI: Add and export kvm_has_da_feature helper
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[03-12 13:31]** [RFC PATCH v3 02/10] coco: host: arm64: Add host TSM callback and IDE stream allocation support
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[03-12 13:31]** [RFC PATCH v3 03/10] coco: host: arm64: Build and register RMM pdev descriptors
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[03-12 13:31]** [RFC PATCH v3 04/10] coco: host: arm64: Add RMM device communication helpers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[03-12 13:31]** [RFC PATCH v3 05/10] coco: host: arm64: Add helper to stop and tear down an RMM pdev
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[03-12 13:31]** [RFC PATCH v3 06/10] coco: host: arm64: Instantiate RMM pdev during device connect
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[03-12 13:31]** [RFC PATCH v3 07/10] X.509: Make certificate parser public
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[03-12 13:31]** [RFC PATCH v3 08/10] X.509: Parse Subject Alternative Name in certificates
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[03-12 13:31]** [RFC PATCH v3 09/10] X.509: Move certificate length retrieval into new helper
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[03-12 13:31]** [RFC PATCH v3 10/10] coco: host: arm64: Register device public key with RMM
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

## 📌 Question

共 1 个 thread

---

### Thread 1: Question about ARM KVM stage2 contiguous bit support for contiguous
 hugetlb

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 15:09:40 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM KVM stage2 对于连续 hugetlb 支持的 contiguous bit 的问题。

在本周的讨论中，Zhou Wang 提出了当前 KVM stage2 支持连续 hugetlb 的情况，但指出在页表项（PTE）中并未设置 contiguous bit，这导致硬件无法为连续的大页创建一个 TLB。为了解决这个问题，他建议在用户内存中中止时，不强制为 CONT_PMD_SHIFT/CONT_PTE_SHIFT 进行 PTE 映射，而是一次性映射所有连续页面，并在此过程中添加 contiguous bit。此外，他还提到需要修改与权限故障相关的代码，并考虑连续 hugetlb 的拆分问题。

Marc Zyngier 对此进行了回应，他认为在 S2 中处理连续提示的用例并不强烈，尤其是在使用匿名内存的情况下。他指出，在内存压力不大的情况下，透明大页（THP）已经能够提供所需的性能提升，而在内存压力大的情况下，连续性可能无法实现。他还强调，如果要进行此项工作，务必提供可重复的基准测试和结果，以证明对大多数工作负载的确有改进。

综上所述，本周讨论主要围绕如何在 ARM KVM stage2 中实现对连续 hugetlb 的支持展开，提出了具体的实现建议和对其必要性的质疑。

#### 📝 邮件列表

1. **[03-13 15:09]** Question about ARM KVM stage2 contiguous bit support for contiguous
 hugetlb
   - 发件人: Zhou Wang <wangzhou1@hisilicon.com>
2. **[03-13 07:49]** Re: Question about ARM KVM stage2 contiguous bit support for contiguous hugetlb
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 GIT PULL

共 2 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.0, take #2

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  6 Mar 2026 11:22:31 +0000

#### 🤖 AI 总结

本邮件线程讨论了 KVM/arm64 在 7.0 版本中的修复补丁。历史讨论中，Marc Zyngier 提出了第二组修复，主要解决了 pKVM 的一个问题，该问题导致当内存块未对齐时，主机无法向前推进。此外，还有一些低严重性的修复，涉及页表代码，Fuad 承诺将开始整理这些问题。

在本周的新讨论中，Paolo Bonzini 确认已将 Marc 提出的修复补丁拉取，并表示将会在近期内发送另一个包含几个烦人的修复的补丁，建议将其一并处理。Marc 对此表示感谢，并表示会等待将所有补丁一起发送。最终，Paolo 确认新的补丁正在发送中。

总结来说，本周的讨论主要集中在补丁的拉取和即将提交的新修复上，显示出参与者之间的良好沟通和协作。

#### 📝 邮件列表

1. **[03-06 11:22]** [GIT PULL] KVM/arm64 fixes for 7.0, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-11 17:58]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #2
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
3. **[03-11 17:04]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-11 18:05]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #2
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
5. **[03-11 17:41]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [GIT PULL] KVM/arm64 fixes for 7.0, take #3

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 11 Mar 2026 17:39:02 +0000

#### 🤖 AI 总结

本邮件主题为「[GIT PULL] KVM/arm64 fixes for 7.0, take #3」，主要讨论了针对 KVM/arm64 的修复补丁。

在本周的新讨论中，Marc Zyngier 提出了针对 7.0 版本的第三组修复补丁，共包含两个修复。这两个修复与之前在 6.19 版本中进行的大规模 vgic 重写有关。第一个修复涉及中断去激活的问题，可能导致虚拟机锁死；第二个修复则与 pKVM 的 CPU 热插拔相关，解决了在线 CPU 无法启动的问题。

具体补丁包括：
1. KVM: arm64: vgic: 从 AP-list 尾部获取 EOIcount 去激活。
2. KVM: arm64: pkvm: 在 CPU 热插拔时不要重新探测 ICH_VTR_EL2.TDS。

Paolo Bonzini 对 Marc Zyngier 的补丁请求表示确认并表示感谢，表明这些修复将被合并。

总结来看，本周的讨论集中在解决 KVM/arm64 中的关键问题上，确保虚拟机的稳定性和性能。

#### 📝 邮件列表

1. **[03-11 17:39]** [GIT PULL] KVM/arm64 fixes for 7.0, take #3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-11 18:42]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #3
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH v1 0/5] basic EL1/EL0 guest support

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  6 Mar 2026 14:26:51 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 单元测试的基本 EL1/EL0 客户支持的补丁（PATCH v1 0/5）。历史讨论中，Joey Gouly 提出了这一补丁的背景，旨在为在 EL1 或 EL0 运行代码提供基础设施，主要用于编写不需要单独地址空间或多个上下文的简单测试。补丁的前 3 个部分为准备工作，第四个补丁添加了“guest”API，最后一个补丁则引入了一个使用该 API 的测试。

在之前的讨论中，Joey 详细描述了补丁的内容，包括添加线程信息助手、处理 SP 的宏以及上下文切换的相关功能。最后一个补丁还增加了一个超管陷阱测试，确保在 EL1 和 EL0 中的代码能够正确运行。

本周的新讨论中，Wei-Lin Chang 针对补丁中的函数命名提出了一些建议，认为某些函数名不够直观，建议使用更清晰的命名方式，例如将 `undef_handler()` 改为更具描述性的名称，并建议在顶层测试函数前添加 `test_` 前缀，以提高可读性。整体来看，本周讨论主要集中在代码可读性和命名规范上。

#### 📝 邮件列表

1. **[03-06 14:26]** [kvm-unit-tests PATCH v1 0/5] basic EL1/EL0 guest support
   - 发件人: Joey Gouly <joey.gouly@arm.com>
2. **[03-06 14:26]** [kvm-unit-tests PATCH v1 5/5] arm64: add hypervisor trapping test
   - 发件人: Joey Gouly <joey.gouly@arm.com>
3. **[03-10 16:08]** Re: [kvm-unit-tests PATCH v1 5/5] arm64: add hypervisor trapping test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

