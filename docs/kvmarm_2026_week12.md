# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-03-23 00:33:44

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 470
- **总 Thread 数**: 36
- **大型 Thread** (>20封): 6 个

### 分类分布

- **PATCH**: 30 threads (442 邮件)
- **RFC**: 1 threads (13 邮件)
- **Question**: 1 threads (3 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Discussion**: 1 threads (2 邮件)
- **Other**: 2 threads (9 邮件)

---

## 📌 PATCH

共 30 个 thread

---

### Thread 1: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 100 | **👥 参与者**: 6 | **📅 开始时间**: Wed, 18 Mar 2026 15:53:24 +0000

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v13 00/48] arm64: 支持 KVM 中的 Arm CCA”，主要围绕在 KVM 中实现 Arm 保密计算架构（CCA）的支持。以下是讨论的总结：

1. **原始 Patch/问题的内容**：
   本系列补丁旨在为 KVM 添加对 Arm CCA 的支持，允许在 KVM 中运行受保护的虚拟机。补丁涉及多个方面，包括 RMM v2.0 的支持、内存管理、寄存器访问等。

2. **之前讨论的要点**：
   历史讨论中提到，RMM v2.0 引入了一些新的特性和 API，简化了与主机的页面大小配置，并改进了对中断和内存管理的处理。此外，补丁还包括对状态 RMI 操作（SRO）的初步支持，允许在操作过程中动态分配内存。

3. **本周的新讨论、进展或结论**：
   - 本周的讨论集中在补丁的细节和实现上，包括如何处理 RMM 的不同状态、如何在虚拟机中管理内存和寄存器访问等。
   - 参与者讨论了如何在 KVM 中实现对 RMM 的支持，包括对寄存器的访问限制、如何处理 MMIO 操作、如何在虚拟机中管理定时器等。
   - 还讨论了如何在用户空间和 KVM 之间传递 PSCI 调用的信息，以及如何处理 RMM 的状态变化。
   - 最后，补丁的各个部分经过审查，参与者提出了改进建议，确保补丁的功能和代码质量。

整体而言，此次讨论为 KVM 中实现 Arm CCA 的支持奠定了基础，涵盖了多个技术细节和实现挑战。

#### 📝 邮件列表

