# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-08-03 00:39:28

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 589
- **总 Thread 数**: 45
- **大型 Thread** (>20封): 9 个

### 分类分布

- **PATCH**: 37 threads (570 邮件)
- **RFC**: 7 threads (17 邮件)
- **GIT PULL**: 1 threads (2 邮件)

---

## 📌 PATCH

共 37 个 thread

---

### Thread 1: [PATCH v4 00/48] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 103 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 24 Jul 2026 10:48:25 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:63 新:40, 19049 tokens)

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
5. **[07-24 10:49]** [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-24 10:50]** [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[07-24 10:50]** [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-24 10:50]** [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[07-24 10:51]** [PATCH v4 13/48] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[07-24 10:52]** [PATCH v4 14/48] KVM: arm64: gic-v5: Set up VMTEs and VPE doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[07-24 10:52]** [PATCH v4 15/48] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[07-24 10:52]** [PATCH v4 16/48] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[07-24 10:53]** [PATCH v4 19/48] KVM: arm64: gic-v5: Add KVM_VGIC_V5_ADDR_TYPE_IRS to
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[07-24 10:53]** [PATCH v4 20/48] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[07-24 10:54]** [PATCH v4 22/48] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[07-24 10:54]** [PATCH v4 23/48] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[07-24 10:54]** [PATCH v4 25/48] KVM: arm64: gic-v5: Add GIC VDPEND hyp call
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[07-24 10:55]** [PATCH v4 26/48] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[07-24 10:55]** [PATCH v4 27/48] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[07-24 10:55]** [PATCH v4 29/48] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[07-24 10:56]** [PATCH v4 30/48] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[07-24 10:56]** [PATCH v4 31/48] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg userspace
 accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[07-24 10:56]** [PATCH v4 32/48] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[07-24 10:57]** [PATCH v4 34/48] KVM: arm64: gic-v5: Add VGICv5 IST save/restore UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[07-24 10:57]** [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[07-24 10:57]** [PATCH v4 37/48] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[07-24 10:58]** [PATCH v4 38/48] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[07-24 10:58]** [PATCH v4 41/48] KVM: selftests: Add VGICv5 NR_IRQS attribute tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[07-24 10:59]** [PATCH v4 42/48] KVM: selftests: Add VGICv5 IRS_REGS attribute tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[07-24 11:00]** [PATCH v4 46/48] KVM: selftests: Add VGICv5 SPI injection tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[07-24 11:00]** [PATCH v4 47/48] KVM: selftests: Add VGICv5 LPI delivery tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[07-24 11:10]** Re: [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: sashiko-bot@kernel.org
33. **[07-24 11:11]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: sashiko-bot@kernel.org
34. **[07-24 11:14]** Re: [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: sashiko-bot@kernel.org
35. **[07-24 11:19]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from
 IRS config frame
   - 发件人: sashiko-bot@kernel.org
36. **[07-24 11:19]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI
 hosts
   - 发件人: sashiko-bot@kernel.org
37. **[07-24 11:21]** Re: [PATCH v4 01/48] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: sashiko-bot@kernel.org
38. **[07-24 11:21]** Re: [PATCH v4 13/48] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: sashiko-bot@kernel.org
39. **[07-24 11:22]** Re: [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: sashiko-bot@kernel.org
40. **[07-24 11:26]** Re: [PATCH v4 15/48] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: sashiko-bot@kernel.org
41. **[07-24 11:27]** Re: [PATCH v4 14/48] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: sashiko-bot@kernel.org
42. **[07-24 11:30]** Re: [PATCH v4 19/48] KVM: arm64: gic-v5: Add
 KVM_VGIC_V5_ADDR_TYPE_IRS to UAPI
   - 发件人: sashiko-bot@kernel.org
43. **[07-24 11:33]** Re: [PATCH v4 22/48] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: sashiko-bot@kernel.org
44. **[07-24 11:34]** Re: [PATCH v4 25/48] KVM: arm64: gic-v5: Add GIC VDPEND hyp call
   - 发件人: sashiko-bot@kernel.org
45. **[07-24 11:39]** Re: [PATCH v4 26/48] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: sashiko-bot@kernel.org
46. **[07-24 11:41]** Re: [PATCH v4 23/48] KVM: arm64: gic-v5: Set IRICHPPIDIS based on
 IRS enable state
   - 发件人: sashiko-bot@kernel.org
47. **[07-24 11:41]** Re: [PATCH v4 16/48] KVM: arm64: gic-v5: Request doorbells when
 VPEs enter WFI
   - 发件人: sashiko-bot@kernel.org
48. **[07-24 11:46]** Re: [PATCH v4 34/48] KVM: arm64: gic-v5: Add VGICv5 IST
 save/restore UAPI
   - 发件人: sashiko-bot@kernel.org
49. **[07-24 11:48]** Re: [PATCH v4 27/48] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: sashiko-bot@kernel.org
50. **[07-24 11:52]** Re: [PATCH v4 30/48] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: sashiko-bot@kernel.org
51. **[07-24 12:02]** Re: [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: sashiko-bot@kernel.org
52. **[07-24 12:02]** Re: [PATCH v4 41/48] KVM: selftests: Add VGICv5 NR_IRQS attribute
 tests
   - 发件人: sashiko-bot@kernel.org
53. **[07-24 12:05]** Re: [PATCH v4 32/48] KVM: arm64: gic-v5: Handle userspace accesses
 to IRS MMIO region
   - 发件人: sashiko-bot@kernel.org
54. **[07-24 12:06]** Re: [PATCH v4 42/48] KVM: selftests: Add VGICv5 IRS_REGS attribute
 tests
   - 发件人: sashiko-bot@kernel.org
55. **[07-24 12:09]** Re: [PATCH v4 31/48] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg
 userspace accessors
   - 发件人: sashiko-bot@kernel.org
56. **[07-24 12:15]** Re: [PATCH v4 46/48] KVM: selftests: Add VGICv5 SPI injection tests
   - 发件人: sashiko-bot@kernel.org
57. **[07-24 12:18]** Re: [PATCH v4 47/48] KVM: selftests: Add VGICv5 LPI delivery tests
   - 发件人: sashiko-bot@kernel.org
58. **[07-24 12:19]** Re: [PATCH v4 37/48] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: sashiko-bot@kernel.org
59. **[07-24 12:19]** Re: [PATCH v4 29/48] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: sashiko-bot@kernel.org
60. **[07-25 10:35]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Marc Zyngier <maz@kernel.org>
61. **[07-25 11:08]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Marc Zyngier <maz@kernel.org>
62. **[07-25 11:40]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from IRS config frame
   - 发件人: Marc Zyngier <maz@kernel.org>
63. **[07-25 11:56]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Marc Zyngier <maz@kernel.org>
64. **[07-27 17:39]** Re: [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: Fuad Tabba <tabba@google.com>
65. **[07-27 18:55]** Re: [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
66. **[07-27 19:34]** Re: [PATCH v4 20/48] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO emulation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
67. **[07-27 19:56]** Re: [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
68. **[07-27 20:26]** Re: [PATCH v4 38/48] Documentation: KVM: Add docs for KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
69. **[07-28 13:14]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI hosts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
70. **[07-30 16:06]** Re: [PATCH v4 20/48] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
71. **[07-31 07:18]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI
 hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
72. **[07-31 07:21]** Re: [PATCH v4 03/48] irqchip/gic-v5: Set up gic_kvm_info on ACPI
 hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
73. **[07-31 07:24]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from
 IRS config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
74. **[07-31 08:35]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
75. **[07-31 08:55]** Re: [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
76. **[07-31 09:11]** Re: [PATCH v4 10/48] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
77. **[07-31 09:19]** Re: [PATCH v4 38/48] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
78. **[07-31 09:20]** Re: [PATCH v4 01/48] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
79. **[07-31 09:29]** Re: [PATCH v4 02/48] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
80. **[07-31 09:32]** Re: [PATCH v4 06/48] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
81. **[07-31 09:33]** Re: [PATCH v4 08/48] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
82. **[07-31 09:35]** Re: [PATCH v4 07/48] KVM: arm64: gic-v5: Extract host IRS caps from
 IRS config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
83. **[07-31 10:17]** Re: [PATCH v4 14/48] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
84. **[07-31 10:20]** Re: [PATCH v4 16/48] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
85. **[07-31 10:22]** Re: [PATCH v4 19/48] KVM: arm64: gic-v5: Add
 KVM_VGIC_V5_ADDR_TYPE_IRS to UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
86. **[07-31 13:05]** Re: [PATCH v4 22/48] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
87. **[07-31 13:15]** Re: [PATCH v4 13/48] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
88. **[07-31 13:16]** Re: [PATCH v4 15/48] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
89. **[07-31 13:18]** Re: [PATCH v4 25/48] KVM: arm64: gic-v5: Add GIC VDPEND hyp call
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
90. **[07-31 13:32]** Re: [PATCH v4 23/48] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
91. **[07-31 13:37]** Re: [PATCH v4 26/48] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
92. **[07-31 13:49]** Re: [PATCH v4 27/48] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
93. **[07-31 14:13]** Re: [PATCH v4 29/48] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
94. **[07-31 14:21]** Re: [PATCH v4 30/48] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
95. **[07-31 14:27]** Re: [PATCH v4 31/48] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg
 userspace accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
96. **[07-31 14:35]** Re: [PATCH v4 34/48] KVM: arm64: gic-v5: Add VGICv5 IST save/restore
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
97. **[07-31 14:42]** Re: [PATCH v4 32/48] KVM: arm64: gic-v5: Handle userspace accesses to
 IRS MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
98. **[07-31 14:46]** Re: [PATCH v4 37/48] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
99. **[07-31 14:49]** Re: [PATCH v4 47/48] KVM: selftests: Add VGICv5 LPI delivery tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
100. **[07-31 14:54]** Re: [PATCH v4 46/48] KVM: selftests: Add VGICv5 SPI injection tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
101. **[07-31 15:52]** Re: [PATCH v4 42/48] KVM: selftests: Add VGICv5 IRS_REGS attribute
 tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
102. **[07-31 16:24]** Re: [PATCH v4 41/48] KVM: selftests: Add VGICv5 NR_IRQS attribute
 tests
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
103. **[07-31 16:43]** Re: [PATCH v4 35/48] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 2: [PATCH v5 00/31] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 67 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 31 Jul 2026 15:08:28 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:67, 88477 tokens)

#### 📝 邮件列表

1. **[07-31 15:08]** [PATCH v5 00/31] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[07-31 15:08]** [PATCH v5 01/31] vfio: Use file-based reference counting for KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[07-31 15:08]** [PATCH v5 02/31] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[07-31 15:08]** [PATCH v5 03/31] KVM: Allow KVM implementations to switch off MMIO independent of Kconfig
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[07-31 15:08]** [PATCH v5 04/31] arm64: Use proper include variant
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[07-31 15:08]** [PATCH v5 05/31] arm64: ptrace: Use constants for compat register numbers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[07-31 15:08]** [PATCH v5 06/31] arm64/sysreg: Convert SPSR_ELx to automatic register generation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[07-31 15:08]** [PATCH v5 07/31] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[07-31 15:08]** [PATCH v5 08/31] KVM: arm64: Use accessor functions for gprs during reset
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[07-31 15:08]** [PATCH v5 09/31] KVM: arm64: Refactor core-reset into a separate function
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[07-31 15:08]** [PATCH v5 10/31] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[07-31 15:08]** [PATCH v5 11/31] arm64: Share arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[07-31 15:08]** [PATCH v5 12/31] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[07-31 15:08]** [PATCH v5 13/31] KVM: s390: Prepare moving KVM/s390 to arch/s390/kvm/s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[07-31 15:08]** [PATCH v5 14/31] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[07-31 15:08]** [PATCH v5 15/31] KVM: s390: Guard KVM/s390 behind CONFIG_KVM_S390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[07-31 15:08]** [PATCH v5 16/31] KVM: s390: Move PGM code definitions to asm/kvm_host.h
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[07-31 15:08]** [PATCH v5 17/31] KVM: s390: Prepare gmap for a second KVM implementation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[07-31 15:08]** [PATCH v5 18/31] KVM: s390: gmap: Move storage key and CMMA code to kvm/s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[07-31 15:08]** [PATCH v5 19/31] KVM: s390: gmap: Move prefix handling to kvm/s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[07-31 15:08]** [PATCH v5 20/31] KVM: s390: Prepare KVM/s390 for a second KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[07-31 15:08]** [PATCH v5 21/31] s390: Use arm64 headers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[07-31 15:08]** [PATCH v5 22/31] KVM: s390: Use arm64 code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[07-31 15:08]** [PATCH v5 23/31] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[07-31 15:08]** [PATCH v5 24/31] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[07-31 15:08]** [PATCH v5 25/31] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[07-31 15:08]** [PATCH v5 26/31] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[07-31 15:08]** [PATCH v5 27/31] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[07-31 15:08]** [PATCH v5 28/31] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
30. **[07-31 15:08]** [PATCH v5 29/31] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
31. **[07-31 15:08]** [PATCH v5 30/31] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
32. **[07-31 15:08]** [PATCH v5 31/31] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
33. **[07-31 13:16]** Re: [PATCH v5 04/31] arm64: Use proper include variant
   - 发件人: sashiko-bot@kernel.org
34. **[07-31 13:21]** Re: [PATCH v5 05/31] arm64: ptrace: Use constants for compat
 register numbers
   - 发件人: sashiko-bot@kernel.org
35. **[07-31 13:26]** Re: [PATCH v5 02/31] KVM: Make device name configurable
   - 发件人: sashiko-bot@kernel.org
36. **[07-31 13:26]** Re: [PATCH v5 07/31] KVM: arm64: Access elements of vcpu_gp_regs
 individually
   - 发件人: sashiko-bot@kernel.org
37. **[07-31 13:27]** Re: [PATCH v5 01/31] vfio: Use file-based reference counting for
 KVM
   - 发件人: sashiko-bot@kernel.org
38. **[07-31 13:28]** Re: [PATCH v5 03/31] KVM: Allow KVM implementations to switch off
 MMIO independent of Kconfig
   - 发件人: sashiko-bot@kernel.org
39. **[07-31 13:30]** Re: [PATCH v5 06/31] arm64/sysreg: Convert SPSR_ELx to automatic
 register generation
   - 发件人: sashiko-bot@kernel.org
40. **[07-31 13:30]** Re: [PATCH v5 09/31] KVM: arm64: Refactor core-reset into a
 separate function
   - 发件人: sashiko-bot@kernel.org
41. **[07-31 13:31]** Re: [PATCH v5 10/31] arm64: Prepare sharing arm64 headers with s390
   - 发件人: sashiko-bot@kernel.org
42. **[07-31 13:36]** Re: [PATCH v5 08/31] KVM: arm64: Use accessor functions for gprs
 during reset
   - 发件人: sashiko-bot@kernel.org
43. **[07-31 13:37]** Re: [PATCH v5 13/31] KVM: s390: Prepare moving KVM/s390 to
 arch/s390/kvm/s390
   - 发件人: sashiko-bot@kernel.org
44. **[07-31 13:39]** Re: [PATCH v5 11/31] arm64: Share arm64 headers with s390
   - 发件人: sashiko-bot@kernel.org
45. **[07-31 13:42]** Re: [PATCH v5 16/31] KVM: s390: Move PGM code definitions to
 asm/kvm_host.h
   - 发件人: sashiko-bot@kernel.org
46. **[07-31 13:43]** Re: [PATCH v5 14/31] KVM: s390: Move s390 kvm code into a
 subdirectory
   - 发件人: sashiko-bot@kernel.org
47. **[07-31 13:43]** Re: [PATCH v5 12/31] KVM: arm64: Share arm64 code with s390
   - 发件人: sashiko-bot@kernel.org
48. **[07-31 13:47]** Re: [PATCH v5 17/31] KVM: s390: Prepare gmap for a second KVM
 implementation
   - 发件人: sashiko-bot@kernel.org
49. **[07-31 13:47]** Re: [PATCH v5 15/31] KVM: s390: Guard KVM/s390 behind
 CONFIG_KVM_S390
   - 发件人: sashiko-bot@kernel.org
50. **[07-31 13:50]** Re: [PATCH v5 19/31] KVM: s390: gmap: Move prefix handling to
 kvm/s390
   - 发件人: sashiko-bot@kernel.org
51. **[07-31 13:50]** Re: [PATCH v5 20/31] KVM: s390: Prepare KVM/s390 for a second KVM
 module
   - 发件人: sashiko-bot@kernel.org
52. **[07-31 13:52]** Re: [PATCH v5 22/31] KVM: s390: Use arm64 code
   - 发件人: sashiko-bot@kernel.org
53. **[07-31 13:54]** Re: [PATCH v5 21/31] s390: Use arm64 headers
   - 发件人: sashiko-bot@kernel.org
54. **[07-31 13:56]** Re: [PATCH v5 18/31] KVM: s390: gmap: Move storage key and CMMA
 code to kvm/s390
   - 发件人: sashiko-bot@kernel.org
55. **[07-31 13:57]** Re: [PATCH v5 25/31] s390/hwcaps: Report SAE support as hwcap
   - 发件人: sashiko-bot@kernel.org
56. **[07-31 14:03]** Re: [PATCH v5 23/31] s390: Introduce Start Arm Execution
 instruction
   - 发件人: sashiko-bot@kernel.org
57. **[07-31 14:06]** Re: [PATCH v5 26/31] KVM: s390: Add basic arm64 kvm module
   - 发件人: sashiko-bot@kernel.org
58. **[07-31 14:09]** Re: [PATCH v5 24/31] KVM: s390: arm64: Introduce host definitions
   - 发件人: sashiko-bot@kernel.org
59. **[07-31 14:17]** Re: [PATCH v5 30/31] KVM: s390: arm64: Implement basic page fault
 handler
   - 发件人: sashiko-bot@kernel.org
60. **[07-31 15:17]** Re: [PATCH v5 06/31] arm64/sysreg: Convert SPSR_ELx to automatic register generation
   - 发件人: Marc Zyngier <maz@kernel.org>
61. **[07-31 14:18]** Re: [PATCH v5 28/31] KVM: s390: arm64: Implement vm/vcpu create
 destroy.
   - 发件人: sashiko-bot@kernel.org
62. **[07-31 14:24]** Re: [PATCH v5 27/31] KVM: s390: arm64: Implement required functions
   - 发件人: sashiko-bot@kernel.org
63. **[07-31 14:25]** Re: [PATCH v5 31/31] KVM: s390: arm64: Enable KVM_ARM64 config and
 Kbuild
   - 发件人: sashiko-bot@kernel.org
64. **[07-31 14:42]** Re: [PATCH v5 29/31] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: sashiko-bot@kernel.org
65. **[07-31 16:50]** Re: [PATCH v5 06/31] arm64/sysreg: Convert SPSR_ELx to automatic
 register generation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
66. **[07-31 16:54]** Re: [PATCH v5 01/31] vfio: Use file-based reference counting for KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
67. **[07-31 09:15]** Re: [PATCH v5 01/31] vfio: Use file-based reference counting for KVM
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 3: [PATCH v9 00/16] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 45 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 20 Jul 2026 14:37:54 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:20 新:25, 6171 tokens)

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
18. **[07-20 06:01]** Re: [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3
 traps on all CPUs
   - 发件人: sashiko-bot@kernel.org
19. **[07-20 06:03]** Re: [PATCH v9 12/16] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: sashiko-bot@kernel.org
20. **[07-20 06:08]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: sashiko-bot@kernel.org
21. **[07-29 16:11]** Re: [PATCH v9 01/16] KVM: arm64: Serialize repeated vCPU initialization
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
22. **[07-29 16:16]** Re: [PATCH v9 02/16] KVM: arm64: PMU: Stop updating MDCR_EL2.HPMN
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
23. **[07-29 16:19]** Re: [PATCH v9 03/16] KVM: arm64: PMU: Freeze counter count after
 first run
   - 发件人: Fuad Tabba <tabba@google.com>
24. **[07-29 16:22]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Fuad Tabba <tabba@google.com>
25. **[07-29 16:23]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Fuad Tabba <tabba@google.com>
26. **[07-29 16:35]** Re: [PATCH v9 05/16] KVM: arm64: PMU: Keep implemented counter mask EL-independent
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
27. **[07-29 16:47]** Re: [PATCH v9 06/16] KVM: arm64: PMU: Recreate events after MDCR_EL2 changes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
28. **[07-29 17:03]** Re: [PATCH v9 07/16] tools headers: Use u* types for bitfield helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
29. **[07-29 17:23]** Re: [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
30. **[07-29 17:24]** Re: [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
31. **[07-29 17:33]** Re: [PATCH v9 10/16] KVM: arm64: Don't clear vcpu->cpu in kvm_arch_vcpu_put()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
32. **[07-29 17:39]** Re: [PATCH v9 11/16] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
33. **[07-29 18:44]** Re: [PATCH v9 12/16] KVM: arm64: PMU: Pass the pPMU to kvm_map_pmu_event()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[07-29 18:45]** Re: [PATCH v9 12/16] KVM: arm64: PMU: Pass the pPMU to kvm_map_pmu_event()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
35. **[07-29 18:46]** Re: [PATCH v9 08/16] KVM: arm64: selftests: Cover PMU state in MDCR_EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
36. **[07-29 18:58]** Re: [PATCH v9 13/16] KVM: arm64: PMU: Pass the target CPU to kvm_pmu_probe_armpmu()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
37. **[07-29 19:18]** Re: [PATCH v9 14/16] KVM: arm64: PMU: Implement fixed-counters-only emulation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[07-29 20:14]** Re: [PATCH v9 15/16] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
39. **[07-29 20:45]** Re: [PATCH v9 16/16] KVM: arm64: selftests: Test PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
40. **[07-30 14:44]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
41. **[07-30 15:12]** Re: [PATCH v9 09/16] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
42. **[07-30 07:29]** Re: [PATCH v9 00/16] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
43. **[07-30 15:36]** Re: [PATCH v9 14/16] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
44. **[07-30 07:52]** Re: [PATCH v9 14/16] KVM: arm64: PMU: Implement fixed-counters-only emulation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
45. **[07-30 08:15]** Re: [PATCH v9 04/16] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 4: [PATCH v4 00/29] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3

**📧 邮件数**: 44 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 30 Jul 2026 08:09:53 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:44, 20921 tokens)

#### 📝 邮件列表

1. **[07-30 08:09]** [PATCH v4 00/29] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-30 08:09]** [PATCH v4 01/29] arm64: sysreg: Emit RESx/UNKN values for Mapping/Fields definitions
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-30 08:09]** [PATCH v4 02/29] arm64: Update ID_AA64MMFR4_EL1 description to 2026-03 JSON release
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-30 08:09]** [PATCH v4 03/29] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-30 08:09]** [PATCH v4 04/29] KVM: arm64: Drop __HCRX_EL2_* masks
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-30 08:09]** [PATCH v4 05/29] KVM: arm64: Plumb HCRX_EL2.SRMASKEn in HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-30 08:09]** [PATCH v4 06/29] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL register
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-30 08:10]** [PATCH v4 07/29] KVM: arm64: Don't evaluate HCR_EL2.NV nor HFGITR_EL2.ERET on ERET fast path
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-30 08:10]** [PATCH v4 08/29] arm64: Add ARM64_HAS_NV2P1 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-30 08:10]** [PATCH v4 09/29] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-30 08:10]** [PATCH v4 10/29] KVM: arm64: Relax CNTHCTL_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[07-30 08:10]** [PATCH v4 11/29] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-30 08:10]** [PATCH v4 12/29] arm64: Add FEAT_NV2p1 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[07-30 08:10]** [PATCH v4 13/29] arm64: sysreg: Add NVHCR_EL2 description as a mirror of HCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[07-30 08:10]** [PATCH v4 14/29] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[07-30 08:10]** [PATCH v4 15/29] arm64: Add ARM64_HAS_NV3 capability
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-30 08:10]** [PATCH v4 16/29] KVM: arm64: Split NV-specific exit fixups from the non-NV handling
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[07-30 08:10]** [PATCH v4 17/29] KVM: arm64: Add NV3 control bits to HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[07-30 08:10]** [PATCH v4 18/29] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[07-30 08:10]** [PATCH v4 19/29] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[07-30 08:10]** [PATCH v4 20/29] KVM: arm64: Add sanitisation for NVHCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[07-30 08:10]** [PATCH v4 21/29] KVM: arm64: Add NVHCR_EL2 handling to the sysreg array
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[07-30 08:10]** [PATCH v4 22/29] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[07-30 08:10]** [PATCH v4 23/29] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[07-30 08:10]** [PATCH v4 24/29] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[07-30 08:10]** [PATCH v4 25/29] KVM: arm64: Engage NV3 TLBI trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[07-30 08:10]** [PATCH v4 26/29] KVM: arm64: Add FEAT_NV3 detection
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[07-30 08:10]** [PATCH v4 27/29] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[07-30 08:10]** [PATCH v4 28/29] KVM: arm64: selftest: Add NVHCR_EL2 to get-reg-list
   - 发件人: Marc Zyngier <maz@kernel.org>
