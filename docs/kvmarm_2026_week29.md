# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-07-20 00:38:51

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 583
- **总 Thread 数**: 50
- **大型 Thread** (>20封): 9 个

### 分类分布

- **PATCH**: 41 threads (520 邮件)
- **RFC**: 6 threads (59 邮件)
- **GIT PULL**: 2 threads (3 邮件)
- **Other**: 1 threads (1 邮件)

---

## 📌 PATCH

共 41 个 thread

---

### Thread 1: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 58 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 15:28:02 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 的 KVM 中对 Arm CCA（保密计算架构）的支持，主要集中在一系列补丁（PATCH v15 00/37）上。

1. **原始补丁/问题内容**：
   该补丁系列旨在为 KVM 提供对 Arm CCA 的支持，允许在 KVM 中运行受保护的虚拟机（VM）。补丁分为多个部分，涵盖了 RMM（运行时管理器）支持、内存管理、虚拟 CPU（vCPU）处理等。

2. **之前讨论要点**：
   之前的讨论主要集中在如何将 RMM 的功能集成到 KVM 中，包括如何处理虚拟机的内存、如何创建和管理 Realm（领域）等。讨论中提到 RMM v2.0 的新特性以及如何在 KVM 中实现这些特性。

3. **本周新讨论、进展或结论**：
   本周的讨论包括多个补丁的提交，涵盖了 Realm 的创建、内存映射、PSCI 请求处理、SVE（可扩展向量扩展）支持等。补丁中引入了对 Realm 的状态管理、内存保护、异常处理等功能的实现。此外，讨论中还提到了一些代码的重构和优化，以提高系统的稳定性和性能。参与者对补丁的细节进行了审查，并提出了一些改进建议。

总体而言，本周的讨论和补丁提交标志着对 KVM 中 Arm CCA 支持的进一步完善，确保了在虚拟化环境中对保密计算的有效管理。

#### 📝 邮件列表

1. **[07-15 15:28]** [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:28]** [PATCH v15 01/37] KVM: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-15 15:28]** [PATCH v15 02/37] KVM: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Steven Price <steven.price@arm.com>
4. **[07-15 15:28]** [PATCH v15 03/37] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Steven Price <steven.price@arm.com>
5. **[07-15 15:28]** [PATCH v15 04/37] KVM: arm64: CCA: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
6. **[07-15 15:28]** [PATCH v15 05/37] KVM: arm64: CCA: Check for LPA2 support
   - 发件人: Steven Price <steven.price@arm.com>
7. **[07-15 15:28]** [PATCH v15 06/37] KVM: arm64: CCA: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
8. **[07-15 15:28]** [PATCH v15 07/37] KVM: arm64: CCA: Add basic infrastructure for creating a realm
   - 发件人: Steven Price <steven.price@arm.com>
9. **[07-15 15:28]** [PATCH v15 08/37] KVM: arm64: CCA: Don't expose unsupported capabilities for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
10. **[07-15 15:28]** [PATCH v15 09/37] KVM: arm64: CCA: Allow passing the machine type in KVM creation
   - 发件人: Steven Price <steven.price@arm.com>
11. **[07-15 15:28]** [PATCH v15 10/37] KVM: arm64: CCA: Tear down RTTs
   - 发件人: Steven Price <steven.price@arm.com>
