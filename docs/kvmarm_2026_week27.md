# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-07-06 00:44:43

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 393
- **总 Thread 数**: 27
- **大型 Thread** (>20封): 6 个

### 分类分布

- **PATCH**: 23 threads (367 邮件)
- **RFC**: 2 threads (17 邮件)
- **Question**: 1 threads (2 邮件)
- **Discussion**: 1 threads (7 邮件)

---

## 📌 PATCH

共 23 个 thread

---

### Thread 1: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 68 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 3 Jul 2026 15:50:32 +0000

#### 🤖 AI 总结

本邮件讨论主题为「[PATCH v3 00/40] KVM: arm64: 添加 GICv5 IRS 支持」，主要涉及对 KVM 中 GICv5 IRS 的实现及相关功能的补充。

1. **原始 patch/问题的内容**：
   本次补丁系列旨在为 KVM 的 arm64 架构添加对 GICv5 IRS（中断路由服务）的支持，使得 GICv5 客户端能够使用 SPI（共享中断）和 LPI（本地中断），而不仅限于 PPI（私有中断）。补丁中涉及到 IRS 的 MMIO（内存映射输入输出）接口、虚拟机表（VMTE）管理、VPE（虚拟处理单元）门铃等功能。

2. **之前讨论要点**：
   之前的讨论集中在如何实现 GICv5 的基本功能，包括对 PPI 的支持，以及如何管理中断状态和虚拟机的生命周期。补丁中还提到需要确保 IRS 的状态在保存和恢复过程中保持一致，避免出现不一致的中断状态。

3. **本周的新讨论、进展或结论**：
   本周的讨论主要集中在补丁的具体实现细节上，包括 IRS MMIO 注册、SPI 和 LPI 的状态管理、以及如何处理用户空间对 IRS 的访问。补丁还引入了新的系统寄存器访问接口，确保在虚拟机迁移时能够正确保存和恢复 IRS 状态。此外，邮件中还指出了在实现过程中需要注意的潜在问题，如对 IRS 状态的同步、内存分配的安全性等。

总的来说，本次补丁系列为 KVM 的 GICv5 支持提供了重要的功能扩展，尤其是在中断管理和虚拟化方面，增强了系统的灵活性和性能。

#### 📝 邮件列表