30. **[07-30 08:10]** [PATCH v4 29/29] arm64: Add override for ID_AA64MMFR4_EL1.NV_frac
   - 发件人: Marc Zyngier <maz@kernel.org>
31. **[07-30 07:29]** Re: [PATCH v4 03/29] KVM: arm64: Merge guest's HCRX_EL2 using
 NV_HCRX_GUEST_EXCLUDE
   - 发件人: sashiko-bot@kernel.org
32. **[07-30 07:40]** Re: [PATCH v4 14/29] arm64: sysreg: Add HCRX_EL2 bits related to
 FEAT_NV3
   - 发件人: sashiko-bot@kernel.org
33. **[07-30 08:48]** Re: [PATCH v4 14/29] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
34. **[07-30 07:56]** Re: [PATCH v4 09/29] KVM: arm64: Relax CPTR_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: sashiko-bot@kernel.org
35. **[07-30 07:58]** Re: [PATCH v4 21/29] KVM: arm64: Add NVHCR_EL2 handling to the
 sysreg array
   - 发件人: sashiko-bot@kernel.org
36. **[07-30 09:01]** Re: [PATCH v4 03/29] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
37. **[07-30 08:05]** Re: [PATCH v4 23/29] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: sashiko-bot@kernel.org
38. **[07-30 08:09]** Re: [PATCH v4 11/29] KVM: arm64: Expose FEAT_NV2p1 to NV guests
   - 发件人: sashiko-bot@kernel.org