1. **[03-18 15:53]** [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[03-18 15:53]** [PATCH v13 01/48] kvm: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Steven Price <steven.price@arm.com>
3. **[03-18 15:53]** [PATCH v13 02/48] kvm: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Steven Price <steven.price@arm.com>
4. **[03-18 15:53]** [PATCH v13 03/48] arm64: RME: Handle Granule Protection Faults (GPFs)
   - 发件人: Steven Price <steven.price@arm.com>
5. **[03-18 15:53]** [PATCH v13 04/48] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Steven Price <steven.price@arm.com>
6. **[03-18 15:53]** [PATCH v13 05/48] arm64: RMI: Temporarily add SMCs from RMM v1.0 spec
   - 发件人: Steven Price <steven.price@arm.com>
7. **[03-18 15:53]** [PATCH v13 06/48] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
8. **[03-18 15:53]** [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
9. **[03-18 15:53]** [PATCH v13 08/48] arm64: RMI: Configure the RMM with the host's page size
   - 发件人: Steven Price <steven.price@arm.com>
10. **[03-18 15:53]** [PATCH v13 09/48] arm64: RMI: Check for LPA2 support
   - 发件人: Steven Price <steven.price@arm.com>
11. **[03-18 15:53]** [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Steven Price <steven.price@arm.com>
12. **[03-18 15:53]** [PATCH v13 11/48] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
13. **[03-18 15:53]** [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Steven Price <steven.price@arm.com>
14. **[03-18 15:53]** [PATCH v13 13/48] kvm: arm64: Don't expose unsupported capabilities for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
15. **[03-18 15:53]** [PATCH v13 14/48] KVM: arm64: Allow passing machine type in KVM creation
   - 发件人: Steven Price <steven.price@arm.com>
16. **[03-18 15:53]** [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
17. **[03-18 15:53]** [PATCH v13 16/48] arm64: RMI: Activate realm on first VCPU run
   - 发件人: Steven Price <steven.price@arm.com>
18. **[03-18 15:53]** [PATCH v13 17/48] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
19. **[03-18 15:53]** [PATCH v13 18/48] arm64: RMI: Support for the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
20. **[03-18 15:53]** [PATCH v13 19/48] KVM: arm64: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
21. **[03-18 15:53]** [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
22. **[03-18 15:53]** [PATCH v13 21/48] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>
23. **[03-18 15:53]** [PATCH v13 22/48] KVM: arm64: Handle realm MMIO emulation
   - 发件人: Steven Price <steven.price@arm.com>
24. **[03-18 15:53]** [PATCH v13 23/48] KVM: arm64: Expose support for private memory
   - 发件人: Steven Price <steven.price@arm.com>
25. **[03-18 15:53]** [PATCH v13 24/48] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
26. **[03-18 15:53]** [PATCH v13 25/48] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Steven Price <steven.price@arm.com>
27. **[03-18 15:53]** [PATCH v13 26/48] arm64: RMI: Create the realm descriptor
   - 发件人: Steven Price <steven.price@arm.com>
28. **[03-18 15:53]** [PATCH v13 27/48] arm64: RMI: Runtime faulting of memory
   - 发件人: Steven Price <steven.price@arm.com>
29. **[03-18 15:53]** [PATCH v13 28/48] KVM: arm64: Handle realm VCPU load
   - 发件人: Steven Price <steven.price@arm.com>
30. **[03-18 15:53]** [PATCH v13 29/48] KVM: arm64: Validate register access for a Realm VM
   - 发件人: Steven Price <steven.price@arm.com>
31. **[03-18 15:53]** [PATCH v13 30/48] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Steven Price <steven.price@arm.com>
32. **[03-18 15:53]** [PATCH v13 31/48] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
33. **[03-18 15:53]** [PATCH v13 32/48] arm64: Don't expose stolen time for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
34. **[03-18 15:53]** [PATCH v13 33/48] arm64: RMI: allow userspace to inject aborts
   - 发件人: Steven Price <steven.price@arm.com>
35. **[03-18 15:53]** [PATCH v13 34/48] arm64: RMI: support RSI_HOST_CALL
   - 发件人: Steven Price <steven.price@arm.com>
36. **[03-18 15:53]** [PATCH v13 35/48] arm64: RMI: Allow checking SVE on VM instance
   - 发件人: Steven Price <steven.price@arm.com>
37. **[03-18 15:54]** [PATCH v13 36/48] arm64: RMI: Always use 4k pages for realms
   - 发件人: Steven Price <steven.price@arm.com>
38. **[03-18 15:54]** [PATCH v13 37/48] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Steven Price <steven.price@arm.com>
39. **[03-18 15:54]** [PATCH v13 38/48] arm64: RMI: Enable PMU support with a realm guest
   - 发件人: Steven Price <steven.price@arm.com>
40. **[03-18 15:54]** [PATCH v13 39/48] arm64: RMI: Propagate number of breakpoints and watchpoints to userspace
   - 发件人: Steven Price <steven.price@arm.com>
41. **[03-18 15:54]** [PATCH v13 40/48] arm64: RMI: Set breakpoint parameters through SET_ONE_REG
   - 发件人: Steven Price <steven.price@arm.com>
42. **[03-18 15:54]** [PATCH v13 41/48] arm64: RMI: Initialize PMCR.N with number counter supported by RMM
   - 发件人: Steven Price <steven.price@arm.com>
43. **[03-18 15:54]** [PATCH v13 42/48] arm64: RMI: Propagate max SVE vector length from RMM
   - 发件人: Steven Price <steven.price@arm.com>
44. **[03-18 15:54]** [PATCH v13 43/48] arm64: RMI: Configure max SVE vector length for a Realm
   - 发件人: Steven Price <steven.price@arm.com>
45. **[03-18 15:54]** [PATCH v13 44/48] arm64: RMI: Provide register list for unfinalized RMI RECs
   - 发件人: Steven Price <steven.price@arm.com>
46. **[03-18 15:54]** [PATCH v13 45/48] arm64: RMI: Provide accurate register list
   - 发件人: Steven Price <steven.price@arm.com>
47. **[03-18 15:54]** [PATCH v13 46/48] KVM: arm64: Expose KVM_ARM_VCPU_REC to user space
   - 发件人: Steven Price <steven.price@arm.com>
48. **[03-18 15:54]** [PATCH v13 47/48] arm64: RMI: Enable realms to be created
   - 发件人: Steven Price <steven.price@arm.com>
49. **[03-18 15:54]** [PATCH v13 48/48] [WIP] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
50. **[03-18 16:07]** Re: [PATCH v13 04/48] arm64: RMI: Add SMC definitions for calling
 the RMM
   - 发件人: Joey Gouly <joey.gouly@arm.com>
51. **[03-18 16:53]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
52. **[03-18 17:07]** Re: [PATCH v13 04/48] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Steven Price <steven.price@arm.com>
53. **[03-19 10:24]** Re: [PATCH v13 36/48] arm64: RMI: Always use 4k pages for realms
   - 发件人: Joey Gouly <joey.gouly@arm.com>
54. **[03-19 10:27]** Re: [PATCH v13 37/48] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Joey Gouly <joey.gouly@arm.com>
55. **[03-19 10:31]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
56. **[03-19 10:38]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
57. **[03-19 10:41]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
58. **[03-19 12:47]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
59. **[03-19 14:09]** Re: [PATCH v13 13/48] kvm: arm64: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
60. **[03-19 15:20]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Steven Price <steven.price@arm.com>
61. **[03-19 15:25]** Re: [PATCH v13 13/48] kvm: arm64: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
62. **[03-19 16:02]** Re: [PATCH v13 36/48] arm64: RMI: Always use 4k pages for realms
   - 发件人: Steven Price <steven.price@arm.com>
63. **[03-19 16:11]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating
 a realm.
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
64. **[03-19 16:17]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
65. **[03-19 16:24]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating a
 realm.
   - 发件人: Steven Price <steven.price@arm.com>
66. **[03-19 16:42]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
67. **[03-19 17:17]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating
 a realm.
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
68. **[03-19 17:35]** Re: [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
69. **[03-19 17:36]** Re: [PATCH v13 46/48] KVM: arm64: Expose KVM_ARM_VCPU_REC to user
 space
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
70. **[03-19 18:05]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
71. **[03-19 18:10]** Re: [PATCH v13 17/48] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
72. **[03-19 18:25]** Re: [PATCH v13 26/48] arm64: RMI: Create the realm descriptor
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
73. **[03-19 18:41]** Re: [PATCH v13 27/48] arm64: RMI: Runtime faulting of memory
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
74. **[03-19 18:46]** Re: [PATCH v13 37/48] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
75. **[03-19 18:50]** Re: [PATCH v13 39/48] arm64: RMI: Propagate number of breakpoints
 and watchpoints to userspace
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
76. **[03-19 18:53]** Re: [PATCH v13 45/48] arm64: RMI: Provide accurate register list
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
77. **[03-19 19:01]** Re: [PATCH v13 23/48] KVM: arm64: Expose support for private memory
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
78. **[03-19 17:02]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
79. **[03-20 10:37]** Re: [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
80. **[03-20 11:15]** Re: [PATCH v13 21/48] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
81. **[03-20 14:08]** Re: [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
82. **[03-20 16:01]** Re: [PATCH v13 07/48] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
83. **[03-20 16:07]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating a
 realm.
   - 发件人: Steven Price <steven.price@arm.com>
84. **[03-20 16:12]** Re: [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
85. **[03-20 16:14]** Re: [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
86. **[03-20 16:26]** Re: [PATCH v13 17/48] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
87. **[03-20 16:32]** Re: [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
88. **[03-20 16:39]** Re: [PATCH v13 23/48] KVM: arm64: Expose support for private memory
   - 发件人: Steven Price <steven.price@arm.com>
89. **[03-20 16:41]** Re: [PATCH v13 26/48] arm64: RMI: Create the realm descriptor
   - 发件人: Steven Price <steven.price@arm.com>
90. **[03-20 16:44]** Re: [PATCH v13 27/48] arm64: RMI: Runtime faulting of memory
   - 发件人: Steven Price <steven.price@arm.com>
91. **[03-20 16:45]** Re: [PATCH v13 37/48] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Steven Price <steven.price@arm.com>
92. **[03-20 16:45]** Re: [PATCH v13 39/48] arm64: RMI: Propagate number of breakpoints and
 watchpoints to userspace
   - 发件人: Steven Price <steven.price@arm.com>
93. **[03-20 16:45]** Re: [PATCH v13 45/48] arm64: RMI: Provide accurate register list
   - 发件人: Steven Price <steven.price@arm.com>
94. **[03-20 16:45]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
95. **[03-20 13:15]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
96. **[03-21 13:04]** Re: [PATCH v13 15/48] arm64: RMI: RTT tear down
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
97. **[03-21 13:21]** Re: [PATCH v13 05/48] arm64: RMI: Temporarily add SMCs from RMM v1.0 spec
   - 发件人: Marc Zyngier <maz@kernel.org>
98. **[03-21 16:20]** Re: [PATCH v13 26/48] arm64: RMI: Create the realm descriptor
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
99. **[03-21 16:23]** Re: [PATCH v13 37/48] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
100. **[03-21 16:34]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating
 a realm.
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 2: [PATCH v6 00/39] KVM: arm64: Introduce vGIC-v5 with PPI support

**📧 邮件数**: 61 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 17 Mar 2026 11:39:57 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下支持虚拟 GICv5（Generic Interrupt Controller v5）的相关补丁和进展。

1. **原始补丁内容**：
   本次补丁系列的核心是引入对 GICv5 的支持，特别是 PPI（Private Peripheral Interrupt）的处理。补丁系列的目标是使 KVM 能够在 ARM64 系统上支持 GICv5，包括对 PPI 的管理和中断注入。

2. **历史讨论要点**：
   之前的讨论主要集中在 GICv5 的实现细节上，包括如何处理 PPI 的状态、优先级以及如何在虚拟机中正确注入中断。参与者们讨论了 GICv5 与 GICv3 的不同之处，以及如何确保在 GICv5 环境下的兼容性和性能优化。

3. **本周的新讨论与进展**：
   - 本周的讨论中，补丁系列中的多个功能得到了实现和完善，包括 PPI 的直接注入、状态保存与恢复、以及对 GICv5 特性的文档更新。
   - 参与者们还讨论了如何在不支持 GICv5 的保护虚拟机中隐藏相关特性，确保系统的稳定性。
   - 新增的自测试用例确保了 GICv5 的基本功能正常，并验证了用户空间对 PPI 的驱动能力。
   - 讨论中提到的代码优化和结构调整，旨在提高代码的可读性和执行效率。

总体而言，本周的讨论和补丁更新显著推进了 KVM 在 ARM64 平台上对 GICv5 的支持，为未来的虚拟化工作奠定了基础。

#### 📝 邮件列表

1. **[03-17 11:39]** [PATCH v6 00/39] KVM: arm64: Introduce vGIC-v5 with PPI support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[03-17 11:40]** [PATCH v6 01/39] KVM: arm64: vgic-v3: Drop userspace write
 sanitization for ID_AA64PFR0.GIC on GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[03-17 11:40]** [PATCH v6 02/39] KVM: arm64: vgic: Rework vgic_is_v3() and add
 vgic_host_has_gicvX()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[03-17 11:40]** [PATCH v6 03/39] KVM: arm64: Return early from
 kvm_finalize_sys_regs() if guest has run
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[03-17 11:40]** [PATCH v6 04/39] KVM: arm64: vgic: Split out mapping IRQs and setting
 irq_ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[03-17 11:41]** [PATCH v6 05/39] arm64/sysreg: Add remaining GICv5 ICC_ & ICH_
 sysregs for KVM support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[03-17 11:41]** [PATCH v6 06/39] arm64/sysreg: Add GICR CDNMIA encoding
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[03-17 11:41]** [PATCH v6 07/39] KVM: arm64: gic-v5: Add ARM_VGIC_V5 device to KVM
 headers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[03-17 11:42]** [PATCH v6 08/39] KVM: arm64: gic: Introduce interrupt type helpers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[03-17 11:42]** [PATCH v6 09/39] KVM: arm64: gic-v5: Add Arm copyright header
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[03-17 11:42]** [PATCH v6 10/39] KVM: arm64: gic-v5: Detect implemented PPIs on boot
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[03-17 11:42]** [PATCH v6 11/39] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[03-17 11:43]** [PATCH v6 12/39] KVM: arm64: gic-v5: Support GICv5 FGTs & FGUs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[03-17 11:43]** [PATCH v6 13/39] KVM: arm64: gic-v5: Add emulation for
 ICC_IAFFIDR_EL1 accesses
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[03-17 11:43]** [PATCH v6 14/39] KVM: arm64: gic-v5: Trap and emulate ICC_IDR0_EL1
 accesses
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[03-17 11:43]** [PATCH v6 15/39] KVM: arm64: gic-v5: Add vgic-v5 save/restore hyp
 interface
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[03-17 11:44]** [PATCH v6 16/39] KVM: arm64: gic-v5: Implement GICv5 load/put and
 save/restore
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[03-17 11:44]** [PATCH v6 17/39] KVM: arm64: gic-v5: Finalize GICv5 PPIs and generate
 mask
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[03-17 11:44]** [PATCH v6 18/39] KVM: arm64: gic: Introduce queue_irq_unlock to
 irq_ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[03-17 11:44]** [PATCH v6 19/39] KVM: arm64: gic-v5: Implement PPI interrupt
 injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[03-17 11:45]** [PATCH v6 20/39] KVM: arm64: gic-v5: Init Private IRQs (PPIs) for
 GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[03-17 11:45]** [PATCH v6 21/39] KVM: arm64: gic-v5: Clear TWI if single task running
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[03-17 11:45]** [PATCH v6 22/39] KVM: arm64: gic-v5: Check for pending PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[03-17 11:45]** [PATCH v6 23/39] KVM: arm64: gic-v5: Trap and mask guest
 ICC_PPI_ENABLERx_EL1 writes
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[03-17 11:46]** [PATCH v6 24/39] KVM: arm64: Introduce set_direct_injection irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[03-17 11:46]** [PATCH v6 25/39] KVM: arm64: gic-v5: Implement direct injection of
 PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[03-17 11:46]** [PATCH v6 26/39] KVM: arm64: gic-v5: Support GICv5 interrupts with
 KVM_IRQ_LINE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[03-17 11:46]** [PATCH v6 27/39] KVM: arm64: gic-v5: Create and initialise vgic_v5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[03-17 11:47]** [PATCH v6 28/39] KVM: arm64: gic-v5: Initialise ID and priority bits
 when resetting vcpu
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[03-17 11:47]** [PATCH v6 29/39] KVM: arm64: gic-v5: Enlighten arch timer for GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[03-17 11:47]** [PATCH v6 30/39] KVM: arm64: gic-v5: Mandate architected PPI for PMU
 emulation on GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[03-17 11:48]** [PATCH v6 31/39] KVM: arm64: gic: Hide GICv5 for protected guests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[03-17 11:48]** [PATCH v6 32/39] KVM: arm64: gic-v5: Hide FEAT_GCIE from NV GICv5
 guests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[03-17 11:48]** [PATCH v6 33/39] KVM: arm64: gic-v5: Introduce kvm_arm_vgic_v5_ops
 and register them
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[03-17 11:48]** [PATCH v6 34/39] KVM: arm64: gic-v5: Set ICH_VCTLR_EL2.En on boot
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[03-17 11:49]** [PATCH v6 35/39] KVM: arm64: gic-v5: Probe for GICv5 device
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[03-17 11:49]** [PATCH v6 36/39] Documentation: KVM: Introduce documentation for
 VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[03-17 11:49]** [PATCH v6 37/39] KVM: arm64: gic-v5: Communicate userspace-driveable
 PPIs via a UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[03-17 11:49]** [PATCH v6 38/39] KVM: arm64: selftests: Introduce a minimal GICv5 PPI
 selftest
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[03-17 11:50]** [PATCH v6 39/39] KVM: arm64: selftests: Add no-vgic-v5 selftest
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[03-17 16:00]** Re: [PATCH v6 04/39] KVM: arm64: vgic: Split out mapping IRQs and setting irq_ops
   - 发件人: Marc Zyngier <maz@kernel.org>
42. **[03-17 16:31]** Re: [PATCH v6 19/39] KVM: arm64: gic-v5: Implement PPI interrupt injection
   - 发件人: Marc Zyngier <maz@kernel.org>
43. **[03-17 16:42]** Re: [PATCH v6 20/39] KVM: arm64: gic-v5: Init Private IRQs (PPIs) for GICv5
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[03-17 17:08]** Re: [PATCH v6 22/39] KVM: arm64: gic-v5: Check for pending PPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[03-17 18:05]** Re: [PATCH v6 29/39] KVM: arm64: gic-v5: Enlighten arch timer for GICv5
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[03-18 15:34]** Re: [PATCH v6 35/39] KVM: arm64: gic-v5: Probe for GICv5 device
   - 发件人: Joey Gouly <joey.gouly@arm.com>
47. **[03-18 17:30]** Re: [PATCH v6 04/39] KVM: arm64: vgic: Split out mapping IRQs and
 setting irq_ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
48. **[03-18 17:31]** Re: [PATCH v6 19/39] KVM: arm64: gic-v5: Implement PPI interrupt
 injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
49. **[03-18 17:34]** Re: [PATCH v6 20/39] KVM: arm64: gic-v5: Init Private IRQs (PPIs) for
 GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
50. **[03-19 08:27]** Re: [PATCH v6 22/39] KVM: arm64: gic-v5: Check for pending PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
51. **[03-19 08:36]** Re: [PATCH v6 35/39] KVM: arm64: gic-v5: Probe for GICv5 device
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
52. **[03-19 08:59]** Re: [PATCH v6 29/39] KVM: arm64: gic-v5: Enlighten arch timer for
 GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
53. **[03-19 10:02]** Re: [PATCH v6 01/39] KVM: arm64: vgic-v3: Drop userspace write
 sanitization for ID_AA64PFR0.GIC on GICv5
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
54. **[03-19 10:12]** Re: [PATCH v6 03/39] KVM: arm64: Return early from
 kvm_finalize_sys_regs() if guest has run
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
55. **[03-19 10:31]** Re: [PATCH v6 11/39] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
56. **[03-19 10:34]** Re: [PATCH v6 13/39] KVM: arm64: gic-v5: Add emulation for
 ICC_IAFFIDR_EL1 accesses
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
57. **[03-19 10:38]** Re: [PATCH v6 14/39] KVM: arm64: gic-v5: Trap and emulate
 ICC_IDR0_EL1 accesses
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
58. **[03-19 11:35]** Re: [PATCH v6 01/39] KVM: arm64: vgic-v3: Drop userspace write
 sanitization for ID_AA64PFR0.GIC on GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
59. **[03-19 11:41]** Re: [PATCH v6 03/39] KVM: arm64: Return early from
 kvm_finalize_sys_regs() if guest has run
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
60. **[03-19 14:02]** Re: [PATCH v6 11/39] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
61. **[03-20 10:27]** Re: [PATCH v6 01/39] KVM: arm64: vgic-v3: Drop userspace write
 sanitization for ID_AA64PFR0.GIC on GICv5
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>

---

### Thread 3: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework

**📧 邮件数**: 47 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 16 Mar 2026 17:54:33 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上对 `user_mem_abort()` 函数的重构工作，Marc Zyngier 提出了一个包含 17 个补丁的系列更新。

1. **原始补丁/问题内容**：
   该系列补丁的目标是对 `user_mem_abort()` 函数进行重构，以提高代码的可读性和可维护性。补丁包括将函数拆分为更小的、易于管理的部分，减少函数之间的状态共享，增强代码的结构化。

2. **之前讨论要点**：
   在此之前，Fuad Tabba 提出的补丁集已经开始了类似的重构工作。Marc 在此基础上进行了进一步的改进，增加了对状态的上下文化处理，并引入了新的结构体以简化参数传递。

3. **本周的新讨论、进展或结论**：
   本周的讨论集中在补丁的具体实现上，Marc 提出了多个补丁，逐步去除冗余的状态变量，简化了权限处理逻辑，并将 VMA 相关信息移至新的结构体 `kvm_s2_fault_vma_info` 中。Fuad 对这些补丁给予了积极的反馈，并表示将开始详细审查。多个补丁已经获得了审阅通过，显示出社区对这一重构工作的认可。

总的来说，这一系列补丁旨在通过重构和清理代码来提升 KVM 的可维护性和性能，社区成员对此表示支持并积极参与讨论。

#### 📝 邮件列表

1. **[03-16 17:54]** [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-16 17:54]** [PATCH 01/17] KVM: arm64: Kill fault->ipa
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-16 17:54]** [PATCH 02/17] KVM: arm64: Make fault_ipa immutable
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-16 17:54]** [PATCH 03/17] KVM: arm64: Move fault context to const structure
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-16 17:54]** [PATCH 04/17] KVM: arm64: Replace fault_is_perm with a helper
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-16 17:54]** [PATCH 05/17] KVM: arm64: Constrain fault_granule to kvm_s2_fault_map()
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-16 17:54]** [PATCH 06/17] KVM: arm64: Kill write_fault from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-16 17:54]** [PATCH 07/17] KVM: arm64: Kill exec_fault from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-16 17:54]** [PATCH 08/17] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[03-16 17:54]** [PATCH 09/17] KVM: arm64: Move VMA-related information to kvm_s2_fault_vma_info
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[03-16 17:54]** [PATCH 10/17] KVM: arm64: Kill logging_active from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[03-16 17:54]** [PATCH 11/17] KVM: arm64: Restrict the scope of the 'writable' attribute
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[03-16 17:54]** [PATCH 12/17] KVM: arm64: Move kvm_s2_fault.{pfn,page} to kvm_s2_vma_info
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[03-16 17:54]** [PATCH 13/17] KVM: arm64: Replace force_pte with a max_map_size attribute
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[03-16 17:54]** [PATCH 14/17] KVM: arm64: Move device mapping management into kvm_s2_fault_pin_pfn()
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[03-16 17:54]** [PATCH 15/17] KVM: arm64: Directly expose mapping prot and kill kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[03-16 17:54]** [PATCH 16/17] KVM: arm64: Simplify integration of adjust_nested_*_perms()
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[03-16 17:54]** [PATCH 17/17] KVM: arm64: Convert gmem_abort() to struct kvm_s2_fault_desc
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[03-16 19:45]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Fuad Tabba <tabba@google.com>
20. **[03-16 20:26]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Fuad Tabba <tabba@google.com>
21. **[03-16 20:33]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Fuad Tabba <tabba@google.com>
22. **[03-17 08:23]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[03-17 09:22]** Re: [PATCH 01/17] KVM: arm64: Kill fault->ipa
   - 发件人: Fuad Tabba <tabba@google.com>
24. **[03-17 09:38]** Re: [PATCH 02/17] KVM: arm64: Make fault_ipa immutable
   - 发件人: Fuad Tabba <tabba@google.com>
25. **[03-17 10:26]** Re: [PATCH 03/17] KVM: arm64: Move fault context to const structure
   - 发件人: Fuad Tabba <tabba@google.com>
26. **[03-17 10:49]** Re: [PATCH 04/17] KVM: arm64: Replace fault_is_perm with a helper
   - 发件人: Fuad Tabba <tabba@google.com>
27. **[03-17 11:04]** Re: [PATCH 05/17] KVM: arm64: Constrain fault_granule to kvm_s2_fault_map()
   - 发件人: Fuad Tabba <tabba@google.com>
28. **[03-17 11:20]** Re: [PATCH 06/17] KVM: arm64: Kill write_fault from kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>
29. **[03-17 11:44]** Re: [PATCH 07/17] KVM: arm64: Kill exec_fault from kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>
30. **[03-17 12:12]** Re: [PATCH 08/17] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>
31. **[03-17 12:51]** Re: [PATCH 09/17] KVM: arm64: Move VMA-related information to kvm_s2_fault_vma_info
   - 发件人: Fuad Tabba <tabba@google.com>
32. **[03-17 13:23]** Re: [PATCH 10/17] KVM: arm64: Kill logging_active from kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>
33. **[03-17 13:31]** Re: [PATCH 08/17] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
34. **[03-17 13:55]** Re: [PATCH 11/17] KVM: arm64: Restrict the scope of the 'writable' attribute
   - 发件人: Fuad Tabba <tabba@google.com>
35. **[03-17 14:24]** Re: [PATCH 12/17] KVM: arm64: Move kvm_s2_fault.{pfn,page} to kvm_s2_vma_info
   - 发件人: Fuad Tabba <tabba@google.com>
36. **[03-17 15:08]** Re: [PATCH 13/17] KVM: arm64: Replace force_pte with a max_map_size attribute
   - 发件人: Fuad Tabba <tabba@google.com>
37. **[03-17 15:41]** Re: [PATCH 14/17] KVM: arm64: Move device mapping management into kvm_s2_fault_pin_pfn()
   - 发件人: Fuad Tabba <tabba@google.com>
38. **[03-17 16:14]** Re: [PATCH 15/17] KVM: arm64: Directly expose mapping prot and kill kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>
39. **[03-17 16:45]** Re: [PATCH 16/17] KVM: arm64: Simplify integration of adjust_nested_*_perms()
   - 发件人: Fuad Tabba <tabba@google.com>
40. **[03-17 17:03]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
41. **[03-17 17:50]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Fuad Tabba <tabba@google.com>
42. **[03-17 17:58]** Re: [PATCH 17/17] KVM: arm64: Convert gmem_abort() to struct kvm_s2_fault_desc
   - 发件人: Fuad Tabba <tabba@google.com>
43. **[03-17 18:02]** Re: [PATCH 00/17] KVM: arm64: More user_mem_abort() rework
   - 发件人: Fuad Tabba <tabba@google.com>
44. **[03-18 13:43]** Re: [PATCH 04/17] KVM: arm64: Replace fault_is_perm with a helper
   - 发件人: Joey Gouly <joey.gouly@arm.com>
45. **[03-18 14:22]** Re: [PATCH 09/17] KVM: arm64: Move VMA-related information to
 kvm_s2_fault_vma_info
   - 发件人: Joey Gouly <joey.gouly@arm.com>
46. **[03-18 16:14]** Re: [PATCH 09/17] KVM: arm64: Move VMA-related information to kvm_s2_fault_vma_info
   - 发件人: Fuad Tabba <tabba@google.com>
47. **[03-21 09:50]** Re: [PATCH 09/17] KVM: arm64: Move VMA-related information to kvm_s2_fault_vma_info
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 4: [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support

**📧 邮件数**: 44 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 19 Mar 2026 15:49:42 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 vGIC-v5 设备的补丁系列，主要集中在对 ARM64 架构的虚拟化支持上，尤其是 PPI（私有中断）的实现。

1. **原始补丁内容**：补丁系列的目标是引入 vGIC-v5 设备，支持 PPI。初始版本仅支持 PPI，未来将扩展支持 SPI 和 LPI。

2. **历史讨论要点**：之前的讨论中，补丁经历了多个版本的迭代，主要关注如何在 GICv5 主机上实现 PPI 的支持，以及如何处理与 GICv3 的兼容性问题。补丁中提到的关键变化包括 IRQ 操作的重构、对 GICv5 系统寄存器的支持等。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的最终实现上，涉及多个方面的更新：
   - 引入了 PPI 的直接注入机制，允许硬件直接将 PPI 状态注入到虚拟机中。
   - 增加了对 GICv5 的文档支持，明确了用户空间驱动的 PPI 的限制。
   - 提供了自测用例，确保 GICv5 的基本功能正常工作。
   - 讨论了 GICv5 在受保护虚拟机中的隐藏问题，确保不暴露给不支持的虚拟机。

总的来说，这一系列补丁的目标是增强 KVM 对 GICv5 的支持，确保在 ARM64 架构上实现更高效的中断管理和虚拟化功能。

#### 📝 邮件列表

1. **[03-19 15:49]** [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[03-19 15:49]** [PATCH v7 01/41] KVM: arm64: vgic-v3: Drop userspace write
 sanitization for ID_AA64PFR0.GIC on GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[03-19 15:50]** [PATCH v7 02/41] KVM: arm64: vgic: Rework vgic_is_v3() and add
 vgic_host_has_gicvX()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[03-19 15:50]** [PATCH v7 03/41] KVM: arm64: Return early from
 kvm_finalize_sys_regs() if guest has run
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[03-19 15:50]** [PATCH v7 04/41] KVM: arm64: Init vcpu prior to the timers and PMU
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[03-19 15:51]** [PATCH v7 05/41] KVM: arm64: vgic: Split out mapping IRQs and setting
 irq_ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[03-19 15:51]** [PATCH v7 06/41] arm64/sysreg: Add remaining GICv5 ICC_ & ICH_
 sysregs for KVM support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[03-19 15:51]** [PATCH v7 07/41] arm64/sysreg: Add GICR CDNMIA encoding
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[03-19 15:51]** [PATCH v7 08/41] KVM: arm64: gic-v5: Add ARM_VGIC_V5 device to KVM
 headers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[03-19 15:52]** [PATCH v7 09/41] KVM: arm64: gic: Introduce interrupt type helpers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[03-19 15:52]** [PATCH v7 10/41] KVM: arm64: gic-v5: Add Arm copyright header
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[03-19 15:52]** [PATCH v7 11/41] KVM: arm64: gic-v5: Detect implemented PPIs on boot
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[03-19 15:52]** [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[03-19 15:53]** [PATCH v7 13/41] KVM: arm64: gic-v5: Support GICv5 FGTs & FGUs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[03-19 15:53]** [PATCH v7 14/41] KVM: arm64: gic-v5: Add emulation for
 ICC_IAFFIDR_EL1 accesses
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[03-19 15:53]** [PATCH v7 15/41] KVM: arm64: gic-v5: Trap and emulate ICC_IDR0_EL1
 accesses
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[03-19 15:53]** [PATCH v7 16/41] KVM: arm64: gic-v5: Add vgic-v5 save/restore hyp
 interface
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[03-19 15:54]** [PATCH v7 17/41] KVM: arm64: gic-v5: Implement GICv5 load/put and
 save/restore
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[03-19 15:54]** [PATCH v7 18/41] KVM: arm64: gic-v5: Finalize GICv5 PPIs and generate
 mask
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[03-19 15:54]** [PATCH v7 19/41] KVM: arm64: gic: Introduce queue_irq_unlock to
 irq_ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[03-19 15:54]** [PATCH v7 20/41] KVM: arm64: gic-v5: Implement PPI interrupt
 injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[03-19 15:55]** [PATCH v7 21/41] KVM: arm64: gic-v5: Init Private IRQs (PPIs) for
 GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[03-19 15:55]** [PATCH v7 22/41] KVM: arm64: gic-v5: Clear TWI if single task running
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[03-19 15:55]** [PATCH v7 23/41] KVM: arm64: gic-v5: Check for pending PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[03-19 15:55]** [PATCH v7 24/41] KVM: arm64: gic-v5: Trap and mask guest
 ICC_PPI_ENABLERx_EL1 writes
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[03-19 15:56]** [PATCH v7 25/41] KVM: arm64: Introduce set_direct_injection irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[03-19 15:56]** [PATCH v7 26/41] KVM: arm64: gic-v5: Implement direct injection of
 PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[03-19 15:56]** [PATCH v7 27/41] KVM: arm64: gic-v5: Support GICv5 interrupts with
 KVM_IRQ_LINE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[03-19 15:56]** [PATCH v7 28/41] KVM: arm64: gic-v5: Create and initialise vgic_v5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[03-19 15:57]** [PATCH v7 29/41] KVM: arm64: gic-v5: Initialise ID and priority bits
 when resetting vcpu
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[03-19 15:57]** [PATCH v7 30/41] irqchip/gic-v5: Introduce minimal irq_set_type() for
 PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[03-19 15:57]** [PATCH v7 31/41] KVM: arm64: gic-v5: Enlighten arch timer for GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[03-19 15:58]** [PATCH v7 32/41] KVM: arm64: gic-v5: Mandate architected PPI for PMU
 emulation on GICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[03-19 15:58]** [PATCH v7 33/41] KVM: arm64: gic: Hide GICv5 for protected guests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[03-19 15:58]** [PATCH v7 34/41] KVM: arm64: gic-v5: Hide FEAT_GCIE from NV GICv5
 guests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[03-19 15:58]** [PATCH v7 35/41] KVM: arm64: gic-v5: Introduce kvm_arm_vgic_v5_ops
 and register them
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[03-19 15:59]** [PATCH v7 36/41] KVM: arm64: gic-v5: Set ICH_VCTLR_EL2.En on boot
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[03-19 15:59]** [PATCH v7 37/41] KVM: arm64: gic-v5: Probe for GICv5 device
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[03-19 15:59]** [PATCH v7 38/41] Documentation: KVM: Introduce documentation for
 VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[03-19 15:59]** [PATCH v7 39/41] KVM: arm64: gic-v5: Communicate userspace-driveable
 PPIs via a UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[03-19 16:00]** [PATCH v7 40/41] KVM: arm64: selftests: Introduce a minimal GICv5 PPI
 selftest
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
42. **[03-19 16:00]** [PATCH v7 41/41] KVM: arm64: selftests: Add no-vgic-v5 selftest
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
43. **[03-19 18:26]** Re: [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[03-19 18:50]** Re: (subset) [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 5: [PATCH v10 00/30] KVM: arm64: Implement support for SME

**📧 邮件数**: 37 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 06 Mar 2026 17:00:52 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现对 SME（Scalable Matrix Extension）的支持的补丁系列。补丁的主要内容包括更新系统寄存器定义、动态配置 SME 状态、支持 SME 控制寄存器等。

在历史讨论中，Mark Brown 提出了多个补丁，主要关注用户空间 ABI、SVE 和 SME 的寄存器访问、动态配置等方面。补丁系列的目标是确保 KVM 能够有效管理和虚拟化 SME 特性，特别是在处理浮点状态和向量长度配置时。

在本周的新讨论中，参与者对多个补丁进行了审查并给予了反馈。Catalin Marinas 和 Jean-Philippe Brucker 对补丁的具体实现提出了建议和修改意见，包括对 SMIDR 值的处理、寄存器访问宏的重命名、以及对 SME 特性的冗余检查等。整体上，讨论集中在确保补丁的正确性和优化代码结构上。

总结来看，本周的讨论主要是对历史补丁的审查与反馈，未提出新的补丁或重大变更，但通过审查过程，进一步推动了补丁的完善和实现。

#### 📝 邮件列表

1. **[03-06 17:00]** [PATCH v10 00/30] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[03-06 17:00]** [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[03-06 17:00]** [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[03-06 17:00]** [PATCH v10 03/30] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[03-06 17:00]** [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[03-06 17:00]** [PATCH v10 05/30] KVM: arm64: Pay attention to FFR parameter in
 SVE save and load
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[03-06 17:00]** [PATCH v10 06/30] KVM: arm64: Pull ctxt_has_ helpers to start of
 sysreg-sr.h
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[03-06 17:00]** [PATCH v10 07/30] KVM: arm64: Move SVE state access macros after
 feature test macros
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[03-06 17:01]** [PATCH v10 08/30] KVM: arm64: Rename SVE finalization constants to
 be more general
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[03-06 17:01]** [PATCH v10 09/30] KVM: arm64: Define internal features for SME
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[03-06 17:01]** [PATCH v10 10/30] KVM: arm64: Rename sve_state_reg_region
   - 发件人: Mark Brown <broonie@kernel.org>
12. **[03-06 17:01]** [PATCH v10 11/30] KVM: arm64: Store vector lengths in an array
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[03-06 17:01]** [PATCH v10 12/30] KVM: arm64: Factor SVE code out of
 fpsimd_lazy_switch_to_host()
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[03-06 17:01]** [PATCH v10 13/30] KVM: arm64: Document the KVM ABI for SME
   - 发件人: Mark Brown <broonie@kernel.org>
15. **[03-06 17:01]** [PATCH v10 14/30] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[03-06 17:01]** [PATCH v10 15/30] KVM: arm64: Support SME control registers
   - 发件人: Mark Brown <broonie@kernel.org>
17. **[03-06 17:01]** [PATCH v10 16/30] KVM: arm64: Support TPIDR2_EL0
   - 发件人: Mark Brown <broonie@kernel.org>
18. **[03-06 17:01]** [PATCH v10 17/30] KVM: arm64: Support SME identification registers
 for guests
   - 发件人: Mark Brown <broonie@kernel.org>
19. **[03-16 16:34]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
20. **[03-16 17:37]** Re: [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
21. **[03-16 17:42]** Re: [PATCH v10 03/30] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
22. **[03-16 17:44]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
23. **[03-18 17:27]** Re: [PATCH v10 17/30] KVM: arm64: Support SME identification
 registers for guests
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
24. **[03-18 17:29]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
25. **[03-18 17:30]** Re: [PATCH v10 05/30] KVM: arm64: Pay attention to FFR parameter in
 SVE save and load
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
26. **[03-18 17:31]** Re: [PATCH v10 06/30] KVM: arm64: Pull ctxt_has_ helpers to start of
 sysreg-sr.h
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
27. **[03-18 17:32]** Re: [PATCH v10 07/30] KVM: arm64: Move SVE state access macros after
 feature test macros
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
28. **[03-18 17:33]** Re: [PATCH v10 08/30] KVM: arm64: Rename SVE finalization constants
 to be more general
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
29. **[03-18 17:44]** Re: [PATCH v10 09/30] KVM: arm64: Define internal features for SME
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
30. **[03-18 17:46]** Re: [PATCH v10 10/30] KVM: arm64: Rename sve_state_reg_region
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
31. **[03-18 17:48]** Re: [PATCH v10 11/30] KVM: arm64: Store vector lengths in an array
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
32. **[03-18 17:49]** Re: [PATCH v10 12/30] KVM: arm64: Factor SVE code out of
 fpsimd_lazy_switch_to_host()
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
33. **[03-18 17:50]** Re: [PATCH v10 09/30] KVM: arm64: Define internal features for SME
   - 发件人: Mark Brown <broonie@kernel.org>
34. **[03-18 17:51]** Re: [PATCH v10 13/30] KVM: arm64: Document the KVM ABI for SME
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
35. **[03-18 17:53]** Re: [PATCH v10 14/30] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
36. **[03-18 17:54]** Re: [PATCH v10 15/30] KVM: arm64: Support SME control registers
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>
37. **[03-18 17:55]** Re: [PATCH v10 16/30] KVM: arm64: Support TPIDR2_EL0
   - 发件人: Jean-Philippe Brucker <jpb@kernel.org>

---

### Thread 6: [PATCH 00/10] KVM: arm64: Adopt scoped resource management (guard)
 for EL1 and EL2

**📧 邮件数**: 21 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 16 Mar 2026 17:35:21 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下采用范围资源管理（guard）的补丁系列，共包含 10 个补丁。Fuad Tabba 提出了这一系列补丁，旨在通过使用 `<linux/cleanup.h>` 中的 `guard()` 和 `scoped_guard()` 宏来改进 EL1 和 EL2 的锁管理，减少锁泄漏和死锁的风险。

在历史讨论中，Fuad 提到在审查 Sebastien 的 GIC 硬化系列时发现了锁泄漏的问题，这促使他提出了这一补丁系列。补丁分为两部分：前五个补丁针对 EL2，后五个补丁针对 EL1，主要是将手动的锁管理替换为自动的范围管理，从而简化代码并提高可读性。

在本周的新讨论中，Fuad 提交了多个补丁，逐步将手动的锁调用迁移到 `guard()` 宏中，简化了错误处理流程，消除了对手动解锁的需求。参与者 Marc Zyngier 对这一方法表示支持，但也提出了在代码修改时逐步转换的建议，以避免后续维护中的困难。Jonathan Cameron 则提醒在同一函数中混用 `goto` 和 `guard()` 可能导致问题，建议在实现中保持一致性。

整体来看，本周的讨论集中在补丁的具体实现和代码风格的优化上，参与者们对补丁的方向表示认可，同时也提出了改进建议。

#### 📝 邮件列表

1. **[03-16 17:35]** [PATCH 00/10] KVM: arm64: Adopt scoped resource management (guard)
 for EL1 and EL2
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[03-16 17:35]** [PATCH 01/10] KVM: arm64: Add scoped resource management (guard) for hyp_spinlock
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[03-16 17:35]** [PATCH 02/10] KVM: arm64: Use guard(hyp_spinlock) in page_alloc.c
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[03-16 17:35]** [PATCH 03/10] KVM: arm64: Use guard(hyp_spinlock) in ffa.c
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[03-16 17:35]** [PATCH 04/10] KVM: arm64: Use guard(hyp_spinlock) in mm.c
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[03-16 17:35]** [PATCH 05/10] KVM: arm64: Use guard(hyp_spinlock) in pkvm.c
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[03-16 17:35]** [PATCH 06/10] KVM: arm64: Use guard(mutex) in mmu.c
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[03-16 17:35]** [PATCH 07/10] KVM: arm64: Use scoped resource management in arm.c
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[03-16 17:35]** [PATCH 08/10] KVM: arm64: Use guard(spinlock) in psci.c
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[03-16 17:35]** [PATCH 09/10] KVM: arm64: Use guard(spinlock) in reset.c
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[03-16 17:35]** [PATCH 10/10] KVM: arm64: Use guard(mutex) in pkvm.c
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[03-16 17:39]** Re: [PATCH 00/10] KVM: arm64: Adopt scoped resource management
 (guard) for EL1 and EL2
   - 发件人: Fuad Tabba <tabba@google.com>
13. **[03-17 08:20]** Re: [PATCH 00/10] KVM: arm64: Adopt scoped resource management (guard) for EL1 and EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[03-17 09:06]** Re: [PATCH 00/10] KVM: arm64: Adopt scoped resource management
 (guard) for EL1 and EL2
   - 发件人: Fuad Tabba <tabba@google.com>
15. **[03-17 17:40]** Re: [PATCH 03/10] KVM: arm64: Use guard(hyp_spinlock) in ffa.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
16. **[03-17 17:44]** Re: [PATCH 04/10] KVM: arm64: Use guard(hyp_spinlock) in mm.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
17. **[03-17 17:47]** Re: [PATCH 05/10] KVM: arm64: Use guard(hyp_spinlock) in pkvm.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
18. **[03-17 17:50]** Re: [PATCH 06/10] KVM: arm64: Use guard(mutex) in mmu.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
19. **[03-17 17:53]** Re: [PATCH 07/10] KVM: arm64: Use scoped resource management in
 arm.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
20. **[03-17 17:54]** Re: [PATCH 08/10] KVM: arm64: Use guard(spinlock) in psci.c
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
21. **[03-17 18:01]** Re: [PATCH 03/10] KVM: arm64: Use guard(hyp_spinlock) in ffa.c
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 7: [PATCH v11 00/16] Direct Map Removal Support for guest_memfd

**📧 邮件数**: 17 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 17 Mar 2026 14:10:32 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 中 guest_memfd 的直接映射移除支持的补丁（PATCH v11 00/16），旨在提高虚拟机内存的安全性，特别是防止 Spectre 风格的攻击。

1. **原始补丁内容**：该补丁系列扩展了 guest_memfd 的功能，使其能够从主机内核的直接映射中移除虚拟机的来宾内存。这种移除可以有效阻止潜在的投机执行攻击，因为内核页表中不再包含指向来宾内存的条目。

2. **历史讨论要点**：之前的讨论集中在如何实现这一功能的设计和实现细节，包括对不同架构的支持和相关的系统调用（如 write()）的兼容性。补丁经过多次迭代，逐步完善了实现方案。

3. **本周新讨论与进展**：本周的讨论主要围绕补丁的具体实现，包括对内存设置函数的改进、添加 folio_{zap,restore}_direct_map 辅助函数、以及在 KVM 中引入 GUEST_MEMFD_FLAG_NO_DIRECT_MAP 标志。该标志用于在创建 guest_memfd 时指示是否移除直接映射。此外，补丁还增加了自测试，以确保在移除直接映射的情况下，虚拟机能够正常执行 MMIO 操作。整体上，本周的讨论显示出对补丁的积极反馈和逐步完善的过程。

#### 📝 邮件列表

1. **[03-17 14:10]** [PATCH v11 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
2. **[03-17 14:10]** [PATCH v11 01/16] set_memory: set_direct_map_* to take address
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
3. **[03-17 14:10]** [PATCH v11 02/16] set_memory: add folio_{zap,restore}_direct_map
 helpers
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
4. **[03-17 14:11]** [PATCH v11 03/16] mm/secretmem: make use of
 folio_{zap,restore}_direct_map
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
5. **[03-17 14:11]** [PATCH v11 04/16] mm/gup: drop secretmem optimization from
 gup_fast_folio_allowed
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
6. **[03-17 14:11]** [PATCH v11 05/16] mm/gup: drop local variable in
 gup_fast_folio_allowed
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
7. **[03-17 14:11]** [PATCH v11 06/16] mm: introduce AS_NO_DIRECT_MAP
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
8. **[03-17 14:11]** [PATCH v11 07/16] KVM: guest_memfd: Add stub for
 kvm_arch_gmem_invalidate
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
9. **[03-17 14:12]** [PATCH v11 08/16] KVM: x86: define
 kvm_arch_gmem_supports_no_direct_map()
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
10. **[03-17 14:12]** [PATCH v11 09/16] KVM: arm64: define
 kvm_arch_gmem_supports_no_direct_map()
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
11. **[03-17 14:12]** [PATCH v11 10/16] KVM: guest_memfd: Add flag to remove from direct
 map
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
12. **[03-17 14:12]** [PATCH v11 11/16] KVM: selftests: load elf via bounce buffer
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
13. **[03-17 14:12]** [PATCH v11 12/16] KVM: selftests: set KVM_MEM_GUEST_MEMFD in
 vm_mem_add() if guest_memfd != -1
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
14. **[03-17 14:13]** [PATCH v11 13/16] KVM: selftests: Add guest_memfd based
 vm_mem_backing_src_types
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
15. **[03-17 14:13]** [PATCH v11 14/16] KVM: selftests: cover
 GUEST_MEMFD_FLAG_NO_DIRECT_MAP in existing selftests
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
16. **[03-17 14:13]** [PATCH v11 15/16] KVM: selftests: stuff vm_mem_backing_src_type into
 vm_shape
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
17. **[03-17 14:13]** [PATCH v11 16/16] KVM: selftests: Test guest execution from direct
 map removed gmem
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>

---

### Thread 8: [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay

**📧 邮件数**: 12 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 21 Mar 2026 21:24:14 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁系列，主要涉及对 PSCI（Power State Coordination Interface）中继的重构。Marc Zyngier 提出了五个补丁，目的是对现有代码进行清理和简化，尽管这些补丁并不修复任何特定问题。

在历史讨论中，Marc 提到他在调试过程中发现 PSCI 中继代码的可读性较差，因此决定进行重构。补丁内容包括：将错误处理移动到函数末尾、简化 CPU 启动时的 BTI（Branch Target Identification）处理、将某些函数标记为内部标签、使用直接函数指针替代布尔值来判断 CPU 状态，以及移除多余的 ISB（Instruction Synchronization Barrier）。

本周的讨论中，Fuad Tabba 对所有补丁进行了审查并给予了“已审核”标记，确认了补丁的有效性，并提出了对补丁 4 的小修正建议。整体来看，本周的进展主要集中在对补丁的审查和确认上，未出现新的问题或争议。

#### 📝 邮件列表

1. **[03-21 21:24]** [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-21 21:24]** [PATCH 1/5] KVM: arm64: pkvm: Move error handling to the end of kvm_hyp_cpu_entry
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-21 21:24]** [PATCH 2/5] KVM: arm64: pkvm: Simplify BTI handling on CPU boot
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-21 21:24]** [PATCH 3/5] KVM: arm64: pkvm: Turn __kvm_hyp_init_cpu into an inner label
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-21 21:24]** [PATCH 4/5] KVM: arm64: pkvm: Use direct function pointers for cpu_{on,resume}
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-21 21:24]** [PATCH 5/5] KVM: arm64: Remove extra ISBs when using msr_hcr_el2
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-22 15:08]** Re: [PATCH 1/5] KVM: arm64: pkvm: Move error handling to the end of kvm_hyp_cpu_entry
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[03-22 15:37]** Re: [PATCH 2/5] KVM: arm64: pkvm: Simplify BTI handling on CPU boot
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[03-22 15:43]** Re: [PATCH 3/5] KVM: arm64: pkvm: Turn __kvm_hyp_init_cpu into an
 inner label
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[03-22 15:49]** Re: [PATCH 4/5] KVM: arm64: pkvm: Use direct function pointers for cpu_{on,resume}
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[03-22 15:55]** Re: [PATCH 5/5] KVM: arm64: Remove extra ISBs when using msr_hcr_el2
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[03-22 15:57]** Re: [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 9: [PATCH v3 00/36] KVM: arm64: Add support for protected guest memory with pKVM

**📧 邮件数**: 10 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  5 Mar 2026 14:43:13 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上支持受保护来宾内存的补丁（PATCH v3 00/36）。该补丁旨在通过 pKVM（Protected Kernel Virtual Machine）实现来宾虚拟机的内存隔离，增强安全性。

**历史讨论**中，Will Deacon 提出了多个补丁，主要包括：
1. 引入新的 pKVM 超调用，以支持将内存页面捐赠给受保护的来宾。
2. 处理内核访问不可访问页面时的异常情况，避免系统崩溃。
3. 允许用户空间创建受保护的虚拟机，并对其进行配置。

**本周新讨论**中，Marc Zyngier 对补丁提出了一些具体问题和建议：
1. 对于 KVM_MAX_OWNER_ID 和 PKVM_ID_GUEST 的关系提出疑问，建议定义应更为清晰。
2. 表达了对增加配置选项的反对意见，认为现有的命令行选项已足够。
3. 针对如何处理内存回收和故障注入的机制进行了深入讨论，提出了对 EL3 处理故障的信任问题。

总体来看，讨论围绕补丁的实现细节、配置选项的必要性以及内存管理的安全性展开，参与者对如何优化 pKVM 的实现提出了建设性的意见。

#### 📝 邮件列表

1. **[03-05 14:43]** [PATCH v3 00/36] KVM: arm64: Add support for protected guest memory with pKVM
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-05 14:43]** [PATCH v3 11/36] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-05 14:43]** [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-05 14:43]** [PATCH v3 26/36] KVM: arm64: Return -EFAULT from VCPU_RUN on access to a poisoned pte
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-05 14:43]** [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Will Deacon <will@kernel.org>
6. **[03-20 12:38]** Re: [PATCH v3 11/36] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-20 13:22]** Re: [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-20 16:20]** Re: [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-20 16:35]** Re: [PATCH v3 26/36] KVM: arm64: Return -EFAULT from VCPU_RUN on access to a poisoned pte
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[03-21 09:39]** Re: [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 10: [PATCH v1 00/13] KVM: arm64: Refactor user_mem_abort() into a
 state-object model

**📧 邮件数**: 10 | **👥 参与者**: 3 | **📅 开始时间**: Fri,  6 Mar 2026 14:02:19 +0000

#### 🤖 AI 总结

本邮件讨论的主题是对 KVM 的 arm64 架构中的 `user_mem_abort()` 函数进行重构，目的是将其改造成一个状态对象模型，以提高代码的可读性和可维护性。

**原始 patch/问题的内容**：
Fuad Tabba 提出的补丁系列（共 13 个补丁）旨在通过将 `user_mem_abort()` 函数拆分为更小的、专注的辅助函数来简化其复杂性。该函数目前的实现过于庞大，导致错误处理和状态管理困难，尤其是在处理早期错误返回时容易造成资源泄露。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 对补丁表示认可，认为这是一个有价值的起点，并鼓励进一步的改进。Fuad 也表示拆分代码的过程令人满意，期待更多的反馈和建议。

**本周的新讨论、进展或结论**：
本周，Marc Zyngier 提出了进一步的改进建议，计划去掉 `kvm_s2_fault` 结构，并以更灵活的方式管理状态。此外，Joey Gouly 对前两个补丁进行了审核，表示认可，并提出了一些小的改进意见。整体来看，讨论氛围积极，参与者对补丁的方向表示支持，并在不断推动代码的优化。

#### 📝 邮件列表

1. **[03-06 14:02]** [PATCH v1 00/13] KVM: arm64: Refactor user_mem_abort() into a
 state-object model
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[03-06 14:02]** [PATCH v1 01/13] KVM: arm64: Extract VMA size resolution in user_mem_abort()
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[03-06 14:02]** [PATCH v1 02/13] KVM: arm64: Introduce struct kvm_s2_fault to user_mem_abort()
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[03-06 14:02]** [PATCH v1 11/13] KVM: arm64: Optimize early exit checks in kvm_s2_fault_pin_pfn()
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[03-06 15:34]** Re: [PATCH v1 00/13] KVM: arm64: Refactor user_mem_abort() into a state-object model
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-06 15:44]** Re: [PATCH v1 00/13] KVM: arm64: Refactor user_mem_abort() into a
 state-object model
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[03-16 18:13]** Re: [PATCH v1 00/13] KVM: arm64: Refactor user_mem_abort() into a state-object model
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-17 15:07]** Re: [PATCH v1 01/13] KVM: arm64: Extract VMA size resolution in
 user_mem_abort()
   - 发件人: Joey Gouly <joey.gouly@arm.com>
9. **[03-17 16:00]** Re: [PATCH v1 02/13] KVM: arm64: Introduce struct kvm_s2_fault to
 user_mem_abort()
   - 发件人: Joey Gouly <joey.gouly@arm.com>
10. **[03-17 17:10]** Re: [PATCH v1 11/13] KVM: arm64: Optimize early exit checks in
 kvm_s2_fault_pin_pfn()
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 11: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 9 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 13 Mar 2026 14:45:37 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM 架构的 MPAM（Memory Partitioning and Monitoring）功能的补丁系列，特别是与 KVM/arm64 和 resctrl 的集成。历史讨论中，Ben Horgan 提出了一个补丁系列（PATCH v6 00/40），该系列简化了内存带宽利用率的实现，暂时不支持内存带宽利用率，并将 CDP（Cache Allocation Technology）功能隐藏在 CONFIG_EXPERT 选项下，以避免潜在的 PARTID 超出范围问题。

在本周的新讨论中，参与者们对该补丁系列进行了测试，结果表明 L3 CPOR（Cache Partitioning on Read）功能在 Ampere 实现上工作正常，延迟表现符合预期。Jesse Chick 和 Shaopeng Tan 都确认了补丁的有效性并进行了测试。Jonathan Cameron 和 Zeng Heng 对补丁的具体实现进行了审核，表示认可并提供了反馈。Zeng Heng 还提到，虽然隐藏 CDP 是一种短期解决方案，但需要进一步修改 resctrl 以处理挂载会话之间的 limbo 状态。

总体来看，本周的讨论集中在补丁的测试结果和审核反馈上，显示出该补丁系列在功能实现上的积极进展。

#### 📝 邮件列表

1. **[03-13 14:45]** [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
2. **[03-13 14:45]** [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after applying configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
3. **[03-13 14:45]** [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind CONFIG_EXPERT
   - 发件人: Ben Horgan <ben.horgan@arm.com>
4. **[03-16 17:25]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Jesse Chick <jessechick@os.amperecomputing.com>
5. **[03-17 17:22]** Re: [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after
 applying configuration
   - 发件人: Jonathan Cameron <jonathan.cameron@huawei.com>
6. **[03-18 08:09]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Shaopeng Tan (Fujitsu) <tan.shaopeng@fujitsu.com>
7. **[03-18 10:22]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
8. **[03-18 10:23]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[03-18 19:04]** Re: [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind
 CONFIG_EXPERT
   - 发件人: Zeng Heng <zengheng4@huawei.com>

---

### Thread 12: [PATCH v2 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 18 Mar 2026 19:19:12 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 ARM64 架构的 C1-Pro 处理器的错误修复，具体是针对 Erratum 4193714（CVE-2026-0995）的补丁版本 2（PATCH v2 0/4）。

**原始问题及补丁内容**：
C1-Pro 处理器在执行 TLB（Translation Lookaside Buffer）无效化和 DSB（Data Synchronization Barrier）序列时，可能无法确保所有 SME（Scalable Matrix Extension）内存访问的完成。为了解决这个问题，补丁提出了一种方法，在所有启用 SME 的受影响 CPU 上执行 DSB，以确保 SME 访问在确认 IPI（Inter-Processor Interrupt）之前完成。

**历史讨论要点**：
之前的讨论集中在补丁的初始版本上，补丁的主要逻辑是通过全局的 `sme_active_cpus` 掩码来跟踪哪些 CPU 在用户空间中启用了 SME，并向这些 CPU 发送 IPI 以同步 TLB 维护。补丁还讨论了 DMB（Data Memory Barrier）的必要性，并提出了使用 `alternative_has_cap_unlikely()` 代替 `cpus_have_final_cap()` 的建议。

**本周新讨论及进展**：
本周的讨论主要围绕补丁的具体实现和细节修改。Catalin Marinas 提出了对补丁的多个改进，包括在 SME 禁用时不启用该补丁、引入新的 TLB 维护函数、以及对 `sme_set_active()` 函数的注释更新。此外，James Morse 提出了在 KVM 中添加 SMC 钩子以处理 SME dvmsync 错误的补丁。Will Deacon 对补丁提出了一些小的修改建议，并询问了补丁的合并计划。Catalin 表示将根据反馈进行调整并在下周重新提交补丁。

总体而言，本周的讨论进一步细化了补丁的实现细节，并为后续的版本更新奠定了基础。

#### 📝 邮件列表

1. **[03-18 19:19]** [PATCH v2 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[03-18 19:19]** [PATCH v2 1/4] arm64: tlb: Introduce __tlbi_sync_s1ish_{kernel,batch}() for TLB maintenance
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[03-18 19:19]** [PATCH v2 2/4] arm64: tlb: Pass the corresponding mm to __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
4. **[03-18 19:19]** [PATCH v2 3/4] arm64: errata: Work around early CME DVMSync acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-18 19:19]** [PATCH v2 4/4] KVM: arm64: Add SMC hook for SME dvmsync erratum
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
6. **[03-18 19:22]** [RFC PATCH] arm64: errata: Use mm_cpumask() for the CME DVMSync workaround
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
7. **[03-19 13:32]** Re: [PATCH v2 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-19 15:45]** Re: [PATCH v2 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 13: [PATCH 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  2 Mar 2026 16:57:53 +0000

#### 🤖 AI 总结

本邮件讨论主题为针对 Arm C1-Pro 处理器的 erratum 4193714（CVE-2026-0995）的补丁。该 erratum 导致在执行 TLBI+DSB 序列时，可能无法确保所有 SME（可扩展矩阵扩展）内存访问的完成，从而可能在内存访问未完成时重用页面。为了解决这个问题，补丁提出在所有启用 SME 的受影响 CPU 上执行 DSB，以确保 SME 访问的完成。

在历史讨论中，参与者们探讨了该补丁的有效性及其对系统的影响。Will Deacon 提出，如果完全禁用 SME（通过命令行参数 arm64.nosme），则该补丁可能不再必要。Catalin Marinas 和其他参与者讨论了该 erratum 的具体实现细节，确保在 SME 访问之前观察到 sme_active_cpus 的掩码。

在本周的新讨论中，Mark Rutland 强调了 C1-Pro 在 TLB 无效化方面提供的微架构特性，指出在特定情况下，TLBI 的处理顺序可能影响 SME 访问的结果。他进一步解释了在执行 SME 指令时，如何确保先前的存储操作被全局观察到，以避免使用过时的翻译。

总体而言，讨论集中在补丁的必要性、实现细节及其对系统性能的潜在影响上，参与者们对如何有效处理该 erratum 进行了深入的技术探讨。

#### 📝 邮件列表

1. **[03-02 16:57]** [PATCH 0/4] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[03-02 16:57]** [PATCH 3/4] arm64: errata: Work around early CME DVMSync acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[03-05 14:32]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-06 12:00]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-09 10:13]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
6. **[03-10 15:35]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
7. **[03-12 14:55]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-17 12:09]** Re: [PATCH 3/4] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 14: [PATCH v3] tracing: Generate undef symbols allowlist for simple_ring_buffer

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 16 Mar 2026 09:28:45 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），其内容为“生成简单环形缓冲区的未定义符号允许列表”。该补丁旨在通过自动检测符号来增强允许列表的鲁棒性，替代原有的硬编码列表，以应对不同架构下编译器和工具生成的符号维护困难的问题。

在之前的讨论中，补丁经历了多个版本的修改。主要改动包括：确保启用 KASAN 以避免在某些架构上禁用 FORTIFY_SOURCE，使用 filechk 工具，移除过时的 extra-y，添加 simple_ring_buffer 和 memcpy() 以生成更多符号，以及添加 __sancov。

在本周的新讨论中，Vincent Donnefort 提到已将补丁添加到随机配置构建中，等待测试结果。Arnd Bergmann 反馈在几百个随机配置构建中发现了一处遗漏，补丁需要添加 "__msan" 符号以处理特定的未定义符号。Marc Zyngier 随后确认已将此修改合并，并表示补丁已成功应用。

总结来说，该补丁的开发和测试进展顺利，最终已被合并到主线代码中。

#### 📝 邮件列表

1. **[03-16 09:28]** [PATCH v3] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-16 12:06]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Arnd Bergmann <arnd@arndb.de>
3. **[03-16 10:09]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Steven Rostedt <rostedt@goodmis.org>
4. **[03-16 21:47]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Arnd Bergmann <arnd@arndb.de>
5. **[03-16 21:48]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Arnd Bergmann <arnd@arndb.de>
6. **[03-17 09:03]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-17 09:04]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-17 09:04]** Re: [PATCH v3] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 15: [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 17 Mar 2026 18:26:36 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在通过 debugfs 暴露影子页表（shadow page tables），以提高调试和测试的能力。

**原始补丁内容**：
补丁 v2 包含两个主要部分：一是使 KVM 的页表转储代码支持第二级 MMU（s2 mmu），二是创建一个新的 debugfs 目录“nested”，在其中为每个有效的 s2 mmu 暴露其影子页表，文件名格式为 `0x<vttbr>-0x<vtcr>-s2-{en,dis}abled`。

**之前讨论要点**：
在补丁 v1 中，开发者提出了类似的功能，但未能充分考虑到 s2 mmu 的支持。补丁 v2 解决了这些问题，并进行了小幅改进，包括将 debugfs 条目与配置选项 `CONFIG_PTDUMP_STAGE2_DEBUGFS` 关联。

**本周新讨论及进展**：
本周的讨论中，Wei-Lin Chang 提交了补丁 v2，得到了 Sebastian 和 Joey Gouly 的审核与认可。Marc Zyngier 也提供了代码示例，并建议在输出的十六进制值中添加前导零，以提高可读性。最终，补丁得到了确认，标志着该功能的进一步完善和即将合并。

#### 📝 邮件列表

1. **[03-17 18:26]** [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-17 18:26]** [PATCH v2 1/2] KVM: arm64: ptdump: Make KVM ptdump code s2 mmu aware
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[03-17 18:26]** [PATCH v2 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[03-18 11:42]** Re: [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Joey Gouly <joey.gouly@arm.com>
5. **[03-19 16:01]** Re: [PATCH v2 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-21 16:36]** Re: [PATCH v2 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 16: [PATCH v5 0/5] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs

**📧 邮件数**: 6 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 17 Mar 2026 20:10:33 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试（selftests）进行改进，主要集中在 `set_id_regs` 函数的诊断信息提升上。

**原始 patch/问题的内容**：
Mark Brown 提出了一个包含五个补丁的系列，旨在改善在执行 guest 寄存器读取和重置值保持测试时的诊断信息。当前的测试在失败时仅返回致命断言，未能明确指出出错的寄存器。

**之前讨论要点**：
在之前的讨论中，开发者们关注到测试输出缺乏详细信息，导致调试困难。因此，补丁系列的目标是将每个寄存器的测试结果单独报告，并将致命断言替换为标准的 kselftest 报告，以提高可读性和可调试性。

**本周的新讨论、进展或结论**：
本周的讨论中，Mark Brown 提交了补丁的最新版本（v5），并逐一详细描述了每个补丁的修改内容，包括：
1. 将寄存器读取和重置测试的结果分别报告。
2. 将寄存器位域有效性检查的致命断言改为非致命报告。
3. 针对 aarch64 仅系统跳过 32 位 ID 寄存器的测试，以避免虚假错误。
4. 引入 `is_aarch32_id_reg()` 函数以简化对 32 位 ID 寄存器的检查。

这些改进将显著提升测试的诊断能力，使开发者能够更容易地识别和解决问题。

#### 📝 邮件列表

1. **[03-17 20:10]** [PATCH v5 0/5] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[03-17 20:10]** [PATCH v5 1/5] KVM: selftests: arm64: Report set_id_reg reads of
 test registers as tests
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[03-17 20:10]** [PATCH v5 2/5] KVM: selftests: arm64: Report register reset tests
 individually
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[03-17 20:10]** [PATCH v5 3/5] KVM: selftests: arm64: Make set_id_regs bitfield
 validatity checks non-fatal
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[03-17 20:10]** [PATCH v5 4/5] KVM: selftests: arm64: Skip all 32 bit IDs when
 set_id_regs is aarch64 only
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[03-17 20:10]** [PATCH v5 5/5] KVM: selftests: arm64: Use is_aarch32_id_reg() in
 test_vm_ftr_id_regs()
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 17: [PATCH RESEND 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Sun,  8 Mar 2026 23:18:27 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于KVM（Kernel-based Virtual Machine）在arm64架构下的一个补丁，旨在通过debugfs暴露影子页表，以提高对嵌套虚拟化（NV）的调试和测试能力。

**原始补丁内容**：
补丁的核心是通过debugfs暴露影子页表，具体实现包括教会KVM的ptdump代码处理不同的s2 MMU，并在每个虚拟机创建时生成一个新的“nested”目录，目录中包含每个有效s2 MMU的影子页表文件。

**之前讨论要点**：
在历史讨论中，参与者对补丁的实现进行了审查和建议。Sebastian Ene建议将某些定义的大小隐藏在宏后面，以提高代码的可读性和安全性。Marc Zyngier则提出了直接表达字符串的方式，认为这样更为明确，并且编译器能够优化为常量。

**本周的新讨论**：
在本周的讨论中，Wei-Lin Chang对Marc Zyngier的建议表示感谢，并确认将根据建议进行修改。这表明补丁的开发者对反馈持开放态度，并积极进行调整，以提高代码质量。

总体来看，讨论围绕着如何更好地实现和优化补丁，以提高KVM在arm64架构下的调试能力，参与者之间的互动积极且富有建设性。

#### 📝 邮件列表

1. **[03-08 23:18]** [PATCH RESEND 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-08 23:18]** [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[03-11 15:41]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[03-13 22:28]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[03-14 09:39]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-16 10:52]** Re: [PATCH RESEND 2/2] KVM: arm64: nv: Expose shadow page tables in
 debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 18: [PATCH v2 00/11] arm64: Fully disable configured-out features

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  2 Mar 2026 11:56:41 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的补丁系列，旨在完全禁用在编译时配置的特性，以改善内核中对这些特性的处理。

**原始补丁内容**：
Marc Zyngier 提出的补丁系列（PATCH v2 00/11）主要关注如何处理在编译时禁用的特性，确保这些特性不会在内核的其他部分泄露。补丁包括标记某些特性为不兼容、在二级引导路径中不更新被覆盖的特性等。

**之前讨论要点**：
在之前的讨论中，Marc Zyngier 提到了一些特性（如指针认证、SVE等）在编译时的决策会导致内核中不同部分对特性的认知不一致，可能引发状态泄露的问题。补丁的目标是通过完全移除这些特性在清理后的 ID 寄存器中的可见性来解决这一问题。

**本周新讨论进展**：
本周的讨论中，Catalin Marinas 对补丁进行了深入分析，指出了在处理覆盖特性时可能出现的逻辑不一致性，尤其是在处理二级 CPU 时的“粘性”特性问题。他表示支持补丁，但也提出了对不同 CPU 状态下的处理一致性问题的担忧。此外，他建议在某些情况下可以考虑简化配置的可见性，以减少潜在的复杂性和未来的问题。

总体来看，邮件讨论集中在如何更好地管理 ARM64 架构中编译时禁用特性的处理，确保内核的稳定性和一致性。

#### 📝 邮件列表

1. **[03-02 11:56]** [PATCH v2 00/11] arm64: Fully disable configured-out features
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-02 11:56]** [PATCH v2 01/11] arm64: Skip update of an idreg field affected by an override
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-02 11:56]** [PATCH v2 03/11] arm64: Add logic to fully remove features from sanitised id registers
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-19 15:34]** Re: [PATCH v2 01/11] arm64: Skip update of an idreg field affected
 by an override
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-19 17:38]** Re: [PATCH v2 03/11] arm64: Add logic to fully remove features from
 sanitised id registers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 19: [PATCH v4 0/4] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 17 Mar 2026 15:36:48 +0900

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（内核虚拟机）在异构 arm64 系统中使用多个主机 PMU（性能监控单元）的补丁（PATCH v4 0/4）。该补丁的主要目的是解决在 vCPU（虚拟中央处理器）迁移到具有不兼容 PMU 的物理 CPU（pCPU）时，性能计数器（如 PMCCNTR_EL0）停止递增的问题。这种情况虽然在架构上是允许的，但会导致 Windows 客户机崩溃。

补丁引入了 `KVM_ARM_VCPU_PMU_V3_FIXED_COUNTERS_ONLY` 属性，允许 KVM 在不支持可编程事件计数器的情况下模拟 PMUv3，从而使 Windows 客户机能够在异构系统上可靠运行，而无需 vCPU 钉扎。这一变化使得 VMM（虚拟机监控器）能够在所有可用的 pCPU 上调度 vCPU，充分利用主机硬件。

在本周的新讨论中，Akihiko Odaki 提出了四个补丁，分别是：添加 `kvm_pmu_enabled_counter_mask()` 函数、保护 PMU 列表以避免读取争用、引入 `FIXED_COUNTERS_ONLY` 属性，以及对该属性的自测。每个补丁都针对特定功能进行了改进和测试，确保新属性的正确性和稳定性。整体来看，本周的讨论集中在补丁的实现细节和测试验证上，显示出对 KVM 性能监控功能的持续优化。

#### 📝 邮件列表

1. **[03-17 15:36]** [PATCH v4 0/4] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[03-17 15:36]** [PATCH v4 1/4] KVM: arm64: PMU: Add kvm_pmu_enabled_counter_mask()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[03-17 15:36]** [PATCH v4 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[03-17 15:36]** [PATCH v4 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[03-17 15:36]** [PATCH v4 4/4] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 20: [PATCH] KVM: arm64: Fix the descriptor address in __kvm_at_swap_desc()

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 17 Mar 2026 19:57:48 +0800

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: Fix the descriptor address in __kvm_at_swap_desc()”，主要讨论了修复 KVM 中 arm64 架构的描述符地址计算问题。

在历史讨论中，未提供具体的背景信息，但本周的讨论集中在一个重要的补丁上。补丁的核心问题是使用错误的方式计算 S1/S2 描述符的虚拟地址，具体表现为在计算时错误地将偏移量乘以 8。补丁的作者 Zenghui Yu 指出，正确的计算方式应该是直接使用 `hva + offset`，而不是 `hva + offset*8`。该补丁修复了这一问题，并标记为修复了之前的提交 f6927b41d573。

在本周的新讨论中，Marc Zyngier 对 Zenghui Yu 的发现表示感谢，并对补丁的及时修复表示赞赏。最终，Zenghui Yu 确认该补丁已被应用，并将其纳入修复列表。此次讨论表明，团队对代码质量的重视以及快速响应问题的能力。

#### 📝 邮件列表

1. **[03-17 19:57]** [PATCH] KVM: arm64: Fix the descriptor address in __kvm_at_swap_desc()
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
2. **[03-17 13:37]** Re: [PATCH] KVM: arm64: Fix the descriptor address in __kvm_at_swap_desc()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-17 13:44]** Re: [PATCH] KVM: arm64: Fix the descriptor address in __kvm_at_swap_desc()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 21: [PATCH v17 0/8] support FEAT_LSUI

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 14 Mar 2026 17:51:25 +0000

#### 🤖 AI 总结

本邮件线程讨论了支持 Arm 架构中的 FEAT_LSUI 特性的补丁集（PATCH v17 0/8）。FEAT_LSUI 自 Armv9.6 起提供了特权级别的加载/存储指令，允许访问用户内存而无需清除 PSTATE.PAN 位。该补丁主要应用于 futex 原子操作等场景。

在历史讨论中，Yeoreum Yun 提到补丁集的更新内容，包括移除 __lsui_cmpxchg32() 中的循环，修改了一些注释并将其移至提交信息中。此外，补丁中第 7 个部分提出在启用 FEAT_LSUI 时使用 CAST 指令来交换虚拟机描述符，从而避免清除 PAN 位的需求。讨论中还指出，某些 CPU 可能会报告 FEAT_LSUI 但缺乏 FEAT_PAN，因此需要在缺少 FEAT_PAN 的情况下对 LSUI 指令进行包装。

在本周的新讨论中，Marc Zyngier 对第 7 个补丁进行了审核并表示支持，标记为“Reviewed-by”，显示出对该补丁的认可。这一进展表明补丁集在审查过程中取得了积极反馈，接下来可能会进入合并阶段。

#### 📝 邮件列表

1. **[03-14 17:51]** [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[03-14 17:51]** [PATCH v17 7/8] KVM: arm64: use CAST instruction for swapping guest descriptor
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[03-17 11:04]** Re: [PATCH v17 7/8] KVM: arm64: use CAST instruction for swapping guest descriptor
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 22: [PATCH v2] tracing: Generate undef symbols allowlist for simple_ring_buffer

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 10:58:29 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（PATCH v2），旨在为 `simple_ring_buffer` 生成未定义符号的允许列表。该补丁的目的是通过自动检测符号，取代硬编码的符号列表，从而提高跨架构的维护性。补丁的作者是 Vincent Donnefort。

在历史讨论中，Vincent 提到该补丁的初步版本已经接近完美，但在 RISC-V 架构等某些架构中，存在一些逻辑问题，这可能影响到符号的处理。Nathan Chancellor 对补丁提出了一些建议，包括使用 `filechk` 和移除过时的 `extra-y`，并建议将 `simple_ring_buffer` 添加到允许列表中。

在本周的新讨论中，Vincent 更新了补丁，发布了 v3 版本，并表示已经在本地进行了全面测试，涵盖了所有模块配置以及多种架构，使用了 clang 和 gcc 编译器。Vincent 对 Nathan 的帮助表示感谢，显示出讨论的积极进展和合作精神。

#### 📝 邮件列表

1. **[03-13 10:58]** [PATCH v2] tracing: Generate undef symbols allowlist for simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-13 09:37]** Re: [PATCH v2] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Nathan Chancellor <nathan@kernel.org>
3. **[03-16 09:31]** Re: [PATCH v2] tracing: Generate undef symbols allowlist for
 simple_ring_buffer
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 23: [PATCH] tracing: Adjust cmd_check_undefined to show unexpected
 undefined symbols

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 20 Mar 2026 14:29:33 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 Linux 内核追踪功能的补丁（patch），其目的是调整 `cmd_check_undefined` 命令，以便在检测到未定义符号时能够输出相关信息，帮助开发者理解构建失败的原因。

在历史讨论中，补丁的背景是由于在 `kernel/trace/Makefile` 中，当 `check_undefined` 命令失败时，缺乏输出信息使得开发者难以诊断问题。补丁通过捕获 `$(NM)` 和 `grep` 命令的输出，在构建失败时打印出未定义符号的详细信息，从而提高了可调试性。该补丁修复了之前提交的 commit `a717943d8ecc`，并建议将其合并到 KVM ARM 树中。

在本周的新讨论中，Nathan Chancellor 提交了补丁，并详细描述了其功能和实现方式。Arnd Bergmann 对该补丁表示认可，认为其非常有帮助，并期待在未来的开发中频繁使用。整体来看，本周的讨论进展顺利，补丁得到了积极的反馈，表明其将被进一步采纳。

#### 📝 邮件列表

1. **[03-20 14:29]** [PATCH] tracing: Adjust cmd_check_undefined to show unexpected
 undefined symbols
   - 发件人: Nathan Chancellor <nathan@kernel.org>
2. **[03-20 22:34]** Re: [PATCH] tracing: Adjust cmd_check_undefined to show unexpected undefined
 symbols
   - 发件人: Arnd Bergmann <arnd@arndb.de>

---

### Thread 24: [PATCH] KVM: arm64: vgic: Annotate struct vgic_dist with __counted_by_ptr

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 19 Mar 2026 01:54:10 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic（虚拟通用中断控制器）结构体进行的补丁。补丁的核心内容是为 `struct vgic_dist` 中的 `spis` 指针字段添加 `__counted_by_ptr` 属性，以便更好地追踪与该指针相关的元素数量。

在历史讨论中，补丁的背景并未详细阐述，但可以推测出，`nr_spis` 字段用于记录 `spis` 数组中的元素数量，并在 `vgic_init()` 函数中初始化。补丁的目的是通过代码注释提高代码的可读性和可维护性，确保在内存管理时能够正确跟踪指针的引用计数。

本周的新讨论中，Bill Wendling 提出了补丁的具体实现，并说明了 `nr_spis` 的初始化和使用方法。Kees Cook 对补丁进行了审查，并提出了对函数参数的可读性改进建议，认为可以直接使用 `dist->nr_spis` 而不是将其作为参数传递给 `kvm_vgic_dist_init()`。他还询问了在调用 `kvm_vgic_dist_init()` 之前，`dist->spis` 是否保证为 NULL。最终，Kees Cook 表示支持该补丁并给予了审查通过的反馈。

#### 📝 邮件列表

1. **[03-19 01:54]** [PATCH] KVM: arm64: vgic: Annotate struct vgic_dist with __counted_by_ptr
   - 发件人: Bill Wendling <morbo@google.com>
2. **[03-20 12:08]** Re: [PATCH] KVM: arm64: vgic: Annotate struct vgic_dist with
 __counted_by_ptr
   - 发件人: Kees Cook <kees@kernel.org>

---

### Thread 25: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 05 Mar 2026 16:28:16 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（内核虚拟机）在 arm64 架构下处理 PMUVer（性能监控单元版本）作为无符号数的补丁（patch）。该补丁旨在解决 PMUVer 和 PerfMon ID 字段的符号问题，最初由 James Clark 提出。补丁的背景是 Clark 在测试 "ARM64 PMU Partitioning" 补丁时发现了这些问题，并通过代码检查发现了第二个问题。

在历史讨论中，Clark 提到补丁的 v2 版本做了几项重要修改，包括正确处理 ID_AA64DFR0_EL1_PMUVer_IMP_DEF，修复了 cpufeature.c 中的符号错误，并重构了 has_pmuv3() 函数以保持一致性。

本周的新讨论中，Marc Zyngier 对该补丁进行了审查，认为由于该补丁对 KVM 的影响较小，建议将其通过 arm64/perf 树进行路由，并表示支持该补丁（Reviewed-by）。这表明补丁得到了积极的反馈，可能会在未来的版本中被合并。

#### 📝 邮件列表

1. **[03-05 16:28]** [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned
   - 发件人: James Clark <james.clark@linaro.org>
2. **[03-19 16:51]** Re: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 26: [PATCH v5 00/41] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 18 Mar 2026 09:52:59 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 ARM MPAM（内存性能监控架构）的补丁，旨在为 KVM/arm64 和 resctrl 提供支持。该补丁的主要内容是添加相关的“胶合代码”，以便更好地管理缓存资源。

在之前的讨论中，虽然没有具体的历史邮件记录，但可以推测出该补丁的提出是为了增强内核对 L3 缓存分区的支持，尤其是容量基础的分配方式。

在本周的新讨论中，参与者 Howard Zhang 提出了关于内核中 MPAM 支持的几个问题，特别是询问是否有计划将 L3 分区与容量基础的分配方式一起上游。对此，Ben Horgan 回应表示，确实有一些初步工作正在进行，以确定如何将新的 schema 添加到 resctrl 中，并预计缓存容量、CMIN/CMAX 将是最早使用这些新特性的功能之一。他还提供了一个链接，指向有关如何引入新 schema 的讨论。

总体来看，本周的讨论集中在对补丁的进一步细化和未来功能的规划上，显示出对 MPAM 支持的持续关注和发展。

#### 📝 邮件列表

1. **[03-18 09:52]** Re: [PATCH v5 00/41] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Howard Zhang <Howard.Zhang@arm.com>
2. **[03-18 11:16]** Re: [PATCH v5 00/41] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>

---

### Thread 27: [PATCH] KVM: arm64: avoid unused-variable warning

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 10:49:16 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在解决未使用变量的警告问题。

1. **原始 patch/问题的内容**：
   Arnd Bergmann 提出了一个补丁，目的是修复在 `arch/arm64/kvm/hyp_trace.c` 文件中，`cpu` 变量仅在条件编译块内使用，导致在没有用户时产生未使用变量的警告。补丁建议将 `#ifdef` 语句替换为等效的 `IS_ENABLED()` 检查，以避免此类警告。

2. **之前的讨论要点**：
   在历史讨论中，补丁的背景和具体问题被详细阐述，指出了未使用变量的警告是由于代码结构不当引起的，并提供了修复方案。

3. **本周的新讨论、进展或结论**：
   本周，Marc Zyngier 对补丁进行了回复，确认已将其应用到下一个版本中，并表示感谢。这表明补丁得到了认可并将被纳入未来的更新中。

总体来看，此次讨论有效地解决了代码中的警告问题，并推动了 KVM 的进一步完善。

#### 📝 邮件列表

1. **[03-13 10:49]** [PATCH] KVM: arm64: avoid unused-variable warning
   - 发件人: Arnd Bergmann <arnd@kernel.org>
2. **[03-17 09:17]** Re: [PATCH] KVM: arm64: avoid unused-variable warning
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 28: [PATCH] KVM: arm64: Remove @arch from __load_stage2()

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 18 Mar 2026 22:43:05 +0800

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: Remove @arch from __load_stage2()”，由Zenghui Yu提出，主要内容是建议在KVM的arm64架构中移除`__load_stage2()`函数中的`@arch`参数。根据提交记录，`@arch`参数自从提交`fe49fd940e22`后已不再需要，因为可以直接通过`kvm_s2_mmu`结构体获取相应的VTCR。

在历史讨论中，虽然没有具体的邮件记录，但可以推测之前的讨论集中在`__load_stage2()`函数的参数设计和必要性上。此次补丁的提出是基于对代码的审查，确认`@arch`参数的冗余性。

在本周的新讨论中，Zenghui Yu提交了补丁，详细列出了对多个文件的修改，包括删除`__load_stage2()`函数中的`@arch`参数，并相应调整了调用该函数的地方。补丁涉及的文件包括`kvm_mmu.h`、`at.c`、`mem_protect.h`、`switch.c`和`tlb.c`等，共修改了8个文件，增加10行代码，删除11行代码。该补丁的提交标志着对KVM arm64代码的进一步简化和优化。

#### 📝 邮件列表

1. **[03-18 22:43]** [PATCH] KVM: arm64: Remove @arch from __load_stage2()
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

### Thread 29: [PATCH] KVM: arm64: selftests: Avoid testing the IMPDEF behavior

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 17 Mar 2026 21:15:58 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试，具体是针对避免测试 IMPDEF 行为的补丁（patch）。

1. **原始 patch/问题的内容**：Zenghui Yu 提出的补丁旨在移除对 IMPDEF 行为的测试，原因是无法强制 KVM 在模拟 AT 指令时使用“慢路径”。补丁中删除了相关的测试代码，并对注释进行了改进。

2. **之前的讨论要点**：本次讨论没有提供历史讨论的背景信息，因此无法总结之前的讨论要点。

3. **本周的新讨论、进展或结论**：在本周的邮件中，Zenghui Yu 提出了补丁的具体修改，包括删除了对 TEST_ACCESS_FLAG 的测试，更新了相关注释，以更准确地反映 KVM 在处理 AT 指令时的行为。这一修改有助于简化测试代码，并避免不必要的测试，从而提高代码的可维护性。

总的来说，本周的讨论集中在补丁的实施和相关代码的优化上，反映了开发者对 KVM 自测试的持续改进。

#### 📝 邮件列表

1. **[03-17 21:15]** [PATCH] KVM: arm64: selftests: Avoid testing the IMPDEF behavior
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

### Thread 30: [PATCH v3 15/15] KVM: arm64: selftests: Add test for AT emulation

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 17 Mar 2026 20:51:34 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试，特别是针对 AT（Access Type）仿真的测试补丁。该补丁的编号为 PATCH v3 15/15，旨在增强 KVM 的测试覆盖率。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁是为了修复或改进 KVM 在处理访问标志时的行为，尤其是在仿真过程中可能出现的错误。

在本周的新讨论中，参与者 Zenghui Yu 提到需要修正一个关于访问标志故障的处理，指出在特定情况下（AF 位为 0 且 HA 未启用）应当处理访问标志故障。他还提到已经向 QEMU 提交了相关的修复。此外，Zenghui Yu 表示由于无法强制使用慢速仿真路径，应该避免测试不符合预期的行为（即 TEST_ACCESS_FLAG），并计划提交一个补丁以移除该测试。

总体来看，本周的讨论集中在对补丁的进一步修正和优化上，强调了在测试中避免不必要的复杂性。

#### 📝 邮件列表

1. **[03-17 20:51]** Re: [PATCH v3 15/15] KVM: arm64: selftests: Add test for AT emulation
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

## 📌 RFC

共 1 个 thread

---

### Thread 1: [RFC PATCH 00/14] KVM: ITS hardening for pKVM

**📧 邮件数**: 13 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 10 Mar 2026 12:49:19 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 pKVM 的 KVM ITS 硬化补丁系列（RFC PATCH 00/14），旨在增强 KVM 的设备访问安全性，防止攻击者通过 GIC/ITS 控制器篡改虚拟机内存。历史讨论中，Sebastian Ene 提出了多个补丁，重点在于为 KVM 提供必要的设备访问陷阱与仿真机制，并对 GIC/ITS 控制器进行硬化，以保护超管内存。

在之前的讨论中，参与者对补丁的命名和结构进行了深入探讨，建议使用更一致的术语来描述超管状态和主机状态的区别。此外，讨论还涉及了补丁的实现细节，包括 ITS 表的访问限制和命令队列的共享机制。

本周的新讨论中，Fuad Tabba 对多个补丁提出了具体的改进建议，包括命名一致性、代码逻辑的清晰性和安全性检查。他指出了潜在的错误和改进点，如处理 MMIO 陷阱时的顺序问题、内存对齐检查以及对 ITS 表的访问控制等。Sebastian 对这些反馈表示认可，并承诺将进行相应的修正和更新。整体来看，讨论集中在确保补丁的安全性和代码质量上，以实现更可靠的虚拟化环境。

#### 📝 邮件列表

1. **[03-10 12:49]** [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-10 12:49]** [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for KVM
 host deprivilege
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[03-10 12:49]** [PATCH 06/14] KVM: arm64: Add infrastructure for ITS emulation setup
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[03-10 12:49]** [PATCH 07/14] KVM: arm64: Restrict host access to the ITS tables
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[03-10 12:49]** [PATCH 08/14] KVM: arm64: Trap & emulate the ITS MAPD command
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[03-12 17:56]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[03-13 11:26]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[03-16 10:46]** Re: [PATCH 06/14] KVM: arm64: Add infrastructure for ITS emulation setup
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[03-16 16:13]** Re: [PATCH 07/14] KVM: arm64: Restrict host access to the ITS tables
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[03-17 09:40]** Re: [PATCH 06/14] KVM: arm64: Add infrastructure for ITS emulation setup
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[03-17 10:20]** Re: [PATCH 08/14] KVM: arm64: Trap & emulate the ITS MAPD command
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[03-20 14:42]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>
13. **[03-20 15:11]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

## 📌 Question

共 1 个 thread

---

### Thread 1: Question about ARM KVM stage2 contiguous bit support for contiguous
 hugetlb

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 13 Mar 2026 15:09:40 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM KVM 阶段 2 对于连续大页（contiguous hugetlb）支持的相关问题。

**原始 patch/问题的内容**：
Zhou Wang 提出了当前 KVM 阶段 2 支持连续大页，但在页表项（PTE）中未设置连续位，导致硬件无法为连续大页创建一个 TLB。为此，他建议在用户内存中中止时，不强制为连续页进行 PTE 映射，而是一次性映射所有连续页面，并在此过程中添加连续位。

**之前的讨论要点**：
Marc Zyngier 对此表示怀疑，认为在匿名内存的情况下，支持连续位的用例并不强。他指出，在内存压力不大的情况下，透明大页（THP）已经能够提供所需的性能提升，而在内存压力大的情况下，获得连续性是非常困难的。

**本周的新讨论、进展或结论**：
Zhou Wang 在本周的邮件中提到，他们希望使用 64KB 的基本页面，这样可以有 2M 的连续 PTE 和 512M 的块页面，但后者可能会浪费更多内存。他们在硬件仿真器上进行了初步测试，发现虚拟化的成本从 17% 降低到 3%。测试是在一个具有 4 个虚拟 CPU 和 8GB 内存的 VM 上进行的，使用 64KB 基本页面和 2M 连续大页的系统。Zhou Wang 表示将会在真实芯片上进行更多测试。

#### 📝 邮件列表

1. **[03-13 15:09]** Question about ARM KVM stage2 contiguous bit support for contiguous
 hugetlb
   - 发件人: Zhou Wang <wangzhou1@hisilicon.com>
2. **[03-13 07:49]** Re: Question about ARM KVM stage2 contiguous bit support for contiguous hugetlb
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-19 20:54]** Re: Question about ARM KVM stage2 contiguous bit support for
 contiguous hugetlb
   - 发件人: Zhou Wang <wangzhou1@hisilicon.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.0, take #4

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 20 Mar 2026 09:41:51 +0000

#### 🤖 AI 总结

本邮件讨论主题为 KVM/arm64 的修复补丁，主要针对 7.0 版本的修复。Marc Zyngier 提出了两项修复，主要涉及嵌套虚拟化的场景。

首先，补丁的内容包括：
1. 清除从重置状态恢复的虚拟 CPU（vcpu）的待处理异常状态，以避免影响其执行的第一条指令。
2. 修复地址转换仿真中的指针运算错误，确保在正确的页表项（PTE）上设置硬件访问位，而不是错误的位置。

在之前的讨论中，未提及具体的历史背景，但可以推测这些问题可能在嵌套虚拟化的使用场景中被观察到，并且是稳定性候选项。

本周的新讨论中，Marc Zyngier 强调了这两项修复的重要性，并请求将其合并到主分支中。这些修复被认为是必要的，以提高 KVM/arm64 的稳定性和可靠性。整体来看，本周的进展集中在确认和推动这些修复补丁的合并上。

#### 📝 邮件列表

1. **[03-20 09:41]** [GIT PULL] KVM/arm64 fixes for 7.0, take #4
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Discussion

共 1 个 thread

---

### Thread 1: [kvmtool PATCH v6 01/17] util/update_headers: Update
 linux/const.h from linux sources

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 19 Mar 2026 15:25:58 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于更新 `linux/const.h` 文件的补丁（patch），该补丁属于 kvmtool 项目的一部分。补丁的目的是将 `const.h` 文件从 Linux 源代码中更新，以确保 kvmtool 使用的是最新的常量定义。

在之前的讨论中，参与者对是否需要将 `const.h` 添加到更新列表进行了探讨。Will Deacon 提出，考虑到 `const.h` 与 virtio 和 kvm 头文件的不同，可能不需要更新该文件，建议直接使用静态版本。

在本周的新讨论中，Suzuki K Poulose 对 Will 的意见表示赞同，并承认在测试中遗漏了对该补丁的结构调整。他决定按照 Will 的建议，删除对 `const.h` 的更新部分。最终，Suzuki 确认将不再包含该更新，表示感谢并结束了讨论。

总结而言，本周的讨论主要集中在是否更新 `const.h`，最终决定不进行更新，保持使用静态版本。

#### 📝 邮件列表

1. **[03-19 15:25]** Re: [kvmtool PATCH v6 01/17] util/update_headers: Update
 linux/const.h from linux sources
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-20 10:40]** Re: [kvmtool PATCH v6 01/17] util/update_headers: Update
 linux/const.h from linux sources
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

## 📌 Other

共 2 个 thread

---

### Thread 1: [kvm-unit-tests PATCH v1 0/3] arm64: Add Stage-2 MMU and Nested Guest Framework

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 16 Mar 2026 15:43:46 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的 KVM 单元测试的三个补丁，主要涉及 Stage-2 MMU 和嵌套虚拟机框架的实现。

1. **原始补丁内容**：补丁系列旨在引入一种轻量级的基础设施，用于管理 ARM64 Stage-2 转换表和执行嵌套虚拟机。这些组件对于测试高级虚拟化特性（如嵌套虚拟化和 GICv4 直接中断注入）至关重要。补丁包括一个通用的 Stage-2 MMU 库，支持多种转换粒度（4K、16K、64K）和动态页表管理。

2. **之前讨论要点**：在之前的讨论中，参与者强调了该实现的初步性质，指出由于其处于早期阶段，可能缺少一些关键的架构元素或边界情况处理。讨论还提到需要在 L2 虚拟机中实现自己的分页，以便进行更全面的测试。

3. **本周的新讨论与进展**：本周的讨论中，Jing Zhang 提出了三个补丁的具体实现，包括 Stage-2 MMU 的管理库、裸机虚拟机执行框架以及 Stage-2 MMU 需求分页测试。Yao Yuan 建议在 L2 中实现 L1 的分页映射以支持更多测试，而 Marc Zyngier 则建议不要硬编码偏移量，建议从官方源生成这些定义，并指出 HCR_EL2.DC 在 KVM 中不被支持，可能会被弃用。

总的来说，本周的讨论集中在补丁的具体实现和未来改进的建议上，显示出对 ARM64 虚拟化测试框架的持续关注和开发。

#### 📝 邮件列表

1. **[03-16 15:43]** [kvm-unit-tests PATCH v1 0/3] arm64: Add Stage-2 MMU and Nested Guest Framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[03-16 15:43]** [kvm-unit-tests PATCH v1 1/3] lib: arm64: Add stage2 page table
 management library
   - 发件人: Jing Zhang <jingzhangos@google.com>
3. **[03-16 15:43]** [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest
 execution framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
4. **[03-16 15:43]** [kvm-unit-tests PATCH v1 3/3] arm64: Add Stage-2 MMU demand paging test
   - 发件人: Jing Zhang <jingzhangos@google.com>
5. **[03-17 09:46]** Re: [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest
 execution framework
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
6. **[03-17 08:09]** Re: [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest execution framework
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [kvm-unit-tests PATCH v1 0/5] basic EL1/EL0 guest support

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  6 Mar 2026 14:26:51 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 单元测试的基本 EL1/EL0 客户支持的补丁（PATCH v1 0/5）。该补丁旨在为在 EL1 或 EL0 运行代码提供基础设施，主要用于编写不需要独立地址空间或多个上下文的简单测试。

在历史讨论中，Joey Gouly 提出了五个补丁，其中前三个为准备性补丁，第四个补丁引入了“guest” API，最后一个补丁则使用该 API 添加了测试功能。特别是补丁 4 通过添加 `run_in_el1()` 和 `run_in_el0()` 函数，使得在 EL1 和 EL0 中运行指定函数成为可能，并且在 EL1 中共享地址空间。

在本周的新讨论中，Wei-Lin Chang 针对补丁 4 提出了一个问题，询问在执行 `eret` 指令之前是否需要添加指令屏障（isb），指出 `eret` 本身已经是一个上下文同步事件。此讨论表明对补丁细节的关注，可能影响补丁的最终实现。

总体来看，本周的讨论集中在补丁的实现细节上，特别是关于上下文同步的技术问题。

#### 📝 邮件列表

1. **[03-06 14:26]** [kvm-unit-tests PATCH v1 0/5] basic EL1/EL0 guest support
   - 发件人: Joey Gouly <joey.gouly@arm.com>
2. **[03-06 14:26]** [kvm-unit-tests PATCH v1 4/5] arm64: add EL0/EL1 guest functionality
   - 发件人: Joey Gouly <joey.gouly@arm.com>
3. **[03-17 00:41]** Re: [kvm-unit-tests PATCH v1 4/5] arm64: add EL0/EL1 guest
 functionality
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

