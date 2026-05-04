# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-05-04 00:45:15

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 378
- **总 Thread 数**: 31
- **大型 Thread** (>20封): 5 个

### 分类分布

- **PATCH**: 18 threads (247 邮件)
- **RFC**: 7 threads (119 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Discussion**: 2 threads (2 邮件)
- **Other**: 3 threads (8 邮件)

---

## 📌 PATCH

共 18 个 thread

---

### Thread 1: [PATCH 00/43] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 66 | **👥 参与者**: 5 | **📅 开始时间**: Mon, 27 Apr 2026 16:06:01 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）中 GICv5（Generic Interrupt Controller version 5）IRS（Interrupt Routing Service）支持的多个补丁和改进。

1. **原始补丁/问题内容**：
   本系列补丁旨在为 KVM 的 arm64 架构添加对 GICv5 IRS 的支持，使得 GICv5 客户机能够使用 SPI（共享中断）和 LPI（本地中断），而不仅限于 PPI（私有中断）。补丁包括对 IRS MMIO 接口的实现，允许 KVM 处理 IRS 的状态和配置。

2. **之前讨论要点**：
   之前的讨论集中在如何将 GICv5 的功能集成到 KVM 中，特别是如何管理中断状态、分配和管理虚拟机表（VMTE）以及如何处理 IRS 的 MMIO 访问。参与者们强调了 GICv5 的复杂性，尤其是在中断生命周期管理方面。

3. **本周的新讨论、进展或结论**：
   本周的讨论主要围绕补丁的具体实现和代码审查。Sascha Bischoff 提出了多个补丁，涵盖了 IRS 的 MMIO 读写、SPI 和 LPI 的注入、以及 IST（中断状态表）的保存与恢复机制。Marc Zyngier 和 Vladimir Murzin 提出了代码优化建议，指出了一些潜在的错误处理和代码可读性问题。最终，补丁集的目标是确保 KVM 能够正确支持 GICv5 的完整功能，包括对 SPIs 和 LPIs 的管理，以及在虚拟机迁移时的状态保存与恢复。

总之，本邮件线程展示了 KVM 团队在实现 GICv5 IRS 支持方面的努力，以及在代码审查过程中对质量和性能的关注。

#### 📝 邮件列表

1. **[04-27 16:06]** [PATCH 00/43] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[04-27 16:06]** [PATCH 01/43] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG encodings
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[04-27 16:06]** [PATCH 02/43] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[04-27 16:07]** [PATCH 03/43] KVM: arm64: gic-v5: Add resident/non-resident hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[04-27 16:07]** [PATCH 04/43] irqchip/gic-v5: Provide IRS config frame attrs to KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[04-27 16:07]** [PATCH 05/43] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[04-27 16:08]** [PATCH 06/43] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[04-27 16:08]** [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[04-27 16:08]** [PATCH 08/43] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[04-27 16:09]** [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[04-27 16:09]** [PATCH 10/43] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[04-27 16:09]** [PATCH 11/43] KVM: arm64: gic-v5: Make VPEs valid in vgic_v5_reset()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[04-27 16:10]** [PATCH 12/43] KVM: arm64: gic-v5: Clear db_fired flag before making
 VPE non-resident
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[04-27 16:10]** [PATCH 13/43] KVM: arm64: gic-v5: Make VPEs (non-)resident in
 vgic_load/put
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[04-27 16:10]** [PATCH 14/43] KVM: arm64: gic-v5: Request VPE doorbells when going
 non-resident
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[04-27 16:11]** [PATCH 15/43] KVM: arm64: gic-v5: Handle doorbells in
 kvm_vgic_vcpu_pending_irq()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[04-27 16:11]** [PATCH 16/43] KVM: arm64: gic-v5: Initialise and teardown VMTEs &
 doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[04-27 16:11]** [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and
 disable on teardown
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[04-27 16:12]** [PATCH 18/43] KVM: arm64: gic-v5: Define remaining IRS MMIO registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[04-27 16:12]** [PATCH 19/43] KVM: arm64: gic-v5: Introduce struct vgic_v5_irs and
 IRS base address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[04-27 16:12]** [PATCH 20/43] KVM: arm64: gic-v5: Add IRS IODEV to iodev_types and
 generic MMIO handlers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[04-27 16:13]** [PATCH 21/43] KVM: arm64: gic-v5: Add KVM_VGIC_V5_ADDR_TYPE_IRS to
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[04-27 16:13]** [PATCH 22/43] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[04-27 16:13]** [PATCH 23/43] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS enable
 state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[04-27 16:14]** [PATCH 24/43] KVM: arm64: gic-v5: Call IRS init/teardown from vgic_v5
 init/teardown
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[04-27 16:14]** [PATCH 25/43] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[04-27 16:14]** [PATCH 26/43] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[04-27 16:15]** [PATCH 27/43] KVM: arm64: selftests: Update vGICv5 selftest to set
 IRS address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[04-27 16:15]** [PATCH 28/43] KVM: arm64: gic-v5: Introduce SPI AP list
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[04-27 16:15]** [PATCH 29/43] KVM: arm64: gic-v5: Add GIC VDPEND and GIC VDRCFG hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[04-27 16:16]** [PATCH 30/43] KVM: arm64: gic-v5: Track SPI state for in-flight SPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[04-27 16:16]** [PATCH 31/43] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[04-27 16:16]** [PATCH 32/43] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[04-27 16:17]** [PATCH 33/43] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[04-27 16:17]** [PATCH 34/43] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[04-27 16:17]** [PATCH 35/43] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg userspace
 set/get interface
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[04-27 16:18]** [PATCH 36/43] KVM: arm64: gic-v5: Implement save/restore mechanisms
 for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[04-27 16:18]** [PATCH 37/43] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[04-27 16:19]** [PATCH 38/43] KVM: arm64: gic-v5: Add VGIC_GRP_IRS_REGS/VGIC_GRP_IST
 to UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[04-27 16:19]** [PATCH 39/43] KVM: arm64: gic-v5: Plumb in has/set/get_attr for
 sysregs & IRS MMIO regs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[04-27 16:19]** [PATCH 40/43] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
42. **[04-27 16:20]** [PATCH 41/43] Documentation: KVM: Add KVM_DEV_ARM_VGIC_GRP_IRS_REGS
 to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
43. **[04-27 16:20]** [PATCH 42/43] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
44. **[04-27 16:20]** [PATCH 43/43] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
45. **[04-28 15:28]** Re: [PATCH 03/43] KVM: arm64: gic-v5: Add resident/non-resident hyp calls
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[04-28 15:54]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
47. **[04-28 15:56]** Re: [PATCH 04/43] irqchip/gic-v5: Provide IRS config frame attrs to KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
48. **[04-28 16:20]** Re: [PATCH 05/43] KVM: arm64: gic-v5: Extract host IRS caps from IRS config frame
   - 发件人: Marc Zyngier <maz@kernel.org>
49. **[04-28 16:55]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Joey Gouly <joey.gouly@arm.com>
50. **[04-28 17:40]** Re: [PATCH 06/43] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Marc Zyngier <maz@kernel.org>
51. **[04-29 11:25]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE tables
   - 发件人: Marc Zyngier <maz@kernel.org>
52. **[04-29 13:50]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Joey Gouly <joey.gouly@arm.com>
53. **[04-29 15:29]** Re: [PATCH 08/43] KVM: arm64: gic-v5: Introduce guest IST alloc and management
   - 发件人: Marc Zyngier <maz@kernel.org>
54. **[04-29 17:04]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Marc Zyngier <maz@kernel.org>
55. **[04-30 09:46]** Re: [PATCH 10/43] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Marc Zyngier <maz@kernel.org>
56. **[04-30 09:57]** Re: [PATCH 43/43] Documentation: KVM: Add the VGICv5 IRS save/restore sequences
   - 发件人: Peter Maydell <peter.maydell@linaro.org>
57. **[04-30 10:37]** Re: [PATCH 11/43] KVM: arm64: gic-v5: Make VPEs valid in vgic_v5_reset()
   - 发件人: Marc Zyngier <maz@kernel.org>
58. **[04-30 11:26]** Re: [PATCH 13/43] KVM: arm64: gic-v5: Make VPEs (non-)resident in vgic_load/put
   - 发件人: Marc Zyngier <maz@kernel.org>
59. **[04-30 11:37]** Re: [PATCH 14/43] KVM: arm64: gic-v5: Request VPE doorbells when going non-resident
   - 发件人: Marc Zyngier <maz@kernel.org>
60. **[04-30 13:23]** Re: [PATCH 16/43] KVM: arm64: gic-v5: Initialise and teardown VMTEs & doorbells
   - 发件人: Marc Zyngier <maz@kernel.org>
61. **[05-01 16:40]** Re: [PATCH 03/43] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
62. **[05-01 16:42]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
63. **[05-01 16:44]** Re: [PATCH 05/43] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
64. **[05-01 16:46]** Re: [PATCH 04/43] irqchip/gic-v5: Provide IRS config frame attrs to
 KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
65. **[05-01 16:54]** Re: [PATCH 06/43] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
66. **[05-01 19:54]** Re: [PATCH 36/43] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>

---

### Thread 2: [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 32 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  1 May 2026 11:19:02 +0000

#### 🤖 AI 总结

本邮件讨论主题为「[PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)」，主要围绕为 KVM 提供 SMMUv3 驱动的补丁系列进行讨论。

**原始 patch/问题的内容**：
该补丁系列旨在为 KVM 提供 SMMUv3 支持，允许通过“捕获和模拟”方式来管理设备的 DMA 隔离。补丁系列的第六版（v6）基于之前版本的反馈进行了改进，包括对新合并的受保护虚拟机支持的重构和代码优化。

**之前讨论要点**：
历史讨论中提到，补丁系列经历了多个版本的迭代，逐步实现了完整的 PV 接口、DMA 隔离、命令队列和流表的模拟等功能。参与者们讨论了如何优化代码结构，以便更好地支持 KVM 的需求。

**本周的新讨论、进展或结论**：
本周的讨论集中在补丁的具体实现上，包括：
1. 增加了对命令队列（CMDQ）和流表（STE）的模拟功能，确保在 SMMU 启用时能够正确处理命令。
2. 引入了 DMA 隔离的支持，允许通过 IOMMU 驱动注册操作来实现。
3. 讨论了如何共享其他队列（如 PRI 和 EVTQ），确保它们在启用时不会被捐赠给虚拟机。
4. 对 SMMUv3 的初始化、命令发送和数据中断处理进行了详细的实现和测试。

此外，邮件中还提到了一些代码结构的优化建议，强调了在实现过程中保持代码的可维护性和可读性的重要性。整体上，讨论表明该补丁系列在实现 SMMUv3 驱动的过程中取得了显著进展，并为未来的功能扩展奠定了基础。

#### 📝 邮件列表

1. **[05-01 11:19]** [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-01 11:19]** [PATCH v6 01/25] KVM: arm64: Generalize trace clock
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-01 11:19]** [PATCH v6 02/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-01 11:19]** [PATCH v6 03/25] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-01 11:19]** [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation into
 common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-01 11:19]** [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[05-01 11:19]** [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[05-01 11:19]** [PATCH v6 07/25] KVM: arm64: iommu: Introduce IOMMU driver infrastructure
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[05-01 11:19]** [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
10. **[05-01 11:19]** [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>
11. **[05-01 11:19]** [PATCH v6 10/25] KVM: arm64: iommu: Support DABT for IOMMU
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[05-01 11:19]** [PATCH v6 11/25] iommu/arm-smmu-v3-kvm: Add SMMUv3 driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
13. **[05-01 11:19]** [PATCH v6 12/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
14. **[05-01 11:19]** [PATCH v6 13/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
15. **[05-01 11:19]** [PATCH v6 14/25] iommu/arm-smmu-v3-kvm: Add MMIO emulation
   - 发件人: Mostafa Saleh <smostafa@google.com>
16. **[05-01 11:19]** [PATCH v6 15/25] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[05-01 11:19]** [PATCH v6 16/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
18. **[05-01 11:19]** [PATCH v6 17/25] iommu/arm-smmu-v3-kvm: Emulate CMDQ for host
   - 发件人: Mostafa Saleh <smostafa@google.com>
19. **[05-01 11:19]** [PATCH v6 18/25] iommu/arm-smmu-v3-kvm: Shadow stream table
   - 发件人: Mostafa Saleh <smostafa@google.com>
20. **[05-01 11:19]** [PATCH v6 19/25] iommu/arm-smmu-v3-kvm: Shadow STEs
   - 发件人: Mostafa Saleh <smostafa@google.com>
21. **[05-01 11:19]** [PATCH v6 20/25] iommu/arm-smmu-v3-kvm: Share other queues
   - 发件人: Mostafa Saleh <smostafa@google.com>
22. **[05-01 11:19]** [PATCH v6 21/25] iommu/arm-smmu-v3-kvm: Emulate GBPA
   - 发件人: Mostafa Saleh <smostafa@google.com>
23. **[05-01 11:19]** [PATCH v6 22/25] iommu/io-pgtable-arm: Support io-pgtable-arm in the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
24. **[05-01 11:19]** [PATCH v6 23/25] iommu/arm-smmu-v3-kvm: Shadow the CPU stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
25. **[05-01 11:19]** [PATCH v6 24/25] iommu/arm-smmu-v3-kvm: Enable nesting
   - 发件人: Mostafa Saleh <smostafa@google.com>
26. **[05-01 11:19]** [PATCH v6 25/25] KVM: arm64: Add documentation for pKVM DMA isolation
   - 发件人: Mostafa Saleh <smostafa@google.com>
27. **[05-01 09:24]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
28. **[05-01 09:41]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
29. **[05-01 09:44]** Re: [PATCH v6 03/25] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
30. **[05-01 09:47]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
31. **[05-01 09:51]** Re: [PATCH v6 13/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
32. **[05-01 10:00]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>

---

### Thread 3: [PATCH v2 00/28] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 30 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 28 Apr 2026 17:55:52 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 160886 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:30, 120073 tokens)

#### 📝 邮件列表

1. **[04-28 17:55]** [PATCH v2 00/28] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[04-28 17:55]** [PATCH v2 01/28] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[04-28 17:55]** [PATCH v2 02/28] KVM, vfio: remove symbol_get(kvm_get_kvm_safe) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[04-28 17:55]** [PATCH v2 03/28] KVM, vfio: remove symbol_get(kvm_put_kvm) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[04-28 17:55]** [PATCH v2 04/28] arm64: Provide arm64 UAPI for other host architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[04-28 17:55]** [PATCH v2 05/28] arm64: Extract sysreg definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[04-28 17:55]** [PATCH v2 06/28] arm64: Provide arm64 API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[04-28 17:55]** [PATCH v2 07/28] KVM: arm64: Provide arm64 KVM API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[04-28 17:56]** [PATCH v2 08/28] arm64: Extract pstate definitions from ptrace
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[04-28 17:56]** [PATCH v2 09/28] KVM: arm64: Share kvm_emulate definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[04-28 17:56]** [PATCH v2 10/28] KVM: arm64: Make some arm64 KVM code shareable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[04-28 17:56]** [PATCH v2 11/28] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[04-28 17:56]** [PATCH v2 12/28] KVM: arm64: Share reset general register code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[04-28 17:56]** [PATCH v2 13/28] KVM: arm64: Extract & share ipa size shift calculation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[04-28 17:56]** [PATCH v2 14/28] MAINTAINERS: Add Steffen as reviewer for KVM/arm64
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[04-28 17:56]** [PATCH v2 15/28] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[04-28 17:56]** [PATCH v2 16/28] KVM: S390: Refactor gmap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[04-28 17:56]** [PATCH v2 17/28] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[04-28 17:56]** [PATCH v2 18/28] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[04-28 17:56]** [PATCH v2 19/28] KVM: s390: Prepare kvm-s390 for a second kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[04-28 17:56]** [PATCH v2 20/28] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[04-28 17:56]** [PATCH v2 21/28] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[04-28 17:56]** [PATCH v2 22/28] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[04-28 17:56]** [PATCH v2 23/28] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[04-28 17:56]** [PATCH v2 24/28] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[04-28 17:56]** [PATCH v2 25/28] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[04-28 17:56]** [PATCH v2 26/28] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[04-28 17:56]** [PATCH v2 27/28] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[04-28 17:56]** [PATCH v2 28/28] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
30. **[04-29 10:04]** Re: [PATCH v2 04/28] arm64: Provide arm64 UAPI for other host
 architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 4: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)

**📧 邮件数**: 19 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 30 Apr 2026 12:14:04 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine） 的补丁集，主题为「KVM 脏位清理加速器（HACDBS）」。该补丁集的主要目的是为 arm64 架构引入一个硬件加速的脏位清理机制，以提高虚拟机内存管理的效率。

**补丁内容**：
补丁集包含 12 个补丁，主要涉及添加 HACDBS 支持的代码，包括检测和初始化 HACDBSIRQ、实现硬件加速的脏位清理例程等。补丁的第一部分主要是为了测试和依赖关系的处理，后续补丁则逐步实现了具体的功能。

**历史讨论要点**：
在之前的讨论中，参与者探讨了补丁的结构、功能分配以及如何在 MAINTAINERS 文件中添加维护者信息等问题。Leonardo Bras 提出了多个问题，寻求社区的反馈，包括补丁的分布是否合理、是否需要在 MAINTAINERS 中添加条目、调试信息的处理等。

**本周新讨论与进展**：
本周的讨论中，Leonardo Bras 提交了多个补丁，并对补丁的功能进行了详细说明。Marc Zyngier 对补丁进行了初步反馈，建议移除调试基础设施，并对如何让用户空间控制相关功能提出了疑问。Leonardo 也分享了在 QEMU 中进行的测试结果，指出 HACDBS 在某些情况下性能不如软件清理，表示将继续进行更深入的性能测试。

总的来说，本次讨论集中在 HACDBS 的实现细节、性能评估以及如何在 KVM 中有效集成这一新特性。

#### 📝 邮件列表

1. **[04-30 12:14]** [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[04-30 12:14]** [PATCH v1 01/12] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[04-30 12:14]** [PATCH v1 02/12] KVM: arm64: HDBSS bits
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[04-30 12:14]** [PATCH v1 03/12] arm64/cpufeature: Add system-wide FEAT_HACDBS detection
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[04-30 12:14]** [PATCH v1 04/12] arm64/sysreg: Add HACDBS consumer and base registers
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[04-30 12:14]** [PATCH v1 05/12] KVM: arm64: Detect (via ACPI) and initialize HACDBSIRQ
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[04-30 12:14]** [PATCH v1 06/12] KVM: arm64: dirty_bit: Add base FEAT_HACDBS cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[04-30 12:14]** [PATCH v1 07/12] kvm: Add arch-generic interface for hw-accelerated dirty-bitmap cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[04-30 12:14]** [PATCH v1 08/12] KVM: arm64: Add hardware-accelerated dirty-bitmap cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[04-30 12:14]** [PATCH v1 09/12] kvm/dirty_ring: Introduce get_memslot and move helpers to header
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[04-30 12:14]** [PATCH v1 10/12] kvm/dirty_ring: Add arch-generic interface for hw-accelerated dirty-ring cleaning
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[04-30 12:14]** [PATCH v1 11/12] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[04-30 12:14]** [PATCH v1 12/12] KVM: arm64: Enable KVM_HW_DIRTY_BIT
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[04-30 14:14]** Re: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[04-30 14:29]** Re: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
16. **[04-30 15:51]** Re: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[04-30 16:35]** Re: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
18. **[05-01 11:11]** Re: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Mark Brown <broonie@kernel.org>
19. **[05-03 10:01]** Re: [PATCH v1 04/12] arm64/sysreg: Add HACDBS consumer and base
 registers
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 5: [PATCH 0/8] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes

**📧 邮件数**: 19 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 28 Apr 2026 11:30:00 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的多个补丁，主要集中在 EL2 同步和 pKVM 阶段 2 错误传播的修复。

1. **原始补丁内容**：本系列补丁（共 8 个）旨在修复 EL2 上的上下文同步问题和 pKVM 阶段 2 的错误传播。补丁分为三个主要组：EL2 上下文同步（补丁 1-2）、小修复（补丁 3-4）和 pKVM 阶段 2 错误传播（补丁 5-8）。

2. **之前讨论要点**：历史讨论中没有具体的补丁内容，但参与者们关注了如何确保 EL2 异常的入口和出口是上下文同步事件，以及如何处理在 pKVM 中可能导致致命错误的内存映射失败。

3. **本周的新讨论与进展**：本周的讨论主要围绕补丁的具体实现和潜在问题展开。Fuad Tabba 提出了多个补丁，修复了 EL2 上的同步问题和 pKVM 的错误传播。Will Deacon 对某些补丁提出了质疑，特别是关于错误处理的逻辑，认为在处理单页映射失败时不应尝试回滚。最终，Fuad 同意根据 Will 的建议进行修正，并计划在后续版本中进行调整。此外，Yao Yuan 和其他参与者对补丁表示支持，整体讨论氛围积极，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[04-28 11:30]** [PATCH 0/8] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[04-28 11:30]** [PATCH 1/8] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[04-28 11:30]** [PATCH 2/8] KVM: arm64: Synchronise HCR_EL2 writes on the guest exit path
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[04-28 11:30]** [PATCH 3/8] KVM: arm64: Guard against NULL vcpu on VHE hyp panic path
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[04-28 11:30]** [PATCH 4/8] KVM: arm64: Fix __deactivate_fgt macro parameter typo
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[04-28 11:30]** [PATCH 5/8] KVM: arm64: Propagate stage-2 map failure on host->guest share
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[04-28 11:30]** [PATCH 6/8] KVM: arm64: Propagate stage-2 map failure on host->guest donation
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[04-28 11:30]** [PATCH 7/8] KVM: arm64: Propagate stage-2 map failure on guest->host share
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[04-28 11:30]** [PATCH 8/8] KVM: arm64: Propagate stage-2 map failure on guest->host unshare
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[04-28 14:45]** Re: [PATCH 6/8] KVM: arm64: Propagate stage-2 map failure on
 host->guest donation
   - 发件人: Will Deacon <will@kernel.org>
11. **[04-28 14:50]** Re: [PATCH 2/8] KVM: arm64: Synchronise HCR_EL2 writes on the guest
 exit path
   - 发件人: Will Deacon <will@kernel.org>
12. **[04-28 15:21]** Re: [PATCH 2/8] KVM: arm64: Synchronise HCR_EL2 writes on the guest
 exit path
   - 发件人: Fuad Tabba <tabba@google.com>
13. **[04-28 15:36]** Re: [PATCH 6/8] KVM: arm64: Propagate stage-2 map failure on
 host->guest donation
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[04-28 17:57]** Re: [PATCH 6/8] KVM: arm64: Propagate stage-2 map failure on
 host->guest donation
   - 发件人: Will Deacon <will@kernel.org>
15. **[04-28 18:03]** Re: [PATCH 6/8] KVM: arm64: Propagate stage-2 map failure on
 host->guest donation
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[04-30 10:22]** Re: [PATCH 1/8] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
17. **[04-30 10:07]** Re: [PATCH 1/8] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Will Deacon <will@kernel.org>
18. **[04-30 13:18]** Re: [PATCH 1/8] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Fuad Tabba <tabba@google.com>
19. **[04-30 13:37]** Re: [PATCH 1/8] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 6: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 18 | **👥 参与者**: 1 | **📅 开始时间**: Sun,  3 May 2026 09:33:20 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM/ARM 的补丁系列，旨在引入可定制的 AArch64 KVM 主机模型，特别是增强对可写 ID 寄存器字段的支持。

### 原始补丁内容
补丁系列的核心是增强当前 KVM 主机模型，使用户空间能够覆盖部分 ID 寄存器的值，以便在不同主机硬件之间迁移虚拟机时提供更大的灵活性。

### 之前讨论要点
在历史讨论中，补丁系列的背景和目标被详细阐述。自 Linux v6.7 版本以来，KVM/ARM 允许用户空间覆盖部分 ID 寄存器的值，且可写字段的列表在不断增加。补丁通过生成的 ID 寄存器描述文件来实现这一功能，并引入了多个脚本以自动化生成和更新相关的代码。

### 本周的新讨论和进展
本周的讨论集中在补丁的具体实现上，包括：
1. 引入了多个脚本以自动生成 ID 寄存器的定义和属性。
2. 实现了对可写 ID 寄存器的查询和处理，确保在 KVM 中能够正确读取和写入这些寄存器。
3. 特殊处理了某些寄存器（如 REVIDR_EL1 和 AIDR_EL1），这些寄存器虽然可写，但没有公开命名字段。
4. 增加了文档说明，指导如何通过 ID 寄存器配置主机 CPU 模型的特性。

最终，这些补丁将使 KVM/ARM 在处理 ID 寄存器时更加灵活和强大，提升了虚拟化的能力。

#### 📝 邮件列表

1. **[05-03 09:33]** [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[05-03 09:33]** [PATCH v4 01/17] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-03 09:33]** [PATCH v4 02/17] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[05-03 09:33]** [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-03 09:33]** [PATCH v4 04/17] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[05-03 09:33]** [PATCH v4 05/17] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-03 09:33]** [PATCH v4 06/17] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[05-03 09:33]** [PATCH v4 07/17] target/arm/cpu-sysreg-properties.c: Generate code with new script
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[05-03 09:33]** [PATCH v4 08/17] target/arm/kvm: Introduce kvm_get_writable_id_regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[05-03 09:33]** [PATCH v4 09/17] arm/cpu: accessors for writable id registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[05-03 09:33]** [PATCH v4 10/17] arm/kvm: Allow reading all the writable ID registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[05-03 09:33]** [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[05-03 09:33]** [PATCH v4 12/17] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[05-03 09:33]** [PATCH v4 13/17] target/arm/kvm: Special case REVIDR_EL1 and AIDR_EL1
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[05-03 09:33]** [PATCH v4 14/17] target/arm/kvm: Special case ID_AA64ISAR0_EL1 RES0 [24, 27] bits
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[05-03 09:33]** [PATCH v4 15/17] arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[05-03 09:33]** [PATCH v4 16/17] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[05-03 09:33]** [PATCH v4 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 7: [PATCH v4 0/3] Enforce host page-size alignment for shared buffers

**📧 邮件数**: 17 | **👥 参与者**: 6 | **📅 开始时间**: Mon, 27 Apr 2026 12:01:05 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于在共享缓冲区中强制执行主机页面大小对齐的补丁系列。该补丁的主要目的是确保在私有内存客户机与主机之间共享的缓冲区遵循主机的页面大小对齐要求，以避免潜在的内核崩溃。

### 原始补丁/问题内容
补丁系列（[PATCH v4 0/3]）旨在解决私有内存客户机在与虚拟机监控程序共享缓冲区时的对齐问题。由于这些共享缓冲区也由主机内核访问，因此必须与主机的页面大小对齐。

### 之前讨论要点
在之前的讨论中，参与者强调了不正确的内存访问可能导致的安全隐患，尤其是在用户空间访问这些缓冲区时。补丁引入了新的辅助函数 `mem_decrypt_granule_size()` 和 `mem_decrypt_align()`，用于强制执行所需的对齐和大小约束。

### 本周的新讨论、进展或结论
本周的讨论集中在补丁的具体实现和结构上。参与者对补丁的结构提出了建议，认为应该将 `mem_decrypt_granule_size()` 的实现和相关调用分开，以提高代码的清晰度和可维护性。此外，关于如何处理主机和客户机之间的页面大小对齐问题的讨论也引发了不同的观点，特别是关于 RHI（Realm Host Interface）和 RSI（Realm Service Interface）的命名和实现细节。Aneesh Kumar K.V 表示将根据反馈进行补丁的修订，以确保更好地遵循页面对齐的要求。

#### 📝 邮件列表

1. **[04-27 12:01]** [PATCH v4 0/3] Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[04-27 12:01]** [PATCH v4 1/3] dma-direct: swiotlb: handle swiotlb alloc/free outside __dma_direct_alloc_pages
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[04-27 12:01]** [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[04-27 12:01]** [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[04-27 10:27]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-27 11:33]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[04-27 10:38]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
8. **[04-27 10:49]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
9. **[04-28 17:50]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
10. **[04-28 17:52]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
11. **[04-28 18:19]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
12. **[04-28 14:31]** Re: [PATCH v4 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[04-28 14:49]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[04-28 14:56]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Will Deacon <will@kernel.org>
15. **[04-28 16:22]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[04-29 14:31]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
17. **[04-29 14:33]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

### Thread 8: [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes

**📧 邮件数**: 10 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  1 May 2026 12:21:43 +0100

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 EL2 同步和 pKVM 阶段-2 错误传播修复的补丁（PATCH v2 0/6）。该补丁的主要目的是修复在 EL2 级别的异常处理和内存管理中的一些问题，以提高系统的稳定性和可靠性。

历史讨论中并未提及具体的补丁内容，但本周的讨论集中在补丁的具体实现和修改上。Fuad Tabba 提交了六个补丁，主要包括：
1. 修复 SCTLR_EL2.EIS 和 SCTLR_EL2.EOS 的处理，以确保异常进入和退出始终被视为上下文同步事件。
2. 增加对 NULL vcpu 指针的保护，以避免在处理异常时出现空指针解引用。
3. 修正了一个宏参数的拼写错误，确保代码的可读性和一致性。
4. 为 pKVM 自测虚拟 CPU 的内存缓存进行初始化，以满足后续补丁的要求。
5. 在主机到客人共享和捐赠的过程中，增加了对 vcpu 内存缓存的预检查，以防止因内存不足导致的错误。
6. 进一步增强了对捐赠请求的内存检查，确保在状态变更前进行有效的内存管理。

本周的讨论中，参与者 Ben Horgan 提出了对补丁描述的建议，认为应保留某些信息以帮助理解补丁的目的，Fuad 表示可以根据需要重新引入这些信息。整体来看，本周的讨论进一步推动了补丁的完善和清晰化。

#### 📝 邮件列表

1. **[05-01 12:21]** [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[05-01 12:21]** [PATCH v2 1/6] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[05-01 12:21]** [PATCH v2 2/6] KVM: arm64: Guard against NULL vcpu on VHE hyp panic path
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[05-01 12:21]** [PATCH v2 3/6] KVM: arm64: Fix __deactivate_fgt macro parameter typo
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[05-01 12:21]** [PATCH v2 4/6] KVM: arm64: Seed pkvm_ownership_selftest vcpu memcache
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[05-01 12:21]** [PATCH v2 5/6] KVM: arm64: Pre-check vcpu memcache for host->guest share
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[05-01 12:21]** [PATCH v2 6/6] KVM: arm64: Pre-check vcpu memcache for host->guest donate
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[05-01 14:47]** Re: [PATCH v2 1/6] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[05-01 16:01]** Re: [PATCH v2 1/6] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[05-01 16:07]** Re: [PATCH v2 1/6] KVM: arm64: Make EL2 exception entry and exit
 context-synchronization events
   - 发件人: Ben Horgan <ben.horgan@arm.com>

---

### Thread 9: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 22 Apr 2026 10:25:40 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下验证 FF-A（Firmware Framework for Arm）内存访问描述符位置的补丁。

**原始补丁内容**：
Sebastian Ene 提出的补丁旨在防止 pKVM 超级管理程序假设端点内存访问描述符（EMAD）紧跟在 FF-A 内存区域头之后，并在验证 FF-A 内存借用/共享事务时强制执行其严格位置。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 对补丁的逻辑提出质疑，认为强制位置的假设与 FF-A 规范相悖，因为规范允许内存区域头与 EMAD 之间存在可变间隙。Sebastian 解释了当前驱动程序的实现选择，并讨论了如何在未来可能进行更改。Sudeep Holla 也参与了讨论，提出了对现有函数的扩展建议，以确保内存偏移的有效性。

**本周的新讨论与进展**：
在本周的讨论中，Sebastian 提出了在偏移超出范围时使用 BUG_ON 的建议，并考虑在 ffa_mem_desc_offset 函数中进行偏移验证。M.samet Duman 对这一变化表示认可，尽管他尚未进行测试，但认为该更改是合理的。Sebastian 表示希望重新提交补丁的更新版本，以反映这些讨论的结果。

#### 📝 邮件列表

1. **[04-22 10:25]** [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[04-22 13:24]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-22 13:35]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[04-22 20:29]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
5. **[04-23 09:17]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[04-23 10:55]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
7. **[04-27 11:36]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[04-27 15:48]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: M.samet Duman <dumanmehmetsamet@icloud.com>

---

### Thread 10: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Apr 2026 09:38:55 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，目的是避免完全解除影子 S2 映射（shadow s2 unmap）。补丁的核心在于优化内存管理，尤其是在处理反向映射时的复杂性。

在历史讨论中，参与者 Marc Zyngier 和 Wei-Lin Chang 针对补丁的实现细节进行了深入探讨。Marc 提出了对术语使用的一些建议，并讨论了在特定上下文中选择 kvm_s2_mmu 实例时的引用计数问题。此外，他们还探讨了使用 RCU（读-复制-更新）机制来处理并行访问的可能性，以及在反向映射记录失败时如何安全地管理 maple tree 的指针。

在本周的新讨论中，Wei-Lin Chang 表示经过与 Marc 的讨论，他们认为将 maple tree 作为指针的做法会增加复杂性，因此决定在下一个版本中直接将 maple tree 实例添加到 kvm_s2_mmu 结构中。这一决定旨在简化实现，同时保持对非嵌套 MMU 的支持。

总结而言，本周的进展是 Wei-Lin Chang 确定了补丁的方向，将 maple tree 直接集成到 kvm_s2_mmu 中，以减少复杂性并提高代码的可维护性。

#### 📝 邮件列表

1. **[04-15 09:38]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-16 00:05]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[04-16 11:50]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-24 20:45]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[04-29 17:31]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 11: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 22 Apr 2026 07:55:56 +0100

#### 🤖 AI 总结

在邮件讨论中，主题为“[PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive”的补丁旨在解决在嵌套VGIC状态转换时，IRQ 27（定时器中断）被停用导致的问题。历史讨论中，Marc Zyngier和Vishnu Pajjuri探讨了在不同层级的中断停用过程中可能出现的行为，Marc提出了对补丁的实现细节的疑问，尤其是关于ICC_DIR_EL1的处理。

在本周的新讨论中，Marc Zyngier询问了Vishnu的CPU是否实现了SEIS（ICC_CTLR_EL1.SEIS == 1），并指出在某些情况下可能会出现双重停用的情况，这在实现了SEIS的CPU上可能会导致错误。Marc还提供了一个补丁的修改建议，旨在避免在嵌套VGIC状态下进行物理中断的停用，以减少潜在问题。

总体来看，讨论集中在补丁的实现细节及其可能引发的边界情况，Marc继续寻求解决方案并提供了具体的代码修改建议。

#### 📝 邮件列表

1. **[04-22 07:55]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-22 20:27]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive
   - 发件人: Vishnu Pajjuri <vishnu@os.amperecomputing.com>
3. **[04-26 10:14]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-26 15:07]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-28 21:37]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Apr 2026 17:36:07 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“在用户空间中使用 irqchip 时从 WFI（Wait For Interrupt）唤醒”。Marc Zyngier 提出该补丁，指出用户空间 irqchip 支持在过去四年中一直存在问题，且未能在 PMU（Performance Monitoring Unit）中断时唤醒。Marc 认为这一特性应被移除，因为它在十年前的设计就是个糟糕的主意。

在之前的讨论中，Yao Yuan 提出了一个建议，创建一个新的辅助函数 `kvm_should_notify_us_irqchip()`，以简化代码并替换重复的部分。但 Marc 反对这一提议，认为引入辅助函数会使得补丁的回溯变得复杂，并且他有计划进一步简化与该特性相关的其他调用。

本周的新讨论中，Yao Yuan 表达了对 Marc 观点的认同，并感谢其详细解释，表明双方在该问题上的共识。整体来看，讨论集中在如何修复现有问题以及是否保留该特性上，最终倾向于简化处理而非引入新功能。

#### 📝 邮件列表

1. **[04-23 17:36]** [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-24 14:33]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
3. **[04-24 08:24]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-27 13:31]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>

---

### Thread 13: [PATCH] KVM: arm64: Handle permission faults with guest_memfd

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 30 Apr 2026 14:23:51 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: 处理 guest_memfd 的权限故障”，主要讨论了在 KVM 的 arm64 架构中如何处理与 guest_memfd 相关的权限故障。

**原始 patch/问题的内容**：
该 patch 旨在修复在处理权限故障时，gmem_abort() 函数的行为。具体来说，当存在有效的映射且仅修改权限时，kvm_pgtable_stage2_map() 不会进行更改，导致 KVM 返回到故障指令并可能陷入无限循环。该 patch 通过使用 kvm_pgtable_stage2_relax_perms() 来放宽权限，从而允许虚拟机继续执行。

**之前讨论要点**：
在历史讨论中，未有具体的邮件记录，但可以推测之前的讨论集中在如何更有效地处理权限故障以及对现有代码的潜在问题上。

**本周的新讨论、进展或结论**：
本周的讨论主要集中在对 patch 的细节审查上。Alexandru Elisei 提出了修复方案，Fuad Tabba 对代码中的一些细节提出了改进建议，包括初始化 memcache 变量和保持代码风格一致性。Alexandru 同意了这些建议，并表示会进行相应的修改。Fuad 也对 patch 进行了审核，表示已准备好接受这些修改。整体来看，本周的讨论推动了 patch 的完善，确保了代码的健壮性和一致性。

#### 📝 邮件列表

1. **[04-30 14:23]** [PATCH] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[04-30 15:48]** Re: [PATCH] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[05-01 15:18]** Re: [PATCH] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 14: [PATCH v6 0/2] KVM: arm64: Support FF-A direct messaging
 interfaces

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 01 May 2026 05:34:31 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中支持 FF-A（Firmware Framework for Arm）直接消息接口的补丁。

1. **原始补丁内容**：本次补丁集包含两个主要部分，分别是对 FFA_MSG_SEND_DIRECT_REQ 和 FFA_MSG_SEND_DIRECT_REQ2 的支持。补丁的目标是实现直接消息的发送，确保在处理过程中过滤掉框架消息，并对消息的有效性进行验证。

2. **之前的讨论要点**：在之前的讨论中，第二个补丁曾被删除，原因是用例不明确。然而，随着 TPM 设备在使用 pkvm 启动时的需求出现，补丁的用例变得清晰，因此重新提交了补丁。

3. **本周的新讨论与进展**：本周的讨论中，Per Larsen 和 Sebastian Ene 提交了补丁的最新版本（v6），并详细说明了各个补丁的修改内容。补丁经过测试，能够在 QEMU 中成功启动 Android。补丁的关键更新包括对消息发送者的验证、框架消息的过滤以及对 FF-A 1.2 版本的支持。所有补丁均已获得 Yeoreum Yun 的审核通过。

总的来说，本周的讨论集中在补丁的细节修改和测试结果上，推动了 FF-A 直接消息接口的实现进程。

#### 📝 邮件列表

1. **[05-01 05:34]** [PATCH v6 0/2] KVM: arm64: Support FF-A direct messaging
 interfaces
   - 发件人: Per Larsen via B4 Relay <devnull+perlarsen.google.com@kernel.org>
2. **[05-01 05:34]** [PATCH v6 1/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ in host
 handler
   - 发件人: Per Larsen via B4 Relay <devnull+perlarsen.google.com@kernel.org>
3. **[05-01 05:34]** [PATCH v6 2/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ2 in
 host handler
   - 发件人: Per Larsen via B4 Relay <devnull+perlarsen.google.com@kernel.org>

---

### Thread 15: [PATCH v5 0/2] KVM: arm64: Support FF-A direct messaging
 interfaces

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 30 Apr 2026 22:40:19 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构上支持 FF-A（Firmware Framework for Arm）直接消息接口的补丁（PATCH v5 0/2）。该补丁旨在增强 KVM 的功能，使其能够处理 FF-A 的直接消息传递。

在历史讨论中，补丁的具体内容和背景并未详细列出，但可以推测该补丁是基于之前的反馈进行的改进。参与者 Per Larsen 提到他在处理 v5 版本的反馈，并承认之前未能仔细阅读反馈和检查规范，导致了审查周期的浪费。

在本周的新讨论中，Yeoreum Yun 询问了补丁的进展情况，而 Per Larsen 则表示正在处理反馈，并对延迟回复表示歉意。此外，他提到将添加一个新的掩码，以检查发送者 ID 是否与 HOST_FFA_ID 匹配，以确保补丁的正确性。

总体来看，本周的讨论主要集中在补丁的进展和对之前反馈的响应上，显示出参与者对改进 KVM 功能的持续关注。

#### 📝 邮件列表

1. **[04-30 22:40]** Re: [PATCH v5 0/2] KVM: arm64: Support FF-A direct messaging
 interfaces
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[04-30 19:18]** Re: [PATCH v5 1/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ in
 host handler
   - 发件人: Per Larsen <perl@immunant.com>
3. **[04-30 19:30]** Re: [PATCH v5 0/2] KVM: arm64: Support FF-A direct messaging
 interfaces
   - 发件人: Per Larsen <perl@immunant.com>

---

### Thread 16: [PATCH v2 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 30 Apr 2026 16:02:39 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）的两个补丁，主要目的是修复 Endpoint Memory Access Descriptor（EMAD）偏移量计算的问题。

**原始补丁/问题内容**：
补丁系列旨在修复 EMAD 偏移量的计算，并为 FF-A 驱动和 pKVM 超级管理程序添加必要的边界检查。FF-A 规范在版本 1.1 之前未明确指定 EMAD 的偏移量，导致默认假设其紧随内存区域头部之后。版本 1.1 之后，规范要求使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。

**之前讨论要点**：
在补丁的 v1 版本中，pKVM 超级管理程序严格要求 EMAD 紧跟在内存区域头部之后，但这种假设与规范不符，因此在 v2 版本中移除了这一强制要求。

**本周的新讨论、进展或结论**：
本周的讨论中，Sebastian Ene 提交了补丁 v2，主要包括两个部分：
1. 更新 `arm_ffa` 驱动以正确计算 EMAD 偏移量，并添加边界检查，确保计算的偏移量不超过 `max_fragsize`。
2. 修改 pKVM 超级管理程序的验证逻辑，确保 EMAD 的偏移量在邮箱缓冲区的边界内，而不再假设其位置。

这些修改确保了驱动和超管程序的一致性，符合 FF-A 规范，避免了潜在的内存访问错误。

#### 📝 邮件列表

1. **[04-30 16:02]** [PATCH v2 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[04-30 16:02]** [PATCH v2 1/2] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[04-30 16:02]** [PATCH v2 2/2] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 17: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri,  1 May 2026 11:44:48 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下如何将 FFA_NOTIFICATION* 调用转发至 TrustZone 的补丁（patch）。该补丁的主要目的是移除 pKVM FF-A 代理中的 FFA_NOTIFICATION* 调用的阻止列表，以便能够使用 Arm FF-A 规范中定义的异步信号机制与安全服务进行通信。

在之前的讨论中，虽然没有具体的历史邮件记录，但可以推测出，阻止这些调用的原因主要是出于安全考虑，担心可能存在虚拟机 ID 欺骗或内存安全问题。然而，补丁的作者 Sebastian Ene 提出，当前的设置中，主机作为唯一的非安全端点，且 FFA_NOTIFICATION* 调用仅通过寄存器参数传递 VM ID 和 VCPU ID 等信息，不涉及内存地址，因此转发这些调用不会引发安全隐患。

本周的新讨论中，Sebastian Ene 提交了该补丁，并详细解释了移除阻止的理由，强调了主机的安全性和调用机制的安全性。补丁已在代码中进行了相应修改，删除了对 FFA_NOTIFICATION* 调用的限制。

#### 📝 邮件列表

1. **[05-01 11:44]** [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 18: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 30 Apr 2026 10:37:24 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的时钟功能进行加固的补丁。补丁的主要内容是针对 `trace_clock_update()` 函数中可能出现的除零和越界位移问题进行基本的检查，以避免在主机出现故障时导致时钟值不同步。

在之前的讨论中并没有相关的历史邮件，因此本周的讨论是首次提出的。Mostafa Saleh 提出了这个补丁，指出虽然时钟更新来自不可信的源，但仍需进行基本的有效性检查，以确保系统的稳定性。补丁通过在 `trace_clock_update()` 函数中添加了对 `mult` 和 `shift` 参数的检查，确保它们在合理范围内，避免潜在的错误。

本周的进展是补丁已被提交，并包含了具体的代码修改，增加了三行代码以实现上述检查。这一改动旨在提升 KVM 的安全性和可靠性。

#### 📝 邮件列表

1. **[04-30 10:37]** [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

## 📌 RFC

共 7 个 thread

---

### Thread 1: [RFC PATCH v2 00/28] KVM: s390: Introduce arm64 KVM - using symlinks

**📧 邮件数**: 29 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 28 Apr 2026 18:04:57 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 159518 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:29, 118355 tokens)

#### 📝 邮件列表

1. **[04-28 18:04]** [RFC PATCH v2 00/28] KVM: s390: Introduce arm64 KVM - using symlinks
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[04-28 18:04]** [RFC PATCH v2 01/28] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[04-28 18:04]** [RFC PATCH v2 02/28] KVM, vfio: remove symbol_get(kvm_get_kvm_safe) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[04-28 18:05]** [RFC PATCH v2 03/28] KVM, vfio: remove symbol_get(kvm_put_kvm) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[04-28 18:05]** [RFC PATCH v2 04/28] arm64: Provide arm64 UAPI for s390 host architecture
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[04-28 18:05]** [RFC PATCH v2 05/28] arm64: Extract sysreg definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[04-28 18:05]** [RFC PATCH v2 06/28] arm64: Provide arm64 API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[04-28 18:05]** [RFC PATCH v2 07/28] KVM: arm64: Provide arm64 KVM API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[04-28 18:05]** [RFC PATCH v2 08/28] arm64: Extract pstate definitions from ptrace
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[04-28 18:05]** [RFC PATCH v2 09/28] KVM: arm64: Share kvm_emulate definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[04-28 18:05]** [RFC PATCH v2 10/28] KVM: arm64: Make some arm64 KVM code shareable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[04-28 18:05]** [RFC PATCH v2 11/28] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[04-28 18:05]** [RFC PATCH v2 12/28] KVM: arm64: Share reset general register code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[04-28 18:05]** [RFC PATCH v2 13/28] KVM: arm64: Extract & share ipa size shift calculation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[04-28 18:05]** [RFC PATCH v2 14/28] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[04-28 18:05]** [RFC PATCH v2 15/28] MAINTAINERS: Add Steffen as reviewer for KVM/arm64
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[04-28 18:05]** [RFC PATCH v2 16/28] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[04-28 18:05]** [RFC PATCH v2 17/28] KVM: S390: Refactor gmap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[04-28 18:05]** [RFC PATCH v2 18/28] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[04-28 18:05]** [RFC PATCH v2 19/28] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[04-28 18:05]** [RFC PATCH v2 20/28] KVM: s390: Prepare kvm-s390 for a second kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[04-28 18:05]** [RFC PATCH v2 21/28] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[04-28 18:05]** [RFC PATCH v2 22/28] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[04-28 18:05]** [RFC PATCH v2 23/28] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[04-28 18:05]** [RFC PATCH v2 24/28] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[04-28 18:05]** [RFC PATCH v2 25/28] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[04-28 18:05]** [RFC PATCH v2 26/28] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[04-28 18:05]** [RFC PATCH v2 27/28] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[04-28 18:05]** [RFC PATCH v2 28/28] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 2: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM

**📧 邮件数**: 24 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 23 Apr 2026 12:20:53 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 Linux 内核中重新调用 `ima_init()` 函数，以解决延迟初始化时 TPM（受信任的平台模块）未准备好的问题。原始的补丁（patch）提议在 `late_initcall_sync` 阶段再次调用 `ima_init()`，以确保 TPM 可用时再进行 IMA（Integrity Measurement Architecture）的初始化。

在历史讨论中，参与者们探讨了补丁的合理性和潜在问题。Yeoreum Yun 提到希望通过减少代码重复来优化 `init_ima_core` 的实现。Mimi Zohar 和 Paul Moore 质疑在 `late_initcall_sync` 阶段初始化 IMA 是否安全，并强调需要确保 TPM 可用性。Paul 还提出了使用 LSM 通知机制来同步 TPM 状态的想法。

在本周的新讨论中，Paul 和其他参与者继续探讨如何在不重复初始化的情况下解决 IMA 和 TPM 之间的依赖问题。Yeoreum 表示，虽然 LSM 通知机制可能有助于解决问题，但需要明确区分 TPM 存在与否的情况。Roberto Sassu 强调，任何解决方案都应避免多次尝试初始化 IMA，而应建立有效的同步机制，以确保系统的稳定启动。

总体来看，讨论围绕如何安全有效地处理 IMA 和 TPM 的初始化顺序展开，参与者们对补丁的实现细节和潜在影响进行了深入的探讨。

#### 📝 邮件列表

1. **[04-23 12:20]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[04-23 13:34]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[04-23 13:53]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
4. **[04-23 09:43]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
5. **[04-23 14:55]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[04-23 15:03]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
7. **[04-23 15:33]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[04-23 14:01]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
9. **[04-23 19:13]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
10. **[04-23 21:27]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
11. **[04-24 06:57]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
12. **[04-24 16:15]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
13. **[04-24 16:57]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
14. **[04-24 17:08]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
15. **[04-24 18:00]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
16. **[04-24 18:10]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
17. **[04-24 18:49]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
18. **[04-25 05:53]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
19. **[04-27 21:31]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
20. **[04-27 21:31]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
21. **[04-28 14:21]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
22. **[04-29 15:33]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Roberto Sassu <roberto.sassu@huaweicloud.com>
23. **[04-29 20:36]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
24. **[04-29 20:43]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>

---

### Thread 3: [RFC PATCH v4 00/16] coco/TSM: Implement host-side support for Arm CCA TDISP setup

**📧 邮件数**: 17 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 27 Apr 2026 14:23:28 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于实现 Arm CCA TDISP 设置的主机端支持的补丁系列（RFC PATCH v4 00/16）。该补丁系列主要涉及 Realm 虚拟设备（vdev）对象的创建与管理、设备认证请求的服务以及 KVM/RMM 流程的完成。

**原始补丁/问题内容**：
补丁系列实现了主机端的更改，以支持 Arm CCA TDISP 的端到端设置。主要功能包括：
- 主机端的 vdev 通信和生命周期管理
- 主机处理 RHI DA 对象的读取和大小请求
- KVM 处理 vdev 请求的退出和映射验证

**之前讨论要点**：
在历史讨论中，补丁经历了多次更新，主要是根据 RMM 2.0bet1 规范进行调整，并对 vdev 请求的处理进行了重构。参与者们讨论了补丁的依赖关系和实现细节，确保与现有系统的兼容性。

**本周的新讨论、进展或结论**：
本周的讨论集中在补丁的具体实现上，包括对 vdev 状态转换、设备内存映射的处理，以及如何在设备映射时处理错误。补丁还增加了对设备测量和接口报告的支持，允许客人请求最新的设备状态。此外，补丁启用了在创建 Realm 时的 DA 功能，以增强设备的安全性和功能性。参与者们对补丁的细节进行了深入探讨，确保其在 KVM 环境中的有效性和稳定性。

#### 📝 邮件列表

1. **[04-27 14:23]** [RFC PATCH v4 00/16] coco/TSM: Implement host-side support for Arm CCA TDISP setup
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[04-27 14:23]** [RFC PATCH v4 01/16] iommu/arm-smmu-v3: Discover RME support and realm IRQ topology
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[04-27 14:23]** [RFC PATCH v4 02/16] iommu/arm-smmu-v3: Save the programmed MSI message in msi_desc
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[04-27 14:23]** [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm viommu plumbing
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[04-27 14:23]** [RFC PATCH v4 04/16] iommu/arm-smmu-v3: Track realm pSMMU users with refcount_t
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[04-27 14:23]** [RFC PATCH v4 05/16] coco: host: arm64: Add support for virtual device communication
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[04-27 14:23]** [RFC PATCH v4 06/16] coco: host: arm64: Add support for RMM vdev objects
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[04-27 14:23]** [RFC PATCH v4 07/16] coco: host: arm64: Add pdev stream key refresh and purge helpers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[04-27 14:23]** [RFC PATCH v4 08/16] coco: host: arm64: Add helpers to unlock and destroy RMM vdev
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[04-27 14:23]** [RFC PATCH v4 09/16] coco: host: arm64: Add support for da object read RHI handling
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[04-27 14:23]** [RFC PATCH v4 10/16] coco: host: arm64: Add helper for cached object fetches
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[04-27 14:23]** [RFC PATCH v4 11/16] coco: host: arm64: Fetch interface report via RMI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
13. **[04-27 14:23]** [RFC PATCH v4 12/16] coco: host: arm64: Fetch device measurements via RMI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
14. **[04-27 14:23]** [RFC PATCH v4 13/16] coco: host: KVM: arm64: Handle vdev validate-mapping exits
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
15. **[04-27 14:23]** [RFC PATCH v4 14/16] KVM: arm64: Unmap device mappings when a private granule is destroyed
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
16. **[04-27 14:23]** [RFC PATCH v4 15/16] coco: host: arm64: Transition vdevs to TDISP RUN state
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
17. **[04-27 14:23]** [RFC PATCH v4 16/16] KVM: arm64: CCA: enable DA in realm create parameters
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

### Thread 4: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks

**📧 邮件数**: 15 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 27 Apr 2026 12:21:07 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于 ARM CCA IDE 设置的补丁系列，主要通过连接/断开回调实现主机端的支持。该补丁系列包含了多个关键功能，包括设备特性检测、TSM 回调连接、RMM pdev 描述符的创建与注册、设备公钥的处理等。

在历史讨论中，补丁的背景和依赖关系被明确，特别是与 RMM 2.0bet1 规范的对接，以及与 KVM CCA 补丁集的依赖。之前的讨论主要集中在如何优化主机端 pdev 生命周期管理，以更好地符合 RMM 规范的流程。

本周的新讨论中，补丁的具体实现细节被逐步展开。Aneesh Kumar K.V 提出了多个补丁，包括：
1. 增加了 RMM 设备通信的辅助函数。
2. 实现了 RMM pdev 的停止和销毁功能。
3. 引入了 X.509 证书解析的公共接口，以支持 PCI 设备认证。
4. 增强了对 IDE 流的支持，包括非一致性流和根端口 pdev 的引用计数管理。

此外，补丁还处理了设备间的流连接和断开，确保在 IDE 设备的流管理中，根端口 pdev 在流连接期间保持有效。整体来看，讨论强调了补丁在 ARM CCA 环境下的适应性和灵活性，允许设备在没有 DOE 邮箱的情况下继续初始化。

#### 📝 邮件列表

1. **[04-27 12:21]** [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[04-27 12:21]** [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback and IDE stream allocation support
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[04-27 12:21]** [RFC PATCH v4 02/14] coco: host: arm64: Create RMM pdev objects for PCI endpoints
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[04-27 12:21]** [RFC PATCH v4 03/14] coco: host: arm64: Add RMM device communication helpers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[04-27 12:21]** [RFC PATCH v4 04/14] coco: host: arm64: Add helper to stop and tear down an RMM pdev
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[04-27 12:21]** [RFC PATCH v4 05/14] X.509: Make certificate parser public
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[04-27 12:21]** [RFC PATCH v4 06/14] X.509: Parse Subject Alternative Name in certificates
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[04-27 12:21]** [RFC PATCH v4 07/14] X.509: Move certificate length retrieval into new helper
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[04-27 12:21]** [RFC PATCH v4 08/14] coco: host: arm64: Register device public key with RMM
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[04-27 12:21]** [RFC PATCH v4 09/14] coco: host: arm64: Initialize RMM pdev state for TDISP IDE connect
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[04-27 12:21]** [RFC PATCH v4 10/14] coco: host: arm64: Coordinate peer stream waits during pdev communication
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[04-27 12:21]** [RFC PATCH v4 11/14] coco: host: arm64: Connect RMM pdev streams for IDE devices
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
13. **[04-27 12:21]** [RFC PATCH v4 12/14] coco: host: arm64: Refcount root-port pdevs used by IDE streams
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
14. **[04-27 12:21]** [RFC PATCH v4 13/14] PCI/TSM: Move CMA DOE mailbox discovery out of pci_tsm_pf0_constructor()
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
15. **[04-27 12:21]** [RFC PATCH v4 14/14] coco: host: arm64: Add NCOH_SYS stream support for RC endpoints
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

### Thread 5: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for Live
 Update

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 28 Apr 2026 22:29:40 +0000

#### 🤖 AI 总结

本邮件讨论主题为“KVM: 孤立虚拟机的照管者方法以实现实时更新”，主要提出了一种新的架构设计，旨在减少主机内核重启时对虚拟机的影响。

1. **原始问题/补丁内容**：该提案旨在通过引入一个名为“照管者”的组件，使孤立虚拟机在主机内核重启期间继续执行，避免虚拟机的停顿，从而实现零停机时间的维护。

2. **之前讨论要点**：在历史讨论中，参与者们探讨了如何在不影响虚拟机执行的情况下，管理主机内核的重启。提案强调了照管者的设计，旨在使虚拟机在主机重启时保持运行状态，减少停机时间。

3. **本周的新讨论与进展**：本周的讨论集中在照管者的架构、ABI设计及其安全性上。参与者提出了照管者作为独立子系统或内核模块的不同实现方式，并讨论了如何在不影响主机内核的情况下进行状态序列化和恢复。还有人建议在设计中考虑地址空间隔离，以增强安全性。此外，针对如何处理虚拟机之间的中断和时间管理问题，参与者们提出了多种解决方案和优化建议。

总体而言，讨论围绕照管者的设计及其在实时更新中的作用展开，强调了在实现过程中需要考虑的安全性和可扩展性问题。

#### 📝 邮件列表

1. **[04-28 22:29]** [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for Live
 Update
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
2. **[04-29 10:13]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Alexander Graf <graf@amazon.com>
3. **[04-29 09:40]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: David Woodhouse <dwmw2@infradead.org>
4. **[04-29 16:02]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
5. **[04-29 16:13]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
6. **[04-30 15:28]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
7. **[04-30 16:27]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: David Woodhouse <dwmw2@infradead.org>
8. **[05-01 05:32]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
9. **[05-01 09:56]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: David Woodhouse <dwmw2@infradead.org>
10. **[05-01 21:48]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
11. **[05-01 22:07]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
12. **[05-03 18:57]** Re: [RFC] proposal: KVM: Orphaned VMs: The Caretaker approach for
 Live Update
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

### Thread 6: [RFC PATCH v4 00/11] coco/TSM: Arm CCA guest TDISP lock/accept flow with verification and DMA enable

**📧 邮件数**: 12 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 27 Apr 2026 13:57:54 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于 Arm CCA（可信计算架构）客体的补丁系列，主要涉及 TDISP（可信设备接口）锁定和接受流程的实现，以及 DMA（直接内存访问）启用的相关工作。

**原始补丁内容**：该补丁系列实现了 TSM（TEE 安全管理器）相关的锁定、解锁和接受回调，以支持 Arm CCA 的 TDISP 设置。补丁包括了客体侧的 DA（数据证明）管道，确保设备在 TDI 锁定和运行状态之间的过渡，验证主机提供的证据，并在认证成功后启用 DMA。

**之前讨论要点**：补丁基于 RMM 2.0bet1 规范，更新了客体侧的 DA 代码，修复了 Kconfig 中的拼写错误，并添加了 RHI（Realm Host Interface）和 DA 辅助函数，以支持设备状态转换和对象刷新。

**本周新讨论和进展**：
1. **补丁更新**：本周的补丁更新包括对 TDI 状态转换的支持、接口报告缓存的刷新、测量请求的实现，以及对 DA 证据的验证。
2. **DMA 行为调整**：更新了接受设备的 DMA 行为，确保它们仅访问私有内存，并避免使用共享内存路径。
3. **接受回调实现**：实现了 TSM 接受回调，确保在设备通过认证后，正确分配和注册保护的 MMIO 范围，并将 TDI 状态转换为运行状态。

整体来看，本周的讨论集中在补丁的细节实现和对 DMA 行为的调整上，进一步推动了 Arm CCA 的功能完善。

#### 📝 邮件列表

1. **[04-27 13:57]** [RFC PATCH v4 00/11] coco/TSM: Arm CCA guest TDISP lock/accept flow with verification and DMA enable
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[04-27 13:57]** [RFC PATCH v4 01/11] coco: guest: arm64: Guest TSM callback and realm device lock support
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[04-27 13:57]** [RFC PATCH v4 02/11] coco: guest: arm64: Fix a typo in the ARM_CCA_GUEST Kconfig help string ("and" -> "an").
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[04-27 13:57]** [RFC PATCH v4 03/11] coco: guest: arm64: Add Realm Host Interface and guest DA helper
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[04-27 13:57]** [RFC PATCH v4 04/11] coco: guest: arm64: Support guest-initiated TDI lock/unlock transitions
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[04-27 13:57]** [RFC PATCH v4 05/11] coco: guest: arm64: Refresh interface-report cache during device lock
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[04-27 13:58]** [RFC PATCH v4 06/11] coco: guest: arm64: Add measurement refresh via RHI_DA_VDEV_GET_MEASUREMENTS
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[04-27 13:58]** [RFC PATCH v4 07/11] coco: guest: arm64: Add guest APIs to read host-cached DA objects
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[04-27 13:58]** [RFC PATCH v4 08/11] coco: guest: arm64: Verify DA evidence with RSI_VDEV_GET_INFO digests
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[04-27 13:58]** [RFC PATCH v4 09/11] coco: guest: arm64: Hook TSM accept to Realm TDISP RUN transition
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[04-27 13:58]** [RFC PATCH v4 10/11] coco: arm64: dma: Update force_dma_unencrypted for accepted devices
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[04-27 13:58]** [RFC PATCH v4 11/11] coco: guest: arm64: Enable vdev DMA after attestation
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>

---

### Thread 7: [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue

**📧 邮件数**: 10 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 24 Apr 2026 14:23:45 +0100

#### 🤖 AI 总结

本邮件讨论的主题是修复 IMA（Integrity Measurement Architecture）与 TPM（Trusted Platform Module）初始化顺序问题的补丁系列。历史讨论中，Jonathan McDowell 提出了一个补丁系列，旨在通过在 late_initcall_sync 阶段初始化 IMA，解决 TPM 在 IMA 初始化时未完全注册的问题，从而避免 IMA 无法正确扩展 TPM 测量的情况。

在本周的新讨论中，Mimi Zohar 提出了一个补丁，旨在调试延迟初始化调用的测量记录，并询问在将 IMA 初始化推迟到 late_initcall_sync 时，可能缺失多少记录。Yeoreum Yun 反馈了测试结果，确认在 boot_aggregate 和 boot_aggregate_late 之间没有测量日志，除了可以忽略的内核版本记录。Mimi 和 Paul Moore 讨论了 TPM 初始化的顺序问题，指出 TPM 的初始化通常在 device_initcall 阶段进行，但在某些情况下可能会被推迟，这可能导致 IMA 在 TPM 尚未准备好时运行，从而进入旁路模式。

总体而言，讨论围绕如何确保 IMA 和 TPM 的初始化顺序，以避免潜在的测量记录丢失，参与者们对不同架构的测试结果表示关注，并希望进一步验证补丁的安全性和有效性。

#### 📝 邮件列表

1. **[04-24 14:23]** [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue
   - 发件人: Jonathan McDowell <noodles@earth.li>
2. **[04-29 16:01]** [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
3. **[04-30 10:48]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[04-30 17:39]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
5. **[04-30 18:35]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
6. **[04-30 21:51]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
7. **[05-01 12:52]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: David Safford <david.safford@gmail.com>
8. **[05-03 07:36]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
9. **[05-03 08:42]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
10. **[05-03 12:46]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #1

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 24 Apr 2026 16:14:43 +0100

#### 🤖 AI 总结

本邮件线程讨论了 KVM/arm64 在 7.1 版本中的修复补丁。历史讨论中，Marc Zyngier 提出了第一批 KVM/arm64 的修复补丁，主要针对 idreg 处理、长期存在的回归问题、SMCCC 合规性等进行了修复，并附带了一些清理工作。Marc 邀请 Paolo 进行合并，并表示详细信息已在邮件中提供。

在本周的新讨论中，Paolo Bonzini 对 Marc 的补丁进行了确认，表示已成功合并，并感谢 Marc 的工作。这表明补丁已获得认可并进入了代码库。

总结而言，此次讨论主要围绕 KVM/arm64 的修复补丁，历史讨论中提出了多项修复点，而本周的进展则是确认了补丁的合并，标志着修复工作的顺利推进。

#### 📝 邮件列表

1. **[04-24 16:14]** [GIT PULL] KVM/arm64 fixes for 7.1, take #1
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-27 10:25]** Re: [GIT PULL] KVM/arm64 fixes for 7.1, take #1
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Discussion

共 2 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: add wfx test case

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 01 May 2026 15:21:19 +0100

#### 🤖 AI 总结

本邮件主题为“[kvm-unit-tests PATCH] arm: add wfx test case”，主要讨论了在 KVM 单元测试中添加针对 ARM 体系结构的 WFx 测试用例。

在本周的新讨论中，参与者 Alexandru Elisei 提到，他正在使用 kvm-unit-test 来验证 QEMU 对指令的 TCG（翻译块生成）建模。他引用了之前的补丁系列（PATCH v4 0/7），该补丁旨在全面建模 ARM A-profile 的 WFxT 指令。虽然他对当前的建模表示信心（因为它基本上被视为 NOP），但他希望确认在不同模式下的行为是否符合预期。

本周的讨论主要集中在如何确保测试的准确性，尤其是在 KVM 环境下可能出现的失败情况。Alexandru 表示可以将测试限制在 TCG 模式，以便更好地分析和验证指令的行为。

总结来说，本周的讨论延续了对 WFx 测试用例的关注，强调了对指令建模的验证工作，以及在不同执行环境下的测试策略。

#### 📝 邮件列表

1. **[05-01 15:21]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: =?utf-8?Q?Alex_Benn=C3=A9e?= <alex.bennee@linaro.org>

---

### Thread 2: [kvm-unit-tests PATCH] arm: add wfx test case

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 28 Apr 2026 15:56:33 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM 单元测试中为 ARM 架构添加 WFX 测试用例的补丁（patch）。本周的讨论主要集中在补丁的内容及其扩展可能性。

原始补丁的目的是在 KVM 单元测试中引入 WFX 测试用例，以验证 ARM 架构下的相关功能。由于邮件列表中没有历史讨论的记录，因此我们无法提供之前讨论的具体要点。

在本周的新讨论中，参与者 Joey Gouly 对补丁表示认可，并提出了一个建议：理想情况下，应该扩展测试用例，使其能够与 SMP（对称多处理）一起工作，从而更全面地测试相关代码路径。对此，另一位参与者 Alex Bennée 表示赞同，认为这个建议是可行的。

总结来看，本周的讨论主要围绕补丁的实施及其扩展方向展开，参与者们对补丁的基本内容表示支持，并探讨了进一步提升测试覆盖率的可能性。

#### 📝 邮件列表

1. **[04-28 15:56]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: =?utf-8?Q?Alex_Benn=C3=A9e?= <alex.bennee@linaro.org>

---

## 📌 Other

共 3 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: add wfx test case

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 27 Apr 2026 14:00:45 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM 架构的 KVM 单元测试补丁，主题为“添加 WFX 测试用例”。该补丁由 Alex Bennée 提出，旨在实现对 WFI、WFE、WFIT 和 WFET 指令的测试，利用 KVM 单元测试的基础设施来处理 GIC 和中断。

在历史讨论中，补丁的内容包括新增的 `wfx.c` 测试文件，以及对相关头文件和配置文件的修改，整体增加了 153 行代码。补丁的核心是测试 WFX 指令的功能，确保它们在不同条件下的正确性。

本周的新讨论中，参与者 Joey Gouly 提出了对补丁的几个小建议，包括使用动态计算的超时值替代硬编码的超时值，并建议在代码中添加注释以说明测试目的。此外，他还建议在处理中断时采用更灵活的方式，以便测试可以在不同的异常级别下运行。

Alex Elisei 也对补丁提出了意见，指出在中断处理时应确保正确的中断确认，以避免在 KVM 环境中可能出现的 WFI 和 WFE 指令的潜在问题。他提到，KVM 可能不会捕获 WFI 指令，这可能导致测试失败。

总的来说，本周的讨论集中在补丁的细节改进和潜在的实现问题上，参与者们积极提供反馈以提高补丁的质量。

#### 📝 邮件列表

1. **[04-27 14:00]** [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: =?UTF-8?q?Alex=20Benn=C3=A9e?= <alex.bennee@linaro.org>
2. **[04-28 14:26]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: Joey Gouly <joey.gouly@arm.com>
3. **[05-01 14:15]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 2: [kvm-unit-tests PATCH v2 0/7] arm64: Add Stage-2 MMU and Nested Guest Framework

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 13 Apr 2026 13:46:23 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 Stage-2 MMU 和嵌套客人框架的补丁系列，旨在为测试高级虚拟化特性（如嵌套虚拟化和 GICv4 直接中断注入）提供轻量级基础设施。

在历史讨论中，Jing Zhang 提出了一个补丁系列，包含七个补丁，介绍了一个支持多种翻译粒度（4K、16K、64K）和动态页表管理的通用 Stage-2 MMU 库。此外，还增加了一个处理客人生命周期的执行框架，以及一个新的测试用例，用于验证 Stage-2 MMU 的故障处理能力，确保虚拟机监控程序能够正确识别和处理由客人访问未映射内存引发的 Stage-2 数据中止。

在本周的新讨论中，Wei-Lin Chang 对补丁 7 提出了进一步的建议，指出在 Stage-2 中，4K 粒度的支持并不保证，因此在创建 Stage-2 MMU 之前应检查 ID_AA64MMFR0_EL1.TGran*_2 的值。此外，他还提到，客人 VTCR_EL2.T0SZ 的最小值受实现的物理地址范围限制，因此在 s2mmu_enable() 函数中，仅通过 64 - VA_BITS 计算可能会生成不支持的 T0SZ。

总结来看，讨论围绕补丁的有效性和兼容性展开，强调了在实现过程中需要注意的细节。

#### 📝 邮件列表

1. **[04-13 13:46]** [kvm-unit-tests PATCH v2 0/7] arm64: Add Stage-2 MMU and Nested Guest Framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[04-13 13:46]** [kvm-unit-tests PATCH v2 7/7] arm64: Add Stage-2 MMU demand paging test
   - 发件人: Jing Zhang <jingzhangos@google.com>
3. **[04-29 15:47]** Re: [kvm-unit-tests PATCH v2 7/7] arm64: Add Stage-2 MMU demand
 paging test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 3: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to match Linux kernel

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 22 Apr 2026 14:08:20 +0100

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于对 KVM 单元测试的一个补丁，旨在更新 ARM64 架构中 ESR_ELx 的定义，以与 Linux 内核保持一致。该补丁由 Joey Gouly 提出，主要目的是支持 EL2 级别的 MMU 系列操作，将 ESR_EL1* 的名称替换为 ESR_ELx，以确保一致性。

在历史讨论中，Joey 提到该补丁是为了配合 EL2 阶段的 MMU 系列，且补丁内容是从 Linux 内核的相关头文件中复制而来。邮件中还提到该补丁是对之前补丁的替代。

在本周的新讨论中，Jing Zhang 对该补丁进行了审查，并表示已审核通过。这表明补丁得到了认可，可能会在后续的开发中被采纳。

总体来看，本周的讨论进展顺利，补丁得到了审查者的支持，为后续的合并奠定了基础。

#### 📝 邮件列表

1. **[04-22 14:08]** [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to match Linux kernel
   - 发件人: Joey Gouly <joey.gouly@arm.com>
2. **[04-29 15:53]** Re: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to
 match Linux kernel
   - 发件人: Jing Zhang <jingzhangos@google.com>

---