39. **[07-30 08:12]** Re: [PATCH v4 22/29] KVM: arm64: Add routing for NVHCR_EL2 trap
   - 发件人: sashiko-bot@kernel.org
40. **[07-30 10:42]** Re: [PATCH v4 03/29] KVM: arm64: Merge guest's HCRX_EL2 using
 NV_HCRX_GUEST_EXCLUDE
   - 发件人: Joey Gouly <joey.gouly@arm.com>
41. **[07-30 10:48]** Re: [PATCH v4 02/29] arm64: Update ID_AA64MMFR4_EL1 description to
 2026-03 JSON release
   - 发件人: Joey Gouly <joey.gouly@arm.com>
42. **[07-30 11:23]** Re: [PATCH v4 01/29] arm64: sysreg: Emit RESx/UNKN values for
 Mapping/Fields definitions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
43. **[07-30 14:39]** Re: [PATCH v4 03/29] KVM: arm64: Merge guest's HCRX_EL2 using NV_HCRX_GUEST_EXCLUDE
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[07-31 11:51]** Re: [PATCH v4 00/29] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 5: [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support

**📧 邮件数**: 28 | **👥 参与者**: 5 | **📅 开始时间**: Wed, 15 Jul 2026 15:27:31 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:6 新:22, 11051 tokens)

