# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-07-27 00:40:25

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 500
- **总 Thread 数**: 52
- **大型 Thread** (>20封): 6 个

### 分类分布

- **PATCH**: 42 threads (433 邮件)
- **RFC**: 7 threads (63 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Discussion**: 1 threads (1 邮件)
- **Other**: 1 threads (2 邮件)

---

## 📌 PATCH

共 42 个 thread

---

### Thread 1: [PATCH v4 00/48] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 87 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 24 Jul 2026 10:48:25 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 153855 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:87, 119647 tokens)

#### 📝 邮件列表

1. **[07-24 10:48]** [PATCH v4 00/48] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[07-24 10:48]** [PATCH v4 01/48] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[07-24 10:48]** [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame attrs to
 KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[07-24 10:49]** [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[07-24 10:49]** [PATCH v4 04/48] KVM: arm64: gic-v5: Define remaining IRS MMIO
 registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-24 10:49]** [PATCH v4 05/48] arm64/sysreg: Add GICv5 GIC VDPEND encoding
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[07-24 10:49]** [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-24 10:50]** [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[07-24 10:50]** [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[07-24 10:50]** [PATCH v4 09/48] KVM: arm64: gic-v5: Create and manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[07-24 10:50]** [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[07-24 10:51]** [PATCH v4 11/48] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[07-24 10:51]** [PATCH v4 12/48] KVM: arm64: gic-v5: Keep GICv5 vCPU limit
 model-specific
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[07-24 10:51]** [PATCH v4 13/48] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[07-24 10:52]** [PATCH v4 14/48] KVM: arm64: gic-v5: Set up VMTEs and VPE doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[07-24 10:52]** [PATCH v4 15/48] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[07-24 10:52]** [PATCH v4 16/48] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[07-24 10:52]** [PATCH v4 17/48] KVM: arm64: gic-v5: Introduce struct vgic_v5_irs and
 IRS base address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[07-24 10:53]** [PATCH v4 18/48] KVM: arm64: gic-v5: Add IRS IODEV support to MMIO
 handlers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[07-24 10:53]** [PATCH v4 19/48] KVM: arm64: gic-v5: Add KVM_VGIC_V5_ADDR_TYPE_IRS to
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[07-24 10:53]** [PATCH v4 20/48] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[07-24 10:53]** [PATCH v4 21/48] KVM: arm64: gic-v5: Initialise per-VM IRS state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[07-24 10:54]** [PATCH v4 22/48] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[07-24 10:54]** [PATCH v4 23/48] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[07-24 10:54]** [PATCH v4 24/48] KVM: arm64: selftests: Update vGICv5 selftest to set
 IRS address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[07-24 10:54]** [PATCH v4 25/48] KVM: arm64: gic-v5: Add GIC VDPEND hyp call
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[07-24 10:55]** [PATCH v4 26/48] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[07-24 10:55]** [PATCH v4 27/48] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[07-24 10:55]** [PATCH v4 28/48] Documentation: KVM: Extend VGICv5 device attribute
 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[07-24 10:55]** [PATCH v4 29/48] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[07-24 10:56]** [PATCH v4 30/48] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[07-24 10:56]** [PATCH v4 31/48] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg userspace
 accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[07-24 10:56]** [PATCH v4 32/48] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[07-24 10:56]** [PATCH v4 33/48] KVM: arm64: gic-v5: Add CoreSight MMIO regs to IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[07-24 10:57]** [PATCH v4 34/48] KVM: arm64: gic-v5: Add VGICv5 IST save/restore UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[07-24 10:57]** [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[07-24 10:57]** [PATCH v4 36/48] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[07-24 10:57]** [PATCH v4 37/48] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[07-24 10:58]** [PATCH v4 38/48] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[07-24 10:58]** [PATCH v4 39/48] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[07-24 10:58]** [PATCH v4 40/48] KVM: selftests: Add VGICv5 IRS address attribute
 tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
42. **[07-24 10:58]** [PATCH v4 41/48] KVM: selftests: Add VGICv5 NR_IRQS attribute tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
43. **[07-24 10:59]** [PATCH v4 42/48] KVM: selftests: Add VGICv5 IRS_REGS attribute tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
44. **[07-24 10:59]** [PATCH v4 43/48] KVM: selftests: Add VGICv5 IST attribute tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
45. **[07-24 10:59]** [PATCH v4 44/48] KVM: selftests: Add VGICv5 USERSPACE_PPIS tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
46. **[07-24 11:00]** [PATCH v4 45/48] KVM: selftests: Add VGICv5 CPU sysreg attribute
 tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
47. **[07-24 11:00]** [PATCH v4 46/48] KVM: selftests: Add VGICv5 SPI injection tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
48. **[07-24 11:00]** [PATCH v4 47/48] KVM: selftests: Add VGICv5 LPI delivery tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
49. **[07-24 11:00]** [PATCH v4 48/48] KVM: selftests: Add VGICv5 IST save/restore coverage
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
50. **[07-24 11:10]** Re: [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: sashiko-bot@kernel.org
51. **[07-24 11:11]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: sashiko-bot@kernel.org
52. **[07-24 11:14]** Re: [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: sashiko-bot@kernel.org
53. **[07-24 11:19]** Re: [PATCH v4 09/48] KVM: arm64: gic-v5: Create and manage VM and
 VPE tables
   - 发件人: sashiko-bot@kernel.org
54. **[07-24 11:19]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from
 IRS config frame
   - 发件人: sashiko-bot@kernel.org
55. **[07-24 11:19]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI
 hosts
   - 发件人: sashiko-bot@kernel.org
56. **[07-24 11:20]** Re: [PATCH v4 11/48] KVM: arm64: gic-v5: Implement VMT/vIST IRS
 MMIO Ops
   - 发件人: sashiko-bot@kernel.org
57. **[07-24 11:21]** Re: [PATCH v4 01/48] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: sashiko-bot@kernel.org
58. **[07-24 11:21]** Re: [PATCH v4 13/48] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: sashiko-bot@kernel.org
59. **[07-24 11:22]** Re: [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: sashiko-bot@kernel.org
60. **[07-24 11:26]** Re: [PATCH v4 15/48] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: sashiko-bot@kernel.org
61. **[07-24 11:27]** Re: [PATCH v4 14/48] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: sashiko-bot@kernel.org
62. **[07-24 11:30]** Re: [PATCH v4 19/48] KVM: arm64: gic-v5: Add
 KVM_VGIC_V5_ADDR_TYPE_IRS to UAPI
   - 发件人: sashiko-bot@kernel.org
63. **[07-24 11:33]** Re: [PATCH v4 22/48] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: sashiko-bot@kernel.org
64. **[07-24 11:34]** Re: [PATCH v4 25/48] KVM: arm64: gic-v5: Add GIC VDPEND hyp call
   - 发件人: sashiko-bot@kernel.org
65. **[07-24 11:39]** Re: [PATCH v4 26/48] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: sashiko-bot@kernel.org
66. **[07-24 11:41]** Re: [PATCH v4 23/48] KVM: arm64: gic-v5: Set IRICHPPIDIS based on
 IRS enable state
   - 发件人: sashiko-bot@kernel.org
67. **[07-24 11:41]** Re: [PATCH v4 16/48] KVM: arm64: gic-v5: Request doorbells when
 VPEs enter WFI
   - 发件人: sashiko-bot@kernel.org
68. **[07-24 11:45]** Re: [PATCH v4 20/48] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and
 MMIO emulation
   - 发件人: sashiko-bot@kernel.org
69. **[07-24 11:46]** Re: [PATCH v4 34/48] KVM: arm64: gic-v5: Add VGICv5 IST
 save/restore UAPI
   - 发件人: sashiko-bot@kernel.org
70. **[07-24 11:48]** Re: [PATCH v4 27/48] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: sashiko-bot@kernel.org
71. **[07-24 11:52]** Re: [PATCH v4 30/48] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: sashiko-bot@kernel.org
72. **[07-24 12:02]** Re: [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: sashiko-bot@kernel.org
73. **[07-24 12:02]** Re: [PATCH v4 41/48] KVM: selftests: Add VGICv5 NR_IRQS attribute
 tests
   - 发件人: sashiko-bot@kernel.org
74. **[07-24 12:05]** Re: [PATCH v4 32/48] KVM: arm64: gic-v5: Handle userspace accesses
 to IRS MMIO region
   - 发件人: sashiko-bot@kernel.org
75. **[07-24 12:06]** Re: [PATCH v4 42/48] KVM: selftests: Add VGICv5 IRS_REGS attribute
 tests
   - 发件人: sashiko-bot@kernel.org
76. **[07-24 12:09]** Re: [PATCH v4 31/48] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg
 userspace accessors
   - 发件人: sashiko-bot@kernel.org
77. **[07-24 12:15]** Re: [PATCH v4 46/48] KVM: selftests: Add VGICv5 SPI injection tests
   - 发件人: sashiko-bot@kernel.org
78. **[07-24 12:18]** Re: [PATCH v4 47/48] KVM: selftests: Add VGICv5 LPI delivery tests
   - 发件人: sashiko-bot@kernel.org
79. **[07-24 12:19]** Re: [PATCH v4 37/48] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: sashiko-bot@kernel.org
80. **[07-24 12:19]** Re: [PATCH v4 29/48] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: sashiko-bot@kernel.org
81. **[07-25 10:06]** Re: [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame attrs to KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
82. **[07-25 10:18]** Re: [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame attrs to KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
83. **[07-25 10:35]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Marc Zyngier <maz@kernel.org>
84. **[07-25 11:08]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Marc Zyngier <maz@kernel.org>
85. **[07-25 11:10]** Re: [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and LINK_IDLE fields
   - 发件人: Marc Zyngier <maz@kernel.org>
86. **[07-25 11:40]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from IRS config frame
   - 发件人: Marc Zyngier <maz@kernel.org>
87. **[07-25 11:56]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [PATCH v3 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3

**📧 邮件数**: 62 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 22 Jul 2026 08:42:06 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 ARM64 架构的两个新特性扩展：FEAT_NV2p1 和 FEAT_NV3 的支持，涉及一系列补丁的提交和讨论。

1. **原始补丁内容**：
   - FEAT_NV2p1 主要是修复在嵌套虚拟化配置中，EL1 访问 CNTHCTL_EL2 和 CPTR_EL2 时缺失的状态位，减少陷阱的发生。
   - FEAT_NV3 则更为复杂，改变了在嵌套虚拟化环境中 ERET 的行为，通过引入 NVHCR_EL2 寄存器来优化对 ERET 和 TLBI 指令的处理。

2. **之前的讨论要点**：
   - 之前的讨论集中在如何实现这两个特性的细节，以及它们对性能的影响。Marc Zyngier 提到在 FVP 模型上进行了测试，L1 客户端的指令减少了约 1.5%，而 L2 和 L3 客户端的性能提升更为显著。

3. **本周的新讨论与进展**：
   - 本周的讨论主要围绕补丁的实现细节，Marc Zyngier 提交了多个补丁，逐步完善对 FEAT_NV2p1 和 FEAT_NV3 的支持，包括对 NVHCR_EL2 的描述、上下文切换、以及对新控制位的处理。
   - 参与者对补丁进行了审查，提出了一些潜在问题和改进建议，确保补丁的正确性和性能优化。
   - 讨论中还涉及了对新特性的动态检测和注册，以确保这些功能在适当的硬件上能够被正确启用。

整体而言，本周的讨论推动了对 ARM64 嵌套虚拟化特性的支持进展，确保了补丁的有效性和性能提升。

#### 📝 邮件列表

1. **[07-22 08:42]** [PATCH v3 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-22 08:42]** [PATCH v3 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping/Fields definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-22 08:42]** [PATCH v3 02/28] arm64: Update ID_AA64MMFR4_EL1 description to 2026-03 JSON release
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-22 08:42]** [PATCH v3 03/28] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-22 08:42]** [PATCH v3 04/28] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-22 08:42]** [PATCH v3 05/28] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-22 08:42]** [PATCH v3 06/28] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL register
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-22 08:42]** [PATCH v3 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor HFGITR_EL2.ERET on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-22 08:42]** [PATCH v3 08/28] arm64: Add ARM64_HAS_NV2P1 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-22 08:42]** [PATCH v3 09/28] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-22 08:42]** [PATCH v3 10/28] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[07-22 08:42]** [PATCH v3 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-22 08:42]** [PATCH v3 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[07-22 08:42]** [PATCH v3 13/28] arm64: sysreg: Add NVHCR_EL2 description as a mirror of HCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-22 08:42]** [PATCH v3 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[07-22 08:42]** [PATCH v3 15/28] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-22 08:42]** [PATCH v3 16/28] KVM: arm64: Split NV-specific exit fixups from the non-NV handling
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[07-22 08:42]** [PATCH v3 17/28] KVM: arm64: Add NV3 control bits to HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[07-22 08:42]** [PATCH v3 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[07-22 08:42]** [PATCH v3 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[07-22 08:42]** [PATCH v3 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[07-22 08:42]** [PATCH v3 21/28] KVM: arm64: Add NVHCR_EL2 handling to the sysreg array
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[07-22 08:42]** [PATCH v3 22/28] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[07-22 08:42]** [PATCH v3 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[07-22 08:42]** [PATCH v3 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[07-22 08:42]** [PATCH v3 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[07-22 08:42]** [PATCH v3 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[07-22 08:42]** [PATCH v3 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[07-22 08:42]** [PATCH v3 28/28] arm64: Add override for ID_AA64MMFR4_EL1.NV_frac
   - 发件人: Marc Zyngier <maz@kernel.org>
30. **[07-22 07:55]** Re: [PATCH v3 01/28] arm64: sysreg: Emit RESx/UNKN values for
 Mapping/Fields definitions
   - 发件人: sashiko-bot@kernel.org
31. **[07-22 08:11]** Re: [PATCH v3 14/28] arm64: sysreg: Add HCRX_EL2 bits related to
 FEAT_NV3
   - 发件人: sashiko-bot@kernel.org
32. **[07-22 08:13]** Re: [PATCH v3 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: sashiko-bot@kernel.org
33. **[07-22 08:23]** Re: [PATCH v3 16/28] KVM: arm64: Split NV-specific exit fixups from
 the non-NV handling
   - 发件人: sashiko-bot@kernel.org
34. **[07-22 08:32]** Re: [PATCH v3 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: sashiko-bot@kernel.org
35. **[07-22 08:38]** Re: [PATCH v3 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: sashiko-bot@kernel.org
36. **[07-22 08:50]** Re: [PATCH v3 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: sashiko-bot@kernel.org
37. **[07-22 08:53]** Re: [PATCH v3 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: sashiko-bot@kernel.org
38. **[07-22 09:56]** Re: [PATCH v3 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
39. **[07-22 09:57]** Re: [PATCH v3 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
40. **[07-22 08:57]** Re: [PATCH v3 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: sashiko-bot@kernel.org
41. **[07-22 10:01]** Re: [PATCH v3 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
42. **[07-22 10:04]** Re: [PATCH v3 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
43. **[07-22 10:04]** Re: [PATCH v3 25/28] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[07-22 10:05]** Re: [PATCH v3 01/28] arm64: sysreg: Emit RESx/UNKN values for Mapping/Fields definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[07-22 09:06]** Re: [PATCH v3 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: sashiko-bot@kernel.org
46. **[07-22 10:08]** Re: [PATCH v3 16/28] KVM: arm64: Split NV-specific exit fixups from the non-NV handling
   - 发件人: Marc Zyngier <maz@kernel.org>
47. **[07-22 10:11]** Re: [PATCH v3 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
48. **[07-22 10:16]** Re: [PATCH v3 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
49. **[07-22 10:18]** Re: [PATCH v3 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
50. **[07-24 14:04]** Re: [PATCH v3 07/28] KVM: arm64: Don't evaluate HCR_EL2.NV nor
 HFGITR_EL2.ERET on ERET fast path
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
51. **[07-24 14:06]** Re: [PATCH v3 09/28] KVM: arm64: Relax CPTR_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
52. **[07-24 14:07]** Re: [PATCH v3 11/28] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
53. **[07-24 14:08]** Re: [PATCH v3 12/28] arm64: Add FEAT_NV2p1 detection
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
54. **[07-24 14:08]** Re: [PATCH v3 13/28] arm64: sysreg: Add NVHCR_EL2 description as a
 mirror of HCR_EL2
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
55. **[07-24 14:11]** Re: [PATCH v3 16/28] KVM: arm64: Split NV-specific exit fixups from
 the non-NV handling
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
56. **[07-24 14:13]** Re: [PATCH v3 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
57. **[07-24 14:15]** Re: [PATCH v3 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
58. **[07-24 14:16]** Re: [PATCH v3 20/28] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
59. **[07-24 16:10]** Re: [PATCH v3 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
60. **[07-24 16:40]** Re: [PATCH v3 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
61. **[07-24 16:41]** Re: [PATCH v3 26/28] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
62. **[07-24 16:43]** Re: [PATCH v3 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>

---

### Thread 3: [PATCH v3 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 36 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 20 Jul 2026 18:14:56 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的补丁系列，主要关注引入 pKVM 超级管理器堆分配器的实现。

1. **原始 Patch/问题内容**：
   该补丁系列的核心是引入一个动态内存分配器（hyp_allocator）用于 pKVM 超级管理器，以解决之前的设计中超管内存使用与主机约束紧密耦合的问题。该分配器允许超管在需要时动态分配和回收内存，从而提高虚拟机的可扩展性。

2. **之前讨论要点**：
   在历史讨论中，参与者们探讨了 pKVM 的内存管理问题，包括如何有效地处理内存捐赠和回收。之前的设计依赖于主机提供的连续内存，这在内存高度碎片化时会导致问题。引入动态分配器后，超管可以独立管理内存，简化了内存回收路径。

3. **本周的新讨论、进展或结论**：
   本周的讨论集中在补丁的具体实现上，包括多个子补丁的提交和审查。参与者们提出了对代码的改进建议，例如确保在内存分配失败时适当地处理错误，以及在回收内存时考虑内存缓存中的页面。此外，补丁还引入了自测试机制，以验证堆分配器的功能。参与者们对补丁的整体方向表示支持，并针对具体实现细节进行了深入讨论，确保代码的健壮性和安全性。

总的来说，这一系列补丁的目标是通过引入动态内存分配器来改善 pKVM 的内存管理，从而提高虚拟机的性能和可扩展性。

#### 📝 邮件列表

1. **[07-20 18:14]** [PATCH v3 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-20 18:14]** [PATCH v3 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-20 18:14]** [PATCH v3 02/17] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-20 18:14]** [PATCH v3 03/17] KVM: arm64: Add pkvm_map_private_va_range
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-20 18:15]** [PATCH v3 04/17] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-20 18:15]** [PATCH v3 05/17] KVM: arm64: Allow kvm_hyp_memcache usage outside of stage-2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[07-20 18:15]** [PATCH v3 06/17] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-20 18:15]** [PATCH v3 07/17] KVM: arm64: Add PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[07-20 18:15]** [PATCH v3 08/17] KVM: arm64: Add reclaim interface for the pKVM heap alloc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[07-20 18:15]** [PATCH v3 09/17] KVM: arm64: Add selftests for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-20 18:15]** [PATCH v3 10/17] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[07-20 18:15]** [PATCH v3 11/17] KVM: arm64: Filter out non-kernel addresses in kern_hyp_va
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[07-20 18:15]** [PATCH v3 12/17] KVM: arm64: Move hyp_vm refcount into the structure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[07-20 18:15]** [PATCH v3 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[07-20 18:15]** [PATCH v3 14/17] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[07-20 18:15]** [PATCH v3 15/17] KVM: arm64: Reject hyp trace descriptors with fewer
 CPUs than hyp_nr_cpus
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[07-20 18:15]** [PATCH v3 16/17] KVM: arm64: Reject hyp trace descriptors with fewer
 than 3 pages
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[07-20 18:15]** [PATCH v3 17/17] KVM: arm64: Alloc simple_buffer_page using pKVM hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[07-20 17:25]** Re: [PATCH v3 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: sashiko-bot@kernel.org
20. **[07-20 17:26]** Re: [PATCH v3 04/17] KVM: arm64: Add a heap allocator for the pKVM
 hyp
   - 发件人: sashiko-bot@kernel.org
21. **[07-20 17:27]** Re: [PATCH v3 02/17] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: sashiko-bot@kernel.org
22. **[07-20 17:28]** Re: [PATCH v3 11/17] KVM: arm64: Filter out non-kernel addresses in
 kern_hyp_va
   - 发件人: sashiko-bot@kernel.org
23. **[07-20 17:29]** Re: [PATCH v3 03/17] KVM: arm64: Add pkvm_map_private_va_range
   - 发件人: sashiko-bot@kernel.org
24. **[07-20 17:31]** Re: [PATCH v3 09/17] KVM: arm64: Add selftests for the pKVM heap
 allocator
   - 发件人: sashiko-bot@kernel.org
25. **[07-20 17:32]** Re: [PATCH v3 08/17] KVM: arm64: Add reclaim interface for the pKVM
 heap alloc
   - 发件人: sashiko-bot@kernel.org
26. **[07-20 17:36]** Re: [PATCH v3 07/17] KVM: arm64: Add PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: sashiko-bot@kernel.org
27. **[07-20 17:41]** Re: [PATCH v3 14/17] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM
 heap allocator
   - 发件人: sashiko-bot@kernel.org
28. **[07-20 17:44]** Re: [PATCH v3 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap
 allocator
   - 发件人: sashiko-bot@kernel.org
29. **[07-20 17:47]** Re: [PATCH v3 17/17] KVM: arm64: Alloc simple_buffer_page using
 pKVM hyp allocator
   - 发件人: sashiko-bot@kernel.org
30. **[07-23 08:19]** Re: [PATCH v3 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Fuad Tabba <tabba@google.com>
31. **[07-23 13:14]** Re: [PATCH v3 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Fuad Tabba <tabba@google.com>
32. **[07-23 13:30]** Re: [PATCH v3 03/17] KVM: arm64: Add pkvm_map_private_va_range
   - 发件人: Fuad Tabba <tabba@google.com>
33. **[07-23 14:19]** Re: [PATCH v3 04/17] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Fuad Tabba <tabba@google.com>
34. **[07-23 16:08]** Re: [PATCH v3 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap
 allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
35. **[07-23 16:11]** Re: [PATCH v3 04/17] KVM: arm64: Add a heap allocator for the pKVM
 hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
36. **[07-23 17:10]** Re: [PATCH v3 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 4: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5

**📧 邮件数**: 25 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 9 Jul 2026 18:40:20 +0800

#### 🤖 AI 总结

本邮件线程讨论了支持 Armv9.5 引入的硬件脏页状态跟踪特性（FEAT_HDBSS）的补丁系列（PATCH v4 0/6）。该特性旨在通过硬件辅助来优化脏页跟踪，减少扫描脏页的开销。

在历史讨论中，Tian Zheng 提出了补丁的背景和目的，强调 HDBSS 特性如何增强对翻译表描述符脏状态的跟踪。讨论中提到，DBM（脏位修改器）属性的引入可以自动将写清页提升为写脏，避免因缺少写权限而导致的陷阱。Leonardo Bras 和其他参与者对补丁的实现细节进行了深入探讨，包括 HDBSS 缓冲区的处理和故障处理机制。

在本周的新讨论中，Leonardo Bras 提出了关于 DBM 和脏环的编码问题，讨论了如何在启用脏跟踪时处理懒惰拆分的情况。Inochi Amaoto 关注 HDBSS 缓冲区与脏环的大小关系，提出在配置脏环时需要考虑 HDBSS 的条目数量，以避免内存使用过大。参与者们对缓冲区管理策略进行了多种方案的讨论，强调了根据工作负载调整缓冲区大小的重要性。

总体来看，讨论集中在如何有效实现 HDBSS 特性及其与现有脏页跟踪机制的兼容性上，参与者们对补丁的细节和潜在影响进行了积极的交流。

#### 📝 邮件列表

1. **[07-09 18:40]** [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
2. **[07-09 18:40]** [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[07-09 18:40]** [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
4. **[07-13 15:06]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[07-14 15:38]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
6. **[07-14 11:50]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-14 12:59]** [PATCH v4 0/6] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[07-14 12:59]** [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[07-14 21:27]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
10. **[07-14 15:19]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-16 00:05]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[07-16 00:39]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[07-16 17:14]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
14. **[07-16 10:16]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Oliver Upton <oupton@kernel.org>
15. **[07-17 11:58]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
16. **[07-17 14:51]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
17. **[07-17 16:21]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
18. **[07-17 16:44]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
19. **[07-20 13:58]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
20. **[07-21 16:53]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Inochi Amaoto <inochiama@gmail.com>
21. **[07-21 15:18]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
22. **[07-22 13:14]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Inochi Amaoto <inochiama@gmail.com>
23. **[07-22 12:04]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
24. **[07-22 14:09]** Re: [PATCH v4 2/6] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
25. **[07-23 09:17]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Inochi Amaoto <inochiama@gmail.com>

---

### Thread 5: [PATCH v9 00/16] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 24 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 14:37:54 +0900

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上对性能监控单元（PMU）支持的改进，主要集中在引入多种主机 PMU 的使用。

1. **原始 patch/问题的内容**：
   提出的补丁（PATCH v9 00/16）旨在解决在异构 arm64 系统上，KVM 的 PMU 模拟仅基于单一主机 PMU 实例的问题。当虚拟 CPU（vCPU）迁移到具有不兼容 PMU 的物理 CPU（pCPU）时，计数器可能停止递增，导致 Windows 客户机崩溃。补丁引入了 `KVM_ARM_VCPU_PMU_V3_FIXED_COUNTERS_ONLY` 属性，使得 PMUv3 可以在不需要可编程事件计数器的情况下被模拟，从而提高了系统的兼容性和稳定性。

2. **之前的讨论要点**：
   之前的讨论主要集中在如何处理 vCPU 的初始化和 PMU 状态的管理，确保在不同的 pCPU 上运行时不会导致状态不一致。补丁版本逐步演进，添加了多个功能和修复，确保 PMU 状态在虚拟机运行期间的一致性。

3. **本周的新讨论、进展或结论**：
   本周的讨论主要围绕补丁的具体实现和测试，包括对 `FIXED_COUNTERS_ONLY` 模式的支持，确保在该模式下，vCPU 可以在任何具有 PMU 的物理 CPU 上运行。还讨论了如何在设置事件过滤器时处理状态，确保在不同条件下的错误处理（如 EBUSY）。此外，补丁还增加了自测试，以验证新功能的正确性和稳定性。整体来看，补丁的进展顺利，增强了 KVM 对 PMU 的支持，提升了系统的兼容性和性能。

#### 📝 邮件列表

1. **[07-20 14:37]** [PATCH v9 00/16] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[07-20 14:37]** [PATCH v9 01/16] KVM: arm64: Serialize repeated vCPU
 initialization
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[07-20 14:37]** [PATCH v9 02/16] KVM: arm64: PMU: Stop updating MDCR_EL2.HPMN
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[07-20 14:37]** [PATCH v9 03/16] KVM: arm64: PMU: Freeze counter count after first
 run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[07-20 14:37]** [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS after
 first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[07-20 14:37]** [PATCH v9 05/16] KVM: arm64: PMU: Keep implemented counter mask
 EL-independent
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[07-20 14:38]** [PATCH v9 06/16] KVM: arm64: PMU: Recreate events after MDCR_EL2
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[07-20 14:38]** [PATCH v9 07/16] tools headers: Use u* types for bitfield helpers
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[07-20 14:38]** [PATCH v9 08/16] KVM: arm64: selftests: Cover PMU state in
 MDCR_EL2
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
10. **[07-20 14:38]** [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
11. **[07-20 14:38]** [PATCH v9 10/16] KVM: arm64: Don't clear vcpu->cpu in
 kvm_arch_vcpu_put()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
12. **[07-20 14:38]** [PATCH v9 11/16] KVM: arm64: PMU: Protect the list of PMUs with
 RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
13. **[07-20 14:38]** [PATCH v9 12/16] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
14. **[07-20 14:38]** [PATCH v9 13/16] KVM: arm64: PMU: Pass the target CPU to
 kvm_pmu_probe_armpmu()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
15. **[07-20 14:38]** [PATCH v9 14/16] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
16. **[07-20 14:38]** [PATCH v9 15/16] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
17. **[07-20 14:38]** [PATCH v9 16/16] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
18. **[07-20 05:53]** Re: [PATCH v9 05/16] KVM: arm64: PMU: Keep implemented counter mask
 EL-independent
   - 发件人: sashiko-bot@kernel.org
19. **[07-20 05:57]** Re: [PATCH v9 06/16] KVM: arm64: PMU: Recreate events after
 MDCR_EL2 changes
   - 发件人: sashiko-bot@kernel.org
20. **[07-20 05:58]** Re: [PATCH v9 02/16] KVM: arm64: PMU: Stop updating MDCR_EL2.HPMN
   - 发件人: sashiko-bot@kernel.org
21. **[07-20 06:01]** Re: [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3
 traps on all CPUs
   - 发件人: sashiko-bot@kernel.org
22. **[07-20 06:03]** Re: [PATCH v9 12/16] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: sashiko-bot@kernel.org
23. **[07-20 06:08]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: sashiko-bot@kernel.org
24. **[07-20 06:17]** Re: [PATCH v9 14/16] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: sashiko-bot@kernel.org

---

### Thread 6: [PATCH v1 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary

**📧 邮件数**: 19 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 20 Jul 2026 17:13:32 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上的补丁系列，主要目的是恢复主机与超管（hyp）之间的超调用（hypercall）类型检查。以下是讨论的主要内容：

1. **原始补丁/问题内容**：补丁系列的核心在于修复 SMCCC（Secure Monitor Call Convention）转换后，超调用参数类型检查丢失的问题。Fuad Tabba 提出通过在 `kvm_hcall.h` 中声明超调用的签名，并生成类型安全的存根（stub），以确保调用者与处理程序之间的参数类型一致。

2. **之前讨论要点**：在历史讨论中，Marc 提到在快速转换到 SMCCC 时，丢失了所有的类型检查，导致参数类型、数量或顺序不一致而没有任何编译警告。Fuad 提出了通过生成存根来重新引入编译时检查的方案。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的具体实现上，包括修复了多个现存的警告，确保了在 C=2 模式下的源代码检查。此外，补丁系列的前六个补丁不依赖于类型检查的实现，可以单独提交。Sashiko AI 评审也指出了一些潜在问题，Fuad 对这些问题进行了回应，并表示将继续改进补丁。

总体而言，该补丁系列旨在提高 KVM arm64 的类型安全性，确保超调用的参数在编译时得到验证，从而减少运行时错误的可能性。

#### 📝 邮件列表

1. **[07-20 17:13]** [PATCH v1 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-20 17:13]** [PATCH v1 01/11] tracing: Include linux/types.h in trace_remote_event.h
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-20 17:13]** [PATCH v1 02/11] KVM: arm64: nVHE: Share the stacktrace per-CPU declarations with EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-20 17:13]** [PATCH v1 03/11] KVM: arm64: nVHE: Declare the hyp event IDs before defining them
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-20 17:13]** [PATCH v1 04/11] KVM: arm64: nVHE: Use NULL to reset the trace buffer backing pointer
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-20 17:13]** [PATCH v1 05/11] KVM: arm64: nVHE: Run the source checker under C=2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-20 17:13]** [PATCH v1 06/11] arm64: pi: Run the source checker on the libfdt objects under C=2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-20 17:13]** [PATCH v1 07/11] KVM: arm64: nVHE: Pass host VA arguments as pointers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-20 17:13]** [PATCH v1 08/11] KVM: arm64: Move the host hypercall interface to its own header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[07-20 17:13]** [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at the caller
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[07-20 17:24]** [PATCH v1 10/11] KVM: arm64: nVHE: Check hypercall handlers against the declared ABI
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[07-20 17:24]** [PATCH v1 11/11] KVM: arm64: Tag host-VA hypercall parameters __hostva
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
13. **[07-20 17:29]** Re: [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at
 the caller
   - 发件人: sashiko-bot@kernel.org
14. **[07-20 17:42]** Re: [PATCH v1 10/11] KVM: arm64: nVHE: Check hypercall handlers
 against the declared ABI
   - 发件人: sashiko-bot@kernel.org
15. **[07-20 17:55]** Re: [PATCH v1 11/11] KVM: arm64: Tag host-VA hypercall parameters
 __hostva
   - 发件人: sashiko-bot@kernel.org
16. **[07-20 18:59]** Re: [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at
 the caller
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[07-20 19:01]** Re: [PATCH v1 10/11] KVM: arm64: nVHE: Check hypercall handlers
 against the declared ABI
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[07-20 19:24]** Re: [PATCH v1 11/11] KVM: arm64: Tag host-VA hypercall parameters __hostva
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
19. **[07-20 14:32]** Re: [PATCH v1 01/11] tracing: Include linux/types.h in
 trace_remote_event.h
   - 发件人: Steven Rostedt <rostedt@goodmis.org>

---

### Thread 7: [PATCH v12 00/29] KVM: arm64: Implement support for SME

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Thu, 09 Jul 2026 19:27:21 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中实现对 SME（Scalable Matrix Extension）的支持，主要围绕一个名为“[PATCH v12 00/29] KVM: arm64: Implement support for SME”的补丁进行。

**原始补丁内容**：该补丁旨在为 arm64 架构的 KVM 实现对 SME 的支持，特别关注用户空间 ABI 和 SVE（Scalable Vector Extension）寄存器的访问。

**之前的讨论要点**：在历史讨论中，参与者们对补丁的具体实现进行了多次审查，提出了对提交信息的清晰度、代码中的小错误以及潜在的同步问题的建议。特别是关于在加载 SME 状态时，如何动态配置 FA64 和 ZT0 的访问权限，以避免在 KVM 客户端中不必要的浮点状态重载。

**本周的新讨论与进展**：本周的讨论集中在对 ISB（Instruction Synchronization Barrier）使用的优化上。Mark Rutland 和 Mark Brown 强调不应进行投机性优化，建议在代码中使用无条件的 ISB，以确保系统的稳定性和一致性。Rutland 提出了一种新的代码结构，旨在在更新 SMCR_EL1 时更清晰地处理 ISB 的调用。这一讨论表明，尽管存在优化的需求，参与者们仍然对保持代码的简洁和安全性持谨慎态度。

#### 📝 邮件列表

1. **[07-09 19:27]** [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-09 19:27]** [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-16 11:52]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[07-16 16:28]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-18 01:35]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-18 14:30]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-18 15:24]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[07-19 09:35]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when loading SME state
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-19 13:40]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-23 13:30]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[07-23 13:47]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[07-23 14:29]** Re: [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 8: [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes

**📧 邮件数**: 12 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 17 Jul 2026 14:03:10 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM（Protected KVM）阶段2映射和内存缓存修复的补丁系列（PATCH v5 0/7）。该补丁旨在解决多个与内存管理和映射相关的实际问题。

在历史讨论中，Fuad Tabba 提出了补丁的多个关键改动，包括恢复权限故障和脏日志内存缓存的补充、优化映射对象的处理、以及在启用强制写回（FWB）时跳过不必要的缓存清理等。这些补丁的目标是提高 pKVM 的稳定性和性能，避免不必要的警告和错误。

在本周的新讨论中，参与者 Bradley Morgan 对多个补丁进行了审查并表示认可，确认了补丁的有效性（LGTM）。他还建议在某些情况下将补丁的返回值进行合并，并提出了对代码的细微修改意见。Fuad 对于这些建议进行了回应，表示他倾向于保留某些返回值的独立性，并讨论了后续可能的回溯问题。

总体来看，本周的讨论主要集中在对补丁的审查和细节的优化上，参与者之间的互动积极，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[07-17 14:03]** [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-17 14:03]** [PATCH v5 4/7] KVM: arm64: Skip pKVM stage-2 flush when FWB is enabled
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-17 14:03]** [PATCH v5 5/7] KVM: arm64: Don't WARN on pKVM stage-2 map failures
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-17 14:03]** [PATCH v5 6/7] KVM: arm64: Don't advertise eager page splitting under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-17 14:03]** [PATCH v5 7/7] KVM: arm64: selftests: Add stage-2 block transition test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-21 11:50]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_4/7=5D_KVM=3A_arm64=3A_Skip_p?=
 =?US-ASCII?Q?KVM_stage-2_flush_when_FWB_is_enabled?=
   - 发件人: Bradley Morgan <include@grrlz.net>
7. **[07-21 11:50]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_5/7=5D_KVM=3A_arm64=3A_Don=27?=
 =?US-ASCII?Q?t_WARN_on_pKVM_stage-2_map_failures?=
   - 发件人: Bradley Morgan <include@grrlz.net>
8. **[07-21 12:19]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_6/7=5D_KVM=3A_arm64=3A_Don=27t_ad?=
 =?US-ASCII?Q?vertise_eager_page_splitting_under_pKVM?=
   - 发件人: Bradley Morgan <include@grrlz.net>
9. **[07-21 12:22]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_7/7=5D_KVM=3A_arm64=3A_selfte?=
 =?US-ASCII?Q?sts=3A_Add_stage-2_block_transition_test?=
   - 发件人: Bradley Morgan <include@grrlz.net>
10. **[07-21 12:24]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_0/7=5D_KVM=3A_arm64=3A_pKVM?=
 =?US-ASCII?Q?_stage-2_mapping_and_memcache_fixes?=
   - 发件人: Bradley Morgan <include@grrlz.net>
11. **[07-21 13:24]** Re: [PATCH v5 6/7] KVM: arm64: Don't advertise eager page splitting
 under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[07-21 14:04]** =?US-ASCII?Q?Re=3A_=5BPATCH_v5_6/7=5D_KVM=3A_arm64=3A_Don=27t_ad?=
 =?US-ASCII?Q?vertise_eager_page_splitting_under_pKVM?=
   - 发件人: Bradley Morgan <include@grrlz.net>

---

### Thread 9: [PATCH v2 00/18] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 12 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 18:53:57 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM 超级管理程序的动态内存分配器的补丁系列（PATCH v2 00/18）。该补丁旨在解决 pKVM 之前缺乏动态内存分配器的问题，所有虚拟机和 VCPU 结构必须在主机上预先分配，导致内存使用受到主机约束的限制，影响了虚拟机的可扩展性。

在历史讨论中，Vincent Donnefort 提出了引入一个自定义的堆分配器（hyp_allocator），以便在 pKVM 超级管理程序中动态分配内存。讨论中还涉及了如何处理错误路径中的内存释放，以及对内存分配的保护机制的有效性。

本周的新讨论主要集中在对补丁的细节修订上。Vincent 和 Fuad Tabba 经过深入讨论，确认了对内存保护机制的改进不会引入额外成本，并决定在提交信息中添加更多细节。此外，针对内存分配的错误处理和验证机制也进行了确认，确保在出现错误时能够正确回滚并释放内存。

总体来看，讨论进展顺利，补丁的细节得到了进一步完善，参与者对内存管理的安全性和有效性达成了一致。

#### 📝 邮件列表

1. **[07-06 18:53]** [PATCH v2 00/18] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-06 18:54]** [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-06 18:54]** [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in __pkvm_init_vm
 error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-06 18:54]** [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-14 19:35]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-15 11:59]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-15 13:09]** Re: [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in
 __pkvm_init_vm error path
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-15 16:07]** Re: [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM
 hyp allocator
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-20 13:30]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM
 hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[07-20 14:41]** Re: [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in
 __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-20 15:04]** Re: [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM
 hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[07-20 15:10]** Re: [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using pKVM
 hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 10: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 15:28:02 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 Arm CCA（保密计算架构）支持的补丁系列，特别是第 12 个补丁，涉及在领域（realms）中支持 VGIC（虚拟通用中断控制器）。

**原始补丁内容**：
Steven Price 提出的补丁系列旨在为 KVM 添加对 Arm CCA 的支持，允许在受保护的虚拟机中运行。该补丁是之前 44 个补丁系列的第二部分，主要聚焦于将通用固件和 RMM（运行时管理器）支持分离，以便于其他工作使用。

**之前讨论要点**：
在历史讨论中，补丁的基础结构已被重构，旨在简化审查过程。补丁的主要问题在于如何处理缺少 ARM64_HAS_ICH_HCR_EL2_TDIR 特性的主机 CPU，这可能导致领域客户无法正常启动。

**本周新讨论与进展**：
本周的讨论集中在 Kohei Enju 的测试反馈上，他指出在缺少 TDIR 支持的 CPU 上，补丁无法按预期工作。Marc Zyngier 强调，现代 CPU 应该支持 TDIR，因此不打算为不支持 TDIR 的系统添加额外的仿真层。Steven Price 也表示，若存在不支持 TDIR 的 CCA 系统，则应考虑不支持 CCA 或实现必要的陷阱处理。最终，Steven 提供了一个初步的补丁，处理缺失的 GICv3 CPU 接口陷阱，供 Kohei 测试。Kohei 对此表示感谢，并计划进一步研究该补丁。整体来看，讨论中对补丁的实施细节和支持范围进行了深入探讨，尚未达成最终结论。

#### 📝 邮件列表

1. **[07-15 15:28]** [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:28]** [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-22 17:27]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
4. **[07-22 10:27]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-22 14:31]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
6. **[07-23 15:38]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
7. **[07-23 15:56]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
8. **[07-23 09:07]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-23 18:02]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
10. **[07-23 15:46]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
11. **[07-24 14:40]** Re: [PATCH v15 12/37] KVM: arm64: CCA: Support the VGIC in realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>

---

### Thread 11: [PATCH 0/5] KVM: arm64: Make ICH_VTR_EL2 accesses an inlined literal

**📧 邮件数**: 11 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 14:22:14 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构下对 ICH_VTR_EL2 寄存器访问的优化，主要通过将其访问转变为内联字面量（inlined literal）来提高性能。

1. **原始 patch/问题的内容**：Marc Zyngier 提出了一个包含五个补丁的系列，旨在将 ICH_VTR_EL2 的访问方式改为内联字面量，以减少对该寄存器的访问次数，从而提高嵌套 KVM 实例下的性能。

2. **之前的讨论要点**：在历史讨论中，Marc 指出 ICH_VTR_EL2 在虚拟化环境中是一个常量，通常会在内存中缓存。之前的实现中存在对 `kvm_vgic_global_state` 的访问，但由于某些原因不再映射该状态，因此需要寻找更高效的访问方式。

3. **本周的新讨论、进展或结论**：本周的讨论集中在补丁的具体实现上，包括添加新的帮助函数以提供 ICH_VTR_EL2 的内联字面量、将大部分对该寄存器的访问替换为内联调用，以及简化 GICv3 的初始配置。参与者还讨论了补丁中的一些潜在问题，如违反 `noinstr` 安全规则的情况。Marc 对这些问题进行了回应，并表示将调整补丁以解决这些问题。

整体来看，这一系列补丁旨在通过优化 ICH_VTR_EL2 的访问方式，提升 KVM 在嵌套虚拟化环境中的性能表现。

#### 📝 邮件列表

1. **[07-20 14:22]** [PATCH 0/5] KVM: arm64: Make ICH_VTR_EL2 accesses an inlined literal
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-20 14:22]** [PATCH 1/5] KVM: arm64: vgic-v3: Make vtr_to_* helpers use architectural field symbols
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-20 14:22]** [PATCH 2/5] KVM: arm64: Add a helper providing an inlined literal value for ICH_VTR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-20 14:22]** [PATCH 2/5] KVM: arm64: Add a helper providing an inlined litteral value for ICH_VTR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-20 14:22]** [PATCH 3/5] KVM: arm64: Convert most ICH_VTR_EL2 accesses to inlined literal value
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-20 14:22]** [PATCH 4/5] KVM: arm64: vgic-v3: Simplify initial GICv3 configuration sampling
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-20 14:22]** [PATCH 5/5] KVM: arm64: vgic-v3: Kill kvm_vgic_global_state.ich_vtr_el2
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-20 13:38]** Re: [PATCH 4/5] KVM: arm64: vgic-v3: Simplify initial GICv3
 configuration sampling
   - 发件人: sashiko-bot@kernel.org
9. **[07-20 13:46]** Re: [PATCH 2/5] KVM: arm64: Add a helper providing an inlined
 literal value for ICH_VTR_EL2
   - 发件人: sashiko-bot@kernel.org
10. **[07-20 15:49]** Re: [PATCH 2/5] KVM: arm64: Add a helper providing an inlined literal value for ICH_VTR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-20 15:50]** Re: [PATCH 4/5] KVM: arm64: vgic-v3: Simplify initial GICv3 configuration sampling
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH] KVM: arm64: ptdump: Flush the last region

**📧 邮件数**: 10 | **👥 参与者**: 4 | **📅 开始时间**: Sat, 18 Jul 2026 00:12:33 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 ptdump 功能，特别是如何正确输出最后一个区域的内容。

**原始 patch/问题的内容**：
Wei-Lin Chang 提出的补丁旨在解决当前 stage-2 ptdump 在遍历每个叶子条目时，未能输出最后一个区域的问题。由于 note_page() 仅在检测到级别或保护的变化时才会输出，因此最后一个区域如果没有变化则不会被转储。为了解决这一问题，补丁建议手动调用 note_page()。

**之前的讨论要点**：
在历史讨论中，参与者们关注到补丁的实现方式，认为手动调用 note_page() 可能不是最佳方案。Mark Rutland 提出可以使用 note_page_flush() 来替代手动调用，从而简化代码并避免潜在的错误。

**本周的新讨论、进展或结论**：
本周的讨论中，Mark Rutland 和其他参与者继续探讨使用 note_page_flush() 的可行性，并指出当前实现存在的问题。Wei-Lin Chang 进一步分析了使用 note_page_flush() 时可能出现的错误，并提出了改进方案，包括在 note_page_flush() 中使用 ptdump_state.range[] 来确定结束地址。最终，参与者们达成共识，计划在 KVM ptdump 中初始化 ptdump_state.range[]，并在遍历结束时调用 note_page_flush()。这一改进将有助于确保输出的准确性和完整性。

#### 📝 邮件列表

1. **[07-18 00:12]** [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[07-20 09:35]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[07-20 14:23]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Dev Jain <dev.jain@arm.com>
4. **[07-20 10:03]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-20 14:40]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Dev Jain <dev.jain@arm.com>
6. **[07-20 15:00]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Dev Jain <dev.jain@arm.com>
7. **[07-20 11:58]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[07-20 12:08]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[07-20 13:37]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[07-20 22:21]** Re: [PATCH] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 13: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Jul 2026 13:40:50 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于为 KVM（Kernel-based Virtual Machine）在 arm64 架构中添加 GICv5 IRS（中断路由系统）支持的补丁（PATCH v3 00/40）。该补丁包含约6000行新代码，主要涉及用户空间接口的修改和 GICv5 的保存/恢复机制。

在之前的讨论中，参与者们关注了补丁的复杂性和潜在问题，尤其是保存和恢复序列的顺序性问题。Fuad Tabba 提出了对用户空间接口的改进建议，强调了在保存/恢复过程中需要严格检查数据大小，以避免潜在的内存溢出和数据不一致问题。

本周的讨论中，Fuad 和 Sascha Bischoff 继续深入探讨补丁的细节。Fuad 提出了对 GICv5 中 PPI（私有中断）编号的不同处理方式的疑虑，并建议在代码中明确界定循环边界，以确保不会超出位图的范围。Sascha 则表示将会在下一个版本中包含更多的自测代码，以确保功能的完整性和正确性，并同意将保存/恢复功能与 IRS、SPI 和 LPI 支持一起提交，以便于审查。

总的来说，本周的讨论围绕补丁的细节和测试展开，双方达成一致，认为将相关功能整合在一起有助于提升代码的可审查性和稳定性。

#### 📝 邮件列表

1. **[07-21 13:40]** Re: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-21 15:32]** Re: [PATCH v3 33/40] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg
 userspace accessors
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-21 16:42]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-22 14:39]** Re: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[07-22 14:58]** Re: [PATCH v3 33/40] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg
 userspace accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-22 16:10]** Re: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-22 15:18]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-22 18:57]** Re: [PATCH v3 36/40] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-24 10:28]** Re: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 14: [PATCH v2 0/6] KVM: arm64: Make ICH_VTR_EL2 accesses an inlined literal

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Jul 2026 18:07:48 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 ICH_VTR_EL2 寄存器访问的优化。Marc Zyngier 提出了一个补丁系列，旨在将 ICH_VTR_EL2 的访问方式改为内联字面量，以减少在非虚拟化环境中产生的陷阱，从而降低不必要的开销。根据测试，实施该补丁后，L3 工作负载的墙钟时间减少了 5%。

历史讨论中，Marc 提到补丁的第一版存在多个问题，因此进行了重构。主要修改包括将“损坏的 SEIS”检测移动到 CPU 错误修正框架中，简化了 GICv3 的初始配置采样，并引入了一个新的内联字面量值的辅助函数来替代直接读取系统寄存器的方式。

在本周的新讨论中，Marc 提交了六个补丁，分别涉及到将 ICH_VTR_EL2 的访问转换为内联字面量、简化配置采样、以及移除对全局状态的依赖。Oliver Upton 对补丁进行了积极的反馈，并表示将其应用于下一步开发中，表明该系列补丁已得到认可并准备合并。

#### 📝 邮件列表

1. **[07-21 18:07]** [PATCH v2 0/6] KVM: arm64: Make ICH_VTR_EL2 accesses an inlined literal
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-21 18:07]** [PATCH v2 1/6] KVM: arm64: vgic-v3: Make vtr_to_* helpers use architectural field symbols
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-21 18:07]** [PATCH v2 2/6] KVM: arm64: Move GICv3 broken SEIS implementation detection to a CPU errrata
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-21 18:07]** [PATCH v2 3/6] KVM: arm64: Add a helper providing an inlined literal value for ICH_VTR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-21 18:07]** [PATCH v2 4/6] KVM: arm64: Convert most ICH_VTR_EL2 accesses to inlined literal value
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-21 18:07]** [PATCH v2 5/6] KVM: arm64: vgic-v3: Simplify initial GICv3 configuration sampling
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-21 18:07]** [PATCH v2 6/6] KVM: arm64: vgic-v3: Kill kvm_vgic_global_state.ich_vtr_el2
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-21 10:57]** Re: [PATCH v2 2/6] KVM: arm64: Move GICv3 broken SEIS implementation
 detection to a CPU errrata
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[07-21 11:24]** Re: [PATCH v2 0/6] KVM: arm64: Make ICH_VTR_EL2 accesses an inlined literal
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 15: [PATCH v2 0/2] KVM: arm64: KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 10 Jul 2026 12:48:17 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的两个补丁，旨在修复 hyp_trace_buffer_alloc_bpages_backing 中的潜在内存泄漏问题。

**原始补丁内容**：
补丁系列由 Vincent Donnefort 提出，主要包括两个修复：
1. 修复 hyp_trace_buffer_alloc_bpages_backing 中的潜在内存泄漏。
2. 修复 hyp_trace_load() 中的 hyp_trace_desc 分配大小问题。

**之前的讨论要点**：
在历史邮件中，Vincent 介绍了补丁的背景和变更记录，并收集了 Fuad Tabba 的审核和测试反馈，确保补丁的有效性和稳定性。

**本周的新讨论与进展**：
本周的讨论主要集中在补丁的应用和进一步的改进上。Marc Zyngier 确认已将补丁应用于修复中，并感谢 Vincent 的贡献。Wei-Lin Chang 提出了关于 ptdump 的两个新补丁，解决了 ptdump 输出中最后区域的缺失问题，并对 note_page_flush() 进行了改进。Dev Jain 和 Marc Zyngier 对代码格式提出了建议，确保代码风格的一致性。整体来看，本周的讨论推动了补丁的实施和代码质量的提升。

#### 📝 邮件列表

1. **[07-10 12:48]** [PATCH v2 0/2] KVM: arm64: KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-23 17:11]** Re: [PATCH v2 0/2] KVM: arm64: KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-24 19:54]** [PATCH v2 0/2] arm64: ptdump flush fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[07-24 19:54]** [PATCH v2 1/2] arm64: ptdump: Make note_page_flush() range aware
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[07-24 19:54]** [PATCH v2 2/2] KVM: arm64: ptdump: Flush the last region
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[07-25 22:46]** Re: [PATCH v2 2/2] KVM: arm64: ptdump: Flush the last region
   - 发件人: Dev Jain <dev.jain@arm.com>
7. **[07-25 18:28]** Re: [PATCH v2 2/2] KVM: arm64: ptdump: Flush the last region
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-26 13:41]** Re: [PATCH v2 2/2] KVM: arm64: ptdump: Flush the last region
   - 发件人: Dev Jain <dev.jain@arm.com>

---

### Thread 16: [PATCH v7 00/24] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Jul 2026 11:58:41 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 在 arm64 架构下的 SMMUv3 驱动支持，特别是针对 pKVM 的“trap and emulate”功能。最初的补丁（PATCH v7 00/24）由 Mostafa Saleh 提出，旨在实现完整的 pv 接口，并在后续版本中添加了 DMA 隔离和命令队列的阴影管理等功能。

在历史讨论中，Mostafa 提出了多个补丁版本，逐步完善了 SMMUv3 驱动的实现，特别是关于 IOMMU 的主机阶段-2 页表和命令队列的阴影管理。讨论中涉及到的关键点包括如何在驱动初始化后创建页表、如何处理权限变化的回调等。

在本周的新讨论中，参与者 Sebastian Ene 提出了对命令队列大小和是否需要数据同步屏障（dsb）的疑问。Mostafa 对此进行了回应，表示可以将队列大小固定，并解释了在写入命令时使用的屏障机制。此外，Sebastian 还询问了在 IOMMU 中处理无效描述符的方式，以及在快照失败时是否需要提供相应的去初始化回调。Mostafa 进一步讨论了 DMA 隔离的可选性和错误处理的方式，显示出对补丁的持续优化和完善的关注。

总体来看，本周讨论集中在对补丁细节的深入探讨和优化建议上，推动了 SMMUv3 驱动的进一步发展。

#### 📝 邮件列表

1. **[07-15 11:58]** [PATCH v7 00/24] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-15 11:58]** [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-15 11:58]** [PATCH v7 14/24] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-23 14:55]** Re: [PATCH v7 14/24] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[07-23 15:15]** Re: [PATCH v7 14/24] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[07-23 15:29]** Re: [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[07-24 07:29]** Re: [PATCH v7 07/24] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 17: [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 15:27:31 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 Arm RMM（Realm Management Monitor）v2.0 的支持，包含了六个补丁的提交。补丁的主要内容是为 RMM 提供通用固件层，以便与 RMM 进行通信，符合 RMM v2.0-bet2 规范。这一系列补丁的分拆使得 RMM 支持可以作为其他工作的基础，而不需要依赖后续的 KVM Realm 支持。

在历史讨论中，Steven Price 提出了多个补丁，包括添加 SMC 调用 RMM 的定义和确保 RMM 对内存有 GPT（GUID Partition Table）条目等。讨论中提到了一些潜在问题，例如主机内存分配失败被错误解析为 RMI 固件错误，以及成功消息中缺少换行符等。

在本周的新讨论中，Steven Price 针对之前的补丁回复了关于内存块对齐和错误消息的问题，指出了一个潜在的错误，并确认了换行符缺失的问题。Kohei Enju 也对补丁中的某些内容提出了疑问，认为某些部分可能是 RMM v1.0 支持的遗留物，且在 RMM v2.0 接口中不再需要。整体来看，本周的讨论集中在对补丁细节的审查和潜在问题的确认上。

#### 📝 邮件列表

1. **[07-15 15:27]** [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:27]** [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling the RMM
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-15 15:27]** [PATCH 6/6] firmware: arm_rmm: Ensure the RMM has GPT entries for memory
   - 发件人: Steven Price <steven.price@arm.com>
4. **[07-15 15:47]** Re: [PATCH 6/6] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: sashiko-bot@kernel.org
5. **[07-20 16:03]** Re: [PATCH 6/6] firmware: arm_rmm: Ensure the RMM has GPT entries for
 memory
   - 发件人: Steven Price <steven.price@arm.com>
6. **[07-23 16:11]** Re: [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling
 the RMM
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>

---

### Thread 18: [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 22 Jul 2026 20:26:58 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构下如何向客户机暴露 PMMIR_EL1.SLOTS 寄存器的补丁（PATCH v3 0/4）。该补丁的目的是解决在使用 PMUv3p4 的核心上运行性能工具时，无法正确解析默认指标的问题。

补丁的主要内容包括：
1. **补丁内容**：补丁分为四个部分，主要通过引入新的 vCPU 特性标志 KVM_ARM_VCPU_PMU_V3_STRICT 来控制 PMMIR_EL1.SLOTS 的暴露。补丁中包含对 PMMIR_EL1.SLOTS 的访问、事件计数器的配置以及对旧版本的兼容性处理。

2. **历史讨论要点**：在之前的讨论中，参与者对如何在保持向后兼容的同时，安全地暴露 PMU 信息进行了探讨，特别是在异构系统中。

3. **本周新讨论与进展**：本周的讨论集中在补丁的具体实现上，参与者提出了对补丁的审查意见，包括逻辑错误和 API 合同的潜在问题，如未增加 `KVM_VCPU_MAX_FEATURES` 以适应新标志，导致特性验证失败。此外，讨论还指出在严格模式下不应自动创建默认 PMU 的实现问题。

综上所述，本次邮件讨论围绕 KVM 在 arm64 架构下的 PMU 特性进行了深入的技术交流，提出了补丁的具体实现和存在的问题，旨在提高虚拟化性能和兼容性。

#### 📝 邮件列表

1. **[07-22 20:26]** [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>
2. **[07-22 20:26]** [PATCH v3 1/4] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict PMUv3 UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
3. **[07-22 20:27]** [PATCH v3 2/4] KVM: arm64: Advertise STALL_SLOT* in PMCEID1 under strict PMUv3 UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
4. **[07-22 20:27]** [PATCH v3 3/4] KVM: arm64: Ignore writes to PMCR_EL0.N when using strict UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
5. **[07-22 20:27]** [PATCH v3 4/4] KVM: arm64: Add KVM_ARM_VCPU_PMU_V3_STRICT vCPU feature
   - 发件人: Congkai Tan <congkai@amazon.com>
6. **[07-22 20:47]** Re: [PATCH v3 1/4] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict
 PMUv3 UAPI
   - 发件人: sashiko-bot@kernel.org

---

### Thread 19: [PATCH 0/2] KVM: arm64: Fix host-directed debug for non-protected pKVM guests

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 26 Jul 2026 15:36:41 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 arm64 架构下对非保护 pKVM 客户机的主机引导调试功能的问题。原始的 patch 包括两个部分：第一个 patch 旨在将外部 MDSCR_EL1 状态传递给 pKVM hyp vCPU，以确保在主机拥有调试寄存器时，能够正确处理调试异常；第二个 patch 则增加了一个用户空间观察点的自测，确保在使用硬件调试时能够正确报告访问的地址。

在之前的讨论中，主要关注了 patch 1 的实现细节，指出在调用 `flush_debug_state()` 时，未能将 `external_mdscr_el1` 传递给 hyp vCPU，导致调试异常无法触发。Fuad Tabba 提到这个问题是在为保护虚拟机添加自托管调试支持时发现的。

本周的新讨论中，Fuad 提交了两个 patch，并对其进行了详细说明。第一个 patch 解决了调试状态传递的问题，而第二个 patch 则添加了针对用户空间观察点的测试。值得注意的是，Sashiko AI 的审查指出了潜在的安全问题，认为该 patch 可能会破坏 pKVM 客户机的隔离性。Fuad 对此回应称，保护虚拟机状态隔离的工作正在进行中，预计很快会有进展。

#### 📝 邮件列表

1. **[07-26 15:36]** [PATCH 0/2] KVM: arm64: Fix host-directed debug for non-protected pKVM guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-26 15:36]** [PATCH 1/2] KVM: arm64: Flush external_mdscr_el1 to the pKVM hyp vCPU
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-26 15:36]** [PATCH 2/2] KVM: arm64: selftests: Add a userspace watchpoint test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-26 14:54]** Re: [PATCH 1/2] KVM: arm64: Flush external_mdscr_el1 to the pKVM
 hyp vCPU
   - 发件人: sashiko-bot@kernel.org
5. **[07-26 15:58]** Re: [PATCH 1/2] KVM: arm64: Flush external_mdscr_el1 to the pKVM hyp vCPU
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 20: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 11:51:00 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于修复 KVM 在 arm64 架构下的 hyp_trace 时钟禁用问题的补丁（PATCH v2）。该补丁由 Vincent Donnefort 提出，主要修复了 hyp_trace_clock_enable() 函数中的禁用路径问题，避免在取消工作后重新初始化和重新调度时钟。同时，清理了未使用的 hyp_trace_clock::lock 和冗余的 hyp_trace_clock::running，因为 trace_remote 框架已对回调 enable_tracing 的调用进行了序列化。

在历史讨论中，Vincent 提到该补丁修复了一个已存在于发布内核中的问题（提交 ID: b22888917fa41），并附上了相关的修复信息。

在本周的新讨论中，参与者 Fuad Tabba 建议将修复和清理分为两个独立的补丁，以便更好地进行回溯。Marc Zyngier 对此表示不太理解，但希望能尽快达成一致。最终，Fuad 表示对合并补丁没有强烈的偏好，并给予了补丁审核通过的反馈。Marc 最后确认该补丁已被应用于修复中，并感谢大家的贡献。

#### 📝 邮件列表

1. **[07-15 11:51]** [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-20 20:45]** Re: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-21 07:52]** Re: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-21 07:55]** Re: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-23 17:11]** Re: [PATCH v2] KVM: arm64: Fix hyp_trace clock disabling
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 21: [PATCH v2] KVM: arm64: Optimize protected mode and FWB

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 21 Jul 2026 08:56:45 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的优化补丁，主题为“[PATCH v2] KVM: arm64: Optimize protected mode and FWB”。该补丁旨在优化受保护模式下的缓存管理，特别是在支持 FWB（Fine-Grained Write Buffering）的情况下，避免不必要的缓存清理操作。