12. **[07-15 15:28]** [PATCH v15 11/37] KVM: arm64: CCA: Allocate and free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
13. **[07-15 15:28]** [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
14. **[07-15 15:28]** [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
15. **[07-15 15:28]** [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
16. **[07-15 15:28]** [PATCH v15 15/37] KVM: arm64: CCA: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>
17. **[07-15 15:28]** [PATCH v15 16/37] KVM: arm64: CCA: Handle realm MMIO emulation
   - 发件人: Steven Price <steven.price@arm.com>
18. **[07-15 15:28]** [PATCH v15 17/37] KVM: arm64: Expose support for private memory
   - 发件人: Steven Price <steven.price@arm.com>
19. **[07-15 15:28]** [PATCH v15 18/37] KVM: arm64: CCA: Create the realm descriptor
   - 发件人: Steven Price <steven.price@arm.com>
20. **[07-15 15:28]** [PATCH v15 19/37] KVM: arm64: CCA: Activate realms on first vCPU run
   - 发件人: Steven Price <steven.price@arm.com>
21. **[07-15 15:28]** [PATCH v15 20/37] KVM: arm64: CCA: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
22. **[07-15 15:28]** [PATCH v15 21/37] KVM: arm64: CCA: Set RIPAS of initial memslots
   - 发件人: Steven Price <steven.price@arm.com>
23. **[07-15 15:28]** [PATCH v15 22/37] KVM: arm64: CCA: Support runtime faulting of memory
   - 发件人: Steven Price <steven.price@arm.com>
24. **[07-15 15:28]** [PATCH v15 23/37] KVM: arm64: CCA: Handle realm vCPU load
   - 发件人: Steven Price <steven.price@arm.com>
25. **[07-15 15:28]** [PATCH v15 24/37] KVM: arm64: CCA: Validate register access for Realm VMs
   - 发件人: Steven Price <steven.price@arm.com>
26. **[07-15 15:28]** [PATCH v15 25/37] KVM: arm64: CCA: Handle Realm PSCI requests
   - 发件人: Steven Price <steven.price@arm.com>
27. **[07-15 15:28]** [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
28. **[07-15 15:28]** [PATCH v15 27/37] KVM: arm64: CCA: Allow userspace to inject aborts
   - 发件人: Steven Price <steven.price@arm.com>
29. **[07-15 15:28]** [PATCH v15 28/37] KVM: arm64: CCA: Support RSI_HOST_CALL
   - 发件人: Steven Price <steven.price@arm.com>
30. **[07-15 15:28]** [PATCH v15 29/37] KVM: arm64: CCA: Allow checking SVE on VM instance
   - 发件人: Steven Price <steven.price@arm.com>
31. **[07-15 15:28]** [PATCH v15 30/37] KVM: arm64: CCA: Prevent Device mappings for realms
   - 发件人: Steven Price <steven.price@arm.com>
32. **[07-15 15:28]** [PATCH v15 31/37] KVM: arm64: CCA: Propagate breakpoint and watchpoint counts to userspace
   - 发件人: Steven Price <steven.price@arm.com>
33. **[07-15 15:28]** [PATCH v15 32/37] KVM: arm64: CCA: Set breakpoint parameters through SET_ONE_REG
   - 发件人: Steven Price <steven.price@arm.com>
34. **[07-15 15:28]** [PATCH v15 33/37] KVM: arm64: CCA: Propagate max SVE vector length from the RMM
   - 发件人: Steven Price <steven.price@arm.com>
35. **[07-15 15:28]** [PATCH v15 34/37] KVM: arm64: CCA: Configure max SVE vector length for a Realm
   - 发件人: Steven Price <steven.price@arm.com>
36. **[07-15 15:28]** [PATCH v15 35/37] KVM: arm64: CCA: Provide register list for unfinalized RECs
   - 发件人: Steven Price <steven.price@arm.com>
37. **[07-15 15:28]** [PATCH v15 36/37] KVM: arm64: CCA: Provide an accurate register list
   - 发件人: Steven Price <steven.price@arm.com>
38. **[07-15 15:28]** [PATCH v15 37/37] KVM: arm64: CCA: Enable realms to be created
   - 发件人: Steven Price <steven.price@arm.com>
39. **[07-15 16:46]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Marc Zyngier <maz@kernel.org>
40. **[07-15 16:59]** Re: [PATCH v15 02/37] KVM: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Marc Zyngier <maz@kernel.org>
41. **[07-15 17:14]** Re: [PATCH v15 09/37] KVM: arm64: CCA: Allow passing the machine type in KVM creation
   - 发件人: Marc Zyngier <maz@kernel.org>
42. **[07-15 17:15]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
43. **[07-15 17:22]** Re: [PATCH v15 02/37] KVM: arm64: Avoid including linux/kvm_host.h in
 kvm_pgtable.h
   - 发件人: Steven Price <steven.price@arm.com>
44. **[07-15 17:25]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[07-15 17:31]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
46. **[07-15 17:43]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Marc Zyngier <maz@kernel.org>
47. **[07-16 09:36]** Re: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
48. **[07-16 10:17]** Re: [PATCH v15 09/37] KVM: arm64: CCA: Allow passing the machine type
 in KVM creation
   - 发件人: Steven Price <steven.price@arm.com>
49. **[07-16 10:17]** Re: [PATCH v15 26/37] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
50. **[07-16 10:20]** Re: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
51. **[07-16 10:23]** Re: [PATCH v15 05/37] KVM: arm64: CCA: Check for LPA2 support
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
52. **[07-16 10:37]** Re: [PATCH v15 09/37] KVM: arm64: CCA: Allow passing the machine type in KVM creation
   - 发件人: Marc Zyngier <maz@kernel.org>
53. **[07-16 10:40]** Re: [PATCH v15 06/37] KVM: arm64: CCA: Define the user ABI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
54. **[07-16 10:42]** Re: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
55. **[07-16 11:19]** Re: [PATCH v15 27/37] KVM: arm64: CCA: Allow userspace to inject
 aborts
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
56. **[07-16 11:22]** Re: [PATCH v15 28/37] KVM: arm64: CCA: Support RSI_HOST_CALL
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
57. **[07-16 11:25]** Re: [PATCH v15 17/37] KVM: arm64: Expose support for private memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
58. **[07-16 11:38]** Re: [PATCH v15 25/37] KVM: arm64: CCA: Handle Realm PSCI requests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 2: [PATCH v2 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3

**📧 邮件数**: 57 | **👥 参与者**: 6 | **📅 开始时间**: Tue, 14 Jul 2026 10:16:13 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上添加对 FEAT_NV2p1 和 FEAT_NV3 的支持的补丁系列。补丁的主要内容包括：

1. **原始补丁/问题内容**：
   - FEAT_NV2p1 主要修复了在嵌套虚拟化配置下，EL1 访问 CNTHCTL_EL2 和 CPTR_EL2 时缺失的状态位，减少了陷阱的数量。
   - FEAT_NV3 则更为复杂，改变了在嵌套虚拟化环境中 ERET 的行为，通过引入 NVHCR_EL2 寄存器来优化性能。

2. **之前讨论要点**：
   - 该系列补丁经过在 FVP 模型上的测试，显示出对 L1 客户机的指令减少约 1.5%，而在 L2 和 L3 客户机上则有更显著的性能提升。
   - 参与者讨论了补丁的设计和实现细节，包括对系统寄存器的处理和性能评估。

3. **本周的新讨论、进展或结论**：
   - 本周的讨论集中在补丁的具体实现上，包括对 NVHCR_EL2 的处理、对 CPTR_EL2 和 CNTHCTL_EL2 的访问优化，以及对 FEAT_NV3 的检测和暴露。
   - 参与者对补丁的多个方面进行了审查，并提出了一些潜在问题，如缺失的同步事件和寄存器状态泄露等。
   - Marc Zyngier 强调了补丁的设计意图，并针对审查反馈进行了回应，确保补丁的正确性和有效性。

总体而言，本周的讨论推动了对 KVM 嵌套虚拟化支持的进一步完善，同时也暴露出了一些需要解决的问题。

#### 📝 邮件列表

1. **[07-14 10:16]** [PATCH v2 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-14 10:16]** [PATCH v2 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping/Fields definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-14 10:16]** [PATCH v2 02/28] arm64: Update ID_AA64MMFR4_EL1 description to 2026-03 JSON release
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-14 10:16]** [PATCH v2 03/28] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-14 10:16]** [PATCH v2 04/28] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-14 10:16]** [PATCH v2 05/28] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-14 10:16]** [PATCH v2 06/28] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL register
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-14 10:16]** [PATCH v2 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor HFGITR_EL2.ERET on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-14 10:16]** [PATCH v2 08/28] arm64: Add ARM64_HAS_NV2P1 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-14 10:16]** [PATCH v2 09/28] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-14 10:16]** [PATCH v2 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[07-14 10:16]** [PATCH v2 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-14 10:16]** [PATCH v2 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[07-14 10:16]** [PATCH v2 13/28] arm64: sysreg: Add NVHCR_EL2 description as a mirror of HCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-14 10:16]** [PATCH v2 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[07-14 10:16]** [PATCH v2 15/28] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-14 10:16]** [PATCH v2 16/28] KVM: arm64: Split NV-specific exit fixups from the non-NV handling
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[07-14 10:16]** [PATCH v2 17/28] KVM: arm64: Add NV3 control bits to HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[07-14 10:16]** [PATCH v2 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[07-14 10:16]** [PATCH v2 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[07-14 10:16]** [PATCH v2 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[07-14 10:16]** [PATCH v2 21/28] KVM: arm64: Add NVHCR_EL2 handling to the sysreg array
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[07-14 10:16]** [PATCH v2 22/28] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[07-14 10:16]** [PATCH v2 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[07-14 10:16]** [PATCH v2 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[07-14 10:16]** [PATCH v2 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[07-14 10:16]** [PATCH v2 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[07-14 10:16]** [PATCH v2 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[07-14 10:16]** [PATCH v2 28/28] arm64: Add override for ID_AA64MMFR4_EL1.NV_frac
   - 发件人: Marc Zyngier <maz@kernel.org>
30. **[07-14 09:40]** Re: [PATCH v2 15/28] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: sashiko-bot@kernel.org
31. **[07-14 09:45]** Re: [PATCH v2 14/28] arm64: sysreg: Add HCRX_EL2 bits related to
 FEAT_NV3
   - 发件人: sashiko-bot@kernel.org
32. **[07-14 09:46]** Re: [PATCH v2 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: sashiko-bot@kernel.org
33. **[07-14 09:48]** Re: [PATCH v2 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: sashiko-bot@kernel.org
34. **[07-14 09:53]** Re: [PATCH v2 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: sashiko-bot@kernel.org
35. **[07-14 10:03]** Re: [PATCH v2 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: sashiko-bot@kernel.org
36. **[07-14 10:07]** Re: [PATCH v2 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: sashiko-bot@kernel.org
37. **[07-14 10:12]** Re: [PATCH v2 09/28] KVM: arm64: Relax CPTR_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: sashiko-bot@kernel.org
38. **[07-14 10:15]** Re: [PATCH v2 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: sashiko-bot@kernel.org
39. **[07-14 10:24]** Re: [PATCH v2 21/28] KVM: arm64: Add NVHCR_EL2 handling to the
 sysreg array
   - 发件人: sashiko-bot@kernel.org
40. **[07-14 12:42]** Re: [PATCH v2 15/28] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
41. **[07-14 12:45]** Re: [PATCH v2 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
42. **[07-14 13:56]** Re: [PATCH v2 21/28] KVM: arm64: Add NVHCR_EL2 handling to the sysreg array
   - 发件人: Marc Zyngier <maz@kernel.org>
43. **[07-14 14:04]** Re: [PATCH v2 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[07-14 14:18]** Re: [PATCH v2 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
45. **[07-14 15:12]** Re: [PATCH v2 09/28] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[07-14 15:22]** Re: [PATCH v2 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
47. **[07-14 15:23]** Re: [PATCH v2 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
48. **[07-14 15:41]** Re: [PATCH v2 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
49. **[07-14 15:42]** Re: [PATCH v2 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
50. **[07-14 15:44]** Re: [PATCH v2 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
51. **[07-15 01:16]** Re: [PATCH v2 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
52. **[07-15 08:33]** Re: [PATCH v2 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
53. **[07-15 01:00]** Re: [PATCH v2 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor
 HFGITR_EL2.ERET on ERET fast path
   - 发件人: Oliver Upton <oupton@kernel.org>
54. **[07-15 09:19]** Re: [PATCH v2 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor HFGITR_EL2.ERET on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
55. **[07-15 01:25]** Re: [PATCH v2 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor
 HFGITR_EL2.ERET on ERET fast path
   - 发件人: Oliver Upton <oupton@kernel.org>
56. **[07-17 17:44]** Re: [PATCH v2 03/28] KVM: arm64: Merge guest's HCRX_EL2 using
 NV_HCRX_GUEST_EXCLUDE
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
57. **[07-17 17:44]** Re: [PATCH v2 06/28] KVM: arm64: Classify CPTR_EL2 as a
 SR_LOC_SPECIAL register
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>

---

### Thread 3: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5

**📧 邮件数**: 56 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 9 Jul 2026 18:40:20 +0800

#### 🤖 AI 总结

本邮件线程讨论了支持 ARMv9.5 引入的 HDBSS（硬件脏页状态跟踪结构）特性的一系列补丁。补丁的主要目的是通过硬件支持来提高脏页跟踪的效率，减少扫描脏页的开销。

在历史讨论中，Tian Zheng 提出了六个补丁，涵盖了 HDBSS 的基础设施、每个虚拟 CPU 的缓冲管理、故障处理以及脏日志变化时 HDBSS 的启用/禁用等功能。补丁中提到的 DBM（脏位修改器）属性允许硬件自动将写入干净的页面标记为脏，以避免因缺少写权限而导致的陷阱。

本周的新讨论中，参与者们对补丁进行了深入的审查和讨论。Leonardo Bras 提出了对 HDBSS 启用的不同策略建议，强调了在用户启用急切拆分时应使用不同的 DBM 行为。此外，讨论中还提到 HDBSS 缓冲区的大小应与脏环缓冲区匹配，以避免在两者都满时的复杂情况。Tian Zheng 也同意将 HDBSS 缓冲区大小设置为 512 条目，并不建议向用户空间暴露配置接口，以避免混淆。

总体而言，邮件讨论集中在如何优化 HDBSS 的实现及其与现有脏页跟踪机制的兼容性，确保在不同使用场景下的有效性和性能。

#### 📝 邮件列表

1. **[07-09 18:40]** [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
2. **[07-09 18:40]** [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[07-09 18:40]** [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
4. **[07-09 18:40]** [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
5. **[07-09 18:40]** [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
6. **[07-13 11:31]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-13 12:17]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[07-13 14:39]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[07-13 15:06]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[07-13 15:50]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-13 17:27]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[07-14 09:14]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
13. **[07-14 15:15]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
14. **[07-14 08:23]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-14 15:38]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
16. **[07-14 15:44]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
17. **[07-14 16:58]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty
 logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
18. **[07-14 17:37]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
19. **[07-14 11:19]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
20. **[07-14 11:20]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
21. **[07-14 18:39]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
22. **[07-14 11:47]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Leonardo Bras <leo.bras@arm.com>
23. **[07-14 11:50]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
24. **[07-14 12:16]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Leonardo Bras <leo.bras@arm.com>
25. **[07-14 12:20]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
26. **[07-14 12:59]** [PATCH v4 0/6] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
27. **[07-14 12:59]** [PATCH v4 1/6] KVM: arm64: Use a variable for the canonical GPA in kvm_s2_fault_map()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
28. **[07-14 12:59]** [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
29. **[07-14 12:59]** [PATCH v4 3/6] KVM: arm64: nv: Add nested revmap broken tracepoint
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
30. **[07-14 12:59]** [PATCH v4 4/6] KVM: arm64: Refactor kvm_unmap_gfn_range() with common variables
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
31. **[07-14 12:59]** [PATCH v4 5/6] KVM: arm64: nv: Remove reverse map entries during TLBI handling
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
32. **[07-14 12:59]** [PATCH v4 6/6] KVM: arm64: nv: Create nested IPA direct map to speed up reverse map removal
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
33. **[07-14 21:27]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
34. **[07-14 21:29]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
35. **[07-14 21:34]** Re: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
36. **[07-14 15:19]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
37. **[07-14 15:33]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Leonardo Bras <leo.bras@arm.com>
38. **[07-15 17:16]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
39. **[07-15 15:28]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Leonardo Bras <leo.bras@arm.com>
40. **[07-15 23:45]** Re: [PATCH v4 3/6] KVM: arm64: nv: Add nested revmap broken
 tracepoint
   - 发件人: Oliver Upton <oupton@kernel.org>
41. **[07-16 00:05]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Oliver Upton <oupton@kernel.org>
42. **[07-16 15:15]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty
 logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
43. **[07-16 00:39]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Oliver Upton <oupton@kernel.org>
44. **[07-16 16:37]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty
 logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
45. **[07-16 09:56]** Re: [PATCH v4 3/6] KVM: arm64: nv: Add nested revmap broken tracepoint
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[07-16 17:14]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
47. **[07-16 17:25]** Re: [PATCH v4 3/6] KVM: arm64: nv: Add nested revmap broken
 tracepoint
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
48. **[07-16 10:16]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Oliver Upton <oupton@kernel.org>
49. **[07-17 11:58]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
50. **[07-17 12:06]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
51. **[07-17 14:51]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
52. **[07-17 15:23]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty
 logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
53. **[07-17 16:21]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
54. **[07-17 16:44]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
55. **[07-17 16:50]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Leonardo Bras <leo.bras@arm.com>
56. **[07-17 16:53]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 4: [PATCH v2 00/18] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 43 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 18:53:57 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM 的 arm64 架构中引入 pKVM 超级管理程序的堆分配器的补丁系列（PATCH v2 00/18）。该补丁旨在解决 pKVM 之前缺乏动态内存分配器的问题，导致超管的内存使用受到主机限制，影响了虚拟机的可扩展性。补丁系列中引入了一个动态映射的自定义堆分配器（hyp_allocator），并为其提供了一系列支持功能。

在历史讨论中，Vincent Donnefort 提出了多个补丁，逐步构建了堆分配器所需的基础设施，包括地址映射、内存回收接口和自测试功能等。这些补丁的主要目标是将超管的内存管理从主机转移到超管自身，从而提高内存的灵活性和效率。

在本周的新讨论中，参与者 Fuad Tabba 对多个补丁进行了审查并提出了改进建议，包括函数命名、补丁消息的清晰度以及潜在的性能问题等。他建议在某些补丁中增加对威胁模型的描述，并讨论了内存对齐和内存回收的相关问题。总体来看，本周的讨论集中在对补丁的细节审查和优化建议上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[07-06 18:53]** [PATCH v2 00/18] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-06 18:53]** [PATCH v2 01/18] KVM: arm64: Add __pkvm_private_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-06 18:53]** [PATCH v2 02/18] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-06 18:54]** [PATCH v2 03/18] KVM: arm64: Add __hyp_allocator_map for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-06 18:54]** [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-06 18:54]** [PATCH v2 05/18] KVM: arm64: Allow kvm_hyp_memcache usage outside of stage-2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[07-06 18:54]** [PATCH v2 06/18] KVM: arm64: Add topup interface for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-06 18:54]** [PATCH v2 07/18] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[07-06 18:54]** [PATCH v2 08/18] KVM: arm64: Handle PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[07-06 18:54]** [PATCH v2 09/18] KVM: arm64: Add reclaim interface for the pKVM heap alloc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-06 18:54]** [PATCH v2 10/18] KVM: arm64: Add selftests for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[07-06 18:54]** [PATCH v2 11/18] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[07-06 18:54]** [PATCH v2 12/18] KVM: arm64: Filter out non-kernel addresses in kern_hyp_va
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[07-06 18:54]** [PATCH v2 13/18] KVM: arm64: Move hyp_vm refcount into the structure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[07-06 18:54]** [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in __pkvm_init_vm
 error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[07-06 18:54]** [PATCH v2 15/18] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[07-06 18:54]** [PATCH v2 16/18] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[07-06 18:54]** [PATCH v2 17/18] KVM: arm64: Reject hyp trace descriptors with fewer
 CPUs than hyp_nr_cpus
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[07-06 18:54]** [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
20. **[07-14 17:59]** Re: [PATCH v2 01/18] KVM: arm64: Add __pkvm_private_range_pa
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
21. **[07-14 18:48]** Re: [PATCH v2 02/18] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
22. **[07-14 18:53]** Re: [PATCH v2 03/18] KVM: arm64: Add __hyp_allocator_map for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
23. **[07-14 19:35]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
24. **[07-14 20:00]** Re: [PATCH v2 05/18] KVM: arm64: Allow kvm_hyp_memcache usage outside
 of stage-2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
25. **[07-14 20:28]** Re: [PATCH v2 06/18] KVM: arm64: Add topup interface for the pKVM
 heap allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
26. **[07-14 20:45]** Re: [PATCH v2 07/18] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
27. **[07-14 21:10]** Re: [PATCH v2 09/18] KVM: arm64: Add reclaim interface for the pKVM
 heap alloc
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
28. **[07-15 07:28]** Re: [PATCH v2 08/18] KVM: arm64: Handle PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
29. **[07-15 09:58]** Re: [PATCH v2 03/18] KVM: arm64: Add __hyp_allocator_map for the
 pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
30. **[07-15 10:24]** Re: [PATCH v2 03/18] KVM: arm64: Add __hyp_allocator_map for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
31. **[07-15 11:59]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
32. **[07-15 12:07]** Re: [PATCH v2 10/18] KVM: arm64: Add selftests for the pKVM heap allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
33. **[07-15 12:20]** Re: [PATCH v2 11/18] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[07-15 12:30]** Re: [PATCH v2 12/18] KVM: arm64: Filter out non-kernel addresses in kern_hyp_va
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
35. **[07-15 12:35]** Re: [PATCH v2 13/18] KVM: arm64: Move hyp_vm refcount into the structure
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
36. **[07-15 12:35]** Re: [PATCH v2 11/18] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
37. **[07-15 13:09]** Re: [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in
 __pkvm_init_vm error path
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[07-15 13:33]** Re: [PATCH v2 15/18] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
39. **[07-15 13:55]** Re: [PATCH v2 15/18] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap
 allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
40. **[07-15 13:58]** Re: [PATCH v2 15/18] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
41. **[07-15 14:12]** Re: [PATCH v2 16/18] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM heap allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
42. **[07-15 14:54]** Re: [PATCH v2 17/18] KVM: arm64: Reject hyp trace descriptors with
 fewer CPUs than hyp_nr_cpus
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
43. **[07-15 16:07]** Re: [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM
 hyp allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 5: [PATCH v13 00/32] KVM: arm64: Implement support for SME

**📧 邮件数**: 33 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 20 Jul 2026 00:07:27 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现对 SME（Scalable Matrix Extension）的支持，主要内容如下：

1. **原始 Patch/问题内容**：
   本次讨论的补丁系列（PATCH v13 00/32）旨在为 KVM 的 arm64 实现 SME 的支持，涉及到新的向量长度、控制寄存器及其与 SVE（Scalable Vector Extension）的交互。

2. **之前讨论要点**：
   在历史讨论中，参与者提到 SME 的实现与 SVE 有许多相似之处，但 SME 引入了新的向量长度和控制机制。补丁中还提到，SME 的支持仅限于非保护模式的 KVM 客户端，并且在实现中需要考虑到 SVE 和 SME 的寄存器访问冲突。

3. **本周的新讨论、进展或结论**：
   本周的讨论集中在补丁的具体实现上，包括对 SME 控制寄存器的支持、用户空间对 ZA 和 ZT0 寄存器的访问、以及如何在 KVM 中处理 SME 异常。此外，补丁还增加了对 SME 状态的上下文切换支持，并确保在嵌套虚拟机中也能正确处理 SME。参与者一致认为，SME 的实现需要与 SVE 的实现相协调，以避免复杂性和潜在的错误。

总的来说，本周的讨论和补丁更新为 KVM 在 arm64 上支持 SME 提供了重要的技术细节和实现方向，确保了与现有 SVE 功能的兼容性。

#### 📝 邮件列表

1. **[07-20 00:07]** [PATCH v13 00/32] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-20 00:07]** [PATCH v13 01/32] arm64/sysreg: Define full value
 read/modify/write helpers
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-20 00:07]** [PATCH v13 02/32] arm64/fpsimd: Ensure all of ZCR_EL1 is
 initialised from idle
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-20 00:07]** [PATCH v13 03/32] arm64/fpsimd: Configure all ZCR/SMCR bits when
 loading task state
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-20 00:07]** [PATCH v13 04/32] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-20 00:07]** [PATCH v13 05/32] arm64/sve: Factor virtualizable VL discovery out
 of SVE specific code
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[07-20 00:07]** [PATCH v13 06/32] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[07-20 00:07]** [PATCH v13 07/32] KVM: arm64: Remove bitrotted comment on
 handle_sve()
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[07-20 00:07]** [PATCH v13 08/32] KVM: arm64: Handle FEAT_IDST for guest accesses
 to hidden registers
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-20 00:07]** [PATCH v13 09/32] KVM: arm64: Pull ctxt_has_ helpers to start of
 sysreg-sr.h
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[07-20 00:07]** [PATCH v13 10/32] KVM: arm64: Rename SVE finalization constants to
 be more general
   - 发件人: Mark Brown <broonie@kernel.org>
12. **[07-20 00:07]** [PATCH v13 11/32] KVM: arm64: Remove special case for FP state
 loading from ZCR_EL2 traps
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[07-20 00:07]** [PATCH v13 12/32] KVM: arm64: Define internal features for SME
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[07-20 00:07]** [PATCH v13 13/32] KVM: arm64: Rename sve_state_reg_region
   - 发件人: Mark Brown <broonie@kernel.org>
15. **[07-20 00:07]** [PATCH v13 14/32] KVM: arm64: Store vector lengths in an array
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[07-20 00:07]** [PATCH v13 15/32] KVM: arm64: Factor SVE code out of
 fpsimd_lazy_switch_to_host()
   - 发件人: Mark Brown <broonie@kernel.org>
17. **[07-20 00:07]** [PATCH v13 16/32] KVM: arm64: Document the KVM ABI for SME
   - 发件人: Mark Brown <broonie@kernel.org>
18. **[07-20 00:07]** [PATCH v13 17/32] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Mark Brown <broonie@kernel.org>
19. **[07-20 00:07]** [PATCH v13 18/32] KVM: arm64: Support SME control registers
   - 发件人: Mark Brown <broonie@kernel.org>
20. **[07-20 00:07]** [PATCH v13 19/32] KVM: arm64: Support TPIDR2_EL0
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[07-20 00:07]** [PATCH v13 20/32] KVM: arm64: Support SME identification registers
 for guests
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[07-20 00:07]** [PATCH v13 21/32] KVM: arm64: Support SME priority registers
   - 发件人: Mark Brown <broonie@kernel.org>
23. **[07-20 00:07]** [PATCH v13 22/32] KVM: arm64: Support userspace access to
 streaming mode Z and P registers
   - 发件人: Mark Brown <broonie@kernel.org>
24. **[07-20 00:07]** [PATCH v13 23/32] KVM: arm64: Flush register state on writes to
 SVCR.SM and SVCR.ZA
   - 发件人: Mark Brown <broonie@kernel.org>
25. **[07-20 00:07]** [PATCH v13 24/32] KVM: arm64: Expose SME specific state to
 userspace
   - 发件人: Mark Brown <broonie@kernel.org>
26. **[07-20 00:07]** [PATCH v13 25/32] KVM: arm64: Context switch SME state for guests
   - 发件人: Mark Brown <broonie@kernel.org>
27. **[07-20 00:07]** [PATCH v13 26/32] KVM: arm64: Handle SME exceptions
   - 发件人: Mark Brown <broonie@kernel.org>
28. **[07-20 00:07]** [PATCH v13 27/32] KVM: arm64: Expose SME to nested guests
   - 发件人: Mark Brown <broonie@kernel.org>
29. **[07-20 00:07]** [PATCH v13 28/32] KVM: arm64: Provide interface for configuring
 and enabling SME for guests
   - 发件人: Mark Brown <broonie@kernel.org>
30. **[07-20 00:07]** [PATCH v13 29/32] KVM: arm64: selftests: Remove spurious check for
 single bit safe values
   - 发件人: Mark Brown <broonie@kernel.org>
31. **[07-20 00:07]** [PATCH v13 30/32] KVM: arm64: selftests: Skip impossible invalid
 value tests
   - 发件人: Mark Brown <broonie@kernel.org>
32. **[07-20 00:07]** [PATCH v13 31/32] KVM: arm64: selftests: Add SME system registers
 to get-reg-list
   - 发件人: Mark Brown <broonie@kernel.org>
33. **[07-20 00:07]** [PATCH v13 32/32] KVM: arm64: selftests: Add SME to set_id_regs
 test
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 6: [PATCH v7 00/24] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 32 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Jul 2026 11:58:41 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 ARM64 SMMUv3 驱动的多个补丁，主要集中在 pKVM 的实现和功能扩展上。

1. **原始补丁内容**：补丁系列的主要目标是为 KVM 提供 SMMUv3 支持，允许在受保护的虚拟机中实现 DMA 隔离。补丁包括对 SMMU 命令队列（CMDQ）和流表（STE）的仿真，以及对 MMIO 空间的处理。

2. **历史讨论要点**：之前的讨论主要集中在如何设计和实现 SMMUv3 驱动，以确保在虚拟化环境中能够有效地处理设备的内存访问。参与者们讨论了如何通过命令队列和流表的仿真来实现 DMA 隔离，并确保这些操作不会被宿主机绕过。

3. **本周的新讨论和进展**：本周的讨论包括多个补丁的提交和修改，主要包括：
   - 为 SMMU 添加了 MMIO 仿真和 CMDQ 功能，确保宿主机对命令队列的访问受到限制。
   - 讨论了如何在 SMMU 启用和禁用时共享和取消共享其他队列（如 PRIQ 和 EVTQ）。
   - 引入了对流表的仿真，确保在宿主机发送 CFGI_STE 命令时能够正确更新影子流表。
   - 讨论了如何在 KVM 中实现 IOMMU 的支持，包括对 io-pgtable-arm 的集成。

总的来说，本周的讨论和补丁提交进一步增强了 KVM 对 ARM64 SMMUv3 的支持，确保了在受保护的虚拟机中实现 DMA 隔离的能力。

#### 📝 邮件列表

1. **[07-15 11:58]** [PATCH v7 00/24] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-15 11:58]** [PATCH v7 01/24] KVM: arm64: Add a generic clock
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-15 11:58]** [PATCH v7 02/24] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-15 11:58]** [PATCH v7 03/24] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[07-15 11:58]** [PATCH v7 04/24] iommu/arm-smmu-v3: Move TLB range invalidation into
 common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[07-15 11:58]** [PATCH v7 05/24] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[07-15 11:58]** [PATCH v7 06/24] KVM: arm64: iommu: Introduce IOMMU driver infrastructure
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[07-15 11:58]** [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[07-15 11:58]** [PATCH v7 08/24] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>
10. **[07-15 11:58]** [PATCH v7 09/24] KVM: arm64: iommu: Support DABT for IOMMU
   - 发件人: Mostafa Saleh <smostafa@google.com>
11. **[07-15 11:58]** [PATCH v7 10/24] iommu/arm-smmu-v3-kvm: Add SMMUv3 driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[07-15 11:58]** [PATCH v7 11/24] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
13. **[07-15 11:58]** [PATCH v7 12/24] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
14. **[07-15 11:58]** [PATCH v7 13/24] iommu/arm-smmu-v3-kvm: Add MMIO emulation
   - 发件人: Mostafa Saleh <smostafa@google.com>
15. **[07-15 11:58]** [PATCH v7 14/24] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
16. **[07-15 11:58]** [PATCH v7 15/24] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[07-15 11:58]** [PATCH v7 16/24] iommu/arm-smmu-v3-kvm: Emulate CMDQ for host
   - 发件人: Mostafa Saleh <smostafa@google.com>
18. **[07-15 11:58]** [PATCH v7 17/24] iommu/arm-smmu-v3-kvm: Shadow stream table
   - 发件人: Mostafa Saleh <smostafa@google.com>
19. **[07-15 11:58]** [PATCH v7 18/24] iommu/arm-smmu-v3-kvm: Shadow STEs
   - 发件人: Mostafa Saleh <smostafa@google.com>
20. **[07-15 11:59]** [PATCH v7 19/24] iommu/arm-smmu-v3-kvm: Share other queues
   - 发件人: Mostafa Saleh <smostafa@google.com>
21. **[07-15 11:59]** [PATCH v7 20/24] iommu/arm-smmu-v3-kvm: Emulate GBPA
   - 发件人: Mostafa Saleh <smostafa@google.com>
22. **[07-15 11:59]** [PATCH v7 21/24] iommu/io-pgtable-arm: Support io-pgtable-arm in the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
23. **[07-15 11:59]** [PATCH v7 22/24] iommu/arm-smmu-v3-kvm: Shadow the CPU stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
24. **[07-15 11:59]** [PATCH v7 23/24] iommu/arm-smmu-v3-kvm: Enable nesting
   - 发件人: Mostafa Saleh <smostafa@google.com>
25. **[07-15 11:59]** [PATCH v7 24/24] KVM: arm64: Add documentation for pKVM DMA isolation
   - 发件人: Mostafa Saleh <smostafa@google.com>
26. **[07-15 14:48]** Re: [PATCH v7 01/24] KVM: arm64: Add a generic clock
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
27. **[07-15 14:13]** Re: [PATCH v7 01/24] KVM: arm64: Add a generic clock
   - 发件人: Mostafa Saleh <smostafa@google.com>
28. **[07-15 15:34]** Re: [PATCH v7 01/24] KVM: arm64: Add a generic clock
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
29. **[07-15 18:26]** Re: [PATCH v7 02/24] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
30. **[07-15 18:56]** Re: [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
31. **[07-15 18:28]** Re: [PATCH v7 02/24] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
32. **[07-15 18:43]** Re: [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 7: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 31 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 3 Jul 2026 15:50:32 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于为 KVM（Kernel-based Virtual Machine）在 arm64 架构上添加 GICv5 IRS（Interrupt Routing System）支持的补丁系列。

**原始补丁内容**：
Sascha Bischoff 提出的补丁系列旨在扩展 KVM 对 GICv5 的支持，允许 GICv5 客户机使用 SPIs（共享中断）和 LPIs（本地中断），从而不再局限于 PPIs（私有中断）。该系列补丁使得在 Arm FVP 模型上启动完整的 Linux 客户机成为可能。

**之前讨论要点**：
在历史讨论中，参与者探讨了 GICv5 中断状态的管理、SPI 注入的支持以及相关文档的更新。特别提到需要跟踪 SPI 状态以确保中断的正确处理，并讨论了如何在 GICv5 中实现 SPI 的生命周期管理。此外，文档更新也强调了 IRS MMIO（内存映射输入输出）区域的要求。

**本周新讨论与进展**：
本周的讨论主要集中在对补丁的进一步修改和问题的解决上。Sascha 表示将暂时放弃某些用户空间通知支持，并讨论了如何优化 SPI 状态跟踪的实现。此外，针对文档的更新，Sascha 详细说明了 GICv5 IRS 地址属性及其 GPA 布局要求，并对相关文档进行了清理和补充。整体来看，本周的讨论强调了对补丁的细节调整和文档准确性的提升。

#### 📝 邮件列表

1. **[07-03 15:50]** [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[07-03 16:04]** [PATCH v3 27/40] KVM: arm64: gic-v5: Track SPI state for in-flight
 SPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[07-03 16:05]** [PATCH v3 29/40] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[07-03 16:05]** [PATCH v3 30/40] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[07-03 16:06]** [PATCH v3 31/40] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-03 16:07]** [PATCH v3 34/40] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[07-03 16:08]** [PATCH v3 35/40] KVM: arm64: gic-v5: Add CoreSight MMIO regs to IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-03 16:08]** [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[07-03 16:09]** [PATCH v3 37/40] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[07-03 16:09]** [PATCH v3 38/40] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[07-03 16:10]** [PATCH v3 40/40] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[07-03 16:27]** Re: [PATCH v3 30/40] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: sashiko-bot@kernel.org
13. **[07-03 16:33]** Re: [PATCH v3 40/40] Documentation: KVM: Add the VGICv5 IRS
 save/restore sequences
   - 发件人: sashiko-bot@kernel.org
14. **[07-03 16:36]** Re: [PATCH v3 31/40] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: sashiko-bot@kernel.org
15. **[07-03 16:36]** Re: [PATCH v3 37/40] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: sashiko-bot@kernel.org
16. **[07-03 16:37]** Re: [PATCH v3 38/40] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: sashiko-bot@kernel.org
17. **[07-03 16:41]** Re: [PATCH v3 35/40] KVM: arm64: gic-v5: Add CoreSight MMIO regs to
 IRS
   - 发件人: sashiko-bot@kernel.org
18. **[07-03 16:41]** Re: [PATCH v3 27/40] KVM: arm64: gic-v5: Track SPI state for
 in-flight SPIs
   - 发件人: sashiko-bot@kernel.org
19. **[07-03 16:42]** Re: [PATCH v3 34/40] KVM: arm64: gic-v5: Handle userspace accesses
 to IRS MMIO region
   - 发件人: sashiko-bot@kernel.org
20. **[07-03 16:43]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: sashiko-bot@kernel.org
21. **[07-03 16:53]** Re: [PATCH v3 29/40] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: sashiko-bot@kernel.org
22. **[07-15 16:02]** Re: [PATCH v3 27/40] KVM: arm64: gic-v5: Track SPI state for
 in-flight SPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[07-15 16:28]** Re: [PATCH v3 29/40] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[07-15 16:28]** Re: [PATCH v3 30/40] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[07-15 16:31]** Re: [PATCH v3 31/40] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[07-15 16:34]** Re: [PATCH v3 35/40] KVM: arm64: gic-v5: Add CoreSight MMIO regs to
 IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[07-15 16:37]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[07-15 16:40]** Re: [PATCH v3 37/40] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[07-15 16:44]** Re: [PATCH v3 38/40] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[07-15 16:46]** Re: [PATCH v3 34/40] KVM: arm64: gic-v5: Handle userspace accesses to
 IRS MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[07-15 16:57]** Re: [PATCH v3 40/40] Documentation: KVM: Add the VGICv5 IRS
 save/restore sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 8: [PATCH v5 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)

**📧 邮件数**: 24 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 14 Jul 2026 11:15:53 +0100

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM (Kernel-based Virtual Machine) 在 arm64 架构下的 pKVM vCPU 状态管理的补丁系列（PATCH v5 0/8）。该系列补丁的主要目的是优化在 EL2（异常级别2）下的 vCPU 状态管理，减少在世界切换时对非保护型客户机状态的重复复制。

**原始补丁/问题内容**：
补丁系列重构了 pKVM 在 EL2 下的 vCPU 状态管理，避免在每次世界切换时复制未保护客户机的状态。补丁包括对系统寄存器访问器的重命名、状态同步的延迟实现，以及对 VGIC（虚拟通用中断控制器）状态的优化。

**之前讨论要点**：
之前的讨论主要集中在如何有效地管理 vCPU 状态，确保在 EL2 下的状态隔离和性能优化。补丁的结构包括准备性重构、vCPU 查找原语的实现以及 VGIC 状态的同步。

**本周的新讨论、进展或结论**：
本周的讨论中，参与者对补丁的各个部分进行了逐一审查，提出了潜在问题和改进建议。补丁的功能性变更被认为是合理的，且得到了多位开发者的认可。特别是对 VGIC 状态的管理和延迟状态同步的实现，得到了积极的反馈。整体而言，补丁系列在优化 pKVM 的 vCPU 状态管理方面取得了显著进展，参与者对后续的实现充满期待。

#### 📝 邮件列表

1. **[07-14 11:15]** [PATCH v5 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-14 11:15]** [PATCH v5 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-14 11:15]** [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-14 11:15]** [PATCH v5 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-14 11:15]** [PATCH v5 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-14 11:15]** [PATCH v5 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-14 11:15]** [PATCH v5 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-14 11:16]** [PATCH v5 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-14 11:16]** [PATCH v5 8/8] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[07-14 10:43]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: sashiko-bot@kernel.org
11. **[07-14 11:52]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[07-14 11:10]** Re: [PATCH v5 4/8] KVM: arm64: Move PSCI helper functions to a
 shared header
   - 发件人: sashiko-bot@kernel.org
13. **[07-14 12:15]** Re: [PATCH v5 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
14. **[07-14 12:19]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[07-14 11:53]** Re: [PATCH v5 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
16. **[07-14 13:17]** Re: [PATCH v5 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[07-14 12:20]** Re: [PATCH v5 7/8] KVM: arm64: Add primitives to flush/sync the
 VGIC state at EL2
   - 发件人: sashiko-bot@kernel.org
18. **[07-14 12:33]** Re: [PATCH v5 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
19. **[07-14 14:04]** Re: [PATCH v5 7/8] KVM: arm64: Add primitives to flush/sync the VGIC
 state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[07-14 14:08]** Re: [PATCH v5 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
21. **[07-14 16:19]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[07-14 16:32]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
23. **[07-14 17:39]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[07-14 17:44]** Re: [PATCH v5 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 9: [PATCH v6 16/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions

**📧 邮件数**: 20 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 10 Jul 2026 17:01:07 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 ARM SMMU v3 和 KVM 的补丁（PATCH v6 16/25），主要是添加 CMDQ 功能。

**原始补丁内容**：该补丁旨在增强 KVM 的 IOMMU 驱动，具体是为 ARM SMMU v3 添加 CMDQ 函数，以支持更高效的命令队列处理。

**历史讨论要点**：在之前的讨论中，参与者提出了对补丁的多个改进建议，包括对函数参数的命名、超时设置的优化，以及对 IOMMU 驱动的文档化需求等。讨论中还涉及了如何在 hypervisor 代码中更清晰地管理 DMA 隔离等问题。

**本周的新讨论与进展**：本周的讨论主要集中在补丁的具体实现细节上。Mostafa Saleh 和 Vincent Donnefort 就补丁中的具体函数调用、内存管理和 IOMMU 初始化顺序等问题进行了深入交流。Mostafa 表示将根据反馈进行修改，包括移除不必要的跟踪时钟支持，并处理可能的溢出问题。此外，双方还探讨了如何更好地将 IOMMU 逻辑与 KVM 的核心逻辑解耦，以提高代码的可维护性和清晰度。

总体而言，本周的讨论推动了补丁的进一步完善，参与者对补丁的方向达成了一致，预计将在后续版本中实施这些改进。

#### 📝 邮件列表

1. **[07-10 17:01]** Re: [PATCH v6 16/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-10 17:17]** Re: [PATCH v6 07/25] KVM: arm64: iommu: Introduce IOMMU driver
 infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-10 17:33]** Re: [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-13 10:13]** Re: [PATCH v6 07/25] KVM: arm64: iommu: Introduce IOMMU driver
 infrastructure
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[07-13 10:35]** Re: [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[07-13 11:07]** Re: [PATCH v6 16/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[07-13 14:24]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-13 14:00]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[07-13 16:14]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[07-13 16:27]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-13 15:51]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[07-13 15:58]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
13. **[07-13 17:03]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[07-13 18:19]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
15. **[07-14 09:16]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[07-14 08:29]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[07-14 09:43]** Re: [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[07-14 09:47]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[07-14 08:56]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
20. **[07-14 09:01]** Re: [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 10: [PATCH v12 00/29] KVM: arm64: Implement support for SME

**📧 邮件数**: 18 | **👥 参与者**: 4 | **📅 开始时间**: Thu, 09 Jul 2026 19:27:21 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在 KVM（内核虚拟机）中实现对 SME（Scalable Matrix Extension）的支持，涉及到多个补丁（patch）的提交和讨论。

1. **原始补丁内容**：Mark Brown 提交的补丁系列（[PATCH v12 00/29]）旨在为 arm64 架构的 KVM 实现对 SME 的支持，主要关注用户空间 ABI、SVE（Scalable Vector Extension）寄存器的访问以及 SME 状态的上下文切换等问题。

2. **之前的讨论要点**：历史讨论中，参与者们对补丁的具体实现进行了深入探讨，包括如何动态配置 FA64 和 ZT0 寄存器、在 KVM 客户端中切换 SME 状态的必要性，以及如何优化代码以避免不必要的寄存器写入。Fuad Tabba 和 Mark Brown 之间的交流也涉及到对补丁逻辑的审查和建议。

3. **本周的新讨论与进展**：本周的讨论中，参与者们提出了对补丁描述的改进建议，强调了测试寄存器接口的重要性，并讨论了在返回用户空间时寄存器的重置问题。Mark Rutland 提出了潜在的错误和代码改进建议，尤其是关于 ZCR_ELx 寄存器的处理。参与者们一致认为在优化代码时应保持简单性，避免引入复杂性，确保稳定性。

总体来看，本周的讨论集中在对补丁的细节审查和改进建议上，参与者们关注代码的清晰性和稳定性，以确保 SME 在 KVM 中的有效实现。

#### 📝 邮件列表

1. **[07-09 19:27]** [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-09 19:27]** [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-09 19:27]** [PATCH v12 04/29] arm64/sve: Factor virtualizable VL discovery out
 of SVE specific code
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-09 19:27]** [PATCH v12 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-12 15:03]** Re: [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-12 15:12]** Re: [PATCH v12 04/29] arm64/sve: Factor virtualizable VL discovery
 out of SVE specific code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-12 15:40]** Re: [PATCH v12 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-13 13:07]** Re: [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[07-13 13:53]** Re: [PATCH v12 04/29] arm64/sve: Factor virtualizable VL discovery
 out of SVE specific code
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-13 14:30]** Re: [PATCH v12 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[07-16 11:52]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[07-16 16:28]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[07-18 01:35]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[07-18 14:30]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[07-18 15:24]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[07-19 09:35]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when loading SME state
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-19 13:40]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
18. **[07-19 13:59]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 11: [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support

**📧 邮件数**: 18 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Jul 2026 15:27:31 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于在 Linux 内核中添加对 Arm Realm Management Monitor (RMM) v2.0 支持的补丁系列，共包含六个补丁。补丁的主要内容包括实现与 RMM 的通用固件层交互，支持状态性 RMI 操作（SRO），以及配置 RMM 的主机页面大小等功能。

在历史讨论中，补丁的背景是为了支持 Arm CCA 主机，之前的讨论集中在如何将 RMM 支持与 KVM 的支持分开，以便于其他工作能够在不依赖 KVM 的情况下进行。

本周的新讨论中，Steven Price 提出了补丁的具体实现，包括：
1. **补丁内容**：添加了 RMM 的 SMC 定义、直接调用的包装函数、初始化时的 RMI 支持检查、主机页面大小配置、SRO 支持等。
2. **新进展**：补丁经过了 Sashiko AI 的审查，提出了一些潜在问题，包括结构体中的隐式填充、未初始化的堆栈变量读取等。Steven 对这些问题进行了回应，并表示将进行相应的修正。

总体来看，本周的讨论强调了补丁的实现细节和潜在问题的修复，确保 RMM 的支持能够顺利集成到 Linux 内核中。

#### 📝 邮件列表

1. **[07-15 15:27]** [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:27]** [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling the RMM
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-15 15:27]** [PATCH 2/6] firmware: arm_rmm: Add wrappers for direct RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
4. **[07-15 15:27]** [PATCH 3/6] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
5. **[07-15 15:27]** [PATCH 4/6] firmware: arm_rmm: Configure the RMM with the host's page size
   - 发件人: Steven Price <steven.price@arm.com>
6. **[07-15 15:27]** [PATCH 5/6] firmware: arm_rmm: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
7. **[07-15 15:27]** [PATCH 6/6] firmware: arm_rmm: Ensure the RMM has GPT entries for memory
   - 发件人: Steven Price <steven.price@arm.com>
8. **[07-15 14:38]** Re: [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling
 the RMM
   - 发件人: sashiko-bot@kernel.org
9. **[07-15 14:49]** Re: [PATCH 2/6] firmware: arm_rmm: Add wrappers for direct RMI
 calls
   - 发件人: sashiko-bot@kernel.org
10. **[07-15 15:06]** Re: [PATCH 3/6] firmware: arm_rmm: Check for RMI support at init
   - 发件人: sashiko-bot@kernel.org
11. **[07-15 15:18]** Re: [PATCH 4/6] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: sashiko-bot@kernel.org
12. **[07-15 15:29]** Re: [PATCH 5/6] firmware: arm_rmm: Add support for SRO
   - 发件人: sashiko-bot@kernel.org
13. **[07-15 15:47]** Re: [PATCH 6/6] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: sashiko-bot@kernel.org
14. **[07-16 11:59]** Re: [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling
 the RMM
   - 发件人: Steven Price <steven.price@arm.com>
15. **[07-16 15:28]** Re: [PATCH 2/6] firmware: arm_rmm: Add wrappers for direct RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
16. **[07-16 15:28]** Re: [PATCH 3/6] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
17. **[07-16 16:41]** Re: [PATCH 4/6] firmware: arm_rmm: Configure the RMM with the host's
 page size
   - 发件人: Steven Price <steven.price@arm.com>
18. **[07-16 17:04]** Re: [PATCH 5/6] firmware: arm_rmm: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 12: [PATCH v6 0/8] KVM: arm64: pKVM vCPU state management at EL2

**📧 邮件数**: 16 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 09:12:30 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM（Protected KVM）vCPU 状态管理的补丁系列（PATCH v6 0/8）。该系列补丁旨在优化 vCPU 状态在主机与 EL2（异常级别 2）之间的传递，减少每次世界切换时对非保护虚拟机状态的复制。

**原始补丁内容**：
补丁系列的核心是重构 pKVM 的 vCPU 状态管理，主要包括：
1. 提供 vCPU 查找帮助函数。
2. 实现 VGIC（虚拟通用中断控制器）状态的同步与刷新。
3. 对非保护虚拟机的寄存器状态实现延迟复制，只有在主机需要时才进行状态同步。

**之前讨论要点**：
在之前的讨论中，参与者们对 vCPU 状态管理的现有实现进行了评估，指出了在每次切换时复制状态的性能问题，并提出了通过延迟同步来优化的建议。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现上，包括：
1. 对 vCPU 重置帮助函数的提取和重用。
2. 对 VGIC 状态的处理进行了优化，以减少 EL2 对主机 VGIC 状态的直接引用。
3. 实现了 lazy vCPU 状态同步，确保只有在主机需要时才将状态从 EL2 复制回主机。
4. 参与者们对补丁进行了评审，提出了一些潜在问题和改进建议。

整体来看，这一系列补丁的目标是提升 KVM 在处理保护虚拟机时的性能和安全性，同时确保系统的稳定性。

#### 📝 邮件列表

1. **[07-15 09:12]** [PATCH v6 0/8] KVM: arm64: pKVM vCPU state management at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-15 09:12]** [PATCH v6 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-15 09:12]** [PATCH v6 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-15 09:12]** [PATCH v6 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-15 09:12]** [PATCH v6 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-15 09:12]** [PATCH v6 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-15 09:12]** [PATCH v6 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-15 09:12]** [PATCH v6 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-15 09:12]** [PATCH v6 8/8] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[07-15 08:24]** Re: [PATCH v6 4/8] KVM: arm64: Move PSCI helper functions to a
 shared header
   - 发件人: sashiko-bot@kernel.org
11. **[07-15 09:28]** Re: [PATCH v6 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[07-15 08:34]** Re: [PATCH v6 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
13. **[07-15 08:37]** Re: [PATCH v6 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
14. **[07-15 10:18]** Re: [PATCH v6 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[07-15 10:20]** Re: [PATCH v6 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
16. **[07-17 14:43]** Re: [PATCH v6 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 13: [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 16 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  6 Jul 2026 10:52:00 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（内核虚拟机）的补丁系列，主要涉及在 s390 架构中引入 arm64 KVM 的实现。补丁的核心内容是通过在构建时提取 arm64 的相关定义和实现，来实现 s390 和 arm64 之间的代码和头文件共享，从而减少对现有 arm64 代码的修改。

在历史讨论中，参与者 Steffen Eiden 提出了多个补丁，涉及共享头文件、访问 vcpu_gp_regs 结构体的元素、为第二个 KVM 模块做准备以及实现 vCPU IOCTLs 等。Marc Zyngier 对某些补丁提出了分割和重组的建议，以减少代码复杂性和提高可读性，强调了文档化的重要性。

在本周的新讨论中，Marc Zyngier 和 Steffen Eiden 继续探讨了补丁的具体实现细节，特别是关于异常处理和代码一致性的问题。Claudio Imbrenda 对补丁中“几乎重命名”的做法表示不满，建议在提交补丁时先进行必要的宏修改，以便后续的代码移动更为清晰。整体来看，讨论集中在如何优化补丁的结构和确保代码的清晰性与一致性。

#### 📝 邮件列表

1. **[07-06 10:52]** [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[07-06 10:52]** [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[07-06 10:52]** [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[07-06 10:52]** [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[07-06 10:52]** [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[07-06 18:44]** Re: [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-06 22:22]** Re: [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-08 11:44]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-10 11:54]** Re: [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[07-10 13:56]** Re: [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs
 individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[07-10 16:07]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[07-13 16:33]** Re: [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-13 16:42]** Re: [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[07-13 16:46]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-13 18:38]** Re: [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM
 module
   - 发件人: Claudio Imbrenda <imbrenda@linux.ibm.com>
16. **[07-14 12:40]** Re: [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM
 module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 14: [PATCH] KVM: arm64: Avoid naming collision in tracing

**📧 邮件数**: 12 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 12 Jul 2026 15:38:35 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在避免跟踪功能中的命名冲突。最初的补丁由 Mostafa Saleh 提出，指出在禁用超监视器跟踪（CONFIG_NVHE_EL2_TRACING）时，trace_clock() 函数的静态内联存根与在 linux/trace_clock.h 中已经声明的 extern 函数发生冲突，导致编译错误。

在历史讨论中，参与者 Fuad Tabba 对补丁的重命名提出了建议，并确认了补丁的修改是全面且正确的。讨论中还提到了一些小问题，如补丁标题的格式。

在本周的新讨论中，Vincent Donnefort 表达了对无法重现该问题的困惑，并询问了对方的配置文件情况。随后，Mostafa 提出了可能的函数重命名方案，建议使用 trace_hyp_clock() 和 trace_hyp_clock_update() 来避免命名冲突。最终，Vincent 同意了这个建议，并表示将重新提交补丁，同时对补丁标题的修改也提出了建议，以更好地区分超监视器跟踪和内核跟踪。

总体来看，本周的讨论集中在补丁的具体实现和命名上，参与者们积极交流，推动了补丁的完善。

#### 📝 邮件列表

1. **[07-12 15:38]** [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-12 17:19]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-12 19:19]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-12 20:30]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-13 09:02]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-13 09:05]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[07-13 09:11]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-13 08:19]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[07-13 08:26]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
10. **[07-13 09:34]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-13 08:40]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[07-13 09:55]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 15: [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 17 Jul 2026 14:03:10 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM（Protected KVM）阶段-2 映射和内存缓存的修复补丁（PATCH v5 0/7）。该补丁主要集中在解决在 pKVM 环境中出现的多个内存管理问题。

**原始问题和补丁内容**：
补丁的主要目标是修复 pKVM 阶段-2 walker 中的几个缺陷，包括非缓存映射的缓存维护、权限故障时的内存缓存补充、以及在特定硬件上进行的全缓存刷新等问题。补丁还引入了自测功能，以确保在处理阶段-2 块转换时不会导致主机崩溃。

**之前的讨论要点**：
在历史讨论中，参与者提到之前版本（v4）中删除了一些重要的修复，导致了真实的错误。Fuad Tabba 在审查 Bradley Morgan 的“映射缓存”系列时，发现了这些问题并重新整合了相关修复。

**本周的新讨论和进展**：
本周的讨论中，Fuad Tabba 提交了补丁的最新版本（v5），并详细说明了每个补丁的修改内容和修复的具体问题。此外，参与者还讨论了潜在的安全问题，例如恶意嵌套（L1）客户机可能导致 KVM 主机崩溃的情况。Marc Zyngier 提出了对当前补丁的看法，认为应更加谨慎地处理权限故障，以避免掩盖潜在的错误。

总体来看，本周的讨论集中在补丁的具体实现和潜在的安全隐患上，强调了在 pKVM 环境中进行内存管理时的复杂性和重要性。

#### 📝 邮件列表

1. **[07-17 14:03]** [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-17 14:03]** [PATCH v5 1/7] KVM: arm64: Skip cache maintenance for non-cacheable pKVM mappings
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-17 14:03]** [PATCH v5 2/7] KVM: arm64: Top up the memcache for pKVM permission faults
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-17 14:03]** [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty logging faults
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-17 14:03]** [PATCH v5 4/7] KVM: arm64: Skip pKVM stage-2 flush when FWB is enabled
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-17 14:03]** [PATCH v5 5/7] KVM: arm64: Don't WARN on pKVM stage-2 map failures
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-17 14:03]** [PATCH v5 6/7] KVM: arm64: Don't advertise eager page splitting under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-17 14:03]** [PATCH v5 7/7] KVM: arm64: selftests: Add stage-2 block transition test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-17 13:15]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: sashiko-bot@kernel.org
10. **[07-17 15:17]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[07-18 09:44]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty logging faults
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 16: [PATCH v3 0/3] Optimize S2 page splitting

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Wed,  8 Jul 2026 14:40:56 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是优化 S2 页分裂的补丁（PATCH v3 0/3）。该补丁的主要目的是通过引入新的遍历标志，跳过某些页表级别，从而提高页分裂的效率。历史讨论中，Leonardo Bras 提出了该补丁的初步想法，指出在遍历页表时可以推断出某些信息，从而避免不必要的遍历，减少性能开销。

在之前的讨论中，Wei-Lin Chang 对补丁中的术语提出了建议，认为“level-$LEVEL”的表述不够清晰，可能会导致混淆。此外，Dev Jain 询问了关于 `force_pte` 参数的具体情况，讨论了其对页表创建的影响。

在本周的新讨论中，Leonardo Bras 针对 `kvm_pgtable_stage2_split()` 函数的实现细节进行了澄清，指出在内存紧张时可能会影响页表的分裂。同时，参与者们继续讨论了补丁中术语的命名问题，达成了一致意见，计划在下一版本中进行改进。整体来看，本周的讨论主要集中在补丁的具体实现和术语的清晰化上。

#### 📝 邮件列表

1. **[07-08 14:40]** [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[07-08 14:40]** [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[07-11 06:53]** Re: [PATCH v3 2/3] KVM: arm64: Introduce
 KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[07-12 20:20]** Re: [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Dev Jain <dev.jain@arm.com>
5. **[07-13 11:08]** Re: [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[07-13 11:14]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-14 06:41]** Re: [PATCH v3 2/3] KVM: arm64: Introduce
 KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[07-14 11:13]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 17: [PATCH v8 00/11] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 10 Jul 2026 20:14:54 +0900

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 系统上使用多个主机 PMU（性能监控单元）的补丁（PATCH v8 00/11）。该补丁旨在解决在异构 arm64 系统中，vCPU（虚拟 CPU）迁移到具有不兼容 PMU 的 pCPU（物理 CPU）时，导致计数器停止增量的问题。当前的解决方法要求 VMM（虚拟机监控器）将 vCPU 固定在共享兼容 PMU 的 pCPU 上，这在实现上较为复杂。

在历史讨论中，Akihiko Odaki 提出了多个补丁，主要集中在序列化用户空间对 MDCR_EL2 的访问，以及实现仅固定计数器的 PMU 模拟。讨论中提到，现有的实现可能会导致用户空间设置的合法值被覆盖。

本周的新讨论中，Oliver Upton 对补丁提出了质疑，认为不应更新 MDCR_EL2.HPMN，以避免覆盖用户空间的合法值，并建议在 KVM_ARM_VCPU_INIT 调用时确保重置值合理。Akihiko Odaki 同意这一观点，并表示将更新补丁以停止在 vCPU 初始化后重写 MDCR_EL2.HPMN，从而消除对用户空间访问的序列化需求。此外，Odaki 放弃了实现仅固定计数器的补丁，认为该更改未能有效覆盖所有不希望支持的边界情况。整体来看，讨论围绕如何更好地处理 PMU 的兼容性和用户空间的访问控制展开。

#### 📝 邮件列表

1. **[07-10 20:14]** [PATCH v8 00/11] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[07-10 20:14]** [PATCH v8 01/11] KVM: arm64: Serialize userspace MDCR_EL2 access
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[07-10 20:15]** [PATCH v8 09/11] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[07-13 00:33]** Re: [PATCH v8 01/11] KVM: arm64: Serialize userspace MDCR_EL2 access
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[07-13 00:41]** Re: [PATCH v8 09/11] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[07-14 06:31]** Re: [PATCH v8 01/11] KVM: arm64: Serialize userspace MDCR_EL2 access
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[07-14 06:50]** Re: [PATCH v8 09/11] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 18: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 17 Jul 2026 13:48:20 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）中添加 VCPU 平面调度状态和辅助功能的补丁（PATCH 35/60）。该补丁旨在增强虚拟化环境中的安全性和调度能力。

在历史讨论中，参与者 Jörg Rödel 提出了将虚拟化基于安全（VSM）的实现尽量移至用户空间，以简化内核的实现并提高 VSM 支持的上游能力。他建议优先考虑更高特权的平面，以便于引入更高的特权级别。

本周的新讨论中，Nicolas Saenz Julienne 和 James Bottomley 继续探讨平面调度的实现细节。Bottomley 强调不必严格遵循 VSM 模型，建议采用一种“密封”模型，使得不同平面可以相互隔离，避免安全漏洞。同时，他指出，虽然每个虚拟机的地址空间是独立的，但 KVM 的内存属性是按平面划分的，这样可以实现 VSM 的内存保护。

Nicolas 也提到，当前的平面模型可能需要更灵活的地址空间管理，以避免过多的开销，并确保安全性。整体来看，讨论集中在如何平衡安全性、性能和实现复杂性的问题上，参与者们对补丁的潜在影响和实现细节进行了深入的探讨。

#### 📝 邮件列表

1. **[07-17 13:48]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: Saenz Julienne, Nicolas <nsaenz@amazon.es>
2. **[07-17 10:35]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: James Bottomley <James.Bottomley@HansenPartnership.com>
3. **[07-17 11:56]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: James Bottomley <James.Bottomley@HansenPartnership.com>
4. **[07-17 17:33]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: Saenz Julienne, Nicolas <nsaenz@amazon.es>
5. **[07-17 14:26]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: James Bottomley <James.Bottomley@HansenPartnership.com>

---

### Thread 19: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 10 Jul 2026 15:21:28 -0700

#### 🤖 AI 总结

本邮件线程讨论的主题是针对 AmpereOne 处理器的 erratum AC03_CPU_57 和 AC04_CPU_29 的补丁。该补丁旨在解决在处理器中通过 ICC_DIR_EL1 或 ICC_EOIRx_EL1 关闭未激活的物理中断时，导致 CPU 丢失中断挂起状态的问题，从而影响未来中断的传递。补丁由 D Scott Phillips 提交，并得到了 Marc Zyngier 的支持。

在历史讨论中，D Scott Phillips 解释了该问题的根本原因，并确认这是一个小的 bug 修复，虽然在特定情况下可能会导致问题。Marc Zyngier 进一步确认了补丁的有效性，并表示理解了问题的本质。

在本周的新讨论中，D Scott Phillips 提到 AmpereOne AC04 支持 gicv4.1，这意味着对待 pending vlpi/vsgi 的处理路径不同，因此不会引发相同的问题。Marc Zyngier 认为需要在 errata 文档中增加关于直接注入的说明，以提高清晰度，并表示将会进行相应的补充。这一系列讨论表明，开发者们在努力确保补丁的准确性和完整性，以便更好地解决相关问题。

#### 📝 邮件列表

1. **[07-10 15:21]** [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>
2. **[07-11 08:37]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-14 16:06]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57
 and AC04_CPU_29
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>
4. **[07-15 13:29]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-15 06:55]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57
 and AC04_CPU_29
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>

---

### Thread 20: [PATCH v6 0/3] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs

**📧 邮件数**: 4 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 19 Jul 2026 20:24:39 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）自测试的补丁系列，主要集中在改进 ARM64 架构下的 `set_id_regs` 功能的诊断信息。

1. **原始补丁内容**：补丁的目标是改善在运行 ARM64 系统时，关于访客寄存器读取和重置值保持测试的诊断信息。当前的实现使用立即致命的断言，导致在测试失败时无法明确指出是哪个寄存器出现问题。补丁通过将这些断言替换为标准的 kselftest 报告，使得每个寄存器的测试结果都能被单独报告，从而提高了可读性和调试效率。

2. **之前讨论要点**：在之前的讨论中，开发者们关注到现有测试在失败时缺乏详细信息，导致调试过程变得困难。补丁的设计旨在解决这一问题，确保每个寄存器的测试结果都能清晰地反馈。

3. **本周的新讨论与进展**：本周的讨论中，Mark Brown 提交了三个补丁，分别针对寄存器读取、寄存器重置测试和位域有效性检查进行了改进。每个补丁都得到了 Ben Horgan 的审核，并且在实现上进行了细致的调整，例如将寄存器名称存储在数组中以便于报告。整体上，这些补丁显著提升了测试的可用性和可读性，确保开发者在进行调试时能更快地定位问题。

#### 📝 邮件列表

1. **[07-19 20:24]** [PATCH v6 0/3] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-19 20:24]** [PATCH v6 1/3] KVM: selftests: arm64: Report set_id_reg reads of
 test registers as tests
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-19 20:24]** [PATCH v6 2/3] KVM: selftests: arm64: Report register reset tests
 individually
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-19 20:24]** [PATCH v6 3/3] KVM: selftests: arm64: Make set_id_regs bitfield
 validatity checks non-fatal
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 21: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 30 Jun 2026 13:09:59 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 shadow ptdump 修复。Wei-Lin Chang 提出的补丁系列（PATCH v2 0/6）旨在解决 shadow ptdump debugfs 文件的问题，主要是由于无法为每个 mmu 创建独立的 ptdump 文件，因此创建了一个名为 "shadow_page_tables" 的单一文件，用于转储所有有效 mmu 的页面表信息。

在历史讨论中，补丁的主要内容包括创建一个新的 ptdump 文件，能够在请求时输出所有有效的 shadow 页面表信息，并解决了在 kvm_arch_flush_shadow_all() 中的并发问题，确保在读取时不会发生竞争条件。此外，审查中指出了一些潜在问题，如并发重新分配 nested_mmus 数组可能导致的 Use-After-Free 问题。

在本周的新讨论中，Wei-Lin Chang 针对审查反馈进行了回应，指出在调用 kvm_arch_flush_shadow_all() 时不会有运行的 vCPU 进行竞争，并计划调整 kvm_ptdump_parser_init() 的顺序，以确保在可能的错误返回之前设置 st->kvm。同时，他承认缺失了 stage-2 ptdump 的最后一行数据，并表示这将作为一个独立问题在后续修复。整体来看，本周的讨论进一步明确了补丁的实现细节和后续计划。

#### 📝 邮件列表

1. **[06-30 13:09]** [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[06-30 13:10]** [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump file
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[06-30 12:27]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: sashiko-bot@kernel.org
4. **[07-17 15:52]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 22: [PATCH v6 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Jul 2026 12:51:36 +0200

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VGIC（虚拟通用中断控制器）进行的两个补丁（patch）的修复工作，主要解决了 LPI（本地中断）的释放和重新注册过程中的竞争条件问题。

**原始补丁内容**：
补丁 v6 主要包括两个部分：第一个补丁修复了 LPI 释放和重新注册之间的竞争条件，可能导致 LPI 结构泄漏或被过早删除；第二个补丁则缓解了在注册 LPI 时可能出现的 -ENOMEM 错误。

**之前讨论要点**：
在历史讨论中，补丁经历了多次迭代，主要集中在如何安全地管理 LPI 的引用计数和避免在并发情况下的错误。开发者们讨论了如何在不同的 CPU 上处理 LPI 的释放和注册，以确保数据一致性。

**本周新讨论及进展**：
本周的讨论中，开发者 Carlos López 提出了补丁的具体实现，详细描述了如何通过调整引用计数的处理方式来避免竞争条件，并在注册新 LPI 时使用 GFP_NOWAIT 标志来防止内存分配失败。Sashiko AI 也对补丁进行了审查，指出了潜在的高优先级问题，强调了在 LPI 注册过程中未处理 -ENOMEM 错误的风险。整体来看，本周的讨论进一步完善了补丁的细节，并引发了对潜在问题的关注。

#### 📝 邮件列表

1. **[07-15 12:51]** [PATCH v6 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-15 12:51]** [PATCH v6 1/2] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
3. **[07-15 12:51]** [PATCH v6 2/2] KVM: arm64: vgic: Mitigate potential LPI registration failure
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
4. **[07-15 11:10]** Re: [PATCH v6 2/2] KVM: arm64: vgic: Mitigate potential LPI
 registration failure
   - 发件人: sashiko-bot@kernel.org

---

### Thread 23: [PATCH] KVM: arm64: Reject guest_memfd memslots when the VM has MTE

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 12:07:56 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下处理 guest_memfd 内存槽的补丁。补丁的主要内容是，当虚拟机启用了 MTE（Memory Tagging Extension）时，拒绝使用 guest_memfd 作为内存槽的后备存储。这是因为在使用 guest_memfd 文件创建的虚拟内存区域（VMA）中，MTE 不被允许，从而避免了潜在的内存管理问题。

在之前的讨论中，Alexandru Elisei 提出了该补丁，指出当前的实现允许在启用 MTE 的情况下创建 guest_memfd 内存槽，这与 KVM 的设计意图相悖。补丁通过在内存区域准备阶段拒绝此类内存槽来解决该问题。

本周的新讨论中，参与者 Fuad Tabba 提出了对补丁的改进建议，包括添加修复标签和优化条件判断逻辑。Alexandru 同意了这些建议，并表示将在下一版本中实现这些改动。此外，Alexandru 还提到将检查所有内存槽，以确保在启用 MTE 功能时没有任何内存槽是由 guest_memfd 文件支持的。整体来看，本周的讨论集中在补丁的细节优化和潜在问题的进一步解决上。

#### 📝 邮件列表

1. **[07-14 12:07]** [PATCH] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-14 12:44]** Re: [PATCH] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-14 14:15]** Re: [PATCH] KVM: arm64: Reject guest_memfd memslots when the VM has
 MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[07-14 15:13]** Re: [PATCH] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 24: [PATCH v4 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 10:59:19 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM 虚拟 CPU 状态管理的补丁系列（PATCH v4 0/8）。该补丁旨在优化 pKVM 在 EL2（异常级别2）下的 vCPU 状态转移，减少在每次世界切换时对非保护来宾状态的复制，从而提高性能。

在历史讨论中，Fuad Tabba 提到该补丁系列基于 Will 的 pKVM 基础设施，重构了 vCPU 状态的转移方式，并引入了 vCPU 查找助手和 VGIC（虚拟通用中断控制器）刷新/同步功能，以减少 EL2 对主机状态的引用。此外，补丁还将一些准备代码进行了重组，以便于后续的功能扩展。

在本周的新讨论中，Oliver Upton 提出了对补丁中函数命名的建议，建议将包装函数命名为 `vcpu_{read,write}_sys_reg()`，以避免与现有实现的混淆。Fuad 对此表示赞同，并确认将进行相应的修改。

总结而言，本周的讨论主要集中在补丁的命名规范上，未涉及功能上的重大变化。

#### 📝 邮件列表

1. **[07-06 10:59]** [PATCH v4 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-06 10:59]** [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-13 17:30]** Re: [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[07-14 07:41]** Re: [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 25: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 12 Jul 2026 15:25:32 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是为 arm64 添加 guest_memfd 支持的补丁（patch）。该补丁的主要内容包括：在 kvm__register_ram_guest_memfd() 中断言 guest_memfd 大于等于 0，使用 kvm_userspace_memory_region2 仅用于 guest_memfd 插槽，并在拆卸时关闭 guest_memfd 文件描述符等。补丁经过多次修改，之前的版本（v1 和 v2）也进行了相应的调整和优化。

在历史讨论中，参与者对补丁的各个方面进行了详细讨论，包括对代码的改进建议和功能的验证。补丁在 v2 版本中增加了对 MTE 的禁用选项，并得到了多位开发者的认可和审核。

在本周的新讨论中，参与者 Alexandru Elisei 和 Suzuki K Poulose 对补丁表示支持，分别进行了代码审核并确认其在 Orion O6 板上的测试结果，表明补丁在实际环境中运行良好。整体来看，补丁得到了积极的反馈，且测试结果表明其功能正常，推动了该功能的进一步发展。

#### 📝 邮件列表

1. **[07-12 15:25]** [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-17 09:54]** Re: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[07-17 11:28]** Re: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 26: [PATCH v2] KVM: arm64: Avoid naming collision in tracing

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 13 Jul 2026 14:13:20 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构中避免跟踪命名冲突的补丁（PATCH v2）。该补丁的主要目的是解决在禁用超管跟踪（CONFIG_NVHE_EL2_TRACING）时，`trace_clock()` 函数的静态内联定义与已在 `linux/trace_clock.h` 中声明的外部函数发生冲突的问题。这种冲突可能在未来引入更多用户时导致编译错误，尤其是与 SMMUv3 驱动相关的情况。

在之前的讨论中，补丁得到了参与者的关注，Mostafa Saleh 提出了补丁的具体实现方案，并指出虽然当前没有其他文件包含 `<nvhe/clock.h>`，但这并不是代码的初衷。补丁修改了 `nvhe/clock.h`、`nvhe/clock.c` 和 `nvhe/trace.c` 三个文件，以避免命名冲突。

在本周的新讨论中，Mostafa Saleh 收到了来自 Vincent Donnefort 的审核反馈，并得到了认可。最终，Oliver Upton 确认该补丁已被应用到下一个版本中，标志着该问题的解决。整体来看，此次讨论顺利推进，补丁得到了积极的反馈并成功整合。

#### 📝 邮件列表

1. **[07-13 14:13]** [PATCH v2] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-13 16:01]** Re: [PATCH v2] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-15 00:57]** Re: [PATCH v2] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 27: [PATCH] KVM: arm64: Fix hyp_trace clock disabling

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 19:10:10 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 hyp_trace 时钟禁用问题的补丁（patch）。该补丁的主要内容是修正 `hyp_trace_clock_enable()` 函数中的禁用路径，确保在取消工作后能够提前返回，而不是重新初始化和重新调度时钟。同时，补丁还清理了未使用的 `hyp_trace_clock::lock` 和冗余的 `hyp_trace_clock::running` 成员，因为 trace_remote 框架已经对回调的调用进行了序列化。

在之前的讨论中，未提及具体的历史讨论内容，但补丁的提交是为了修复一个特定的提交（b22888917fa4），该提交与 nVHE/pKVM hyp 的启动时钟同步相关。

在本周的新讨论中，Vincent Donnefort 提交了补丁，并在后续邮件中回应了 Sashiko AI 机器人对补丁的审查，指出了一个潜在的问题：在 `hyp_trace_enable_tracing()` 的错误路径中缺少清理，可能导致时钟同步的延迟工作泄漏。此外，Vincent 还承认即使他认为 HVC 不会失败，但仍需妥善处理回滚，以避免引入工作队列的损坏。整体来看，本周的讨论集中在补丁的完善和潜在问题的处理上。

#### 📝 邮件列表

1. **[07-14 19:10]** [PATCH] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-14 18:25]** Re: [PATCH] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: sashiko-bot@kernel.org
3. **[07-15 08:13]** Re: [PATCH] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 28: [PATCH v2 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  8 Jul 2026 08:54:31 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 pKVM/nVHE 虚拟化环境的补丁系列，主要是引入了一个新的超管事件 "hyp_printk"，旨在增强超管的日志记录能力。该补丁允许开发者将信息记录到超管跟踪缓冲区，类似于内核中的 `trace_printk()` 函数，从而简化了调试过程，尤其是在 Android 的 pKVM 调试中。

在历史讨论中，Vincent Donnefort 提出了这个补丁系列，并附加了两个相关的补丁，其中一个是 `REMOTE_EVENT_CUSTOM_PRINTK()` 辅助函数，允许使用动态原型和格式创建 printk 事件。这些补丁得到了 Fuad Tabba 的审核和测试。

在本周的新讨论中，Steven Rostedt 对补丁表示认可，并询问该补丁将通过 arm64 或 KVM 树提交，确认了补丁的接受。这表明该补丁在社区中获得了积极的反馈，且即将进入下一步的合并流程。整体来看，讨论围绕着增强虚拟化日志记录功能的补丁展开，显示出社区对改进调试工具的重视。

#### 📝 邮件列表

1. **[07-08 08:54]** [PATCH v2 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-08 08:54]** [PATCH v2 3/4] tracing/remotes: Add REMOTE_EVENT_CUSTOM_PRINTK() helper
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-14 18:40]** Re: [PATCH v2 3/4] tracing/remotes: Add
 REMOTE_EVENT_CUSTOM_PRINTK() helper
   - 发件人: Steven Rostedt <rostedt@goodmis.org>

---

### Thread 29: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 13:37:52 +0900

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM64 架构的 RMI（Realm Management Interface）补丁，主题为“允许填充初始内容”（[PATCH v14 26/44] arm64: RMI: Allow populating initial contents）。该补丁的主要目的是改进 RMI 的错误处理，确保在发生错误时返回适当的 Linux 错误码。

在历史讨论中，补丁的背景并未详细说明，但可以推测出之前的讨论集中在如何处理 RMI 返回值的问题上。参与者 Steven Price 提出了一个关键问题，即 rmi_rtt_data_map_init() 函数返回的原始 RMI 值在失败时是正值，这可能导致后续函数错误地将其视为成功的页面填充数量。

本周的新讨论中，Kohei Enju 和 Steven Price 进行了深入的技术交流。Kohei 指出需要将正的错误值转换为 -ENXIO，以避免错误传播。Steven 认可了这一点，并指出需要在处理返回值时考虑到 ret==0 的情况，承诺在下次提交中修正。此外，他们还讨论了在多线程环境中可能出现的竞争条件，建议在调用 realm_ensure_created() 时加锁以确保线程安全。

总体来看，本周的讨论推动了补丁的改进，解决了潜在的错误处理和并发问题，为后续的代码提交奠定了基础。

#### 📝 邮件列表

1. **[07-14 13:37]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
2. **[07-15 15:06]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 30: [PATCH v2 0/3] KVM: arm64: Tidy up is_created

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 11:31:26 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁系列，主题为“整理 is_created”。该补丁系列的主要目的是清理与 hypervisor 相关的 `kvm->arch.pkvm.is_created` 标志的代码，该标志用于跟踪虚拟机（VM）是否已在 EL2（异常级别 2）中实例化。

在历史讨论中，Fuad Tabba 提出了这个补丁系列，并指出自 v1 版本以来没有代码更改，仅添加了 Keir 的审核意见。补丁主要删除了与该标志相关的无用或冗余代码，而不影响任何功能路径，确保了与正在进行的 pKVM（受保护的 KVM）上游工作之间没有依赖关系。

在本周的新讨论中，Oliver Upton 确认已将该补丁应用到下一个版本中，并列出了具体的补丁内容，包括删除未使用的 EL2 端 is_created 写入、去除 pkvm_init_host_vm() 中无法到达的早期检查，以及删除 pkvm_hyp_vm_is_created() 中冗余的 READ_ONCE() 调用。这表明该补丁系列得到了认可并即将实施。

#### 📝 邮件列表

1. **[07-06 11:31]** [PATCH v2 0/3] KVM: arm64: Tidy up is_created
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-15 00:57]** Re: [PATCH v2 0/3] KVM: arm64: Tidy up is_created
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 31: [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in the nested context.

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 16:11:58 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic（虚拟通用中断控制器）中，避免在嵌套上下文中对 IRQ（中断请求）进行重复停用的补丁（PATCH v2）。

**原始补丁内容**：
该补丁旨在解决在嵌套状态下，物理中断已经通过 LR（中断路由寄存器）中的硬件位停用的情况。尽管再次停用不会造成直接危害，但在 AmpereOne 处理器上可能会触发一个已知的错误，从而导致 CPU 丢失中断待处理状态，影响未来中断的交付。

**之前讨论要点**：
历史讨论中并未提供具体的补丁或问题背景，但补丁的提交信息中提到，之前的代码在处理 IRQ 停用时未考虑嵌套状态的影响，可能导致不必要的错误。

**本周的新讨论与进展**：
本周的讨论中，D Scott Phillips 提交了补丁并详细说明了其目的和背景。Sashiko AI 评审指出了补丁中的潜在问题，包括在嵌套状态下跳过 `vgic_v3_deactivate_phys()` 的条件可能导致物理中断永久处于激活状态。此外，还提到了一些预先存在的问题，如 KVM 在处理 L2 的 `SYS_ICC_DIR_EL1` 访问时可能会损坏 L1 的 VGIC 状态，以及恶意嵌套的来宾虚拟机可能触发主机的警告。整体来看，讨论集中在补丁的有效性和潜在风险上。

#### 📝 邮件列表

1. **[07-14 16:11]** [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in the nested context.
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>
2. **[07-14 23:50]** Re: [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in
 the nested context.
   - 发件人: sashiko-bot@kernel.org

---

### Thread 32: [PATCH] arm64: Query per-VM capabilities when selecting vCPU features

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 12:03:29 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH] arm64: Query per-VM capabilities when selecting vCPU features”，主要讨论了在选择虚拟CPU特性时如何查询每个虚拟机（VM）的能力。

原始补丁的内容是针对KVM（Kernel-based Virtual Machine）在arm64架构下的改进，旨在通过`kvm__supports_vm_extension()`函数查询每个VM的特性，而不是依赖于全局的`/dev/kvm`文件描述符。这是因为受保护的虚拟机支持的特性子集与主机的特性不同，原有的实现无法正确反映VM的能力，导致在初始化时可能请求不支持的特性（如SVE）。

在之前的讨论中，补丁的背景并未详细列出，但可以推测出这是对现有KVM功能的必要改进，以确保虚拟机能够正确识别和使用其支持的特性。

本周的新讨论中，Fuad Tabba提交了补丁，并阐述了其必要性。Suzuki K Poulose对该补丁表示认可，并给予了审核通过的反馈，认为这种改进是合理的，并指出与CCA（Common Criteria Assurance）也有类似的实现。

总结来看，此次讨论集中在改进KVM对每个虚拟机特性的查询机制上，确保虚拟机能够正确使用其支持的功能，得到了参与者的积极反馈。

#### 📝 邮件列表

1. **[07-14 12:03]** [PATCH] arm64: Query per-VM capabilities when selecting vCPU features
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-14 12:15]** Re: [PATCH] arm64: Query per-VM capabilities when selecting vCPU
 features
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 33: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 08:10:48 +0900

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现嵌套阶段2反向映射的补丁（PATCH v3 0/5）。该补丁旨在增强虚拟化功能，特别是在处理嵌套虚拟化时的地址映射。

在历史讨论中，虽然没有具体的邮件记录，但可以推测之前的讨论涉及补丁的设计和实现细节，以及它在当前 KVM 代码基础上的适用性。

本周的新讨论主要集中在补丁的更新进展上。参与者 Itaru Kitayama 提到，由于该补丁系列与最近的 kvmarm/fixes 不再兼容，希望 Wei-Lin Chang 能够更新补丁系列。Wei-Lin Chang 回复表示由于同时在处理其他事务，更新进度有所延迟，但他正在准备 v4 版本，并计划在本周内发布。

总结来看，当前的讨论主要围绕补丁的更新和测试计划，表明开发者们在积极推进嵌套虚拟化的功能实现。

#### 📝 邮件列表

1. **[07-14 08:10]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
2. **[07-14 06:47]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 34: [PATCH] KVM: arm64: Update Fuad Tabba's email address

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 19 Jul 2026 17:32:57 +0100

#### 🤖 AI 总结

本邮件讨论的主题是更新 Fuad Tabba 的电子邮件地址，以便更好地反映其在 KVM/arm64 领域的工作。Fuad 提出了一个补丁（patch），将其在 KVM/arm64 维护者列表中的邮箱从原来的 tabba@google.com 更新为 fuad.tabba@linux.dev，并在 .mailmap 文件中添加了相应的条目，以确保历史提交能够正确映射到新的邮箱地址。

在之前的讨论中并没有相关的内容，邮件列表中仅有这一条新讨论。

本周的讨论中，Fuad Tabba 提交了该补丁，具体修改包括在 .mailmap 文件中添加一行以映射新的邮箱地址，并在 MAINTAINERS 文件中更新了其维护者的联系信息。这一补丁的目的是为了确保其在内核工作中的邮箱信息准确无误，便于其他开发者联系。

#### 📝 邮件列表

1. **[07-19 17:32]** [PATCH] KVM: arm64: Update Fuad Tabba's email address
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 35: [PATCH] KVM: arm64: ptdump: Flush the last region

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 18 Jul 2026 00:12:33 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 ptdump 功能的一个补丁，旨在解决最后一个区域未被正确输出的问题。

**原始补丁内容**：
补丁的核心是修改 ptdump 的实现，使其在遍历每个叶子条目时，能够正确输出最后一个区域的信息。当前实现中，note_page() 仅在检测到级别或保护的变化时输出数据，因此最后一个区域在没有变化的情况下被遗漏。补丁通过在遍历结束时手动调用 note_page()，并将地址设置为 BIT(ia_bits)（即访客 IPA 空间的结束位置）和级别设置为 -1，来确保最后区域被输出。

**之前讨论要点**：
在历史讨论中，未提供具体的讨论内容或反馈，因此我们无法总结之前的讨论要点。

**本周的新讨论、进展或结论**：
本周的讨论中，Wei-Lin Chang 提交了该补丁，并详细说明了补丁的实现逻辑和目的。补丁的代码修改涉及到两个文件，增加了必要的调用以确保最后区域的输出。补丁已被提交并标记为修复了之前的一个问题，相关链接和报告者信息也被包含在内。当前没有其他参与者的反馈或讨论。

#### 📝 邮件列表

1. **[07-18 00:12]** [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 36: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 17 Jul 2026 14:22:07 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构中 FPSIMD（浮点 SIMD）模块的一个补丁，具体内容为将 SME（Scalable Matrix Extension）保存和恢复的功能内联化。

在历史讨论中，没有提供具体的补丁或背景信息，因此我们无法得知该补丁的详细内容或之前的讨论要点。

本周的新讨论中，参与者 Mark Rutland 提到，该补丁已在 GCC 的一个提交中合并，提交哈希为 090f3e78a10b5ce14fd80de82d3e8dda8af1cae6，标题为“aarch64: Make Uc[ij] constraints public”。他指出，未来一旦最低支持的工具链版本为 GCC 14.1.0 及以上和 LLVM 18.1.0 及以上时，就可以使用该功能。

总结而言，本周的讨论主要集中在补丁的合并状态及其对未来工具链版本的依赖，未涉及更多的技术细节或争议。

#### 📝 邮件列表

1. **[07-17 14:22]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 37: [PATCH] KVM: arm64: Use consistent type for pool size

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 15 Jul 2026 15:01:25 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的内存池大小类型一致性问题。Mostafa Saleh 提出了一项补丁，旨在将内存池的大小统一为“unsigned long”类型，以避免在调用 `hyp_early_alloc_contig()` 和 `hyp_pool_init()` 时发生截断到 32 位的问题。虽然目前这种截断不会造成严重问题（因为需要 4G 字节的内存切割才能溢出），但随着新用户（如 IOMMU）的加入，内存切割的大小将变得难以推理。

补丁具体修改了四个文件，主要是将函数参数类型从 `unsigned int` 改为 `unsigned long`，以确保在处理大内存时不会出现问题。此外，Mostafa 还提到在 SMMUv3 中为内存池大小添加了一个上限，以避免溢出。

本周的讨论中，Mostafa 提交了补丁并详细说明了修改的必要性，强调了在未来可能出现的内存管理问题。邮件中没有其他参与者的回复或进一步讨论。

#### 📝 邮件列表

1. **[07-15 15:01]** [PATCH] KVM: arm64: Use consistent type for pool size
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 38: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 15 Jul 2026 11:51:00 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复 hyp_trace 时钟禁用的相关问题。

**原始补丁内容**：补丁的主要目的是修复 `hyp_trace_clock_enable()` 函数中的禁用路径，避免在取消工作后重新初始化和重新调度时钟。补丁还清理了未使用的 `hyp_trace_clock::lock` 和冗余的 `hyp_trace_clock::running`，因为 trace_remote 框架已经对回调的调用进行了序列化。

**之前的讨论要点**：该补丁是对之前提交的补丁（b22888917fa4）进行的改进，主要解决了在启用跟踪时可能出现的错误处理问题。

**本周的新讨论与进展**：本周的邮件中，Vincent Donnefort 提交了补丁的第二个版本（v2），在此版本中，针对 `__tracing_enable` 出现错误时进行了回滚处理。补丁的代码更改和逻辑调整已被详细列出，并且补丁已附上了签名，表明其作者的认同。

总体来看，本周的讨论集中在补丁的细节改进上，确保了在错误情况下的处理更加稳健。

#### 📝 邮件列表

1. **[07-15 11:51]** [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 39: [PATCH v8 00/20] KVM: selftests: Add eventfd+VFIO IRQ test

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 14 Jul 2026 11:41:17 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）自测试的补丁集，主要内容是增加 eventfd 和 VFIO IRQ 测试。该补丁集包含 20 个补丁，旨在增强 KVM 的自测试功能，特别是在中断处理和设备支持方面。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁集的提出是为了改善 KVM 的中断管理能力，尤其是在使用 eventfd 和 VFIO 设备时的表现。

本周的讨论中，Sean Christopherson 表示已将该补丁集应用到 kvm-x86 的 irq_test 中，并感谢贡献者。补丁集中的关键补丁包括：
- 构建并链接 VFIO 自测试库到 KVM 自测试中。
- 添加用于读取和写入访客内存的宏。
- 实现 IRQ 发送和接收的测试，以及对 VFIO 设备的支持。
- 增加对 IRQ 亲和性和 IRQ 重映射的验证功能。

整体来看，本周的进展表明该补丁集已成功整合到 KVM 的测试框架中，标志着对 KVM 中断处理能力的进一步增强。

#### 📝 邮件列表

1. **[07-14 11:41]** Re: [PATCH v8 00/20] KVM: selftests: Add eventfd+VFIO IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 40: [PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 14 Jul 2026 17:04:11 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）中处理仅使用 `guest_memfd` 的内存槽时，忽略 MMU 通知器的补丁（PATCH v2）。该补丁的核心内容是，当内存槽仅由 `guest_memfd` 提供时，虚拟机的内存映射直接通过 `guest_memfd` 文件获取，而不是通过用户空间映射。因此，MMU 通知器对这些内存槽并不适用。

在历史讨论中，补丁的初版（v1）已被提出，主要问题是 KVM 的 MMU 通知器仍然会修改二级 MMU 的页表，导致内存在下次访问时被重新映射。补丁的更新版本（v2）在此基础上进行了改进，明确忽略这些内存槽的 MMU 通知器，以减少不必要的操作。

在本周的新讨论中，补丁的作者 Alexandru Elisei 提供了补丁的详细实现和测试结果，确认在 arm64 平台上，使用 KVM_PRE_FAULT_MEMORY 映射整个二级地址空间后，`guest_memfd` 的内存仍然保持映射状态。此外，补丁还针对之前讨论中提到的未平衡失效问题进行了修复，并根据反馈修改了提交信息。整体来看，本周的讨论主要集中在补丁的实现细节和测试验证上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[07-14 17:04]** [PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 41: [PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 13 Jul 2026 22:07:43 +0000

#### 🤖 AI 总结

本邮件主题为“[PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes”，主要讨论了针对 ARM64 架构的 KVM（Kernel-based Virtual Machine）进行的 VHE（Virtualization Host Extensions）专用启动修复的补丁。

在历史讨论部分没有提供具体内容，因此我们无法了解该补丁的详细背景或之前的讨论要点。

在本周的新讨论中，参与者 Colton Lewis 对 Sasha Levin 的回复表示感谢，但未提供进一步的技术细节或进展。这表明目前讨论仍处于初步阶段，可能需要更多参与者的反馈或进一步的技术探讨。

总体来看，本周的讨论没有实质性的进展，主要是对补丁的确认和感谢，后续可能需要更多的技术交流以推动补丁的实施。

#### 📝 邮件列表

1. **[07-13 22:07]** Re: [PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

## 📌 RFC

共 6 个 thread

---

### Thread 1: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots

**📧 邮件数**: 22 | **👥 参与者**: 6 | **📅 开始时间**: Thu,  2 Jul 2026 15:29:09 +0100

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于 KVM（内核虚拟机）对仅支持 `guest_memfd` 的内存插槽实现脏页日志记录的补丁（RFC PATCH 0/3）。该补丁旨在允许共享内存的脏页日志记录，以便用户空间可以更灵活地访问和管理内存。

**历史讨论要点**：
最初的补丁由 Alexandru Elisei 提出，主要关注于如何在 KVM 中实现对 `guest_memfd` 仅内存插槽的脏页日志记录。历史讨论中，参与者们对补丁的必要性和实现细节进行了深入探讨，特别是如何处理内存插槽的状态变化以及用户空间的访问问题。Sean Christopherson 提出了一些技术上的担忧，特别是关于内存状态不一致的问题。

**本周新讨论**：
在最近的讨论中，参与者们继续探讨了补丁的实现细节和潜在问题。David Hildenbrand 强调了在更新内存插槽标志时，如何确保 VCPU 的一致性。Alexandru Elisei 提出了对 SPE（安全处理扩展）与迁移之间的关系的看法，认为在当前架构下，SPE 的广泛使用可能受到限制。讨论中还提到，TDX（可信数据扩展）在进行实时迁移时也需要对 `guest_memfd` 插槽的脏页日志记录功能进行支持。

总体而言，本周的讨论集中在如何确保补丁的实现能够满足不同架构的需求，并解决在迁移和内存管理过程中可能出现的技术挑战。

#### 📝 邮件列表

1. **[07-02 15:29]** [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-02 15:29]** [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[07-02 15:29]** [RFC PATCH 2/3] KVM: Implement dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[07-06 14:43]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[07-06 17:56]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[07-06 18:29]** Re: [RFC PATCH 2/3] KVM: Implement dirty page logging for
 guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[07-07 17:58]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
8. **[07-07 18:05]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
9. **[07-07 18:12]** Re: [RFC PATCH 2/3] KVM: Implement dirty page logging for
 guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
10. **[07-07 10:12]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[07-09 12:21]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[07-09 12:01]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[07-09 13:33]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[07-10 11:26]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Mark Rutland <mark.rutland@arm.com>
15. **[07-10 11:44]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
16. **[07-10 11:18]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Oliver Upton <oupton@kernel.org>
17. **[07-13 15:42]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
18. **[07-13 14:48]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
19. **[07-13 16:03]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
20. **[07-13 16:11]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
21. **[07-13 09:13]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
22. **[07-13 22:39]** Re: [RFC PATCH 2/3] KVM: Implement dirty page logging for
 guest_memfd-only memslots
   - 发件人: Kishen Maloor <kishen.maloor@intel.com>

---

### Thread 2: [RFC PATCH v3 00/19] named CPU models for Arm64 on KVM

**📧 邮件数**: 20 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 16 Jul 2026 21:38:39 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 上 Arm64 的命名 CPU 模型的 RFC PATCH v3，主要内容包括对 Arm64 CPU 模型的支持、相关功能的实现以及一系列补丁的提交。

1. **原始 patch/问题的内容**：该补丁系列旨在为 KVM 上的 Arm64 提供命名 CPU 模型支持，以解决当前 QEMU 仅支持 `-cpu host/max` 的限制，从而阻碍了不同 CPU 特性的虚拟机的实时迁移。命名模型为客户机提供了严格的 CPU 特性契约，并允许通过覆盖特定 ID 寄存器字段来定制模型。

2. **之前讨论要点**：历史讨论中提到，命名模型的引入将使得 QEMU 能够更好地与 x86 生态系统保持功能一致性，支持 QMP 反射和管理层的需求。补丁系列经过多次迭代，逐步完善了命名模型的实现细节和 QMP 支持。

3. **本周的新讨论、进展或结论**：本周的讨论集中在多个补丁的提交上，包括对 ID 寄存器的处理、命名模型的层次结构、QMP 命令的添加等。特别是新增了对 Nvidia Grace 和其他命名模型的支持，增强了对 ID 寄存器字段的处理逻辑，并引入了查询 CPU 属性信息的 QMP 命令。此外，补丁还解决了在不同虚拟化环境下的 ID 寄存器写回问题，确保了模型的正确性和兼容性。整体上，讨论推动了 Arm64 命名 CPU 模型的实现进程，增强了 KVM 的功能。

#### 📝 邮件列表

1. **[07-16 21:38]** [RFC PATCH v3 00/19] named CPU models for Arm64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
2. **[07-16 21:38]** [RFC PATCH v3 01/19] target/arm/sysreg: regenerate cpu-sysregs.h.inc
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
3. **[07-16 21:38]** [RFC PATCH v3 02/19] scripts: bug fixes in update-aarch64-cpu-sysreg-properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
4. **[07-16 21:38]** [RFC PATCH v3 03/19] target/arm: regenerate cpu-idregs.h.inc
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
5. **[07-16 21:38]** [RFC PATCH v3 04/19] target/arm: expose all ID regs fields as properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
6. **[07-16 21:38]** [RFC PATCH v3 05/19] target/arm/kvm: enable writable implementation ID registers
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
7. **[07-16 21:38]** [RFC PATCH v3 06/19] target/arm/kvm: Read all ID registers from KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
8. **[07-16 21:38]** [RFC PATCH v3 07/19] target/arm/kvm: handle special ID registers cases when reading from KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
9. **[07-16 21:38]** [RFC PATCH v3 08/19] target/arm/kvm: Handle writeback for special ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
10. **[07-16 21:38]** [RFC PATCH v3 09/19] target/arm: Add named cpu model infra + graviton3 named model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
11. **[07-16 21:38]** [RFC PATCH v3 10/19] target/arm: Add Nvidia Grace named model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
12. **[07-16 21:38]** [RFC PATCH v3 11/19] target/arm: fix sve and pauth finalize for named cpu models
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
13. **[07-16 21:38]** [RFC PATCH v3 12/19] target/arm: Introduce stub files required for qmp support
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
14. **[07-16 21:38]** [RFC PATCH v3 13/19] target/arm/qmp: add named models and properties to cpu-model-expansion
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
15. **[07-16 21:38]** [RFC PATCH v3 14/19] target/arm/kvm: compute supported values for ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
16. **[07-16 21:38]** [RFC PATCH v3 15/19] target/arm/kvm: introduce kvm_arm_get_host_isar helper
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
17. **[07-16 21:38]** [RFC PATCH v3 16/19] qmp: add query-cpu-props-info command
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
18. **[07-16 21:38]** [RFC PATCH v3 17/19] target/arm: Report 0 as supported for ID fields gated by vCPU init flags
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
19. **[07-16 21:38]** [RFC PATCH v3 18/19] target/arm/qmp: hook blockers in query-cpu-definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[07-16 21:38]** [RFC PATCH v3 19/19] target/arm/kvm: fix host model writeback when kernel supports EL2
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 3: [RFC PATCH 0/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 16 Jul 2026 19:39:31 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁系列，主要集中在使用 TTBR1_EL2 进行 hVHE（Hypervisor Virtualization Extensions）运行时映射的问题。

**原始补丁/问题内容**：
补丁系列的目标是将 hVHE 的运行时映射从 TTBR0_EL2 移动到 TTBR1_EL2，以便更好地利用 EL2&0 转换机制，支持更现代的内核映射方式。当前实现仍使用传统的 nVHE（Non-Virtualization Extensions）地址布局，导致不必要的兼容性问题。

**之前讨论要点**：
在之前的讨论中，补丁的设计理念得到了认可，主要关注于如何清晰地区分内核映射符号和线性映射地址。补丁系列通过引入新的 API 和明确的地址转换逻辑来解决这一问题，确保在 hVHE 模式下能够正确处理地址映射。

**本周的新讨论、进展或结论**：
本周的讨论中，Aneesh Kumar K.V 提出了多个补丁，包括将内核映射符号和线性映射的 API 拆分、明确地址转换方法，以及最终实现将 hVHE 的运行时映射迁移到 TTBR1_EL2。参与者对补丁的潜在问题进行了审查，指出了一些高优先级和中等优先级的潜在问题，例如对控制平面系统寄存器的写入后缺乏必要的指令屏障（isb），以及错误处理路径的死代码等。整体来看，补丁系列在设计上得到了积极反馈，但仍需解决提出的潜在问题。

#### 📝 邮件列表

1. **[07-16 19:39]** [RFC PATCH 0/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[07-16 19:39]** [RFC PATCH 1/5] KVM: arm64: Make hyp symbol address conversion explicit
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[07-16 19:39]** [RFC PATCH 2/5] KVM: arm64: Split hyp mapping APIs by address type
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[07-16 19:39]** [RFC PATCH 3/5] KVM: arm64: Split hyp VA-to-PA conversion by address type
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[07-16 19:39]** [RFC PATCH 4/5] KVM: arm64: Rename the hyp private VA allocation base
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[07-16 19:39]** [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[07-16 14:26]** Re: [RFC PATCH 2/5] KVM: arm64: Split hyp mapping APIs by address
 type
   - 发件人: sashiko-bot@kernel.org
8. **[07-16 14:27]** Re: [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime
 mappings
   - 发件人: sashiko-bot@kernel.org

---

### Thread 4: [RFC PATCH 0/2] KVM: arm64: Support BBM level 3

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 17 Jul 2026 13:08:58 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下支持 BBM（Break-Before-Make）级别 3 的补丁系列。该补丁的主要目的是通过直接替换 stage-2 PTE（Page Table Entry）来提高性能，避免软件实现的复杂性。

在历史讨论中，补丁的背景和动机被明确指出：支持 BBM 级别 3 可以在主机 CPU 的 stage-2 和 SMMUv3 之间共享页表，提升 KVM 的保护性能。补丁分为两个部分：第一个补丁用于清理旧的 PTE，第二个补丁实现了 BBM 级别 3 的核心逻辑。

本周的新讨论中，Mostafa Saleh 提出了补丁的具体实现细节，包括如何在支持 BBM 级别 3 的情况下，原子性地更新 PTE 并进行 TLB（Translation Lookaside Buffer）失效处理。讨论中还提到了一些潜在问题，如在替换块映射时可能违反架构要求，导致 TLB 冲突。Oliver Upton 建议在实现中明确假设 KVM 不会更改活动翻译的访问权限属性，并提出了对未来优化的想法。

总体而言，本周的讨论集中在补丁的实现细节、潜在问题和未来的改进方向上，参与者们积极交流以确保补丁的有效性和稳定性。

#### 📝 邮件列表

1. **[07-17 13:08]** [RFC PATCH 0/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-17 13:08]** [RFC PATCH 1/2] KVM: arm64: Add stage2_clean_old_pte()
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-17 13:09]** [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-17 13:28]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: sashiko-bot@kernel.org
5. **[07-17 14:15]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[07-17 13:56]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[07-18 19:54]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 5: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 19 Jul 2026 15:25:54 +0530

#### 🤖 AI 总结

本邮件讨论的主题是关于一个 RFC PATCH，内容为“KVM: 忽略仅用于 guest_memfd 的 memslots 的 MMU 通知器”。该补丁旨在解决内核中的一个问题，具体是针对 guest_memfd 相关的内存插槽，避免 MMU 通知器引发的潜在问题。

在历史讨论中，并没有提供具体的背景信息或之前的讨论要点，因此我们无法得知该补丁的详细背景或之前的争议。

本周的讨论由参与者 Jeffin820 提出，他对 Sean Christopherson 提出的补丁进行了测试。Jeffin 表示，他使用了 XIAO WU 提供的重现程序、vanilla syzbot 重现程序以及自定义的重现程序进行测试。结果显示，在未打补丁的内核上，这些重现程序均能触发使用后释放（UAF）问题，但在应用了该补丁后，问题得以解决。

综上所述，本周的进展表明，该补丁有效地解决了之前存在的 UAF 问题，显示出其在提高内核稳定性方面的潜力。

#### 📝 邮件列表

1. **[07-19 15:25]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Jeffin820 <jeffinphilip14@gmail.com>

---

### Thread 6: [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 17 Jul 2026 09:26:57 -0700

#### 🤖 AI 总结

本邮件讨论了一个针对 KVM 的用户空间 API（uAPI）提案，旨在允许虚拟机监控器（VMM）以编程方式查询通用中断状态（GSI）及中断旁路（irqbypass）状态。该提案的主要动机是解决 VMM 和 KVM 之间在中断虚拟化状态方面的操作差距。KVM 在内核层面上持有每个 GSI 的实时状态，但缺乏高层语义信息；而 VMM 则拥有完整的中断拓扑信息，但无法稳定地查询这些 GSI 的实际运行状态。

提案中提出的设计原则包括架构无关性、可扩展性和解耦性，建议通过一个新的 ioctl（KVM_GET_GSI_STATE）来实现。该 ioctl 允许 VMM 查询特定 GSI 的状态，并返回相关的状态标志和性能计数器。

在本周的新讨论中，邮件中详细描述了提案的 API 定义、实现步骤以及开放问题。参与者讨论了结构和标志的全面性、故障原因的覆盖、性能计数器的处理方式以及未来扩展性的考虑。该提案被认为是提升 KVM 在生产环境中可观察性和可管理性的重大进展，期待社区的反馈。

#### 📝 邮件列表

1. **[07-17 09:26]** [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status
   - 发件人: Jing Zhang <jingzhangos@google.com>

---

## 📌 GIT PULL

共 2 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.2, take #2

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  8 Jul 2026 17:12:42 +0100

#### 🤖 AI 总结

本邮件线程讨论了 KVM/arm64 在 7.2 版本中的修复补丁，主要由 Marc Zyngier 提出。历史讨论中，Marc 提到这次补丁包含了几个关键修复：首先是针对 arm64 的 `kvm_io_bus_get_dev()` 函数的锁定问题，其次是一些 S2 页表的修复，还包括针对 pKVM 的 FFA 代理修复，以及一个非常冷门的修复，涉及从 MMIO 进行符号扩展加载的仿真问题。这些修复旨在解决 KVM 支持 32 位 ARM 时遗留的一些问题。

在本周的新讨论中，Paolo Bonzini 确认已经拉取了之前的补丁，并表示将继续处理后续的修复。这表明补丁的整合进展顺利，且参与者之间的沟通良好。

总体来看，本周的讨论主要是对历史讨论的确认和进展更新，未涉及新的技术问题或争议。

#### 📝 邮件列表

1. **[07-08 17:12]** [GIT PULL] KVM/arm64 fixes for 7.2, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-15 12:14]** Re: [GIT PULL] KVM/arm64 fixes for 7.2, take #2
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

### Thread 2: [GIT PULL] KVM/arm64 fixes for 7.2, take #1

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 15 Jul 2026 12:13:10 +0200

#### 🤖 AI 总结

本邮件主题为「[GIT PULL] KVM/arm64 fixes for 7.2, take #1」，主要讨论了针对 KVM/arm64 的修复补丁。该补丁旨在解决在 7.2 版本中发现的一些问题。

在历史讨论部分没有提供具体的背景信息，邮件中没有提及之前的讨论要点，因此我们无法了解补丁的详细内容或其背景。

在本周的新讨论中，Marc Zyngier 提到感谢 Paolo Bonzini 的工作，并确认已将补丁合并。Paolo 对于合并的延迟表示歉意，但也指出这一点在之前已被知晓。

总结来看，本周的讨论主要集中在确认补丁的合并上，虽然没有提供具体的技术细节，但显示出开发者之间的良好沟通与协作。

#### 📝 邮件列表

1. **[07-15 12:13]** Re: [GIT PULL] KVM/arm64 fixes for 7.2, take #1
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for
 LLVM objcopy compatibility

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 16 Jul 2026 17:33:15 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 单元测试的 Makefile 修改，旨在确保在使用 llvm-objcopy 构建 EFI 二进制文件时，保留 .dynstr 段，以避免构建失败。

**原始 patch/问题的内容**：
Colton Lewis 提出了一个补丁，修改了 arm、riscv 和 x86 的 Makefile，增加了对 .dynstr 段的保留。之前在使用 llvm-objcopy 时，如果不保留 .dynstr 段，会导致错误，提示该段无法被移除，因为它被 .dynamic 段引用。

**之前讨论要点**：
由于邮件中没有提供历史讨论的内容，因此无法总结之前的讨论要点。

**本周的新讨论、进展或结论**：
本周，Colton Lewis 提交了该补丁，具体修改了三个 Makefile 文件，确保在构建过程中包含 .dynstr 段。补丁的签署者为 Colton Lewis，并得到了 Gemini 团队的协助。该修改旨在解决使用 llvm-objcopy 时的构建问题，确保 EFI 二进制文件能够顺利生成。

#### 📝 邮件列表

1. **[07-16 17:33]** [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for
 LLVM objcopy compatibility
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

