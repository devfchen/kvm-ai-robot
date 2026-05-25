# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-05-25 00:52:39

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 369
- **总 Thread 数**: 40
- **大型 Thread** (>20封): 5 个

### 分类分布

- **PATCH**: 33 threads (337 邮件)
- **RFC**: 3 threads (22 邮件)
- **Bug Report**: 1 threads (5 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Discussion**: 2 threads (3 邮件)

---

## 📌 PATCH

共 33 个 thread

---

### Thread 1: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 60 | **👥 参与者**: 5 | **📅 开始时间**: Wed, 13 May 2026 14:17:08 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的 KVM 中支持 Arm CCA（保密计算架构）的补丁系列（PATCH v14 00/44）。该补丁旨在实现受保护虚拟机的运行，主要更新包括使用主机的页面大小、简化的用户 API 以及通过系统寄存器传递 GIC 状态等。

在历史讨论中，补丁的背景和主要变更被详细阐述，包括 RMM（Realm Management Monitor）功能的实现、内存委托和未委托的处理、以及对 Granule Protection Faults 的支持等。补丁的多个版本经过多次修改，逐步完善了对 RMM v2.0-bet1 规范的适配。

在本周的新讨论中，参与者针对补丁中的具体实现提出了一系列问题和建议。例如，Gavin Shan 指出补丁中某些定义与现有规范不一致，Aneesh Kumar K.V 则建议对函数命名进行更改以提高可读性。此外，Marc Zyngier 也对补丁的整体结构和代码一致性提出了改进意见。总体来看，讨论集中在确保补丁的准确性和符合最新规范上，参与者们积极交流以推动补丁的进一步完善。

#### 📝 邮件列表

1. **[05-13 14:17]** [PATCH v14 00/44] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[05-13 14:17]** [PATCH v14 01/44] kvm: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Steven Price <steven.price@arm.com>
3. **[05-13 14:17]** [PATCH v14 02/44] kvm: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Steven Price <steven.price@arm.com>
4. **[05-13 14:17]** [PATCH v14 03/44] arm64: RME: Handle Granule Protection Faults (GPFs)
   - 发件人: Steven Price <steven.price@arm.com>
5. **[05-13 14:17]** [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Steven Price <steven.price@arm.com>
6. **[05-13 14:17]** [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
7. **[05-13 14:17]** [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
8. **[05-13 14:17]** [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's page size
   - 发件人: Steven Price <steven.price@arm.com>
9. **[05-13 14:17]** [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Steven Price <steven.price@arm.com>
10. **[05-13 14:17]** [PATCH v14 09/44] arm64: RMI: Provide functions to delegate/undelegate ranges of memory
   - 发件人: Steven Price <steven.price@arm.com>
11. **[05-13 14:17]** [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
12. **[05-13 14:17]** [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Steven Price <steven.price@arm.com>
13. **[05-13 14:17]** [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
14. **[05-13 14:17]** [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>
15. **[05-13 14:17]** [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Steven Price <steven.price@arm.com>
16. **[05-13 14:17]** [PATCH v14 37/44] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Steven Price <steven.price@arm.com>
17. **[05-18 17:08]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Gavin Shan <gshan@redhat.com>
18. **[05-19 11:05]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
19. **[05-19 11:25]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT
 entries for memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
20. **[05-19 11:32]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
21. **[05-19 12:01]** Re: [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating
 a realm.
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
22. **[05-19 12:24]** Re: [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
23. **[05-19 15:10]** Re: [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
24. **[05-19 15:32]** Re: [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
25. **[05-19 11:13]** Re: [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
26. **[05-19 15:55]** Re: [PATCH v14 37/44] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
27. **[05-19 18:25]** Re: [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
28. **[05-19 14:06]** Re: [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
29. **[05-20 17:01]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Steven Price <steven.price@arm.com>
30. **[05-21 10:21]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Gavin Shan <gshan@redhat.com>
31. **[05-21 10:39]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
32. **[05-21 10:51]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's
 page size
   - 发件人: Gavin Shan <gshan@redhat.com>
33. **[05-21 10:58]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Gavin Shan <gshan@redhat.com>
34. **[05-21 14:38]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
35. **[05-21 11:19]** Re: [PATCH v14 01/44] kvm: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Marc Zyngier <maz@kernel.org>
36. **[05-21 11:26]** Re: [PATCH v14 02/44] kvm: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Marc Zyngier <maz@kernel.org>
37. **[05-21 13:25]** Re: [PATCH v14 03/44] arm64: RME: Handle Granule Protection Faults (GPFs)
   - 发件人: Marc Zyngier <maz@kernel.org>
38. **[05-21 13:40]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Marc Zyngier <maz@kernel.org>
39. **[05-21 13:49]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Marc Zyngier <maz@kernel.org>
40. **[05-21 14:02]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Marc Zyngier <maz@kernel.org>
41. **[05-21 14:30]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's page size
   - 发件人: Marc Zyngier <maz@kernel.org>
42. **[05-21 14:47]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Marc Zyngier <maz@kernel.org>
43. **[05-21 14:59]** Re: [PATCH v14 09/44] arm64: RMI: Provide functions to delegate/undelegate ranges of memory
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[05-21 15:24]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[05-21 15:35]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[05-21 15:50]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
47. **[05-21 15:53]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's
 page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
48. **[05-21 16:11]** Re: [PATCH v14 02/44] kvm: arm64: Avoid including linux/kvm_host.h in
 kvm_pgtable.h
   - 发件人: Steven Price <steven.price@arm.com>
49. **[05-21 16:11]** Re: [PATCH v14 01/44] kvm: arm64: Include kvm_emulate.h in
 kvm/arm_psci.h
   - 发件人: Steven Price <steven.price@arm.com>
50. **[05-21 16:15]** Re: [PATCH v14 03/44] arm64: RME: Handle Granule Protection Faults
 (GPFs)
   - 发件人: Steven Price <steven.price@arm.com>
51. **[05-21 16:33]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Steven Price <steven.price@arm.com>
52. **[05-21 16:39]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
53. **[05-21 16:44]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
54. **[05-21 16:44]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
55. **[05-21 16:44]** Re: [PATCH v14 05/44] arm64: RMI: Add wrappers for RMI calls
   - 发件人: Steven Price <steven.price@arm.com>
56. **[05-21 16:49]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
57. **[05-21 17:01]** Re: [PATCH v14 09/44] arm64: RMI: Provide functions to
 delegate/undelegate ranges of memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
58. **[05-21 23:36]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's
 page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
59. **[05-22 10:58]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Marc Zyngier <maz@kernel.org>
60. **[05-22 11:02]** Re: [PATCH v14 09/44] arm64: RMI: Provide functions to delegate/undelegate ranges of memory
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 40 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 21 May 2026 14:49:07 +0000

#### 🤖 AI 总结

本邮件线程讨论了对 KVM (Kernel-based Virtual Machine) 的 GICv5 (Generic Interrupt Controller v5) 的支持，特别是 IRS (Interrupt Routing Service) 的实现和相关的补丁。

1. **原始补丁/问题内容**：
   本次补丁系列（共39个补丁）旨在为 KVM 的 arm64 架构添加对 GICv5 IRS 的支持。补丁内容包括 IRS 的 MMIO 接口、虚拟中断状态表（IST）的管理、SPI（共享中断）和 LPI（本地中断）的处理等。

2. **之前讨论要点**：
   之前的讨论主要集中在 GICv5 的基本架构和对 PPIs（私有中断）的支持上。GICv5 的设计允许更灵活的中断管理，但在实现过程中需要确保与现有 KVM 结构的兼容性。

3. **本周的新讨论、进展或结论**：
   本周的讨论主要集中在补丁的具体实现和功能上，包括：
   - 引入 IRS 相关的 MMIO 处理函数，确保 KVM 能够正确处理 IRS 的状态和配置。
   - 增加了对 SPI 和 LPI 的支持，允许 KVM 通过 IRS 进行中断注入。
   - 讨论了在 VM 恢复时如何正确处理 IST 的保存和恢复，确保中断状态的一致性。
   - 介绍了 IRS 的 UAPI（用户空间 API），使用户能够设置 IRS 的基地址和 SPI 数量。
   - 详细描述了 IRS 的保存和恢复顺序，强调了在 VM 运行之前必须完成的步骤。

整体而言，这一系列补丁的目标是使 KVM 能够更好地支持 GICv5 的功能，特别是在中断管理和虚拟化方面的增强。

#### 📝 邮件列表

1. **[05-21 14:49]** [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[05-21 14:49]** [PATCH v2 01/39] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[05-21 14:49]** [PATCH v2 02/39] irqchip/gic-v5: Provide OF IRS config frame attrs to
 KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[05-21 14:50]** [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[05-21 14:50]** [PATCH v2 04/39] KVM: arm64: gic-v5: Define remaining IRS MMIO
 registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[05-21 14:50]** [PATCH v2 05/39] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[05-21 14:51]** [PATCH v2 06/39] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[05-21 14:51]** [PATCH v2 07/39] KVM: arm64: gic-v5: Extract host IRS caps from IRS
 config frame
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[05-21 14:51]** [PATCH v2 08/39] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[05-21 14:52]** [PATCH v2 09/39] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[05-21 14:52]** [PATCH v2 10/39] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[05-21 14:52]** [PATCH v2 11/39] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[05-21 14:53]** [PATCH v2 12/39] KVM: arm64: gic-v5: Keep GICv5 vCPU limit
 model-specific
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[05-21 14:53]** [PATCH v2 13/39] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[05-21 14:53]** [PATCH v2 14/39] KVM: arm64: gic-v5: Set up VMTEs and VPE doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[05-21 14:54]** [PATCH v2 15/39] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[05-21 14:54]** [PATCH v2 16/39] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[05-21 14:54]** [PATCH v2 17/39] KVM: arm64: gic-v5: Introduce struct vgic_v5_irs and
 IRS base address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[05-21 14:55]** [PATCH v2 18/39] KVM: arm64: gic-v5: Add IRS IODEV support to MMIO
 handlers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
20. **[05-21 14:55]** [PATCH v2 19/39] KVM: arm64: gic-v5: Add KVM_VGIC_V5_ADDR_TYPE_IRS to
 UAPI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
21. **[05-21 14:55]** [PATCH v2 20/39] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
22. **[05-21 14:56]** [PATCH v2 21/39] KVM: arm64: gic-v5: Initialise per-VM IRS state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[05-21 14:56]** [PATCH v2 22/39] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[05-21 14:57]** [PATCH v2 23/39] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[05-21 14:57]** [PATCH v2 24/39] KVM: arm64: selftests: Update vGICv5 selftest to set
 IRS address
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[05-21 14:57]** [PATCH v2 25/39] KVM: arm64: gic-v5: Introduce SPI AP list
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[05-21 14:58]** [PATCH v2 26/39] KVM: arm64: gic-v5: Add GIC VDPEND and GIC VDRCFG
 hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[05-21 14:58]** [PATCH v2 27/39] KVM: arm64: gic-v5: Track SPI state for in-flight
 SPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[05-21 14:58]** [PATCH v2 28/39] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[05-21 14:59]** [PATCH v2 29/39] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
31. **[05-21 14:59]** [PATCH v2 30/39] Documentation: KVM: Extend VGICv5 docs for
 KVM_VGIC_V5_ADDR_TYPE_IRS
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
32. **[05-21 14:59]** [PATCH v2 31/39] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
33. **[05-21 15:00]** [PATCH v2 32/39] KVM: arm64: gic-v5: Mask per-vcpu PPI state in
 vgic_v5_finalize_ppi_state()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
34. **[05-21 15:00]** [PATCH v2 33/39] KVM: arm64: gic-v5: Add GICv5 EL1 sysreg userspace
 accessors
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
35. **[05-21 15:00]** [PATCH v2 34/39] KVM: arm64: gic-v5: Handle userspace accesses to IRS
 MMIO region
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
36. **[05-21 15:01]** [PATCH v2 35/39] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[05-21 15:01]** [PATCH v2 36/39] Documentation: KVM: Document
 KVM_DEV_ARM_VGIC_GRP_CPU_SYSREGS for VGICv5
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[05-21 15:01]** [PATCH v2 37/39] Documentation: KVM: Add
 KVM_DEV_ARM_VGIC_GRP_IRS_REGS to VGICv5 docs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[05-21 15:02]** [PATCH v2 38/39] Documentation: KVM: Add docs for
 KVM_DEV_ARM_VGIC_GRP_IST
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[05-21 15:02]** [PATCH v2 39/39] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 3: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations

**📧 邮件数**: 26 | **👥 参与者**: 5 | **📅 开始时间**: Mon, 11 May 2026 09:57:27 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（内核虚拟机）文档的补丁，旨在明确 KVM 在主机内核升级和回滚过程中应保持的访客可见兼容性期望。

### 原始补丁内容
David Woodhouse 提出的补丁文档阐述了 KVM 应该维护访客可见的兼容性，特别是：
- KVM 的 IOCTL 保存和恢复状态必须足够支持内核版本间的实时迁移和更新。
- 新内核引入的访客可见变化应提供机制让用户空间选择旧行为。

### 之前讨论要点
在历史讨论中，参与者们探讨了 KVM 在不同架构（如 x86 和 ARM）上的兼容性问题。Paolo Bonzini 指出，x86 通过 CPUID 提供一致的访客视图，但 ARM 的兼容性尚未成熟。Marc Zyngier 强调用户空间需要发现主机和 KVM 的组合能力，并对 KVM 的兼容性表示关注。

### 本周新讨论进展
本周的讨论集中在补丁的实际应用和一个简单的修复上，David Woodhouse 提出补丁被拒绝的理由不合理，认为 KVM 应该负责维护访客的兼容性。Will Deacon 和其他参与者支持这一观点，强调 KVM 在 ARM64 上应当追求稳定性和成熟度。Marc Zyngier 则对保留某些“错误行为”表示质疑，认为不应为了兼容性而保留不必要的缺陷。讨论中达成共识，补丁文档是有益的，但对具体修复的看法仍存在分歧。

总体来看，邮件线程反映了 KVM 在维护访客兼容性方面的复杂性和不同参与者的技术立场。

#### 📝 邮件列表

1. **[05-11 09:57]** [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[05-11 17:14]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
3. **[05-11 17:38]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
4. **[05-11 18:56]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
5. **[05-13 09:42]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-13 10:24]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
7. **[05-13 14:43]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
8. **[05-13 14:57]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
9. **[05-13 18:24]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
10. **[05-19 11:41]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
11. **[05-19 12:11]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Will Deacon <will@kernel.org>
12. **[05-19 12:44]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
13. **[05-19 14:13]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
14. **[05-19 13:38]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[05-19 13:42]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
16. **[05-19 13:56]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[05-19 13:59]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
18. **[05-19 14:24]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
19. **[05-19 15:53]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
20. **[05-19 15:13]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
21. **[05-19 14:10]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Oliver Upton <oupton@kernel.org>
22. **[05-19 22:58]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
23. **[05-19 15:57]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Oliver Upton <oupton@kernel.org>
24. **[05-20 00:33]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
25. **[05-20 10:47]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Oliver Upton <oupton@kernel.org>
26. **[05-20 19:29]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 4: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 24 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 19 May 2026 15:27:14 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于增强 KVM/ARM 的补丁系列，主题为“引入可定制的 aarch64 KVM 主机模型”。该补丁的核心是增强现有的 KVM 主机模型，使其能够设置可写的 ID 寄存器字段，以提高在不同主机硬件之间迁移虚拟机的灵活性。

在历史讨论中，补丁的版本从 v4 更新到 v5，主要改进包括生成与 ARM ID 寄存器相关的头文件、修复了 ID 寄存器的可见性问题，并增加了对可写字段的更好支持。

本周的新讨论中，Eric Auger 提出了多个补丁，涵盖了以下几个方面：
1. 引入了用于自动生成 ID 寄存器定义的脚本，确保与最新的 ARM 架构保持一致。
2. 在 KVM 中添加了获取可写 ID 寄存器位掩码的功能，并在 CPU 初始化时存储这些信息。
3. 允许从主机读取和写入可写的 ID 寄存器值，并在 KVM 中进行同步。
4. 处理特殊情况，如 REVIDR_EL1 和 AIDR_EL1，这些寄存器虽然可写，但不暴露命名字段。
5. 最后，增加了对 ID 寄存器属性的文档说明，帮助用户理解如何配置这些寄存器。

总体来看，这一系列补丁旨在提升 KVM/ARM 的功能，使其能够更好地支持虚拟化和迁移操作。

#### 📝 邮件列表

1. **[05-19 15:27]** [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[05-19 15:27]** [PATCH v5 01/18] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-19 15:27]** [PATCH v5 02/18] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[05-19 15:27]** [PATCH v5 03/18] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-19 15:27]** [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[05-19 15:27]** [PATCH v5 05/18] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-19 15:27]** [PATCH v5 06/18] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[05-19 15:27]** [PATCH v5 07/18] target/arm/cpu-idregs.h.inc: generate with script
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[05-19 15:27]** [PATCH v5 08/18] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[05-19 15:27]** [PATCH v5 09/18] target/arm/kvm: Introduce kvm_get_writable_id_regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[05-19 15:27]** [PATCH v5 10/18] target/arm/cpu64: Retrieve writable ID reg map in aarch64_host_initfn()
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[05-19 15:27]** [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[05-19 15:27]** [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[05-19 15:27]** [PATCH v5 13/18] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[05-19 15:27]** [PATCH v5 14/18] target/arm/kvm: Special case REVIDR_EL1 and AIDR_EL1
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[05-19 15:27]** [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that shouldn't be
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[05-19 15:27]** [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[05-19 15:27]** [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[05-19 15:27]** [PATCH v5 18/18] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
20. **[05-21 15:23]** Re: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Sebastian Ott <sebott@redhat.com>
21. **[05-21 15:27]** Re: [PATCH v5 08/18] target/arm/cpu_idregs: generate tables for
 Arm64 ID registers and fields
   - 发件人: Sebastian Ott <sebott@redhat.com>
22. **[05-21 15:43]** Re: [PATCH v5 09/18] target/arm/kvm: Introduce
 kvm_get_writable_id_regs
   - 发件人: Sebastian Ott <sebott@redhat.com>
23. **[05-21 15:47]** Re: [PATCH v5 10/18] target/arm/cpu64: Retrieve writable ID reg map
 in aarch64_host_initfn()
   - 发件人: Sebastian Ott <sebott@redhat.com>
24. **[05-21 16:22]** Re: [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers
 from host
   - 发件人: Sebastian Ott <sebott@redhat.com>

---

### Thread 5: [PATCH v2 00/18] KVM: arm64: vgic-v5 fixes for 7.2

**📧 邮件数**: 21 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 20 May 2026 10:19:31 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH v2 00/18] KVM: arm64: vgic-v5 fixes for 7.2”，主要讨论了针对 KVM 中 ARM64 架构的 VGIC-v5 相关修复和改进。

1. **原始 patch/问题的内容**：该补丁系列旨在修复 VGIC-v5 的 PPI（Private Peripheral Interrupt）支持，目标是为即将到来的 7.2 版本进行清理和改进。补丁包括对 PPI 相关功能的优化和错误修复。

2. **之前讨论要点**：在历史讨论中，Marc Zyngier 提到之前的版本未能在 7.1 窗口内提交，因此重新发布了该系列补丁。补丁中修复了一些文档中的拼写错误，并进行了代码结构的优化。

3. **本周的新讨论、进展或结论**：本周的讨论集中在对补丁的具体实现上，包括：
   - 增加了 `for_each_visible_v5_ppi()` 迭代器，以简化代码。
   - 将 PPI 能力移入 `kvm_vgic_global_state` 结构中。
   - 移除了不必要的检查，并优化了 PPI 的分配逻辑。
   - 讨论了对 GICv5 的支持限制为 64 个 PPI，并添加了对 NV（Nested Virt）处理的支持。
   - 提高了自测试的错误处理能力，确保了 GICv5 的功能完整性。

整体来看，本周的讨论和补丁更新旨在提升 KVM 对 ARM64 VGIC-v5 的支持，确保其在 7.2 版本中的稳定性和性能。

#### 📝 邮件列表

1. **[05-20 10:19]** [PATCH v2 00/18] KVM: arm64: vgic-v5 fixes for 7.2
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-20 10:19]** [PATCH v2 01/18] KVM: arm64: vgic-v5: Add for_each_visible_v5_ppi() iterator
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-20 10:19]** [PATCH v2 02/18] KVM: arm64: vgic-v5: Move PPI caps into kvm_vgic_global_state
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-20 10:19]** [PATCH v2 03/18] KVM: arm64: vgic-v5: Remove use of __assign_bit() with a constant
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[05-20 10:19]** [PATCH v2 04/18] KVM: arm64: vgic-v5: Drop pointless ARM64_HAS_GICV5_CPUIF check
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-20 10:19]** [PATCH v2 05/18] KVM: arm64: vgic: Constify struct irq_ops usage
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-20 10:19]** [PATCH v2 06/18] KVM: arm64: vgic: Consolidate vgic_allocate_private_irqs_locked()
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-20 10:19]** [PATCH v2 07/18] KVM: arm64: vgic-v5: Drop defensive checks from vgic_v5_ppi_queue_irq_unlock()
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[05-20 10:19]** [PATCH v2 08/18] KVM: arm64: vgic: Rationalise per-CPU irq accessor
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[05-20 10:19]** [PATCH v2 09/18] KVM: arm64: vgic-v5: Limit support to 64 PPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[05-20 10:19]** [PATCH v2 10/18] KVM: arm64: vgic-v5: Add missing trap handing for NV triage
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[05-20 10:19]** [PATCH v2 11/18] KVM: arm64: vgic-v5: Atomically assign bits to PPI DVI bitmap
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[05-20 10:19]** [PATCH v2 12/18] KVM: arm64: selftests: Add missing GIC CDEN to no-vgic-v5 selftest
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[05-20 10:19]** [PATCH v2 13/18] KVM: arm64: selftests: Cleanup unused vars in GICv5 PPI selftest
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[05-20 10:19]** [PATCH v2 14/18] KVM: arm64: selftests: Improve error handling for GICv5 PPI selftest
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[05-20 10:19]** [PATCH v2 15/18] Documentation: KVM: Fix typos in VGICv5 documentation
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[05-20 10:19]** [PATCH v2 16/18] Documentation: KVM: Clarify that PMU_V3_IRQ IntID requirements for GICv5
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[05-20 10:19]** [PATCH v2 17/18] irqchip/gic-v5: Immediately exec priority drop following activate
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[05-20 10:19]** [PATCH v2 18/18] KVM: arm64: Fix arch timer interrupts for GICv3-on-GICv5 guests
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[05-20 14:26]** Re: [PATCH v2 03/18] KVM: arm64: vgic-v5: Remove use of
 __assign_bit() with a constant
   - 发件人: Joey Gouly <joey.gouly@arm.com>
21. **[05-20 14:54]** Re: [PATCH v2 10/18] KVM: arm64: vgic-v5: Add missing trap handing
 for NV triage
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 6: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups

**📧 邮件数**: 19 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 21 May 2026 14:25:38 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的 KVM 中 FPSIMD、SVE 和 SME 状态管理代码的清理工作。Mark Rutland 提出了一个包含 18 个补丁的系列，旨在简化和优化相关代码，使其更易于维护和扩展，尤其是在添加 SME 支持时。

1. **原始补丁内容**：补丁系列主要集中在清理低级的 FPSIMD/SVE/SME 状态管理代码，包括减少代码重复、简化调用约定、增强调试能力以及移除不必要的代码。

2. **历史讨论要点**：之前的讨论主要围绕如何改进 SVE 和 SME 状态的管理，确保在内存中更安全地管理状态，并使得调试工具（如 KASAN 和 KCSAN）能够有效工作。

3. **本周的新讨论与进展**：本周的讨论中，Mark 提出了多个补丁，逐步将 SVE 和 SME 的保存/恢复逻辑从汇编代码转移到内联 C 代码中，以提高可读性和可维护性。此外，补丁还引入了新的不透明类型 `struct sve_state`，以替代原先的 `void*` 指针，减少潜在的错误。最终，所有与 FPSIMD 相关的宏被移除，进一步简化了代码结构。

整体而言，这一系列补丁的目标是提升 ARM64 KVM 的代码质量，确保未来的扩展和维护更加高效。

#### 📝 邮件列表

1. **[05-21 14:25]** [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-21 14:25]** [PATCH 01/18] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[05-21 14:25]** [PATCH 02/18] KVM: arm64: Don't override FFR save/restore argument
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[05-21 14:25]** [PATCH 03/18] KVM: arm64: pkvm: Save host FPMR in host cpu context
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-21 14:25]** [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[05-21 14:25]** [PATCH 05/18] arm64: fpsimd: Fold sve_init_regs() into do_sve_acc()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[05-21 14:25]** [PATCH 06/18] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[05-21 14:25]** [PATCH 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
9. **[05-21 14:25]** [PATCH 08/18] arm64: fpsimd: Use assembler for baseline SME instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[05-21 14:25]** [PATCH 09/18] arm64: fpsimd: Move sve_get_vl() and sme_get_vl() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[05-21 14:25]** [PATCH 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[05-21 14:25]** [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
13. **[05-21 14:25]** [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
14. **[05-21 14:25]** [PATCH 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
15. **[05-21 14:25]** [PATCH 14/18] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
16. **[05-21 14:25]** [PATCH 15/18] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
17. **[05-21 14:25]** [PATCH 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
18. **[05-21 14:25]** [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
19. **[05-21 14:25]** [PATCH 18/18] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 7: [PATCH 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 18 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 20 May 2026 16:26:33 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（内核虚拟机）在 arm64 架构下引入 pKVM 超级管理器堆分配器的补丁系列。该补丁旨在解决 pKVM 之前缺乏动态内存分配器的问题，所有虚拟机和虚拟 CPU 结构必须在主机上预先分配，导致内存管理复杂且限制了虚拟机的可扩展性。

**补丁内容**：
1. **补丁系列概述**：引入一个动态映射的自定义堆分配器（hyp_allocator），用于管理 pKVM 超级管理器的内存。初步用户包括 pkvm_hyp_vm 和 pkvm_hyp_vcpu 结构及超管跟踪元数据。
2. **主要构建模块**：
   - **pkvm_hyp_req**：处理内存不足时的请求。
   - **hyp_allocator**：动态管理物理页面的分配和释放。
   - **shrinker**：允许在主机内存压力下回收未使用的超管内存。

**历史讨论要点**：
- 之前的讨论集中在如何优化 pKVM 的内存管理，特别是如何减少主机与超管之间的内存捐赠和回收路径的复杂性。

**本周新讨论与进展**：
- 本周的讨论中，Vincent Donnefort 提出了多个补丁，涵盖了堆分配器的初始化、内存回收接口、以及如何在 pKVM 中动态分配虚拟机和虚拟 CPU 状态结构。此外，还引入了自测功能以确保堆分配器的稳定性和可靠性。补丁的最终目标是实现更高效的内存管理和更好的虚拟机性能。

#### 📝 邮件列表

1. **[05-20 16:26]** [PATCH 00/17] KVM: arm64: Introduce pKVM hypervisor heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-20 16:26]** [PATCH 01/17] KVM: arm64: Add __pkvm_private_range_pa
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-20 16:26]** [PATCH 02/17] KVM: arm64: Add pkvm_remove_mappings
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[05-20 16:26]** [PATCH 03/17] KVM: arm64: Add __hyp_allocator_map for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[05-20 16:26]** [PATCH 04/17] KVM: arm64: Add a heap allocator for the pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[05-20 16:26]** [PATCH 05/17] KVM: arm64: Allow kvm_hyp_memcache usage outside of stage-2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[05-20 16:26]** [PATCH 06/17] KVM: arm64: Add topup interface for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[05-20 16:26]** [PATCH 07/17] KVM: arm64: Add pkvm_hyp_req infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[05-20 16:26]** [PATCH 08/17] KVM: arm64: Handle PKVM_HYP_REQ_HYP_ALLOC request
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[05-20 16:26]** [PATCH 09/17] KVM: arm64: Add reclaim interface for the pKVM heap alloc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[05-20 16:26]** [PATCH 10/17] KVM: arm64: Add selftests for the pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[05-20 16:26]** [PATCH 11/17] KVM: arm64: Add a shrinker for pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[05-20 16:26]** [PATCH 12/17] KVM: arm64: Filter out non-kernel addresses in kern_hyp_va
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[05-20 16:26]** [PATCH 13/17] KVM: arm64: Move hyp_vm refcount into the structure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[05-20 16:26]** [PATCH 14/17] KVM: arm64: Use noclear for PGD in __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[05-20 16:26]** [PATCH 15/17] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[05-20 16:26]** [PATCH 16/17] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM heap allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[05-20 16:26]** [PATCH 17/17] KVM: arm64: Alloc simple_buffer_page using pKVM hyp allocator
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 8: [PATCH v2 0/3] Fix __pkvm_init_vm error path

**📧 邮件数**: 14 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 21 May 2026 11:21:46 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的 pKVM（Paravirtualized Kernel-based Virtual Machine）初始化过程中出现的错误路径的修复。原始的补丁（PATCH v2 0/3）旨在解决在 `__pkvm_init_vm` 函数中可能导致的引用计数泄漏问题，特别是在 `insert_vm_table_entry` 失败时。

在历史讨论中，Sashiko 报告了一个潜在的引用计数泄漏问题，促使开发者 Vincent Donnefort 提出了补丁以修复该问题。补丁的主要内容包括：重置 pKVM 的页面顺序、修复 `__pkvm_init_vm` 的错误路径以及为引用计数页面添加安全检查。

本周的新讨论中，Vincent 提出了三个补丁的具体实现：首先，重置 pKVM 的页面顺序以防止在初始化失败时出现错误；其次，修复 `__pkvm_init_vm` 函数中的错误路径，确保在失败时正确释放内存；最后，引入了一个安全检查以防止引用计数页面的泄漏。参与者 Fuad Tabba 对这些补丁进行了审查并表示支持，提出了一些改进建议，最终达成共识，确保代码的安全性和稳定性。

#### 📝 邮件列表

1. **[05-21 11:21]** [PATCH v2 0/3] Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-21 11:21]** [PATCH v2 1/3] KVM: arm64: Reset page order in pKVM hyp_pool_init
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-21 11:21]** [PATCH v2 2/3] KVM: arm64: Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[05-21 11:21]** [PATCH v2 3/3] KVM: arm64: Add fail-safe for refcounted pages in __pkvm_hyp_donate_host
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[05-21 13:46]** [PATCH v2 0/3] Fixes for hyp_trace.c
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[05-21 13:46]** [PATCH v2 1/3] KVM: arm64: Fix meta-page unsharing in pKVM hyp tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[05-21 13:46]** [PATCH v2 2/3] KVM: arm64: Fix rollback in hyp_trace_buffer_share_hyp()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[05-21 13:46]** [PATCH v2 3/3] KVM: arm64: Fix memory leak in hyp_trace_unload()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[05-21 14:07]** Re: [PATCH v2 0/3] Fix __pkvm_init_vm error path
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[05-21 14:07]** Re: [PATCH v2 1/3] KVM: arm64: Reset page order in pKVM hyp_pool_init
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[05-21 14:07]** Re: [PATCH v2 2/3] KVM: arm64: Fix __pkvm_init_vm error path
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[05-21 14:07]** Re: [PATCH v2 3/3] KVM: arm64: Add fail-safe for refcounted pages in __pkvm_hyp_donate_host
   - 发件人: Fuad Tabba <tabba@google.com>
13. **[05-21 14:21]** Re: [PATCH v2 1/3] KVM: arm64: Reset page order in pKVM hyp_pool_init
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[05-21 14:30]** Re: [PATCH v2 1/3] KVM: arm64: Reset page order in pKVM hyp_pool_init
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 9: [PATCH v4 0/5] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 12 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 20 May 2026 20:49:43 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）的补丁系列，主要目的是修复 Endpoint Memory Access Descriptor（EMAD）偏移量计算及相关的边界检查问题。

**原始补丁内容**：
该补丁系列（PATCH v4 0/5）旨在修复 EMAD 偏移量计算错误，并为 FF-A 驱动和 pKVM 超级管理程序添加必要的边界检查。补丁的关键在于从 FF-A 版本 1.1 开始，内存区域头部不再假设 EMAD 紧随其后，而是通过 `ep_mem_offset` 字段来确定。

**之前讨论要点**：
在历史讨论中，开发者们指出了在 FF-A 版本 1.1 之前，EMAD 的偏移量计算存在问题，导致潜在的内存越界写入。补丁的更新也修复了其他相关问题，确保了驱动和 pKVM 的一致性。

**本周新讨论与进展**：
本周的讨论主要集中在补丁的具体实现和代码审查上。Mostafa Saleh 提出了多个补丁，修复了内存越界写入、添加了 NULL 检查，并改进了偏移量计算的逻辑。Marc Zyngier 对某些边界检查的实现提出了疑问，讨论了 WARN_ON 的使用是否会导致系统崩溃。最终，开发者们达成一致，决定去掉某些可能导致崩溃的检查。Sudeep Holla 对补丁进行了审查并给予了认可。

总体来看，本周的讨论推动了补丁的完善，确保了 FF-A 和 KVM 的稳定性和安全性。

#### 📝 邮件列表

1. **[05-20 20:49]** [PATCH v4 0/5] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-20 20:49]** [PATCH v4 1/5] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-20 20:49]** [PATCH v4 2/5] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-20 20:49]** [PATCH v4 3/5] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-20 20:49]** [PATCH v4 4/5] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-20 20:49]** [PATCH v4 5/5] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[05-21 09:28]** Re: [PATCH v4 4/5] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-21 10:30]** Re: [PATCH v4 4/5] KVM: arm64: Fix bounds checking in
 do_ffa_mem_reclaim()
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[05-21 11:43]** Re: [PATCH v4 4/5] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Mostafa Saleh <smostafa@google.com>
10. **[05-21 13:12]** Re: [PATCH v4 4/5] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[05-21 13:51]** Re: [PATCH v4 2/5] firmware: arm_ffa: Fix out-of-bound writes in
 ffa_setup_and_transmit()
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
12. **[05-21 13:55]** Re: [PATCH v4 3/5] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 10: [PATCH v3 0/6] KVM: arm64: Don't perform vgic-v2 lazy init on timer injection

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 20 May 2026 11:01:54 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-v2（虚拟通用中断控制器）初始化优化，特别是在定时器注入时的懒惰初始化问题。

**原始 patch/问题内容**：
Marc Zyngier 提出了一个补丁系列（PATCH v3 0/6），旨在解决 vgic-v2 在非抢占上下文中初始化的问题，特别是定时器注入时不应执行懒惰初始化。

**之前讨论要点**：
在之前的版本中（v1 和 v2），补丁进行了多次修改，包括简化用户空间中断状态通知、重命名函数以提高可读性、以及移除不必要的中断级别缓存等。补丁得到了社区的认可和支持。

**本周新讨论、进展或结论**：
本周的讨论中，Marc Zyngier 提交了补丁的最终版本，具体包括：
1. 重命名与定时器相关的函数以提高代码可读性。
2. 简化用户空间中断状态的通知逻辑。
3. 移除定时器和 PMU（性能监控单元）的中断级别缓存，以解决潜在的正确性问题。
4. 强制在用户空间或 irqfd 注入中断时进行 vgic 初始化，而在内核中断注入时不再进行初始化，以避免在非抢占上下文中出现问题。

最终，补丁已被应用到主线代码中，标志着这一系列优化的完成。

#### 📝 邮件列表

1. **[05-20 11:01]** [PATCH v3 0/6] KVM: arm64: Don't perform vgic-v2 lazy init on timer injection
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-20 11:01]** [PATCH v3 1/6] KVM: arm64: timer: Repaint kvm_timer_{should,irq_can}_fire() to kvm_timer_{pending,enabled}()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-20 11:01]** [PATCH v3 2/6] KVM: arm64: Simplify userspace notification of interrupt state
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-20 11:01]** [PATCH v3 3/6] KVM: arm64: timer: Kill the per-timer irq level cache
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[05-20 11:01]** [PATCH v3 4/6] KVM: arm64: pmu: Kill the PMU interrupt level cache
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-20 11:01]** [PATCH v3 5/6] KVM: arm64: vgic-v2: Force vgic init on injection outside the run loop
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-20 11:02]** [PATCH v3 6/6] KVM: arm64: vgic-v2: Don't init the vgic on in-kernel interrupt injection
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-20 11:26]** Re: [PATCH v3 0/6] KVM: arm64: Don't perform vgic-v2 lazy init on
 timer injection
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[05-21 08:23]** Re: [PATCH v3 0/6] KVM: arm64: Don't perform vgic-v2 lazy init on timer injection
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 11: [PATCH v2 0/2] KVM: arm64: nv: Reduce FP/SVE overhead on exception/exception return

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 20 May 2026 09:50:34 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于优化 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的 FP/SVE（浮点/SIMD 向量扩展）上下文切换开销，特别是在异常和异常返回时的处理。

**原始 patch/问题的内容**：
Marc Zyngier 提出了两个补丁（PATCH v2 0/2），旨在减少在异常处理过程中不必要的 FP/SVE 上下文切换开销。补丁包括：
1. 跟踪从 L2 到 L1 的异常仿真。
2. 在嵌套的 ERET 或异常处理中，不再保存/恢复 FP 寄存器。

**之前讨论要点**：
在之前的讨论中，Marc 强调了在 L1 和 L2 之间切换时，FP/SVE 状态的共享性，指出保存和恢复这些状态的开销是多余的，尤其是在嵌套异常的情况下。

**本周的新讨论、进展或结论**：
本周的讨论中，Marc 提供了补丁的更新版本，并增加了新的提交信息和注释。参与者 Joey Gouly 和 Mark Rutland 对补丁进行了审查并表示认可，确认了补丁的逻辑和必要性。最终，Marc 宣布补丁已应用到下一个开发版本中。这些改进预计将显著降低在 I/O 密集型工作负载下的处理时间，提升系统性能。

#### 📝 邮件列表

1. **[05-20 09:50]** [PATCH v2 0/2] KVM: arm64: nv: Reduce FP/SVE overhead on exception/exception return
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-20 09:50]** [PATCH v2 1/2] KVM: arm64: nv: Track L2 to L1 exception emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-20 09:50]** [PATCH v2 2/2] KVM: arm64: nv: Don't save/restore FP register during a nested ERET or exception
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-20 12:02]** Re: [PATCH v2 2/2] KVM: arm64: nv: Don't save/restore FP register
 during a nested ERET or exception
   - 发件人: Joey Gouly <joey.gouly@arm.com>
5. **[05-20 14:02]** Re: [PATCH v2 2/2] KVM: arm64: nv: Don't save/restore FP register
 during a nested ERET or exception
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[05-21 07:21]** Re: [PATCH v2 2/2] KVM: arm64: nv: Don't save/restore FP register during a nested ERET or exception
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-21 07:35]** Re: [PATCH v2 2/2] KVM: arm64: nv: Don't save/restore FP register during a nested ERET or exception
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-21 08:07]** Re: [PATCH v2 0/2] KVM: arm64: nv: Reduce FP/SVE overhead on exception/exception return
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 17 May 2026 13:49:55 -0400

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的修复补丁，主要针对 vgic-its（虚拟通用中断控制器）中处理设备表条目（DTE）时的一个安全漏洞。

**原始补丁内容**：
补丁的核心是拒绝恢复的 DTE 中 num_eventid_bits 超出 VITS_TYPER_IDBITS 的情况。此问题可能导致用户空间通过 KVM_DEV_ARM_ITS_RESTORE_TABLES 触发主机端的拒绝服务（DoS），因为超出范围的值会导致 scan_its_table() 函数在持有互斥锁的情况下长时间阻塞 CPU。

**之前讨论要点**：
在历史讨论中，Michael Bommarito 提出了补丁的背景和问题，强调了超出范围的 num_eventid_bits 会导致系统性能问题。参与者们讨论了该问题的严重性及其潜在影响。

**本周的新讨论与进展**：
本周的讨论主要集中在补丁的细节和实现上。Yao Yuan 提出了对补丁的进一步思考，认为即使进行了检查，数据转换的问题仍然存在。Marc Zyngier 则对补丁的实现表示质疑，认为当前的硬编码限制是合理的，并询问是否有可能使其用户空间可配置。最终，Michael Bommarito 提交了补丁的第二版，简化了提交信息，并在代码中添加了必要的检查。该补丁已被应用，标志着该问题的修复。

#### 📝 邮件列表

1. **[05-17 13:49]** [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>
2. **[05-18 14:05]** Re: [PATCH] KVM: arm64: vgic-its: reject restored DTE with
 out-of-range num_eventid_bits
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
3. **[05-18 09:23]** Re: [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-18 09:33]** Re: [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[05-19 09:25]** [PATCH v2] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>
6. **[05-20 14:04]** Re: [PATCH] KVM: arm64: vgic-its: reject restored DTE with
 out-of-range num_eventid_bits
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
7. **[05-20 07:52]** Re: [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-20 08:17]** Re: [PATCH v2] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 13: [PATCH kvmtool v8 0/6] arm64: Nested virtualization support

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 18 May 2026 14:45:50 +0200

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的嵌套虚拟化支持的补丁系列（v8 版本），共包含六个补丁。补丁的主要内容包括引入新的命令行选项以支持嵌套虚拟化、设置维护中断、控制计数器偏移、支持 FEAT_E2H0、生成 HYP 定时器中断说明以及处理虚拟设备的字节序重置。

在历史讨论中，补丁的背景是为了适应 ARMv8.3 架构的更新，允许用户通过命令行选项“--nested”启动虚拟机于 EL2 模式。之前的讨论集中在如何实现这些功能及其对现有系统的影响。

本周的新进展包括：
1. 所有补丁已成功应用到 kvmtool 的主分支。
2. 各补丁的功能得到了确认，包括对维护中断的支持和计数器偏移的控制。
3. 讨论中提到的补丁链接也被提供，便于查阅具体实现。

总的来说，这一系列补丁为 ARM64 的嵌套虚拟化提供了重要的支持，推动了相关功能的实现与测试。

#### 📝 邮件列表

1. **[05-18 14:45]** [PATCH kvmtool v8 0/6] arm64: Nested virtualization support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
2. **[05-18 14:45]** [PATCH kvmtool v8 1/6] arm64: Initial nested virt support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
3. **[05-18 14:45]** [PATCH kvmtool v8 2/6] arm64: nested: Add support for setting maintenance IRQ
   - 发件人: Andre Przywara <andre.przywara@arm.com>
4. **[05-18 14:45]** [PATCH kvmtool v8 3/6] arm64: Add counter offset control
   - 发件人: Andre Przywara <andre.przywara@arm.com>
5. **[05-18 14:45]** [PATCH kvmtool v8 4/6] arm64: Add FEAT_E2H0 support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
6. **[05-18 14:45]** [PATCH kvmtool v8 5/6] arm64: Generate HYP timer interrupt specifiers
   - 发件人: Andre Przywara <andre.przywara@arm.com>
7. **[05-18 14:45]** [PATCH kvmtool v8 6/6] arm64: Handle virtio endianness reset when running nested
   - 发件人: Andre Przywara <andre.przywara@arm.com>
8. **[05-19 16:22]** Re: [PATCH kvmtool v8 0/6] arm64: Nested virtualization support
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 14: [PATCH v4 12/17] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 7 May 2026 19:10:51 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM KVM 的补丁，具体是引入 `kvm_arm_expose_idreg_properties` 功能。该补丁旨在改善 KVM 中的 ID 寄存器属性的暴露。

在历史讨论中，Shameer Kolothum Thodi 提出了对补丁的几个建议和问题，包括在动态内存分配方面的改进、确保在设置可写掩码之前清空缓冲区，以及对 KVM 隐藏寄存器的行为的关注。这些讨论为补丁的改进提供了背景和方向。

在本周的新讨论中，Eric Auger 对 Shameer 的建议做出了回应，确认了一些修改已被采纳，例如使用宏来避免动态分配，并确认在设置可写掩码时会先清空缓冲区。此外，Eric 还提到将会在下一个版本中修复之前未能解决的评论。这表明补丁正在逐步完善，参与者之间的沟通也在持续推动进展。

#### 📝 邮件列表

1. **[05-07 19:10]** RE: [PATCH v4 12/17] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
2. **[05-07 19:22]** RE: [PATCH v4 15/17] arm/cpu: Expose writable ID reg field properties
 on the kvm host vcpu model
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
3. **[05-07 19:44]** RE: [PATCH v4 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
4. **[05-08 13:03]** RE: [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
5. **[05-18 17:09]** Re: [PATCH v4 12/17] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[05-18 17:21]** Re: [PATCH v4 15/17] arm/cpu: Expose writable ID reg field properties
 on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-18 17:27]** Re: [PATCH v4 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[05-19 08:45]** Re: [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 15: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 08 May 2026 18:54:14 +0100

#### 🤖 AI 总结

本邮件讨论的主题是将 Arm FF-A 核心初始化移至平台驱动探测过程中。历史讨论中，Sudeep Holla 提出了一个补丁系列，旨在通过将 FF-A 核心的引导路径转换为平台驱动的探测/移除流程来改善驱动模型。第一个补丁回退了之前的 rootfs_initcall 更改，指出该解决方案不够妥当，可能与 pKVM FF-A 代理的需求冲突。

在本周的新讨论中，Nathan Chancellor 报告了在其两个 arm64 测试机器上遇到的错误信息，表示在补丁应用后，FF-A 驱动探测失败，错误代码为 -95。他询问这是否是预期行为。Yeoreum Yun 随后回应，要求 Nathan 提供其使用的 .config 文件，并分析了错误的可能原因，认为这可能与环境不支持 FF-A 或使用的 SMCCC 版本较低有关。他指出，这种错误在补丁之前并未显示，因为所有 FF-A 初始化都在 initcall 阶段完成，导致即使发生错误也不会打印日志。

总体来看，本周的讨论集中在补丁引入的新错误及其预期行为的确认上，参与者们在寻找解决方案和理解错误来源。

#### 📝 邮件列表

1. **[05-08 18:54]** [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
2. **[05-08 18:54]** [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
3. **[05-22 17:11]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Nathan Chancellor <nathan@kernel.org>
4. **[05-23 05:50]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[05-22 22:05]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Nathan Chancellor <nathan@kernel.org>
6. **[05-23 07:23]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[05-23 07:27]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 16: [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and disable on teardown

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 06 May 2026 16:03:53 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 GICv5（通用中断控制器版本5）的一系列补丁，特别关注于 VPE（虚拟处理单元）的门铃（doorbell）管理。

**原始补丁内容**：
补丁 17/43 的主要目的是在 VPE 重置时启用 VPE 的门铃，并在拆除时禁用。这一补丁旨在优化 VPE 的中断管理。

**之前的讨论要点**：
在历史讨论中，Marc Zyngier 对补丁中使用的 IRQ_NOAUTOEN 设置提出了疑问，认为该设置是多余的，并且建议简化代码。Sascha Bischoff 也对补丁的设计风格提出了意见，认为应该在一个补丁中添加所有寄存器定义，而不是分开处理。

**本周的新讨论与进展**：
在本周的讨论中，Sascha Bischoff 对补丁进行了重构，移除了不必要的 IRQ_NOAUTOEN 设置，并将相关更改整合到 GICv5 虚拟机的初始化和拆除过程中。此外，他还对 SPI（共享中断）数量的要求进行了严格化，确保与 GICv3 的一致性，最小值设定为 32。整体来看，本周的讨论集中在优化和简化代码结构上，确保了更高的代码质量和一致性。

#### 📝 邮件列表

1. **[05-06 16:03]** Re: [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and disable on teardown
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-07 16:10]** Re: [PATCH 18/43] KVM: arm64: gic-v5: Define remaining IRS MMIO registers
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-21 14:06]** Re: [PATCH 14/43] KVM: arm64: gic-v5: Request VPE doorbells when
 going non-resident
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[05-21 14:07]** Re: [PATCH 16/43] KVM: arm64: gic-v5: Initialise and teardown VMTEs &
 doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[05-21 14:12]** Re: [PATCH 36/43] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[05-21 14:17]** Re: [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and
 disable on teardown
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[05-21 14:22]** Re: [PATCH 18/43] KVM: arm64: gic-v5: Define remaining IRS MMIO
 registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 17: [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 17 May 2026 14:13:31 -0400

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vGIC（虚拟通用中断控制器）初始化失败时的私有中断释放问题。最初的补丁由 Michael Bommarito 提出，目的是在 vGIC 的 vCPU 初始化过程中，如果分配私有 IRQ 后注册失败，确保能够释放这些已分配的 IRQ，以避免资源泄漏。

在历史讨论中，补丁被认为是对之前提交的补充，特别是与 vCPU 创建失败时的清理工作相关。补丁的关键在于添加了 `kvm_vgic_vcpu_destroy()` 的调用，以确保在初始化失败时能够正确释放资源。

在本周的新讨论中，Yao Yuan 表达了对补丁的认可，并提出是否需要添加一个 Fixes 标签。经过讨论，最终确定将 Fixes 标签指向相关的历史提交。Michael 随后提交了补丁的 v2 版本，包含了 Yao 的审核标记，并对提交信息进行了精简。Marc Zyngier 最终确认了补丁并表示已将其应用于修复分支。

总结来说，本周的进展主要是补丁的审核和修改，最终版本已被接受并应用。

#### 📝 邮件列表

1. **[05-17 14:13]** [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>
2. **[05-18 13:28]** Re: [PATCH] KVM: arm64: vgic: free private_irqs when init fails
 after allocation
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
3. **[05-18 13:31]** Re: [PATCH] KVM: arm64: vgic: free private_irqs when init fails
 after allocation
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
4. **[05-18 20:26]** Re: [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>
5. **[05-19 08:53]** Re: [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-19 09:50]** [PATCH v2] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>
7. **[05-20 08:17]** Re: [PATCH v2] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 18: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 5 | **👥 参与者**: 5 | **📅 开始时间**: Sun, 10 May 2026 15:53:33 +0100

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现嵌套阶段2反向映射的补丁（PATCH v3 0/5）。该补丁旨在优化在 MMU 通知期间的影子 S2 MMU 取消映射过程，包含两个新的准备补丁，分别用于减少 kvm_s2_mmu 中的空洞和重构 S2 故障处理代码。

在历史讨论中，Wei-Lin Chang 提到该补丁的更新内容，包括去除“污染”术语、使用 xa_{mk, to}_value() 存储和检索 maple 树中的值、避免在 maple 树值中使用第63位等改动。

在本周的新讨论中，参与者们对补丁的进展进行了反馈。Itaru Kitayama 反馈称，应用该补丁后，最近的 kvmarm/fixes 能够在所有三种页面粒度下正常运行，且在没有该补丁的情况下，16KB 内核无法处理阶段2的取消映射路径。此外，Tian Zheng 和 Will Deacon 讨论了与 Armv9.5 引入的 FEAT_HDBSS 相关的寄存器信息，并确认了相关的系统寄存器定义已被应用。

整体来看，本周的讨论主要集中在补丁的测试结果和对新特性的支持上，显示出社区对该补丁的积极反馈和进一步的合作。

#### 📝 邮件列表

1. **[05-10 15:53]** [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-19 16:23]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Will Deacon <will@kernel.org>
3. **[05-19 16:35]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[05-20 16:31]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
5. **[05-20 16:51]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>

---

### Thread 19: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 22 May 2026 19:00:04 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 ZCR_EL2.LEN 寄存器的处理。Mark Brown 提出的补丁旨在修复当前对 ZCR_EL2.LEN 值的限制，确保所有位都能按照架构文档的要求被读取，而不仅仅是限制在最大向量长度（VL）之内。

在历史讨论中，补丁的背景是由于在处理 ZCR_EL2 寄存器时，当前实现对写入的值进行了限制，导致与架构文档不符。Mark 提出，通过在加载来宾状态时配置 ZCR_EL2，可以更好地管理向量长度，从而避免这种限制。

本周的新讨论中，Marc Zyngier 对补丁提出了一些建议，指出在嵌套上下文中（如 L2 来宾）对 ZCR_EL2 的访问存在问题，尤其是直接写入时的处理需要改进。他建议将 ZCR_EL2 转换为一个经过清理的寄存器，以确保一致性和可持续性。Mark 同意了这一点，并表示将进一步澄清补丁的目的和逻辑。

整体来看，本周的讨论集中在补丁的细节和必要的改进上，参与者们达成了一致，认为需要对 ZCR_EL2 的访问进行更严格的处理，以符合架构规范。

#### 📝 邮件列表

1. **[05-22 19:00]** [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[05-23 09:47]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-23 15:38]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[05-23 16:24]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 20: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Sat, 16 May 2026 19:29:54 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试，主要聚焦于基本的嵌套虚拟机（L2）支持。历史讨论中，Wei-Lin Chang 提出了一个补丁系列（PATCH v3 0/9），旨在为 KVM 的自测试添加嵌套虚拟机的基本支持，包括实现 stage-2 的框架、s2_mmu 结构、翻译控制设置以及 stage-2 页表生成器。此外，还增加了一个 shadow_stage2 测试，用于测试 KVM 中的影子页表管理代码。

在之前的讨论中，提到需要启用 L2 的 stage-1 转换，以确保自测试中的原子操作能够正常工作。Oliver Upton 提出可以利用自测试库为 L1 创建的现有 stage-1 表来解决这个问题。

本周的新讨论中，Oliver Upton 对补丁表示感谢，并强调了启用 stage-1 MMU 的必要性。Itaru Kitayama 则建议调整测试的默认设置，以便在不同的内核配置下运行测试，表明他正在与 Wei-Lin Chang 的其他优化系列进行联合测试。这些讨论显示出对补丁的积极反馈和进一步改进的建议。

#### 📝 邮件列表

1. **[05-16 19:29]** [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-16 19:29]** [PATCH v3 5/9] KVM: arm64: selftests: Add shadow_stage2 test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[05-19 14:31]** Re: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[05-22 11:02]** Re: [PATCH v3 5/9] KVM: arm64: selftests: Add shadow_stage2 test
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>

---

### Thread 21: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 18 May 2026 16:31:26 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM 的补丁（PATCH v2），其内容是建议在 `finalise_el2()` 函数中不再初始化 `TPIDR_EL2`。Will Deacon 提出了该补丁，理由是当前的实现中 `TPIDR_EL2` 并不被 hyp stub 代码使用，因此其初始化是多余的。具体来说，补丁指出：

1. 在引导 CPU 上，`TPIDR_EL1` 被用于每个 CPU 的偏移量，直到检测到 `ARM64_HAS_VIRT_HOST_EXTN` 并进行补丁更新。
2. 辅助 CPU 在补丁更新后启动，`TPIDR_EL2` 会在 `init_cpu_task` 中被初始化。
3. KVM hyp 代码在所有辅助 CPU 启动后才会使用 `TPIDR_EL2`。

本周的讨论中，Marc Zyngier 对该补丁进行了审核并表示支持，确认将其纳入 KVM 的 7.2 版本中。整体来看，补丁得到了积极的反馈，并将顺利推进。

#### 📝 邮件列表

1. **[05-18 16:31]** [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Will Deacon <will@kernel.org>
2. **[05-18 16:39]** Re: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-18 16:41]** Re: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-18 16:55]** Re: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 22: [PATCH v10 19/30] KVM: arm64: Provide assembly for SME register
 access

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 21 May 2026 15:51:26 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 SME（Scalable Matrix Extension）寄存器访问的汇编支持的补丁（PATCH v10 19/30）。该补丁旨在提供对 SME 寄存器的访问功能，以增强 KVM 的性能和兼容性。

在之前的讨论中，参与者 Mark Rutland 提到，尽管该补丁的具体实现相对简单，但不应继续在主内核和 KVM 的 hypervisor 代码中重复低级的保存/恢复例程。他建议先进行一系列清理工作，以避免这种重复，并在此基础上构建 KVM 的 SME 支持。

本周的新讨论中，Mark Rutland 表达了对主内核和 KVM 之间改进的期待，但由于审查流程的延迟，他希望在补丁落地后再进行相关改进。Marc Zyngier 也表示，FP/SVE（浮点/SVE）部分仍然过于复杂，难以审计，希望在此之前进行清理。他对 KVM 特定的补丁进行了初步审查，认为没有明显问题，预计部分内容可能会纳入 7.2 版本中。

总体来看，当前讨论集中在补丁的必要性和后续清理工作的优先级上，参与者们一致认为在推进新功能之前，先进行代码的整洁和优化是重要的。

#### 📝 邮件列表

1. **[05-21 15:51]** Re: [PATCH v10 19/30] KVM: arm64: Provide assembly for SME register
 access
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-21 16:17]** Re: [PATCH v10 19/30] KVM: arm64: Provide assembly for SME register
 access
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[05-22 06:52]** Re: [PATCH v10 19/30] KVM: arm64: Provide assembly for SME register access
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 23: [PATCH v3 0/3] Fix __pkvm_init_vm error path

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 21 May 2026 15:33:15 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于修复 `__pkvm_init_vm` 错误路径的补丁（PATCH v3 0/3）。该补丁旨在解决在 `insert_vm_table_entry` 失败时可能出现的引用计数泄漏问题。补丁中还增加了一个安全机制，以确保 `__pkvm_hyp_donate_host` 函数不会导致引用计数页面的泄漏。

在之前的讨论中，Vincent Donnefort 提出了补丁的多个版本，逐步改进了补丁内容，包括在 `hyp_pool_init` 中主动初始化 `hyp_page` 的顺序字段，并确保外部页面的顺序字段为 0，以避免潜在问题。

在本周的新讨论中，Vincent 继续更新补丁，强调了在虚拟机初始化失败时，必须完全拆除其阶段 2 的 `hyp_pool`，并重置页面的引用计数和顺序。此外，Marc Zyngier 对于补丁的频繁更新表示不满，建议 Vincent 在发布之前先理清问题，以减少邮件的数量。

总体来看，本周的讨论集中在补丁的细节改进和对补丁发布频率的反馈上。

#### 📝 邮件列表

1. **[05-21 15:33]** [PATCH v3 0/3] Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-21 15:33]** [PATCH v3 1/3] KVM: arm64: Reset page order in pKVM hyp_pool
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-21 15:44]** Re: [PATCH v3 0/3] Fix __pkvm_init_vm error path
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 24: [PATCH 0/2] Fix __pkvm_init_vm error path

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 21 May 2026 09:12:48 +0100

#### 🤖 AI 总结

本邮件讨论的主题是修复 `__pkvm_init_vm` 的错误路径，涉及两个补丁。首先，Vincent Donnefort 报告了在 `insert_vm_table_entry` 失败时可能导致的引用计数泄漏问题，并提出了相应的补丁。

在历史讨论中，Sashiko 提出了该潜在的引用计数泄漏问题，Vincent 在此基础上进行了补充，增加了一个安全检查，以防止在 `__pkvm_hyp_donate_host` 函数中泄漏引用计数页面。

本周的新讨论中，Vincent 提交了两个补丁：
1. **补丁 1**：修复 `__pkvm_init_vm` 的错误路径。在 `insert_vm_table_entry` 失败时，确保通过调用 `kvm_guest_destroy_stage2()` 来正确释放主机捐赠的内存，防止引用计数泄漏。
2. **补丁 2**：在 `__pkvm_hyp_donate_host` 中添加了一个故障安全机制，以检查页面的引用计数，确保在状态机中不会丢失对页面的访问。

这两个补丁旨在增强 pKVM 的稳定性与安全性，防止潜在的内存管理问题。

#### 📝 邮件列表

1. **[05-21 09:12]** [PATCH 0/2] Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-21 09:12]** [PATCH 1/2] KVM: arm64: Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-21 09:12]** [PATCH 2/2] KVM: arm64: Add fail-safe for refcounted pages in __pkvm_hyp_donate_host
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 25: [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 12 May 2026 12:44:40 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）的补丁，旨在修复 Endpoint Memory Access Descriptor（EMAD）偏移量计算的问题。

在历史讨论中，Sebastian Ene 提出了一个补丁系列，主要修复 EMAD 的偏移量计算，并为 FF-A 驱动和 pKVM 超级管理程序添加必要的边界检查。之前的版本（1.0）中，内存区域头部并未明确指定 EMAD 的偏移量，导致假设 EMAD 紧随其后。然而，从版本 1.1 开始，规范要求使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。Sudeep Holla 对补丁表示认可，并询问如何将这些更改进行路由。

在本周的新讨论中，Sudeep Holla 表示可以在修复了小问题后，给予该补丁“审核通过”（Reviewed-by）的标记，前提是这些更改能够通过 KVM 或其他相关树进行路由。整体来看，补丁得到了积极的反馈，并有望顺利推进。

#### 📝 邮件列表

1. **[05-12 12:44]** [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[05-13 18:23]** Re: [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
3. **[05-18 14:45]** Re: [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 26: [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 14 May 2026 17:26:24 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 nVHE（Non-virtual Hypervisor Execution）和 pKVM（Protected KVM）模式中，处理无效跟踪描述符时的错误。

**原始 patch/问题的内容**：
Vincent Donnefort 提出了一个补丁，旨在确保 pKVM 验证主机提供的跟踪缓冲区描述符。如果发现错误，补丁修复了超管返回值的问题，确保在验证失败时不会简单返回 0。同时，他还将函数重命名为 hyp_trace_desc_is_valid()，并在 nVHE 模式下跳过验证，因为在该模式下信任主机提供的数据。

**之前的讨论要点**：
在历史讨论中，Vincent 详细描述了补丁的目的和实现方式，强调了对主机数据的验证重要性，并提出了函数重命名的理由。

**本周的新讨论、进展或结论**：
在本周的讨论中，Marc Zyngier 确认已将该补丁应用于修复集，并表示感谢。这表明补丁已被接受并将纳入后续版本中，进一步推动了 KVM 的稳定性和可靠性。

#### 📝 邮件列表

1. **[05-14 17:26]** [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-20 08:17]** Re: [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH v6 2/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ2 in
 host handler

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 19 May 2026 12:59:06 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中支持 FFA_MSG_SEND_DIRECT_REQ2 的补丁（patch）。该补丁旨在改进主机处理直接请求的能力。

在历史讨论中，虽然没有具体的邮件记录，但可以推测出该补丁的提出是为了修复主机在处理 FFA 消息时存在的问题，尤其是与函数调用相关的细节。

本周的新讨论主要集中在补丁的实现细节和潜在问题上。参与者 Fuad Tabba 指出，当前的实现中，handle_host_smc() 函数在处理函数 ID 时存在问题，可能导致某些标志位未被正确清除，从而影响后续的逻辑判断。他建议在 kvm_host_ffa_handler() 中传递标准化的 func_id，以避免重新计算带来的错误。此外，Fuad 还提到在请求和响应处理的不对称性，建议在拒绝列表中添加 FFA_FN64_MSG_SEND_DIRECT_RESP，以确保一致性。

总体来看，本周的讨论进一步明确了补丁的实施细节和需要解决的问题，为后续的修正提供了方向。

#### 📝 邮件列表

1. **[05-19 12:59]** Re: [PATCH v6 2/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ2 in
 host handler
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[05-19 13:29]** Re: [PATCH v6 1/2] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ in
 host handler
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 28: [PATCH v3 0/4] KVM: arm64: vgic: Fix IGROUPR writability and IIDR revision control

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 11 May 2026 12:30:42 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic（虚拟中断控制器）修复补丁，主要集中在 IGROUPR 的可写性和 IIDR 版本控制问题。

**原始 patch/问题的内容**：
该补丁系列旨在修复 GICv2/v3 的 IGROUPR 可写性模型，使其能够根据 GICD_IIDR 实现版本一致地进行控制，取代之前的 ad-hoc v2_groups_user_writable 标志。这一改动是为了确保在主机内核升级或降级时，能够保持精确的客户机兼容性。

**之前讨论要点**：
在历史讨论中，David Woodhouse 强调了维护客户机兼容性的重要性，指出这不仅是必要的，而且在某些情况下，回滚也是不可避免的。此外，他提到在其他讨论中，关于 KVM 是否应该在不同版本的主机内核之间维护客户机兼容性的问题也在进行讨论。

**本周的新讨论、进展或结论**：
在本周的讨论中，David Woodhouse 询问是否对该补丁系列有任何技术反馈，并表示他已处理了 Marc 对 v1 版本的反馈。他希望能获得更多的技术意见以推动补丁的进一步完善。

#### 📝 邮件列表

1. **[05-11 12:30]** [PATCH v3 0/4] KVM: arm64: vgic: Fix IGROUPR writability and IIDR revision control
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[05-18 14:56]** Re: [PATCH v3 0/4] KVM: arm64: vgic: Fix IGROUPR writability and
 IIDR revision control
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 29: [PATCH kvmtool v7 0/6] arm64: Nested virtualization support

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 18 May 2026 12:48:15 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于在 arm64 架构上实现嵌套虚拟化支持的补丁（patch），该补丁为 kvmtool 的第七版（v7），共包含六个部分。补丁的主要目的是增强 arm64 平台的虚拟化能力，使其能够支持更复杂的虚拟化场景。

在之前的讨论中，参与者对该补丁的内容表示认可，但指出补丁与其他最近的更改存在轻微冲突。因此，建议补丁的作者 Andre Przywara 进行重基（rebase）并重新提交，以便能够顺利应用。

在本周的新讨论中，Will Deacon 对补丁表示赞同，并请求 Andre 进行重基处理。Andre 随后回应表示会尽快处理并重新发送补丁。整体来看，本周的讨论主要集中在补丁的冲突解决和后续提交上，显示出参与者之间的积极沟通与合作。

#### 📝 邮件列表

1. **[05-18 12:48]** Re: [PATCH kvmtool v7 0/6] arm64: Nested virtualization support
   - 发件人: Will Deacon <will@kernel.org>
2. **[05-18 14:44]** Re: [PATCH kvmtool v7 0/6] arm64: Nested virtualization support
   - 发件人: Andre Przywara <andre.przywara@arm.com>

---

### Thread 30: [PATCH] KVM: arm64: Fix meta-page unsharing in pKVM hyp tracing

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 21 May 2026 10:09:39 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复 pKVM hyp 跟踪中的元页面（meta-page）解除共享的问题。

原始补丁的内容是修复 hyp_trace_buffer_unshare_hyp() 函数中的一个错误，确保在解除共享时能够正确处理所有之前共享的页面，以避免内存泄漏。补丁通过调用 __unshare_page() 函数来解除对元页面的共享，确保所有共享页面都被正确解除。

在之前的讨论中，虽然没有具体的邮件记录，但可以推测该问题的背景与 KVM 的内存管理和跟踪机制有关，特别是在处理 nVHE/pKVM hyp 的情况下，确保内存的有效利用和避免泄漏是非常重要的。

本周的新讨论中，Vincent Donnefort 提出了这一补丁，并详细说明了修复的必要性和实现方式。他指出，之前的实现存在一个拼写错误，导致未能正确解除共享页面。此次补丁的提交旨在解决这一问题，并附上了相关的代码修改。

总结来看，本周的讨论集中在修复 KVM arm64 架构下的内存管理问题，确保了系统的稳定性和资源的有效利用。

#### 📝 邮件列表

1. **[05-21 10:09]** [PATCH] KVM: arm64: Fix meta-page unsharing in pKVM hyp tracing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 31: [PATCH] KVM: arm64: Fix CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 20 May 2026 23:08:30 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复 CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC 配置中的一个拼写错误。该错误导致在 __hyp_do_panic 函数中无法正确禁用阶段2，从而使得 pKVM 的回溯信息变得不可靠。

在历史讨论中，没有提供具体的背景信息或之前的讨论内容，因此我们只能从本周的新讨论中获取信息。Vincent Donnefort 提出了这个补丁，指出了在之前的提交（9019e82c7e46）中引入的拼写错误，并提供了修复方案。补丁通过修正条件编译指令中的拼写错误（将 `PKVM_DISABLE_STAGE2_ON_PANIC` 改为 `CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC`）来确保在发生 panic 时能够正确禁用主机的阶段2。

本周的讨论集中在这个补丁的必要性和修复效果上，Vincent 作为提交者，明确了补丁的目的和重要性。整体来看，此次讨论强调了对 KVM 功能稳定性的重要性，确保在系统出现问题时能够提供可靠的调试信息。

#### 📝 邮件列表

1. **[05-20 23:08]** [PATCH] KVM: arm64: Fix CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 32: [PATCH AUTOSEL 7.0-6.12] KVM: arm64: nv: Consider the DS bit when translating TCR_EL2

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 20 May 2026 07:18:47 -0400

#### 🤖 AI 总结

本周讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的一个补丁，旨在解决 nVHE（Non-Virtualized Hypervisor Extension）L1 虚拟机在使用 52 位虚拟地址时无法启动的问题。该补丁的核心内容是考虑在将 TCR_EL2（Translation Control Register EL2）翻译为 TCR_EL1 时保留 DS（Data Sharing）位。

在历史讨论中，补丁的背景是由于在处理 TCR_EL2 的写入时，未能正确传递由虚拟机设置的 DS 位，导致出现重复的级别 0 故障，从而无法成功启动虚拟机。补丁通过在翻译函数中添加对 DS 位的处理，修复了这一逻辑错误。

本周的讨论中，补丁得到了确认并被标记为适用于稳定版本，参与者指出该补丁是一个简单且必要的修复，能够解决影响 ARM64 KVM 用户的实际启动失败问题。补丁的修改仅涉及一行代码，且不会引入新的功能或 API，因此风险极低。维护者 Marc Zyngier 和其他相关人员已对此补丁表示支持，预计将很快合并到主线代码中。

#### 📝 邮件列表

1. **[05-20 07:18]** [PATCH AUTOSEL 7.0-6.12] KVM: arm64: nv: Consider the DS bit when translating TCR_EL2
   - 发件人: Sasha Levin <sashal@kernel.org>

---

### Thread 33: [PATCH v7 00/17] kvmtool: arm64: Handle PSCI calls in userspace

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 18 May 2026 12:46:35 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 kvmtool 中处理 ARM64 平台的 PSCI 调用的补丁（PATCH v7 00/17）。该补丁旨在增强 kvmtool 的功能，使其能够在用户空间处理 PSCI（电源状态协调接口）调用。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁系列是针对 ARM64 架构的 kvmtool 进行的功能扩展，特别是与电源管理相关的操作。补丁包括对 PSCI 定义的更新、头文件的同步和多个 PSCI 功能的实现，如 CPU_SUSPEND、CPU_ON 和系统关机等。

在本周的新讨论中，参与者 Will Deacon 确认已将该补丁应用到 kvmtool 的主分支，并感谢贡献者 Suzuki K Poulose。补丁的具体内容包括 17 个子补丁，涵盖了从头文件更新到 PSCI 功能实现的各个方面，显示出该补丁在提升 kvmtool 的 ARM64 支持能力方面的重要性。

总之，该补丁系列的成功应用标志着 kvmtool 在处理 ARM64 PSCI 调用方面的一个重要进展。

#### 📝 邮件列表

1. **[05-18 12:46]** Re: [PATCH v7 00/17] kvmtool: arm64: Handle PSCI calls in userspace
   - 发件人: Will Deacon <will@kernel.org>

---

## 📌 RFC

共 3 个 thread

---

### Thread 1: [RFC PATCH 0/2] Optimize S2 page splitting

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 15 May 2026 20:59:01 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于优化 S2 页拆分的补丁（patch），由 Leonardo Bras 提出。补丁的主要目的是通过引入新的返回值来优化页表遍历，减少不必要的遍历步骤，从而提高性能。历史讨论中，Leonardo 介绍了补丁的基本思路，并得到了 Marc Zyngier 的反馈，Marc 指出在软件模型上进行性能测量可能不够准确，建议在实际硬件上进行测试。

在本周的新讨论中，参与者们对补丁进行了深入探讨。Oliver Upton 提出了使用新的遍历标志替代返回值的建议，以简化逻辑。Will Deacon 也提出了限制遍历最大层级的想法，认为这样可以避免复杂性。Leonardo 对这些建议表示感谢，并进一步讨论了如何避免不必要的遍历，尤其是在处理新创建的页表时。

总体来看，本周的讨论集中在如何优化补丁的实现细节上，参与者们提出了多种建议，旨在提高性能并简化代码逻辑。

#### 📝 邮件列表

1. **[05-15 20:59]** [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[05-15 20:59]** [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[05-16 10:15]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-18 00:22]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[05-18 09:52]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Will Deacon <will@kernel.org>
6. **[05-18 14:45]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[05-18 15:09]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[05-19 13:43]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Will Deacon <will@kernel.org>
9. **[05-19 13:56]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[05-19 14:15]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Will Deacon <will@kernel.org>
11. **[05-19 15:35]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[05-19 14:21]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[05-20 12:49]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 2: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 13 May 2026 16:33:43 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个名为“命名 CPU 模型”的 RFC 补丁，旨在为 ARM64 KVM 客户端引入命名的 CPU 模型，以支持跨主机的实时迁移和对客户机可见 CPU 特性的管理。

在历史讨论中，Shaju Abraham 提出了该补丁的基本概念，强调命名 CPU 模型对于管理和迁移的重要性，并给出了使用示例。

本周的新讨论中，Eric Auger 和 Khushit Shah 对补丁的实现细节提出了多个问题和建议。Eric 质疑命名模型中硬编码值的必要性，认为可以通过注释来替代命名字符串。他还询问了如何确保用户能够理解和使用这些命名值。Khushit 则回应了关于 CPU 特性与 ARM ARM 定义的复杂性，并强调了使用内核定义的安全值标签的重要性，以确保 KVM 在实现时不会超出主机的能力。

此外，讨论中提到需要为每个命名模型提供单独的补丁，并在文档中清晰说明覆盖和参考规范的链接。双方都同意需要进一步合作，以确保命名模型的实现符合社区的期望，并能够有效支持未来的迁移需求。

#### 📝 邮件列表

1. **[05-13 16:33]** [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
2. **[05-18 12:27]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-20 13:08]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
4. **[05-20 17:27]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-22 07:59]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 3: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via
 connect/disconnect callbacks

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 18 May 2026 13:59:39 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为「coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks」的 RFC PATCH v4。这一补丁旨在通过连接/断开回调在主机端设置 Arm CCA IDE。

在之前的讨论中，参与者们探讨了该补丁中 RMI 相关的头文件位置问题。Will Deacon 提出，是否可以将这些代码移至 drivers/firmware/ 或 include/linux/arm-rmi.h，以避免将其放在架构代码中。Aneesh Kumar K.V 解释说，这些头文件是为了收集所有与 RMI 相关的助手和定义，并提到如果将 RMI 助手移至更通用的头文件，将需要同时移动 KVM 使用的所有助手，以避免出现两个不同的头文件。

在本周的新讨论中，Suzuki K Poulose 赞同将 RMI 接口移至 drivers/firmware，认为这样可以与其他固件接口代码共存，并减轻架构维护者对驱动代码变更的关注。Will Deacon 也表示支持这一观点，认为这将使代码结构更加清晰。

总体来看，本周的讨论集中在 RMI 相关代码的组织和位置上，参与者们倾向于将其移至更合适的目录，以便于管理和维护。

#### 📝 邮件列表

1. **[05-18 13:59]** Re: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via
 connect/disconnect callbacks
   - 发件人: Will Deacon <will@kernel.org>
2. **[05-18 21:23]** Re: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via
 connect/disconnect callbacks
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
3. **[05-19 09:24]** Re: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via
 connect/disconnect callbacks
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[05-19 10:46]** Re: [RFC PATCH v4 00/14] coco/TSM: Host-side Arm CCA IDE setup via
 connect/disconnect callbacks
   - 发件人: Will Deacon <will@kernel.org>

---

## 📌 Bug Report

共 1 个 thread

---

### Thread 1: [RESEND v3 0/3] Fix __pkvm_init_vm error path

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 21 May 2026 15:36:23 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的一个补丁，旨在修复 `__pkvm_init_vm` 函数中的错误路径问题。该补丁主要解决了在 `insert_vm_table_entry` 失败时可能导致的引用计数泄漏问题。

在历史讨论中，Sashiko 报告了一个潜在的引用计数泄漏问题，触发了对 `__pkvm_init_vm` 和相关函数的审查。之前的讨论集中在如何确保在虚拟机初始化失败时，能够正确释放主机捐赠的内存，并避免引用计数未被正确管理。

本周的讨论中，Vincent Donnefort 提出了三个补丁：首先是重置 pKVM hyp_pool 中页面的顺序，以确保在虚拟机初始化失败时能够正确处理页面的引用计数；其次是修复 `__pkvm_init_vm` 的错误路径，确保在失败时调用 `kvm_guest_destroy_stage2` 来释放资源；最后，增加了对引用计数页面的安全检查，以防止在状态机中出现潜在问题。这些补丁得到了 Fuad Tabba 的审核和测试确认，显示出积极的进展。

#### 📝 邮件列表

1. **[05-21 15:36]** [RESEND v3 0/3] Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-21 15:36]** [RESEND v3 1/3] KVM: arm64: Reset page order in pKVM hyp_pool
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-21 15:36]** [RESEND v3 2/3] KVM: arm64: Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[05-21 15:36]** [RESEND v3 3/3] KVM: arm64: Add fail-safe for refcounted pages in __pkvm_hyp_donate_host
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[05-22 07:53]** Re: [RESEND v3 1/3] KVM: arm64: Reset page order in pKVM hyp_pool
   - 发件人: Fuad Tabba <tabba@google.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #3

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 20 May 2026 08:25:18 +0100

#### 🤖 AI 总结

本邮件线程讨论了 KVM/arm64 在 7.1 版本中的一系列修复补丁。Marc Zyngier 提交了一个包含多个修复的补丁集，主要针对 KVM/arm64 的稳定性和性能改进。

在本周的讨论中，Marc 提到本次补丁集包括两个基于 AI 的修复，均为稳定候选项。此外，还对虚拟化监控器跟踪描述符的验证进行了小幅整理。具体修复内容包括：修复中断翻译表恢复时的 ITS EventID 清理问题、在初始化 vcpu 失败时修复 PPI 内存泄漏、以及在虚拟化监控器跟踪描述符验证失败时正确返回错误，并将此验证限制在受保护模式下。

Paolo Bonzini 对补丁集表示确认并表示感谢，表示已完成相关处理。

总的来说，本周的讨论主要集中在 KVM/arm64 的修复补丁上，Marc 提交的补丁集得到了确认，标志着向 7.1 版本的稳定性提升迈出了重要一步。

#### 📝 邮件列表

1. **[05-20 08:25]** [GIT PULL] KVM/arm64 fixes for 7.1, take #3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-23 10:03]** Re: [GIT PULL] KVM/arm64 fixes for 7.1, take #3
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Discussion

共 2 个 thread

---

### Thread 1: [kvm-unit-tests PATCH v2 6/7] lib: arm64: Add guest-internal
 exception handling (EL1)

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 20 May 2026 15:51:46 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM 单元测试中为 ARM64 架构添加内部异常处理的补丁（patch）。该补丁的目标是增强对 EL1 级别异常的处理能力。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁的初衷是为了改进 ARM64 虚拟化环境下的异常处理机制，特别是在处理 EL1h 异常时的能力。

在本周的新讨论中，参与者 Joey Gouly 对补丁提出了几点改进建议。首先，他指出当前的实现仅处理 EL1h 异常，建议扩展到处理完整的 16 个异常向量。其次，他提到当前结构体的大小为 264 字节，不符合 16 字节对齐的惯例，建议添加一个虚拟字段以确保对齐。此外，他还建议在 `lib/arm64/asm-offsets.c` 中添加一个宏定义，以避免在汇编中硬编码结构体大小。

总体来看，本周的讨论集中在补丁的细节优化上，旨在提升 ARM64 虚拟化环境下的异常处理能力。

#### 📝 邮件列表

1. **[05-20 15:51]** Re: [kvm-unit-tests PATCH v2 6/7] lib: arm64: Add guest-internal
 exception handling (EL1)
   - 发件人: Joey Gouly <joey.gouly@arm.com>
2. **[05-20 16:49]** Re: [kvm-unit-tests PATCH v2 6/7] lib: arm64: Add guest-internal
 exception handling (EL1)
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 2: [kvm-unit-tests PATCH v2 4/7] lib: arm64: Add foundational guest
 execution framework

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 20 May 2026 16:17:38 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM 单元测试中为 ARM64 架构添加基础的来宾执行框架的补丁（PATCH v2 4/7）。该补丁的主要内容是覆盖 EL2 级别的 HCR 寄存器，但目前并没有保存或恢复主机的 HCR 值。

在之前的讨论中，参与者们关注如何有效地管理主机和来宾之间的寄存器状态，尤其是 HCR 寄存器的处理。当前的实现仅在进入来宾时修改 HCR，而未考虑在退出时恢复主机的状态，这可能会导致状态不一致。

在本周的新讨论中，参与者 Joey Gouly 提出了一个建议，建议引入一个 `host_state` 结构体来存储可能影响主机的寄存器和状态，并将其嵌入到 `struct guest` 中，以便在需要时进行保存和恢复。这一建议旨在解决当前实现中的状态管理问题，确保主机和来宾之间的寄存器状态能够正确切换。

#### 📝 邮件列表

1. **[05-20 16:17]** Re: [kvm-unit-tests PATCH v2 4/7] lib: arm64: Add foundational guest
 execution framework
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