在历史讨论中，补丁的主要内容是通过在支持 FWB 的情况下提前返回，来优化 `__clean_dcache_guest_page()` 函数的执行，减少不必要的 TLB（Translation Lookaside Buffer）失效和数据同步操作。补丁的代码修改涉及到 `mem_protect.c` 文件，增加了对 FWB 支持的检查。

本周的新讨论中，参与者对补丁的细节进行了深入探讨。Marc Zyngier 指出补丁中的注释存在不准确之处，Mostafa Saleh 随后确认了这一点，并表示会更新注释。Fuad Tabba 提出建议，认为可以通过引用已有的注释来避免重复，并建议在同一补丁中对其他相关函数进行类似的优化。Mostafa 也同意了这一建议，表示将会在补丁中包含这些改动。

总体来看，本周的讨论集中在补丁的细节修正和代码注释的优化上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[07-21 08:56]** [PATCH v2] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-21 11:10]** Re: [PATCH v2] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-21 10:19]** Re: [PATCH v2] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-22 12:51]** Re: [PATCH v2] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-23 09:12]** Re: [PATCH v2] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 22: [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 20 Jul 2026 19:48:50 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在解决在禁用 hyp_trace_clock 时，时钟工作线程未能正确停止的问题。原始补丁由 Fuad Tabba 提出，主要修改了 `hyp_trace_clock_enable` 函数，确保在禁用时能够取消时钟工作并返回，避免在禁用后重新调度工作。

在之前的讨论中，补丁的背景是基于一个已知问题，即在调用 `hyp_trace_clock_enable()` 函数时，虽然取消了时钟工作，但由于代码逻辑错误，仍然会进入启用路径，导致时钟工作线程未能停止。该补丁旨在修复这一逻辑错误。

在本周的新讨论中，Fuad Tabba 提出了补丁并附上了相关的代码修改。Vincent Donnefort 参与了讨论，确认了之前的相关讨论链接，并表示感谢。同时，Sashiko AI 进行了代码审查，指出了补丁中存在的四个潜在问题，包括未初始化的堆栈内存使用和内核崩溃等。最后，Fuad 对讨论的干扰表示歉意，表明讨论仍在继续，期待进一步的反馈和修正。

#### 📝 邮件列表

1. **[07-20 19:48]** [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-20 20:01]** Re: [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-20 20:02]** Re: [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-20 19:03]** Re: [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable
   - 发件人: sashiko-bot@kernel.org
5. **[07-20 20:04]** Re: [PATCH] KVM: arm64: Stop the hyp trace clock worker on disable
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 23: [PATCH v13 00/32] KVM: arm64: Implement support for SME

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 00:07:27 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现对 SME（Scalable Matrix Extension）的支持。历史讨论中，Mark Brown 提出了一个补丁系列（PATCH v13 00/32），主要关注用户空间 ABI 的设计，特别是 SVE（Scalable Vector Extension）寄存器的向量长度和访问方式等问题。补丁的第二部分（PATCH v13 02/32）则涉及确保 ZCR_EL1 寄存器在从空闲状态恢复时被完全初始化，以避免未来硬件可能引发的问题。

在本周的新讨论中，Mark Rutland 对补丁提出了反馈，认为虽然当前实现有效，但应将其视为更广泛的架构问题，并建议将补丁抄送给稳定版内核，以确保未来硬件的兼容性。他还指出需要对代码进行小幅修改，建议将 'smcr' 变量的作用域限制在相关代码块内。然而，Rutland 在进一步审查后表示，当前的实现仍存在上下文同步不足的问题，需进一步探讨更为具体的解决方案。

总体而言，讨论集中在确保补丁的可靠性和未来兼容性上，参与者们对补丁的改进提出了建设性意见。

#### 📝 邮件列表

1. **[07-20 00:07]** [PATCH v13 00/32] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-20 00:07]** [PATCH v13 02/32] arm64/fpsimd: Ensure all of ZCR_EL1 is
 initialised from idle
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-23 13:58]** Re: [PATCH v13 02/32] arm64/fpsimd: Ensure all of ZCR_EL1 is
 initialised from idle
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[07-24 16:16]** Re: [PATCH v13 02/32] arm64/fpsimd: Ensure all of ZCR_EL1 is
 initialised from idle
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 24: [PATCH v8 00/21] ARM64 PMU Partitioning

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 17:46:19 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 PMU（性能监控单元）分区的补丁（PATCH v8 00/21）。该补丁旨在改善 ARM64 架构中虚拟机与宿主机之间的性能计数器管理。