#### 📝 邮件列表

1. **[07-15 15:27]** [PATCH 0/6] firmware: arm_rmm: Add RMM v2.0 support
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:27]** [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling the RMM
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-15 15:27]** [PATCH 3/6] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
4. **[07-15 15:27]** [PATCH 4/6] firmware: arm_rmm: Configure the RMM with the host's page size
   - 发件人: Steven Price <steven.price@arm.com>
5. **[07-15 15:27]** [PATCH 5/6] firmware: arm_rmm: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
6. **[07-23 16:11]** Re: [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling
 the RMM
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
7. **[07-29 17:02]** Re: [PATCH 1/6] firmware: arm_rmm: Add SMC definitions for calling
 the RMM
   - 发件人: Steven Price <steven.price@arm.com>
8. **[07-31 11:46]** Re: [PATCH 3/6] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[07-31 14:21]** Re: [PATCH 4/6] firmware: arm_rmm: Configure the RMM with the host's
 page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[07-31 19:25]** Re: [PATCH 5/6] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[08-01 13:48]** [PATCH 0/6] KVM: arm64: VNCR TLB invalidation fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[08-01 13:48]** [PATCH 1/6] KVM: arm64: Remove VM-wide VNCR mapping counter
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[08-01 13:48]** [PATCH 2/6] KVM: arm64: Handle negative S1 walk levels in VNCR TLB size evaluation
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[08-01 13:48]** [PATCH 3/6] KVM: arm64: Consider SCTLR_EL2.M when mapping the L1 VNCR page
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[08-01 13:48]** [PATCH 4/6] KVM: arm64: Correctly handle end of VA space TLBI invalidation
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[08-01 13:48]** [PATCH 5/6] KVM: arm64: Couple VNCR fixmap clearing and CPU number invalidation
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[08-01 13:48]** [PATCH 6/6] KVM: arm64: Add VNCR TLB tracking again
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[08-01 13:02]** Re: [PATCH 2/6] KVM: arm64: Handle negative S1 walk levels in VNCR
 TLB size evaluation
   - 发件人: sashiko-bot@kernel.org
19. **[08-01 13:02]** Re: [PATCH 5/6] KVM: arm64: Couple VNCR fixmap clearing and CPU
 number invalidation
   - 发件人: sashiko-bot@kernel.org
20. **[08-01 13:03]** Re: [PATCH 4/6] KVM: arm64: Correctly handle end of VA space TLBI
 invalidation
   - 发件人: sashiko-bot@kernel.org
21. **[08-01 13:04]** Re: [PATCH 6/6] KVM: arm64: Add VNCR TLB tracking again
   - 发件人: sashiko-bot@kernel.org
22. **[08-01 13:08]** Re: [PATCH 1/6] KVM: arm64: Remove VM-wide VNCR mapping counter
   - 发件人: sashiko-bot@kernel.org
23. **[08-01 13:10]** Re: [PATCH 3/6] KVM: arm64: Consider SCTLR_EL2.M when mapping the
 L1 VNCR page
   - 发件人: sashiko-bot@kernel.org
24. **[08-01 14:19]** Re: [PATCH 1/6] KVM: arm64: Remove VM-wide VNCR mapping counter
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[08-01 14:20]** Re: [PATCH 2/6] KVM: arm64: Handle negative S1 walk levels in VNCR TLB size evaluation
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[08-01 14:40]** Re: [PATCH 4/6] KVM: arm64: Correctly handle end of VA space TLBI invalidation
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[08-01 15:51]** Re: [PATCH 5/6] KVM: arm64: Couple VNCR fixmap clearing and CPU number invalidation
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[08-01 18:01]** Re: [PATCH 6/6] KVM: arm64: Add VNCR TLB tracking again
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 6: [PATCH v4 00/11] liveupdate: kvm: Guest_memfd preservation

**📧 邮件数**: 26 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 28 Jul 2026 12:11:27 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:26, 25029 tokens)

#### 📝 邮件列表

1. **[07-28 12:11]** [PATCH v4 00/11] liveupdate: kvm: Guest_memfd preservation
   - 发件人: Tarun Sahu <tarunsahu@google.com>
2. **[07-28 12:11]** [PATCH v4 01/11] liveupdate: Add LIVEUPDATE_GUEST_MEMFD config option
   - 发件人: Tarun Sahu <tarunsahu@google.com>
3. **[07-28 12:11]** [PATCH v4 02/11] KVM: Introduce kvm_create_vm_file() helper
   - 发件人: Tarun Sahu <tarunsahu@google.com>
4. **[07-28 12:11]** [PATCH v4 03/11] KVM: Export kvm_uevent_notify_vm_create()
   - 发件人: Tarun Sahu <tarunsahu@google.com>
5. **[07-28 12:11]** [PATCH v4 04/11] KVM: Track weak reference to vm_file in struct kvm
   - 发件人: Tarun Sahu <tarunsahu@google.com>
6. **[07-28 12:11]** [PATCH v4 05/11] KVM: LUO: Support VM preservation across live updates
   - 发件人: Tarun Sahu <tarunsahu@google.com>
7. **[07-28 12:11]** [PATCH v4 06/11] KVM: guest_memfd: Move internal definitions to
 internal header
   - 发件人: Tarun Sahu <tarunsahu@google.com>
8. **[07-28 12:11]** [PATCH v4 07/11] KVM: guest_memfd: Add support for freezing mappings
   - 发件人: Tarun Sahu <tarunsahu@google.com>
9. **[07-28 12:11]** [PATCH v4 08/11] KVM: guest_memfd: Add support for preservation via LUO
   - 发件人: Tarun Sahu <tarunsahu@google.com>
10. **[07-28 12:11]** [PATCH v4 09/11] docs: liveupdate: Add documentation for VM and
 guest_memfd preservation
   - 发件人: Tarun Sahu <tarunsahu@google.com>
11. **[07-28 12:11]** [PATCH v4 10/11] KVM: selftests: Split ____vm_create() and add vm_create_from_fd()
   - 发件人: Tarun Sahu <tarunsahu@google.com>
12. **[07-28 12:11]** [PATCH v4 11/11] KVM: selftests: Add guest_memfd_preservation_test
   - 发件人: Tarun Sahu <tarunsahu@google.com>
13. **[07-28 12:20]** Re: [PATCH v4 07/11] KVM: guest_memfd: Add support for freezing
 mappings
   - 发件人: sashiko-bot@kernel.org
14. **[07-28 12:21]** Re: [PATCH v4 09/11] docs: liveupdate: Add documentation for VM and
 guest_memfd preservation
   - 发件人: sashiko-bot@kernel.org
15. **[07-28 12:22]** Re: [PATCH v4 01/11] liveupdate: Add LIVEUPDATE_GUEST_MEMFD config
 option
   - 发件人: sashiko-bot@kernel.org
16. **[07-28 12:23]** Re: [PATCH v4 08/11] KVM: guest_memfd: Add support for preservation
 via LUO
   - 发件人: sashiko-bot@kernel.org
17. **[07-28 12:26]** Re: [PATCH v4 03/11] KVM: Export kvm_uevent_notify_vm_create()
   - 发件人: sashiko-bot@kernel.org
18. **[07-28 12:27]** Re: [PATCH v4 05/11] KVM: LUO: Support VM preservation across live
 updates
   - 发件人: sashiko-bot@kernel.org
19. **[07-30 10:36]** Re: [PATCH v4 02/11] KVM: Introduce kvm_create_vm_file() helper
   - 发件人: Ackerley Tng <ackerleytng@google.com>
20. **[07-30 10:43]** Re: [PATCH v4 03/11] KVM: Export kvm_uevent_notify_vm_create()
   - 发件人: Ackerley Tng <ackerleytng@google.com>
21. **[07-30 10:46]** Re: [PATCH v4 07/11] KVM: guest_memfd: Add support for freezing mappings
   - 发件人: Ackerley Tng <ackerleytng@google.com>
22. **[07-30 11:06]** Re: [PATCH v4 01/11] liveupdate: Add LIVEUPDATE_GUEST_MEMFD config option
   - 发件人: Ackerley Tng <ackerleytng@google.com>
23. **[07-30 11:12]** Re: [PATCH v4 07/11] KVM: guest_memfd: Add support for freezing mappings
   - 发件人: Ackerley Tng <ackerleytng@google.com>
24. **[07-30 11:12]** Re: [PATCH v4 06/11] KVM: guest_memfd: Move internal definitions to
 internal header
   - 发件人: Ackerley Tng <ackerleytng@google.com>
