# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-07-13 00:38:35

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 568
- **总 Thread 数**: 47
- **大型 Thread** (>20封): 8 个

### 分类分布

- **PATCH**: 41 threads (525 邮件)
- **RFC**: 2 threads (21 邮件)
- **Question**: 1 threads (12 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Discussion**: 1 threads (8 邮件)
- **Other**: 1 threads (1 邮件)

---

## 📌 PATCH

共 41 个 thread

---

### Thread 1: [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 71 | **👥 参与者**: 7 | **📅 开始时间**: Mon,  6 Jul 2026 10:52:00 +0200

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在 s390 架构上引入 arm64 KVM 支持的补丁系列（PATCH v4 00/27）。以下是对讨论内容的总结：

1. **原始补丁内容**：该补丁系列旨在重构 s390 和 arm64 之间的代码共享方式，采用新的方法在构建时提取 arm64 定义和实现的相关部分，而不是将 arm64 代码移动到共享位置。补丁包括对 KVM 模块的清理、重构和新的 arm64 KVM 模块的引入。

2. **之前的讨论要点**：在历史讨论中，参与者们探讨了如何有效地共享代码，减少对现有 arm64 代码的影响，并确保 s390 可以在不干扰 arm64 的情况下使用这些代码。补丁的结构包括 KVM 符号清理、头文件共享准备、代码共享基础设施等。

3. **本周的新讨论和进展**：本周的讨论集中在补丁的具体实现上，包括对 KVM 设备名称的配置、移除 KVM_MMIO 配置选项、共享 arm64 头文件等。参与者们还讨论了如何处理 vCPU 的创建和销毁、实现 IOCTLs 以及基本的页面故障处理。针对每个补丁，审查者提出了潜在问题和改进建议，包括代码的可维护性、功能实现的完整性等。

总的来说，这个补丁系列的目标是为 s390 架构提供对 arm64 KVM 的支持，同时确保代码的清晰性和可维护性。参与者们积极讨论了实现细节和潜在问题，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[07-06 10:52]** [PATCH v4 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[07-06 10:52]** [PATCH v4 01/27] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[07-06 10:52]** [PATCH v4 02/27] KVM, vfio: remove symbol_get(kvm_get_kvm_safe) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[07-06 10:52]** [PATCH v4 03/27] KVM, vfio: remove symbol_get(kvm_put_kvm) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[07-06 10:52]** [PATCH v4 04/27] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[07-06 10:52]** [PATCH v4 05/27] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[07-06 10:52]** [PATCH v4 06/27] arm64: Use proper include variant
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[07-06 10:52]** [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[07-06 10:52]** [PATCH v4 08/27] KVM: arm64: Prepare sharing arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[07-06 10:52]** [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[07-06 10:52]** [PATCH v4 10/27] KVM: arm64: Refactor core-reset into a separate function
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[07-06 10:52]** [PATCH v4 11/27] s390: Use arm64 headers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[07-06 10:52]** [PATCH v4 12/27] KVM: s390: Use arm64 code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[07-06 10:52]** [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[07-06 10:52]** [PATCH v4 14/27] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[07-06 10:52]** [PATCH v4 15/27] KVM: S390: Prepare gmap for a second KVM implementation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[07-06 10:52]** [PATCH v4 16/27] KVM: s390: gmap: Refactor storage key and CMMA code into separate files
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[07-06 10:52]** [PATCH v4 17/27] KVM: s390: Refactor prefix handling into a separate file
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[07-06 10:52]** [PATCH v4 18/27] KVM: s390: Prepare kvm-s390 for a second kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[07-06 10:52]** [PATCH v4 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[07-06 10:52]** [PATCH v4 20/27] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[07-06 10:52]** [PATCH v4 21/27] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[07-06 10:52]** [PATCH v4 22/27] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[07-06 10:52]** [PATCH v4 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[07-06 10:52]** [PATCH v4 24/27] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[07-06 10:52]** [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[07-06 10:52]** [PATCH v4 26/27] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[07-06 10:52]** [PATCH v4 27/27] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[07-06 09:12]** Re: [PATCH v4 01/27] VFIO: take reference to the KVM module
   - 发件人: sashiko-bot@kernel.org
30. **[07-06 09:14]** Re: [PATCH v4 04/27] KVM: Make device name configurable
   - 发件人: sashiko-bot@kernel.org
31. **[07-06 09:21]** Re: [PATCH v4 08/27] KVM: arm64: Prepare sharing arm64 code with
 s390
   - 发件人: sashiko-bot@kernel.org
32. **[07-06 09:25]** Re: [PATCH v4 03/27] KVM, vfio: remove symbol_get(kvm_put_kvm) from
 vfio
   - 发件人: sashiko-bot@kernel.org
33. **[07-06 09:26]** Re: [PATCH v4 12/27] KVM: s390: Use arm64 code
   - 发件人: sashiko-bot@kernel.org
34. **[07-06 09:31]** Re: [PATCH v4 11/27] s390: Use arm64 headers
   - 发件人: sashiko-bot@kernel.org
35. **[07-06 09:35]** Re: [PATCH v4 14/27] KVM: s390: Move s390 kvm code into a
 subdirectory
   - 发件人: sashiko-bot@kernel.org
36. **[07-06 09:36]** Re: [PATCH v4 15/27] KVM: S390: Prepare gmap for a second KVM
 implementation
   - 发件人: sashiko-bot@kernel.org
37. **[07-06 09:51]** Re: [PATCH v4 22/27] KVM: s390: Add basic arm64 kvm module
   - 发件人: sashiko-bot@kernel.org
38. **[07-06 09:55]** Re: [PATCH v4 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: sashiko-bot@kernel.org
39. **[07-06 10:03]** Re: [PATCH v4 26/27] KVM: s390: arm64: Implement basic page fault
 handler
   - 发件人: sashiko-bot@kernel.org
40. **[07-06 10:04]** Re: [PATCH v4 24/27] KVM: s390: arm64: Implement vm/vcpu create
 destroy.
   - 发件人: sashiko-bot@kernel.org
41. **[07-06 10:07]** Re: [PATCH v4 27/27] KVM: s390: arm64: Enable KVM_ARM64 config and
 Kbuild
   - 发件人: sashiko-bot@kernel.org
42. **[07-06 10:16]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: sashiko-bot@kernel.org
43. **[07-06 13:17]** Re: [PATCH v4 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Janosch Frank <frankja@linux.ibm.com>
44. **[07-06 13:30]** Re: [PATCH v4 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>
45. **[07-06 13:50]** Re: [PATCH v4 21/27] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Janosch Frank <frankja@linux.ibm.com>
46. **[07-06 13:53]** Re: [PATCH v4 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
47. **[07-06 13:58]** Re: [PATCH v4 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
48. **[07-06 14:15]** Re: [PATCH v4 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Janosch Frank <frankja@linux.ibm.com>
49. **[07-06 18:44]** Re: [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Marc Zyngier <maz@kernel.org>
50. **[07-06 16:53]** Re: [PATCH v4 01/27] VFIO: take reference to the KVM module
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
51. **[07-06 21:35]** Re: [PATCH v4 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Marc Zyngier <maz@kernel.org>
52. **[07-06 21:53]** Re: [PATCH v4 05/27] KVM: Remove KVM_MMIO as config option
   - 发件人: Marc Zyngier <maz@kernel.org>
53. **[07-06 14:12]** Re: [PATCH v4 01/27] VFIO: take reference to the KVM module
   - 发件人: Sean Christopherson <seanjc@google.com>
54. **[07-06 22:22]** Re: [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
55. **[07-06 22:28]** Re: [PATCH v4 08/27] KVM: arm64: Prepare sharing arm64 code with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
56. **[07-07 09:20]** Re: [PATCH v4 08/27] KVM: arm64: Prepare sharing arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
57. **[07-07 09:39]** Re: [PATCH v4 01/27] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
58. **[07-07 16:10]** Re: [PATCH v4 24/27] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Marc Zyngier <maz@kernel.org>
59. **[07-08 08:51]** Re: [PATCH v4 24/27] KVM: s390: arm64: Implement vm/vcpu create
 destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
60. **[07-08 08:36]** Re: [PATCH v4 24/27] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Marc Zyngier <maz@kernel.org>
61. **[07-08 11:44]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Marc Zyngier <maz@kernel.org>
62. **[07-08 14:33]** Re: [PATCH v4 15/27] KVM: S390: Prepare gmap for a second KVM
 implementation
   - 发件人: Janosch Frank <frankja@linux.ibm.com>
63. **[07-10 10:54]** Re: [PATCH v4 05/27] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
64. **[07-10 11:22]** Re: [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM
 module
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>
65. **[07-10 11:29]** Re: [PATCH v4 15/27] KVM: S390: Prepare gmap for a second KVM
 implementation
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>
66. **[07-10 11:54]** Re: [PATCH v4 07/27] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
67. **[07-10 12:51]** Re: [PATCH v4 13/27] KVM: s390: Prepare KVM/s390 for a second KVM
 module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
68. **[07-10 13:56]** Re: [PATCH v4 09/27] KVM: arm64: Access elements of vcpu_gp_regs
 individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
69. **[07-10 14:29]** Re: [PATCH v4 15/27] KVM: S390: Prepare gmap for a second KVM
 implementation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
70. **[07-10 15:40]** Re: [PATCH v4 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
71. **[07-10 16:07]** Re: [PATCH v4 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 2: [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 52 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 3 Jul 2026 15:50:32 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构上增加 GICv5 IRS（中断路由器）支持的补丁系列。原始补丁旨在扩展 GICv5 的功能，使其能够支持 SPI（共享中断）和 LPI（本地中断），从而使 GICv5 虚拟机能够更好地运行 Linux 客户端。

在历史讨论中，参与者 Sascha Bischoff 提出了多个补丁，涵盖了 GICv5 的初始化、IRQ（中断请求）管理、虚拟机表（VMTE）和 VPE（虚拟处理单元）门铃域的创建与管理等方面。讨论中还涉及了对现有代码的潜在问题和改进建议，例如对中断状态的管理和内存分配的安全性。

在本周的新讨论中，Sascha 对之前的补丁进行了回应，确认了一些问题并提出了修复方案。他强调了在多 IRS 系统中处理指针的必要性，并对 GIC VDRCFG 指令的使用进行了澄清，指出在没有有效 VPE 的情况下使用该指令是错误的。此外，他还讨论了如何在 VPE 进入 WFI（等待中断）时请求门铃，以及对 IRS 状态的管理和同步问题。

总体而言，本周的讨论集中在补丁的细节修正和潜在问题的解决上，为 GICv5 的稳定性和功能增强奠定了基础。

#### 📝 邮件列表

1. **[07-03 15:50]** [PATCH v3 00/40] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[07-03 15:51]** [PATCH v3 01/40] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[07-03 15:51]** [PATCH v3 02/40] irqchip/gic-v5: Provide OF IRS config frame attrs to
 KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[07-03 15:53]** [PATCH v3 05/40] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[07-03 15:53]** [PATCH v3 06/40] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[07-03 15:54]** [PATCH v3 08/40] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[07-03 15:55]** [PATCH v3 09/40] KVM: arm64: gic-v5: Create and manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[07-03 15:55]** [PATCH v3 10/40] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[07-03 15:56]** [PATCH v3 11/40] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[07-03 15:57]** [PATCH v3 13/40] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[07-03 15:57]** [PATCH v3 14/40] KVM: arm64: gic-v5: Set up VMTEs and VPE doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
12. **[07-03 15:58]** [PATCH v3 15/40] KVM: arm64: gic-v5: Add resident/non-resident hyp
 calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
13. **[07-03 15:58]** [PATCH v3 16/40] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
14. **[07-03 16:00]** [PATCH v3 20/40] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
15. **[07-03 16:01]** [PATCH v3 22/40] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
16. **[07-03 16:02]** [PATCH v3 23/40] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
17. **[07-03 16:03]** [PATCH v3 26/40] KVM: arm64: gic-v5: Add GIC VDPEND and GIC VDRCFG
 hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
18. **[07-03 16:04]** [PATCH v3 28/40] KVM: arm64: gic: Introduce set_pending_state() to
 irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
19. **[07-03 16:22]** Re: [PATCH v3 06/40] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: sashiko-bot@kernel.org
20. **[07-03 16:23]** Re: [PATCH v3 15/40] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: sashiko-bot@kernel.org
21. **[07-03 16:24]** Re: [PATCH v3 02/40] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: sashiko-bot@kernel.org
22. **[07-03 16:25]** Re: [PATCH v3 08/40] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: sashiko-bot@kernel.org
23. **[07-03 16:26]** Re: [PATCH v3 13/40] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: sashiko-bot@kernel.org
24. **[07-03 16:27]** Re: [PATCH v3 14/40] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: sashiko-bot@kernel.org
25. **[07-03 16:28]** Re: [PATCH v3 05/40] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: sashiko-bot@kernel.org
26. **[07-03 16:31]** Re: [PATCH v3 26/40] KVM: arm64: gic-v5: Add GIC VDPEND and GIC
 VDRCFG hyp calls
   - 发件人: sashiko-bot@kernel.org
27. **[07-03 16:31]** Re: [PATCH v3 09/40] KVM: arm64: gic-v5: Create and manage VM and
 VPE tables
   - 发件人: sashiko-bot@kernel.org
28. **[07-03 16:32]** Re: [PATCH v3 28/40] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: sashiko-bot@kernel.org
29. **[07-03 16:33]** Re: [PATCH v3 01/40] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: sashiko-bot@kernel.org
30. **[07-03 16:34]** Re: [PATCH v3 23/40] KVM: arm64: gic-v5: Set IRICHPPIDIS based on
 IRS enable state
   - 发件人: sashiko-bot@kernel.org
31. **[07-03 16:34]** Re: [PATCH v3 10/40] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: sashiko-bot@kernel.org
32. **[07-03 16:35]** Re: [PATCH v3 16/40] KVM: arm64: gic-v5: Request doorbells when
 VPEs enter WFI
   - 发件人: sashiko-bot@kernel.org
33. **[07-03 16:38]** Re: [PATCH v3 20/40] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and
 MMIO emulation
   - 发件人: sashiko-bot@kernel.org
34. **[07-03 16:39]** Re: [PATCH v3 11/40] KVM: arm64: gic-v5: Implement VMT/vIST IRS
 MMIO Ops
   - 发件人: sashiko-bot@kernel.org
35. **[07-03 16:47]** Re: [PATCH v3 22/40] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: sashiko-bot@kernel.org
36. **[07-07 12:30]** Re: [PATCH v3 01/40] irqchip/gic-v5: Allow KVM setup without a
 maintenance IRQ
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
37. **[07-07 12:48]** Re: [PATCH v3 02/40] irqchip/gic-v5: Provide OF IRS config frame
 attrs to KVM
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
38. **[07-07 14:28]** Re: [PATCH v3 05/40] arm64/sysreg: Add GICv5 GIC VDPEND and VDRCFG
 encodings
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
39. **[07-07 15:08]** Re: [PATCH v3 06/40] arm64/sysreg: Update ICC_CR0_EL1 with LINK and
 LINK_IDLE fields
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
40. **[07-07 15:11]** Re: [PATCH v3 08/40] KVM: arm64: gic-v5: Add VPE doorbell domain
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
41. **[07-08 14:44]** Re: [PATCH v3 09/40] KVM: arm64: gic-v5: Create and manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
42. **[07-08 14:46]** Re: [PATCH v3 10/40] KVM: arm64: gic-v5: Introduce guest IST alloc
 and management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
43. **[07-08 14:49]** Re: [PATCH v3 11/40] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO
 Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
44. **[07-08 14:53]** Re: [PATCH v3 13/40] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
45. **[07-08 14:56]** Re: [PATCH v3 14/40] KVM: arm64: gic-v5: Set up VMTEs and VPE
 doorbells
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
46. **[07-08 15:00]** Re: [PATCH v3 15/40] KVM: arm64: gic-v5: Add resident/non-resident
 hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
47. **[07-08 15:35]** Re: [PATCH v3 16/40] KVM: arm64: gic-v5: Request doorbells when VPEs
 enter WFI
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
48. **[07-09 09:28]** Re: [PATCH v3 20/40] KVM: arm64: gic-v5: Add GICv5 IRS IODEV and MMIO
 emulation
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
49. **[07-09 09:55]** Re: [PATCH v3 22/40] KVM: arm64: gic-v5: Register the IRS IODEV
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
50. **[07-09 11:39]** Re: [PATCH v3 23/40] KVM: arm64: gic-v5: Set IRICHPPIDIS based on IRS
 enable state
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
51. **[07-10 09:44]** Re: [PATCH v3 26/40] KVM: arm64: gic-v5: Add GIC VDPEND and GIC
 VDRCFG hyp calls
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
52. **[07-10 09:51]** Re: [PATCH v3 28/40] KVM: arm64: gic: Introduce set_pending_state()
 to irq_op
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 3: [PATCH v11 00/29] KVM: arm64: Implement support for SME

**📧 邮件数**: 39 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 09 Jul 2026 01:51:37 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现对 SME（Scalable Matrix Extension）的支持，包含了 29 个补丁的详细内容。

**1. 原始补丁/问题的内容：**
补丁的主要目的是在 KVM 中实现对 SME 的支持，允许在非保护的 KVM 客户端中使用 SME。SME 引入了新的向量长度和控制寄存器，类似于 SVE（Scalable Vector Extension），并且在某些情况下，SME 可以独立于 SVE 使用。

**2. 之前的讨论要点：**
在历史讨论中，参与者关注了用户空间 ABI 的设计，特别是如何处理 SVE 和 SME 的寄存器访问，以及如何在不同状态下（如流模式）配置向量长度。补丁还讨论了如何在 KVM 中处理 SME 的控制寄存器和状态。

**3. 本周的新讨论、进展或结论：**
本周的讨论集中在补丁的具体实现上，包括对 SME 状态的上下文切换支持、寄存器访问控制、异常处理以及如何在嵌套客户机中暴露 SME。补丁还提供了对 SME 特定寄存器的用户空间访问支持，并确保在写入 SVCR（SME 控制寄存器）时正确处理状态变化。此外，参与者讨论了如何在 KVM 中配置和启用 SME，确保在最终化后不再允许更改 SVE 和 SME 的配置。

最后，补丁经过多次修改，参与者对其进行了审查和测试，确保在不同的虚拟化模式下（如 nVHE 和 VHE）都能正常工作。

#### 📝 邮件列表

1. **[07-09 01:51]** [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-09 01:51]** [PATCH v11 01/29] arm64/sysreg: Define full value
 read/modify/write helpers
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-09 01:51]** [PATCH v11 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-09 01:51]** [PATCH v11 03/29] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-09 01:51]** [PATCH v11 04/29] arm64/sve: Factor virtualizable VL discovery out
 of SVE specific code
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-09 01:51]** [PATCH v11 05/29] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[07-09 01:51]** [PATCH v11 06/29] KVM: arm64: Handle FEAT_IDST for guest accesses
 to hidden registers
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[07-09 01:51]** [PATCH v11 07/29] KVM: arm64: Pull ctxt_has_ helpers to start of
 sysreg-sr.h
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[07-09 01:51]** [PATCH v11 08/29] KVM: arm64: Rename SVE finalization constants to
 be more general
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-09 01:51]** [PATCH v11 09/29] KVM: arm64: Define internal features for SME
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[07-09 01:51]** [PATCH v11 10/29] KVM: arm64: Rename sve_state_reg_region
   - 发件人: Mark Brown <broonie@kernel.org>
12. **[07-09 01:51]** [PATCH v11 11/29] KVM: arm64: Store vector lengths in an array
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[07-09 01:51]** [PATCH v11 12/29] KVM: arm64: Factor SVE code out of
 fpsimd_lazy_switch_to_host()
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[07-09 01:51]** [PATCH v11 13/29] KVM: arm64: Document the KVM ABI for SME
   - 发件人: Mark Brown <broonie@kernel.org>
15. **[07-09 01:51]** [PATCH v11 14/29] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[07-09 01:51]** [PATCH v11 15/29] KVM: arm64: Support SME control registers
   - 发件人: Mark Brown <broonie@kernel.org>
17. **[07-09 01:51]** [PATCH v11 16/29] KVM: arm64: Support TPIDR2_EL0
   - 发件人: Mark Brown <broonie@kernel.org>
18. **[07-09 01:51]** [PATCH v11 17/29] KVM: arm64: Support SME identification registers
 for guests
   - 发件人: Mark Brown <broonie@kernel.org>
19. **[07-09 01:51]** [PATCH v11 18/29] KVM: arm64: Support SME priority registers
   - 发件人: Mark Brown <broonie@kernel.org>
20. **[07-09 01:51]** [PATCH v11 19/29] KVM: arm64: Support userspace access to
 streaming mode Z and P registers
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[07-09 01:51]** [PATCH v11 20/29] KVM: arm64: Flush register state on writes to
 SVCR.SM and SVCR.ZA
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[07-09 01:51]** [PATCH v11 21/29] KVM: arm64: Expose SME specific state to
 userspace
   - 发件人: Mark Brown <broonie@kernel.org>
23. **[07-09 01:51]** [PATCH v11 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Mark Brown <broonie@kernel.org>
24. **[07-09 01:52]** [PATCH v11 23/29] KVM: arm64: Handle SME exceptions
   - 发件人: Mark Brown <broonie@kernel.org>
25. **[07-09 01:52]** [PATCH v11 24/29] KVM: arm64: Expose SME to nested guests
   - 发件人: Mark Brown <broonie@kernel.org>
26. **[07-09 01:52]** [PATCH v11 25/29] KVM: arm64: Provide interface for configuring
 and enabling SME for guests
   - 发件人: Mark Brown <broonie@kernel.org>
27. **[07-09 01:52]** [PATCH v11 26/29] KVM: arm64: selftests: Remove spurious check for
 single bit safe values
   - 发件人: Mark Brown <broonie@kernel.org>
28. **[07-09 01:52]** [PATCH v11 27/29] KVM: arm64: selftests: Skip impossible invalid
 value tests
   - 发件人: Mark Brown <broonie@kernel.org>
29. **[07-09 01:52]** [PATCH v11 28/29] KVM: arm64: selftests: Add SME system registers
 to get-reg-list
   - 发件人: Mark Brown <broonie@kernel.org>
30. **[07-09 01:52]** [PATCH v11 29/29] KVM: arm64: selftests: Add SME to set_id_regs
 test
   - 发件人: Mark Brown <broonie@kernel.org>
31. **[07-09 11:26]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
32. **[07-09 12:28]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Rutland <mark.rutland@arm.com>
33. **[07-09 12:31]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[07-09 12:36]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
35. **[07-09 12:43]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
36. **[07-09 12:49]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
37. **[07-09 12:49]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Rutland <mark.rutland@arm.com>
38. **[07-09 13:08]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
39. **[07-09 13:21]** Re: [PATCH v11 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 4: [PATCH v12 00/29] KVM: arm64: Implement support for SME

**📧 邮件数**: 34 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 09 Jul 2026 19:27:21 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在 KVM（内核虚拟机）中实现对 ARM64 SME（可扩展矩阵扩展）的支持，主要集中在一系列补丁的提交和讨论。

1. **原始补丁内容**：补丁系列的核心是实现对 SME 的支持，特别是在非保护模式的 KVM 客户中。SME 引入了新的向量长度和控制寄存器，类似于 SVE（可扩展向量扩展），并允许在流模式下使用 SVE 寄存器。

2. **历史讨论要点**：之前的讨论主要围绕如何处理 SME 的 ABI（应用程序二进制接口），以及如何在用户空间和内核之间有效管理寄存器访问。补丁的设计考虑了与 SVE 的兼容性，确保在最终化时不会引入复杂性。

3. **本周新讨论和进展**：本周的讨论集中在补丁的测试和验证上。参与者报告了在不同的主机配置（如 VHE 和 nVHE 模式）下，正常和保护客户的启动情况良好。补丁通过了对 ID 寄存器和寄存器列表的测试，确保了新添加的 SME 寄存器的可见性和功能。此外，讨论中提到需要在未来的补丁中处理 SME 特定的寄存器访问和异常处理。

总的来说，这一系列补丁的实施标志着 KVM 在 ARM64 平台上对新硬件特性的支持，尤其是 SME 的引入，进一步增强了虚拟化能力。

#### 📝 邮件列表

1. **[07-09 19:27]** [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[07-09 19:27]** [PATCH v12 01/29] arm64/sysreg: Define full value
 read/modify/write helpers
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[07-09 19:27]** [PATCH v12 02/29] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[07-09 19:27]** [PATCH v12 03/29] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[07-09 19:27]** [PATCH v12 04/29] arm64/sve: Factor virtualizable VL discovery out
 of SVE specific code
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[07-09 19:27]** [PATCH v12 05/29] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[07-09 19:27]** [PATCH v12 06/29] KVM: arm64: Handle FEAT_IDST for guest accesses
 to hidden registers
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[07-09 19:27]** [PATCH v12 07/29] KVM: arm64: Pull ctxt_has_ helpers to start of
 sysreg-sr.h
   - 发件人: Mark Brown <broonie@kernel.org>
9. **[07-09 19:27]** [PATCH v12 08/29] KVM: arm64: Rename SVE finalization constants to
 be more general
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[07-09 19:27]** [PATCH v12 09/29] KVM: arm64: Define internal features for SME
   - 发件人: Mark Brown <broonie@kernel.org>
11. **[07-09 19:27]** [PATCH v12 10/29] KVM: arm64: Rename sve_state_reg_region
   - 发件人: Mark Brown <broonie@kernel.org>
12. **[07-09 19:27]** [PATCH v12 11/29] KVM: arm64: Store vector lengths in an array
   - 发件人: Mark Brown <broonie@kernel.org>
13. **[07-09 19:27]** [PATCH v12 12/29] KVM: arm64: Factor SVE code out of
 fpsimd_lazy_switch_to_host()
   - 发件人: Mark Brown <broonie@kernel.org>
14. **[07-09 19:27]** [PATCH v12 13/29] KVM: arm64: Document the KVM ABI for SME
   - 发件人: Mark Brown <broonie@kernel.org>
15. **[07-09 19:27]** [PATCH v12 14/29] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Mark Brown <broonie@kernel.org>
16. **[07-09 19:27]** [PATCH v12 15/29] KVM: arm64: Support SME control registers
   - 发件人: Mark Brown <broonie@kernel.org>
17. **[07-09 19:27]** [PATCH v12 16/29] KVM: arm64: Support TPIDR2_EL0
   - 发件人: Mark Brown <broonie@kernel.org>
18. **[07-09 19:27]** [PATCH v12 17/29] KVM: arm64: Support SME identification registers
 for guests
   - 发件人: Mark Brown <broonie@kernel.org>
19. **[07-09 19:27]** [PATCH v12 18/29] KVM: arm64: Support SME priority registers
   - 发件人: Mark Brown <broonie@kernel.org>
20. **[07-09 19:27]** [PATCH v12 19/29] KVM: arm64: Support userspace access to
 streaming mode Z and P registers
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[07-09 19:27]** [PATCH v12 20/29] KVM: arm64: Flush register state on writes to
 SVCR.SM and SVCR.ZA
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[07-09 19:27]** [PATCH v12 21/29] KVM: arm64: Expose SME specific state to
 userspace
   - 发件人: Mark Brown <broonie@kernel.org>
23. **[07-09 19:27]** [PATCH v12 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Mark Brown <broonie@kernel.org>
24. **[07-09 19:27]** [PATCH v12 23/29] KVM: arm64: Handle SME exceptions
   - 发件人: Mark Brown <broonie@kernel.org>
25. **[07-09 19:27]** [PATCH v12 24/29] KVM: arm64: Expose SME to nested guests
   - 发件人: Mark Brown <broonie@kernel.org>
26. **[07-09 19:27]** [PATCH v12 25/29] KVM: arm64: Provide interface for configuring
 and enabling SME for guests
   - 发件人: Mark Brown <broonie@kernel.org>
27. **[07-09 19:27]** [PATCH v12 26/29] KVM: arm64: selftests: Remove spurious check for
 single bit safe values
   - 发件人: Mark Brown <broonie@kernel.org>
28. **[07-09 19:27]** [PATCH v12 27/29] KVM: arm64: selftests: Skip impossible invalid
 value tests
   - 发件人: Mark Brown <broonie@kernel.org>
29. **[07-09 19:27]** [PATCH v12 28/29] KVM: arm64: selftests: Add SME system registers
 to get-reg-list
   - 发件人: Mark Brown <broonie@kernel.org>
30. **[07-09 19:27]** [PATCH v12 29/29] KVM: arm64: selftests: Add SME to set_id_regs
 test
   - 发件人: Mark Brown <broonie@kernel.org>
31. **[07-10 09:43]** Re: [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
32. **[07-12 15:03]** Re: [PATCH v12 00/29] KVM: arm64: Implement support for SME
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
33. **[07-12 15:12]** Re: [PATCH v12 04/29] arm64/sve: Factor virtualizable VL discovery
 out of SVE specific code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[07-12 15:40]** Re: [PATCH v12 22/29] KVM: arm64: Context switch SME state for guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 5: [PATCH v2 00/18] KVM: arm64: Introduce pKVM hypervisor heap allocator

**📧 邮件数**: 27 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 18:53:57 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM 超级管理程序的动态内存分配器的补丁系列（PATCH v2 00/18）。该补丁系列的主要目标是引入一个新的堆分配器（hyp_allocator），以解决 pKVM 之前缺乏动态内存分配的问题。

**原始问题**：
pKVM 之前的设计要求所有虚拟机（VM）和虚拟 CPU（VCPU）结构在主机上预先分配并捐赠给超级管理程序，这导致了内存使用的紧密耦合和扩展性限制。

**历史讨论要点**：
之前的讨论集中在如何实现动态分配器的基本构件，包括处理内存不足的请求、动态映射物理页面、以及在主机内存压力下回收未使用的内存等。

**本周新讨论及进展**：
1. **新补丁**：引入了多个补丁，逐步实现了堆分配器的功能，包括内存分配、回收、以及与主机的交互接口。
2. **自测**：添加了自测功能，以确保堆分配器的核心机制正常工作。
3. **内存回收**：实现了与主机内存管理子系统的集成，允许在主机内存压力下自动回收未使用的内存。
4. **代码审查**：Sashiko AI 进行了代码审查，提出了若干潜在问题，包括内存对齐和内存管理的安全性等。

整体来看，这一系列补丁旨在提升 pKVM 的内存管理能力，增强其可扩展性和性能，同时确保系统的稳定性和安全性。

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
20. **[07-06 18:12]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM
 hyp
   - 发件人: sashiko-bot@kernel.org
21. **[07-06 18:13]** Re: [PATCH v2 11/18] KVM: arm64: Add a shrinker for pKVM
   - 发件人: sashiko-bot@kernel.org
22. **[07-06 18:14]** Re: [PATCH v2 06/18] KVM: arm64: Add topup interface for the pKVM
 heap allocator
   - 发件人: sashiko-bot@kernel.org
23. **[07-06 18:17]** Re: [PATCH v2 14/18] KVM: arm64: Use noclear for PGD in
 __pkvm_init_vm error path
   - 发件人: sashiko-bot@kernel.org
24. **[07-06 18:19]** Re: [PATCH v2 18/18] KVM: arm64: Alloc simple_buffer_page using
 pKVM hyp allocator
   - 发件人: sashiko-bot@kernel.org
25. **[07-06 18:24]** Re: [PATCH v2 15/18] KVM: arm64: Alloc pkvm_hyp_vm using pKVM heap
 allocator
   - 发件人: sashiko-bot@kernel.org
26. **[07-06 18:24]** Re: [PATCH v2 16/18] KVM: arm64: Alloc pkvm_hyp_vcpu using pKVM
 heap allocator
   - 发件人: sashiko-bot@kernel.org
27. **[07-08 16:54]** Re: [PATCH v2 04/18] KVM: arm64: Add a heap allocator for the pKVM
 hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 6: [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 26 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 06 Jul 2026 19:03:23 +0900

#### 🤖 AI 总结

本邮件线程讨论了 KVM 在 arm64 系统中对多个主机 PMU（性能监控单元）的支持，特别是引入了一个新的特性：KVM_ARM_VCPU_PMU_V3_FIXED_COUNTERS_ONLY 属性。

**原始 patch/问题内容**：
该补丁系列的目标是解决在异构 arm64 系统中，KVM 的 PMU 模拟仅基于单个主机 PMU 实例的限制。当 vCPU 迁移到具有不兼容 PMU 的 pCPU 时，计数器会停止递增，导致 Windows 客户机可能崩溃。当前的解决方法是将 vCPU 固定到共享兼容 PMU 的 pCPU，这在 QEMU/libvirt 中实现起来困难。

**之前讨论要点**：
在历史讨论中，参与者们探讨了如何在不兼容的 PMU 之间进行 vCPU 的迁移，以及如何确保 KVM 能够在异构系统上可靠运行。补丁系列经过多次修改，逐步完善了对 PMU 的支持和错误处理。

**本周的新讨论、进展或结论**：
本周的讨论集中在补丁的具体实现和潜在问题上。Akihiko Odaki 提出了多个补丁，涵盖了禁止在不覆盖所有 CPU 的情况下使用 vPMU、保护 PMU 列表、实现仅固定计数器的模拟等。Oliver Upton 提出了对某些实现的建议和改进意见，特别是关于 CPU 热插拔和 PMU 可用性检查的处理。最终，Odaki 表示将根据讨论结果进行补丁的修订，并计划在未来版本中实现这些改进。整体来看，讨论推动了 KVM 在 arm64 系统中对 PMU 支持的进一步完善。

#### 📝 邮件列表

1. **[07-06 19:03]** [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[07-06 19:03]** [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[07-06 19:03]** [PATCH v8 2/7] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[07-06 19:03]** [PATCH v8 3/7] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[07-06 19:03]** [PATCH v8 4/7] KVM: arm64: PMU: Pass the target CPU to
 kvm_pmu_probe_armpmu()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[07-06 19:03]** [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[07-06 19:03]** [PATCH v8 6/7] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[07-06 19:03]** [PATCH v8 7/7] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[07-06 10:53]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: sashiko-bot@kernel.org
10. **[07-06 11:13]** Re: [PATCH v8 6/7] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: sashiko-bot@kernel.org
11. **[07-06 10:04]** Re: [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[07-06 10:58]** Re: [PATCH v8 6/7] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[07-06 11:23]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[07-06 11:28]** Re: [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Oliver Upton <oupton@kernel.org>
15. **[07-07 08:58]** Re: [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[07-07 01:10]** Re: [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Oliver Upton <oupton@kernel.org>
17. **[07-07 10:41]** Re: [PATCH v8 0/7] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[07-07 20:08]** Re: [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
19. **[07-07 20:23]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
20. **[07-07 20:36]** Re: [PATCH v8 6/7] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
21. **[07-07 21:52]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
22. **[07-07 11:02]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Oliver Upton <oupton@kernel.org>
23. **[07-07 11:20]** Re: [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Oliver Upton <oupton@kernel.org>
24. **[07-08 17:32]** Re: [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
25. **[07-08 18:43]** Re: [PATCH v8 5/7] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
26. **[07-11 15:18]** Re: [PATCH v8 1/7] KVM: arm64: Disallow vPMU when pPMUs do not cover
 all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 7: [PATCH kvmtool v1 0/5] Add guest_memfd support for arm64

**📧 邮件数**: 22 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  6 Jul 2026 09:35:50 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于为 arm64 添加 guest_memfd 支持的补丁系列（PATCH kvmtool v1 0/5）。该补丁旨在为非保护虚拟机提供通过 guest_memfd 作为后备内存的功能，适用于常规 KVM 和 pKVM。

在历史讨论中，Fuad Tabba 提到之前的补丁过于复杂且已过时，因此进行了重新设计。本周的讨论中，Fuad 提交了五个补丁，具体内容包括：
1. 修复了 kvm__for_each_mem_bank() 函数中的未初始化返回值问题。
2. 移除了 die() 函数末尾的多余换行符。
3. 将内存注册函数统一切换为使用 kvm_userspace_memory_region2。
4. 在 kvm__register_mem() 中添加了 guest_memfd 支持。
5. 为 arm64 添加了 --guest-memfd 选项，以支持通过 mmap 创建 guest RAM。

本周的进展中，参与者对补丁进行了讨论，Suzuki K Poulose 提出使用 kvm_userspace_memory_region2 可能会影响旧版 KVM 的兼容性，Fuad 表示可以在需要时保留旧的 ioctl 调用以兼容老版本。Alexandru Elisei 也提出了一些改进建议，Fuad 表示将在下一个版本中进行修正。

总体来看，该补丁系列旨在增强 arm64 的内存管理能力，尤其是在使用 guest_memfd 的场景下，讨论中也关注了向后兼容性和代码简洁性的问题。

#### 📝 邮件列表

1. **[07-06 09:35]** [PATCH kvmtool v1 0/5] Add guest_memfd support for arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-06 09:35]** [PATCH kvmtool v1 1/5] Initialize the return value in kvm__for_each_mem_bank()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-06 09:35]** [PATCH kvmtool v1 2/5] Remove newline from end of die() aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-06 09:35]** [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all memory registration
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-06 09:35]** [PATCH kvmtool v1 4/5] Add guest_memfd support to kvm__register_mem()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-06 09:35]** [PATCH kvmtool v1 5/5] arm64: Add --guest-memfd option to back guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-06 11:23]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[07-06 11:41]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-06 11:46]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Will Deacon <will@kernel.org>
10. **[07-06 11:47]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[07-06 11:53]** Re: [PATCH kvmtool v1 2/5] Remove newline from end of die() aborts
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[07-06 11:57]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
13. **[07-06 11:57]** Re: [PATCH kvmtool v1 2/5] Remove newline from end of die() aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
14. **[07-06 11:59]** Re: [PATCH kvmtool v1 3/5] Use kvm_userspace_memory_region2 for all
 memory registration
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[07-06 12:00]** Re: [PATCH kvmtool v1 4/5] Add guest_memfd support to
 kvm__register_mem()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[07-06 12:13]** Re: [PATCH kvmtool v1 4/5] Add guest_memfd support to
 kvm__register_mem()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[07-06 12:18]** Re: [PATCH kvmtool v1 5/5] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[07-06 12:24]** Re: [PATCH kvmtool v1 5/5] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
19. **[07-06 12:25]** Re: [PATCH kvmtool v1 4/5] Add guest_memfd support to kvm__register_mem()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[07-06 13:34]** Re: [PATCH kvmtool v1 4/5] Add guest_memfd support to
 kvm__register_mem()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[07-08 14:02]** Re: [PATCH kvmtool v1 5/5] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
22. **[07-08 16:59]** Re: [PATCH kvmtool v1 5/5] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 8: [PATCH 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3

**📧 邮件数**: 21 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  2 Jul 2026 17:02:20 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上新增的两个特性支持：FEAT_NV2p1 和 FEAT_NV3。原始的补丁系列（共28个补丁）旨在改进嵌套虚拟化的处理，特别是修复了在 NV 配置下从 EL1 访问某些寄存器时缺失的状态位（FEAT_NV2p1），以及通过引入新的寄存器 NVHCR_EL2 改变 ERET 的行为（FEAT_NV3）。

在历史讨论中，Marc Zyngier 提出了多个补丁，分别处理了 CPTR_EL2 的分类、CPTR_EL2 处理的放宽、HCR_EL2 的非 VNCR 寄存器化、以及 NVHCR_EL2 的上下文切换等问题。这些补丁的目标是确保 KVM 在支持新特性时的兼容性和性能。

在本周的新讨论中，参与者 Joey Gouly 对多个补丁进行了审查并表示认可，指出了一些细微之处。特别是他对 HCR_EL2 的处理提出了警示，但也确认了后续补丁对 NV3 的进一步修改。此外，关于 kvm_has_nv{2,3}() 函数的讨论中，Joey 提出是否需要检查 NV2 的支持，Marc 则回应说这是不必要的，因为 KVM 始终将相关字段暴露为0。

总体来看，本周的讨论主要集中在对补丁的审查和确认上，未出现重大争议，显示出对补丁系列的广泛支持。

#### 📝 邮件列表

1. **[07-02 17:02]** [PATCH 00/28] KVM: arm64: Add support for FEAT_NV2p1 and FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-02 17:02]** [PATCH 06/28] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL register
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-02 17:02]** [PATCH 09/28] KVM: arm64: Relax CPTR_EL2 handling when FEAT_NV2p1 is present
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-02 17:02]** [PATCH 14/28] arm64: sysreg: Add HCRX_EL2 bits related to FEAT_NV3
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-02 17:02]** [PATCH 17/28] KVM: arm64: Add NV3 control bits to HCRX_EL2 sanitisation
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[07-02 17:02]** [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-02 17:02]** [PATCH 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[07-02 17:02]** [PATCH 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[07-02 17:02]** [PATCH 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-02 17:02]** [PATCH 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[07-07 12:33]** Re: [PATCH 06/28] KVM: arm64: Classify CPTR_EL2 as a SR_LOC_SPECIAL
 register
   - 发件人: Joey Gouly <joey.gouly@arm.com>
12. **[07-07 14:55]** Re: [PATCH 09/28] KVM: arm64: Relax CPTR_EL2 handling when
 FEAT_NV2p1 is present
   - 发件人: Joey Gouly <joey.gouly@arm.com>
13. **[07-08 12:18]** Re: [PATCH 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Joey Gouly <joey.gouly@arm.com>
14. **[07-08 15:11]** Re: [PATCH 23/28] KVM: arm64: Add NVHCR_EL2 context switching
   - 发件人: Joey Gouly <joey.gouly@arm.com>
15. **[07-08 16:13]** Re: [PATCH 24/28] KVM: arm64: Engage NV3 ERET trap elision
   - 发件人: Joey Gouly <joey.gouly@arm.com>
16. **[07-09 13:04]** Re: [PATCH 19/28] KVM: arm64: Make HCR_EL2 a non-VNCR register
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[07-10 15:24]** Re: [PATCH 27/28] KVM: arm64: Expose FEAT_NV3 to guests
   - 发件人: Joey Gouly <joey.gouly@arm.com>
18. **[07-10 15:56]** Re: [PATCH 14/28] arm64: sysreg: Add HCRX_EL2 bits related to
 FEAT_NV3
   - 发件人: Joey Gouly <joey.gouly@arm.com>
19. **[07-10 16:17]** Re: [PATCH 17/28] KVM: arm64: Add NV3 control bits to HCRX_EL2
 sanitisation
   - 发件人: Joey Gouly <joey.gouly@arm.com>
20. **[07-10 16:30]** Re: [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Joey Gouly <joey.gouly@arm.com>
21. **[07-10 23:36]** Re: [PATCH 18/28] KVM: arm64: Add kvm_has_nv{2,3}() predicates
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 9: [PATCH v2 00/13] KVM Dirty-bit cleaning hw accelerator (HACDBS)

**📧 邮件数**: 16 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 29 Jun 2026 12:17:48 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 脏位清理硬件加速器（HACDBS）的补丁集，主要由 Leonardo Bras 提出。补丁集的目标是创建一个架构通用的脏位清理加速接口，以提高虚拟机内存脏追踪的效率。

在历史讨论中，Leonardo 提出了多个补丁，特别是针对 arm64 架构的补丁，涉及到启用急切大页拆分（eager hugepage splitting）和实现硬件加速的脏环清理例程。讨论中提到了一些潜在的问题，例如在脏环清理过程中可能出现的用户空间内存访问未验证和缺失的 TLB 失效等问题。

在本周的新讨论中，Leonardo 针对急切拆分和懒拆分的实现细节进行了深入探讨。他强调了在启用 HDBSS 的系统中，如何处理脏位追踪和页面拆分的逻辑。讨论中提到，懒拆分时需要在首次脏写时进行页面拆分，而急切拆分则是在构建 S2 时设置 DBM 位。参与者们对如何在运行时处理页表格式的变化进行了讨论，确保在实现过程中不会引入安全隐患。

总体而言，本周的讨论集中在补丁的细节调整和潜在问题的解决上，参与者们积极交流，以确保补丁的安全性和有效性。

#### 📝 邮件列表

1. **[06-29 12:17]** [PATCH v2 00/13] KVM Dirty-bit cleaning hw accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[06-29 12:17]** [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[06-29 12:18]** [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[06-29 11:36]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: sashiko-bot@kernel.org
5. **[06-29 11:49]** Re: [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated
 dirty-ring cleaning routine
   - 发件人: sashiko-bot@kernel.org
6. **[06-29 15:47]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[06-29 10:06]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[06-29 18:26]** Re: [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[06-30 13:58]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[06-30 08:44]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[06-30 18:09]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[06-30 11:43]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[07-01 11:45]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[07-06 15:00]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
15. **[07-07 14:38]** Re: [PATCH v2 12/13] KVM: arm64: Add hardware-accelerated dirty-ring cleaning routine
   - 发件人: Leonardo Bras <leo.bras@arm.com>
16. **[07-10 16:43]** Re: [PATCH v2 02/13] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 10: [PATCH v8 00/11] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 15 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 10 Jul 2026 20:14:54 +0900

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的性能监控单元（PMU）支持的多个补丁，特别是引入了“固定计数器仅”模式的补丁。

1. **原始补丁内容**：补丁系列的核心是引入 `KVM_ARM_VCPU_PMU_V3_FIXED_COUNTERS_ONLY` 属性，允许在不支持可编程事件计数器的情况下，依然在异构系统上可靠地运行 Windows 客户机。该补丁旨在解决当前 vCPU 迁移到不兼容 PMU 的物理 CPU 时，计数器停止递增的问题。

2. **之前讨论要点**：历史讨论中提到，现有的解决方案需要将 vCPU 固定到共享兼容 PMU 的物理 CPU，这在 QEMU/libvirt 中实现起来非常复杂，并限制了可用的物理 CPU 子集。补丁通过引入新的属性，允许在任何具有兼容硬件 PMU 的物理 CPU 上运行 vCPU，从而简化了调度和资源利用。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的具体实现和测试上，包括对 MDCR_EL2 的访问序列化、更新工具头文件以与内核同步、以及为新的固定计数器模式添加自测。参与者还讨论了实现过程中遇到的潜在问题，如数据竞争和 PMU 配置的有效性检查。邮件中还提到了一些代码审查的反馈，指出了需要注意的高优先级问题。

总体而言，本周的讨论推动了对 KVM arm64 PMU 支持的进一步完善，确保在异构环境中能够稳定运行。

#### 📝 邮件列表

1. **[07-10 20:14]** [PATCH v8 00/11] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[07-10 20:14]** [PATCH v8 01/11] KVM: arm64: Serialize userspace MDCR_EL2 access
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[07-10 20:14]** [PATCH v8 02/11] tools headers: Sync bitfield.h with the kernel
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[07-10 20:14]** [PATCH v8 03/11] KVM: arm64: selftests: Cover PMU state in
 MDCR_EL2
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[07-10 20:14]** [PATCH v8 04/11] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[07-10 20:14]** [PATCH v8 05/11] KVM: arm64: Don't clear vcpu->cpu in
 kvm_arch_vcpu_put()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[07-10 20:15]** [PATCH v8 06/11] KVM: arm64: PMU: Protect the list of PMUs with
 RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[07-10 20:15]** [PATCH v8 07/11] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[07-10 20:15]** [PATCH v8 08/11] KVM: arm64: PMU: Pass the target CPU to
 kvm_pmu_probe_armpmu()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
10. **[07-10 20:15]** [PATCH v8 09/11] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
11. **[07-10 20:15]** [PATCH v8 10/11] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
12. **[07-10 20:15]** [PATCH v8 11/11] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
13. **[07-10 11:36]** Re: [PATCH v8 01/11] KVM: arm64: Serialize userspace MDCR_EL2
 access
   - 发件人: sashiko-bot@kernel.org
14. **[07-10 11:40]** Re: [PATCH v8 04/11] arm64: errata: Require Apple IMPDEF PMUv3
 traps on all CPUs
   - 发件人: sashiko-bot@kernel.org
15. **[07-10 11:48]** Re: [PATCH v8 09/11] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: sashiko-bot@kernel.org

---

### Thread 11: [PATCH v4 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)

**📧 邮件数**: 15 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 10:59:19 +0100

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态管理的补丁系列（PATCH v4 0/8）。该系列补丁旨在优化在 EL2 层面上处理非保护虚拟机的 vCPU 状态管理，减少不必要的状态复制。

### 原始补丁/问题内容
补丁系列的核心是重构 pKVM 在世界切换时的 vCPU 状态管理，避免在每次切换时都复制非保护虚拟机的状态。补丁包括对 vCPU 查找、VGIC（虚拟通用中断控制器）状态的同步和延迟状态复制等功能的实现。

### 之前讨论要点
在历史讨论中，补丁的设计基于 Will 的 pKVM 基础设施系列，强调了在 EL2 层面上引入适当的状态转移原语，以减少对主机状态的引用。补丁还进行了准备性重构，将一些代码移至共享头文件和 HYP（Hypervisor）中。

### 本周的新讨论、进展或结论
本周的讨论集中在补丁的具体实现细节上，包括对 vCPU 状态的延迟同步、VGIC 状态的最小化暴露等。参与者对补丁进行了审查，提出了一些潜在问题，如在处理非保护虚拟机时，系统寄存器的修改可能会被忽略。Fuad Tabba 进一步回应了这些问题，并确认了补丁的设计意图和后续计划。

总的来说，该补丁系列旨在通过优化状态管理，提高 pKVM 的性能和安全性，减少主机与虚拟机之间的状态交互。

#### 📝 邮件列表

1. **[07-06 10:59]** [PATCH v4 0/8] KVM: arm64: pKVM vCPU state management at EL2 (series A)
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-06 10:59]** [PATCH v4 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-06 10:59]** [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-06 10:59]** [PATCH v4 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-06 10:59]** [PATCH v4 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-06 10:59]** [PATCH v4 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[07-06 10:59]** [PATCH v4 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[07-06 10:59]** [PATCH v4 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-06 10:59]** [PATCH v4 8/8] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[07-06 10:25]** Re: [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: sashiko-bot@kernel.org
11. **[07-06 10:28]** Re: [PATCH v4 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
12. **[07-06 10:36]** Re: [PATCH v4 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
13. **[07-06 12:48]** Re: [PATCH v4 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
14. **[07-06 12:53]** Re: [PATCH v4 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[07-06 12:59]** Re: [PATCH v4 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 12: [PATCH v3 0/3] Optimize S2 page splitting

**📧 邮件数**: 14 | **👥 参与者**: 5 | **📅 开始时间**: Wed,  8 Jul 2026 14:40:56 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于优化 S2 页分割的补丁（PATCH v3 0/3）。该补丁的主要目的是通过引入新的遍历标志来跳过不必要的页表级别，从而提高性能。具体来说，如果一个三级条目被遍历，意味着其父级二级条目已经被分割，因此可以跳过对其子节点的遍历。

在历史讨论中，补丁的背景主要集中在如何优化页分割的性能，特别是在处理脏位追踪时的效率。之前的讨论指出，遍历所有条目是多余的，补丁提出的优化措施可以显著减少运行时间，尤其是在内存已经分割的情况下。

本周的新讨论中，参与者对补丁进行了详细的技术审查，提出了一些潜在问题和改进建议。例如，有人指出在页表遍历的起始根级别也应考虑跳过的情况。此外，补丁的代码逻辑和注释的清晰度也受到关注，参与者建议在下一版本中改进说明，以便更好地理解补丁的目的和实现方式。

总体而言，本周的讨论推动了补丁的进一步完善，参与者们积极反馈，期待在后续版本中看到更清晰的实现和文档。

#### 📝 邮件列表

1. **[07-08 14:40]** [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[07-08 14:40]** [PATCH v3 1/3] KVM: arm64: Avoid re-testing walk_continue
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[07-08 14:40]** [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[07-08 14:40]** [PATCH v3 3/3] KVM: arm64: Make stage2_split_walker() skip unnecessary walks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[07-08 13:50]** Re: [PATCH v3 2/3] KVM: arm64: Introduce
 KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: sashiko-bot@kernel.org
6. **[07-08 16:25]** Re: [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[07-08 16:49]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
8. **[07-08 17:16]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[07-08 17:41]** Re: [PATCH v3 1/3] KVM: arm64: Avoid re-testing walk_continue
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[07-08 18:00]** Re: [PATCH v3 1/3] KVM: arm64: Avoid re-testing walk_continue
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[07-08 18:17]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[07-09 15:25]** Re: [PATCH v3 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[07-11 06:53]** Re: [PATCH v3 2/3] KVM: arm64: Introduce
 KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
14. **[07-12 20:20]** Re: [PATCH v3 0/3] Optimize S2 page splitting
   - 发件人: Dev Jain <dev.jain@arm.com>

---

### Thread 13: [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception Masking

**📧 邮件数**: 14 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 3 Jul 2026 18:01:18 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM64 架构的补丁系列，主要是实现对 ARMv8.8-A/v9.3-A 硬件 NMI 扩展（FEAT_NMI）的支持，并重新设计异常屏蔽机制。补丁的核心内容包括使用 PSTATE.ALLINT 来管理超级优先级中断，并对现有的 DAIF 宏进行重构，以提高代码的可读性和维护性。

在历史讨论中，参与者们关注了补丁的实现细节，提出了关于函数内联标记和数据结构设计的建议。例如，Leonardo Bras 提出了将某些函数标记为 `__always_inline` 的必要性，并讨论了使用位域来压缩异常状态的存储。

在本周的新讨论中，Jinjie Ruan 表达了对 NMI 支持的兴奋，并表示希望与其他开发者（如 Vladimir）合作，推动相关功能的主线合并。针对 DAIF 宏的存放位置，Breno Leitao 提到可能会导致循环依赖问题。Jinjie 还回应了关于位域设计的建议，解释了字段宽度的选择是为了在软件层面上有效打包异常状态，而不是直接映射硬件寄存器布局。

总的来说，讨论围绕补丁的实现细节、代码重构的必要性以及开发者之间的协作展开，显示出对提升 ARM64 架构异常处理能力的共同关注。

#### 📝 邮件列表

1. **[07-03 18:01]** [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception Masking
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
2. **[07-03 18:01]** [PATCH 01/17] arm64: Move DAIF macros to ptrace.h and use them centrally
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
3. **[07-03 18:01]** [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
4. **[07-03 14:38]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[07-03 14:48]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[07-03 15:15]** Re: [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception
 Masking
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[07-03 09:44]** Re: [PATCH 01/17] arm64: Move DAIF macros to ptrace.h and use them
 centrally
   - 发件人: Breno Leitao <leitao@debian.org>
8. **[07-06 09:10]** Re: [PATCH 00/17] arm64: Support FEAT_NMI and Rework Exception
 Masking
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
9. **[07-06 20:57]** Re: [PATCH 01/17] arm64: Move DAIF macros to ptrace.h and use them
 centrally
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
10. **[07-06 21:00]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract
 logical mask
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
11. **[07-06 14:02]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[07-06 21:15]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract
 logical mask
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>
13. **[07-06 14:43]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract logical mask
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[07-07 16:39]** Re: [PATCH 02/17] arm64: Rework exception masking into abstract
 logical mask
   - 发件人: Jinjie Ruan <ruanjinjie@huawei.com>

---

### Thread 14: [PATCH v5 00/10] coco: guest: Enforce host page-size alignment for shared buffers

**📧 邮件数**: 14 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  6 Jul 2026 11:34:22 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个名为“[PATCH v5 00/10] coco: guest: Enforce host page-size alignment for shared buffers”的补丁系列，旨在加强在机密计算环境中，客体与主机之间共享缓冲区的页面大小对齐要求。

**补丁内容**：该补丁系列提出了两个主要约束：共享缓冲区的地址必须对齐到CoCo共享粒度大小，且大小必须是该粒度大小的倍数。补丁中引入了通用辅助函数以支持这些要求，并更新了多个内存分配路径以确保对齐。

**历史讨论**：在之前的讨论中，参与者提到在机密计算环境中，主机和客体可能使用不同的页面大小进行内存管理，因此需要确保共享缓冲区的对齐，以避免潜在的内存访问错误和内核崩溃。

**本周新讨论**：本周的讨论集中在补丁的具体实现上，包括对共享ITS分配、DMA映射、SWIOTLB池等的对齐处理。参与者Marc Zyngier对补丁中的变量命名提出了建议，强调清晰性和代码可维护性。Aneesh Kumar K.V则回应了这些建议，并表示愿意根据反馈进行调整。

总的来说，本周的讨论进一步推动了补丁的完善，确保在机密计算环境中共享缓冲区的安全性和稳定性。

#### 📝 邮件列表

1. **[07-06 11:34]** [PATCH v5 00/10] coco: guest: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[07-06 11:34]** [PATCH v5 01/10] mm/mem_encrypt: Add helpers for shared-buffer alignment
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[07-06 11:34]** [PATCH v5 02/10] irqchip/gic-v3-its: Align shared ITS allocations to the CoCo shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[07-06 11:34]** [PATCH v5 03/10] dma-mapping: Pass allocation attrs to contiguous allocation helpers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[07-06 11:34]** [PATCH v5 04/10] dma-direct: Align CoCo shared DMA allocations to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[07-06 11:34]** [PATCH v5 05/10] swiotlb: Align shared IO TLB pools to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[07-06 11:34]** [PATCH v5 06/10] swiotlb: Reject misaligned restricted DMA pools for CoCo guests
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[07-06 11:34]** [PATCH v5 07/10] dma-buf: system_heap: Enforce shared-granule alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[07-06 11:34]** [PATCH v5 08/10] arm64: realm: Move Realm memory encryption ops to RSI code
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[07-06 11:34]** [PATCH v5 09/10] arm64: realm: Add RHI helper to query IPA state change alignment
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[07-06 11:34]** [PATCH v5 10/10] arm64: realm: Expose the CCA shared granule size through mem_encrypt ops
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[07-06 14:35]** Re: [PATCH v5 02/10] irqchip/gic-v3-its: Align shared ITS allocations to the CoCo shared granule size
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[07-06 19:12]** Re: [PATCH v5 02/10] irqchip/gic-v3-its: Align shared ITS
 allocations to the CoCo shared granule size
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
14. **[07-06 15:44]** Re: [PATCH v5 02/10] irqchip/gic-v3-its: Align shared ITS allocations to the CoCo shared granule size
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 15: [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5

**📧 邮件数**: 13 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 9 Jul 2026 18:40:20 +0800

#### 🤖 AI 总结

本邮件线程讨论了对 ARMv9.5 引入的硬件脏页状态跟踪结构（HDBSS）特性的支持，包含六个补丁的系列更新。

1. **原始补丁内容**：该系列补丁旨在增强对 HDBSS 特性的支持，HDBSS 通过硬件辅助跟踪内存页的脏状态，显著降低了脏页扫描的开销，从而降低了实时迁移的执行开销。

2. **之前讨论要点**：在之前的讨论中，补丁的 v3 版本引入了懒惰的脏页访问处理，而 v4 版本则在 MMU 初始化时直接注入脏位修改器（DBM），避免了首次脏访问时的页面故障。此外，补丁还确保在迁移设置期间自动启用 HDBSS，以防止大页在迁移后不被正确拆分。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的具体实现上，包括：
   - 增加了 HDBSS 的每个虚拟 CPU 的缓冲管理。
   - 实现了 HDBSS 的故障处理和缓冲区刷新机制。
   - 自动启用/禁用 HDBSS 功能，基于内存槽的脏日志状态。
   - 参与者讨论了补丁中的潜在问题和改进建议，包括内存泄漏、锁定机制的缺失和错误处理等。

总的来说，这一系列补丁的目标是通过引入 HDBSS 特性，提升 ARM64 架构下 KVM 的脏页跟踪效率，并在讨论中持续关注实现中的问题和优化建议。

#### 📝 邮件列表

1. **[07-09 18:40]** [PATCH v4 0/6] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
2. **[07-09 18:40]** [PATCH v4 1/6] KVM: arm64: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[07-09 18:40]** [PATCH v4 2/6] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
4. **[07-09 18:40]** [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware dirty tracking
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
5. **[07-09 18:40]** [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
6. **[07-09 18:40]** [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer flush
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
7. **[07-09 18:40]** [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on dirty logging change
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
8. **[07-09 11:00]** Re: [PATCH v4 2/6] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: sashiko-bot@kernel.org
9. **[07-09 11:03]** Re: [PATCH v4 1/6] KVM: arm64: Enable eager hugepage splitting if
 HDBSS is available
   - 发件人: sashiko-bot@kernel.org
10. **[07-09 11:14]** Re: [PATCH v4 3/6] KVM: arm64: Add auto DBM support for hardware
 dirty tracking
   - 发件人: sashiko-bot@kernel.org
11. **[07-09 11:15]** Re: [PATCH v4 4/6] KVM: arm64: Add HDBSS per-vCPU buffer management
   - 发件人: sashiko-bot@kernel.org
12. **[07-09 11:26]** Re: [PATCH v4 5/6] KVM: arm64: Add HDBSS fault handling and buffer
 flush
   - 发件人: sashiko-bot@kernel.org
13. **[07-09 11:34]** Re: [PATCH v4 6/6] KVM: arm64: Add auto HDBSS enable/disable on
 dirty logging change
   - 发件人: sashiko-bot@kernel.org

---

### Thread 16: [PATCH 6.6 v2 0/6] arm64: KVM: Backport VHE-only boot fixes

**📧 邮件数**: 13 | **👥 参与者**: 3 | **📅 开始时间**: Wed,  8 Jul 2026 22:51:18 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构 KVM 的一系列补丁，主要集中在 VHE（虚拟化硬件扩展）启动修复上。原始补丁的目的是解决在 KVM 嵌套虚拟化环境中，6.6.y 内核启动时可能出现的挂起问题，特别是在某些 CPU 上，HCR_EL2.E2H 状态未被正确初始化。

在历史讨论中，补丁系列的背景是由于 ARMv9.5 引入了 ID_AA64MMFR4_EL1，导致 FEAT_E2H0 变为可选，进而影响了启动过程。之前的讨论主要集中在如何确保 HCR_EL2.E2H 的状态在启动时被正确初始化，以避免在嵌套虚拟化环境中出现问题。

本周的新讨论中，参与者对补丁进行了逐一审查和修改，提出了多个具体改进建议，包括：
1. 修复了对 FEAT_E2H0 未实现的早期处理。
2. 确保在 KVM PSCI 入口点中早期初始化 HCR_EL2.E2H。
3. 重新设计 HCR_EL2.E2H 的 RES1 检测逻辑，以适应不同类型的 CPU。

此外，Sashiko AI 评审工具也指出了一些潜在问题，如缺乏必要的上下文同步事件（ISB）和对系统寄存器的写入后缺少同步等。最后，Marc Zyngier 提醒参与者注意补丁提交的格式要求，确保每个补丁都有适当的签名。

#### 📝 邮件列表

1. **[07-08 22:51]** [PATCH 6.6 v2 0/6] arm64: KVM: Backport VHE-only boot fixes
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-08 22:51]** [PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[07-08 22:51]** [PATCH 6.6 v2 2/6] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[07-08 22:51]** [PATCH 6.6 v2 3/6] arm64: Fix early handling of FEAT_E2H0 not being implemented
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[07-08 22:51]** [PATCH 6.6 v2 4/6] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[07-08 22:51]** [PATCH 6.6 v2 5/6] KVM: arm64: Initialize SCTLR_EL1 in __kvm_hyp_init_cpu()
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[07-08 22:51]** [PATCH 6.6 v2 6/6] arm64: Revamp HCR_EL2.E2H RES1 detection
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[07-08 22:59]** Re: [PATCH 6.6 v2 2/6] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: sashiko-bot@kernel.org
9. **[07-08 22:59]** Re: [PATCH 6.6 v2 6/6] arm64: Revamp HCR_EL2.E2H RES1 detection
   - 发件人: sashiko-bot@kernel.org
10. **[07-08 23:01]** Re: [PATCH 6.6 v2 3/6] arm64: Fix early handling of FEAT_E2H0 not
 being implemented
   - 发件人: sashiko-bot@kernel.org
11. **[07-08 23:03]** Re: [PATCH 6.6 v2 4/6] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: sashiko-bot@kernel.org
12. **[07-08 23:03]** Re: [PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for
 ID_AA64MMFR4_EL1
   - 发件人: sashiko-bot@kernel.org
13. **[07-09 11:16]** Re: [PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 17: [PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Thu,  9 Jul 2026 22:35:57 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构 KVM 的一系列补丁，主要集中在 VHE（Virtualization Host Extensions）模式下的引导修复。原始补丁提出了在 6.6.y 版本中回溯 VHE 仅引导修复，以解决在 KVM 嵌套虚拟化下引导时可能出现的挂起问题。补丁系列的目标是确保在某些 CPU 上，HCR_EL2.E2H 能够可靠地初始化，以避免引导失败。

历史讨论中，补丁的背景是由于架构更新使得 FEAT_E2H0 成为可选项，导致某些硬件在未初始化的情况下可能会进入未知状态。之前的讨论主要集中在如何处理 HCR_EL2.E2H 的初始化以及相关的系统寄存器配置。

本周的新讨论中，补丁的多个版本被提交并进行了细致的修改，包括增加了对冲突的解决说明、修复了早期处理 FEAT_E2H0 的错误、以及确保在 KVM PSCI 入口点中早期初始化 HCR_EL2.E2H。参与者们对补丁进行了审查，并确认了其有效性，最终将该系列补丁排入 6.6 版本中。整体来看，本周的进展标志着对 VHE 模式引导问题的有效解决，增强了 KVM 的稳定性和可靠性。

#### 📝 邮件列表

1. **[07-09 22:35]** [PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-09 22:35]** [PATCH 6.6 v3 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[07-09 22:35]** [PATCH 6.6 v3 2/6] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[07-09 22:36]** [PATCH 6.6 v3 3/6] arm64: Fix early handling of FEAT_E2H0 not being implemented
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[07-09 22:36]** [PATCH 6.6 v3 4/6] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[07-09 22:36]** [PATCH 6.6 v3 5/6] KVM: arm64: Initialize SCTLR_EL1 in __kvm_hyp_init_cpu()
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[07-09 22:36]** [PATCH 6.6 v3 6/6] arm64: Revamp HCR_EL2.E2H RES1 detection
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[07-09 22:45]** Re: [PATCH 6.6 v3 2/6] arm64: Treat HCR_EL2.E2H as RES1 when
 ID_AA64MMFR4_EL1.E2H0 is negative
   - 发件人: sashiko-bot@kernel.org
9. **[07-09 22:46]** Re: [PATCH 6.6 v3 3/6] arm64: Fix early handling of FEAT_E2H0 not
 being implemented
   - 发件人: sashiko-bot@kernel.org
10. **[07-09 22:46]** Re: [PATCH 6.6 v3 4/6] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: sashiko-bot@kernel.org
11. **[07-10 17:03]** Re: [PATCH 6.6 v3 0/6] arm64: KVM: Backport VHE-only boot fixes
   - 发件人: Sasha Levin <sashal@kernel.org>

---

### Thread 18: [PATCH kvmtool v2 0/4] Add guest_memfd support for arm64

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  8 Jul 2026 19:25:06 +0100

#### 🤖 AI 总结

本邮件线程讨论了对 arm64 平台的 KVM 工具添加对 guest_memfd 的支持，主要由 Fuad Tabba 提出并进行补充。

1. **原始 patch/问题的内容**：该补丁系列（共四个补丁）旨在为 arm64 的非保护虚拟机提供使用 guest_memfd 作为来宾内存的支持。补丁包括修复代码中的问题、添加 guest_memfd 相关的内存注册功能，以及实现一个新的命令行选项 `--guest-memfd`，用于创建基于 guest_memfd 的来宾内存。

2. **之前讨论要点**：在历史讨论中，Fuad 提到之前的实现过于复杂且过时，因此进行了重新设计。补丁的前两个部分修复了代码中的一些小错误，而后两个部分则实现了 guest_memfd 的核心功能。

3. **本周的新讨论、进展或结论**：本周的讨论集中在补丁的具体实现细节上。Alexandru Elisei 提出了对错误处理的建议，建议在调用 `kvm__register_ram_guest_memfd()` 前检查返回值，以避免潜在的错误。此外，他还指出，启用 MTE 时与 guest_memfd 可能存在不兼容问题，Fuad 同意在使用 `--guest-memfd` 时禁用 MTE，并在用户界面中提供相关提示。Fuad 表示将在下一个版本中进行这些调整。

整体来看，该系列补丁的讨论体现了对代码质量和用户体验的关注，参与者积极提出建议以优化实现。

#### 📝 邮件列表

1. **[07-08 19:25]** [PATCH kvmtool v2 0/4] Add guest_memfd support for arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-08 19:25]** [PATCH kvmtool v2 1/4] Initialize the return value in kvm__for_each_mem_bank()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-08 19:25]** [PATCH kvmtool v2 2/4] Remove newline from end of die() aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-08 19:25]** [PATCH kvmtool v2 3/4] Add support for registering guest_memfd-backed memory regions
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-08 19:25]** [PATCH kvmtool v2 4/4] arm64: Add --guest-memfd option to back guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-09 16:07]** Re: [PATCH kvmtool v2 3/4] Add support for registering
 guest_memfd-backed memory regions
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
7. **[07-09 16:08]** Re: [PATCH kvmtool v2 4/4] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
8. **[07-09 16:32]** Re: [PATCH kvmtool v2 3/4] Add support for registering
 guest_memfd-backed memory regions
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[07-09 16:33]** Re: [PATCH kvmtool v2 4/4] arm64: Add --guest-memfd option to back
 guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 19: [PATCH v6 01/25] KVM: arm64: Generalize trace clock

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 10 Jul 2026 15:19:51 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的时间跟踪功能的泛化。最初的补丁（PATCH v6 01/25）旨在对现有的 trace_clock 接口进行改进，以支持更安全的时间跟踪机制。

在历史讨论中，参与者 Mostafa Saleh 提出了对现有 trace_clock 的担忧，认为在多线程环境下使用可能存在风险。他建议将 trace_clock 和新的 hyp_clock 分开，hyp_clock 不需要与主机同步，从而降低风险。

本周的新讨论中，Vincent Donnefort 对补丁进行了深入分析，提出了将 trace_clock 接口保持不变，并在同一文件中引入 hyp_clock 的想法。他强调了在不同情况下（如跟踪开启或关闭时）应有不同的时钟行为。此外，Mostafa 表示将遵循 Vincent 的建议，保持现有的跟踪代码不变，并引入两个新函数来读取系统定时器和初始化虚拟机监控器。

总体来看，本周的讨论集中在如何平衡安全性与功能性，确保时间跟踪的准确性与可靠性，同时也在探索更好的实现方式。

#### 📝 邮件列表

1. **[07-10 15:19]** Re: [PATCH v6 01/25] KVM: arm64: Generalize trace clock
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-10 15:24]** Re: [PATCH v6 01/25] KVM: arm64: Generalize trace clock
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-10 17:01]** Re: [PATCH v6 16/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-10 17:17]** Re: [PATCH v6 07/25] KVM: arm64: iommu: Introduce IOMMU driver
 infrastructure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-10 17:33]** Re: [PATCH v6 09/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-10 18:08]** Re: [PATCH v6 02/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[07-12 13:44]** Re: [PATCH v6 01/25] KVM: arm64: Generalize trace clock
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[07-12 15:29]** Re: [PATCH v6 02/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 20: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 30 Jun 2026 13:09:59 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM arm64 的 shadow ptdump 修复的补丁（PATCH v2 0/6）。该补丁旨在解决 shadow ptdump debugfs 文件的问题，创建一个名为 "shadow_page_tables" 的单一文件，以便于转储所有有效的 MMU 页表信息。历史讨论中，参与者 Wei-Lin Chang 和 Itaru Kitayama 就补丁的实现细节进行了深入交流，特别是关于 shadow stage 2 转换表的构建和输出信息的准确性。

在本周的新讨论中，Itaru Kitayama 对补丁的实现进行了确认，指出 shadow stage-2 转换表确实是以 52 位 IPA 构建的，这与 L1 设置的 init_s2_mmu() 中的值无关。Wei-Lin Chang 也表示，虽然可以根据需求添加 shadow_ipa_range 和 shadow_stage2_levels 文件，但目前从 PARange 中推断这些信息并不困难。最终，Itaru Kitayama 提出了对补丁的测试确认，表示在最新的 kvmarm/fixes 内核中，补丁能够正确提取映射信息。

总结而言，本周的讨论主要集中在补丁的确认和潜在的扩展上，参与者们对补丁的功能和实现细节达成了一致。

#### 📝 邮件列表

1. **[06-30 13:09]** [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[07-02 15:55]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
3. **[07-02 08:41]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[07-03 08:02]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
5. **[07-03 11:24]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[07-09 16:34]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
7. **[07-10 07:43]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[07-10 16:26]** Re: [PATCH v2 0/6] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>

---

### Thread 21: [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 2 Jul 2026 19:04:18 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构上暴露 PMMIR_EL1.SLOTS 的补丁系列（PATCH v2 0/3）。该补丁旨在解决在运行 perf 工具时，因无法读取 PMMIR_EL1.SLOTS 导致的错误。补丁引入了一个新的 vCPU 特性标志 KVM_ARM_VCPU_PMU_V3_STRICT，以确保向来宾正确暴露该寄存器。

在历史讨论中，补丁的背景被详细阐述，指出当前的 KVM 实现会将 PMMIR_EL1.SLOTS 视为只读（RAZ/WI），导致 perf 工具无法正常工作。补丁的第一部分增加了新的特性标志，而后续的补丁则针对该特性进行了行为调整。

在本周的新讨论中，参与者对补丁进行了进一步的审查和修改建议。Oliver Upton 提出了多个改进意见，包括确保与用户空间的兼容性、补丁顺序的调整等。Congkai Tan 对这些建议进行了采纳，并表示已将修改整合到 v3 版本中，并进行了测试，结果符合预期。最终，Congkai 计划尽快发送 v3 补丁以供进一步审查。整体来看，本周的讨论集中在补丁的细节完善和测试反馈上。

#### 📝 邮件列表

1. **[07-02 19:04]** [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>
2. **[07-06 11:31]** [PATCH v2 0/3] KVM: arm64: Tidy up is_created
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-06 11:31]** [PATCH v2 1/3] KVM: arm64: Drop the unused EL2-side is_created write
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-06 11:31]** [PATCH v2 2/3] KVM: arm64: Remove unreachable early checks in pkvm_init_host_vm()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-06 11:31]** [PATCH v2 3/3] KVM: arm64: Drop redundant READ_ONCE() in pkvm_hyp_vm_is_created()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-07 15:28]** Re: [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[07-10 06:44]** Re: [PATCH v2 0/3] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>

---

### Thread 22: [PATCH v2 0/2] KVM: arm64: KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 10 Jul 2026 12:48:17 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的两个补丁，旨在修复潜在的内存泄漏问题和描述符分配大小错误。

**原始 patch/问题内容**：
补丁系列的主要目标是修复在 `hyp_trace_buffer_alloc_bpages_backing` 函数中可能出现的内存泄漏问题，以及在 `hyp_trace_load` 函数中对 `hyp_trace_desc` 的分配大小计算错误。

**之前讨论要点**：
在补丁的 v1 版本中，Vincent Donnefort 提出了这两个问题，并在后续版本中根据 Fuad Tabba 的反馈进行了修改，增加了对内存泄漏的处理，并修正了描述符的分配逻辑。

**本周的新讨论、进展或结论**：
本周的讨论中，Vincent 提交了补丁的 v2 版本，修复了内存泄漏问题，确保在 `__map_hyp` 失败时能够释放已分配的页面。同时，修正了描述符的大小计算，并增加了溢出检查。Fuad Tabba 对这两个补丁进行了测试，确认在 v7.2-rc2 版本上编译成功，并在保护和非保护的虚拟机上均能正常运行，最终获得了他的认可和测试通过的反馈。Sashiko AI 也对补丁进行了审查，提出了潜在的边界计算问题，但 Vincent 表示该问题已在补丁中得到解决。

#### 📝 邮件列表

1. **[07-10 12:48]** [PATCH v2 0/2] KVM: arm64: KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-10 12:48]** [PATCH v2 1/2] KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-10 12:48]** [PATCH v2 2/2] KVM: arm64: Fix hyp_trace_desc allocation size in hyp_trace_load()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-10 12:02]** Re: [PATCH v2 2/2] KVM: arm64: Fix hyp_trace_desc allocation size
 in hyp_trace_load()
   - 发件人: sashiko-bot@kernel.org
5. **[07-10 14:19]** Re: [PATCH v2 2/2] KVM: arm64: Fix hyp_trace_desc allocation size in
 hyp_trace_load()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[07-12 16:56]** Re: [PATCH v2 2/2] KVM: arm64: Fix hyp_trace_desc allocation size in hyp_trace_load()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 23: [PATCH v5 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Thu,  9 Jul 2026 16:42:23 +0200

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 arm64 虚拟化中 VGIC 的两个补丁，旨在修复与 LPI（本地中断线）释放和重新注册处理相关的竞争条件问题。

**原始补丁内容**：
补丁 v5 包含两个主要修复：第一个补丁修复了 LPI 释放和重新注册之间的竞争条件，可能导致 LPI 结构泄漏或被提前删除；第二个补丁则缓解了在注册新 LPI 时可能出现的 -ENOMEM 错误。

**之前讨论要点**：
在历史讨论中，补丁经过多次版本迭代，逐步解决了代码审查中提出的问题，包括在释放 LPI 时的引用计数处理和锁的使用。开发者们讨论了如何确保在并发情况下，LPI 的释放和注册不会相互干扰。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现上。Carlos López 提出了对补丁的进一步修改，确保在注册新 LPI 时，使用 `GFP_NOWAIT` 进行内存分配，以避免在竞争条件下导致的内存分配失败。此外，Sashiko AI 进行了审查，指出了潜在的内存泄漏和死锁风险，开发者们对此进行了回应，确认在最新的补丁中已解决相关问题。整体来看，补丁的讨论和修改进展顺利，目标是提高 KVM 的稳定性和性能。

#### 📝 邮件列表

1. **[07-09 16:42]** [PATCH v5 0/2] KVM: arm64: vgic: Fix racy LPI release and re-registration handling
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
2. **[07-09 16:42]** [PATCH v5 1/2] KVM: arm64: vgic: Fix race between LPI release and re-registration
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
3. **[07-09 16:42]** [PATCH v5 2/2] KVM: arm64: vgic: Mitigate potential LPI registration failure
   - 发件人: =?UTF-8?q?Carlos=20L=C3=B3pez?= <clopez@suse.de>
4. **[07-09 14:59]** Re: [PATCH v5 1/2] KVM: arm64: vgic: Fix race between LPI release
 and re-registration
   - 发件人: sashiko-bot@kernel.org
5. **[07-09 15:09]** Re: [PATCH v5 2/2] KVM: arm64: vgic: Mitigate potential LPI
 registration failure
   - 发件人: sashiko-bot@kernel.org
6. **[07-09 17:52]** Re: [PATCH v5 2/2] KVM: arm64: vgic: Mitigate potential LPI
 registration failure
   - 发件人: =?UTF-8?Q?Carlos_L=C3=B3pez?= <clopez@suse.de>

---

### Thread 24: [PATCH v3 0/2] KVM: arm64: Fix and test MMIO sign-extending loads

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  6 Jul 2026 12:55:20 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下修复和测试 MMIO（内存映射 I/O）符号扩展加载的问题。

1. **原始 patch/问题的内容**：该补丁主要解决从模拟 MMIO 读取时，符号扩展加载（如 LDRSB、LDRSH 和 LDRSW）返回零扩展值而非所需的符号扩展值的问题。此问题源于 2014 年的代码掩码，导致在处理设备内存时未正确扩展符号。

2. **之前的讨论要点**：在之前的讨论中，参与者确认了补丁的必要性，并指出了代码中的错误。补丁 1 修复了符号扩展问题，而补丁 2 则增加了自测试以确保不会出现回归。

3. **本周的新讨论、进展或结论**：本周的讨论中，Fuad Tabba 提交了补丁 v3 的更新，移除了不必要的代码，并得到了 Oliver Upton 的审核确认。补丁已被 Marc Zyngier 应用到修复列表中，确保了 MMIO 加载的符号扩展问题得到解决。此外，针对自测试的反馈，Fuad 解释了 PTE_USER 的使用并确认其正确性。整体来看，讨论进展顺利，补丁已成功整合。

#### 📝 邮件列表

1. **[07-06 12:55]** [PATCH v3 0/2] KVM: arm64: Fix and test MMIO sign-extending loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-06 12:55]** [PATCH v3 1/2] KVM: arm64: Fix sign-extension of MMIO loads
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-06 12:55]** [PATCH v3 2/2] KVM: arm64: selftests: Add MMIO sign-extending load test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-06 12:08]** Re: [PATCH v3 2/2] KVM: arm64: selftests: Add MMIO sign-extending
 load test
   - 发件人: sashiko-bot@kernel.org
5. **[07-06 13:19]** Re: [PATCH v3 2/2] KVM: arm64: selftests: Add MMIO sign-extending
 load test
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[07-06 17:19]** Re: [PATCH v3 0/2] KVM: arm64: Fix and test MMIO sign-extending loads
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 25: [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 12 Jul 2026 15:25:32 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 arm64 架构的 KVM 工具添加对 `guest_memfd` 的支持，包含四个补丁。补丁的主要目的是使 KVM 能够使用 `guest_memfd` 来支持虚拟机的内存管理。

在历史讨论中，Fuad Tabba 提到之前的实现过于复杂，因此进行了重新设计。补丁系列的第一部分修复了代码中的一些问题，包括未初始化的返回值和多余的换行符。接下来的补丁则实现了将 `guest_memfd` 作为内存区域的后端，允许通过 `KVM_SET_USER_MEMORY_REGION2` 注册这些内存区域。

本周的新讨论中，Fuad 提供了补丁的具体修改内容，包括：
1. 在 `kvm__register_ram_guest_memfd()` 中添加了对 `guest_memfd` 的支持，并确保在拆卸时关闭文件描述符。
2. 添加了新的命令行选项 `--guest-memfd`，用于创建基于 `guest_memfd` 的虚拟机内存。
3. 讨论了在使用 `--guest-memfd` 时禁用 MTE（内存拓扑扩展），并指出受保护的虚拟机尚不支持该选项。

总的来说，这一系列补丁旨在简化和增强 KVM 对 `guest_memfd` 的支持，以便在 arm64 架构上更有效地管理虚拟机的内存。

#### 📝 邮件列表

1. **[07-12 15:25]** [PATCH kvmtool v3 0/4] Add guest_memfd support for arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[07-12 15:25]** [PATCH kvmtool v3 1/4] Initialize the return value in kvm__for_each_mem_bank()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-12 15:25]** [PATCH kvmtool v3 2/4] Remove newline from end of die() aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-12 15:25]** [PATCH kvmtool v3 3/4] Add support for registering guest_memfd-backed memory regions
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[07-12 15:25]** [PATCH kvmtool v3 4/4] arm64: Add --guest-memfd option to back guest RAM with guest_memfd
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 26: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 10 Jul 2026 15:21:28 -0700

#### 🤖 AI 总结

本邮件讨论的主题是针对 AmpereOne 处理器的 erratum AC03_CPU_57 和 AC04_CPU_29 的补丁。该补丁旨在解决在 AmpereOne 中，若通过 ICC_DIR_EL1 或 ICC_EOIRx_EL1 关闭一个非活动的、最高优先级的挂起中断，会导致 CPU 丢失中断挂起状态，并阻止未来中断的传递。补丁的工作原理是在虚拟化通用中断控制器（vgic）中避免此问题。

在之前的讨论中，参与者们追踪到一个与嵌套虚拟化相关的挂起问题，确认是由于 AmpereOne 的 CPU erratum 引起的。D Scott Phillips 提到他对补丁进行了测试，未再出现挂起现象，但对 vgic 的逻辑并不十分熟悉，希望能获得更多建议。

本周的新讨论中，Sashiko-bot 提出了对补丁的潜在问题，包括可能导致物理中断状态泄漏的风险，以及对非嵌套（L1）客户机的拒绝服务攻击向量的担忧。Marc Zyngier 对此表示，补丁确实是一个小的错误修复，并讨论了与嵌套 vgic 相关的状态处理问题。他还建议在补丁中增加更多的注释和修复信息，以便于后续的维护和回溯。整体来看，讨论集中在补丁的有效性和潜在风险上，参与者们对 erratum 的理解和处理方式进行了深入探讨。

#### 📝 邮件列表

1. **[07-10 15:21]** [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: D Scott Phillips <scott@os.amperecomputing.com>
2. **[07-10 22:37]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57
 and AC04_CPU_29
   - 发件人: sashiko-bot@kernel.org
3. **[07-11 08:37]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-11 08:53]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-11 23:27]** Re: [PATCH] arm64: errata: Mitigate AmpereOne erratum AC03_CPU_57 and AC04_CPU_29
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH] KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Tue,  7 Jul 2026 17:50:29 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在修复 `hyp_trace_buffer_alloc_bpages_backing` 函数中可能导致的内存泄漏问题。具体来说，当 `__map_hyp` 函数调用失败时，已分配的后备页面未被释放，导致内存泄漏。补丁通过在错误发生时释放这些页面来解决此问题。

在历史讨论中，补丁的背景是由 Sashiko 提出的，指出 `trace_remote_alloc_buffer` 在分配每 CPU 环形缓冲区时存在类似的内存泄漏问题。Vincent Donnefort 提交了这个补丁，并在邮件中详细描述了修复的内容和逻辑。

本周的新讨论中，参与者对补丁进行了积极的反馈。Fuad Tabba 表示补丁经过审查并已测试通过，同时提出了代码清晰度的建议，建议将描述赋值的操作移到错误检查之后。此外，Vincent 也确认了 Fuad 提到的另一个潜在问题，并表示将其提交到跟踪邮件列表中进行进一步讨论。

总体来看，本周的讨论集中在补丁的审查和潜在问题的识别上，参与者们对补丁的有效性表示认可，并提出了改进建议。

#### 📝 邮件列表

1. **[07-07 17:50]** [PATCH] KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-07 17:02]** Re: [PATCH] KVM: arm64: Fix potential leak in
 hyp_trace_buffer_alloc_bpages_backing
   - 发件人: sashiko-bot@kernel.org
3. **[07-07 19:32]** Re: [PATCH] KVM: arm64: Fix potential leak in hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[07-08 08:43]** Re: [PATCH] KVM: arm64: Fix potential leak in
 hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-08 16:19]** Re: [PATCH] KVM: arm64: Fix potential leak in
 hyp_trace_buffer_alloc_bpages_backing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 28: [PATCH v2 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Wed,  8 Jul 2026 08:54:31 +0100

#### 🤖 AI 总结

本邮件讨论主题为「[PATCH v2 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor」，主要涉及为 pKVM/nVHE 虚拟机监控器添加日志记录功能。

**原始 patch/问题的内容**：
该系列补丁引入了一个名为 "hyp_printk" 的事件，允许开发者将信息记录到虚拟机监控器的跟踪缓冲区，类似于内核中的 `trace_printk()` 函数。这一功能旨在增强调试能力，尤其是在 Android 的 pKVM 环境中。

**之前讨论要点**：
在历史讨论中，补丁的初步版本（v1）已经被提出，主要关注如何实现这一功能。开发者 Vincent Donnefort 在补丁中提到，添加此功能将有助于更早地启用跟踪，并对相关代码进行了清理。

**本周的新讨论、进展或结论**：
本周的讨论集中在补丁的具体实现上，包括：
1. **补丁 1**：允许在主机未被剥夺权限之前调用 pKVM 的共享和取消共享功能，以支持更早的跟踪。
2. **补丁 2**：将 `kvm_define_hypevents.h` 移动到更合适的位置以便于管理。
3. **补丁 3**：新增 `REMOTE_EVENT_CUSTOM_PRINTK()` 帮助器，支持动态打印格式。
4. **补丁 4**：实现 `trace_hyp_printk()`，允许开发者记录多种格式的日志信息。

所有补丁均已获得 Fuad Tabba 的审核和测试，显示出该功能的实现得到了积极的反馈和支持。整体来看，这一系列补丁将显著提升 pKVM/nVHE 的调试能力。

#### 📝 邮件列表

1. **[07-08 08:54]** [PATCH v2 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[07-08 08:54]** [PATCH v2 1/4] KVM: arm64: Allow early calls to pKVM host_share/unshare_hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[07-08 08:54]** [PATCH v2 2/4] KVM: arm64: Move kvm_define_hypevents.h to arch/arm64/kvm/
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[07-08 08:54]** [PATCH v2 3/4] tracing/remotes: Add REMOTE_EVENT_CUSTOM_PRINTK() helper
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[07-08 08:54]** [PATCH v2 4/4] KVM: arm64: Add hyp_printk event to nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 29: [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Thu,  2 Jul 2026 10:38:37 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）的补丁系列，旨在修复 Endpoint Memory Access Descriptor（EMAD）偏移量计算的问题。历史讨论中，Sebastian Ene 提出了一个补丁系列，主要解决 FF-A 版本 1.1 之前内存区域头部未明确指定 EMAD 偏移量的问题，并增加了必要的边界检查。

在本周的新讨论中，Marc Zyngier 确认已将补丁应用于修复，并列出了具体的提交内容，包括修复边界检查、验证内存访问描述符的偏移量、确保 FFA 范围页面对齐等。Will Deacon 也表示支持将驱动程序的更改通过 KVM 树进行合并，Marc 随后表示将会将这些补丁加入待处理列表。

总体来看，本周的讨论主要集中在补丁的应用和后续合并的确认上，显示出参与者对修复工作的积极响应和协作。

#### 📝 邮件列表

1. **[07-02 10:38]** [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[07-07 11:58]** Re: (subset) [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[07-07 12:56]** Re: (subset) [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset
 calculations
   - 发件人: Will Deacon <will@kernel.org>
4. **[07-07 15:03]** Re: (subset) [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-07 15:04]** Re: (subset) [PATCH v9 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 30: [PATCH] KVM: arm64: Avoid naming collision in tracing

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 12 Jul 2026 15:38:35 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在避免追踪功能中的命名冲突。补丁的主要内容是，当禁用超监视器追踪（CONFIG_NVHE_EL2_TRACING）时，定义了一个静态内联存根函数 `trace_clock()`，但该函数在 `linux/trace_clock.h` 中已被声明为外部函数。这可能导致编译时的命名冲突，尤其是在手动包含 `<nvhe/clock.h>` 时。

在之前的讨论中，参与者 Mostafa Saleh 提出了补丁，并指出当前的实现虽然没有立即的问题，但未来可能会因 SMMUv3 驱动的使用而引发更多冲突。Fuad Tabba 对补丁进行了审查，认为重命名是正确且完整的，并提出了两个小建议：一是补丁格式的细节，二是关于 `hyp_trace_clock` 的命名可能会造成可读性问题。

本周的新讨论中，Mostafa 和 Fuad 继续交流命名问题，Mostafa 提议添加 `hyp_` 前缀以避免冲突，而 Fuad 则建议使用 `el2_` 前缀，但对这个选择并不满意。整体来看，讨论集中在补丁的命名和格式上，参与者们积极寻求最佳解决方案。

#### 📝 邮件列表

1. **[07-12 15:38]** [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[07-12 17:19]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[07-12 19:19]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[07-12 20:30]** Re: [PATCH] KVM: arm64: Avoid naming collision in tracing
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 31: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 03 Jul 2026 17:25:05 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 的补丁，主题为「KVM: guest_memfd: 添加标志以从直接映射中移除」。该补丁旨在改进 KVM 中的内存管理，特别是在处理共享内存时的安全性和性能。

在历史讨论中，Brendan Jackman 和 Ackerley Tng 提到，补丁的原型已经完成，但存在一些关于内存页零化和故障路径的担忧。Ackerley 强调了在页面缓存中保持页面非存在状态的重要性，以避免在后续处理时丧失零化能力。

在本周的新讨论中，Sean Christopherson 表达了对补丁的看法，认为在主机中省略零化操作的复杂性不值得，尽管这可能会导致共享内存的安全性问题。他提到，尽量将内存管理工作与 guest_memfd 分开是更好的选择。Brendan Jackman 进一步支持这一观点，建议禁止对未映射页面使用 __GFP_ZERO 标志，以避免混淆。Lorenzo Stoakes 也表示支持这个方向，并认为当前的共识是合理的。

总体而言，本周的讨论集中在如何平衡性能与安全性，以及如何设计补丁以避免未来的复杂性。

#### 📝 邮件列表

1. **[07-03 17:25]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
2. **[07-06 16:09]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[07-10 08:50]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Brendan Jackman <brendan.jackman@linux.dev>
4. **[07-10 13:01]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Lorenzo Stoakes <ljs@kernel.org>

---

### Thread 32: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Wed,  1 Jul 2026 19:24:28 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在记录 pKVM 阶段 2 映射是否可缓存。原始补丁由 Bradley Morgan 提出，指出 pKVM 在执行阶段 2 操作时使用自己的映射列表，而在刷新路径中直接使用该列表，导致失去了通用阶段 2 遍历器所进行的 PTE 属性检查。因此，补丁建议记录映射是否可缓存，并跳过对不可缓存映射的缓存维护。

在历史讨论中，Dev Jain 和 Marc Zyngier 提出了对补丁的看法。Dev Jain 质疑是否需要 Fixes 标签，并讨论了缓存维护指令的适用性。Marc Zyngier 则强调了在不期望缓存的情况下执行缓存维护操作的无意义性，并指出了可能导致的问题。

在本周的新讨论中，Dev Jain 对 Marc Zyngier 的解释表示感谢，表明讨论在一定程度上达成了共识，但并未提出新的技术细节或进展。整体来看，补丁的必要性得到了认可，后续可能会继续深入讨论其实现细节。

#### 📝 邮件列表

1. **[07-01 19:24]** [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Bradley Morgan <include@grrlz.net>
2. **[07-05 19:38]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is
 cacheable
   - 发件人: Dev Jain <dev.jain@arm.com>
3. **[07-05 20:27]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is cacheable
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[07-09 19:36]** Re: [PATCH v4] KVM: arm64: Record whether pKVM stage 2 mapping is
 cacheable
   - 发件人: Dev Jain <dev.jain@arm.com>

---

### Thread 33: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 23 Jun 2026 11:41:39 -0700

#### 🤖 AI 总结

本邮件线程讨论了 KVM（Kernel-based Virtual Machine）在 arm64 架构下对硬件描述符更新的支持，特别是实现 FEAT_HAFDBS 和 FEAT_HAFT 特性。Oliver Upton 提出的补丁系列主要目的是为嵌套 MMU 添加对硬件脏状态和表访问标志的支持，尽管 KVM 本身并不直接使用这些特性，但内核在一级页表中确实需要。

在历史讨论中，Oliver 提出了补丁 [PATCH 07/22]，该补丁旨在为写入访问时在阶段 2 的描述符上设置脏状态。补丁的实现涉及对 `nested.c` 文件的修改，增加了对脏状态的处理逻辑。

在本周的新讨论中，Wei-Lin Chang 提到最新的 M.c Arm ARM 文档中，关于 R_RKMHW 的行为已不再适用，而是由 R_ZYGHJ 取代。Oliver 对此表示感谢，并承诺在补丁的 v2 版本中进行修正。这表明讨论者们在不断更新和完善补丁，以确保其符合最新的文档和标准。

#### 📝 邮件列表

1. **[06-23 11:41]** [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-23 11:41]** [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[07-06 17:50]** Re: [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[07-08 00:35]** Re: [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 34: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y

**📧 邮件数**: 4 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 06 Jul 2026 21:31:22 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于将 ARM64 VHE 启动修复程序回移植到 6.6.y 版本的补丁（PATCH 0/5）。该补丁旨在解决在 ARM64 虚拟化环境中启动时遇到的问题，特别是与 L1 嵌套客户机的启动挂起相关的故障。

在历史讨论中，参与者们已经对补丁的内容进行了初步审查，并讨论了补丁的必要性和适用性。特别是，Oliver Upton 提到在尝试使用这些补丁启动 6.1 版本时遇到了新的启动挂起问题，因此他认为在 6.1 或更早版本上应用补丁没有意义。

在本周的新讨论中，Colton Lewis 对 Oliver 的反馈进行了回应，确认将会在下一封邮件中包含更多上下文信息，并表示会确保测试所有相关模式。此外，Sasha Levin 也对补丁进行了审查，认为补丁内容较小，添加没有问题。整体来看，本周的讨论主要集中在补丁的审查和后续测试计划上，参与者们对补丁的实施持积极态度。

#### 📝 邮件列表

1. **[07-06 21:31]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[07-06 21:31]** Re: [PATCH 4/5] KVM: arm64: Initialize HCR_EL2.E2H early
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[07-06 21:32]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[07-06 21:32]** Re: [PATCH 0/5] Backport ARM64 VHE boot fixes to 6.6.y
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 35: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 8 Jul 2026 16:25:55 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现的 `pre_fault_memory` 功能的补丁（PATCH v5 2/5）。该补丁旨在添加一种机制，以便在处理内存故障时预先映射特定的地址范围。

在之前的讨论中，参与者 Jack Thomson 提到，故障处理机制已经重构，使用 `struct kvm_s2_fault_desc` 来存储故障信息，并对补丁的实现细节进行了初步探讨。然而，关于 `KVM_PRE_FAULT_MEMORY` 的具体功能，Alexandru Elisei 提出了疑问，想了解该功能是否能保证在 ioctl 完成后，指定的地址范围仍然映射在虚拟机的 stage 2 表中。

在本周的新讨论中，Alexandru Elisei 经过思考后意识到，KVM 不能保证在 ioctl 返回后内存仍然映射，因此他自我解答了之前的疑问。此外，他还指出，文档中提到的“新创建的 stage-2 PTEs 被标记为已访问”并未说明现有的 PTEs 是否也会被标记，这一细节值得进一步解释。整体来看，本周的讨论主要集中在对补丁功能的理解和实现细节的澄清上。

#### 📝 邮件列表

1. **[07-08 16:25]** Re: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-10 17:00]** Re: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[07-10 17:03]** Re: [PATCH v5 2/5] KVM: arm64: Add pre_fault_memory implementation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 36: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  6 Jul 2026 15:01:28 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中支持 FEAT_HDBSS 的补丁（PATCH v3 3/5）。该补丁旨在增强 KVM 的功能，以适应最新的硬件特性。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁的提出是为了实现与 HACDBS v2 相关的新特性，提升虚拟化性能和兼容性。

在本周的新讨论中，参与者主要是 Tian Zheng 和 Leonardo Bras。Tian 提到他已经完成了补丁的 v4 版本，并进行了最后的内部审查。他在新版本中对照了最新的 HACDBS v2 实现，特别是在初始化阶段中自动插入 KVM_PGTABLE_S2_DBM 的标志。此外，他指出 v4 版本尚未支持脏环模式，当前系列主要集中在脏位图模式，并计划在提交信息中明确说明这一点，以避免审查过程中的混淆。Tian 计划在本周晚些时候发布 v4 版本。

整体来看，本周的讨论主要集中在补丁的进展和即将发布的新版本上，显示出开发者之间的积极沟通与合作。

#### 📝 邮件列表

1. **[07-06 15:01]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[07-07 14:11]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[07-07 11:07]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 37: [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  1 Jul 2026 16:16:18 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 S2 权限放宽的修复补丁。

**原始 patch/问题内容**：
Oliver Upton 提出了两个小修复补丁，旨在解决 S2 权限放宽过程中的问题。第一个补丁涉及在更新 PTE（Page Table Entry）时可能使用未初始化的栈变量作为 TLBI TTL（Translation Lookaside Buffer Invalidation Time-to-Live）提示，可能导致过时的 TLB 条目保持有效。第二个补丁则是针对权限放宽过程中无条件更新 XN（Execute Never）属性的问题。

**之前讨论要点**：
在历史讨论中，Upton 详细解释了这两个补丁的潜在问题和解决方案，强调了在权限放宽时需要确保状态的正确性，以避免不必要的错误。

**本周的新讨论、进展或结论**：
在本周的讨论中，Marc Zyngier 确认已将这两个补丁应用到修复列表中，并感谢 Upton 的贡献。补丁已成功提交，分别为确保在放宽权限时级别始终初始化和仅在请求时更新 XN 属性。这标志着该问题的解决进展。

#### 📝 邮件列表

1. **[07-01 16:16]** [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[07-06 17:19]** Re: [PATCH 0/2] KVM: arm64: Fixes for S2 permission relaxation
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 38: [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 27 Jun 2026 11:51:05 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 的补丁，主题为“将 kvm_io_bus_get_dev() 的锁定责任移交给调用者”。该补丁的目的是解决在调用 kvm_io_bus_get_dev() 时可能出现的生命周期问题，因为该函数返回的设备仅通过地址匹配，若返回的设备类型不符合预期，调用者在检查对象时可能会遇到问题。

在历史讨论中，Marc Zyngier 提出了这个补丁，指出由于该辅助函数只有一个使用者，最简单的解决方案是将锁定责任转移给调用者，这样调用者可以根据需要保持 srcu 锁的持有状态，从而避免潜在的生命周期问题。

在本周的新讨论中，Marc Zyngier 确认该补丁已被应用于修复集，并表示感谢。这表明补丁已成功整合到代码库中，解决了之前提到的问题。整体来看，这次讨论围绕着 KVM 的锁定机制进行了有效的改进，确保了设备的正确管理。

#### 📝 邮件列表

1. **[06-27 11:51]** [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[07-06 17:19]** Re: [PATCH v2] KVM: Move kvm_io_bus_get_dev() locking responsibilities to callers
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 39: [PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 09 Jul 2026 20:30:07 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM64 架构的补丁，具体内容为“[PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1”。该补丁的目的是为 ID_AA64MMFR4_EL1 寄存器添加新的布局，以便更好地支持系统寄存器的管理。

在历史讨论中，没有提供具体的背景信息或之前的讨论内容，因此我们无法了解该补丁的前期讨论要点。

在本周的新讨论中，参与者 Colton Lewis 对 Marc Zyngier 的回复表示感谢，并提到他从中学到了不少技巧，同时承诺会在后续的补丁中包含他的签名（SoB）。这表明该补丁的讨论正在进行中，且参与者之间的交流是积极的，但目前尚未看到具体的技术反馈或进一步的修改建议。

总结而言，本周的讨论主要集中在补丁的后续处理和参与者之间的互动上，尚未涉及具体的技术细节或问题解决。

#### 📝 邮件列表

1. **[07-09 20:30]** Re: [PATCH 6.6 v2 1/6] arm64: sysreg: Add layout for ID_AA64MMFR4_EL1
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 40: [PATCH v1 1/4] KVM: arm64: Allow early calls to pKVM
 host_share/unshare_hyp

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 7 Jul 2026 17:53:30 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上进行的补丁，具体内容是允许对 pKVM 的早期调用，涉及到 host_share 和 unshare_hyp 的功能。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁旨在改善 KVM 的功能，可能是为了提升虚拟化性能或简化某些操作的流程。

在本周的新讨论中，参与者 Vincent Donnefort 回复了 Fuad Tabba 的邮件，提到他已经在 lore.kernel.org 上发布了相关的补丁信息。这表明该补丁的开发正在推进，并且可能会在未来的讨论中得到更多的反馈和审查。

总体而言，本周的讨论主要集中在补丁的发布和后续的跟进上，尚未涉及具体的技术细节或反馈。

#### 📝 邮件列表

1. **[07-07 17:53]** Re: [PATCH v1 1/4] KVM: arm64: Allow early calls to pKVM
 host_share/unshare_hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 41: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 6 Jul 2026 09:43:24 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM64 架构的补丁（PATCH v14 26/44），其目的是允许在 RMI（Remote Memory Interface）中填充初始内容。该补丁的具体内容尚未详细描述，但其目标是增强 ARM64 的内存管理功能。

在之前的讨论中，提到了一些关键的修改和检查，其中 Steven Price 指出，Sean 最近将某个检查移至调用 `kvm_gmem_populate()` 之前，并返回了错误代码 -EINVAL。这一修改的理由也适用于 CCA（Cache Coherency Architecture），暗示在内存管理过程中需要更严格的检查。

在本周的新讨论中，Ackerley Tng 引用了 Steven Price 的观点，强调了对补丁逻辑的进一步理解和应用。这表明参与者们正在积极评估补丁的影响，并考虑如何确保在内存填充过程中遵循正确的检查机制。

总体来看，本周的讨论集中在对补丁逻辑的深入分析和潜在影响的评估上，显示出对 ARM64 内存管理改进的持续关注。

#### 📝 邮件列表

1. **[07-06 09:43]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

## 📌 RFC

共 2 个 thread

---

### Thread 1: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots

**📧 邮件数**: 20 | **👥 参与者**: 5 | **📅 开始时间**: Thu,  2 Jul 2026 15:29:09 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的一项补丁，旨在为仅支持 `guest_memfd` 的内存插槽实现脏页日志记录功能。补丁的主要内容包括允许对共享内存进行脏页日志记录，并且架构可以通过 `KVM_CAP_GUEST_MEMFD_MMAP_LOG_DIRTY_PAGES` 能力来声明对该功能的支持。

在历史讨论中，Alexandru Elisei 提出了三个补丁，分别涉及如何使用内存插槽 ID 跟踪关联的内存插槽、实现脏页日志记录，以及对 `guest_memfd` 的支持。讨论中提到，当前 KVM 不允许更改由 `guest_memfd` 支持的内存插槽的标志，只能创建和删除这些插槽。

在本周的新讨论中，参与者们对补丁进行了深入的技术审查。David Hildenbrand 提出了对补丁文档化的建议，认为需要明确补丁的目的和使用场景。Sean Christopherson 则讨论了在更新内存插槽标志时可能出现的竞争条件，并质疑是否需要引入额外的布尔值来平衡更新。Alexandru 进一步解释了补丁的设计思路，强调了在处理内存插槽更新时需要避免的不一致状态，并提出了对补丁的改进建议。

总体来看，讨论集中在补丁的实现细节、潜在的竞争条件以及如何确保在用户空间和内核之间的内存一致性等问题上。参与者们对补丁的必要性和可行性表示关注，并探讨了未来可能的改进方向。

#### 📝 邮件列表

1. **[07-02 15:29]** [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[07-02 15:29]** [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[07-02 15:29]** [RFC PATCH 2/3] KVM: Implement dirty page logging for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[07-06 09:14]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
5. **[07-06 14:45]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
6. **[07-06 14:43]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[07-06 14:46]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track of
 associated memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[07-06 17:56]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[07-06 18:29]** Re: [RFC PATCH 2/3] KVM: Implement dirty page logging for
 guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[07-07 17:58]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
11. **[07-07 18:05]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
12. **[07-07 18:05]** Re: [RFC PATCH 1/3] KVM: guest_memfd: Use memslot id to keep track
 of associated memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
13. **[07-07 18:12]** Re: [RFC PATCH 2/3] KVM: Implement dirty page logging for
 guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
14. **[07-07 10:12]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
15. **[07-09 12:21]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Mark Rutland <mark.rutland@arm.com>
16. **[07-09 12:01]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
17. **[07-09 13:33]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Oliver Upton <oupton@kernel.org>
18. **[07-10 11:26]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Mark Rutland <mark.rutland@arm.com>
19. **[07-10 11:44]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
20. **[07-10 11:18]** Re: [RFC PATCH 0/3] KVM: Dirty page logging for guest_memfd-only
 memslots
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 2: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 06 Jul 2026 14:28:11 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为“query-arm-cpu-props-info”的 RFC PATCH（版本2，第23个补丁），主要针对 ARM 架构的 QEMU 目标。该补丁旨在添加一个新的查询功能，以获取 ARM CPU 属性信息。

在历史讨论中，并没有提供具体的上下文或之前的讨论内容，因此我们无法得知补丁的详细背景或早期的争论点。

在本周的新讨论中，参与者 Markus Armbruster 对 Khushit Shah 提出的关于使用结构体（struct）来实现动态类型的建议进行了回应。他表示，使用结构体来组织数据是一种合理的方式，尤其是在 QAPI（QEMU 应用程序接口）中实现动态类型时。他还提到自己需要进一步理解在此处使用动态类型的原因。

总体来看，本周的讨论集中在如何更有效地实现动态类型的结构上，尽管没有达成明确的结论，但参与者之间的互动显示出对补丁内容的深入思考。

#### 📝 邮件列表

1. **[07-06 14:28]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Markus Armbruster <armbru@redhat.com>

---

## 📌 Question

共 1 个 thread

---

### Thread 1: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP

**📧 邮件数**: 12 | **👥 参与者**: 6 | **📅 开始时间**: Sat, 4 Jul 2026 15:45:56 +0800

#### 🤖 AI 总结

本邮件线程讨论了在 KVM 中，如何确保每个虚拟 CPU (vCPU) 的 TLB 和 I-cache 是私有的，尤其是在 VTTBR_EL2.CnP 设置为 1 的情况下。

**原始 patch/问题内容**：讨论的核心在于 `kvm_arch_vcpu_load()` 函数中的 TLB 和 I-cache 失效机制是否足够保证每个 vCPU 的私有性。Tangnianyao 提出，当 VTTBR_EL2.CnP 为 1 时，当前的失效机制似乎无法确保这一点。

**之前讨论要点**：Wei-Lin Chang 指出，若涉及两个阶段的 TLB 共享，必须在两个阶段都设置 CnP 为 1，才能允许 TLB 条目共享。Tangnianyao 质疑在某些情况下，KVM 的失效机制可能不足以保证 vCPU 的私有性，尤其是在多个 vCPU 同时运行于同一物理核心的 SMT 线程时。

**本周新讨论和进展**：本周的讨论中，Tangnianyao 和其他参与者进一步探讨了 CnP 设置对 TLB 共享的影响。Marc Zyngier 强调，若 TLB 被多个处理单元共享，KVM 需要忽略来宾的设置，以确保安全性。Oliver Upton 也补充道，KVM 仍需在 CnP 为 0 的情况下进行失效，以维护每个 vCPU 的私有性。整体来看，讨论集中在如何平衡性能与私有性保障之间的矛盾。

#### 📝 邮件列表

1. **[07-04 15:45]** Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
2. **[07-05 18:28]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[07-06 11:30]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
4. **[07-06 08:25]** Re: Question about the "TLBs and I-cache are private to each vCPU" guarantee with VTTBR_EL2.CnP
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[07-06 16:25]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
6. **[07-06 09:44]** Re: Question about the "TLBs and I-cache are private to each vCPU" guarantee with VTTBR_EL2.CnP
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[07-06 22:15]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
8. **[07-06 16:18]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Will Deacon <will@kernel.org>
9. **[07-06 16:33]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[07-07 10:41]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>
11. **[07-06 23:36]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[07-08 16:10]** Re: Question about the "TLBs and I-cache are private to each vCPU"
 guarantee with VTTBR_EL2.CnP
   - 发件人: Tangnianyao <tangnianyao@huawei.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.2, take #2

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed,  8 Jul 2026 17:12:42 +0100

#### 🤖 AI 总结

本邮件讨论了 KVM/arm64 在 7.2 版本中的第二批修复补丁。Marc Zyngier 提交了这组补丁，主要解决了以下几个问题：首先，修复了 `kvm_io_bus_get_dev()` 函数中的锁定问题，确保返回对象类型的检查不存在线程竞争；其次，修复了在放宽权限时页面表遍历级别的初始化问题；再次，正确更新放宽权限时的 XN 属性；最后，修复了从仿真 MMIO 区域加载数据时的符号扩展问题。此外，还包括一系列针对 pKVM 的 FFA 代理修复和 FFA 驱动的调整。

在之前的讨论中，邮件提到这组补丁是基于 12 天前发布的 `kvmarm-fixes-7.2-1` 标签的基础上进行的更新。 

本周的新讨论中，Marc Zyngier 请求将这些修复补丁合并到主线代码中，并提供了相关的 Git 仓库链接供拉取最新更改。整体来看，这些补丁旨在提高 KVM/arm64 的稳定性和性能，解决了一些历史遗留问题。

#### 📝 邮件列表

1. **[07-08 17:12]** [GIT PULL] KVM/arm64 fixes for 7.2, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Discussion

共 1 个 thread

---

### Thread 1: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 26 Jun 2026 10:48:05 +0200

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在 Linux 内核时间管理中添加对 AUX 时钟的支持，具体是针对 `ktime_get_snapshot_id()` 函数的补丁（patch 09/24）。

**原始 patch/问题的内容**：
该补丁旨在为 `ktime_get_snapshot_id()` 函数添加对 AUX 时钟的支持，以便能够正确处理与 AUX 时钟相关的时间戳。

**之前讨论要点**：
在历史讨论中，参与者探讨了 AUX 时钟与全局 MONORAW 时钟之间的关系，指出 AUX 时钟的 MONORAW 值应基于其自身的时钟源而非全局时钟。此外，讨论中提到需要统一不同时间管理器之间的锁定机制，并对相关文档进行了澄清，以确保在代码和文档中正确描述与 AUX 时钟相关的时间戳。

**本周的新讨论、进展或结论**：
在本周的讨论中，Thomas Weißschuh 对补丁进行了审查，并表示感谢，确认补丁的内容得到了认可。此时，补丁已被标记为“Reviewed”，表明其准备进入下一步的处理阶段。

总体来看，讨论围绕 AUX 时钟的支持展开，强调了时间戳的准确性和文档的清晰性，且补丁在本周获得了积极的反馈。

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
8. **[07-06 10:42]** Re: [PATCH] timekeeping: Document monotonic raw timestamps in
 snapshots correctly
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [linux-next:master] BUILD REGRESSION
 5c73cd9f0819c1c44e373e3dabb68318b1de1a12

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 08 Jul 2026 09:52:07 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个与 Linux 内核构建相关的回归问题，主题为「BUILD REGRESSION」。该问题源于最近的提交（5c73cd9f0819c1c44e373e3dabb68318b1de1a12），该提交添加了针对 20260707 的 Linux-next 特定文件。

在本周的讨论中，内核测试机器人报告了多个错误和警告，包括：
1. 在 `arch/arm64/kvm/hyp/pgtable.c` 中，存在从 `int` 到 `s8` 的隐式转换警告。
2. 在 `include/vdso/limits.h` 中，存在从 `int` 到 `s8` 的溢出警告。
3. 在 `kernel/bpf/task_iter.c` 中，变量 `mmput_needed` 被设置但未使用的警告。

此外，还报告了一个可能的内部编译器错误，涉及 `drivers/mtd/parsers/redboot.c`。

本周的进展主要集中在确认这些错误和警告的性质，开发者们被鼓励检查这些问题是否为假阳性。邮件中没有提及具体的修复方案或后续步骤，但测试结果显示共测试了 279 种配置，表明该问题的影响范围较广。

#### 📝 邮件列表

1. **[07-08 09:52]** [linux-next:master] BUILD REGRESSION
 5c73cd9f0819c1c44e373e3dabb68318b1de1a12
   - 发件人: kernel test robot <lkp@intel.com>

---