在历史讨论中，补丁的背景和目标被阐明，但并未提供具体的历史邮件内容。本周的讨论主要集中在补丁的实现细节和潜在问题上。

本周的讨论中，James Clark 提出了对补丁的具体建议，认为默认参数 `arm_pmuv3.reserved_host_counters` 应设为 0 而非 -1，以便更直观地表示宿主机不保留计数器。此外，他报告了在测试中遇到的几个问题，包括在虚拟机中运行时性能计数器的异常行为。Colton Lewis 对这些问题表示关注，并承诺将进一步调查。同时，他提到可能需要改进文档，以帮助用户更好地理解参数设置和补丁的工作机制。

总体来看，本周的讨论强调了补丁在实际应用中的复杂性和潜在的错误，参与者们一致认为需要更清晰的文档和进一步的测试来确保补丁的有效性和稳定性。

#### 📝 邮件列表

1. **[07-20 17:46]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: James Clark <james.clark@linaro.org>
2. **[07-21 23:03]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[07-22 10:05]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: James Clark <james.clark@linaro.org>
4. **[07-23 20:57]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 25: [PATCH v2] KVM: arm64: Reject guest_memfd memslots when the VM has MTE

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 20 Jul 2026 14:09:42 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 guest_memfd 内存槽的处理，特别是在启用 MTE（Memory Tagging Extension）时的兼容性问题。