25. **[07-30 11:16]** Re: [PATCH v4 08/11] KVM: guest_memfd: Add support for preservation
 via LUO
   - 发件人: Ackerley Tng <ackerleytng@google.com>
26. **[07-30 11:18]** Re: [PATCH v4 11/11] KVM: selftests: Add guest_memfd_preservation_test
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

### Thread 7: [PATCH v4 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 24 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 31 Jul 2026 15:35:24 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:24, 29960 tokens)

#### 📝 邮件列表

1. **[07-31 15:35]** [PATCH v4 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-31 15:35]** [PATCH v4 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-31 15:35]** [PATCH v4 02/17] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-31 15:35]** [PATCH v4 03/17] KVM: arm64: Add pkvm_map_private_va_range
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-31 15:35]** [PATCH v4 04/17] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-31 15:35]** [PATCH v4 05/17] KVM: arm64: Allow kvm_hyp_memcache usage outside of stage-2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[07-31 15:35]** [PATCH v4 06/17] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-31 15:35]** [PATCH v4 07/17] KVM: arm64: Add PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[07-31 15:35]** [PATCH v4 08/17] KVM: arm64: Add reclaim interface for the pKVM heap alloc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[07-31 15:35]** [PATCH v4 09/17] KVM: arm64: Add selftests for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[07-31 15:35]** [PATCH v4 10/17] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[07-31 15:35]** [PATCH v4 11/17] KVM: arm64: Filter out non-kernel addresses in kern_hyp_va
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[07-31 15:35]** [PATCH v4 12/17] KVM: arm64: Move hyp_vm refcount into the structure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[07-31 15:35]** [PATCH v4 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[07-31 15:35]** [PATCH v4 14/17] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[07-31 15:35]** [PATCH v4 15/17] KVM: arm64: Reject hyp trace descriptors with fewer
 CPUs than hyp_nr_cpus
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[07-31 15:35]** [PATCH v4 16/17] KVM: arm64: Reject hyp trace descriptors with fewer
 than 3 pages
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[07-31 15:35]** [PATCH v4 17/17] KVM: arm64: Alloc simple_buffer_page using pKVM hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[07-31 14:45]** Re: [PATCH v4 06/17] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: sashiko-bot@kernel.org
20. **[07-31 14:51]** Re: [PATCH v4 05/17] KVM: arm64: Allow kvm_hyp_memcache usage
 outside of stage-2
   - 发件人: sashiko-bot@kernel.org
21. **[07-31 14:52]** Re: [PATCH v4 07/17] KVM: arm64: Add PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: sashiko-bot@kernel.org
22. **[07-31 15:03]** Re: [PATCH v4 09/17] KVM: arm64: Add selftests for the pKVM heap
 allocator
   - 发件人: sashiko-bot@kernel.org
23. **[07-31 15:04]** Re: [PATCH v4 14/17] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM
 heap allocator
   - 发件人: sashiko-bot@kernel.org
24. **[07-31 15:06]** Re: [PATCH v4 13/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap
 allocator
   - 发件人: sashiko-bot@kernel.org

---

### Thread 8: [PATCH v17 00/14] KVM: arm64: Provide guest support for GCS

**📧 邮件数**: 22 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 31 Jul 2026 13:25:38 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:22, 18307 tokens)

#### 📝 邮件列表

1. **[07-31 13:25]** [PATCH v17 00/14] KVM: arm64: Provide guest support for GCS
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-31 13:25]** [PATCH v17 01/14] arm64/gcs: Ensure FGTs for EL1 GCS instructions
 are disabled
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-31 13:25]** [PATCH v17 02/14] KVM: arm64: Fix FGT mapping for
 HFGITR_EL2.nGCSEPP
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-31 13:25]** [PATCH v17 03/14] KVM: arm64: Manage GCS access and registers for
 guests
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-31 13:25]** [PATCH v17 04/14] KVM: arm64: Ensure GCS memory effects are
 visible
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-31 13:25]** [PATCH v17 05/14] KVM: arm64: Set PSTATE.EXLOCK when entering an
 exception
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[07-31 13:25]** [PATCH v17 06/14] KVM: arm64: Validate GCS exception lock when
 emulating ERET
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[07-31 13:25]** [PATCH v17 07/14] KVM: arm64: Forward GCS exceptions to nested
 guests
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[07-31 13:25]** [PATCH v17 08/14] KVM: arm64: Enforce EXLOCK for SPSR and ELR
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-31 13:25]** [PATCH v17 09/14] KVM: arm64: Allow GCS to be enabled for guests
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[07-31 13:25]** [PATCH v17 10/14] KVM: selftests: arm64: Add GCS registers to
 get-reg-list
   - 发件人: Mark Brown <broonie@kernel.org>
12. **[07-31 13:25]** [PATCH v17 11/14] KVM: selftests: arm64: Add GCS to set_id_regs
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[07-31 13:25]** [PATCH v17 12/14] KVM: selftests: arm64: Only restore SPSR_EL1 and
 ELR_EL1 if they change
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[07-31 13:25]** [PATCH v17 13/14] tools: Synchronise the kernel esr.h
   - 发件人: Mark Brown <broonie@kernel.org>
15. **[07-31 13:25]** [PATCH v17 14/14] KVM: selftests: arm64: Add GCS EXLOCK exception
 emulation test
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[07-31 12:56]** Re: [PATCH v17 03/14] KVM: arm64: Manage GCS access and registers
 for guests
   - 发件人: sashiko-bot@kernel.org
17. **[07-31 12:58]** Re: [PATCH v17 07/14] KVM: arm64: Forward GCS exceptions to nested
 guests
   - 发件人: sashiko-bot@kernel.org
18. **[07-31 13:03]** Re: [PATCH v17 02/14] KVM: arm64: Fix FGT mapping for
 HFGITR_EL2.nGCSEPP
   - 发件人: sashiko-bot@kernel.org
19. **[07-31 13:03]** Re: [PATCH v17 10/14] KVM: selftests: arm64: Add GCS registers to
 get-reg-list
   - 发件人: sashiko-bot@kernel.org
20. **[07-31 14:31]** Re: [PATCH v17 10/14] KVM: selftests: arm64: Add GCS registers to
 get-reg-list
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[07-31 14:47]** Re: [PATCH v17 02/14] KVM: arm64: Fix FGT mapping for
 HFGITR_EL2.nGCSEPP
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[07-31 16:26]** Re: [PATCH v17 03/14] KVM: arm64: Manage GCS access and registers
 for guests
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 9: [PATCH v3 00/11] KVM Dirty-bit cleaning hw accelerator (HACDBS)

**📧 邮件数**: 21 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 29 Jul 2026 11:45:35 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:21, 18757 tokens)

#### 📝 邮件列表

1. **[07-29 11:45]** [PATCH v3 00/11] KVM Dirty-bit cleaning hw accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[07-29 11:45]** [PATCH v3 01/11] KVM: arm64: HDBSS bits
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[07-29 11:45]** [PATCH v3 02/11] arm64/cpufeature: Add system-wide FEAT_HACDBS detection
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[07-29 11:45]** [PATCH v3 03/11] arm64/sysreg: Add HACDBS consumer and base registers
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[07-29 11:45]** [PATCH v3 04/11] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[07-29 11:45]** [PATCH v3 05/11] kvm: Add arch-generic interface for hw-accelerated dirty-bitmap cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-29 11:45]** [PATCH v3 06/11] KVM: arm64: Add hardware-accelerated dirty-bitmap cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[07-29 11:45]** [PATCH v3 07/11] KVM: arm64: Dirty-bitmap: avoid splitting previously split blocks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[07-29 11:45]** [PATCH v3 08/11] kvm/dirty_ring: Introduce get_memslot and move helpers to header
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[07-29 11:45]** [PATCH v3 09/11] kvm/dirty_ring: Add arch-generic interface for hw-accelerated dirty-ring cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-29 11:45]** [PATCH v3 10/11] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[07-29 11:45]** [PATCH v3 11/11] KVM: arm64: Enable KVM_HW_DIRTY_BIT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[07-29 10:55]** Re: [PATCH v3 01/11] KVM: arm64: HDBSS bits
   - 发件人: sashiko-bot@kernel.org
14. **[07-29 10:57]** Re: [PATCH v3 04/11] KVM: arm64: dirty_bit: Add base FEAT_HACDBS
 cleaning routine
   - 发件人: sashiko-bot@kernel.org
15. **[07-29 11:00]** Re: [PATCH v3 05/11] kvm: Add arch-generic interface for
 hw-accelerated dirty-bitmap cleaning
   - 发件人: sashiko-bot@kernel.org
16. **[07-29 11:02]** Re: [PATCH v3 02/11] arm64/cpufeature: Add system-wide FEAT_HACDBS
 detection
   - 发件人: sashiko-bot@kernel.org
17. **[07-29 11:08]** Re: [PATCH v3 07/11] KVM: arm64: Dirty-bitmap: avoid splitting
 previously split blocks
   - 发件人: sashiko-bot@kernel.org
18. **[07-29 11:14]** Re: [PATCH v3 09/11] kvm/dirty_ring: Add arch-generic interface for
 hw-accelerated dirty-ring cleaning
   - 发件人: sashiko-bot@kernel.org
