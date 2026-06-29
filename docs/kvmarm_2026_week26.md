# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-06-29 00:55:34

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 312
- **总 Thread 数**: 37
- **大型 Thread** (>20封): 3 个

### 分类分布

- **PATCH**: 29 threads (279 邮件)
- **RFC**: 2 threads (11 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Discussion**: 3 threads (10 邮件)
- **Other**: 2 threads (11 邮件)

---

## 📌 PATCH

共 29 个 thread

---

### Thread 1: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT

**📧 邮件数**: 46 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 23 Jun 2026 11:41:39 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构上实现 FEAT_HAFDBS 和 FEAT_HAFT 的一系列补丁（PATCH 00/22）。以下是讨论的主要内容：

1. **原始补丁内容**：
   - 该补丁系列旨在为 KVM 添加对硬件脏状态和访问标志的支持，特别是在嵌套 MMU 中。虽然 KVM 本身并不使用这些特性，但内核在一级页表中确实需要这些功能。

2. **历史讨论要点**：
   - 之前的讨论集中在如何实现这些特性，特别是处理脏状态和访问标志的复杂性。参与者们探讨了如何在不影响性能的情况下实现这些功能，并对现有代码进行了重构和优化。

3. **本周的新讨论与进展**：
   - 本周的讨论中，Oliver Upton 提出了多个补丁，逐步实现了对 HAFDBS 和 HAFT 的支持，包括设置脏状态、处理访问标志等。补丁中还引入了多个结构体和辅助函数，以简化代码和提高可读性。
   - 参与者们对补丁进行了审查，指出了一些潜在的问题和改进建议，例如在某些情况下可能导致权限故障的逻辑错误。
   - 讨论中还提到，HAFDBS 和 HAFT 的实现与现有的 KVM 脏跟踪机制并不直接相关，强调了软件脏跟踪在嵌套 MMU 中的重要性。

总体而言，本周的讨论集中在实现细节和代码优化上，参与者们积极反馈并提出改进建议，以确保补丁的正确性和性能。

#### 📝 邮件列表

1. **[06-23 11:41]** [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-23 11:41]** [PATCH 01/22] KVM: arm64: nv: Introduce struct for stage-2 walk step
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-23 11:41]** [PATCH 02/22] KVM: arm64: nv: Consolidate computation of stage-2 permissions
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-23 11:41]** [PATCH 03/22] KVM: arm64: nv: Get rid of kvm_s2_trans*() accessors
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-23 11:41]** [PATCH 04/22] KVM: arm64: nv: Only shadow writable-dirty guest descs as writable
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-23 11:41]** [PATCH 05/22] KVM: arm64: nv: Pass an access descriptor for stage-2 walks
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[06-23 11:41]** [PATCH 06/22] KVM: arm64: nv: Use a helper for stage-2 descriptor updates
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[06-23 11:41]** [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[06-23 11:41]** [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[06-23 11:41]** [PATCH 09/22] KVM: arm64: Compute S1 permissions as part of s1_walk()
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[06-23 11:41]** [PATCH 10/22] KVM: arm64: Plumb through access descriptor for stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[06-23 11:41]** [PATCH 11/22] KVM: arm64: Use a struct for stage-1 walk context
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[06-23 11:41]** [PATCH 12/22] KVM: arm64: Create helper for stage-1 descriptor updates
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[06-23 11:41]** [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
15. **[06-23 11:41]** [PATCH 14/22] KVM: arm64: Grant write permission when DBM is set at S1
   - 发件人: Oliver Upton <oupton@kernel.org>
16. **[06-23 11:41]** [PATCH 15/22] KVM: arm64: Don't update descriptors for "non-arch" access
   - 发件人: Oliver Upton <oupton@kernel.org>
17. **[06-23 11:41]** [PATCH 16/22] KVM: arm64: nv: Expose FEAT_HAFDBS
   - 发件人: Oliver Upton <oupton@kernel.org>
18. **[06-23 11:41]** [PATCH 17/22] KVM: arm64: Set Access flag on table descriptors at stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
19. **[06-23 11:41]** [PATCH 18/22] KVM: arm64: nv: Set access flag on table descriptors at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
20. **[06-23 11:41]** [PATCH 19/22] KVM: arm64: nv: Expose FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
21. **[06-23 11:41]** [PATCH 20/22] KVM: arm64: selftests: Only test AF behavior for emulated AT insns
   - 发件人: Oliver Upton <oupton@kernel.org>
22. **[06-23 11:42]** [PATCH 21/22] KVM: arm64: selftests: Test AT emulation for FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
23. **[06-23 11:42]** [PATCH 22/22] HACK: KVM: arm64: nv: Set the dirty state for CMOs that fetch for write
   - 发件人: Oliver Upton <oupton@kernel.org>
24. **[06-23 18:54]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: sashiko-bot@kernel.org
25. **[06-23 18:55]** Re: [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: sashiko-bot@kernel.org
26. **[06-23 18:55]** Re: [PATCH 12/22] KVM: arm64: Create helper for stage-1 descriptor
 updates
   - 发件人: sashiko-bot@kernel.org
27. **[06-23 18:57]** Re: [PATCH 02/22] KVM: arm64: nv: Consolidate computation of
 stage-2 permissions
   - 发件人: sashiko-bot@kernel.org
28. **[06-23 18:57]** Re: [PATCH 14/22] KVM: arm64: Grant write permission when DBM is
 set at S1
   - 发件人: sashiko-bot@kernel.org
29. **[06-23 18:58]** Re: [PATCH 04/22] KVM: arm64: nv: Only shadow writable-dirty guest
 descs as writable
   - 发件人: sashiko-bot@kernel.org
30. **[06-23 19:01]** Re: [PATCH 16/22] KVM: arm64: nv: Expose FEAT_HAFDBS
   - 发件人: sashiko-bot@kernel.org
31. **[06-23 19:03]** Re: [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: sashiko-bot@kernel.org
32. **[06-23 19:05]** Re: [PATCH 18/22] KVM: arm64: nv: Set access flag on table
 descriptors at stage-2
   - 发件人: sashiko-bot@kernel.org
33. **[06-23 19:05]** Re: [PATCH 19/22] KVM: arm64: nv: Expose FEAT_HAFT
   - 发件人: sashiko-bot@kernel.org
34. **[06-23 19:05]** Re: [PATCH 21/22] KVM: arm64: selftests: Test AT emulation for
 FEAT_HAFT
   - 发件人: sashiko-bot@kernel.org
35. **[06-23 19:06]** Re: [PATCH 05/22] KVM: arm64: nv: Pass an access descriptor for
 stage-2 walks
   - 发件人: sashiko-bot@kernel.org
36. **[06-23 13:05]** Re: [PATCH 04/22] KVM: arm64: nv: Only shadow writable-dirty guest
 descs as writable
   - 发件人: Oliver Upton <oupton@kernel.org>
37. **[06-23 13:08]** Re: [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
38. **[06-23 13:14]** Re: [PATCH 18/22] KVM: arm64: nv: Set access flag on table
 descriptors at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
39. **[06-23 13:17]** Re: [PATCH 21/22] KVM: arm64: selftests: Test AT emulation for
 FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
40. **[06-23 20:56]** Re: [PATCH 17/22] KVM: arm64: Set Access flag on table descriptors
 at stage-1
   - 发件人: sashiko-bot@kernel.org
41. **[06-26 16:31]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
42. **[06-26 16:49]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
43. **[06-26 17:03]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[06-26 18:12]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[06-26 10:35]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
46. **[06-26 10:45]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 2: [PATCH v8 00/20] KVM: selftests: Add eventfd+VFIO IRQ test

**📧 邮件数**: 28 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 26 Jun 2026 14:35:13 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM 的自测试补丁系列，主题为「添加 eventfd+VFIO IRQ 测试」。该补丁系列的目标是验证通过 eventfd 和 VFIO 设备的中断传递。

**原始 patch/问题的内容**：
补丁系列的核心是添加一个自测试，确保 KVM 能够通过 eventfd 机制正确传递中断。该测试将使用 VFIO 设备来验证中断的真实传递。

**之前讨论要点**：
在之前的讨论中，开发者们对补丁进行了多次版本迭代，主要集中在代码的可读性、功能的完善以及测试的稳定性上。例如，补丁中增加了对随机数生成器的初始化，以确保每次测试的随机性。

**本周的新讨论、进展或结论**：
本周的讨论中，开发者们提交了多个补丁，主要包括：
1. 添加了新的测试选项，如 `-d` 用于指定 VFIO 设备，`-e` 用于设置空的 GSI 路由，`-m` 用于在触发中断前迁移 vCPU 等。
2. 引入了对 xAPIC 模式的支持，允许用户选择在 x2APIC 或 xAPIC 模式下运行测试。
3. 针对 IRQ 亲和性和中断路由的动态变化进行了验证，确保 KVM 在这些情况下的正确性。

此外，Sashiko AI 评审也指出了一些潜在问题，如读取 `/proc/interrupts` 时的缓冲区大小不足等。整体来看，讨论集中在增强测试的功能和稳定性上，确保 KVM 的中断处理能力得到充分验证。

#### 📝 邮件列表

1. **[06-26 14:35]** [PATCH v8 00/20] KVM: selftests: Add eventfd+VFIO IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[06-26 14:35]** [PATCH v8 01/20] KVM: selftests: Build and link selftests/vfio/lib
 into KVM selftests
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[06-26 14:35]** [PATCH v8 02/20] KVM: selftests: Add macros to read/write+sync
 to/from guest memory
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[06-26 14:35]** [PATCH v8 03/20] KVM: selftests: Rename guest_rng to kvm_rng
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[06-26 14:35]** [PATCH v8 04/20] KVM: selftests: Initialize the default/global pRNG
 during kvm_selftest_init()
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[06-26 14:35]** [PATCH v8 05/20] KVM: selftests: Seed libc's RNG before using it to
 generate a seed for KVM's pRNG
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[06-26 14:35]** [PATCH v8 06/20] KVM: selftests: Add helper to generate random u64 in
 range [min,max]
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[06-26 14:35]** [PATCH v8 07/20] KVM: selftests: Add an irqfd send+receive (and later
 IRQ bypass) test
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[06-26 14:35]** [PATCH v8 08/20] KVM: selftests: Add helper to get host IRQ from
 device MSI-X for IRQ bypass test
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[06-26 14:35]** [PATCH v8 09/20] KVM: selftests: Add VFIO device support to eventfd
 IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[06-26 14:35]** [PATCH v8 10/20] KVM: selftests: Add a helper to set proc IRQ
 affinity for IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[06-26 14:35]** [PATCH v8 11/20] KVM: selftests: Verify interrupts are received when
 IRQ affinity changes in IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[06-26 14:35]** [PATCH v8 12/20] KVM: selftests: Add option to set empty routing
 between IRQs in eventfd IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
14. **[06-26 14:35]** [PATCH v8 13/20] KVM: selftests: Make number of IRQs configurable in
 IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
15. **[06-26 14:35]** [PATCH v8 14/20] KVM: selftests: Verify non-postable IRQ remapping in
 IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
16. **[06-26 14:35]** [PATCH v8 15/20] KVM: selftests: Add kvm_gettid() wrapper and convert users
   - 发件人: Sean Christopherson <seanjc@google.com>
17. **[06-26 14:35]** [PATCH v8 16/20] KVM: selftests: Add kvm_sched_getaffinity() wrapper
 and convert users
   - 发件人: Sean Christopherson <seanjc@google.com>
18. **[06-26 14:35]** [PATCH v8 17/20] KVM: selftests: Add a utility to pin a task to a
 random CPU, given a CPU set
   - 发件人: Sean Christopherson <seanjc@google.com>
19. **[06-26 14:35]** [PATCH v8 18/20] KVM: selftests: Verify vCPU migration during IRQ
 delivery in IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
20. **[06-26 14:35]** [PATCH v8 19/20] KVM: selftests: Make number of vCPUs configurable in
 IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
21. **[06-26 14:35]** [PATCH v8 20/20] KVM: selftests: Add xAPIC support in eventfd IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
22. **[06-26 21:42]** Re: [PATCH v8 08/20] KVM: selftests: Add helper to get host IRQ
 from device MSI-X for IRQ bypass test
   - 发件人: sashiko-bot@kernel.org
23. **[06-26 21:43]** Re: [PATCH v8 05/20] KVM: selftests: Seed libc's RNG before using
 it to generate a seed for KVM's pRNG
   - 发件人: sashiko-bot@kernel.org
24. **[06-26 21:44]** Re: [PATCH v8 01/20] KVM: selftests: Build and link
 selftests/vfio/lib into KVM selftests
   - 发件人: sashiko-bot@kernel.org
25. **[06-26 21:44]** Re: [PATCH v8 06/20] KVM: selftests: Add helper to generate random
 u64 in range [min,max]
   - 发件人: sashiko-bot@kernel.org
26. **[06-26 21:46]** Re: [PATCH v8 11/20] KVM: selftests: Verify interrupts are received
 when IRQ affinity changes in IRQ test
   - 发件人: sashiko-bot@kernel.org
27. **[06-26 21:48]** Re: [PATCH v8 04/20] KVM: selftests: Initialize the default/global
 pRNG during kvm_selftest_init()
   - 发件人: sashiko-bot@kernel.org
28. **[06-26 14:59]** Re: [PATCH v8 04/20] KVM: selftests: Initialize the default/global
 pRNG during kvm_selftest_init()
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 3: [PATCH v2 1/2] KVM: arm64: skip pKVM cache flushes for non cacheable mappings

**📧 邮件数**: 24 | **👥 参与者**: 5 | **📅 开始时间**: Tue, 23 Jun 2026 16:37:55 +0000

#### 🤖 AI 总结

本邮件线程讨论了两个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主要集中在 pKVM（Protected KVM）的缓存管理和权限故障处理上。

1. **原始补丁内容**：
   - **补丁 1**：跳过对非缓存映射的 pKVM 缓存刷新，避免不必要的缓存维护。
   - **补丁 2**：为权限故障补充 pKVM 映射缓存，以解决在处理权限故障时可能出现的空指针解引用问题。

2. **之前讨论要点**：
   - 讨论中提到 pKVM 的映射列表和缓存管理的复杂性，强调了在处理权限故障时需要确保缓存的有效性。
   - 参与者提出了对补丁的改进建议，包括代码结构和补丁版本管理的最佳实践。

3. **本周的新讨论与进展**：
   - 参与者对补丁进行了详细审查，提出了潜在问题和改进建议。例如，Marc Zyngier 提到补丁的结构需要优化，并建议在发送补丁时附加封面信。
   - Bradley Morgan 表示将根据反馈进行补丁的更新（v3），并计划在更多人审查后再提交。
   - 讨论中还涉及到处理 S1PTW（Stage 1 Page Table Walk）权限故障的复杂性，Oliver Upton 提出需要在处理权限故障时考虑读写权限的评估。

整体来看，本周的讨论集中在补丁的细节审查和优化建议上，显示出开发者对 KVM 的持续关注和对代码质量的重视。

#### 📝 邮件列表

1. **[06-23 16:37]** [PATCH v2 1/2] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[06-23 16:37]** [PATCH v2 2/2] KVM: arm64: top up pKVM mapping cache for permission faults
   - 发件人: Bradley Morgan <include@grrlz.net>
3. **[06-23 16:56]** Re: [PATCH v2 2/2] KVM: arm64: top up pKVM mapping cache for
 permission faults
   - 发件人: sashiko-bot@kernel.org
4. **[06-23 18:02]** Re: [PATCH v2 1/2] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-23 18:04]** =?US-ASCII?Q?Re=3A_=5BPATCH_v2_1/2=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
6. **[06-23 18:13]** Re: [PATCH v2 1/2] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[06-23 19:51]** =?US-ASCII?Q?Re=3A_=5BPATCH_v2_1/2=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
8. **[06-23 20:56]** =?US-ASCII?Q?Re=3A_=5BPATCH_v2_1/2=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
9. **[06-24 13:24]** [PATCH v2 0/2] KVM: arm64: nv: Fix permission checks for S1PTW faults
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[06-24 13:24]** [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if HA is set
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[06-24 13:24]** [PATCH v2 2/2] KVM: arm64: nv: Treat S1PTW permission faults specially
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[06-24 20:35]** Re: [PATCH v2 2/2] KVM: arm64: nv: Treat S1PTW permission faults
 specially
   - 发件人: sashiko-bot@kernel.org
13. **[06-24 20:40]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if
 HA is set
   - 发件人: sashiko-bot@kernel.org
14. **[06-24 14:00]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if
 HA is set
   - 发件人: Oliver Upton <oupton@kernel.org>
15. **[06-24 14:22]** Re: [PATCH v2 2/2] KVM: arm64: nv: Treat S1PTW permission faults
 specially
   - 发件人: Oliver Upton <oupton@kernel.org>
16. **[06-25 15:48]** [PATCH v2 0/2] KVM: arm64: Fix and test MMIO sign-extending loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[06-25 15:48]** [PATCH v2 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[06-25 15:48]** [PATCH v2 2/2] KVM: arm64: selftests: Add MMIO sign-extending load test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
19. **[06-25 14:57]** Re: [PATCH v2 2/2] KVM: arm64: selftests: Add MMIO sign-extending
 load test
   - 发件人: sashiko-bot@kernel.org
20. **[06-25 16:43]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if HA is set
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[06-25 17:14]** Re: [PATCH v2 2/2] KVM: arm64: selftests: Add MMIO sign-extending
 load test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
22. **[06-25 12:34]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if
 HA is set
   - 发件人: Oliver Upton <oupton@kernel.org>
23. **[06-25 21:43]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if HA is set
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[06-25 15:18]** Re: [PATCH v2 1/2] KVM: arm64: Only consider S1PTW a write fault if
 HA is set
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 4: [PATCH v3 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 18 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 26 Jun 2026 08:04:00 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM（Protected KVM）虚拟 CPU 状态同步的重构，主要集中在如何优化状态管理以提高性能和安全性。

**原始 patch/问题的内容**：
Fuad Tabba 提交了一系列补丁（PATCH v3 0/8），旨在重构 pKVM 的 vCPU 状态同步机制，减少在每次世界切换时对非受保护客户机状态的复制。补丁包括对 EL2 状态转移的改进，增加了对 vCPU 查找的原语，并实现了懒惰复制机制。

**之前讨论要点**：
在之前的讨论中，参与者们关注了如何在不影响性能的情况下，确保 pKVM 的隔离性和安全性。补丁的设计基于 Will 的 pKVM 基础设施系列，强调了 EL2 应该具备适当的状态转移原语。

**本周的新讨论、进展或结论**：
本周的讨论中，Fuad 提出了补丁的具体实现细节，包括对 vCPU 状态的懒惰同步、VGIC（虚拟通用中断控制器）状态的最小化暴露等。Marc Zyngier 也参与了补丁的开发，并提出了对 VGIC 状态同步的改进建议。邮件中还提到了一些潜在问题和代码审查结果，强调了在 pKVM 中对 GICv2 的支持问题，以及对非受保护客户机状态的处理方式。整体来看，补丁系列得到了积极的反馈，并在逐步完善中。

#### 📝 邮件列表

1. **[06-26 08:04]** [PATCH v3 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[06-26 08:04]** [PATCH v3 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[06-26 08:04]** [PATCH v3 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[06-26 08:04]** [PATCH v3 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[06-26 08:04]** [PATCH v3 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[06-26 08:04]** [PATCH v3 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[06-26 08:04]** [PATCH v3 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[06-26 08:04]** [PATCH v3 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[06-26 08:04]** [PATCH v3 8/8] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[06-26 07:16]** Re: [PATCH v3 4/8] KVM: arm64: Move PSCI helper functions to a
 shared header
   - 发件人: sashiko-bot@kernel.org
11. **[06-26 08:20]** Re: [PATCH v3 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[06-26 07:24]** Re: [PATCH v3 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
13. **[06-26 08:26]** Re: [PATCH v3 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[06-26 07:27]** Re: [PATCH v3 7/8] KVM: arm64: Add primitives to flush/sync the
 VGIC state at EL2
   - 发件人: sashiko-bot@kernel.org
15. **[06-26 07:29]** Re: [PATCH v3 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
16. **[06-26 08:30]** Re: [PATCH v3 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[06-26 08:33]** Re: [PATCH v3 7/8] KVM: arm64: Add primitives to flush/sync the VGIC
 state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[06-26 08:36]** Re: [PATCH v3 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 5: [PATCH v5 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 15 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 23 Jun 2026 11:53:47 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM (Kernel-based Virtual Machine) 的补丁系列，主要涉及将 FFA_NOTIFICATION* 调用转发到 TrustZone，以支持 Arm FF-A 规范中的异步信号机制。

**原始补丁内容**：
补丁系列的目标是移除 pKVM FF-A 代理中的 FFA_NOTIFICATION* 调用黑名单，这些调用被标记为可选，但由于当前的限制，无法与安全服务进行通信。补丁强调，主机作为唯一的非安全端点，不会导致虚拟机 ID 欺骗风险，同时 FFA_NOTIFICATION* 调用仅通过寄存器参数操作，不涉及内存地址，因此不会引发内存混淆攻击。

**之前讨论要点**：
在历史讨论中，补丁经历了多次版本更新，主要集中在严格的参数检查、处理不同版本的 SMC 调用以及确保安全性等方面。参与者们提出了对补丁的建议和修改意见，以确保符合 FF-A 规范。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现上，包括对 FFA_NOTIFICATION_BIND、UNBIND、SET、GET 和 INFO_GET 的支持。参与者对补丁进行了审查，提出了一些潜在问题，如参数验证不当和对未使用参数的严格检查可能导致的兼容性问题。Sebastian Ene 提到将根据 FF-A 版本调整检查逻辑，并计划发布新版本以解决这些问题。整体来看，讨论显示出对补丁的积极反馈，但也反映出对其兼容性的担忧。

#### 📝 邮件列表

1. **[06-23 11:53]** [PATCH v5 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-23 11:53]** [PATCH v5 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-23 11:53]** [PATCH v5 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-23 11:53]** [PATCH v5 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-23 11:53]** [PATCH v5 4/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-23 11:53]** [PATCH v5 5/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-23 11:53]** [PATCH v5 6/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-23 11:53]** [PATCH v5 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-23 12:01]** Re: [PATCH v5 5/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host
 handler
   - 发件人: sashiko-bot@kernel.org
10. **[06-23 12:05]** Re: [PATCH v5 4/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in
 host handler
   - 发件人: sashiko-bot@kernel.org
11. **[06-23 12:06]** Re: [PATCH v5 1/7] KVM: arm64: Enforce strict SBZ checks in the
 FF-A proxy
   - 发件人: sashiko-bot@kernel.org
12. **[06-23 12:07]** Re: [PATCH v5 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in
 host handler
   - 发件人: sashiko-bot@kernel.org
13. **[06-23 12:07]** Re: [PATCH v5 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in
 host handler
   - 发件人: sashiko-bot@kernel.org
14. **[06-25 14:16]** Re: [PATCH v5 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Will Deacon <will@kernel.org>
15. **[06-26 07:48]** Re: [PATCH v5 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 6: [PATCH v6 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 14 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 26 Jun 2026 07:45:38 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构上将 FFA_NOTIFICATION* 调用转发到 TrustZone 的补丁系列（PATCH v6 0/7）。该补丁的主要目的是移除 pKVM FF-A 代理中对 FFA_NOTIFICATION* 调用的阻止，以支持根据 Arm FF-A 规范定义的异步信号机制与安全服务进行通信。

在历史讨论中，补丁的背景被阐述，强调了当前代理的限制以及为何这些调用不应被阻止。补丁的作者 Sebastian Ene 提出了多个版本的补丁，逐步修正了之前的缺陷，并根据反馈进行了调整。

在本周的新讨论中，Sebastian 提交了补丁的多个具体实现，包括对 FFA_NOTIFICATION_BITMAP、FFA_NOTIFICATION_BIND、FFA_NOTIFICATION_UNBIND、FFA_NOTIFICATION_SET、FFA_NOTIFICATION_GET 和 FFA_NOTIFICATION_INFO_GET 的支持。每个补丁都包含了对参数的验证，以确保安全性。此外，参与者对补丁进行了审查，提出了一些潜在问题和改进建议，例如对 MBZ（Must Be Zero）位的验证不够严格。

最终，Will Deacon 对补丁表示认可，并建议在检查版本时增加对主要版本号的验证，以防未来的更新中出现问题。整体而言，本周的讨论集中在补丁的具体实现和安全性验证上，推动了该功能的进一步完善。

#### 📝 邮件列表

1. **[06-26 07:45]** [PATCH v6 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-26 07:45]** [PATCH v6 1/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-26 07:45]** [PATCH v6 2/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-26 07:45]** [PATCH v6 3/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-26 07:45]** [PATCH v6 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-26 07:45]** [PATCH v6 5/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-26 07:45]** [PATCH v6 6/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-26 07:45]** [PATCH v6 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-26 07:55]** Re: [PATCH v6 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host
 handler
   - 发件人: sashiko-bot@kernel.org
10. **[06-26 07:56]** Re: [PATCH v6 7/7] KVM: arm64: Enforce strict SBZ checks in the
 FF-A proxy
   - 发件人: sashiko-bot@kernel.org
11. **[06-26 07:59]** Re: [PATCH v6 5/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host
 handler
   - 发件人: sashiko-bot@kernel.org
12. **[06-26 10:11]** Re: [PATCH v6 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Will Deacon <will@kernel.org>
13. **[06-26 09:24]** Re: [PATCH v6 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
14. **[06-26 11:55]** Re: [PATCH v6 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 7: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Sun, 21 Jun 2026 21:31:55 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在修复 pKVM 回收机制对虚拟机内存管理（mm）的影响。历史讨论中，Bradley Morgan 提出了该补丁，指出保护的来宾故障会将长期锁定的内存计入虚拟机的 mm 中，而在文件释放时，当前的 mm 可能与之无关，因此建议将计费从 kvm->mm 中移除。

在本周的新讨论中，参与者们对补丁进行了积极的反馈。Marc Zyngier 和 Fuad Tabba 都表示补丁看起来是正确的，并分享了他们的测试结果，确认修复了父进程的 VmLck 泄漏问题。Will Deacon 提出了对 kvm_arch_prepare_memory_region() 函数中使用 current->mm 的疑问，认为可能存在潜在问题，但并未影响当前的补丁讨论。

最终，Marc Zyngier 确认已将该补丁应用于修复分支，并表示感谢参与者的贡献。Fuad Tabba 也提到该补丁将被纳入 ACK，以确保对 Pixel 设备的支持。整体来看，本周的讨论集中在补丁的确认和测试结果上，显示出社区对该修复的认可和支持。

#### 📝 邮件列表

1. **[06-21 21:31]** [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[06-22 09:32]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[06-22 09:32]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[06-22 10:16]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-22 15:49]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Bradley Morgan <include@grrlz.net>
6. **[06-23 14:41]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Will Deacon <will@kernel.org>
7. **[06-23 14:50]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[06-23 14:53]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[06-23 15:30]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Will Deacon <will@kernel.org>
10. **[06-23 16:01]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Bradley Morgan <include@grrlz.net>
11. **[06-23 16:03]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[06-23 16:11]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Bradley Morgan <include@grrlz.net>
13. **[06-23 16:46]** Re: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 8: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 8 Jun 2026 10:36:14 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM64 架构的 RMI（资源管理接口）补丁，主题为“允许填充初始内容”。该补丁的目的是改进 KVM（内核虚拟机）在处理内存映射时的错误返回机制，尤其是在处理“保留”字段时，确保能够正确返回错误代码。

在历史讨论中，参与者们关注了 kvm_arm_rmi_populate() 函数可能返回错误的情况，尤其是当“保留”字段被设置时，讨论了如何更好地处理这些错误。Steven Price 和 Suzuki K Poulose 提出了对补丁的改进建议，确保在错误发生时能够及时返回，而不是仅仅发出警告。

本周的新讨论集中在运行时内存故障处理上，Gavin Shan 报告了在使用 virtio-net-pci 设备时遇到的问题，指出共享空间的阶段2页面故障处理存在缺陷，导致数据未能正确传递到 QEMU。Suzuki K Poulose 和其他参与者讨论了如何通过调整内存映射权限来解决这些问题，并确认了需要对 KVM 驱动进行修复以解决当前的权限故障问题。此外，Lorenzo Pieralisi 提到即将发布的 QEMU 补丁将包含相关修复。

总结而言，邮件讨论围绕着 ARM64 RMI 补丁的错误处理和运行时内存故障问题展开，参与者们积极提出改进建议，并确认了后续的修复计划。

#### 📝 邮件列表

1. **[06-08 10:36]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
2. **[06-08 10:41]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[06-08 14:53]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
4. **[06-25 23:53]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
5. **[06-25 16:58]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[06-25 17:19]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[06-26 17:43]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
8. **[06-26 09:47]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[06-26 10:04]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[06-26 21:43]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
11. **[06-26 18:44]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
12. **[06-28 20:33]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>

---

### Thread 9: [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 23 Jun 2026 15:24:40 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 Shadow ptdump 的修复补丁（PATCH 0/3）。该补丁主要解决了两个问题：一是使用后释放（UAF）问题，二是在原子上下文中睡眠的问题。

在历史讨论中，补丁的背景是基于之前的修复和讨论，指出了在关闭 debugfs 文件时，嵌套的 MMU 仍然可能被访问，从而导致 UAF。原有的代码在绑定和解绑上下文时创建和删除 debugfs 文件，但由于这些操作可能会导致睡眠，因此引发了并发问题。

本周的新讨论中，Wei-Lin Chang 提出了具体的修复方案，包括：为每个嵌套的 MMU 实例创建单独的 debugfs 文件，以避免在持有 mmu_lock 时进行文件创建和删除的睡眠操作。此外，邮件中提到了一些潜在的高风险问题，如内核崩溃和空指针解引用，参与者们对此进行了讨论和反馈。Wei-Lin Chang 还指出了在 VM 销毁过程中，debugfs 文件的移除顺序可能导致 UAF 和错误解引用的问题，并提出了改进的思路，包括在 kvm_destroy_vm_debugfs() 中统一移除所有 ptdump 文件，以避免并发访问问题。

总体来看，本周的讨论集中在如何有效解决现有代码中的并发问题和内存管理问题，以确保 KVM 的稳定性和可靠性。

#### 📝 邮件列表

1. **[06-23 15:24]** [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[06-23 15:24]** [PATCH 1/3] KVM: arm64: nv: Print nested mmu info in kvm_ptdump_guest_show()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[06-23 15:24]** [PATCH 2/3] KVM: arm64: ptdump: Store both mmu and kvm pointers in kvm_ptdump_guest_state
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[06-23 15:24]** [PATCH 3/3] KVM: arm64: nv: Move to per nested mmu ptdump files
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[06-23 14:40]** Re: [PATCH 1/3] KVM: arm64: nv: Print nested mmu info in
 kvm_ptdump_guest_show()
   - 发件人: sashiko-bot@kernel.org
6. **[06-23 14:41]** Re: [PATCH 3/3] KVM: arm64: nv: Move to per nested mmu ptdump files
   - 发件人: sashiko-bot@kernel.org
7. **[06-23 19:05]** Re: [PATCH 1/3] KVM: arm64: nv: Print nested mmu info in
 kvm_ptdump_guest_show()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[06-23 19:10]** Re: [PATCH 3/3] KVM: arm64: nv: Move to per nested mmu ptdump files
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[06-24 15:02]** Re: [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
10. **[06-25 08:47]** Re: [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
11. **[06-25 10:54]** Re: [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[06-26 10:37]** Re: [PATCH 0/3] KVM: arm64: nv: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 10: [PATCH v3 0/5] KVM: arm64: nv: Even more VNCR fixes

**📧 邮件数**: 9 | **👥 参与者**: 4 | **📅 开始时间**: Thu, 18 Jun 2026 16:42:01 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VNCR（Virtual Non-Cacheable Register）修复的补丁系列。

1. **原始补丁内容**：Oliver Upton 提出的补丁系列（PATCH v3 0/5）旨在解决 VNCR 处理中的多个问题，特别是关于权限检查和错误处理的缺陷。补丁包括对只读物理页框号（PFN）的处理、在注入中断前重新翻译 VNCR 以及标记虚拟机为有缺陷等。

2. **之前讨论要点**：在历史讨论中，参与者指出了补丁中的潜在问题，例如在只读内存槽上访问 VNCR 时错误地提升权限故障为外部中断（External Abort），以及在处理写入时可能导致的 CPU 死锁等。这些问题的解决需要更复杂的代码重构。

3. **本周的新讨论与进展**：本周的讨论中，Oliver 强调了补丁的目标是快速修复一个严重的漏洞，允许来宾绕过主机权限，并表示更复杂的故障优先级问题可以在后续的清理工作中解决。此外，Marc Zyngier 确认了补丁已被应用到修复分支，并列出了每个补丁的提交信息，表明这些修复已获得认可并实施。

总的来说，本次讨论集中在 VNCR 的权限处理和错误管理上，补丁系列的实施将有助于提高 KVM 的稳定性和安全性。

#### 📝 邮件列表

1. **[06-18 16:42]** [PATCH v3 0/5] KVM: arm64: nv: Even more VNCR fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-18 16:42]** [PATCH v3 1/5] KVM: arm64: nv: Respect read-only PFN when mapping L1 VNCR
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-18 16:42]** [PATCH v3 3/5] KVM: arm64: nv: Re-translate VNCR before injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-19 00:00]** Re: [PATCH v3 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: sashiko-bot@kernel.org
5. **[06-19 00:07]** Re: [PATCH v3 1/5] KVM: arm64: nv: Respect read-only PFN when
 mapping L1 VNCR
   - 发件人: sashiko-bot@kernel.org
6. **[06-22 10:10]** Re: [PATCH v3 1/5] KVM: arm64: nv: Respect read-only PFN when
 mapping L1 VNCR
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[06-22 10:18]** Re: [PATCH v3 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[06-23 16:46]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
9. **[06-23 14:53]** Re: [PATCH v3 0/5] KVM: arm64: nv: Even more VNCR fixes
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 11: [PATCH 0/2] KVM: arm64: Fix and test MMIO sign-extending loads

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 22 Jun 2026 20:06:59 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM 的 arm64 架构中 MMIO（内存映射输入输出）操作的修复和测试，主要集中在处理符号扩展加载的问题。

**原始 patch/问题的内容**：
Fuad Tabba 提出了两个补丁，旨在修复从模拟的 MMIO 读取时符号扩展加载（LDRSB、LDRSH、LDRSW）返回零扩展值的问题。补丁 1 修复了这一问题，补丁 2 则增加了自测以确保该问题不会再次出现。

**之前讨论要点**：
在之前的讨论中，参与者们探讨了 MMIO 读取的字节序和符号扩展的顺序问题。Marc Zyngier 提出，当前的实现可能在处理字节交换时存在逻辑错误，导致符号扩展无法正确执行。Fuad 解释了 ARM 架构中的字节顺序与符号扩展的关系，并认为问题的根源在于操作顺序不当。

**本周的新讨论、进展或结论**：
本周的讨论中，Fuad 收到了 Oliver Upton 的审查反馈，确认了补丁的有效性。Marc Zyngier 进一步建议改进提交日志的描述，并要求增加对大端访问的测试。Fuad 表示将根据反馈进行修改和扩展测试。整体来看，讨论推动了对补丁的理解和完善，确保了 MMIO 操作的正确性。

#### 📝 邮件列表

1. **[06-22 20:06]** [PATCH 0/2] KVM: arm64: Fix and test MMIO sign-extending loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[06-22 20:07]** [PATCH 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[06-22 20:07]** [PATCH 2/2] KVM: arm64: selftests: Add MMIO sign-extending load test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[06-22 17:20]** Re: [PATCH 0/2] KVM: arm64: Fix and test MMIO sign-extending loads
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-23 14:08]** Re: [PATCH 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[06-23 14:51]** Re: [PATCH 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[06-25 11:10]** Re: [PATCH 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[06-25 12:13]** Re: [PATCH 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 12: [PATCH v3 0/3] KVM: arm64: fix pKVM mapping cache corner cases

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 24 Jun 2026 16:00:25 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM 映射缓存问题的修复补丁（PATCH v3 0/3）。本次补丁主要包含三个部分：

1. **原始补丁内容**：
   - **补丁 1**：修复非缓存映射的 pKVM 缓存维护问题。
   - **补丁 2**：解决权限故障时 pKVM 映射缓存的顶补错误。
   - **补丁 3**：修复在脏日志情况下，权限故障仍需进行页面表分配的问题。

2. **之前讨论要点**：
   - 本次补丁是独立的 v3 版本，之前的版本（v2）已增加了补丁 2 的内容。补丁的修改旨在优化 pKVM 的缓存管理，确保在不同情况下（如权限故障和脏日志）能正确处理映射。

3. **本周的新讨论与进展**：
   - 本周的讨论中，Bradley Morgan 提到补丁 3 可能与补丁 2 存在冲突，计划在后续版本中合并更新。最终，他决定暂时放弃补丁 2 和 3，只提交补丁 1。参与者 Marc Zyngier 提出建议，强调在版本发布之间留出时间以便于审查和反思，避免频繁更新导致审查者的忽视。

整体来看，本周的讨论集中在补丁的细节修正和版本管理策略上，反映了开发者在优化 KVM 性能和维护代码质量方面的努力。

#### 📝 邮件列表

1. **[06-24 16:00]** [PATCH v3 0/3] KVM: arm64: fix pKVM mapping cache corner cases
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[06-24 16:00]** [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Bradley Morgan <include@grrlz.net>
3. **[06-24 16:00]** [PATCH v3 2/3] KVM: arm64: top up pKVM mapping cache for permission faults
   - 发件人: Bradley Morgan <include@grrlz.net>
4. **[06-24 16:00]** [PATCH v3 3/3] KVM: arm64: top up stage 2 memcache for dirty logging faults
   - 发件人: Bradley Morgan <include@grrlz.net>
5. **[06-24 18:39]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_3/3=5D_KVM=3A_arm64=3A_top_up_s?=
 =?US-ASCII?Q?tage_2_memcache_for_dirty_logging_faults?=
   - 发件人: Bradley Morgan <include@grrlz.net>
6. **[06-24 18:46]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_3/3=5D_KVM=3A_arm64=3A_top_up_s?=
 =?US-ASCII?Q?tage_2_memcache_for_dirty_logging_faults?=
   - 发件人: Bradley Morgan <include@grrlz.net>
7. **[06-24 19:25]** Re: [PATCH v3 3/3] KVM: arm64: top up stage 2 memcache for dirty logging faults
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[06-24 19:37]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_3/3=5D_KVM=3A_arm64=3A_top_up_s?=
 =?US-ASCII?Q?tage_2_memcache_for_dirty_logging_faults?=
   - 发件人: Bradley Morgan <include@grrlz.net>

---

### Thread 13: [PATCH v2 kvmtool 0/4] Add support for running protected VMs on arm64

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 25 Jun 2026 18:10:41 +0100

#### 🤖 AI 总结

本邮件讨论的主题是为 arm64 架构添加对受保护虚拟机（VM）的支持，包含四个补丁（patch）。补丁的主要内容包括：

1. **原始补丁/问题的内容**：补丁旨在实现受保护虚拟机的创建，允许在 arm64 上运行受保护的虚拟机。补丁中引入了一个新的 `--protected` 参数，以请求从内核创建受保护的 VM 类型，并在设备树中宣传一个保留的 DMA 区域。

2. **之前的讨论要点**：在本周之前的讨论中，补丁 v1 版本已被提交，参与者对其进行了初步的反馈和修改。补丁经过修改后，增加了对较旧主机内核的兼容性检查，并确保用户指定的来宾内存不小于受限 DMA 池的大小。

3. **本周的新讨论、进展或结论**：本周的讨论中，补丁 v2 版本被提交，包含了对之前版本的改进。所有补丁均获得了参与者的测试和审核，最终被 Will Deacon 应用到 kvmtool 的主分支中。补丁的具体实现包括同步内核 UAPI 头文件、为现代 virtio 传输提取基本特性、添加启用 VIRTIO_F_ACCESS_PLATFORM 的助手函数，以及实现对受保护虚拟机的支持。

整体来看，本周的讨论集中在补丁的最终确认和应用上，标志着对 arm64 受保护虚拟机支持的进一步推进。

#### 📝 邮件列表

1. **[06-25 18:10]** [PATCH v2 kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Will Deacon <will@kernel.org>
2. **[06-25 18:10]** [PATCH v2 kvmtool 1/4] Sync kernel UAPI headers with v7.1
   - 发件人: Will Deacon <will@kernel.org>
3. **[06-25 18:10]** [PATCH v2 kvmtool 2/4] virtio: Factor out base features for modern virtio transports
   - 发件人: Will Deacon <will@kernel.org>
4. **[06-25 18:10]** [PATCH v2 kvmtool 3/4] virtio: Add helper for enabling VIRTIO_F_ACCESS_PLATFORM
   - 发件人: Will Deacon <will@kernel.org>
5. **[06-25 18:10]** [PATCH v2 kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
6. **[06-25 20:42]** Re: [PATCH v2 kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[06-26 12:07]** Re: [PATCH v2 kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 14: [PATCH kvmtool 0/4] Add support for running protected VMs on arm64

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 19 Jun 2026 12:54:10 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 arm64 平台的 kvmtool 的补丁，旨在支持运行受保护的虚拟机（VM）。历史讨论中，Will Deacon 提出了一个包含四个补丁的系列，主要是为了在启用 pKVM 的情况下，支持受保护的 VM。补丁中引入了一个新的参数 `--protected`，用于请求创建受保护的 VM 类型，并在设备树中宣传一个保留的 DMA 区域。

在之前的讨论中，Fuad Tabba 对补丁提出了一些建议，包括如何处理内存分配和 DMA 传输的相关问题。他建议在内存不足时发出警告，并对补丁进行了初步的测试和审核。

在本周的新讨论中，Will Deacon 和 Fuad Tabba 继续探讨了如何处理 DMA 内存池的大小问题。Will 提出了一种检查机制，如果虚拟机配置的内存小于所需的 DMA 缓冲区，则会导致错误。Fuad 表示赞同这一改进，并认为比之前的建议更好。Suzuki K Poulose 也参与讨论，提到未来可以考虑让用户指定 DMA 池的大小，以便更灵活地处理不同设备的需求。整体来看，本周的讨论集中在补丁的细节改进和未来可能的扩展上。

#### 📝 邮件列表

1. **[06-19 12:54]** [PATCH kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Will Deacon <will@kernel.org>
2. **[06-19 12:54]** [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
3. **[06-19 14:49]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[06-23 16:34]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
5. **[06-23 17:37]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[06-24 09:53]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[06-25 18:01]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 15: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due to S1PTW

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 23 Jun 2026 14:13:10 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“检查因 S1PTW（Stage 1 Page Table Walk）导致的指令中止的读写权限”。该补丁的主要目的是在处理 S1PTW 时，确保在评估执行权限之前检查读写权限，以避免因缺失权限而导致的错误。

在历史讨论中，未提及具体的补丁内容，但本周的讨论集中在补丁的实现细节上。Oliver Upton 提出了补丁的具体修改，指出 S1PTW 导致的权限错误应被视为表走查缺失读写权限，而非输出翻译的执行权限。补丁通过在检查执行权限之前增加对 S1PTW 的检查，来解决这个问题。

本周的新讨论中，Sashiko-bot 提到了一些潜在问题，指出恶意的 L1 客户机可能会利用 S1PTW 权限错误导致 KVM 进入无限循环。对此，Oliver Upton 进行了回应，认为这种情况并不完全是恶意行为，而是客户机自身的配置问题。同时，Marc Zyngier 也提出了对补丁的建议，认为在处理 HD（Hypervisor Domain）时也应进行类似的评估。最终，Oliver 确认了补丁的有效性，并建议在代码中增加注释以提高可读性。整体来看，本周讨论对补丁的细节进行了深入的审查和优化。

#### 📝 邮件列表

1. **[06-23 14:13]** [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due to S1PTW
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-23 21:32]** Re: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due
 to S1PTW
   - 发件人: sashiko-bot@kernel.org
3. **[06-23 17:07]** Re: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due
 to S1PTW
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-24 09:41]** Re: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due to S1PTW
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-24 02:39]** Re: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due
 to S1PTW
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-24 10:57]** Re: [PATCH] KVM: arm64: nv: Check RW permissions for insn abort due to S1PTW
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 16: [PATCH kvmtool v2 0/7] x86 compilation fixes and arm64 PMU improvements

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 18 Jun 2026 16:49:54 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 工具的多个补丁，主要集中在 x86 编译修复和 arm64 PMU（性能监控单元）改进上。

**原始 patch/问题内容**：
最初的补丁系列（[PATCH kvmtool v2 0/7]）旨在解决编译错误，具体包括在 `disk/core.c` 中的指针类型问题和 `x86/include/kvm/bios.h` 中的属性忽略错误。此外，补丁还涉及对 arm64 PMU 诊断的改进，以便在配置 PMU 时提供更具体的错误信息。

**之前讨论要点**：
在历史讨论中，Alexandru Elisei 提出了补丁的具体内容和目的，Oliver Upton 也建议对代码进行更广泛的清理，以减少重复的错误处理代码。讨论中提到，改进 PMU 诊断的补丁可以避免潜在的数组越界访问。

**本周的新讨论、进展或结论**：
本周的讨论中，Alexandru 和 Oliver 确认了对 PMU 诊断补丁的修改意见，并决定将 PMU 的宏引入当前补丁系列，而其他代码的清理工作将放在后续进行。此外，Will Deacon 宣布已将所有补丁应用到 KVM 工具的主分支中，标志着这些修复和改进的正式集成。

#### 📝 邮件列表

1. **[06-18 16:49]** [PATCH kvmtool v2 0/7] x86 compilation fixes and arm64 PMU improvements
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[06-18 16:50]** [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL diagnostics
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[06-18 12:06]** Re: [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL
 diagnostics
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-22 10:04]** Re: [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL
 diagnostics
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
5. **[06-22 09:55]** Re: [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL
 diagnostics
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-23 14:02]** Re: [PATCH kvmtool v2 0/7] x86 compilation fixes and arm64 PMU improvements
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 17: [PATCH v2 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 19 Jun 2026 08:07:11 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态同步进行重构的补丁（PATCH v2 0/8）。该补丁的主要目的是实现非保护性客户机的懒惰 vCPU 状态同步，以减少不必要的寄存器上下文复制，从而提高性能。

在历史讨论中，Fuad Tabba 提出了补丁的多个改进，包括删除了一些独立的 guard() 转换补丁，并对 PKVM_HOST_STATE_DIRTY 标志进行了分组和注释的澄清。此外，补丁还实现了在每次非保护性退出时同步 PSTATE 和 PC 的功能。

本周的新讨论中，Vincent Donnefort 提出了将状态同步逻辑提取到一个单独的函数 handle_exit_pkvm_state() 中的建议，以提高代码的可读性。Fuad Tabba 对此表示赞同，并确认将在下一个版本中进行修改。

总体来看，讨论围绕着优化 vCPU 状态同步的实现细节，参与者们积极提出建议，以确保补丁的清晰性和功能性。

#### 📝 邮件列表

1. **[06-19 08:07]** [PATCH v2 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-19 08:07]** [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-19 14:12]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[06-19 17:41]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-22 09:49]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[06-22 11:14]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 18: [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops

**📧 邮件数**: 5 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 26 Jun 2026 12:13:44 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于对 KVM（Kernel-based Virtual Machine）中的 `kvm_io_bus_get_dev()` 函数进行改进的补丁。该函数目前仅根据地址匹配设备，这可能导致生命周期问题，因为在调用者检查对象时，匹配的设备可能已经不存在。

历史讨论中，Marc Zyngier 提出了补丁，目的是在返回设备指针之前，增加对设备操作的检查，以确保返回的设备是预期的类型。补丁的实现涉及到在 `kvm_io_bus_get_dev()` 函数中添加一个指向 `kvm_io_device_ops` 的指针，并更新唯一的调用者以传递自己的操作指针。

在本周的新讨论中，参与者对补丁进行了反馈。Sashiko AI 发现了潜在的使用后释放问题，Marc Zyngier 提出可以在持有 SRCU 锁的情况下进行过滤，以避免此问题。Will Deacon 表示支持该补丁，并给予了认可。Oliver Upton 则建议将锁定操作放在调用者中，以确保在访问对象时能够安全地释放 SRCU 锁。

总体来看，本周的讨论集中在补丁的实现细节和潜在问题的解决方案上，参与者们对补丁的方向表示认可，并提出了进一步的优化建议。

#### 📝 邮件列表

1. **[06-26 12:13]** [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[06-26 11:46]** Re: [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops
   - 发件人: sashiko-bot@kernel.org
3. **[06-26 13:41]** Re: [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-26 14:09]** Re: [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops
   - 发件人: Will Deacon <will@kernel.org>
5. **[06-26 10:26]** Re: [PATCH] KVM: Make kvm_io_bus_get_dev() filter devices by ops
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 19: [PATCH 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 19 Jun 2026 08:05:00 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态同步的重构，具体涉及到多个补丁（patch）的提交。

1. **原始 patch/问题的内容**：Fuad Tabba 提交了一系列补丁（共8个），主要目的是重构 pKVM vCPU 状态同步，优化代码结构并提高性能。补丁中提到，删除了一些独立的 guard()/scoped_guard() 转换补丁，并对 VGIC 刷新原语进行了改进，以减少对 ICH_VTR_EL2 的读取。

2. **之前的讨论要点**：在历史讨论中，参与者对补丁进行了审查，指出了新添加的头文件 `include/kvm/arm_psci.h` 在自包含性方面存在问题，缺少对依赖项的包含。Fuad 对此进行了回应，强调该头文件在提交之前就已经存在类似问题，且相关依赖项在其他文件中已经可用。

3. **本周的新讨论、进展或结论**：本周的讨论中，Fuad 再次重申了之前的观点，指出该头文件的自包含性问题并非由他的新补丁引入，且相关依赖项的处理在现有代码中是合理的。整体来看，本周的讨论主要是对之前审查意见的澄清，并未出现新的进展或结论。

总结而言，邮件讨论集中在对 KVM arm64 pKVM 状态同步补丁的审查与回应，强调了代码的自包含性问题及其历史背景。

#### 📝 邮件列表

1. **[06-19 08:05]** [PATCH 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-19 08:05]** [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-19 07:16]** Re: [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared
 header
   - 发件人: sashiko-bot@kernel.org
4. **[06-19 08:24]** Re: [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-26 08:19]** Re: [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 20: [PATCH RESEND v2 0/5] KVM: arm64: nv: Even more VNCR fixes

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  9 Jun 2026 11:55:09 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构下的 VNCR（虚拟网络控制寄存器）的一系列修复补丁，主要由 Oliver Upton 提出并进行更新。

在历史讨论中，Oliver 提出了多个补丁，主要包括：
1. 在映射 L1 VNCR 时，KVM 需要在写入前故障处理 PFN（页框号）。
2. 防止 KVM 映射非内存 PFN 的缓存映射，尽管这与 stage-2 的语义不完全一致。
3. 处理 VNCR 中的中止循环问题，确保在 KVM 无法处理的情况下能够正确处理 VM。

讨论中，Wei-Lin Chang 提出了对代码复杂性的担忧，认为 kvm_translate_vncr() 函数的多重功能和潜在错误使得理解和维护变得困难。他建议对软件 PTW（页表行走）进行重构，以简化错误处理。

在本周的新讨论中，Wei-Lin 对 Oliver 的建议表示感谢，并表示将其列入潜在改进列表，但目前需要优先处理其他修复。这表明讨论仍在继续，未来可能会有进一步的改进和更新。

#### 📝 邮件列表

1. **[06-09 11:55]** [PATCH RESEND v2 0/5] KVM: arm64: nv: Even more VNCR fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-09 11:55]** [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-10 14:46]** Re: [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[06-18 14:52]** Re: [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-23 15:44]** Re: [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 21: [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 17 Jun 2026 14:51:23 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 ARM FF-A（Firmware Framework for Arm）中的 Endpoint Memory Access Descriptor（EMAD）偏移计算问题的补丁系列（PATCH v7 0/7）。该补丁旨在修复 EMAD 偏移计算，并为 FF-A 驱动和 pKVM 虚拟机监控器添加必要的边界检查。

在历史讨论中，Sebastian Ene 提到，FF-A 版本 1.1 之前，内存区域头部没有明确指定 EMAD 的偏移量，导致假设 EMAD 紧随其后。然而，从版本 1.1 开始，规范要求使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。Vincent Donnefort 提出可以用 `ffa_mem_desc_offset()` 替代 `mem_region_len`，但未得到支持。

在本周的新讨论中，Sebastian Ene 和 Vincent Donnefort 讨论了 `ffa_mem_desc_offset` 的使用问题，指出该函数需要解引用 `struct ffa_mem_region` 来提取 `ep_mem_offset`。他们一致认为引入一个辅助函数来获取 `struct ffa_mem_region` 的大小会更容易理解，且该大小根据 FF-A 版本不同而异。Sebastian 表示将会发布新版本的补丁以解决这些问题并收集审查意见。

#### 📝 邮件列表

1. **[06-17 14:51]** [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-17 14:51]** [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-18 17:56]** Re: [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[06-22 09:23]** Re: [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-22 11:22]** Re: [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 22: [PATCH] KVM: selftests: fix steal_time for arm64

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 22 Jun 2026 12:02:05 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM 自测试的补丁，旨在修复 arm64 架构下的 steal_time 测试问题。原始补丁的目的是解决当主机页面大小大于 4K 时，测试出现的失败情况，具体错误信息显示虚拟机的页面数量与主机不兼容。

在之前的讨论中，Zenghui Yu 报告了一个错误，指出在使用 16K 主机页面大小时，测试失败，导致虚拟机页面调整不成功。Sebastian Ott 提出了修复方案，修改了测试代码，以确保虚拟机的页面数量与主机兼容。

在本周的新讨论中，Sebastian 提交了修复补丁，并得到了 Zenghui 的认可，表示代码看起来不错并进行了审核。Zenghui 还提出了一个建议，询问是否使用 `vm_calc_num_guest_pages(VM_MODE_DEFAULT, STEAL_TIME_SIZE)` 来更好地描述要添加的页面数量。

总的来说，本周的讨论集中在补丁的提交和审核上，修复了之前报告的问题，并对代码进行了进一步的优化建议。

#### 📝 邮件列表

1. **[06-22 12:02]** Re: [PATCH] KVM: selftests: fix steal_time for arm64
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
2. **[06-22 16:14]** [PATCH] KVM: selftests: fix steal_time for arm64 with host page size
 > 4K
   - 发件人: Sebastian Ott <sebott@redhat.com>
3. **[06-28 23:32]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
4. **[06-28 23:44]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

### Thread 23: [PATCH v12 13/16] KVM: selftests: Add guest_memfd based
 vm_mem_backing_src_types

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 26 Jun 2026 14:22:35 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）的补丁，主题为“添加基于 guest_memfd 的 vm_mem_backing_src_types”。该补丁旨在增强 KVM 的自测试功能。

在历史讨论中，补丁的背景信息并未详细列出，但可以推测该补丁与内存管理和资源释放相关。具体来说，补丁的实现可能涉及到对虚拟机内存区域的管理。

本周的新讨论中，Brendan Jackman 提出了一个问题，指出在 `__vm_mem_region_delete()` 函数中出现了双重关闭（double-close）的问题，这一问题是由于新引入的 `kvm_free_fd()` 函数导致的。他认为这个问题可以通过让 `__vm_mem_region_delete()` 函数意识到可能是同一个文件描述符来解决。此外，Marc Zyngier 讨论了与 KVM 相关的页面大小和直接映射的支持，确认了相关检查的有效性。最后，Takahiro Itazuri 表示他将推动该补丁的进展，并提到希望借此机会引入 ALLOC_UNMAPPED 功能，以解决一些安全性问题。

总体来看，本周的讨论集中在补丁的潜在问题及其解决方案上，同时也涉及到对 KVM 功能的进一步扩展。

#### 📝 邮件列表

1. **[06-26 14:22]** Re: [PATCH v12 13/16] KVM: selftests: Add guest_memfd based
 vm_mem_backing_src_types
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
2. **[06-26 14:45]** Re: [PATCH v12 09/16] KVM: arm64: define
 kvm_arch_gmem_supports_no_direct_map()
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
3. **[06-26 15:28]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>

---

### Thread 24: [PATCH 6.12] KVM: arm64: Take the SRCU lock for page table walks in fault injection and AT emulation

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 26 Jun 2026 16:42:07 +0300

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的一个补丁，主要涉及在故障注入和 AT 模拟中的页表遍历时获取 SRCU 锁的问题。

**原始补丁内容**：
补丁编号为 6.12，提出在调用 `walk_s1()` 和 `kvm_walk_nested_s2()` 函数时，确保持有 `kvm->srcu` 锁，以防止内存槽的变化。补丁修复了在调用 `__kvm_at_s12()` 和 `__kvm_find_s1_desc_level()` 时未持有该锁的问题。

**之前讨论要点**：
历史讨论中并未提供具体的背景信息，但补丁的修复是基于之前的代码逻辑，确保在进行页表遍历时的安全性。

**本周新讨论进展**：
本周的讨论中，参与者 Alexander Martyniuk 指出补丁的实现细节，并提到只修复了 `__kvm_at_s12()`，而 `__kvm_find_s1_desc_level()` 并不存在。此外，Sashiko AI 评审发现了一个潜在问题，即在进行阶段-2 转换表遍历失败时，可能会返回负错误码而未更新 ESR 或 PAR_EL1，导致阶段-1 IPA 显示为错误的成功状态。Marc Zyngier 则提到之前的讨论链接，表示某些内容可能不需要进一步处理。整体来看，补丁的讨论集中在确保代码的正确性和安全性上。

#### 📝 邮件列表

1. **[06-26 16:42]** [PATCH 6.12] KVM: arm64: Take the SRCU lock for page table walks in fault injection and AT emulation
   - 发件人: Alexander Martyniuk <alexevgmart@gmail.com>
2. **[06-26 13:58]** Re: [PATCH 6.12] KVM: arm64: Take the SRCU lock for page table
 walks in fault injection and AT emulation
   - 发件人: sashiko-bot@kernel.org
3. **[06-26 15:20]** Re: [PATCH 6.12] KVM: arm64: Take the SRCU lock for page table walks in fault injection and AT emulation
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 25: [PATCH] KVM: arm64: skip pKVM cache flushes for non cacheable mappings

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 23 Jun 2026 16:03:39 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在跳过对不可缓存映射的 pKVM 缓存刷新操作。

**原始补丁内容**：
补丁由 Bradley Morgan 提出，目的是记录映射是否为缓存可用，并在处理不可缓存映射时跳过缓存维护。这是因为 pKVM 在执行阶段 2 操作时，使用自己的映射列表，导致其在刷新路径中失去了通用阶段 2 遍历器所做的 PTE 属性检查。

**之前的讨论要点**：
在历史讨论中并没有相关的背景信息，但补丁中提到的修复是针对之前引入的一个问题（提交 ID: e912efed485a），该问题涉及到 pKVM MMU 的引入。

**本周的新讨论与进展**：
本周的讨论中，Bradley Morgan 提交了补丁，并得到了 Sashiko-bot 的反馈，指出了一个潜在的关键问题：在处理权限故障时，如果将映射升级为大页，会跳过内存缓存的补充，导致 `pkvm_pgtable_stage2_map()` 中出现空指针解引用的问题。Bradley 对此表示感谢，并计划在后续补丁中进行修复。

总体来看，本周的讨论集中在补丁的实现细节及其潜在问题的识别上，显示出社区对代码质量的关注。

#### 📝 邮件列表

1. **[06-23 16:03]** [PATCH] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[06-23 16:15]** Re: [PATCH] KVM: arm64: skip pKVM cache flushes for non cacheable
 mappings
   - 发件人: sashiko-bot@kernel.org
3. **[06-23 17:25]** =?US-ASCII?Q?Re=3A_=5BPATCH=5D_KVM=3A_arm64=3A_skip_pKVM_cac?=
 =?US-ASCII?Q?he_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>

---

### Thread 26: [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 27 Jun 2026 11:51:05 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）中的一个补丁，标题为“[PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers”。该补丁的主要内容是将 `kvm_io_bus_get_dev()` 函数的锁定责任转移给调用者，以解决潜在的生命周期问题。原函数在返回设备时，仅通过地址进行匹配，这可能导致在调用者检查对象时，匹配的设备已经消失。

在之前的讨论中，Marc Zyngier 提出了这一问题，并指出现有的实现方式可能导致不一致性。为了解决这一问题，补丁建议将锁定责任转移给唯一的调用者，这样调用者可以根据需要保持 `srcu` 锁的持有状态。此外，该补丁还与其他 `kvm_io_bus*()` 辅助函数保持一致，后者已经要求调用者持有 `srcu` 锁。

在本周的新讨论中，Marc Zyngier 发布了补丁的第二版，并进行了相应的代码修改，简化了实现。Oliver Upton 对补丁进行了审查，并表示支持，确认了补丁的有效性。这表明该补丁得到了积极的反馈，可能会在后续版本中被采纳。

#### 📝 邮件列表

1. **[06-27 11:51]** [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[06-27 11:14]** Re: [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking
 responsibilities to callers
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 27: [PATCH v2 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 18 Jun 2026 13:16:36 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM/arm64 中缺失的 ESR_ELx.IL 在异常注入中的问题。历史讨论中，Fuad Tabba 提出了一个补丁系列（共7个补丁），旨在解决在多种异常情况下（如未知异常、指令中止、数据中止等）未正确设置 ESR_ELx.IL 的问题。根据 ARM 架构的要求，某些异常类必须将 ESR_ELx.IL 设置为1，尽管指令长度不同。

在本周的新讨论中，Marc Zyngier 确认已将这些补丁应用于修复分支，并感谢 Fuad 的工作。补丁包括对注入的未定义异常、指令中止异常、FPAC 异常等的处理，确保在各种情况下都能正确设置 IL 值。具体的补丁提交信息也被列出，显示出各个补丁的功能和提交状态。

总结来说，本周的讨论确认了补丁的应用，标志着该问题的解决进展。

#### 📝 邮件列表

1. **[06-18 13:16]** [PATCH v2 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-23 14:53]** Re: [PATCH v2 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 28: [PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 16 Jun 2026 15:41:42 +0000

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在将 FFA_NOTIFICATION* 调用转发至 TrustZone。该补丁的主要内容是移除 pKVM FF-A 代理中对 FFA_NOTIFICATION* 调用的封锁，这一限制曾妨碍了根据 Arm FF-A 规范定义的异步信号机制与安全服务的通信。

在历史讨论中，Sebastian Ene 提出了该补丁，解释了封锁的原因及其不必要性，强调主机作为唯一的非安全端点（VM ID 0）与安全世界的交互不应受到限制。

在本周的新讨论中，Vincent Donnefort 对整个补丁系列进行了审查，并表示支持，给予了“Reviewed-by”的标记。这表明补丁得到了积极的反馈，可能会在后续的版本中被采纳。整体来看，讨论进展顺利，补丁的接受度较高。

#### 📝 邮件列表

1. **[06-16 15:41]** [PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-23 12:24]** Re: [PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 29: [PATCH v1] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 25 Jun 2026 14:09:02 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 的一个补丁，旨在忽略仅使用 guest_memfd 的内存槽（memslots）中的 MMU 通知（MMU notifiers）。补丁的主要内容是，当内存槽仅由 guest_memfd 提供时，虚拟机的内存映射直接从 guest_memfd 文件获取，而不是通过用户空间映射。因此，MMU 通知不应影响这些内存槽的二级 MMU。

在历史讨论中，参与者提到 MMU 通知在某些情况下会被调用，例如自动 NUMA 平衡，但实际测试中未能验证。补丁的提出者 Alexandru Elisei 认为，这种情况主要会导致性能问题，且需要确保内存在二级 MMU 中保持映射，以支持正在上游的 Arm 特性（SPE）。

本周的新讨论中，Alexandru Elisei 提交了补丁的第一个版本（v1），并详细描述了补丁的实现和测试结果。他提到，经过修改后，KVM 在处理内存映射时不会因用户空间的 munmap 操作而解除对 guest_memfd 相关内存的映射，确保了功能的正确性。此外，补丁还修复了之前讨论中提到的无效化不平衡问题，并对提交信息进行了修改。整体来看，该补丁旨在提升 KVM 对于 guest_memfd 内存槽的处理效率和稳定性。

#### 📝 邮件列表

1. **[06-25 14:09]** [PATCH v1] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

## 📌 RFC

共 2 个 thread

---

### Thread 1: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 7 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 15 Jun 2026 16:52:44 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 的补丁提案，主题为“忽略仅限于 guest_memfd 的内存槽的 MMU 通知器”。该补丁旨在针对仅使用 guest_memfd 的内存槽（即 kvm_memslot_is_gmem_only() 为真时），不再考虑 MMU 通知器的影响，因为虚拟机的内存提供者是 guest_memfd 文件，而不是用户空间的映射。

在历史讨论中，参与者指出该补丁可能会导致主机级的使用后释放（Use-After-Free）问题，特别是 MMU 通知器的跳过可能会破坏 pfncache 重试协议。Sean Christopherson 提到，为了使该补丁生效，需要对 gfn_to_pfn_cache 代码进行修改，以便能够直接从 guest_memfd 中提取数据。

在本周的新讨论中，Ackerley Tng 和 Sean Christopherson 进行了进一步的技术交流，确认了在页面转换过程中，尽管会调用 MMU 通知器，但并不会导致实际的双重解除映射问题。Ackerley 询问是否存在 MMU 通知器无效化与转换之间的使用后释放问题，Sean 确认没有此类问题。

总体来看，讨论逐渐趋于积极，参与者对补丁的技术细节进行了深入探讨，并确认了其可行性。

#### 📝 邮件列表

1. **[06-15 16:52]** [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[06-15 16:09]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: sashiko-bot@kernel.org
3. **[06-15 10:47]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[06-17 14:07]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
5. **[06-17 14:21]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[06-23 16:41]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Ackerley Tng <ackerleytng@google.com>
7. **[06-24 10:32]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 2: [RFC PATCH] KVM: arm64: Set irqfd->producer to enable vLPI routing updates

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 23 Jun 2026 16:14:33 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的补丁，主题为“设置 irqfd->producer 以启用 vLPI 路由更新”。该补丁的目的是解决 ARM64 的 `kvm_arch_irq_bypass_add_producer()` 函数未设置 `irqfd->producer` 的问题，导致 `kvm_irq_routing_update()` 无法调用 ARM64 路由钩子，从而影响 vLPI 的路由更新。

在历史讨论中，补丁的提出者 leixiang 指出，ARM64 的实现与 x86 和 PowerPC 的处理方式不同，导致在路由更新时未能正确处理 vLPI 的解绑。补丁建议在 `kvm_vgic_v4_set_forwarding()` 成功后设置 `irqfd->producer`，并在删除生产者时清除该指针，以确保在锁保护下进行操作。

本周的新讨论中，参与者对补丁进行了评审，指出了几个潜在问题，包括在删除生产者时未清除 `irqfd->producer` 可能导致悬空指针和并发更新问题。同时，Marc Zyngier 提出了对用户空间控制路由的疑问，认为这可能不符合设计初衷。最终，leixiang 认识到该补丁的实现可能会导致更糟糕的情况，决定放弃该补丁的进一步开发。

#### 📝 邮件列表

1. **[06-23 16:14]** [RFC PATCH] KVM: arm64: Set irqfd->producer to enable vLPI routing updates
   - 发件人: leixiang <leixiang@kylinos.cn>
2. **[06-23 08:30]** Re: [RFC PATCH] KVM: arm64: Set irqfd->producer to enable vLPI
 routing updates
   - 发件人: sashiko-bot@kernel.org
3. **[06-23 10:52]** Re: [RFC PATCH] KVM: arm64: Set irqfd->producer to enable vLPI routing updates
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-23 18:26]** Re: [RFC PATCH] KVM: arm64: Set irqfd->producer to enable vLPI routing updates
   - 发件人: leixiang <leixiang@kylinos.cn>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.2, take #1

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 26 Jun 2026 14:35:26 +0100

#### 🤖 AI 总结

本邮件主题为“[GIT PULL] KVM/arm64 fixes for 7.2, take #1”，主要讨论了针对 KVM/arm64 的一系列修复补丁。Marc Zyngier 提到，这些修复补丁中有一些是相对简单的（如 PSTATE.IL 相关），但也有一些较为复杂的问题（如 vgic 和 MOPS），这些都是稳定版本所需的修复。

在历史讨论中，未提及具体的补丁或问题背景，因此本周的讨论成为主要焦点。Marc 提到，Fuad 自愿成为官方审阅者，这对于缓解他和 Oliver 的工作压力非常重要。他期待下周能继续提交类似的修复补丁，因为相关问题仍在不断增加。

本周的新进展包括一系列具体的修复内容，例如修复了在从受保护的虚拟机回收页面时的会计错误，解决了在注入合成异常时的一些架构合规性问题，以及处理了与 LPI 迁移和禁用相关的竞争条件等。此外，Marc 还提到了一些关于异常返回位置错误的严重问题的修复。

总的来说，本周的讨论集中在 KVM/arm64 的重要修复上，并且引入了新的审阅者以增强补丁的审核过程。

#### 📝 邮件列表

1. **[06-26 14:35]** [GIT PULL] KVM/arm64 fixes for 7.2, take #1
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Discussion

共 3 个 thread

---

### Thread 1: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 26 Jun 2026 10:48:05 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于在 `ktime_get_snapshot_id()` 函数中添加对 `CLOCK_AUX` 的支持的补丁（patch 09/24）。该补丁旨在改进时间管理，特别是针对辅助时钟（AUX clocks）的处理。

在历史讨论中，参与者探讨了如何正确计算与 AUX 时钟相关的 `MONORAW` 值。Thomas Gleixner 提到，当前实现可能导致错误，因为 `monoraw` 应基于 `tk_core` 进行计算，而不是 `tkd`。他建议在 7.2 版本中撤回该补丁，并在 7.3 版本中提交修复版本。

本周的新讨论中，Thomas Weißschuh 和其他参与者对补丁进行了深入分析。Thomas Gleixner 认为当前代码从 PTP 和引导的角度是正确的，但也提出了文档中对 `CLOCK_MONOTONIC_RAW` 的描述需要清理。David Woodhouse 则质疑在实际应用中是否会遇到问题，认为由于调用者主要关心系统时间，因此 AUX 时钟的 `monoraw` 问题在实际中可能并不重要。此外，参与者们讨论了如何在文档中更清晰地表达 AUX 时钟与系统时间之间的关系。

总体来看，本周的讨论集中在补丁的正确性、实际影响及文档清晰度上，参与者们达成了一定的共识，但仍需进一步的修正和清理工作。

#### 📝 邮件列表

1. **[06-26 10:48]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
2. **[06-26 12:49]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[06-26 11:51]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
4. **[06-26 13:03]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
5. **[06-26 17:17]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>

---

### Thread 2: [patch V2 18/25] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 22 Jun 2026 09:55:26 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于一个补丁（patch V2 18/25），旨在为任意时钟 ID 准备跨时间戳功能。该补丁的核心内容是扩展 `ktime_get_snapshot_id()` 函数，使其支持 `CLOCK_BOOTTIME` 和 `CLOCK_MONOTONIC_RAW`，以便在时间管理中提供更灵活的时间戳处理。

在之前的讨论中，参与者们探讨了补丁的实现细节，特别是如何确保不同时间戳类型之间的一致性。David Woodhouse 提到，`CLOCK_BOOTTIME` 的支持主要是针对 ARM64 超级跟踪的需求，而 `CLOCK_MONOTONIC_RAW` 则与 PTP 扩展 IOCTL 相关，但在实际应用中似乎并没有显著的价值。

在本周的新讨论中，Thomas Gleixner 和 David Woodhouse 继续探讨了这两个时钟类型的支持是否有必要。Thomas 表达了对一致性的关注，但同时也表示对其实际需求并没有强烈的看法。整体来看，讨论的焦点在于如何在不同的时间戳支持之间保持一致性，而对补丁的实际必要性仍存在分歧。

#### 📝 邮件列表

1. **[06-22 09:55]** Re: [patch V2 18/25] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[06-22 13:07]** Re: [patch V2 18/25] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[06-22 13:34]** Re: [patch V2 18/25] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 3: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to
 match Linux kernel

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 26 Jun 2026 09:37:01 -0500

#### 🤖 AI 总结

本邮件讨论的主题是关于对 KVM 单元测试中的 arm64 架构的 ESR_ELx 定义进行更新，以使其与 Linux 内核保持一致。原始的 patch 提出了这一更新，目的是确保 KVM 单元测试中的定义与 Linux 内核中的定义相匹配，从而提高兼容性和准确性。

在之前的讨论中，虽然没有详细记录，但可以推测出参与者们关注了 ESR_ELx_FSC 的命名和定义的一致性问题，这对于开发和测试过程至关重要。

在本周的新讨论中，Andrew Jones 提到他已经修复了 ESR_ELx_FSC 的命名问题，并将其合并到相关的代码库中。他确认了这一更改已经应用，并表示感谢。这表明该 patch 已经顺利完成并被合并，标志着讨论的积极进展。

#### 📝 邮件列表

1. **[06-26 09:37]** Re: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to
 match Linux kernel
   - 发件人: Andrew Jones <andrew.jones@linux.dev>
2. **[06-26 09:50]** Re: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to
 match Linux kernel
   - 发件人: Andrew Jones <andrew.jones@linux.dev>

---

## 📌 Other

共 2 个 thread

---

### Thread 1: Sashiko review emails to the list

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 19 Jun 2026 15:19:05 +0100

#### 🤖 AI 总结

本邮件线程讨论了 Sashiko 这一工具在 Linux 内核开发中的应用及其邮件反馈机制。最初，Fuad Tabba 提出了 Sashiko 在发现代码中的真实错误方面的有效性，但也指出其发送的邮件数量过多，导致信噪比不理想。Oliver Upton 和 Roman Gushchin 也参与讨论，认为需要改进 Sashiko 的反馈质量，尤其是减少 ARM 架构相关的误报。

在本周的新讨论中，Fuad 提到他提交的 PR 将显著减少 ARM 相关的误报，并鼓励大家反馈任何重复出现的问题。Oliver 表达了对现有问题汇总的需求，希望能有一个集中查看所有已知错误的方式，以避免遗漏。Roman 则表示他正在开发相关功能，预计不久后会推出。

总体来看，讨论集中在如何提高 Sashiko 的反馈质量和实用性，以及如何更有效地管理和跟踪已知问题上。

#### 📝 邮件列表

1. **[06-19 15:19]** Sashiko review emails to the list
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[06-19 09:45]** Re: Sashiko review emails to the list
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-19 11:05]** Re: Sashiko review emails to the list
   - 发件人: Roman Gushchin <roman.gushchin@linux.dev>
4. **[06-21 12:03]** Re: Sashiko review emails to the list
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-22 10:28]** Re: Sashiko review emails to the list
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[06-22 09:53]** Re: Sashiko review emails to the list
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[06-22 12:20]** Re: Sashiko review emails to the list
   - 发件人: Roman Gushchin <roman.gushchin@linux.dev>
8. **[06-22 17:21]** Re: Sashiko review emails to the list
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 2: [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in ACPI initialization

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 19 Jun 2026 00:25:04 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 ARM64 的 ACPI 初始化过程中设置 `is_pl011_uart` 标志的补丁（PATCH v2）。该补丁的目的是解决在通过 ACPI 启动时，控制台 UART 初始化时未正确设置该标志的问题，导致 `__getchar()` 函数错误地将 UART 视为 16550A 设备，从而在使用 PL011 UART 的系统上出现挂起现象。

在历史讨论中，Colton Lewis 提出了该补丁，指出由于未设置 `is_pl011_uart`，导致依赖串行输入的测试（如 `its-migration`）会无限期挂起。补丁更新了 `uart0_init_acpi()` 函数，以检查 SPCR 接口类型并相应地设置 `is_pl011_uart`。

在本周的新讨论中，Andrew Jones 提到已将该补丁合并，并在提交记录中添加了修复信息，确保了补丁的有效性和可追溯性。整体来看，该补丁的合并将改善 ARM64 系统在 ACPI 启动时的串行输入处理，避免了潜在的挂起问题。

#### 📝 邮件列表

1. **[06-19 00:25]** [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in ACPI initialization
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[06-22 11:42]** Re: [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in
 ACPI initialization
   - 发件人: Andrew Jones <andrew.jones@linux.dev>
3. **[06-26 09:51]** Re: [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in
 ACPI initialization
   - 发件人: Andrew Jones <andrew.jones@linux.dev>

---