1. **原始 patch/问题的内容**：Alexandru Elisei 提出的补丁（PATCH v2）旨在解决在启用 MTE 的虚拟机中，无法使用由 guest_memfd 文件映射创建的内存槽的问题。补丁通过在创建内存槽时检查 MTE 状态，拒绝创建不兼容的内存槽，从而避免潜在的错误。

2. **之前的讨论要点**：虽然邮件中没有详细记录历史讨论，但可以推测之前的讨论涉及到如何处理 MTE 和 guest_memfd 的兼容性，以及在创建内存槽时可能存在的逻辑缺陷。

3. **本周的新讨论、进展或结论**：本周的讨论主要集中在补丁的审查和测试上。Fuad Tabba 对补丁进行了测试并表示支持，Marc Zyngier 提出补丁的合理性，但建议在文档中增加相关说明，以帮助新手理解。Alexandru Elisei 同意在下一个版本中更新文档。整体来看，补丁得到了积极的反馈，且即将进行改进。

#### 📝 邮件列表

1. **[07-20 14:09]** [PATCH v2] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-20 16:20]** Re: [PATCH v2] KVM: arm64: Reject guest_memfd memslots when the VM
 has MTE
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-20 16:46]** Re: [PATCH v2] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-21 10:10]** Re: [PATCH v2] KVM: arm64: Reject guest_memfd memslots when the VM
 has MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 26: [PATCH] KVM: arm64: Use consistent type for pool size

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 15 Jul 2026 15:01:25 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“使用一致的类型来表示池大小”。该补丁由 Mostafa Saleh 提出，主要目的是解决在 hypervisor 中所有池大小均为“unsigned long”，但在传递给 hyp_early_alloc_contig() 或 hyp_pool_init() 时会被截断为 32 位的问题。虽然目前这种截断不会造成严重问题，但随着新用户（如 IOMMU）的增加，池大小的推理变得更加复杂，因此需要进行修正。