19. **[07-29 11:18]** Re: [PATCH v3 06/11] KVM: arm64: Add hardware-accelerated
 dirty-bitmap cleaning routine
   - 发件人: sashiko-bot@kernel.org
20. **[07-29 11:21]** Re: [PATCH v3 10/11] KVM: arm64: Add hardware-accelerated
 dirty-ring cleaning routine
   - 发件人: sashiko-bot@kernel.org
21. **[07-29 11:29]** Re: [PATCH v3 11/11] KVM: arm64: Enable KVM_HW_DIRTY_BIT
   - 发件人: sashiko-bot@kernel.org

---

### Thread 10: [PATCH v3 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test

**📧 邮件数**: 20 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 31 Jul 2026 12:56:00 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:20, 22156 tokens)

#### 📝 邮件列表

1. **[07-31 12:56]** [PATCH v3 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[07-31 12:56]** [PATCH v3 01/12] KVM: selftests: Add a KVM syscall wrapper for sched_setaffinity()
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[07-31 12:56]** [PATCH v3 02/12] KVM: selftests: Set threads CPU affinity before
 doing work in hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[07-31 12:56]** [PATCH v3 03/12] KVM: selftests: Pre-set threads affinity in hardware
 disable test when possible
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[07-31 12:56]** [PATCH v3 04/12] KVM: selftests: Return the target CPU from pin_task_to_random_cpu()
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[07-31 12:56]** [PATCH v3 05/12] KVM: selftests: Extract picking of random CPU from
 cpu_set_t to separate API
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[07-31 12:56]** [PATCH v3 06/12] KVM: selftests: Affine threads to random CPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[07-31 12:56]** [PATCH v3 07/12] KVM: selftests: Drop unreachable, dead code from
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[07-31 12:56]** [PATCH v3 08/12] KVM: selftests: Add KVM syscall wrapper for pthread_create()
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[07-31 12:56]** [PATCH v3 09/12] KVM: selftests: Add KVM syscall wrappers for pthread_{cancel,join}()
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[07-31 12:56]** [PATCH v3 10/12] KVM: selftests: Add helper APIs to cancel+join pthreads
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[07-31 12:56]** [PATCH v3 11/12] KVM: selftests: Add KVM syscall wrappers for pthread_{g,s}etaffinity_np()
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[07-31 12:56]** [PATCH v3 12/12] KVM: selftests: Clean up global constants in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
14. **[07-31 20:05]** Re: [PATCH v3 08/12] KVM: selftests: Add KVM syscall wrapper for
 pthread_create()
   - 发件人: sashiko-bot@kernel.org
15. **[07-31 20:11]** Re: [PATCH v3 09/12] KVM: selftests: Add KVM syscall wrappers for
 pthread_{cancel,join}()
   - 发件人: sashiko-bot@kernel.org
16. **[07-31 20:11]** Re: [PATCH v3 03/12] KVM: selftests: Pre-set threads affinity in
 hardware disable test when possible
   - 发件人: sashiko-bot@kernel.org
17. **[07-31 13:50]** Re: [PATCH v3 03/12] KVM: selftests: Pre-set threads affinity in
 hardware disable test when possible
   - 发件人: Sean Christopherson <seanjc@google.com>
18. **[07-31 14:35]** Re: [PATCH v3 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Yosry Ahmed <yosry@kernel.org>
19. **[07-31 14:41]** Re: [PATCH v3 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Sean Christopherson <seanjc@google.com>
20. **[07-31 14:43]** Re: [PATCH v3 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Yosry Ahmed <yosry@kernel.org>

---

### Thread 11: [PATCH v7 0/8] KVM: arm64: pKVM vCPU state management at EL2

**📧 邮件数**: 20 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 29 Jul 2026 14:18:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:20, 12911 tokens)

#### 📝 邮件列表

1. **[07-29 14:18]** [PATCH v7 0/8] KVM: arm64: pKVM vCPU state management at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-29 14:18]** [PATCH v7 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-29 14:18]** [PATCH v7 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-29 14:18]** [PATCH v7 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-29 14:18]** [PATCH v7 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-29 14:18]** [PATCH v7 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-29 14:18]** [PATCH v7 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-29 14:18]** [PATCH v7 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-29 14:18]** [PATCH v7 8/8] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[07-29 13:31]** Re: [PATCH v7 4/8] KVM: arm64: Move PSCI helper functions to a
 shared header
   - 发件人: sashiko-bot@kernel.org
11. **[07-29 14:33]** Re: [PATCH v7 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[07-29 13:34]** Re: [PATCH v7 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: sashiko-bot@kernel.org
13. **[07-29 13:36]** Re: [PATCH v7 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
14. **[07-29 13:39]** Re: [PATCH v7 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
15. **[07-29 14:40]** Re: [PATCH v7 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
16. **[07-29 14:44]** Re: [PATCH v7 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[07-29 14:46]** Re: [PATCH v7 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[07-29 14:52]** Re: [PATCH v7 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Joey Gouly <joey.gouly@arm.com>
19. **[07-29 15:51]** Re: [PATCH v7 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[07-31 11:51]** Re: [PATCH v7 0/8] KVM: arm64: pKVM vCPU state management at EL2
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 12: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush

**📧 邮件数**: 20 | **👥 参与者**: 6 | **📅 开始时间**: Mon, 13 Jul 2026 15:06:10 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:14 新:6, 3822 tokens)

#### 📝 邮件列表

1. **[07-13 15:06]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[07-14 15:38]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[07-14 11:50]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[07-14 12:59]** [PATCH v4 0/6] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[07-14 21:27]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
6. **[07-14 15:19]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-16 00:39]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[07-17 11:58]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
9. **[07-17 14:51]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
10. **[07-17 16:21]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-17 16:44]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[07-20 13:58]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[07-21 16:53]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Inochi Amaoto <inochiama@gmail.com>
14. **[07-21 15:18]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>
15. **[07-28 07:24]** Re: [PATCH v4 0/6] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
16. **[07-28 15:52]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
17. **[07-28 16:49]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
18. **[07-29 16:51]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
19. **[07-29 16:16]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Leonardo Bras <leo.bras@arm.com>
20. **[07-29 16:30]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 13: [PATCH v2 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test

**📧 邮件数**: 18 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 31 Jul 2026 10:06:07 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:18, 21702 tokens)

#### 📝 邮件列表

1. **[07-31 10:06]** [PATCH v2 00/12] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[07-31 10:06]** [PATCH v2 01/12] KVM: selftests: Add a KVM syscall wrapper for sched_setaffinity()
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[07-31 10:06]** [PATCH v2 02/12] KVM: selftests: Set threads CPU affinity before
 doing work in hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[07-31 10:06]** [PATCH v2 03/12] KVM: selftests: Pre-set threads affinity in hardware
 disable test when possible
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[07-31 10:06]** [PATCH v2 04/12] KVM: selftests: Return the target CPU from pin_task_to_random_cpu()
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[07-31 10:06]** [PATCH v2 05/12] KVM: selftests: Extract picking of random CPU from
 cpu_set_t to separate API
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[07-31 10:06]** [PATCH v2 06/12] KVM: selftests: Affine threads to random CPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[07-31 10:06]** [PATCH v2 07/12] KVM: selftests: Drop unreachable, dead code from
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[07-31 10:06]** [PATCH v2 08/12] KVM: selftests: Add KVM syscall wrapper for pthread_create()
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[07-31 10:06]** [PATCH v2 09/12] KVM: selftests: Add KVM syscall wrappers for pthread_{cancel,join}()
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[07-31 10:06]** [PATCH v2 10/12] KVM: selftests: Add helper APIs to cancel+join pthreads
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[07-31 10:06]** [PATCH v2 11/12] KVM: selftests: Add KVM syscall wrappers for pthread_{g,s}etaffinity_np()
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[07-31 10:06]** [PATCH v2 12/12] KVM: selftests: Clean up global constants in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
14. **[07-31 17:15]** Re: [PATCH v2 06/12] KVM: selftests: Affine threads to random CPUs
 in hardware disable test
   - 发件人: sashiko-bot@kernel.org
15. **[07-31 17:18]** Re: [PATCH v2 09/12] KVM: selftests: Add KVM syscall wrappers for
 pthread_{cancel,join}()
   - 发件人: sashiko-bot@kernel.org
16. **[07-31 17:20]** Re: [PATCH v2 08/12] KVM: selftests: Add KVM syscall wrapper for
 pthread_create()
   - 发件人: sashiko-bot@kernel.org
17. **[07-31 17:20]** Re: [PATCH v2 03/12] KVM: selftests: Pre-set threads affinity in
 hardware disable test when possible
   - 发件人: sashiko-bot@kernel.org
18. **[07-31 10:27]** Re: [PATCH v2 06/12] KVM: selftests: Affine threads to random CPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 14: [PATCH 0/9] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test

**📧 邮件数**: 18 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 30 Jul 2026 12:18:59 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:18, 20731 tokens)

#### 📝 邮件列表

1. **[07-30 12:18]** [PATCH 0/9] KVM: selftests: Add more syscall wrappers, fix hardware_disable_test
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[07-30 12:19]** [PATCH 1/9] KVM: selftests: Return the target CPU from pin_task_to_random_cpu()
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[07-30 12:19]** [PATCH 2/9] KVM: selftests: Extract picking of random CPU from
 cpu_set_t to separate API
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[07-30 12:19]** [PATCH 3/9] KVM: selftests: Affine child tasks to other pCPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[07-30 12:19]** [PATCH 4/9] KVM: selftests: Drop unreachable, dead code from hardware
 disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[07-30 12:19]** [PATCH 5/9] KVM: selftests: Add KVM syscall wrapper for pthread_create()
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[07-30 12:19]** [PATCH 6/9] KVM: selftests: Add KVM syscall wrappers for pthread_{cancel,join}()
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[07-30 12:19]** [PATCH 7/9] KVM: selftests: Add helper APIs to cancel+join pthreads
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[07-30 12:19]** [PATCH 8/9] KVM: selftests: Add KVM syscall wrappers for pthread_{g,s}etaffinity_np()
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[07-30 12:19]** [PATCH 9/9] KVM: selftests: Clean up global constants in hardware
 disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[07-30 19:29]** Re: [PATCH 8/9] KVM: selftests: Add KVM syscall wrappers for
 pthread_{g,s}etaffinity_np()
   - 发件人: sashiko-bot@kernel.org
12. **[07-30 19:30]** Re: [PATCH 4/9] KVM: selftests: Drop unreachable, dead code from
 hardware disable test
   - 发件人: sashiko-bot@kernel.org
13. **[07-30 19:30]** Re: [PATCH 5/9] KVM: selftests: Add KVM syscall wrapper for
 pthread_create()
   - 发件人: sashiko-bot@kernel.org
14. **[07-30 19:33]** Re: [PATCH 3/9] KVM: selftests: Affine child tasks to other pCPUs
 in hardware disable test
   - 发件人: sashiko-bot@kernel.org
15. **[07-30 13:24]** Re: [PATCH 8/9] KVM: selftests: Add KVM syscall wrappers for pthread_{g,s}etaffinity_np()
   - 发件人: Sean Christopherson <seanjc@google.com>
16. **[07-31 06:00]** Re: [PATCH 4/9] KVM: selftests: Drop unreachable, dead code from
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
17. **[07-31 08:56]** Re: [PATCH 3/9] KVM: selftests: Affine child tasks to other pCPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>
18. **[07-31 09:03]** Re: [PATCH 3/9] KVM: selftests: Affine child tasks to other pCPUs in
 hardware disable test
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 15: [PATCH v15 00/37] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 15 Jul 2026 15:28:02 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:10, 2652 tokens)

#### 📝 邮件列表

1. **[07-15 15:28]** [PATCH v15 00/37] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[07-15 15:28]** [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
3. **[07-15 15:28]** [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
4. **[07-27 17:14]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
5. **[07-27 10:21]** Re: [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-27 16:01]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-29 11:47]** Re: [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
8. **[07-29 11:58]** Re: [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-30 09:47]** Re: [PATCH v15 13/37] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
10. **[07-30 14:58]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
11. **[07-30 15:57]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[07-30 17:17]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
13. **[07-31 09:57]** Re: [PATCH v15 14/37] KVM: arm64: CCA: Handle realm enter/exit
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>

---

### Thread 16: [PATCH v8 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 13 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 29 Jul 2026 12:13:00 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:13, 6918 tokens)

#### 📝 邮件列表

1. **[07-29 12:13]** [PATCH v8 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[07-29 12:13]** [PATCH v8 1/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[07-29 12:13]** [PATCH v8 2/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[07-29 12:13]** [PATCH v8 3/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[07-29 12:13]** [PATCH v8 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[07-29 12:13]** [PATCH v8 5/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[07-29 12:13]** [PATCH v8 6/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[07-29 12:13]** [PATCH v8 7/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[07-29 12:23]** Re: [PATCH v8 4/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host
 handler
   - 发件人: sashiko-bot@kernel.org
10. **[07-29 12:26]** Re: [PATCH v8 6/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in
 host handler
   - 发件人: sashiko-bot@kernel.org
11. **[07-29 12:27]** Re: [PATCH v8 5/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host
 handler
   - 发件人: sashiko-bot@kernel.org
12. **[07-29 12:29]** Re: [PATCH v8 1/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP
 calls to Trustzone
   - 发件人: sashiko-bot@kernel.org
13. **[07-29 12:34]** Re: [PATCH v8 2/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in
 host handler
   - 发件人: sashiko-bot@kernel.org

---

### Thread 17: [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes

**📧 邮件数**: 11 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 17 Jul 2026 14:03:10 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:6 新:5, 2306 tokens)

#### 📝 邮件列表

1. **[07-17 14:03]** [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-17 14:03]** [PATCH v5 1/7] KVM: arm64: Skip cache maintenance for non-cacheable pKVM mappings
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-17 14:03]** [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty logging faults
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-17 13:15]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: sashiko-bot@kernel.org
5. **[07-17 15:17]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-18 09:44]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty logging faults
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-28 16:29]** Re: [PATCH v5 1/7] KVM: arm64: Skip cache maintenance for
 non-cacheable pKVM mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[07-31 00:10]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[07-31 09:23]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty logging faults
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-31 11:51]** Re: [PATCH v5 0/7] KVM: arm64: pKVM stage-2 mapping and memcache fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[07-31 12:05]** Re: [PATCH v5 3/7] KVM: arm64: Top up stage-2 memcache for dirty
 logging faults
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 18: [PATCH 0/2] KVM: arm64: Fix host-directed debug for non-protected pKVM guests

**📧 邮件数**: 7 | **👥 参与者**: 4 | **📅 开始时间**: Sun, 26 Jul 2026 15:36:41 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:6, 3588 tokens)

#### 📝 邮件列表

1. **[07-26 15:36]** [PATCH 0/2] KVM: arm64: Fix host-directed debug for non-protected pKVM guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-31 11:51]** Re: [PATCH 0/2] KVM: arm64: Fix host-directed debug for non-protected pKVM guests
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[07-31 21:44]** [PATCH 0/2] KVM: arm64: ID register finalisation fixes
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-31 21:44]** [PATCH 1/2] KVM: arm64: Finalize guest-wide sysregs prior to
 per-vCPU sysregs
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-31 21:44]** [PATCH 2/2] KVM: arm64: Block ID register changes after we rely on
 the values
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-31 21:02]** Re: [PATCH 1/2] KVM: arm64: Finalize guest-wide sysregs prior to
 per-vCPU sysregs
   - 发件人: sashiko-bot@kernel.org
7. **[08-02 18:13]** Re: [PATCH 2/2] KVM: arm64: Block ID register changes after we rely
 on the values
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 19: [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests

**📧 邮件数**: 6 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 22 Jul 2026 20:26:58 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:3, 1064 tokens)

#### 📝 邮件列表

1. **[07-22 20:26]** [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>
2. **[07-22 20:26]** [PATCH v3 1/4] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict PMUv3 UAPI
   - 发件人: Congkai Tan <congkai@amazon.com>
3. **[07-22 20:47]** Re: [PATCH v3 1/4] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict
 PMUv3 UAPI
   - 发件人: sashiko-bot@kernel.org
4. **[07-29 10:27]** Re: [PATCH v3 1/4] KVM: arm64: Expose PMMIR_EL1.SLOTS under strict
 PMUv3 UAPI
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-29 12:38]** Re: [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-31 11:51]** Re: [PATCH v3 0/4] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 20: [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue

**📧 邮件数**: 5 | **👥 参与者**: 5 | **📅 开始时间**: Wed, 29 Jul 2026 11:28:52 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:5, 4219 tokens)

#### 📝 邮件列表

1. **[07-29 11:28]** [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: Peng Fan (OSS) <peng.fan@oss.nxp.com>
2. **[07-29 03:42]** Re: [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: sashiko-bot@kernel.org
3. **[07-29 10:50]** Re: [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[07-29 20:52]** Re: [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: Peng Fan <peng.fan@oss.nxp.com>
5. **[07-29 12:09]** Re: [PATCH] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: Frank Li <Frank.li@oss.nxp.com>

---

### Thread 21: [PATCH] KVM: arm64: Drop %pB on nVHE panic when stage-2 is active

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 31 Jul 2026 19:22:31 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:4, 972 tokens)

#### 📝 邮件列表

1. **[07-31 19:22]** [PATCH] KVM: arm64: Drop %pB on nVHE panic when stage-2 is active
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-31 18:38]** Re: [PATCH] KVM: arm64: Drop %pB on nVHE panic when stage-2 is
 active
   - 发件人: sashiko-bot@kernel.org
3. **[08-02 12:26]** Re: [PATCH] KVM: arm64: Drop %pB on nVHE panic when stage-2 is active
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[08-02 12:31]** Re: [PATCH] KVM: arm64: Drop %pB on nVHE panic when stage-2 is active
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 22: [PATCH v3 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 18:14:56 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:1, 586 tokens)

#### 📝 邮件列表

1. **[07-20 18:14]** [PATCH v3 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-20 18:14]** [PATCH v3 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-20 17:25]** Re: [PATCH v3 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: sashiko-bot@kernel.org
4. **[07-31 09:05]** Re: [PATCH v3 01/17] KVM: arm64: Add pkvm_private_va_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 23: [PATCH v1 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Jul 2026 17:13:32 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:2, 1014 tokens)

#### 📝 邮件列表

1. **[07-20 17:13]** [PATCH v1 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-20 17:13]** [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at the caller
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-30 13:37]** Re: [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at the caller
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-30 14:47]** Re: [PATCH v1 09/11] KVM: arm64: Type-check hypercall arguments at
 the caller
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 24: [PATCH v4 8/9] KVM: selftests: Add rule to generate default tests
 for KVM selftests runner

**📧 邮件数**: 4 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 29 Jul 2026 12:07:35 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:4, 3260 tokens)

#### 📝 邮件列表

1. **[07-29 12:07]** Re: [PATCH v4 8/9] KVM: selftests: Add rule to generate default tests
 for KVM selftests runner
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[07-29 12:09]** Re: [PATCH v4 9/9] KVM: selftests: Provide README.rst for KVM
 selftests runner
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[07-29 12:14]** Re: [PATCH v4 6/9] KVM: selftests: Add various print flags to KVM
 selftest runner
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[07-29 12:39]** Re: [PATCH v4 3/9] KVM: selftests: Add timeout option in selftests runner
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 25: [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 23 Jul 2026 16:20:02 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:2, 390 tokens)

#### 📝 邮件列表

1. **[07-23 16:20]** [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-30 13:39]** Re: [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-31 11:51]** Re: [PATCH v3] KVM: arm64: Optimize protected mode with FWB and DIC
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 26: [PATCH v2] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 30 Jul 2026 21:53:02 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 3917 tokens)

#### 📝 邮件列表

1. **[07-30 21:53]** [PATCH v2] arm64: errata: Add NXP iMX8QM workaround for A53 cache
 coherency issue
   - 发件人: Peng Fan (OSS) <peng.fan@oss.nxp.com>
2. **[07-30 14:11]** Re: [PATCH v2] arm64: errata: Add NXP iMX8QM workaround for A53
 cache coherency issue
   - 发件人: sashiko-bot@kernel.org
3. **[07-30 15:32]** Re: [PATCH v2] arm64: errata: Add NXP iMX8QM workaround for A53 cache coherency issue
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH v1] KVM: arm64: vgic: Reset in_kernel on private IRQ allocation failure

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sun,  2 Aug 2026 16:08:45 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 459 tokens)

#### 📝 邮件列表

1. **[08-02 16:08]** [PATCH v1] KVM: arm64: vgic: Reset in_kernel on private IRQ allocation failure
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[08-02 16:55]** Re: [PATCH v1] KVM: arm64: vgic: Reset in_kernel on private IRQ allocation failure
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 28: [PATCH] KVM: arm64: Preserve AArch32 CP64 registers on rejected reads

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat,  1 Aug 2026 17:36:16 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 894 tokens)

#### 📝 邮件列表

1. **[08-01 17:36]** [PATCH] KVM: arm64: Preserve AArch32 CP64 registers on rejected reads
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>
2. **[08-02 12:53]** Re: [PATCH] KVM: arm64: Preserve AArch32 CP64 registers on rejected reads
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 29: [PATCH] arm64: Query per-VM capabilities when selecting vCPU features

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 14 Jul 2026 12:03:29 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 331 tokens)

#### 📝 邮件列表

1. **[07-14 12:03]** [PATCH] arm64: Query per-VM capabilities when selecting vCPU features
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[08-01 12:28]** Re: [PATCH] arm64: Query per-VM capabilities when selecting vCPU features
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 30: [PATCH v8 04/11] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 31 Jul 2026 17:50:22 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 345 tokens)

#### 📝 邮件列表

1. **[07-31 17:50]** Re: [PATCH v8 04/11] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Will Deacon <will@kernel.org>
2. **[08-01 15:34]** Re: [PATCH v8 04/11] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 31: [PATCH] KVM: arm64: nv: Don't skip VNCR invalidation when the TLB
 size is unknown

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 28 Jul 2026 01:26:11 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 1480 tokens)

#### 📝 邮件列表

1. **[07-28 01:26]** [PATCH] KVM: arm64: nv: Don't skip VNCR invalidation when the TLB
 size is unknown
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[07-28 10:46]** Re: [PATCH] KVM: arm64: nv: Don't skip VNCR invalidation when the TLB
 size is unknown
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 32: [PATCH v8 00/21] ARM64 PMU Partitioning

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Jul 2026 20:57:13 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 613 tokens)

#### 📝 邮件列表

1. **[07-23 20:57]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-27 12:04]** Re: [PATCH v8 00/21] ARM64 PMU Partitioning
   - 发件人: James Clark <james.clark@linaro.org>

---

### Thread 33: [PATCH v2] KVM: arm64: Preserve GPRs for AArch32 CP64 reads generating an UNDEF

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun,  2 Aug 2026 20:22:22 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 620 tokens)

#### 📝 邮件列表

1. **[08-02 20:22]** [PATCH v2] KVM: arm64: Preserve GPRs for AArch32 CP64 reads generating an UNDEF
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>

---

### Thread 34: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sat,  1 Aug 2026 12:28:28 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 230 tokens)

#### 📝 邮件列表

1. **[08-01 12:28]** Re: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 35: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 30 Jul 2026 11:37:59 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 868 tokens)

#### 📝 邮件列表

1. **[07-30 11:37]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 36: [PATCH 05/21] perf: arm_pmuv3: Check cntr_mask before using
 pmccntr

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 28 Jul 2026 16:07:44 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 186 tokens)

#### 📝 邮件列表

1. **[07-28 16:07]** Re: [PATCH 05/21] perf: arm_pmuv3: Check cntr_mask before using
 pmccntr
   - 发件人: Robin Murphy <robin.murphy@arm.com>

---

### Thread 37: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 27 Jul 2026 12:11:10 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 217 tokens)

#### 📝 邮件列表

1. **[07-27 12:11]** Re: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

## 📌 RFC

共 7 个 thread

---

### Thread 1: [RFC PATCH v1 0/2] KVM: arm64: CCA: Add MEC policy support for CCA Realms

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 24 Jul 2026 18:40:54 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:3, 1021 tokens)