1. **[07-03 15:50]** [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[07-03 15:51]** [PATCH v3 01/40] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[07-03 15:51]** [PATCH v3 02/40] irqchip/gic-v5: Provide OF IRS config frame attrs to
 KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[07-03 15:52]** [PATCH v3 03/40] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[07-03 15:52]** [PATCH v3 04/40] KVM: arm64: gic-v5: Define remaining IRS MMIO
 registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-03 15:53]** [PATCH v3 05/40] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[07-03 15:53]** [PATCH v3 06/40] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-03 15:54]** [PATCH v3 07/40] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[07-03 15:54]** [PATCH v3 08/40] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[07-03 15:55]** [PATCH v3 09/40] KVM: arm64: gic-v5: Create and manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[07-03 15:55]** [PATCH v3 10/40] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[07-03 15:56]** [PATCH v3 11/40] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[07-03 15:56]** [PATCH v3 12/40] KVM: arm64: gic-v5: Keep GICv5 vCPU limit
 model-specific
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[07-03 15:57]** [PATCH v3 13/40] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[07-03 15:57]** [PATCH v3 14/40] KVM: arm64: gic-v5: Set up VMTEs and VPE doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[07-03 15:58]** [PATCH v3 15/40] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[07-03 15:58]** [PATCH v3 16/40] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[07-03 15:59]** [PATCH v3 17/40] KVM: arm64: gic-v5: Introduce struct vgic_v5_irs and
 IRS base address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[07-03 15:59]** [PATCH v3 18/40] KVM: arm64: gic-v5: Add IRS IODEV support to MMIO
 handlers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[07-03 16:00]** [PATCH v3 19/40] KVM: arm64: gic-v5: Add KVM_VGIC_V5_ADDR_TYPE_IRS to
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[07-03 16:00]** [PATCH v3 20/40] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[07-03 16:01]** [PATCH v3 21/40] KVM: arm64: gic-v5: Initialise per-VM IRS state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[07-03 16:01]** [PATCH v3 22/40] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[07-03 16:02]** [PATCH v3 23/40] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[07-03 16:02]** [PATCH v3 24/40] KVM: arm64: selftests: Update vGICv5 selftest to set
 IRS address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[07-03 16:03]** [PATCH v3 25/40] KVM: arm64: gic-v5: Introduce SPI AP list
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[07-03 16:03]** [PATCH v3 26/40] KVM: arm64: gic-v5: Add GIC VDPEND and GIC VDRCFG
 hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[07-03 16:04]** [PATCH v3 27/40] KVM: arm64: gic-v5: Track SPI state for in-flight
 SPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[07-03 16:04]** [PATCH v3 28/40] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[07-03 16:05]** [PATCH v3 29/40] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[07-03 16:05]** [PATCH v3 30/40] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[07-03 16:06]** [PATCH v3 31/40] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[07-03 16:06]** [PATCH v3 32/40] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[07-03 16:07]** [PATCH v3 33/40] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg userspace
 accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[07-03 16:07]** [PATCH v3 34/40] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[07-03 16:08]** [PATCH v3 35/40] KVM: arm64: gic-v5: Add CoreSight MMIO regs to IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[07-03 16:08]** [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[07-03 16:09]** [PATCH v3 37/40] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[07-03 16:09]** [PATCH v3 38/40] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[07-03 16:10]** [PATCH v3 39/40] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[07-03 16:10]** [PATCH v3 40/40] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
42. **[07-03 16:22]** Re: [PATCH v3 06/40] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: sashiko-bot@kernel.org
43. **[07-03 16:23]** Re: [PATCH v3 15/40] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: sashiko-bot@kernel.org
44. **[07-03 16:24]** Re: [PATCH v3 02/40] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: sashiko-bot@kernel.org
45. **[07-03 16:25]** Re: [PATCH v3 08/40] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: sashiko-bot@kernel.org
46. **[07-03 16:26]** Re: [PATCH v3 13/40] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: sashiko-bot@kernel.org
47. **[07-03 16:27]** Re: [PATCH v3 14/40] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: sashiko-bot@kernel.org
48. **[07-03 16:27]** Re: [PATCH v3 30/40] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: sashiko-bot@kernel.org
49. **[07-03 16:28]** Re: [PATCH v3 05/40] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: sashiko-bot@kernel.org
50. **[07-03 16:31]** Re: [PATCH v3 26/40] KVM: arm64: gic-v5: Add GIC VDPEND and GIC
 VDRCFG hyp calls
   - 发件人: sashiko-bot@kernel.org
51. **[07-03 16:31]** Re: [PATCH v3 09/40] KVM: arm64: gic-v5: Create and manage VM and
 VPE tables
   - 发件人: sashiko-bot@kernel.org
52. **[07-03 16:32]** Re: [PATCH v3 28/40] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: sashiko-bot@kernel.org
53. **[07-03 16:33]** Re: [PATCH v3 01/40] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: sashiko-bot@kernel.org
54. **[07-03 16:33]** Re: [PATCH v3 40/40] Documentation: KVM: Add the VGICv5 IRS
 save/restore sequences
   - 发件人: sashiko-bot@kernel.org
55. **[07-03 16:34]** Re: [PATCH v3 23/40] KVM: arm64: gic-v5: Set IRICHPPIDIS based on
 IRS enable state
   - 发件人: sashiko-bot@kernel.org
56. **[07-03 16:34]** Re: [PATCH v3 10/40] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: sashiko-bot@kernel.org
57. **[07-03 16:35]** Re: [PATCH v3 16/40] KVM: arm64: gic-v5: Request doorbells when
 VPEs enter WFI
   - 发件人: sashiko-bot@kernel.org
58. **[07-03 16:36]** Re: [PATCH v3 31/40] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: sashiko-bot@kernel.org
59. **[07-03 16:36]** Re: [PATCH v3 37/40] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: sashiko-bot@kernel.org
60. **[07-03 16:37]** Re: [PATCH v3 38/40] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: sashiko-bot@kernel.org
61. **[07-03 16:38]** Re: [PATCH v3 20/40] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and
 MMIO emulation
   - 发件人: sashiko-bot@kernel.org
62. **[07-03 16:39]** Re: [PATCH v3 11/40] KVM: arm64: gic-v5: Implement VMT/vIST IRS
 MMIO Ops
   - 发件人: sashiko-bot@kernel.org
63. **[07-03 16:41]** Re: [PATCH v3 35/40] KVM: arm64: gic-v5: Add CoreSight MMIO regs to
 IRS
   - 发件人: sashiko-bot@kernel.org
64. **[07-03 16:41]** Re: [PATCH v3 27/40] KVM: arm64: gic-v5: Track SPI state for
 in-flight SPIs
   - 发件人: sashiko-bot@kernel.org
65. **[07-03 16:42]** Re: [PATCH v3 34/40] KVM: arm64: gic-v5: Handle userspace accesses
 to IRS MMIO region
   - 发件人: sashiko-bot@kernel.org
66. **[07-03 16:43]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: sashiko-bot@kernel.org
67. **[07-03 16:47]** Re: [PATCH v3 22/40] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: sashiko-bot@kernel.org
68. **[07-03 16:53]** Re: [PATCH v3 29/40] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: sashiko-bot@kernel.org

---

### Thread 2: [PATCH 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3

**📧 邮件数**: 55 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  2 Jul 2026 17:02:20 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM (Kernel-based Virtual Machine) 的 arm64 架构的多个补丁，主要集中在对嵌套虚拟化支持的增强，特别是 FEAT_NV2p1 和 FEAT_NV3 的实现。

**原始补丁内容**：
补丁系列的核心是添加对 FEAT_NV2p1 和 FEAT_NV3 的支持。FEAT_NV2p1 主要是修复在嵌套虚拟化配置下，EL1 访问某些寄存器时缺失的状态位，从而减少陷阱的数量。FEAT_NV3 则通过引入新的寄存器 NVHCR_EL2，改变了 ERET 的行为，允许更高效的处理。

**之前讨论要点**：
在历史讨论中，参与者们探讨了如何在现有的 KVM 代码中实现这些新特性，并对其潜在的性能提升进行了评估。Marc Zyngier 提到，虽然这些改进在某些情况下可以显著减少指令数量，但仍需谨慎对待其实际效果。

**本周的新讨论与进展**：
本周的讨论中，Marc Zyngier 提出了多个补丁，涵盖了对寄存器的描述、特性检测、以及如何在 KVM 中处理这些新寄存器的上下文切换等。具体补丁包括：
- 增加对 NVHCR_EL2 的处理和上下文切换支持。
- 实现 FEAT_NV3 的检测和暴露给嵌套虚拟化的客人。
- 讨论了如何在不同的虚拟化上下文中优化 ERET 和 TLBI 指令的处理。

此外，邮件中还提到了一些潜在的代码问题和改进建议，表明开发者们对补丁的质量和稳定性保持高度关注。整体来看，本周的讨论推动了对嵌套虚拟化支持的进一步完善。

#### 📝 邮件列表

1. **[07-02 17:02]** [PATCH 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-02 17:02]** [PATCH 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-02 17:02]** [PATCH 02/28] arm64: Update ID_AA64MMFR4_EL1 description to 2026-03 JSON release
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-02 17:02]** [PATCH 03/28] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-02 17:02]** [PATCH 04/28] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-02 17:02]** [PATCH 05/28] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-02 17:02]** [PATCH 06/28] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL register
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-02 17:02]** [PATCH 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-02 17:02]** [PATCH 08/28] arm64: Add ARM64_HAS_NV2P1 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-02 17:02]** [PATCH 09/28] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-02 17:02]** [PATCH 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[07-02 17:02]** [PATCH 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-02 17:02]** [PATCH 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[07-02 17:02]** [PATCH 13/28] arm64: sysreg: Add NVHCR_EL2 description as a mirror of HCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-02 17:02]** [PATCH 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[07-02 17:02]** [PATCH 15/28] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-02 17:02]** [PATCH 16/28] KVM: arm64: Split NV-specific exit fixups from the non-NV handling
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[07-02 17:02]** [PATCH 17/28] KVM: arm64: Add NV3 control bits to HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[07-02 17:02]** [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[07-02 17:02]** [PATCH 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[07-02 17:02]** [PATCH 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[07-02 17:02]** [PATCH 21/28] KVM: arm64: Add NVHCR_EL2 handling to the sysreg array
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[07-02 17:02]** [PATCH 22/28] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[07-02 17:02]** [PATCH 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[07-02 17:02]** [PATCH 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[07-02 17:02]** [PATCH 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[07-02 17:02]** [PATCH 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[07-02 17:02]** [PATCH 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[07-02 17:02]** [PATCH 28/28] arm64: Add override for ID_AA64MMFR4_EL1.NV_frac
   - 发件人: Marc Zyngier <maz@kernel.org>
30. **[07-02 16:19]** Re: [PATCH 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping
 definitions
   - 发件人: sashiko-bot@kernel.org
31. **[07-02 16:21]** Re: [PATCH 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: sashiko-bot@kernel.org
32. **[07-02 16:24]** Re: [PATCH 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV on ERET
 fast path
   - 发件人: sashiko-bot@kernel.org
33. **[07-02 16:25]** Re: [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: sashiko-bot@kernel.org
34. **[07-02 16:26]** Re: [PATCH 22/28] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: sashiko-bot@kernel.org
35. **[07-02 16:28]** Re: [PATCH 05/28] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2
 sanitisation
   - 发件人: sashiko-bot@kernel.org
36. **[07-02 16:28]** Re: [PATCH 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: sashiko-bot@kernel.org
37. **[07-02 16:34]** Re: [PATCH 03/28] KVM: arm64: Merge guest's HCRX_EL2 using
 NV_HCRX_GUEST_EXCLUDE
   - 发件人: sashiko-bot@kernel.org
38. **[07-02 16:39]** Re: [PATCH 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: sashiko-bot@kernel.org
39. **[07-02 16:39]** Re: [PATCH 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: sashiko-bot@kernel.org
40. **[07-02 16:43]** Re: [PATCH 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: sashiko-bot@kernel.org
41. **[07-02 16:45]** Re: [PATCH 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: sashiko-bot@kernel.org
42. **[07-02 18:41]** Re: [PATCH 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
43. **[07-02 18:46]** Re: [PATCH 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[07-02 18:57]** Re: [PATCH 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[07-02 19:01]** Re: [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[07-02 19:14]** Re: [PATCH 22/28] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: Marc Zyngier <maz@kernel.org>
47. **[07-02 19:18]** Re: [PATCH 05/28] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
48. **[07-02 19:23]** Re: [PATCH 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
49. **[07-02 19:29]** Re: [PATCH 03/28] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
50. **[07-02 18:34]** Re: [PATCH 04/28] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: sashiko-bot@kernel.org
51. **[07-02 21:01]** Re: [PATCH 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
52. **[07-02 21:03]** Re: [PATCH 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
53. **[07-02 21:28]** Re: [PATCH 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
54. **[07-02 22:04]** Re: [PATCH 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
55. **[07-02 22:10]** Re: [PATCH 04/28] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 3: [PATCH v2 00/13] KVM Dirty-bit cleaning hw accelerator (HACDBS)

**📧 邮件数**: 49 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 29 Jun 2026 12:17:48 +0100

#### 🤖 AI 总结

本邮件讨论主题为「KVM Dirty-bit 清理硬件加速器（HACDBS）」，主要围绕一系列补丁（PATCH v2 00/13至PATCH v2 13/13）进行技术讨论。

1. **原始补丁内容**：
   该补丁集旨在创建一个架构通用的脏位清理加速接口，并在此基础上实现针对 arm64 的 HACDBS 加速器。该实现能够加速 KVM 中脏位图和脏环的清理过程。

2. **历史讨论要点**：
   之前的讨论集中在如何实现和测试这一补丁集，特别是它依赖于尚未合并的 HDBSS 补丁集。参与者们讨论了如何确保补丁在合并时准备就绪，并收集反馈以改进实现和测试方法。

3. **本周新讨论及进展**：
   - **补丁实现**：补丁实现了多个功能，包括检测和初始化 HACDBSIRQ、添加基础清理例程、实现硬件加速的脏位清理和脏环清理等。
   - **性能测试**：初步测试显示，使用 HACDBS 的清理速度显著提升，尤其是在处理大内存时。
   - **问题反馈**：Sashiko AI 进行了代码审查，指出了多处潜在问题，包括缺乏上下文同步事件、可能的死锁情况等，开发者们积极响应并计划在后续版本中修复这些问题。
   - **技术细节讨论**：参与者们就如何处理脏位图、如何有效管理内存和 IRQ 进行深入讨论，提出了多种优化建议。

整体而言，本周的讨论推动了 HACDBS 补丁集的进展，并为后续版本的改进奠定了基础。

#### 📝 邮件列表

1. **[06-29 12:17]** [PATCH v2 00/13] KVM Dirty-bit cleaning hw accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[06-29 12:17]** [PATCH v2 01/13] KVM: arm64: HDBSS bits
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[06-29 12:17]** [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[06-29 12:17]** [PATCH v2 03/13] arm64/cpufeature: Add system-wide FEAT_HACDBS detection
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[06-29 12:17]** [PATCH v2 04/13] arm64/sysreg: Add HACDBS consumer and base registers
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[06-29 12:17]** [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[06-29 12:17]** [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[06-29 12:17]** [PATCH v2 07/13] kvm: Add arch-generic interface for hw-accelerated dirty-bitmap cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[06-29 12:17]** [PATCH v2 08/13] KVM: arm64: Add hardware-accelerated dirty-bitmap cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[06-29 12:17]** [PATCH v2 09/13] KVM: arm64: Dirty-bitmap: avoid splitting previously split blocks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[06-29 12:17]** [PATCH v2 10/13] kvm/dirty_ring: Introduce get_memslot and move helpers to header
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[06-29 12:17]** [PATCH v2 11/13] kvm/dirty_ring: Add arch-generic interface for hw-accelerated dirty-ring cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[06-29 12:18]** [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[06-29 12:18]** [PATCH v2 13/13] KVM: arm64: Enable KVM_HW_DIRTY_BIT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
15. **[06-29 11:29]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS
 cleaning routine
   - 发件人: sashiko-bot@kernel.org
16. **[06-29 11:32]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize
 HACDBSIRQ
   - 发件人: sashiko-bot@kernel.org
17. **[06-29 11:34]** Re: [PATCH v2 01/13] KVM: arm64: HDBSS bits
   - 发件人: sashiko-bot@kernel.org
18. **[06-29 11:36]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: sashiko-bot@kernel.org
19. **[06-29 11:38]** Re: [PATCH v2 07/13] kvm: Add arch-generic interface for
 hw-accelerated dirty-bitmap cleaning
   - 发件人: sashiko-bot@kernel.org
20. **[06-29 11:39]** Re: [PATCH v2 09/13] KVM: arm64: Dirty-bitmap: avoid splitting
 previously split blocks
   - 发件人: sashiko-bot@kernel.org
21. **[06-29 11:45]** Re: [PATCH v2 08/13] KVM: arm64: Add hardware-accelerated
 dirty-bitmap cleaning routine
   - 发件人: sashiko-bot@kernel.org
22. **[06-29 11:49]** Re: [PATCH v2 11/13] kvm/dirty_ring: Add arch-generic interface for
 hw-accelerated dirty-ring cleaning
   - 发件人: sashiko-bot@kernel.org
23. **[06-29 11:49]** Re: [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated
 dirty-ring cleaning routine
   - 发件人: sashiko-bot@kernel.org
24. **[06-29 11:52]** Re: [PATCH v2 13/13] KVM: arm64: Enable KVM_HW_DIRTY_BIT
   - 发件人: sashiko-bot@kernel.org
25. **[06-29 13:57]** Re: [PATCH v2 01/13] KVM: arm64: HDBSS bits
   - 发件人: Leonardo Bras <leo.bras@arm.com>
26. **[06-29 15:47]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
27. **[06-29 16:43]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
28. **[06-29 16:54]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
29. **[06-29 17:07]** Re: [PATCH v2 07/13] kvm: Add arch-generic interface for hw-accelerated dirty-bitmap cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
30. **[06-29 17:49]** Re: [PATCH v2 08/13] KVM: arm64: Add hardware-accelerated dirty-bitmap cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
31. **[06-29 17:52]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize
 HACDBSIRQ
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
32. **[06-29 10:06]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
33. **[06-29 18:07]** Re: [PATCH v2 09/13] KVM: arm64: Dirty-bitmap: avoid splitting previously split blocks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
34. **[06-29 18:09]** Re: [PATCH v2 11/13] kvm/dirty_ring: Add arch-generic interface for hw-accelerated dirty-ring cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
35. **[06-29 10:22]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize
 HACDBSIRQ
   - 发件人: Oliver Upton <oupton@kernel.org>
36. **[06-29 18:26]** Re: [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
37. **[06-29 10:36]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS
 cleaning routine
   - 发件人: Oliver Upton <oupton@kernel.org>
38. **[06-30 13:58]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
39. **[06-30 15:50]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
40. **[06-30 15:52]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
41. **[06-30 15:59]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
42. **[06-30 08:44]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
43. **[06-30 09:03]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize
 HACDBSIRQ
   - 发件人: Oliver Upton <oupton@kernel.org>
44. **[06-30 18:09]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
45. **[06-30 18:19]** Re: [PATCH v2 05/13] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
46. **[06-30 11:43]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
47. **[06-30 12:06]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS
 cleaning routine
   - 发件人: Oliver Upton <oupton@kernel.org>
48. **[07-01 11:45]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
49. **[07-01 11:47]** Re: [PATCH v2 06/13] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 4: [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception Masking

**📧 邮件数**: 33 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 3 Jul 2026 18:01:18 +0800

#### 🤖 AI 总结

本邮件线程讨论了对 ARM64 架构的 NMI（非屏蔽中断）支持及异常屏蔽机制的重构，主要内容包括一系列补丁（patch）的提交和讨论。

1. **原始问题和补丁内容**：
   - 本系列补丁旨在实现对 ARMv8.8-A/v9.3-A 硬件 NMI 扩展（FEAT_NMI）的支持，并重构异常屏蔽管理。补丁通过引入 PSTATE.ALLINT 来管理 ARM64 上的超优先级中断。

2. **历史讨论要点**：
   - 之前的讨论指出，现有的 NMI 实现与 DAIF（中断屏蔽标志）管理代码结合不当，导致维护困难。Mark Rutland 强调在添加真正的 NMI 支持之前，必须清理现有的方法。

3. **本周的新讨论和进展**：
   - 本周的讨论集中在补丁的具体实现上，包括对异常屏蔽的重构、引入新的抽象帮助函数、以及对 NMI 的管理。补丁中还包括对 GIC（通用中断控制器）支持 NMI 的实现，确保 NMI 在硬件和软件层面都能正确处理。
   - 参与者对补丁的细节提出了反馈和建议，包括对代码的可读性、性能优化和潜在的错误修复。Sashiko AI 也对多个补丁进行了审查，指出了一些潜在问题。

总体来看，该系列补丁的目标是为 ARM64 架构提供更清晰、可维护的 NMI 支持，同时确保在处理异常时的高效性和准确性。

#### 📝 邮件列表

1. **[07-03 18:01]** [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception Masking
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
2. **[07-03 18:01]** [PATCH 01/17] arm64: Move DAIF macros to ptrace.h and use them centrally
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
3. **[07-03 18:01]** [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
4. **[07-03 18:01]** [PATCH 03/17] arm64: entry: arm64: entry: Move DAIF masking for EL1 exit to C code
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
5. **[07-03 18:01]** [PATCH 04/17] arm64: entry: Add entry-specific helpers
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
6. **[07-03 18:01]** [PATCH 05/17] arm64: Introduce helpers for restoring standard exception masks
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
7. **[07-03 18:01]** [PATCH 06/17] arm64/booting: Document boot requirements for FEAT_NMI
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
8. **[07-03 18:01]** [PATCH 07/17] arm64/sysreg: Add definitions for immediate versions of MSR ALLINT
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
9. **[07-03 18:01]** [PATCH 08/17] arm64/hyp-stub: Enable access to ALLINT
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
10. **[07-03 18:01]** [PATCH 09/17] arm64/idreg: Add an override for FEAT_NMI
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
11. **[07-03 18:01]** [PATCH 10/17] arm64/cpufeature: Detect PE support for FEAT_NMI
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
12. **[07-03 18:01]** [PATCH 11/17] KVM: arm64: Hide FEAT_NMI from guests
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
13. **[07-03 18:01]** [PATCH 12/17] arm64/nmi: Manage masking for superpriority interrupts along with DAIF
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
14. **[07-03 18:01]** [PATCH 13/17] arm64/entry: Don't call preempt_schedule_irq() with NMIs masked
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
15. **[07-03 18:01]** [PATCH 14/17] arm64/irq: Document handling of FEAT_NMI in irqflags.h
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
16. **[07-03 18:01]** [PATCH 15/17] arm64/nmi: Add handling of superpriority interrupts as NMIs
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
17. **[07-03 18:01]** [PATCH 16/17] arm64/nmi: Add Kconfig for NMI
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
18. **[07-03 18:01]** [PATCH 17/17] irqchip/gic-v3: Implement FEAT_GICv3_NMI support
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
19. **[07-03 10:13]** Re: [PATCH 11/17] KVM: arm64: Hide FEAT_NMI from guests
   - 发件人: sashiko-bot@kernel.org
20. **[07-03 10:15]** Re: [PATCH 06/17] arm64/booting: Document boot requirements for
 FEAT_NMI
   - 发件人: sashiko-bot@kernel.org
21. **[07-03 10:15]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract
 logical mask
   - 发件人: sashiko-bot@kernel.org
22. **[07-03 10:16]** Re: [PATCH 08/17] arm64/hyp-stub: Enable access to ALLINT
   - 发件人: sashiko-bot@kernel.org
23. **[07-03 10:17]** Re: [PATCH 04/17] arm64: entry: Add entry-specific helpers
   - 发件人: sashiko-bot@kernel.org
24. **[07-03 10:18]** Re: [PATCH 07/17] arm64/sysreg: Add definitions for immediate
 versions of MSR ALLINT
   - 发件人: sashiko-bot@kernel.org
25. **[07-03 10:19]** Re: [PATCH 15/17] arm64/nmi: Add handling of superpriority
 interrupts as NMIs
   - 发件人: sashiko-bot@kernel.org
26. **[07-03 10:20]** Re: [PATCH 09/17] arm64/idreg: Add an override for FEAT_NMI
   - 发件人: sashiko-bot@kernel.org
27. **[07-03 10:25]** Re: [PATCH 17/17] irqchip/gic-v3: Implement FEAT_GICv3_NMI support
   - 发件人: sashiko-bot@kernel.org
28. **[07-03 10:27]** Re: [PATCH 12/17] arm64/nmi: Manage masking for superpriority
 interrupts along with DAIF
   - 发件人: sashiko-bot@kernel.org
29. **[07-03 10:28]** Re: [PATCH 16/17] arm64/nmi: Add Kconfig for NMI
   - 发件人: sashiko-bot@kernel.org
30. **[07-03 14:38]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
31. **[07-03 14:48]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
32. **[07-03 15:15]** Re: [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception
 Masking
   - 发件人: Mark Rutland <mark.rutland@arm.com>
33. **[07-03 09:44]** Re: [PATCH 01/17] arm64: Move DAIF macros to ptrace.h and use them
 centrally
   - 发件人: Breno Leitao <leitao@debian.org>

---

### Thread 5: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes

**📧 邮件数**: 21 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 30 Jun 2026 13:09:59 +0100

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes”，主要围绕修复 KVM 的影子页面表转储（ptdump）相关问题展开。

**原始 patch/问题的内容**：
Wei-Lin Chang 提出了一个补丁系列，旨在修复影子 ptdump 的调试文件，特别是由于嵌套 MMU 可能在文件打开时被释放而导致的使用后释放（UAF）问题。补丁将多个 per MMU 的 ptdump 文件合并为一个名为“shadow_page_tables”的文件，以简化管理并避免上次讨论中发现的 dentry UAF 问题。

**之前讨论要点**：
在之前的讨论中，参与者指出了影子 ptdump 文件的创建和删除过程存在问题，尤其是在 MMU 锁持有的情况下，调试文件的创建和删除可能会导致休眠，从而引发潜在的错误。补丁的设计旨在解决这些问题，并确保 ptdump 文件的生命周期与其他文件一致。

**本周的新讨论、进展或结论**：
本周的讨论集中在补丁的具体实现上，包括对 UAF 问题的修复、初始化代码的提取以及如何处理嵌套 MMU 的信息输出。参与者对补丁的细节提出了问题和建议，特别是关于如何处理锁和内存释放的问题。Wei-Lin Chang 解释了补丁的设计思路，并回应了关于补丁行为的疑问。整体来看，补丁系列得到了积极的反馈，尽管仍有一些潜在问题需要进一步讨论和解决。

#### 📝 邮件列表

1. **[06-30 13:09]** [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[06-30 13:10]** [PATCH v2 1/6] KVM: arm64: ptdump: Remove shadow ptdump files
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[06-30 13:10]** [PATCH v2 2/6] KVM: arm64: ptdump: Undo making the ptdump code mmu aware
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[06-30 13:10]** [PATCH v2 3/6] KVM: arm64: ptdump: Fix UAF when mmu->pgt is freed
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[06-30 13:10]** [PATCH v2 4/6] KVM: arm64: ptdump: Factor out initialization of kvm_ptdump_guest_state
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[06-30 13:10]** [PATCH v2 5/6] KVM: arm64: ptdump: Extract kvm_ptdump_guest_open() from canonical ptdump path
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[06-30 13:10]** [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump file
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[06-30 12:27]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: sashiko-bot@kernel.org
9. **[07-01 16:00]** Re: [PATCH v2 3/6] KVM: arm64: ptdump: Fix UAF when mmu->pgt is freed
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[07-01 16:28]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump file
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-01 18:27]** Re: [PATCH v2 3/6] KVM: arm64: ptdump: Fix UAF when mmu->pgt is freed
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
12. **[07-01 18:35]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
13. **[07-02 15:55]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
14. **[07-02 08:41]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
15. **[07-02 11:58]** Re: [PATCH v2 3/6] KVM: arm64: ptdump: Fix UAF when mmu->pgt is freed
   - 发件人: Leonardo Bras <leo.bras@arm.com>
16. **[07-02 12:00]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump file
   - 发件人: Leonardo Bras <leo.bras@arm.com>
17. **[07-03 06:48]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
18. **[07-03 08:02]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
19. **[07-03 10:26]** Re: [PATCH v2 3/6] KVM: arm64: ptdump: Fix UAF when mmu->pgt is freed
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
20. **[07-03 11:24]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
21. **[07-03 11:27]** Re: [PATCH v2 6/6] KVM: arm64: ptdump: Introduce the shadow ptdump
 file
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 6: [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 21 | **👥 参与者**: 6 | **📅 开始时间**: Wed, 17 Jun 2026 14:51:23 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A 和 KVM 的一系列补丁（PATCH v7 0/7），主要集中在修复 Endpoint Memory Access Descriptor（EMAD）偏移计算和增强边界检查。补丁的背景是，FF-A 规范在版本 1.1 之前未明确指定 EMAD 的偏移量，导致假设其紧随内存区域头部，但从 1.1 版本起，需使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。

在历史讨论中，参与者们对补丁的多个方面进行了审查和反馈，特别是对内存对齐和参数验证的必要性进行了强调。Sebastian Ene 提出了多个补丁，旨在确保 FF-A 调用的参数正确性和安全性。

在本周的新讨论中，参与者们继续审查补丁，提出了一些潜在问题，例如在处理 `FFA_NOTIFICATION_UNBIND` 和 `FFA_NOTIFICATION_SET` 时的参数验证不足。此外，Sashiko AI 评审工具也发现了一些问题，包括内存腐败和数据竞争的风险。尽管存在这些问题，Will Deacon 表示对某些补丁的认可，并认为不需要更改。

总体而言，本周的讨论集中在补丁的细节审查和潜在问题的识别上，推动了对 ARM FF-A 和 KVM 的进一步完善。

#### 📝 邮件列表

1. **[06-17 14:51]** [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-17 14:51]** [PATCH v7 1/7] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-17 14:51]** [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-18 18:09]** Re: [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[06-29 10:53]** Re: [PATCH v7 1/7] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Jens Wiklander <jens.wiklander@linaro.org>
6. **[06-29 09:35]** [PATCH v7 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-29 09:35]** [PATCH v7 1/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-29 09:35]** [PATCH v7 2/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-29 09:35]** [PATCH v7 3/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
10. **[06-29 09:35]** [PATCH v7 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
11. **[06-29 09:35]** [PATCH v7 5/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
12. **[06-29 09:35]** [PATCH v7 6/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
13. **[06-29 09:35]** [PATCH v7 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
14. **[06-29 10:16]** Re: [PATCH v7 3/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in
 host handler
   - 发件人: sashiko-bot@kernel.org
15. **[06-29 10:25]** Re: [PATCH v7 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host
 handler
   - 发件人: sashiko-bot@kernel.org
16. **[06-29 12:46]** Re: [PATCH v7 6/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in
 host handler
   - 发件人: sashiko-bot@kernel.org
17. **[06-29 12:58]** Re: [PATCH v7 7/7] KVM: arm64: Enforce strict SBZ checks in the
 FF-A proxy
   - 发件人: sashiko-bot@kernel.org
18. **[06-29 15:17]** Re: [PATCH v7 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Will Deacon <will@kernel.org>
19. **[06-30 09:51]** Re: [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Sebastian Ene <sebastianene@google.com>
20. **[06-30 10:13]** Re: [PATCH v7 1/7] optee: ffa: Add NULL check in
 optee_ffa_lend_protmem
   - 发件人: Sebastian Ene <sebastianene@google.com>
21. **[06-30 10:22]** Re: [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 7: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT

**📧 邮件数**: 16 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 23 Jun 2026 11:41:39 -0700

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现 FEAT_HAFDBS 和 FEAT_HAFT 的补丁（patch）系列。该补丁主要目的是为嵌套 MMU（内存管理单元）提供对硬件脏状态和访问标志的支持，以改善虚拟化性能。

在历史讨论中，Oliver Upton 提出了这一补丁系列，并指出现有的 KVM 对硬件描述符更新的支持不足，特别是在大多数可用的 NV2 硬件缺乏 HAFDBS 功能的情况下。讨论中提到，HAFDBS 和 HAFT 的实现对于提高性能和减少系统的实时迁移影响至关重要。参与者们对补丁的细节进行了深入探讨，包括如何在 stage-1 页面表中标记脏状态等问题。

在本周的新讨论中，参与者们对补丁的理解进行了澄清，Leonardo Bras 和 Oliver Upton 之间的交流表明，他们对补丁的目的和实现有了更清晰的认识。此外，Wei-Lin Chang 对于处理写入权限的缓存维护操作（CMO）提出了问题，Oliver 对此进行了详细解答，强调了在嵌套环境下处理这些操作的复杂性。

总体来看，本周的讨论主要集中在对补丁的理解和实现细节的澄清上，参与者们对补丁的潜在影响和性能改进表示关注。

#### 📝 邮件列表

1. **[06-23 11:41]** [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-23 11:41]** [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-23 11:42]** [PATCH 22/22] HACK: KVM: arm64: nv: Set the dirty state for CMOs that fetch for write
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-26 16:31]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[06-26 16:49]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[06-26 17:03]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[06-26 18:12]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[06-26 10:35]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[06-26 10:45]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[06-29 11:29]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[06-29 11:37]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[06-29 11:38]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[06-29 11:39]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[07-01 11:16]** Re: [PATCH 22/22] HACK: KVM: arm64: nv: Set the dirty state for CMOs
 that fetch for write
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
15. **[07-01 10:33]** Re: [PATCH 22/22] HACK: KVM: arm64: nv: Set the dirty state for CMOs
 that fetch for write
   - 发件人: Oliver Upton <oupton@kernel.org>
16. **[07-02 07:50]** Re: [PATCH 22/22] HACK: KVM: arm64: nv: Set the dirty state for CMOs
 that fetch for write
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 8: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y

**📧 邮件数**: 15 | **👥 参与者**: 5 | **📅 开始时间**: Wed,  1 Jul 2026 20:43:37 +0000

#### 🤖 AI 总结

本邮件线程讨论了将 ARM64 VHE 启动修复程序回溯到 6.6.y 稳定版本的补丁系列（共 5 个补丁）。这些修复程序在 6.12.y 及更新版本中已存在，但在 6.6.y 中缺失，导致启用嵌套虚拟化的 L1 客户端无法正常启动，因其 HCR_EL2.E2H 配置不当，可能导致启动挂起或陷阱循环。

历史讨论中，补丁的主要内容包括对 HCR_EL2.E2H 的早期初始化和对 ID_AA64MMFR4_EL1 的处理，以确保在不同 CPU 特性下的兼容性。补丁还解决了在 KVM PSCI 入口点中未初始化 HCR_EL2.E2H 的问题。

本周的新讨论中，参与者针对补丁的细节进行了深入探讨，包括解决冲突的方式、补丁的有效性以及对不同 CPU 实现的兼容性。Oliver Upton 提出需要检查所有 KVM 模式的测试情况，并质疑为何仅针对 6.6.y 进行回溯，建议考虑更早的版本。同时，邮件中也提到了一些代码审查的反馈，指出了潜在的代码问题和改进建议。

总体来看，本周的讨论集中在补丁的实施细节及其对不同版本的影响上，参与者们积极提出建议以确保补丁的有效性和稳定性。

#### 📝 邮件列表

1. **[07-01 20:43]** [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-01 20:43]** [PATCH 1/5] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[07-01 20:43]** [PATCH 2/5] arm64: Treat HCR_EL2.E2H as RES1 when ID_AA64MMFR4_EL1.E2H0
 is negative
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[07-01 20:43]** [PATCH 3/5] arm64: Fix early handling of FEAT_E2H0 not being implemented
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[07-01 20:43]** [PATCH 4/5] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[07-01 20:43]** [PATCH 5/5] arm64: Revamp HCR_EL2.E2H RES1 detection
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[07-01 20:52]** Re: [PATCH 3/5] arm64: Fix early handling of FEAT_E2H0 not being
 implemented
   - 发件人: sashiko-bot@kernel.org
8. **[07-01 20:53]** Re: [PATCH 4/5] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: sashiko-bot@kernel.org
9. **[07-01 20:56]** Re: [PATCH 2/5] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: sashiko-bot@kernel.org
10. **[07-01 16:23]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[07-01 16:30]** Re: [PATCH 2/5] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[07-01 16:45]** Re: [PATCH 4/5] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[07-01 17:01]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[07-01 20:38]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Sasha Levin <sashal@kernel.org>
15. **[07-02 08:16]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Greg KH <gregkh@linuxfoundation.org>

---

### Thread 9: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Wed,  1 Jul 2026 19:24:28 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“记录 pKVM 阶段 2 映射是否可缓存”。该补丁旨在解决 pKVM 在处理阶段 2 操作时未能正确检查页表条目（PTE）属性的问题，具体是通过记录映射是否可缓存，从而避免对不可缓存映射进行缓存维护。

在历史讨论中，补丁的背景未详细列出，但本周的讨论集中在补丁的实现细节和审查过程上。参与者们对补丁的结构和变更日志提出了改进建议，强调了遵循补丁提交流程的重要性，以便于审查和反馈。

本周的新讨论中，Bradley Morgan 提出了补丁的具体实现，并在回应中承认未能正确抄送之前的审查者。Marc Zyngier 和 Leonardo Bras 强调了补丁变更日志的重要性，并讨论了补丁的优化和修复性质。最终，Marc 表示将审查该补丁，并在讨论结束后准备提交下一个版本（V5）。此外，关于是否需要“Fixes”标签的讨论也引发了不同看法，Marc 认为该标签是必要的，以确保补丁的修复性质被明确标识。

总体而言，本周的讨论围绕补丁的细节、审查流程和补丁的修复与优化性质展开，参与者们积极交流以推动补丁的完善。

#### 📝 邮件列表

1. **[07-01 19:24]** [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[07-02 09:59]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-02 12:18]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[07-02 15:52]** =?US-ASCII?Q?Re=3A_=5BPATCH_v4=5D_KVM=3A_arm64=3A_Record_whe?=
 =?US-ASCII?Q?ther_pKVM_stage_2_mapping_is_cacheable?=
   - 发件人: Bradley Morgan <include@grrlz.net>
5. **[07-02 16:13]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[07-02 16:34]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-03 17:59]** =?US-ASCII?Q?Re=3A_=5BPATCH_v4=5D_KVM=3A_arm64=3A_Record_whe?=
 =?US-ASCII?Q?ther_pKVM_stage_2_mapping_is_cacheable?=
   - 发件人: Bradley Morgan <include@grrlz.net>
8. **[07-05 19:38]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is
 cacheable
   - 发件人: Dev Jain <dev.jain@arm.com>
9. **[07-05 15:12]** =?US-ASCII?Q?Re=3A_=5BPATCH_v4=5D_KVM=3A_arm64=3A_Record_whe?=
 =?US-ASCII?Q?ther_pKVM_stage_2_mapping_is_cacheable?=
   - 发件人: Bradley Morgan <include@grrlz.net>
10. **[07-05 20:27]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-05 20:29]** =?US-ASCII?Q?Re=3A_=5BPATCH_v4=5D_KVM=3A_arm64=3A_Record_whe?=
 =?US-ASCII?Q?ther_pKVM_stage_2_mapping_is_cacheable?=
   - 发件人: Bradley Morgan <include@grrlz.net>
12. **[07-05 21:13]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-05 21:17]** =?US-ASCII?Q?Re=3A_=5BPATCH_v4=5D_KVM=3A_arm64=3A_Record_whe?=
 =?US-ASCII?Q?ther_pKVM_stage_2_mapping_is_cacheable?=
   - 发件人: Bradley Morgan <include@grrlz.net>

---

### Thread 10: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory

**📧 邮件数**: 12 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 25 Jun 2026 23:53:32 +1000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构下的 RMI（Runtime Memory Interface）内存运行时故障处理的补丁（PATCH v14 29/44）。该补丁旨在解决在共享空间中处理二级页故障时出现的问题，特别是 virtio-net-pci 设备的数据未能正确传递给 QEMU 的情况。

在历史讨论中，参与者们探讨了补丁的潜在问题，特别是关于权限故障和 MAP_PRIVATE 映射的处理。Gavin Shan 和 Suzuki K Poulose 讨论了如何在共享空间中处理写权限的问题，指出强制写权限可能导致虚拟机监控器（VMM）无法正确识别页面。此外，Lorenzo Pieralisi 提到需要对 KVM 驱动进行修复，以解决在此系列补丁中发现的错误。

在本周的新讨论中，Lorenzo 提到在使用私有内存后端进行测试时，网络接口正常工作，表明补丁的某些问题得到了改善。Kohei Enju 询问了是否计划支持 MEC 策略的选择，Steven Price 表示希望先将基础功能推送到主线，再考虑其他特性。整体来看，讨论显示出对补丁的持续关注和对未来版本（v15）的期待。

#### 📝 邮件列表

1. **[06-25 23:53]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
2. **[06-25 16:58]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[06-26 17:43]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
4. **[06-26 09:47]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[06-26 21:43]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
6. **[06-26 18:44]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
7. **[06-28 20:33]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
8. **[07-01 11:15]** Re: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
9. **[07-01 11:53]** Re: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
10. **[07-01 15:58]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
11. **[07-02 22:49]** Re: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
12. **[07-04 09:36]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>

---

### Thread 11: [PATCH v3 0/3] KVM: arm64: fix pKVM mapping cache corner cases

**📧 邮件数**: 10 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 24 Jun 2026 16:00:25 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁系列，主要目的是修复 pKVM 映射缓存的边界情况。补丁的内容包括三个部分：第一部分修复了非缓存映射的 pKVM 缓存维护问题，第二部分解决了在权限故障时替换页面映射的 pKVM 缓存顶补错误，第三部分则修复了在权限故障情况下仍需分割块映射的通用脏日志记录问题。

在历史讨论中，Bradley Morgan 提出了这些补丁，并详细说明了每个补丁的功能和背景。补丁的 v3 版本是独立发送的，并进行了结构上的调整，以优化缓存可用位的存储。

在本周的新讨论中，参与者 Vincent Donnefort 和 Leonardo Bras 针对补丁中的结构设计进行了深入探讨，提出了使用位域来简化代码的建议，并讨论了使用特定位（如第48位或第63位）存储标志的合理性。Bradley Morgan 对这些建议表示认可，并表示将会在即将发布的 v4 版本中考虑这些反馈。

总体来看，本周讨论主要集中在补丁的实现细节和代码优化建议上，参与者之间的互动积极，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[06-24 16:00]** [PATCH v3 0/3] KVM: arm64: fix pKVM mapping cache corner cases
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[06-24 16:00]** [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Bradley Morgan <include@grrlz.net>
3. **[07-01 14:31]** Re: [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non
 cacheable mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-01 17:05]** Re: [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[07-01 17:40]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_1/3=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
6. **[07-01 17:53]** Re: [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-01 17:54]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_1/3=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
8. **[07-01 17:56]** Re: [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[07-01 17:57]** =?US-ASCII?Q?Re=3A_=5BPATCH_v3_1/3=5D_KVM=3A_arm64=3A_skip_pKVM?=
 =?US-ASCII?Q?_cache_flushes_for_non_cacheable_mappings?=
   - 发件人: Bradley Morgan <include@grrlz.net>
10. **[07-02 11:43]** Re: [PATCH v3 1/3] KVM: arm64: skip pKVM cache flushes for non cacheable mappings
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 12: [PATCH v8 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 10 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 30 Jun 2026 10:20:53 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A 和 KVM 的一系列补丁，主要集中在修复 Endpoint Memory Access Descriptor (EMAD) 的偏移量计算及相关的边界检查问题。

1. **原始补丁内容**：该系列补丁旨在修复 EMAD 偏移量计算错误，并为 FF-A 驱动和 pKVM 超级管理程序添加必要的边界检查。补丁更新了核心 `arm_ffa` 驱动，以正确使用 `ep_mem_offset` 字段计算描述符偏移量，并增强了 pKVM 的验证逻辑，以确保偏移量在邮箱缓冲区的边界内。

2. **之前讨论要点**：在 FF-A 版本 1.1 之前，内存区域头部未明确指定 EMAD 的偏移量，导致假设 EMAD 紧随其后。补丁系列通过修复这些假设和错误，确保与 FF-A 规范的一致性。

3. **本周的新讨论与进展**：本周的讨论中，参与者提交了六个补丁，涵盖了多个方面的修复，包括修复边界检查、确保内存区域的页面对齐、以及在 FFA 处理程序中清零堆栈初始化数据等。Sashiko AI 提供了反馈，指出了一些潜在问题，如可能导致双重释放的错误和高危的主机控制无效句柄问题。整体上，这些补丁被认为是紧急修复，直接影响到超管安全性和内核稳定性。

#### 📝 邮件列表

1. **[06-30 10:20]** [PATCH v8 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-30 10:20]** [PATCH v8 1/6] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-30 10:20]** [PATCH v8 2/6] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-30 10:20]** [PATCH v8 3/6] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-30 10:20]** [PATCH v8 4/6] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-30 10:20]** [PATCH v8 5/6] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-30 10:20]** [PATCH v8 6/6] KVM: arm64: Zero out the stack initialized data in the
 FFA handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-30 10:53]** Re: [PATCH v8 3/6] KVM: arm64: Fix bounds checking in
 do_ffa_mem_reclaim()
   - 发件人: sashiko-bot@kernel.org
9. **[06-30 11:08]** Re: [PATCH v8 5/6] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: sashiko-bot@kernel.org
10. **[06-30 11:19]** Re: [PATCH v8 6/6] KVM: arm64: Zero out the stack initialized data
 in the FFA handler
   - 发件人: sashiko-bot@kernel.org

---

### Thread 13: [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Thu,  2 Jul 2026 10:38:37 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）的多个补丁，主要集中在修复 Endpoint Memory Access Descriptor（EMAD）偏移计算及相关的边界检查。

**原始补丁内容**：该补丁系列旨在修复 EMAD 偏移计算错误，并为 FF-A 驱动和 pKVM 超级管理程序添加必要的边界检查。由于 FF-A 1.1 版本开始，内存区域头部不再默认假设 EMAD 紧随其后，因此需要根据 `ep_mem_offset` 字段来计算内存访问数组的起始位置。

**之前讨论要点**：在历史讨论中，开发者们指出了 FF-A 驱动中存在的多个潜在越界写入问题，并提出了相应的修复建议。补丁系列经过多次迭代，逐步解决了这些问题，并确保与 FF-A 规范的一致性。

**本周新讨论及进展**：本周的讨论中，开发者们提交了六个补丁，涵盖了对 EMAD 偏移的验证、内存区域的边界检查、确保内存范围的页面对齐等多个方面。特别是，补丁修复了在处理 FF-A 版本调用时可能泄露超管堆栈数据的问题。此外，Sashiko AI 提出了潜在的其他问题，提醒开发者注意可能导致系统崩溃的情况。整体来看，这些补丁旨在提升 KVM 的安全性和稳定性。

#### 📝 邮件列表

1. **[07-02 10:38]** [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[07-02 10:38]** [PATCH v9 1/6] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[07-02 10:38]** [PATCH v9 2/6] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[07-02 10:38]** [PATCH v9 3/6] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[07-02 10:38]** [PATCH v9 4/6] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[07-02 10:38]** [PATCH v9 5/6] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[07-02 10:38]** [PATCH v9 6/6] KVM: arm64: Zero out the stack initialized data in the
 FFA handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[07-02 10:48]** Re: [PATCH v9 6/6] KVM: arm64: Zero out the stack initialized data
 in the FFA handler
   - 发件人: sashiko-bot@kernel.org
9. **[07-03 11:35]** Re: [PATCH v9 4/6] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 14: [PATCH v4 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  3 Jul 2026 14:25:59 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的虚拟化通用中断控制器（VGIC）中，涉及 LPI（本地中断）的释放和重新注册处理的竞争条件问题。

**原始 patch/问题的内容**：
Carlos López 提交了两个补丁，旨在解决 LPI 释放和重新注册之间的潜在竞争问题。第一个补丁修复了 LPI 结构可能泄漏或被提前删除的问题，第二个补丁则缓解了在注册 LPI 时可能出现的 -ENOMEM 错误。

**之前讨论要点**：
在历史讨论中，Carlos 逐步修改了补丁以解决代码中的潜在问题，包括在锁定 xarray 时减少引用计数，以避免使用后释放（UAF）的问题，并确保在并发情况下不会发生 LPI 的错误删除。

**本周的新讨论、进展或结论**：
本周，Carlos 提交了补丁的更新版本，并在邮件中详细说明了每个补丁的修复逻辑。Oliver Upton 对补丁提出了建议，强调在释放旧 IRQ 时需要确保其引用计数为零且处于待释放状态，以避免内存泄漏。Oliver 还建议在代码中加入相应的检查，以确保逻辑的正确性。整体上，讨论集中在确保 LPI 处理的安全性和稳定性上，参与者们对补丁的细节进行了深入的技术审查和讨论。

#### 📝 邮件列表

1. **[07-03 14:25]** [PATCH v4 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-03 14:26]** [PATCH v4 1/2] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
3. **[07-03 14:26]** [PATCH v4 2/2] KVM: arm64: vgic: Mitigate potential LPI registration failure
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
4. **[07-03 15:13]** Re: [PATCH v4 1/2] KVM: arm64: vgic: Fix race between LPI release
 and re-registration
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[07-03 15:19]** Re: [PATCH v4 1/2] KVM: arm64: vgic: Fix race between LPI release
 and re-registration
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 15: [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 2 Jul 2026 19:04:18 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构上增强性能监控单元（PMU）功能的补丁系列，主要是为了将 PMMIR_EL1.SLOTS 暴露给虚拟机（guest）。补丁分为三个部分：

1. **原始补丁内容**：补丁系列的核心是引入一个新的 vCPU 特性标志 `KVM_ARM_VCPU_PMU_V3_STRICT`。当该标志被设置时，KVM 不会在 vCPU 初始化时创建默认的 PMU，用户空间必须通过 `KVM_ARM_VCPU_PMU_V3_SET_PMU` 明确选择一个 PMU。这一机制确保了在异构系统中，PMU 的信息可以安全地暴露给虚拟机。

2. **之前讨论要点**：在补丁的 v1 版本中，开发者考虑了向后兼容性和异构系统的需求，因此决定在新特性后面增加一个标志，而不是无条件地暴露 PMMIR_EL1.SLOTS。开发者还对补丁进行了多次修改，以确保功能的正确性和安全性。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的具体实现上，包括如何在用户空间访问和设置 PMMIR_EL1.SLOTS，以及在 `PMCEID1` 中不再屏蔽与 STALL_SLOT 相关的事件。参与者对补丁进行了审查并提出了一些潜在问题，例如在 vCPU 系统寄存器恢复之前可能会出现 PMU 事件计数器状态的静默截断问题。

整体来看，这一系列补丁旨在提升 KVM 在 ARM64 架构上的性能监控能力，同时确保与现有系统的兼容性。

#### 📝 邮件列表

1. **[07-02 19:04]** [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>
2. **[07-02 19:04]** [PATCH v2 1/3] KVM: arm64: Add KVM_ARM_VCPU_PMU_V3_STRICT vCPU feature
   - 发件人: Congkai Tan <congkai@amazon.com>
3. **[07-02 19:04]** [PATCH v2 2/3] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict PMUv3 UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
4. **[07-02 19:04]** [PATCH v2 3/3] KVM: arm64: Advertise STALL_SLOT* in PMCEID1 under strict PMUv3 UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
5. **[07-02 19:29]** Re: [PATCH v2 1/3] KVM: arm64: Add KVM_ARM_VCPU_PMU_V3_STRICT vCPU
 feature
   - 发件人: sashiko-bot@kernel.org

---

### Thread 16: [PATCH v12 02/16] set_memory: add
 folio_{zap,restore}_direct_map helpers

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 03 Jul 2026 10:19:10 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（PATCH v12 02/16），其内容是添加 `folio_{zap,restore}_direct_map` 辅助函数，以改进内存管理。该补丁旨在优化高效的内存映射和管理，尤其是在处理高内存（highmem）时。

在之前的讨论中，参与者们关注到该补丁在高内存情况下存在问题，特别是与 `secretmem` 相关的功能。Nikita Kalyazin 提到，当前的实现存在缺陷，导致在高内存环境下无法正确分配和映射内存。虽然这个问题并不是补丁本身引起的，但它暴露了 Linus 主分支中的一些潜在问题。

本周的新讨论中，Brendan Jackman 和 Mike Rapoport 继续探讨如何解决高内存相关的问题。Brendan 提出了一个建议，即将 `folio_zap_direct_map()` 在高内存情况下设置为无操作（NOP），以简化修复过程。此外，他们讨论了是否应该在高内存系统上禁用 `secretmem`，因为目前没有用户对此功能的需求。

总体来看，本周的讨论集中在如何有效地解决补丁引入的问题，以及对高内存支持的进一步优化建议上。参与者们对补丁的后续改进表示积极态度，并提出了多种解决方案。

#### 📝 邮件列表

1. **[07-03 10:19]** Re: [PATCH v12 02/16] set_memory: add
 folio_{zap,restore}_direct_map helpers
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
2. **[07-03 16:38]** Re: [PATCH v12 02/16] set_memory: add folio_{zap,restore}_direct_map
 helpers
   - 发件人: Mike Rapoport <rppt@kernel.org>
3. **[07-03 14:54]** Re: [PATCH v12 02/16] set_memory: add
 folio_{zap,restore}_direct_map helpers
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
4. **[07-03 17:25]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>

---

### Thread 17: [PATCH v3 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  3 Jul 2026 13:01:28 +0200

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的虚拟化中，修复 LPI（Local Peripheral Interrupt）释放和重新注册处理中的竞争条件问题。

**原始 patch/问题的内容**：
本次讨论的补丁（PATCH v3 0/2）旨在解决两个潜在问题：一是 LPI 结构可能泄漏或被过早删除，二是注册 LPI 时可能出现的 -ENOMEM 错误。

**之前讨论要点**：
在之前的讨论中，开发者 Carlos López 针对这些问题进行了补丁的多次迭代，特别是 v1 和 v2 版本中，针对 Sashiko 的审查反馈进行了修正，确保在 xarray 锁下正确处理引用计数，避免引入使用后释放（UAF）的问题。

**本周的新讨论、进展或结论**：
本周的讨论中，Carlos López 提交了两个补丁：第一个补丁修复了 LPI 释放和重新注册之间的竞争条件，确保在引用计数减少和 xarray 结构移除之间的操作是原子性的；第二个补丁则通过在插入新 LPI 时使用 GFP_NOWAIT，来缓解可能的注册失败问题。Sashiko AI 也对第二个补丁进行了审查，提出了一个低优先级的潜在问题，涉及内存控制组（memcg）会计的处理。

总体而言，本周的讨论集中在确保 LPI 的正确管理和提高系统稳定性上。

#### 📝 邮件列表

1. **[07-03 13:01]** [PATCH v3 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-03 13:01]** [PATCH v3 1/2] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
3. **[07-03 13:01]** [PATCH v3 2/2] KVM: arm64: vgic: Mitigate potential LPI registration failure
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
4. **[07-03 11:18]** Re: [PATCH v3 2/2] KVM: arm64: vgic: Mitigate potential LPI
 registration failure
   - 发件人: sashiko-bot@kernel.org

---

### Thread 18: [PATCH v2] KVM: arm64: vgic: Fix race between LPI release and re-registration

**📧 邮件数**: 4 | **👥 参与者**: 4 | **📅 开始时间**: Fri,  3 Jul 2026 04:15:08 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM 的 arm64 架构中，VGIC（虚拟通用中断控制器）在释放 LPI（本地中断源）和重新注册之间的竞争条件的补丁（PATCH v2）。该补丁旨在解决在 LPI 的引用计数减少和从 LPI xarray 中移除结构体之间可能发生的竞态条件，特别是在多核环境下。

在历史讨论中，补丁指出，当 LPI 的引用计数降至零时，vgic_release_lpi_locked() 函数会在 xarray 锁下移除该结构体并释放它。然而，释放 LPI 的过程可能与其他 CPU 上的 LPI 重新注册（vgic_add_lpi()）发生竞争，导致新注册的 LPI 被错误地删除或泄漏。

本周的新讨论中，参与者对补丁进行了评审，Sashiko 提出了潜在的性能问题，认为在热路径中无条件获取全局 lpi_xa 锁可能导致大量锁竞争。Oliver Upton 也指出了补丁的不足之处，建议使用 __xa_cmpxchg() 仅在拥有的 IRQ 仍在 xarray 中时才进行删除，以避免使用后释放（UAF）问题。此外，Carlos López 提出可以使用 refcount_dec_and_lock_irqsave() 来优化锁的获取，确保只有在引用计数降至零时才获取锁。

总体而言，本周讨论集中在如何更有效地解决竞态条件，同时保持系统性能的平衡。

#### 📝 邮件列表

1. **[07-03 04:15]** [PATCH v2] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-03 02:32]** Re: [PATCH v2] KVM: arm64: vgic: Fix race between LPI release and
 re-registration
   - 发件人: sashiko-bot@kernel.org
3. **[07-03 01:44]** Re: [PATCH v2] KVM: arm64: vgic: Fix race between LPI release and
 re-registration
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[07-03 11:16]** Re: [PATCH v2] KVM: arm64: vgic: Fix race between LPI release and
 re-registration
   - 发件人: =?UTF-8?Q?Carlos_L=C3=B3pez?= <clopez@suse.de>

---

### Thread 19: [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  1 Jul 2026 16:16:18 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 S2 权限放宽问题的两个修复补丁。

**原始问题**：本次讨论的补丁旨在解决 S2 权限放宽过程中可能出现的两个问题。第一个补丁修复了在更新页表条目（PTE）时，可能使用未初始化的栈变量作为 TLBI TTL 提示的情况。第二个补丁则解决了在处理写入故障时，权限放宽不加条件地更新执行权限（XN），可能导致意外的执行权限故障。

**之前讨论要点**：在历史讨论中，未提及具体的补丁内容，但可以推测出参与者关注的是如何确保在权限放宽过程中，系统的稳定性和安全性。

**本周新讨论与进展**：本周，Oliver Upton 提交了两个补丁，分别是确保在放宽权限时总是初始化级别，以及仅在请求时更新 XN 属性。补丁的代码修改了 `pgtable.c` 文件，增加了必要的条件检查，以避免不必要的权限故障。Wei-Lin Chang 对该系列补丁进行了审查并表示通过，表明补丁已获得初步认可。

整体来看，本周的讨论集中在修复 KVM arm64 的权限管理问题，确保系统在处理权限放宽时的正确性与安全性。

#### 📝 邮件列表

1. **[07-01 16:16]** [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[07-01 16:16]** [PATCH 1/2] KVM: arm64: Ensure level is always initialized when relaxing perms
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[07-01 16:16]** [PATCH 2/2] KVM: arm64: Only update XN attr when requested during S2 relaxation
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[07-02 08:16]** Re: [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 20: [PATCH] KVM: selftests: fix steal_time for arm64

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 22 Jun 2026 12:02:05 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM 自测试中的 `steal_time` 问题，特别针对 arm64 架构的情况。原始的 patch 提出了在主机页面大小大于 4K 时，修复测试失败的问题。具体来说，测试在主机页面大小为 16K 时出现了断言失败，导致测试无法正确执行。

在之前的讨论中，Zenghui Yu 和 Sebastian Ott 讨论了该问题的根源，并提出了可能的解决方案。Sebastian 提出了使用 `vm_calc_num_guest_pages(VM_MODE_DEFAULT, STEAL_TIME_SIZE)` 来更好地描述希望添加的页面数量的建议。

在本周的新讨论中，Sebastian 对 Zenghui 的建议表示不以为然，认为这个问题对于用户 API 检查器并不重要，因为虚拟机和虚拟 CPU 实际上并未运行。因此，讨论的焦点转向了该修复的必要性和影响，表明目前的修复可能并不是迫在眉睫的需求。整体来看，本周的讨论没有带来新的进展或结论，主要是对之前讨论的进一步澄清。

#### 📝 邮件列表

1. **[06-22 12:02]** Re: [PATCH] KVM: selftests: fix steal_time for arm64
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
2. **[06-22 16:14]** [PATCH] KVM: selftests: fix steal_time for arm64 with host page size
 > 4K
   - 发件人: Sebastian Ott <sebott@redhat.com>
3. **[06-28 23:44]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
4. **[06-29 14:04]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Sebastian Ott <sebott@redhat.com>

---

### Thread 21: [PATCH] KVM: arm64: vgic: Fix race between LPI release and re-registration

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Fri,  3 Jul 2026 01:35:14 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VGIC（虚拟通用中断控制器）中，修复 LPI（本地中断源）释放与重新注册之间的竞争条件的补丁。

**原始补丁内容**：
补丁旨在解决在 LPI 结构的引用计数递减与从 LPI xarray 中移除该结构之间可能出现的竞争条件。具体而言，当 LPI 的引用计数降至零时，vgic_release_lpi_locked() 会在获取 xarray 锁的情况下移除并释放该结构。然而，这一过程可能与另一 CPU 上的 LPI 重新注册（vgic_add_lpi()）发生竞争，导致新注册的 LPI 被错误地删除或旧的 LPI 被泄漏。

**之前讨论要点**：
在历史讨论中，补丁的背景和潜在问题被详细阐述，指出了在 LPI 释放和注册过程中可能出现的竞态条件。

**本周新讨论与进展**：
本周的讨论中，参与者对补丁进行了进一步的审查。Sashiko AI 机器人指出补丁可能引入了使用后释放（Use-After-Free）和 ABA 漏洞的风险，建议在 vgic_put_irq() 路径下引用计数的递减应在 xarray 锁下进行，以避免在引用计数为零时 LPI 被释放。Carlos López 对此表示认可，并提出在 vgic_release_deleted_lpis() 中，如果条目已被 vgic_add_lpi() 驱逐，则不会找到该条目，因此在延迟路径上是安全的。整体来看，讨论集中在确保补丁的安全性和有效性上。

#### 📝 邮件列表

1. **[07-03 01:35]** [PATCH] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-02 23:52]** Re: [PATCH] KVM: arm64: vgic: Fix race between LPI release and
 re-registration
   - 发件人: sashiko-bot@kernel.org
3. **[07-03 03:49]** Re: [PATCH] KVM: arm64: vgic: Fix race between LPI release and
 re-registration
   - 发件人: =?UTF-8?Q?Carlos_L=C3=B3pez?= <clopez@suse.de>

---

### Thread 22: [PATCH v5 0/5] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 2 Jul 2026 17:36:24 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构上增加 KVM_PRE_FAULT_MEMORY 支持的补丁（PATCH v5 0/5）。该补丁的目标是改进内存管理，特别是在处理页面错误时的性能和效率。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁系列的提出是为了响应对 KVM 在 arm64 平台上内存处理能力的需求，尤其是在预先处理内存故障方面的改进。

在本周的新讨论中，参与者 Alexandru Elisei 提到他希望对该补丁系列进行审查和测试，但遇到了找不到基础提交的问题。他尝试通过 Git 命令查找相关提交，但未能成功，显示出该提交在当前的主分支中不存在。这表明在补丁的整合和版本管理上可能存在一些问题，影响了后续的审查和测试进程。

总体来看，本周的讨论集中在补丁的可用性和版本控制问题上，尚未进入具体的技术评审阶段。

#### 📝 邮件列表

1. **[07-02 17:36]** Re: [PATCH v5 0/5] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 23: [PATCH v3 3/5] KVM: arm64: nv: Avoid full shadow s2 unmap

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 29 Jun 2026 11:38:51 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在避免完全解除映射（full shadow s2 unmap）。该补丁的编号为 PATCH v3 3/5。

在历史讨论中，补丁的具体内容并未详细列出，但可以推测其主要目的是优化 KVM 的地址映射机制，以提高性能和安全性。参与者 Marc Zyngier 和 Wei-Lin Chang 之间的交流表明，他们关注于如何更清晰地命名相关变量，并确保地址对齐的安全性。

在本周的新讨论中，Wei-Lin Chang 对补丁进行了回复，表示将改用“canonical IPA”和“nested IPA”这两个更清晰的名称。此外，他提出了在代码中添加对地址对齐的警告机制，以防止潜在的错误。讨论中还提到将 VALID_ENTRY 和 UNKNOWN_IPA 的测试转化为帮助函数，以便更好地处理现有条目的状态。最后，Wei-Lin Chang 同意将某个函数的调用位置上移，以提高逻辑的合理性。

总体来看，本周的讨论集中在代码清晰性和安全性上，参与者们积极探讨了如何改进补丁的实现。

#### 📝 邮件列表

1. **[06-29 11:38]** Re: [PATCH v3 3/5] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

## 📌 RFC

共 2 个 thread

---

### Thread 1: [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 11 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 16 Jun 2026 15:16:47 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于增强 KVM/ARM 的补丁系列，主要目的是引入可定制的 aarch64 KVM 主机模型，以便在不同硬件之间迁移虚拟机时提供更大的灵活性。补丁的核心内容是允许用户空间覆盖部分 ID 寄存器的值，增强了对可写 ID 寄存器字段的支持。

在历史讨论中，Eric Auger 提出了多个补丁，包括生成 ID 寄存器的枚举值和保留字段，并探讨了如何通过 QEMU 查询可用的 ID 寄存器值。这些补丁旨在提高 KVM 的可扩展性和灵活性。

在本周的新讨论中，Eric Auger 和 Khushit Shah 继续交流补丁的细节。Eric 表示将整合 Khushit 提出的建议，并进一步探讨 CPU 定义的复杂性。Khushit 强调了测试增量设置的重要性，认为仅依靠安全规则可能无法提供足够的精确性。整体来看，本周的讨论集中在补丁的整合和测试方法的优化上，显示出开发者对实现目标的持续关注和合作。

#### 📝 邮件列表

1. **[06-16 15:16]** [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[06-16 15:16]** [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum values
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[06-16 15:17]** [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[06-16 15:17]** [RFC PATCH v6 15/17] target/arm/cpu-idregs.h.inc: Generate reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[06-18 11:26]** Re: [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[06-19 06:05]** Re: [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
7. **[06-19 06:10]** Re: [RFC PATCH v6 15/17] target/arm/cpu-idregs.h.inc: Generate
 reserved fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
8. **[06-19 06:28]** Re: [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum
 values
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
9. **[07-01 16:04]** Re: [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum
 values
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[07-01 16:09]** Re: [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[07-01 16:10]** Re: [RFC PATCH v6 15/17] target/arm/cpu-idregs.h.inc: Generate
 reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 2: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  2 Jul 2026 15:29:09 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（内核虚拟机）中针对仅支持 guest_memfd 的内存槽（memslots）实现脏页日志记录的 RFC（请求反馈补丁）系列。

1. **原始 patch/问题的内容**：
   该系列补丁的目标是为仅支持 guest_memfd 的内存槽实现脏页日志记录。由于这些内存槽的内存与用户空间共享，KVM 目前不允许更改其标志，因此无法启用脏页日志记录。补丁通过修改 guest_memfd 追踪内存槽的方式，使用内存槽 ID 而非指针来避免并发读取时的冲突。

2. **之前讨论要点**：
   之前的讨论主要集中在如何安全地管理内存槽的状态变化，特别是在更改内存槽标志时可能出现的竞争条件。参与者提出了潜在的 bug，指出在并发删除内存槽时可能会留下过时的 SPTE（共享页表条目），导致内存访问错误。

3. **本周的新讨论、进展或结论**：
   本周的讨论中，补丁的作者 Alexandru Elisei 提出了三个补丁：第一个补丁修改了 guest_memfd 的内存槽追踪方式，第二个补丁实现了脏页日志记录，第三个补丁则针对 arm64 架构允许该功能。参与者对补丁的潜在问题进行了反馈，指出了需要关注的 bug。补丁系列已在 arm64 机器上进行了测试，并且作者表示欢迎进一步的建议和改进。

#### 📝 邮件列表

1. **[07-02 15:29]** [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-02 15:29]** [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[07-02 15:29]** [RFC PATCH 2/3] KVM: Implement dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[07-02 15:29]** [RFC PATCH 3/3] KVM: arm64: Allow dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
5. **[07-02 14:47]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: sashiko-bot@kernel.org
6. **[07-02 17:09]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

## 📌 Question

共 1 个 thread

---

### Thread 1: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 4 Jul 2026 15:45:56 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于“TLBs 和 I-cache 对每个 vCPU 的私有性”以及 VTTBR_EL2.CnP 的保证。

在历史讨论中，未提供具体的背景信息，但本周的讨论围绕着 vCPU 的 TLB 和 I-cache 的无效化机制展开。Tangnianyao 提出了对 `kvm_arch_vcpu_load()` 中 TLB 和 I-cache 无效化的理解，质疑在 `VTTBR_EL2.CnP == 1` 的情况下，仅进行局部的无效化是否足以保证 TLB 和 I-cache 对每个 vCPU 的私有性。他指出，即使将无效化扩展到内部共享域，多个来自同一虚拟机的 vCPU 在不同物理处理器上并行运行时，仍然难以确保这一属性。

Wei-Lin Chang 对此进行了回应，解释了在涉及两个阶段时，只有当两个阶段都设置 CnP == 1 时，TLB 条目才会共享。他强调，TLB 和 I-cache 的私有性是因为每个物理 CPU 预期拥有自己的 TLB 和 I-cache，因此在 vCPU 上也必须保持这一属性。Chang 还提到，`__kvm_flush_cpu_context()` 解决了在单个物理 CPU 上多路复用 vCPU 时可能出现的问题，并引用了相关的提交记录以支持他的观点。

本周的讨论主要集中在对 TLB 和 I-cache 私有性保证的理解及其实现机制上，进一步澄清了技术细节和潜在问题。

#### 📝 邮件列表

1. **[07-04 15:45]** Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
2. **[07-05 18:28]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

## 📌 Discussion

共 1 个 thread

---

### Thread 1: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 26 Jun 2026 10:48:05 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于为 `ktime_get_snapshot_id()` 添加 `CLOCK_AUX` 支持的补丁（patch 09/24）。该补丁旨在改进时间管理系统，使其能够处理辅助时钟（AUX clocks）并正确计算与之相关的单调原始时间（MONORAW）。

在历史讨论中，参与者主要探讨了辅助时钟与全局单调原始时间之间的关系，指出辅助时钟的 MONORAW 值应基于其自身的时钟源，而不是全局时钟。Thomas Gleixner 提出了对补丁的认可，并建议清理相关文档中的术语，以避免混淆。

本周的新讨论中，Thomas Gleixner 对补丁的最终版本表示满意，并指出相关结构定义也需要更新。随后，他提交了一份新的补丁，明确了与辅助时钟相关的单调原始时间的文档，强调这些时间戳与系统时钟的单调原始时间之间的偏移关系。新的文档修正了之前的模糊描述，使其更准确地反映了 AUX 时钟的行为。

总结而言，补丁的目标是增强 Linux 内核对辅助时钟的支持，历史讨论提供了背景，而本周的进展则集中在文档的完善和最终确认补丁的有效性上。

#### 📝 邮件列表

1. **[06-26 10:48]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
2. **[06-26 12:49]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[06-26 13:03]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
4. **[06-26 17:17]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
5. **[06-29 05:55]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
6. **[06-29 10:39]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
7. **[07-05 14:38]** [PATCH] timekeeping: Document monotonic raw timestamps in snapshots
 correctly
   - 发件人: Thomas Gleixner <tglx@kernel.org>

---