在历史讨论中，Mostafa 提出了这一问题，并解释了潜在的溢出风险。补丁的提出旨在确保在未来的扩展中，池大小能够得到正确处理。

在本周的新讨论中，Will Deacon 和 Fuad Tabba 分别对该补丁表示认可，Will 表示已确认（Acked-by），而 Fuad 则表示已审核通过（Reviewed-by）。这表明该补丁得到了社区成员的支持，可能会在未来的版本中被合并。

#### 📝 邮件列表

1. **[07-15 15:01]** [PATCH] KVM: arm64: Use consistent type for pool size
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-26 15:01]** Re: [PATCH] KVM: arm64: Use consistent type for pool size
   - 发件人: Will Deacon <will@kernel.org>
3. **[07-26 16:11]** Re: [PATCH] KVM: arm64: Use consistent type for pool size
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 27: [PATCH v5 00/10] coco: guest: Enforce host page-size alignment for shared buffers

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 11:34:22 +0530

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v5 00/10] coco: guest: 强制共享缓冲区的主机页面大小对齐”。该补丁系列旨在加强在机密计算环境中，来宾与主机之间共享缓冲区的对齐要求。由于来宾使用私有内存，主机内核需要以大于来宾页面大小的粒度管理共享/私有状态，因此对齐要求显得尤为重要。