#### 📝 邮件列表

1. **[07-24 18:40]** [RFC PATCH v1 0/2] KVM: arm64: CCA: Add MEC policy support for CCA Realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
2. **[07-24 18:40]** [RFC PATCH v1 1/2] KVM: arm64: CCA: Add support for configuring the Realm MEC policy
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
3. **[07-29 12:47]** Re: [RFC PATCH v1 1/2] KVM: arm64: CCA: Add support for configuring
 the Realm MEC policy
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[07-31 14:09]** Re: [RFC PATCH v1 1/2] KVM: arm64: CCA: Add support for configuring
 the Realm MEC policy
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>
5. **[07-31 11:59]** Re: [RFC PATCH v1 1/2] KVM: arm64: CCA: Add support for configuring
 the Realm MEC policy
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 2: [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 17 Jul 2026 09:26:57 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:2, 1136 tokens)

#### 📝 邮件列表

1. **[07-17 09:26]** [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[07-28 09:45]** Re: [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[07-31 10:26]** Re: [RFC] KVM: Proposed uAPI for querying GSI and irqbypass status
   - 发件人: Jing Zhang <jingzhangos@google.com>

---

### Thread 3: [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Jul 2026 18:21:38 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:2, 487 tokens)

#### 📝 邮件列表

1. **[07-23 18:21]** [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-30 08:52]** Re: [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3
   - 发件人: Linu Cherian <linu.cherian@arm.com>
3. **[07-30 09:30]** Re: [RFC PATCH v2 0/2] KVM: arm64: Add support for BBM level 3
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 4: [RFC PATCH 0/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 16 Jul 2026 19:39:31 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:0, 597 tokens)

#### 📝 邮件列表

1. **[07-16 19:39]** [RFC PATCH 0/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[07-16 19:39]** [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime mappings
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[07-16 14:27]** Re: [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime
 mappings
   - 发件人: sashiko-bot@kernel.org

---

### Thread 5: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 30 Jul 2026 15:46:22 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 293 tokens)

#### 📝 邮件列表

1. **[07-30 15:46]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

### Thread 6: [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime
 mappings

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 28 Jul 2026 19:31:42 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 426 tokens)

#### 📝 邮件列表

1. **[07-28 19:31]** Re: [RFC PATCH 5/5] KVM: arm64: Use TTBR1_EL2 for hVHE runtime
 mappings
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

### Thread 7: [RFC PATCH] KVM: arm64: Add KUnit tests for stage 2 walker memcache consumption

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 27 Jul 2026 18:30:05 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 2790 tokens)

#### 📝 邮件列表

1. **[07-27 18:30]** [RFC PATCH] KVM: arm64: Add KUnit tests for stage 2 walker memcache consumption
   - 发件人: Bradley Morgan <include@grrlz.net>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.2, take #3

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 24 Jul 2026 09:47:42 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 274 tokens)

#### 📝 邮件列表

1. **[07-24 09:47]** [GIT PULL] KVM/arm64 fixes for 7.2, take #3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-28 17:41]** Re: [GIT PULL] KVM/arm64 fixes for 7.2, take #3
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