在历史讨论中，Aneesh Kumar K.V 提出了这一补丁，并详细阐述了其必要性，特别是在 CCA 系统中，Realm 阶段的映射由 RMM 管理，确保缓冲区的对齐可以提高系统的安全性和效率。此外，补丁还涉及将 Realm 内存加密操作移动到 RSI 代码中，以便更好地管理与固件接口的关系。

在本周的新讨论中，Will Deacon 对补丁中的某些内容提出了意见，认为将这些操作放在 arch/arm64 目录下并不合适，建议应将其移至 drivers/firmware/ 目录，以与其他 Arm 固件接口（如 PSCI 等）保持一致。这一反馈表明了对补丁结构和组织的关注，可能会影响后续的补丁修改和提交。

#### 📝 邮件列表

1. **[07-06 11:34]** [PATCH v5 00/10] coco: guest: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[07-06 11:34]** [PATCH v5 08/10] arm64: realm: Move Realm memory encryption ops to RSI code
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[07-21 23:03]** Re: [PATCH v5 08/10] arm64: realm: Move Realm memory encryption ops
 to RSI code
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 28: [PATCH] KVM: arm64: Optimize protected mode and FWB

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 20:35:29 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于优化 KVM 在 arm64 架构下的受保护模式和 FWB（Faulting Write Buffer）功能。最初的 patch 提出了在支持 FWB 的系统中，KVM 可以在处理来宾虚拟机时避免不必要的缓存维护，从而提高性能。具体来说，patch 优化了在受保护模式下调用 `__clean_dcache_guest_page()` 的流程，避免了不必要的循环和 TLB 失效操作。

在之前的讨论中，没有特别提到其他内容，但本周的讨论中，参与者 Mostafa Saleh 提出了 patch 的具体实现，并解释了在支持 FWB 的情况下，如何优化缓存清理操作。Fuad Tabba 对该 patch 表示认可，并建议在代码中增加注释，以便更好地解释在同一文件中不同函数对 FWB 的处理差异。Mostafa 随后回应，将在代码中添加注释，进一步阐明来宾和主机的区别，确保代码的可读性和维护性。

总的来说，本周的讨论集中在对 patch 的认可和细节的进一步完善上，推动了优化工作的进展。

#### 📝 邮件列表

1. **[07-20 20:35]** [PATCH] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-21 08:49]** Re: [PATCH] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-21 08:42]** Re: [PATCH] KVM: arm64: Optimize protected mode and FWB
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 29: [PATCH] KVM: arm64: GICv2: Bound the INTID in vgic_v2_deactivate()

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 25 Jul 2026 17:40:20 +0200

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下 GICv2（通用中断控制器版本2）实现的一个补丁，旨在限制 vgic_v2_deactivate() 函数中的 INTID（中断标识符）范围。

**原始补丁内容**：补丁的主要目的是在 vgic_v2_deactivate() 函数中添加对 INTID 的范围检查，以防止传入的 INTID 超出已实现中断的数量。之前的实现中，如果传入的 INTID 超出范围，可能导致查找返回 NULL，从而触发主机警告或在启用 panic_on_warn 时导致主机崩溃。

**之前讨论要点**：在补丁提交之前，讨论中提到 GICv3 已经实现了对 INTID 的范围检查，而 GICv2 缺乏此检查，因此需要进行修复。

**本周新讨论进展**：本周的讨论中，Karl Mehltretter 提出了补丁的具体实现，并解释了为何需要进行范围检查。Marc Zyngier 认为该检查与 GICv2 的现有逻辑重复，因为 GICv2 不支持 LPIs（本地中断），并建议直接去掉 WARN_ON() 的调用。整体来看，本周讨论围绕补丁的有效性和必要性展开，尚未达成最终结论。

#### 📝 邮件列表

1. **[07-25 17:40]** [PATCH] KVM: arm64: GICv2: Bound the INTID in vgic_v2_deactivate()
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>
2. **[07-25 18:12]** Re: [PATCH] KVM: arm64: GICv2: Bound the INTID in vgic_v2_deactivate()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 30: [PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 17:04:11 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 的补丁，主题为“[PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots”。该补丁的目的是在处理仅使用 guest_memfd 的内存插槽时，忽略 MMU 通知器。因为在这种情况下，虚拟机的内存提供者是 guest_memfd 文件，而不是用户空间映射，导致二级 MMU 与页表之间没有关系，因此 MMU 通知器不适用。

在历史讨论中，Alexandru Elisei 提出了这一补丁，并解释了其背景和必要性。补丁的核心在于解决 MMU 通知器对仅使用 guest_memfd 的内存插槽的影响。

在本周的新讨论中，Sean Christopherson 提到需要解决一个与此相关的问题，涉及到最近的提交（b9220d32799a），该提交允许直接使用固定的高虚拟地址（HVA）填充 gfn_to_pfn_cache，而不需要通过内存插槽。Sean 提出了一个未经过测试的解决方案，计划为 gfn_to_pfn_cache 创建自己的失效序列，从而避免处理仅使用 guest_memfd 的内存插槽。虽然他表示可能需要几周时间才能回到这个问题，但他将其列为高优先级任务，期望能在 7.3 版本中实现。

#### 📝 邮件列表

1. **[07-14 17:04]** [PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-24 12:52]** Re: [PATCH v2] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 31: [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Jul 2026 16:20:02 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于优化 KVM 在 arm64 架构下的受保护模式，主要涉及 FWB（Full Write Buffer）和 DIC（Data Cache Invalidate）功能的使用。

在历史讨论中，Mostafa Saleh 提出了一个补丁（patch v3），旨在通过在支持 FWB 的系统中为来宾虚拟机启用该功能，从而避免在受保护模式下不必要的缓存维护操作。具体来说，补丁优化了 `__clean_dcache_guest_page()` 和 `invalidate_icache_guest_page()` 函数，允许在满足条件时直接返回，减少了 TLB 失效和其他同步操作的调用。

本周的新讨论中，Mostafa Saleh 详细说明了补丁的实现细节，并指出在受保护模式下，若系统支持 FWB 和 DIC，则可以省略某些操作。Fuad Tabba 对该补丁进行了审查并表示支持，确认了补丁的有效性。

总结来看，本周的讨论主要集中在补丁的具体实现和审查反馈上，显示出对优化 KVM 性能的积极态度。

#### 📝 邮件列表

1. **[07-23 16:20]** [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-23 17:29]** Re: [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 32: [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in the nested context.

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 16:11:58 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的虚拟化问题，主要聚焦于避免在嵌套上下文中对 IRQ（中断请求）进行双重停用的情况。

在历史讨论中，D Scott Phillips 提出了一个补丁（patch v2），旨在解决在嵌套状态下，物理中断已经通过硬件位在 LR（Link Register）中停用的情况下，避免额外的停用操作。虽然额外的停用操作在理论上是无害的，但在 AmpereOne 处理器上可能会引发一个错误，导致 CPU 丢失中断挂起状态，并阻止未来中断的传递。该补丁的目标是修复这一问题，并引用了相关的修复记录。

在本周的新讨论中，Marc Zyngier 对该补丁表示感谢，并确认已将其应用于修复列表中，补丁的提交记录为 8a570b19b4b16a8a3b5ffa2b332bd5613110b2d8。这表明该补丁已获得认可并正式纳入代码库。

#### 📝 邮件列表

1. **[07-14 16:11]** [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in the nested context.
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>
2. **[07-23 17:11]** Re: [PATCH v2] KVM: arm64: vgic: Avoid double-deactivate of IRQs in the nested context.
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 33: [PATCH] KVM: arm64: Update Fuad Tabba's email address

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 19 Jul 2026 17:32:57 +0100

#### 🤖 AI 总结

在本次邮件讨论中，Fuad Tabba 提出了一个补丁（patch），旨在更新其在 KVM/arm64 项目中的邮箱地址，将其更改为 fuad.tabba@linux.dev，并在 .mailmap 文件中添加相应条目，以便将之前使用的 tabba@google.com 的提交记录映射到新地址。补丁的具体修改涉及两个文件：.mailmap 和 MAINTAINERS。

在历史讨论中，Fuad Tabba 详细说明了补丁的目的和内容，强调了更新邮箱地址的重要性，以确保其在内核工作中的身份一致性。

在本周的新讨论中，Marc Zyngier 对该补丁进行了确认，表示已将其应用于修复（fixes）中，并感谢 Fuad Tabba 的提交。这表明补丁已经获得认可并成功合并，进一步推动了项目的进展。

#### 📝 邮件列表

1. **[07-19 17:32]** [PATCH] KVM: arm64: Update Fuad Tabba's email address
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-23 17:11]** Re: [PATCH] KVM: arm64: Update Fuad Tabba's email address
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 34: [PATCH v6 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Jul 2026 12:51:36 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的虚拟化通用中断控制器（vgic）中，修复与 LPI（本地中断线）释放和重新注册相关的竞争条件问题。

在历史讨论中，Carlos López 提出了一个补丁（PATCH v6 0/2），旨在解决两个潜在问题：一是可能导致 LPI 结构泄漏或被过早删除的竞争条件，二是注册 LPI 时可能出现的虚假 -ENOMEM 错误。补丁的更新版本（v6）移除了一个可能导致使用后释放（use-after-free）和虚假警告的变量，并避免了锁反转问题。

在本周的新讨论中，Marc Zyngier 确认了补丁已被应用于修复中，并感谢了 Carlos 的贡献。具体补丁包括：
1. 修复 LPI 释放与重新注册之间的竞争条件（commit: cbfe2b24a1ea9de35032dbdd100fdc700f5be92d）。
2. 缓解潜在的 LPI 注册失败问题（commit: 21f12496fdd357ad4e1fcdd07dc80ab7378f7d24）。

整体而言，此次讨论推动了对 KVM 中 LPI 处理的改进，增强了系统的稳定性和可靠性。

#### 📝 邮件列表

1. **[07-15 12:51]** [PATCH v6 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-23 17:11]** Re: [PATCH v6 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 35: [PATCH v4] KVM: arm64: Reject guest_memfd memslots when the VM has MTE

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 22 Jul 2026 10:03:54 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 guest_memfd 内存槽的处理，特别是在启用 MTE（Memory Tagging Extension）时的限制。

**原始 patch 内容**：
Alexandru Elisei 提出的 patch 旨在解决当虚拟机启用 MTE 时，禁止使用 guest_memfd 作为内存槽的情况。由于现有实现中，创建 guest_memfd 支持的内存槽时并未检查 MTE 的状态，可能导致不兼容的内存配置。

**之前讨论要点**：
在历史讨论中，虽然没有具体的邮件记录，但可以推测出该问题的背景是由于 KVM 的内存管理逻辑未能充分考虑 MTE 和 guest_memfd 之间的兼容性，导致潜在的错误配置。

**本周的新讨论与进展**：
在本周的讨论中，Alexandru Elisei 提交了 patch v4，明确指出当虚拟机启用 MTE 时，任何基于 guest_memfd 的内存槽都将被拒绝。此外，Marc Zyngier 迅速回应并确认已将该 patch 应用到修复列表中，表示感谢。这表明该问题得到了及时的关注和解决。

总体来看，此次讨论有效地解决了 KVM 在处理 MTE 和 guest_memfd 时的兼容性问题，确保了系统的稳定性和可靠性。

#### 📝 邮件列表

1. **[07-22 10:03]** [PATCH v4] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-23 17:10]** Re: [PATCH v4] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 36: [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 10:52:00 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 s390 架构中引入 arm64 支持的补丁系列（PATCH v4 00/27）。历史讨论中，Steffen Eiden 提出了一个全新的补丁方案，旨在通过在构建时提取 arm64 的相关定义和实现部分，而不是将 arm64 代码移动到共享位置，从而实现 s390 和 arm64 之间的代码和头文件共享。这种新方法旨在对现有的 arm64 代码和头文件进行最小化修改。

在之前的讨论中，参与者们关注了补丁的设计思路及其对现有代码的影响，强调了代码共享的必要性和实现的复杂性。

在本周的新讨论中，Christian Borntraeger 表示，为了缩小补丁集的规模，他愿意将一些机械性的修改纳入 kvms390->next 分支，并指出这些修改需要进一步的审查和润色，但整体上应该比较简单。这表明该补丁集正在朝着更小、更易于管理的方向发展，并且参与者们对其后续进展持积极态度。

#### 📝 邮件列表

1. **[07-06 10:52]** [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[07-23 14:55]** Re: [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>

---

### Thread 37: [PATCH v3 8/9] KVM: arm64: selftests: Add infrastructure for
 using stage-2 in guest

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Jul 2026 11:47:16 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试基础设施，特别是如何在来宾环境中使用 stage-2 的实现。原始的 patch（[PATCH v3 8/9]）旨在为 KVM 提供支持 stage-2 的自测试框架。

在之前的讨论中，参与者们关注了该 patch 的设计，特别是如何处理地址空间的配置。Itaru Kitayama 提到，当前实现似乎不支持在 16KB 粒度和 DS=0 的情况下使用 48 位 IPA（Intermediate Physical Address），因为这需要两个连接的一级根表。

本周的新讨论中，Itaru 指出 R_DXBSH 的存在使得必须使用连接的翻译表，而 Wei-Lin Chang 则表示他最初的设计是为了避免使用连接的翻译表，以简化实现，但现在面临问题。他提出可以考虑特殊处理这种情况，或者像 KVM 一样始终使用连接的翻译表。讨论表明，参与者们在寻求最佳解决方案，以确保实现的有效性和简洁性。

#### 📝 邮件列表

1. **[07-23 11:47]** Re: [PATCH v3 8/9] KVM: arm64: selftests: Add infrastructure for
 using stage-2 in guest
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
2. **[07-23 10:54]** Re: [PATCH v3 8/9] KVM: arm64: selftests: Add infrastructure for
 using stage-2 in guest
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 38: [PATCH 11/21] KVM: arm64: Context swap Partitioned PMU guest
 registers

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 17:46:37 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“[PATCH 11/21] KVM: arm64: Context swap Partitioned PMU guest registers”。该补丁旨在改进分区 PMU（性能监控单元）访客寄存器的上下文切换。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁是为了解决在虚拟化环境中对 PMU 寄存器的管理问题，可能涉及到动态访客计数器的预留。

在本周的新讨论中，参与者 James Clark 和 Colton Lewis 进行了交流。James 指出，某个函数（kvm_pmu_guest_counter_mask()）在补丁中添加之前就已被使用，暗示补丁的实现可能存在顺序问题。Colton 随即承认了这个错误，并表示将进行修正。

总体来看，本周的讨论主要集中在补丁实现的细节和函数调用顺序的确认上，参与者们积极沟通以确保补丁的正确性和有效性。

#### 📝 邮件列表

1. **[07-20 17:46]** Re: [PATCH 11/21] KVM: arm64: Context swap Partitioned PMU guest
 registers
   - 发件人: James Clark <james.clark@linaro.org>
2. **[07-21 23:05]** Re: [PATCH 11/21] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 39: [PATCH v2] KVM: arm64: Sync SCTLR_EL1 when injecting an exception into a pVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Jul 2026 17:16:24 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构中处理异常时的补丁，标题为「[PATCH v2] KVM: arm64: Sync SCTLR_EL1 when injecting an exception into a pVM」。

**原始补丁内容**：
该补丁旨在解决在向受保护的虚拟机（pVM）注入同步异常时，未同步 SCTLR_EL1 寄存器的问题。具体来说，当 pKVM 注入异常时，`enter_exception64()` 函数会读取 SCTLR_EL1 来设置新的 PSTATE 的 PAN 和 SSBS 位，但在注入异常前，pKVM 只更新了 VBAR_EL1，而没有同步 SCTLR_EL1，这可能导致虚拟机在更新后再陷入异常时使用过时的 PAN/SSBS 值。

**之前讨论要点**：
邮件中没有提供历史讨论的具体内容，说明该补丁可能是首次提交，或之前的讨论未被记录。

**本周新讨论及进展**：
在本周的讨论中，Fuad Tabba 提交了补丁的第二版，并指出该补丁已基于 v7.2-rc4 进行了重基，并没有功能上的变化。随后，Oliver Upton 回复确认已将该补丁应用到下一个版本中，表示感谢。这表明该补丁得到了认可并将被纳入未来的内核版本中。

#### 📝 邮件列表

1. **[07-21 17:16]** [PATCH v2] KVM: arm64: Sync SCTLR_EL1 when injecting an exception into a pVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-21 11:26]** Re: [PATCH v2] KVM: arm64: Sync SCTLR_EL1 when injecting an exception into a pVM
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 40: [PATCH v3] KVM: arm64: Reject guest_memfd memslots when the VM has MTE

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Jul 2026 11:06:54 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 guest_memfd 内存槽的处理，特别是在启用 MTE（Memory Tagging Extension）时的限制。

**原始 patch/问题内容**：
Alexandru Elisei 提出的补丁（PATCH v3）旨在解决当虚拟机启用 MTE 时，禁止创建基于 guest_memfd 的内存槽。由于当前实现中，arch_calc_vm_flag_bits() 并未设置 VM_MTE_ALLOWED，导致用户能够在不满足条件的情况下成功创建内存槽，进而引发潜在问题。

**之前讨论要点**：
在之前的讨论中，补丁的必要性得到了认可，主要集中在确保 MTE 和 guest_memfd 之间的兼容性问题。补丁明确指出，启用 MTE 后，任何与 guest_memfd 相关的内存槽创建都应被拒绝。

**本周的新讨论、进展或结论**：
本周的讨论中，Alexandru 提交了补丁的第三版，增加了文档说明，明确指出 guest_memfd 与 MTE 不兼容，并进行了相关代码的修改。Fuad Tabba 对补丁进行了审查，提出了一些小的语言修正建议，并表示支持补丁的方向，但建议将“不兼容”改为“未支持”，以便于未来可能的更改。整体来看，讨论推动了补丁的完善和最终提交的准备。

#### 📝 邮件列表

1. **[07-21 11:06]** [PATCH v3] KVM: arm64: Reject guest_memfd memslots when the VM has MTE
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-21 11:51]** Re: [PATCH v3] KVM: arm64: Reject guest_memfd memslots when the VM
 has MTE
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 41: [PATCH v2] KVM: arm64: GICv2: Don't WARN on out-of-range GICV_DIR INTID

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 26 Jul 2026 19:48:03 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的 GICv2（通用中断控制器版本2）处理中的一个补丁。补丁的主要内容是修改 `vgic_v2_deactivate()` 函数，避免在处理超出范围的 GICV_DIR INTID 时触发 WARN_ON_ONCE() 警告。

在历史讨论中，补丁的背景是由于 GICv2 不支持 LPI（本地中断），因此当来宾（guest）写入一个超出 SGI、PPI 和 SPI 范围的 INTID 时，查找将返回 NULL，这会导致触发 WARN 警告并可能导致主机崩溃。之前的讨论集中在如何处理这种情况，并提出了警告处理不当可能带来的风险。

在本周的新讨论中，开发者 Karl Mehltretter 提出了补丁的更新版本（v2），决定去掉 WARN_ON_ONCE()，因为在查找前对 INTID 进行范围限制会与 `vgic_get_irq()` 函数中已经执行的范围检查重复。补丁得到了 Marc Zyngier 的建议，并且已提交给稳定版维护团队。

总的来说，本周的讨论主要集中在补丁的优化和对潜在问题的修正上，旨在提高系统的稳定性和可靠性。

#### 📝 邮件列表

1. **[07-26 19:48]** [PATCH v2] KVM: arm64: GICv2: Don't WARN on out-of-range GICV_DIR INTID
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>

---

### Thread 42: [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 23 Jul 2026 17:11:11 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“添加缺失的 hyp_enter 以处理 sysreg 的陷入”。该补丁旨在修复在捕获系统寄存器时缺少 hyp_enter 的问题。

在历史讨论部分，虽然没有具体的讨论记录，但可以推测该补丁是为了确保在处理系统寄存器时，能够正确地进入 Hypervisor 模式，从而提高虚拟化的稳定性和性能。

在本周的新讨论中，Marc Zyngier 对补丁进行了确认，并表示已将其应用于修复列表中，感谢补丁的提交者 Vincent Donnefort。这表明该补丁得到了认可，并将被纳入后续的代码更新中。

总体来看，本周的进展显示出该补丁已经成功被采纳，解决了 KVM 在 arm64 平台上处理系统寄存器时的一个关键问题。

#### 📝 邮件列表

1. **[07-23 17:11]** Re: [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 RFC

共 7 个 thread

---

### Thread 1: [RFC PATCH v3 00/19] named CPU models for Arm64 on KVM

**📧 邮件数**: 24 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 16 Jul 2026 21:38:39 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 上 Arm64 的命名 CPU 模型的 RFC PATCH v3，主要由 Khushit Shah 提出。该补丁系列旨在为 QEMU 添加命名 CPU 模型的支持，主要改进包括基于 Eric Auger 的“可定制主机模型”系列进行重构，并采用了新的 SYSREG_<REG>_<FIELD>=<u64> 属性约定。与之前版本相比，v3 减少了许多复杂性，去除了“复合体”概念及缓存信息的暴露支持。

在历史讨论中，参与者们对补丁的实现细节进行了深入探讨，尤其是如何处理 ID 寄存器的字段暴露和可写性的问题。Eric Auger 提出了对补丁的多个建议，包括将某些补丁拆分以便于审查，以及对非可写寄存器的暴露是否合理等问题。

在本周的新讨论中，Eric 针对每个补丁提出了具体的反馈，强调需要更清晰的文档和代码结构，以便于理解和审查。例如，他建议在补丁描述中添加所有 ID 寄存器的转储信息，并对每个模型使用单独的补丁进行处理。此外，他对补丁中某些功能的必要性和实现方式提出了质疑，认为应当考虑更简洁的解决方案，以避免不必要的复杂性。整体来看，本周的讨论集中在补丁的细节审查和优化建议上。

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
11. **[07-16 21:38]** [RFC PATCH v3 14/19] target/arm/kvm: compute supported values for ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
12. **[07-16 21:38]** [RFC PATCH v3 16/19] qmp: add query-cpu-props-info command
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
13. **[07-20 14:11]** Re: [RFC PATCH v3 01/19] target/arm/sysreg: regenerate
 cpu-sysregs.h.inc
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[07-20 16:24]** Re: [RFC PATCH v3 02/19] scripts: bug fixes in
 update-aarch64-cpu-sysreg-properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[07-20 16:39]** Re: [RFC PATCH v3 03/19] target/arm: regenerate cpu-idregs.h.inc
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[07-21 16:44]** Re: [RFC PATCH v3 04/19] target/arm: expose all ID regs fields as
 properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[07-21 17:03]** Re: [RFC PATCH v3 05/19] target/arm/kvm: enable writable
 implementation ID registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[07-22 08:54]** Re: [RFC PATCH v3 06/19] target/arm/kvm: Read all ID registers from
 KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[07-22 14:05]** Re: [RFC PATCH v3 08/19] target/arm/kvm: Handle writeback for special
 ID register fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
20. **[07-22 14:32]** Re: [RFC PATCH v3 07/19] target/arm/kvm: handle special ID registers
 cases when reading from KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
21. **[07-26 15:14]** Re: [RFC PATCH v3 09/19] target/arm: Add named cpu model infra +
 graviton3 named model
   - 发件人: Eric Auger <eric.auger@redhat.com>
22. **[07-26 15:34]** Re: [RFC PATCH v3 09/19] target/arm: Add named cpu model infra +
 graviton3 named model
   - 发件人: Eric Auger <eric.auger@redhat.com>
23. **[07-26 15:56]** Re: [RFC PATCH v3 08/19] target/arm/kvm: Handle writeback for special
 ID register fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
24. **[07-26 16:22]** Re: [RFC PATCH v3 14/19] target/arm/kvm: compute supported values for
 ID register fields
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 2: [RFC PATCH v7 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 19 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 26 Jul 2026 17:29:38 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于增强 KVM/ARM 的补丁系列，主题为引入可定制的 AArch64 KVM 主机模型。该补丁的主要目标是增加对可写 ID 寄存器字段的支持，以提高在不同主机硬件之间迁移虚拟机的灵活性。

**原始补丁内容**：
补丁系列的核心是增强现有的 KVM 主机模型，使用户空间能够覆盖部分 ID 寄存器的值。补丁定义了可写字段的范围，并通过 QEMU 的 QMP 监控接口提供这些字段的信息。

**历史讨论要点**：
之前的讨论集中在如何处理可写 ID 寄存器的描述和生成，确保与 ARM 架构手册一致。补丁逐步演进，解决了多个问题，包括对枚举值的处理和寄存器初始化的改进。

**本周新讨论与进展**：
1. **新功能实现**：引入了 `kvm_arm_expose_idreg_properties` 函数，分析可写掩码并为可写字段生成属性。这些属性的命名遵循 `SYSREG_<REG>_<FIELD>` 的格式。
2. **文档更新**：增加了对 ID 寄存器属性的文档说明，阐明如何通过主机 CPU 模型配置可选功能。
3. **错误处理**：实现了对意外可写保留字段的跟踪和忽略，确保系统的稳定性。
4. **测试与验证**：通过 QMP 命令验证可写 ID 寄存器的值，确保设置的值符合字段的长度和枚举值要求。

总的来说，该补丁系列的目标是提升 KVM/ARM 在虚拟化环境中的灵活性和稳定性，使得在不同硬件之间迁移虚拟机变得更加可靠。

#### 📝 邮件列表

1. **[07-26 17:29]** [RFC PATCH v7 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[07-26 17:29]** [RFC PATCH v7 01/18] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[07-26 17:29]** [RFC PATCH v7 02/18] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[07-26 17:29]** [RFC PATCH v7 03/18] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[07-26 17:29]** [RFC PATCH v7 04/18] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[07-26 17:29]** [RFC PATCH v7 05/18] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[07-26 17:29]** [RFC PATCH v7 06/18] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[07-26 17:29]** [RFC PATCH v7 07/18] target/arm/cpu-idregs.h.inc: generate with script
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[07-26 17:29]** [RFC PATCH v7 08/18] target/arm/cpu-idregs.h.inc: Generate enum values
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[07-26 17:29]** [RFC PATCH v7 09/18] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[07-26 17:29]** [RFC PATCH v7 10/18] target/arm/kvm: Retrieve writable ID reg map
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[07-26 17:29]** [RFC PATCH v7 11/18] arm/kvm: Initialize all writable ID registers from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[07-26 17:29]** [RFC PATCH v7 12/18] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[07-26 17:29]** [RFC PATCH v7 13/18] target/arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[07-26 17:29]** [RFC PATCH v7 14/18] target/arm/cpu-idregs.h.inc: Generate reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[07-26 17:29]** [RFC PATCH v7 15/18] target/arm/kvm: Ignore and trace unexpected writable reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[07-26 17:29]** [RFC PATCH v7 16/18] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[07-26 17:29]** [RFC PATCH v7 17/18] target/arm/kvm: add utility to write idregs in scratch vcpu
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[07-26 17:29]** [RFC PATCH v7 18/18] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 3: [RFC PATCH 0/2] KVM: arm64: Support BBM level 3

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 17 Jul 2026 13:08:58 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中支持 BBM（Break-Before-Make）级别 3 的补丁系列。最初的补丁由 Mostafa Saleh 提出，目的是为了在 KVM 页表中实现 BBM 级别 3 的支持，这对于主机 CPU 的 stage-2 和 SMMUv3 之间的页面表共享以及在 CPU 操作中避免中间翻译中断具有重要意义。

在历史讨论中，参与者探讨了 BBM 级别 3 的设计和实现细节，包括如何原子性地更新 PTE（Page Table Entry）以及与现有特性的兼容性。Oliver Upton 提出了对实现条件的建议，认为应当依赖于特定的硬件特性以确保 BBM 级别 3 的有效性。

在本周的新讨论中，Mostafa Saleh 指出了一些现有的低效之处，并提出了改进建议，例如在处理 dcache 和 icache 时的优化。Oliver Upton 和 Marc Zyngier 也参与了讨论，确认了某些优化的实现方式，并探讨了在 KVM 中使用的指令的必要性。整体上，本周的讨论集中在对补丁的进一步优化和实现细节的澄清上。

#### 📝 邮件列表

1. **[07-17 13:08]** [RFC PATCH 0/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-17 13:09]** [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-17 13:56]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[07-18 19:54]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[07-20 21:41]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[07-20 23:34]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[07-21 07:36]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-21 08:34]** Re: [RFC PATCH 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 4: [RFC PATCH v1 0/2] KVM: arm64: CCA: Add MEC policy support for CCA Realms

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 24 Jul 2026 18:40:54 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中为 ARM64 架构的 CCA（Confidential Computing Architecture）领域添加 MEC（Memory Encryption Context）策略支持的补丁系列。

**原始补丁内容**：
Kohei Enju 提出了两个补丁，第一部分引入了一个新的 ioctl 接口 KVM_ARM_RMI_CONFIG，允许用户在创建 Realm 之前选择共享或私有的 MEC 策略，默认使用共享策略。第二部分则为 CCA MECIDs 添加了一个资源计费机制，用于管理使用私有 MEC 策略的 Realm。

**历史讨论要点**：
在之前的讨论中，补丁系列基于 Steven Price 的 CCA 主机系列，Kohei 表示希望在相关主机系列合并后更新这些补丁，并将其发布为非 RFC 版本。

**本周新讨论进展**：
本周的讨论中，Kohei 继续阐述补丁的细节，并请求对 KVM ABI 和使用 misc cgroup 进行 MECID 计费的反馈。参与者 Michal Koutný 对补丁表示部分认可，但指出在合并当前补丁之前，需先处理相关依赖的补丁系列。Kohei 也确认了这一点，并表示希望在依赖系列合并后再提交非 RFC 版本。

总的来说，本周的讨论集中在补丁的设计架构和依赖关系上，参与者们对补丁的方向表示支持，但强调了依赖补丁的重要性。

#### 📝 邮件列表

1. **[07-24 18:40]** [RFC PATCH v1 0/2] KVM: arm64: CCA: Add MEC policy support for CCA Realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
2. **[07-24 18:40]** [RFC PATCH v1 1/2] KVM: arm64: CCA: Add support for configuring the Realm MEC policy
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
3. **[07-24 18:40]** [RFC PATCH v1 2/2] cgroup/misc: Add support for Arm CCA MECIDs
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
4. **[07-24 14:52]** Re: [RFC PATCH v1 2/2] cgroup/misc: Add support for Arm CCA MECIDs
   - 发件人: Michal =?utf-8?Q?Koutn=C3=BD?= <mkoutny@suse.com>
5. **[07-25 00:38]** Re: [RFC PATCH v1 2/2] cgroup/misc: Add support for Arm CCA MECIDs
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>

---

### Thread 5: [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Jul 2026 18:21:38 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中为 arm64 架构添加对 BBM（Break-Before-Make）级别 3 的支持。Mostafa Saleh 提出了两个补丁（patch），旨在改进页表管理。

第一个补丁 `stage2_clean_old_pte()` 的目的是清理旧的 PTE（Page Table Entry），以支持 BBM 级别 3 的逻辑。第二个补丁则实现了 BBM 级别 3 的具体支持，允许直接替换 stage-2 PTE，而无需使用软件 BBM 序列。

在历史讨论中，Mostafa 提到 BBM 级别 3 对于 CPU 操作非常有用，特别是在处理页表共享和 SMMUv3 的上下文中。补丁的设计考虑了不同的条件下 BBM 的应用场景，并进行了相应的代码重构，以提高可读性和性能。

本周的新讨论中，Mostafa 提到补丁的测试情况，包括在 C1-Pro 核心和 Qualcomm X1 上的测试结果，未发现冲突中止或 TLB（Translation Lookaside Buffer）损坏。此外，Sashiko AI 评审指出了一个潜在问题，即在 MTE（Memory Tagging Extension）标签存储和 stage-2 PTE 更新之间缺少 DSB（Data Synchronization Barrier）。Mostafa 对此回应表示需要在 `sanitise_mte_tags()` 结束时添加 DSB，以解决可能的竞态条件。

总体来看，本周的讨论集中在补丁的实现细节和潜在问题的解决上，推动了 KVM 的进一步优化。

#### 📝 邮件列表

1. **[07-23 18:21]** [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-23 18:21]** [RFC PATCH v2 1/2] KVM: arm64: Add stage2_clean_old_pte()
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-23 18:21]** [RFC PATCH v2 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-23 18:43]** Re: [RFC PATCH v2 2/2] KVM: arm64: Support BBM level 3
   - 发件人: sashiko-bot@kernel.org
5. **[07-24 08:17]** Re: [RFC PATCH v2 2/2] KVM: arm64: Support BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 6: [RFC PATCH v3 16/19] qmp: add query-cpu-props-info command

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 20 Jul 2026 15:21:22 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为“query-cpu-props-info”命令的 RFC PATCH v3 版本的提案。该补丁旨在为 QEMU 的 QMP（QEMU Machine Protocol）添加一个新的命令，以查询 CPU 属性信息。

在历史讨论中，尚未提供具体的内容或反馈，因此没有相关的讨论要点可供总结。

在本周的新讨论中，参与者 Markus Armbruster 表达了对该补丁的关注，指出目前该系列补丁无法应用于他的环境。他表示需要能够应用补丁，以便检查渲染后的文档，并请求将补丁推送到一个可以供他拉取的位置。这表明该补丁尚未得到广泛测试或验证，参与者希望能进一步推进该补丁的应用和文档检查。

#### 📝 邮件列表

1. **[07-20 15:21]** Re: [RFC PATCH v3 16/19] qmp: add query-cpu-props-info command
   - 发件人: Markus Armbruster <armbru@redhat.com>

---

### Thread 7: [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum
 values

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 20 Jul 2026 15:15:42 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM 架构的补丁（RFC PATCH v6 08/17），该补丁旨在生成枚举值，具体体现在 `target/arm/cpu-idregs.h.inc` 文件中。

在历史讨论中，补丁的初衷是通过脚本生成特定的值范围，以便更好地支持 ARM CPU 的寄存器描述。然而，邮件中并没有提供详细的历史讨论内容。

在本周的新讨论中，参与者 Eric Auger 对补丁的生成结果提出了疑问。他指出，当前脚本生成的值范围（如 SMIDR_EL1.HIP）只返回一个单一值，而不是预期的范围（例如 1 到 15）。他认为这可能不是补丁的最终目标，并提到在生成的差异中并未发现关于“十进制 10 可能被错误解析为 2”的问题，尽管这仍然可能是一个潜在问题。

总的来说，本周的讨论集中在补丁生成的值范围的准确性上，Eric 提出了对补丁进一步改进的建议。

#### 📝 邮件列表

1. **[07-20 15:15]** Re: [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum
 values
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.2, take #3

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 24 Jul 2026 09:47:42 +0100

#### 🤖 AI 总结

本邮件主题为“KVM/arm64 fixes for 7.2, take #3”，由Marc Zyngier于2026年7月24日发送，主要讨论了针对KVM/arm64的修复补丁。

本次补丁主要解决了两个领域的问题：一是修复了与LPI（中断优先级中断）映射相关的竞争条件，二是处理EL2（异常级别2）跟踪管理中的边界情况。此外，补丁还包括了一些CPU缺陷的解决方案、API的整理以及低影响的修复。

具体修复内容包括：
- 修复了从嵌套客户机传播中断停用时的小错误。
- 解决了LPI解除映射和重新注册之间的竞争条件，防止了LPI泄漏。
- 增强了内存分配失败时的LPI映射的稳健性。
- 修复了EL2跟踪时钟禁用的处理。
- 增加了EL2代码中缺失的系统寄存器跟踪点。
- 整理了guest-memfd和MTE的互斥关系。

本周没有其他参与者的回复或讨论，邮件内容集中在补丁的提交和修复内容的概述上。整体来看，这些修复旨在提升KVM/arm64的稳定性和性能。

#### 📝 邮件列表

1. **[07-24 09:47]** [GIT PULL] KVM/arm64 fixes for 7.2, take #3
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Discussion

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section
 for LLVM objcopy compatibility

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 21 Jul 2026 23:07:32 +0000

#### 🤖 AI 总结

本邮件主题为“[kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for LLVM objcopy compatibility”，涉及到对 KVM 单元测试的 Makefile 进行修改，以确保与 LLVM objcopy 的兼容性，特别是保留 .dynstr 段。

在历史讨论中，未有相关的讨论记录，因此本周的新讨论是唯一的内容。Colton Lewis 在邮件中感谢了 Andrew Jones，暗示可能是对之前提出的补丁或建议的认可，但具体的讨论细节并未展开。

本周的进展主要是对补丁的确认，表明该补丁得到了参与者的支持，尽管没有进一步的技术细节或问题被提出。整体来看，本周的讨论集中在对补丁的认可上，未涉及新的技术问题或挑战。

#### 📝 邮件列表

1. **[07-21 23:07]** Re: [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section
 for LLVM objcopy compatibility
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for
 LLVM objcopy compatibility

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 16 Jul 2026 17:33:15 +0000

#### 🤖 AI 总结

在本次邮件讨论中，主题为“[kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for LLVM objcopy compatibility”。历史讨论中，Colton Lewis 提出了一个补丁，旨在解决在使用 llvm-objcopy 构建 EFI 二进制文件时遇到的问题。具体来说，当保留动态节（.dynamic）和符号表（.dynsym）而不保留字符串表（.dynstr）时，会导致构建失败，出现错误提示，表明 .dynstr 节无法被移除，因为它被 .dynamic 节引用。因此，他建议在 arm、riscv 和 x86 的 Makefile 中加入对 .dynstr 节的保留，以确保 EFI 二进制文件能够顺利构建。

在本周的新讨论中，Andrew Jones 回复表示已将该补丁推送（pushed），确认了补丁的实施。这表明该问题得到了及时解决，补丁已被采纳并应用于相关代码中。整体来看，此次讨论有效地解决了 EFI 二进制构建中的兼容性问题。

#### 📝 邮件列表

1. **[07-16 17:33]** [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section for
 LLVM objcopy compatibility
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-21 10:58]** Re: [kvm-unit-tests PATCH] Makefile: efi: preserve .dynstr section
 for LLVM objcopy compatibility
   - 发件人: Andrew Jones <andrew.jones@linux.dev>

---

