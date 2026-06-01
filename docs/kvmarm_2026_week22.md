# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-06-01 00:57:30

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 473
- **总 Thread 数**: 37
- **大型 Thread** (>20封): 8 个

### 分类分布

- **PATCH**: 29 threads (335 邮件)
- **RFC**: 3 threads (24 邮件)
- **Bug Report**: 1 threads (2 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Other**: 3 threads (110 邮件)

---

## 📌 PATCH

共 29 个 thread

---

### Thread 1: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups

**📧 邮件数**: 78 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 21 May 2026 14:25:38 +0100

#### 🤖 AI 总结

在本邮件列表讨论中，Mark Rutland 提出了一个关于 ARM64 和 KVM 的清理补丁系列，共18个补丁，旨在简化 FPSIMD、SVE 和 SME 的状态管理代码，以提高可维护性和调试能力。补丁的主要目标是消除冗余代码，使用不透明类型来管理状态，简化保存和恢复逻辑。

在历史讨论中，补丁系列的背景和目标被详细阐述，强调这是纯粹的代码清理，没有修复任何错误。参与者们对各个补丁进行了审查，并提出了一些小的修改建议。

本周的新讨论中，Mark Rutland 和其他参与者继续对补丁进行审查和讨论，许多补丁获得了“Reviewed-by”的确认，表明它们得到了认可。Rutland 还回应了关于使用 GCC 和 LLVM 的约束问题，并表示将根据工具链的支持情况进行调整。此外，参与者们讨论了补丁合并的方式，Rutland 计划在本周末发布补丁的第二个版本，以解决当前讨论中提出的反馈和建议。总体来看，讨论氛围积极，大家对补丁的方向表示支持。

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
20. **[05-26 15:08]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
21. **[05-26 15:18]** Re: [PATCH 01/18] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[05-26 15:27]** Re: [PATCH 02/18] KVM: arm64: Don't override FFR save/restore
 argument
   - 发件人: Mark Brown <broonie@kernel.org>
23. **[05-26 15:39]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
24. **[05-26 16:28]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
25. **[05-26 16:28]** Re: [PATCH 05/18] arm64: fpsimd: Fold sve_init_regs() into
 do_sve_acc()
   - 发件人: Mark Brown <broonie@kernel.org>
26. **[05-26 16:42]** Re: [PATCH 06/18] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Mark Brown <broonie@kernel.org>
27. **[05-26 16:43]** Re: [PATCH 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Brown <broonie@kernel.org>
28. **[05-26 16:45]** Re: [PATCH 08/18] arm64: fpsimd: Use assembler for baseline SME
 instructions
   - 发件人: Mark Brown <broonie@kernel.org>
29. **[05-26 16:47]** Re: [PATCH 09/18] arm64: fpsimd: Move sve_get_vl() and sme_get_vl()
 inline
   - 发件人: Mark Brown <broonie@kernel.org>
30. **[05-26 16:55]** Re: [PATCH 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Brown <broonie@kernel.org>
31. **[05-26 17:28]** Re: [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Mark Brown <broonie@kernel.org>
32. **[05-26 17:38]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
33. **[05-26 17:44]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Brown <broonie@kernel.org>
34. **[05-26 17:51]** Re: [PATCH 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Rutland <mark.rutland@arm.com>
35. **[05-26 17:53]** Re: [PATCH 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Brown <broonie@kernel.org>
36. **[05-26 17:54]** Re: [PATCH 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Brown <broonie@kernel.org>
37. **[05-26 17:56]** Re: [PATCH 14/18] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Mark Brown <broonie@kernel.org>
38. **[05-27 09:07]** Re: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Marc Zyngier <maz@kernel.org>
39. **[05-27 10:00]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
40. **[05-27 11:10]** Re: [PATCH 01/18] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
41. **[05-27 11:16]** Re: [PATCH 02/18] KVM: arm64: Don't override FFR save/restore
 argument
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
42. **[05-27 11:29]** Re: [PATCH 03/18] KVM: arm64: pkvm: Save host FPMR in host cpu
 context
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
43. **[05-27 11:32]** Re: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
44. **[05-27 12:58]** Re: [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
45. **[05-27 13:05]** Re: [PATCH 05/18] arm64: fpsimd: Fold sve_init_regs() into
 do_sve_acc()
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
46. **[05-27 13:29]** Re: [PATCH 15/18] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Mark Brown <broonie@kernel.org>
47. **[05-27 13:50]** Re: [PATCH 06/18] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
48. **[05-27 13:54]** Re: [PATCH 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Brown <broonie@kernel.org>
49. **[05-27 13:58]** Re: [PATCH 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
50. **[05-27 14:06]** Re: [PATCH 08/18] arm64: fpsimd: Use assembler for baseline SME
 instructions
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
51. **[05-27 14:18]** Re: [PATCH 09/18] arm64: fpsimd: Move sve_get_vl() and sme_get_vl()
 inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
52. **[05-27 14:44]** Re: [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
53. **[05-27 14:51]** Re: [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
54. **[05-27 15:13]** Re: [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Mark Brown <broonie@kernel.org>
55. **[05-27 15:36]** Re: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Will Deacon <will@kernel.org>
56. **[05-27 15:49]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
57. **[05-27 16:34]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
58. **[05-27 17:02]** Re: [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
59. **[05-27 17:10]** Re: [PATCH 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
60. **[05-27 17:11]** Re: [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
61. **[05-27 17:13]** Re: [PATCH 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
62. **[05-27 17:13]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
63. **[05-27 17:23]** Re: [PATCH 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
64. **[05-28 10:45]** Re: [PATCH 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
65. **[05-28 10:51]** Re: [PATCH 14/18] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
66. **[05-28 11:39]** Re: [PATCH 15/18] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
67. **[05-28 11:49]** Re: [PATCH 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
68. **[05-28 13:30]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
69. **[05-28 14:10]** Re: [PATCH 18/18] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
70. **[05-28 14:21]** Re: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
71. **[05-28 15:39]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
72. **[05-28 16:09]** Re: [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
73. **[05-28 16:12]** Re: [PATCH 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
74. **[05-28 17:15]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
75. **[05-28 17:25]** Re: [PATCH 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
76. **[05-28 17:28]** Re: [PATCH 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
77. **[05-28 17:39]** Re: [PATCH 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Brown <broonie@kernel.org>
78. **[05-29 10:10]** Re: [PATCH 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 2: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 53 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 19 May 2026 15:27:14 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于增强 KVM/ARM 的补丁系列，主要目的是引入可定制的 AArch64 KVM 主机模型。该补丁允许用户空间覆盖部分 ID 寄存器的值，以提高在不同主机硬件之间迁移虚拟机的灵活性。

在历史讨论中，Eric Auger 提出了多个补丁，逐步实现了对 ID 寄存器的可写性支持，包括生成寄存器属性定义的脚本、初始化可写 ID 寄存器、以及将修改后的 ID 寄存器值写回 KVM 等功能。这些补丁的目标是使 KVM 能够更好地适应不同的硬件环境。

在本周的新讨论中，参与者们对补丁进行了审查并提出了一些问题和建议。Sebastian Ott 对多个补丁给予了“审核通过”的反馈。Khushit Shah 则提出了一些技术细节，例如在处理 ID 寄存器时需要考虑的条件，以及如何在不同的虚拟化配置下确保 ID 寄存器的正确性。他还建议在生成的 cpu-idregs.h.inc 文件中包含 RES0/1 字段的信息，以便更好地管理寄存器的可写性。

总体来看，本周的讨论集中在补丁的细节和潜在问题上，参与者们积极交流，推动补丁的完善与实施。

#### 📝 邮件列表

1. **[05-19 15:27]** [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[05-19 15:27]** [PATCH v5 06/18] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-19 15:27]** [PATCH v5 08/18] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[05-19 15:27]** [PATCH v5 10/18] target/arm/cpu64: Retrieve writable ID reg map in aarch64_host_initfn()
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-19 15:27]** [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[05-19 15:27]** [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-19 15:27]** [PATCH v5 13/18] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[05-19 15:27]** [PATCH v5 14/18] target/arm/kvm: Special case REVIDR_EL1 and AIDR_EL1
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[05-19 15:27]** [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that shouldn't be
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[05-19 15:27]** [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[05-19 15:27]** [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[05-19 15:27]** [PATCH v5 18/18] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[05-26 16:42]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Sebastian Ott <sebott@redhat.com>
14. **[05-26 16:51]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Sebastian Ott <sebott@redhat.com>
15. **[05-26 17:08]** Re: [PATCH v5 14/18] target/arm/kvm: Special case REVIDR_EL1 and
 AIDR_EL1
   - 发件人: Sebastian Ott <sebott@redhat.com>
16. **[05-27 08:29]** Re: [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Sebastian Ott <sebott@redhat.com>
17. **[05-27 08:37]** Re: [PATCH v5 18/18] arm/cpu-features: document ID reg properties
   - 发件人: Sebastian Ott <sebott@redhat.com>
18. **[05-27 14:35]** Re: [PATCH v5 06/18] scripts: Introduce
 scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
19. **[05-27 14:42]** Re: [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[05-27 14:46]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
21. **[05-27 14:52]** Re: [PATCH v5 08/18] target/arm/cpu_idregs: generate tables for Arm64
 ID registers and fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[05-27 14:54]** Re: [PATCH v5 10/18] target/arm/cpu64: Retrieve writable ID reg map
 in aarch64_host_initfn()
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
23. **[05-27 15:02]** Re: [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers
 from host
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[05-27 15:08]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
25. **[05-27 17:11]** Re: [PATCH v5 06/18] scripts: Introduce
 scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
26. **[05-27 17:14]** Re: [PATCH v5 08/18] target/arm/cpu_idregs: generate tables for Arm64
 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
27. **[05-27 15:16]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
28. **[05-27 15:17]** Re: [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
29. **[05-27 17:17]** Re: [PATCH v5 10/18] target/arm/cpu64: Retrieve writable ID reg map
 in aarch64_host_initfn()
   - 发件人: Eric Auger <eric.auger@redhat.com>
30. **[05-27 17:25]** Re: [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers
 from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
31. **[05-27 15:28]** Re: [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
32. **[05-27 17:30]** Re: [PATCH v5 11/18] arm/kvm: Initialize all writable ID registers
 from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
33. **[05-27 17:32]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
34. **[05-27 15:33]** Re: [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
35. **[05-27 15:44]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
36. **[05-27 17:45]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Eric Auger <eric.auger@redhat.com>
37. **[05-27 17:51]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
38. **[05-27 15:54]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
39. **[05-27 17:55]** Re: [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Eric Auger <eric.auger@redhat.com>
40. **[05-27 15:56]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
41. **[05-27 18:01]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Eric Auger <eric.auger@redhat.com>
42. **[05-27 18:04]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
43. **[05-27 16:11]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
44. **[05-27 16:16]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
45. **[05-27 18:19]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
46. **[05-27 18:30]** Re: [PATCH v5 15/18] target/arm/kvm: Ignore some writable bits that
 shouldn't be
   - 发件人: Eric Auger <eric.auger@redhat.com>
47. **[05-27 19:20]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
48. **[05-28 05:07]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
49. **[05-28 05:29]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
50. **[05-28 17:14]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
51. **[05-28 17:22]** Re: [PATCH v5 13/18] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
52. **[05-28 19:31]** Re: [PATCH v5 16/18] target/arm/cpu: Expose writable ID reg field
 properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
53. **[05-28 19:35]** Re: [PATCH v5 12/18] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 3: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 32 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 13 May 2026 14:17:08 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的 KVM 中对 Arm CCA（保密计算架构）的支持，主要通过一系列补丁（PATCH v14 00/44）进行实现。

**原始补丁内容**：
补丁系列旨在为 KVM 添加对保护虚拟机的支持，利用 Arm CCA 的特性。补丁包括对 RMM（Realm Management Monitor）的多项更新，增强了对虚拟 CPU 和内存管理的支持。

**之前讨论要点**：
在历史讨论中，Steven Price 提出了补丁的多个关键更新，包括简化用户 API、支持 RMI（Realm Management Interface）和 GIC（通用中断控制器）状态的传递等。讨论中还涉及到 RMI 版本检查和错误处理的有效性，确保在初始化时能够正确返回状态。

**本周新讨论进展**：
本周的讨论集中在补丁的细节改进上，参与者提出了对补丁描述的修改建议，强调了在 commit 信息中清晰表述 CAP 和 ioctl 名称的重要性。此外，Gavin Shan 和 Wei-Lin Chang 针对补丁中的具体实现提出了简化和改进的建议，如简化变量使用、改进错误处理逻辑等。Marc Zyngier 也对补丁的主题和结构提出了疑问，要求更清晰的文档说明和一致性。

整体来看，本周的讨论进一步推动了补丁的完善，确保其在实现 KVM 对 Arm CCA 支持时的有效性和可维护性。

#### 📝 邮件列表

1. **[05-13 14:17]** [PATCH v14 00/44] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[05-13 14:17]** [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
3. **[05-13 14:17]** [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
4. **[05-13 14:17]** [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Steven Price <steven.price@arm.com>
5. **[05-13 14:17]** [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
6. **[05-13 14:17]** [PATCH v14 19/44] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
7. **[05-13 14:17]** [PATCH v14 20/44] arm64: RMI: Support for the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
8. **[05-13 14:17]** [PATCH v14 21/44] KVM: arm64: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
9. **[05-13 14:17]** [PATCH v14 22/44] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
10. **[05-13 14:17]** [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>
11. **[05-13 14:17]** [PATCH v14 24/44] KVM: arm64: Handle realm MMIO emulation
   - 发件人: Steven Price <steven.price@arm.com>
12. **[05-13 14:17]** [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
13. **[05-13 14:17]** [PATCH v14 28/44] arm64: RMI: Create the realm descriptor
   - 发件人: Steven Price <steven.price@arm.com>
14. **[05-13 14:17]** [PATCH v14 32/44] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Steven Price <steven.price@arm.com>
15. **[05-21 10:39]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
16. **[05-21 16:49]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
17. **[05-25 16:58]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
18. **[05-26 23:17]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
19. **[05-26 23:27]** Re: [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
20. **[05-26 23:32]** Re: [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
21. **[05-26 23:39]** Re: [PATCH v14 19/44] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
22. **[05-26 23:47]** Re: [PATCH v14 28/44] arm64: RMI: Create the realm descriptor
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
23. **[05-27 11:52]** Re: [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
24. **[05-27 16:21]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[05-28 14:07]** Re: [PATCH v14 20/44] arm64: RMI: Support for the VGIC in realms
   - 发件人: Gavin Shan <gshan@redhat.com>
26. **[05-28 14:11]** Re: [PATCH v14 21/44] KVM: arm64: Support timers in realm RECs
   - 发件人: Gavin Shan <gshan@redhat.com>
27. **[05-28 14:38]** Re: [PATCH v14 22/44] arm64: RMI: Handle realm enter/exit
   - 发件人: Gavin Shan <gshan@redhat.com>
28. **[05-28 15:03]** Re: [PATCH v14 24/44] KVM: arm64: Handle realm MMIO emulation
   - 发件人: Gavin Shan <gshan@redhat.com>
29. **[05-28 15:30]** Re: [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Gavin Shan <gshan@redhat.com>
30. **[05-28 15:51]** Re: [PATCH v14 28/44] arm64: RMI: Create the realm descriptor
   - 发件人: Gavin Shan <gshan@redhat.com>
31. **[05-28 16:55]** Re: [PATCH v14 32/44] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Gavin Shan <gshan@redhat.com>
32. **[05-28 08:10]** Re: [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 4: [PATCH v3 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 28 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 29 May 2026 17:50:14 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 161473 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:28, 120479 tokens)

#### 📝 邮件列表

1. **[05-29 17:50]** [PATCH v3 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[05-29 17:50]** [PATCH v3 01/27] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[05-29 17:50]** [PATCH v3 02/27] KVM, vfio: remove symbol_get(kvm_get_kvm_safe) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[05-29 17:50]** [PATCH v3 03/27] KVM, vfio: remove symbol_get(kvm_put_kvm) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[05-29 17:50]** [PATCH v3 04/27] uapi: KVM: Provide arm64 UAPI for other host architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[05-29 17:50]** [PATCH v3 05/27] arm64: Extract sysreg definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[05-29 17:50]** [PATCH v3 06/27] arm64: Provide arm64 API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[05-29 17:50]** [PATCH v3 07/27] KVM: arm64: Provide arm64 KVM API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[05-29 17:50]** [PATCH v3 08/27] arm64: Extract pstate definitions from ptrace
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[05-29 17:50]** [PATCH v3 09/27] KVM: arm64: Share kvm_emulate definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[05-29 17:50]** [PATCH v3 10/27] KVM: arm64: Make some arm64 KVM code shareable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[05-29 17:50]** [PATCH v3 11/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[05-29 17:50]** [PATCH v3 12/27] KVM: arm64: Share reset general register code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[05-29 17:50]** [PATCH v3 13/27] KVM: arm64: Extract & share ipa size shift calculation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[05-29 17:50]** [PATCH v3 14/27] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[05-29 17:50]** [PATCH v3 15/27] KVM: S390: Refactor gmap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[05-29 17:50]** [PATCH v3 16/27] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[05-29 17:50]** [PATCH v3 17/27] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[05-29 17:50]** [PATCH v3 18/27] KVM: s390: Prepare kvm-s390 for a second kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[05-29 17:50]** [PATCH v3 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[05-29 17:50]** [PATCH v3 20/27] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[05-29 17:50]** [PATCH v3 21/27] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[05-29 17:50]** [PATCH v3 22/27] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[05-29 17:50]** [PATCH v3 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[05-29 17:50]** [PATCH v3 24/27] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[05-29 17:50]** [PATCH v3 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[05-29 17:50]** [PATCH v3 26/27] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[05-29 17:50]** [PATCH v3 27/27] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 5: [PATCH v1 00/26] KVM: arm64 on s390 System Register Handling

**📧 邮件数**: 27 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 29 May 2026 17:55:33 +0200

#### 🤖 AI 总结

本邮件列表讨论的主题是关于在 s390 架构上实现 KVM 的 arm64 系统寄存器处理。以下是讨论的主要内容：

1. **原始 Patch/问题内容**：
   - 提交了一系列补丁（共26个），主要目的是为 KVM/arm64 在 s390 主机上增加系统寄存器处理能力。这包括重构和共享 KVM/arm64 代码，添加 ARM 客户管理功能，以及实现主机的系统寄存器和异常处理。

2. **之前讨论要点**：
   - 之前的讨论集中在如何有效地重构和共享代码，以便在不同架构之间实现寄存器的访问和管理。参与者们讨论了如何处理寄存器的读写、异常注入以及如何确保在不同架构间的兼容性。

3. **本周的新讨论、进展或结论**：
   - 本周的讨论主要集中在具体的补丁实现上，包括对系统寄存器的访问、异常处理机制的实现，以及如何在 s390 上支持 arm64 的特性。补丁中实现了对 ARM 系统寄存器的查询、读写和异常处理，确保了在 KVM 环境下的正确性和性能。此外，讨论中还提到了一些未来的改进方向，比如进一步优化寄存器的处理逻辑和增强对特性的支持。

总的来说，本周的讨论和补丁提交为 KVM 在 s390 上的 arm64 支持奠定了基础，解决了多个关键的技术问题，并为未来的扩展提供了可能性。

#### 📝 邮件列表

1. **[05-29 17:55]** [PATCH v1 00/26] KVM: arm64 on s390 System Register Handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[05-29 17:55]** [PATCH v1 01/26] KVM: arm64: Extract some feature related changes to kvm_feature.h
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[05-29 17:55]** [PATCH v1 02/26] KVM: arm64: Remove __expand_field_sign_(un)signed
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[05-29 17:55]** [PATCH v1 03/26] KVM: arm64: Generalize get_idreg_field_*()
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[05-29 17:55]** [PATCH v1 04/26] KVM: arm64: Generalize kvm_cmp_feat_*()
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[05-29 17:55]** [PATCH v1 05/26] KVM: arm64: Generalize kvm_has_feat_*
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[05-29 17:55]** [PATCH v1 06/26] KVM: arm64: Remove get_idreg_field_*() and kvm_cmp_feat_*()
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[05-29 17:55]** [PATCH v1 07/26] KVM: arm64: Remove kvm_has_feat_range
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[05-29 17:55]** [PATCH v1 08/26] KVM: arm64: Split up feature sysreg sanitisation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[05-29 17:55]** [PATCH v1 09/26] KVM: arm64: Refactor idreg caching into dedicated structure
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[05-29 17:55]** [PATCH v1 10/26] KVM: arm64: Fix set_oslsr_el1 to write to OSLAR_EL1
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[05-29 17:55]** [PATCH v1 11/26] KVM: arm64: Move definitions from sys_regs.c to sys_regs.h
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[05-29 17:55]** [PATCH v1 12/26] KVM: arm64: Add PVM_ prefix to avoid name collisions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[05-29 17:55]** [PATCH v1 13/26] s390: Introduce read/write ARM sysreg instructions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[05-29 17:55]** [PATCH v1 14/26] s390: Introduce Query Available Arm features
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[05-29 17:55]** [PATCH v1 15/26] s390: Add functions to query arm guest time
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[05-29 17:55]** [PATCH v1 16/26] KVM: s390: arm64: Add sysreg related functions and definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[05-29 17:55]** [PATCH v1 17/26] arm64: Extract cputype definitions.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[05-29 17:55]** [PATCH v1 18/26] arm64: Extract cache definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[05-29 17:55]** [PATCH v1 19/26] KVM: arm64: Share KVM feature detection macros
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[05-29 17:55]** [PATCH v1 20/26] KVM: arm64: Share ID reg handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[05-29 17:55]** [PATCH v1 21/26] KVM: arm64: Share sys-reg handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[05-29 17:55]** [PATCH v1 22/26] KVM: arm64: Refactor core reg handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[05-29 17:55]** [PATCH v1 23/26] KVM: s390: arm64: Implement feature sanitisation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[05-29 17:55]** [PATCH v1 24/26] KVM: s390: arm64: Implement sysreg handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[05-29 17:55]** [PATCH v1 25/26] KVM: s390: arm64: Implement exception injection
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[05-29 17:55]** [PATCH v1 26/26] KVM: s390: arm64: Finalize page fault handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 6: [PATCH v2 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups

**📧 邮件数**: 25 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 28 May 2026 17:54:28 +0100

#### 🤖 AI 总结

本周讨论的主题是关于 ARM64 和 KVM 的 FPSIMD、SVE 和 SME 状态管理代码的清理和优化，主要由 Mark Rutland 提出了一系列补丁（共18个）。这些补丁的目标是简化代码结构，减少重复，提升可维护性和可调试性。

1. **原始补丁内容**：补丁系列主要集中在清理低级的 FPSIMD、SVE 和 SME 状态管理代码，目的是使其更易于维护和扩展，同时提高调试能力。补丁中没有修复任何已知的错误。

2. **历史讨论要点**：之前的讨论强调了当前代码的复杂性和冗余，特别是在处理 SVE 和 SME 状态时，使用了不透明的指针和复杂的调用约定，导致易出错且难以理解。

3. **本周新讨论与进展**：
   - 参与者对补丁进行了审查，Mark Brown 和 Vladimir Murzin 等人给予了积极反馈，确认了补丁的有效性。
   - 具体补丁包括将 SVE 和 SME 的保存/恢复逻辑从汇编代码移至内联 C 代码，以便于更清晰的控制流和更好的内存安全性检测。
   - 移除了不再需要的 `<asm/fpsimdmacros.h>` 文件，简化了整体代码结构。

总体来看，本周的讨论和补丁推进了 ARM64 和 KVM 的状态管理代码的清理工作，提升了代码的可读性和可维护性。

#### 📝 邮件列表

1. **[05-28 17:54]** [PATCH v2 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-28 17:54]** [PATCH v2 01/18] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[05-28 17:54]** [PATCH v2 02/18] KVM: arm64: Don't override FFR save/restore argument
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[05-28 17:54]** [PATCH v2 03/18] KVM: arm64: pkvm: Save host FPMR in host cpu context
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-28 17:54]** [PATCH v2 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[05-28 17:54]** [PATCH v2 05/18] arm64: fpsimd: Fold sve_init_regs() into do_sve_acc()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[05-28 17:54]** [PATCH v2 06/18] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[05-28 17:54]** [PATCH v2 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
9. **[05-28 17:54]** [PATCH v2 08/18] arm64: fpsimd: Use assembler for baseline SME instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[05-28 17:54]** [PATCH v2 09/18] arm64: fpsimd: Move sve_get_vl() and sme_get_vl() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[05-28 17:54]** [PATCH v2 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[05-28 17:54]** [PATCH v2 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
13. **[05-28 17:54]** [PATCH v2 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
14. **[05-28 17:54]** [PATCH v2 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
15. **[05-28 17:54]** [PATCH v2 14/18] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
16. **[05-28 17:54]** [PATCH v2 15/18] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
17. **[05-28 17:54]** [PATCH v2 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
18. **[05-28 17:54]** [PATCH v2 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
19. **[05-28 17:54]** [PATCH v2 18/18] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
20. **[05-28 18:11]** Re: [PATCH v2 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[05-28 18:17]** Re: [PATCH v2 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE
 save/restore
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[05-29 09:41]** Re: [PATCH v2 07/18] arm64: fpsimd: Use assembler for SVE
 instructions
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
23. **[05-29 09:42]** Re: [PATCH v2 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
24. **[05-29 09:43]** Re: [PATCH v2 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
25. **[05-29 09:51]** Re: [PATCH v2 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>

---

### Thread 7: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 29 May 2026 08:43:39 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复共享/取消共享超调用失败时的主机与虚拟机跟踪问题。

**原始补丁内容**：
补丁包含两个部分：第一个补丁修复了在调用 `share_pfn_hyp()` 时，如果超调用失败，未能正确清理跟踪节点的问题；第二个补丁则解决了在调用 `unshare_pfn_hyp()` 时，超调用失败导致主机与虚拟机状态不同步的问题。

**之前讨论要点**：
在历史讨论中，参与者指出了当前实现中存在的潜在问题，尤其是超调用失败时未能进行适当的错误处理，可能导致内存泄漏和状态不一致。尽管这些失败路径在实际中很少出现，但仍需关注。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现和潜在的错误处理上。参与者们讨论了超调用是否真的有失败的可能性，建议在代码中添加注释以提高可读性。此外，Marc Zyngier 提出了一些关于错误处理的原则，强调如果某个操作可能失败，则必须处理失败情况；如果不应该失败，则应触发系统崩溃。最终，讨论达成共识，认为补丁的修改是合理的，并且在未来的版本中可以进一步完善错误处理机制。

#### 📝 邮件列表

1. **[05-29 08:43]** [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: tabba@google.com
2. **[05-29 08:43]** [PATCH 1/2] KVM: arm64: Free hyp-share tracking node when share
 hypercall fails
   - 发件人: tabba@google.com
3. **[05-29 08:43]** [PATCH 2/2] KVM: arm64: Avoid host/hyp share desync on unshare
 hypercall failure
   - 发件人: tabba@google.com
4. **[05-29 09:02]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[05-29 09:05]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[05-29 09:15]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare hypercall failure
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-29 09:20]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[05-29 10:21]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[05-29 10:23]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[05-29 10:29]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare hypercall failure
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[05-29 11:06]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[05-29 11:07]** Re: [PATCH 0/2] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 8: [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 9 | **👥 参与者**: 4 | **📅 开始时间**: Thu, 21 May 2026 14:49:07 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 ARM64 架构添加 GICv5 IRS 支持的补丁（PATCH v2 00/39）。该补丁旨在扩展 GICv5 的功能，使其支持共享中断（SPIs）和本地中断（LPIs），从而允许在 Arm FVP 模型上启动完整的 Linux 客户机。

在历史讨论中，Sascha Bischoff 提出了多个补丁，主要集中在如何在 ACPI 主机上正确设置 GICv5 的 KVM 信息，以及支持 SPI 注入的实现。这些补丁旨在解决 KVM 在不同系统架构下对 GICv5 的支持问题。

本周的新讨论中，参与者们针对补丁的具体实现进行了深入交流。Vladimir Murzin 提到一个编译错误，并建议对代码进行修正。Marc Zyngier 和 Lorenzo Pieralisi 则讨论了在 ACPI 主机上设置 GICv5 信息时的一些细节，特别是关于如何处理 GSI 编码和维护中断的逻辑。Sascha 对这些反馈做出了积极响应，承诺将进行必要的修改，并考虑未来的代码清理机会。

总体来看，本周的讨论主要集中在补丁的细节修正和优化上，参与者们积极协作，推动补丁的完善与实施。

#### 📝 邮件列表

1. **[05-21 14:49]** [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[05-21 14:50]** [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[05-21 14:59]** [PATCH v2 29/39] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[05-26 14:41]** Re: [PATCH v2 29/39] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>
5. **[05-27 11:51]** Re: [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-28 09:14]** Re: [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
7. **[05-28 14:59]** Re: [PATCH v2 29/39] KVM: arm64: gic-v5: Support SPI injection
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[05-29 14:33]** Re: [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[05-29 14:41]** Re: [PATCH v2 03/39] irqchip/gic-v5: Setup gic_kvm_info on ACPI hosts
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 9: [PATCH v6 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 27 May 2026 15:02:30 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）中 Endpoint Memory Access Descriptor（EMAD）偏移量计算的问题。此次讨论包含六个补丁，旨在解决与 FF-A 版本 1.1 相关的偏移计算错误，并增强内核的安全性和稳定性。

历史讨论中，之前的补丁未能正确处理 EMAD 的偏移量，导致在 FF-A 版本 1.1 之前，内存区域头部未明确指定 EMAD 的偏移量，造成假设 EMAD 紧随其后。此次补丁系列通过更新 `arm_ffa` 驱动和 pKVM 超级管理程序的验证逻辑，确保偏移量计算符合 FF-A 规范，并添加必要的边界检查。

在本周的新讨论中，Mostafa Saleh 提出了六个补丁，具体包括：
1. 在 `optee` 中添加 NULL 检查以防止空指针解引用。
2. 修复 `ffa_setup_and_transmit` 函数中的越界写入问题。
3. 更新 EMAD 偏移量计算逻辑，确保符合 FF-A 规范。
4. 修复 KVM 中的边界检查，防止越界访问。
5. 验证内存访问描述符的偏移量，确保其在邮箱缓冲区范围内。
6. 确保 FFA 范围的页面对齐。

这些补丁不仅修复了已知的错误，还提高了系统的安全性。参与者对补丁进行了审查并表示支持，确保了补丁的质量和有效性。

#### 📝 邮件列表

1. **[05-27 15:02]** [PATCH v6 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-27 15:02]** [PATCH v6 1/6] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-27 15:02]** [PATCH v6 2/6] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-27 15:02]** [PATCH v6 3/6] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-27 15:02]** [PATCH v6 4/6] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-27 15:02]** [PATCH v6 5/6] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[05-27 15:02]** [PATCH v6 6/6] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[05-28 00:25]** Re: [PATCH v6 1/6] optee: ffa: Add NULL check in
 optee_ffa_lend_protmem
   - 发件人: Sumit Garg <sumit.garg@kernel.org>

---

### Thread 10: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 11 May 2026 11:32:56 +0100

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于一个针对 ARM64 架构的补丁（PATCH v10 04/30），该补丁旨在确定最大可虚拟化的 SME 向量长度。历史讨论中，参与者 Mark Rutland 提到了一些关于补丁的细节，特别是对使用 (SME_VQ_MAX + 1) 的疑虑，认为使用 0 更加清晰，并且讨论了如何处理虚拟化的向量长度（VL）检查。

在本周的新讨论中，Mark Rutland 提出了更具体的算法建议，建议使用 `find_virtualisable_vl` 函数来查找可虚拟化的 VL，并详细描述了如何处理相关的位图和检查逻辑。此外，他还讨论了如何简化 SMCR 和 ZCR 的存储方式，提议将完整的 SMCR 值存储在任务结构中，而不是使用多个布尔值来表示状态，以提高代码的可读性和一致性。

总体而言，本周的讨论集中在如何优化补丁的实现细节和提高代码的可维护性上，参与者们对补丁的逻辑和结构进行了深入的探讨，提出了具体的改进建议。

#### 📝 邮件列表

1. **[05-11 11:32]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-11 21:42]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[05-26 13:48]** Re: [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[05-26 13:53]** Re: [PATCH v10 03/30] arm64/fpsimd: Decide to save ZT0 and streaming
 mode FFR at bind time
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-26 13:55]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[05-26 14:25]** Re: [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[05-26 15:20]** Re: [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[05-26 16:19]** Re: [PATCH v10 02/30] arm64/fpsimd: Update FA64 and ZT0 enables when
 loading SME state
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 11: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Sat, 16 May 2026 19:29:54 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的嵌套虚拟机（L2）支持的自测试（selftests）补丁系列。

1. **原始补丁内容**：Wei-Lin Chang 提出了一个补丁系列（v3），旨在为 KVM 添加基本的嵌套虚拟机支持，特别是通过自测试框架启用 L2 的阶段 2（stage-2）功能。补丁中包括了 s2_mmu 结构、s2 转换控制设置以及阶段 2 页表生成器。此外，还增加了一个名为 shadow_stage2 的测试，以验证 KVM 的影子页表管理代码。

2. **之前讨论要点**：在历史讨论中，Oliver Upton 提到需要确保 L2 的阶段 1 MMU 被启用，以保证原子操作的正常工作，并探讨了是否可以重用 L1 的现有阶段 1 表。这一讨论为后续补丁的设计提供了重要背景。

3. **本周的新讨论与进展**：本周的讨论中，Itaru Kitayama 提出了一个补丁，重构了 shadow_stage2 测试，使其能够使用不同的来宾模式。Wei-Lin Chang 表示赞同，并愿意将此补丁纳入下一个版本。同时，Wei-Lin 还回应了关于 L1 和 L2 表重用的讨论，强调重用 L1 表可以简化测试过程，但也可能影响测试的复杂性。整体来看，本周的讨论推动了补丁的进一步完善和测试的多样化。

#### 📝 邮件列表

1. **[05-16 19:29]** [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-16 19:29]** [PATCH v3 5/9] KVM: arm64: selftests: Add shadow_stage2 test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[05-19 14:31]** Re: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[05-28 13:59]** [PATCH] KVM: selftest: arm64: Run shadow_stage2 varying guest modes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
5. **[05-28 17:02]** Re: [PATCH] KVM: selftest: arm64: Run shadow_stage2 varying guest
 modes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[05-29 07:14]** Re: [PATCH] KVM: selftest: arm64: Run shadow_stage2 varying guest
 modes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
7. **[05-29 14:38]** Re: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 12: [PATCH v5 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 7 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 26 May 2026 15:19:28 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）中 Endpoint Memory Access Descriptor（EMAD）偏移量计算的修复，主要通过一系列补丁（patch）来解决相关问题。

**原始问题**：在 FF-A 版本 1.1 之前，内存区域头部并未明确指定 EMAD 的偏移量，导致假设其紧随头部之后。此后，规范要求使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。

**历史讨论要点**：之前的讨论集中在如何修复内核中由于偏移计算不准确而导致的潜在内存访问错误。补丁系列旨在更新 `arm_ffa` 驱动程序和 pKVM 超级管理程序的验证逻辑，以确保它们遵循 FF-A 规范并进行必要的边界检查。

**本周新讨论与进展**：本周的讨论主要围绕补丁的具体实现，参与者 Mostafa Saleh 和 Sebastian Ene 提出了多个补丁，修复了 EMAD 偏移计算、边界检查和内存访问的相关问题。补丁包括：
1. 修复 `ffa_setup_and_transmit` 函数中的越界写入问题。
2. 更新 `arm_ffa` 驱动程序以正确计算描述符偏移。
3. 强化 pKVM 超级管理程序的验证逻辑，确保 EMAD 偏移在邮箱缓冲区范围内。
4. 确保 FFA 范围的页对齐。

这些补丁的实施将提高系统的稳定性和安全性，确保遵循最新的 FF-A 规范。

#### 📝 邮件列表

1. **[05-26 15:19]** [PATCH v5 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-26 15:19]** [PATCH v5 1/6] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-26 15:19]** [PATCH v5 2/6] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-26 15:19]** [PATCH v5 3/6] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-26 15:19]** [PATCH v5 4/6] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-26 15:19]** [PATCH v5 5/6] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[05-26 15:19]** [PATCH v5 6/6] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 13: [PATCH v2 0/3] Fixes for hyp_trace.c

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 21 May 2026 13:46:10 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 `hyp_trace.c` 的一系列修复补丁（PATCH v2 0/3），主要集中在 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的共享和取消共享操作中的错误处理。

**原始补丁内容**：
补丁主要修复了在 `hyp_trace_buffer_share_hyp()` 中的回滚问题和 `hyp_trace_unload()` 中的内存泄漏。Vincent Donnefort 提到在 v1 版本的审查中发现了一些错误路径和内存泄漏问题。

**之前讨论要点**：
在历史讨论中，Vincent 提到的补丁 v1 版本中存在的问题包括错误处理不当导致的内存泄漏，以及在共享和取消共享操作失败时未能正确清理资源。补丁 v2 版本对此进行了修正。

**本周的新讨论与进展**：
本周的讨论中，Marc Zyngier 确认已将补丁应用到修复列表中。Fuad Tabba 提出了新的补丁，解决了在共享和取消共享操作中可能出现的状态不一致问题，包括：
1. 在 `share_pfn_hyp()` 中处理超调用失败时的节点清理。
2. 在 `unshare_pfn_hyp()` 中确保在调用超调用前不删除跟踪节点。
3. 在 `kvm_share_hyp()` 中实现部分共享失败时的回滚机制。

这些补丁确保了即使在操作失败时，系统的隔离性不会受到影响，且补丁的严重性被评估为较低，可以等待下一个版本发布。

#### 📝 邮件列表

1. **[05-21 13:46]** [PATCH v2 0/3] Fixes for hyp_trace.c
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-27 14:13]** Re: [PATCH v2 0/3] Fixes for hyp_trace.c
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-29 13:17]** [PATCH v2 0/3] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: tabba@google.com
4. **[05-29 13:17]** [PATCH v2 1/3] KVM: arm64: Free hyp-share tracking node when share
 hypercall fails
   - 发件人: tabba@google.com
5. **[05-29 13:17]** [PATCH v2 2/3] KVM: arm64: Avoid host/hyp share desync on unshare
 hypercall failure
   - 发件人: tabba@google.com
6. **[05-29 13:17]** [PATCH v2 3/3] KVM: arm64: Roll back partial shares on
 kvm_share_hyp() failure
   - 发件人: tabba@google.com

---

### Thread 14: [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a platform as a probe miss

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 26 May 2026 11:36:49 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），其内容为“firmware: arm_ffa: 将平台上缺失的 FF-A 特性视为探测失败”。该补丁旨在解决在某些平台上，FF-A 初始化时如果未实现 FF-A 特性，系统会返回 -EOPNOTSUPP 错误，导致驱动核心将其视为探测失败并输出错误信息。补丁的修改是将早期不支持的发现情况转换为 -ENODEV，以减少噪音，同时保留实际 FF-A 初始化问题的报告。

在之前的讨论中，补丁的必要性得到了确认，参与者指出当前的错误处理方式会对有效系统造成误报。

在本周的新讨论中，补丁得到了积极反馈。参与者 Yeoreum Yun 和 Nathan Chancellor 分别表示补丁看起来很好，并进行了测试，确认其有效性。Sudeep Holla 随后表示感谢并确认已将该补丁应用到其代码库中。这表明该补丁已获得认可并准备合并。

#### 📝 邮件列表

1. **[05-26 11:36]** [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a platform as a probe miss
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
2. **[05-26 11:51]** Re: [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a
 platform as a probe miss
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[05-26 12:35]** Re: [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a
 platform as a probe miss
   - 发件人: Nathan Chancellor <nathan@kernel.org>
4. **[05-27 10:09]** Re: [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a
 platform as a probe miss
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
5. **[05-27 10:16]** Re: [PATCH] firmware: arm_ffa: Treat missing FF-A feature on a platform as a probe miss
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 15: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 22 May 2026 19:00:04 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中如何处理 ZCR_EL2.LEN 寄存器值的保存问题。历史讨论中，Mark Brown 提出了一个补丁，旨在确保在处理 ZCR_EL2 时，所有写入的值都能被准确保存，而不是被限制为最大向量长度。这一行为与架构文档的预期不符，因此需要进行修正。

在本周的新讨论中，Mark Rutland 对补丁的必要性提出了质疑，并询问是否已向架构师寻求反馈。他指出，当前的行为似乎没有明确的架构依据，可能需要进一步澄清。Mark Brown 也表示，现有文档对于 ZCR_EL2.LEN 和 SMCR_ELx.LEN 的值是否被视为保留值并不清晰，可能导致不同的解读。他强调，必须明确这些值的处理方式，以避免潜在的误解。

总体来看，本周的讨论集中在对补丁的必要性和架构文档的澄清需求上，参与者们一致认为需要进一步与架构师沟通，以确保对 ZCR_EL2.LEN 值的处理符合架构要求。

#### 📝 邮件列表

1. **[05-22 19:00]** [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[05-25 19:36]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[05-26 11:19]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[05-26 13:03]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-26 14:03]** Re: [PATCH] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 16: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 20 May 2026 16:31:12 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现嵌套的 stage-2 反向映射的补丁（PATCH v3 0/5）。该补丁旨在解决 16KB 页大小下内核无法处理 stage-2 解除映射路径的问题。

在历史讨论中，Itaru Kitayama 提到应用该补丁后，测试结果显示在所有三种页面粒度下均能正常运行。然而，他对补丁的测试方法表示疑问，并提到在没有补丁的情况下，16KB 页的解除映射似乎存在问题。

本周的新讨论中，Marc Zyngier 对 Itaru 的表述提出了疑问，认为如果 16KB 的 S2 解除映射在主线版本中无法工作，这将影响到大量开发硬件的使用。他对补丁中的一些命名和逻辑提出了多项建议，包括对变量命名的清晰度、对对齐问题的检查以及对 VALID_ENTRY 的验证等。此外，他还建议将 VNCR 无效化的处理与 S2 操作分开，以便更好地管理。

Itaru 在最后的回复中确认了在使用最新的 kvmarm/fixes 版本和 16KB 粒度进行测试时，stage-2 解除映射路径未能完成，表示可能与所用的 Ubuntu 用户空间有关，但仍需进一步确认。整体来看，讨论集中在补丁的有效性及其潜在问题上，参与者对补丁的细节和实现提出了建设性的反馈。

#### 📝 邮件列表

1. **[05-20 16:31]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
2. **[05-28 11:19]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-28 13:59]** Re: [PATCH v3 3/5] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-29 09:55]** Re: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>

---

### Thread 17: [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 29 May 2026 00:01:44 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对 ZCR_EL2.LEN 值的处理，主要涉及一个补丁（patch）及其相关问题。

1. **原始 patch/问题的内容**：Mark Brown 提出的补丁旨在修复 KVM 在处理 ZCR_EL2 时的行为，确保所有来自虚拟机的 ZCR_EL2.LEN 值能够被正确保存和使用。当前实现中，当虚拟机写入 ZCR_EL2 时，ZCR_EL2.LEN 的值被限制为最大向量长度（VL），这与架构文档的预期行为不符。

2. **之前的讨论要点**：补丁的背景是基于之前的讨论，指出现有的实现可能导致虚拟机访问超出其配置的向量长度。Marc Zyngier 强调，当前的处理方式并未合理限制虚拟机的访问权限，可能导致不符合预期的行为。

3. **本周的新讨论、进展或结论**：本周的讨论中，Marc Zyngier 对补丁的描述进行了重写，使其更清晰地阐述了问题的核心，即确保虚拟机无法访问超出配置的向量长度。Joey Gouly 对补丁进行了审核并表示支持。补丁经过修改后，确保了在不同访问器（ZCR_EL2 和 ZCR_EL1）下，ZCR_EL2.LEN 字段始终保持状态一致性，并且在恢复 SVE（Scalable Vector Extension）上下文时，硬件总是使用经过限制的值。

总体而言，本次讨论集中在确保 KVM 对 ZCR_EL2 的处理符合架构规范，避免虚拟机访问不应有的资源。

#### 📝 邮件列表

1. **[05-29 00:01]** [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[05-29 10:22]** Re: [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-29 10:46]** Re: [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 18: [PATCH v2 4/4] KVM: arm64: Fallback to a supported value for unsupported guest TGx

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 28 May 2026 09:51:46 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下处理不支持的访客翻译粒度（TGx）的补丁（patch）。该补丁的主要目的是在遇到不支持的 TGx 时，回退到一个支持的值，以确保系统的稳定性和兼容性。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁是系列补丁中的一部分，旨在改善对不同 TGx 的支持。之前的讨论可能集中在如何处理不同的 TGx 以及相关的代码重构上。

在本周的新讨论中，Marc Zyngier 对补丁提出了一些小的改进意见，包括代码可读性和注释的准确性。他指出某些代码逻辑可能会导致误解，并建议将长语句移至声明块的顶部以提高可读性。最终，Marc Zyngier 表示已将补丁应用到下一个版本中，并感谢 Wei-Lin Chang 对小问题的修正。

综上所述，本周的讨论主要集中在补丁的细节改进上，最终达成了将补丁应用于后续版本的共识。

#### 📝 邮件列表

1. **[05-28 09:51]** Re: [PATCH v2 4/4] KVM: arm64: Fallback to a supported value for unsupported guest TGx
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-28 10:24]** Re: [PATCH v2 0/4] KVM: arm64: Handle unsupported guest translation granule sizes
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-28 10:55]** Re: [PATCH v2 0/4] KVM: arm64: Handle unsupported guest translation
 granule sizes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 19: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 18 May 2026 16:31:26 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（内核虚拟机）在 ARM64 架构下的补丁，主题为「[PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()」。该补丁的主要内容是建议在 `__finalise_el2()` 函数中不再配置 `TPIDR_EL2` 寄存器，原因包括：当前的 hyp stub 代码并不使用 `TPIDR_EL2` 的值；在启动 CPU 时，`TPIDR_EL1` 被用于每个 CPU 的偏移量，直到检测到 `ARM64_HAS_VIRT_HOST_EXTN` 的 CPU 特性并对启动替代方案进行补丁；在补丁之前，`cpu_copy_el2regs()` 函数会将 `TPIDR_EL1` 的值复制到 `TPIDR_EL2`，因此在此函数中初始化 `TPIDR_EL2` 是不必要的。

在本周的新讨论中，Marc Zyngier 回复表示已将该补丁应用到下一个版本中，并感谢 Will Deacon 的贡献。这表明该补丁得到了认可并将继续推进。整体来看，本周的进展是补丁的成功应用，标志着讨论的积极结果。

#### 📝 邮件列表

1. **[05-18 16:31]** [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Will Deacon <will@kernel.org>
2. **[05-27 15:32]** Re: [PATCH v2] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 20: [PATCH] KVM: arm64: PMU: Preserve AArch32 counter low bits

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 26 May 2026 15:46:40 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构下的性能监控单元（PMU）相关的补丁，主要目的是修复 AArch32 计数器低位的保存问题。

原始补丁的内容是针对 AArch32 写入 PMU 事件计数器时，无法更新高32位的问题。补丁提出，KVM 应该保留现有的高32位，仅更新由虚拟机提供的低32位，除非调用者明确要求通过 PMCR.P 进行完全重置。当前代码在处理时会将值掩码到旧的高32位，导致低32位总是为零，从而丢弃了虚拟机提供的低32位数据。补丁通过构建新值来解决这一问题，即结合旧的高32位和虚拟机提供的低32位。

在之前的讨论中，补丁的背景是基于之前的提交（26d2d0594d70），该提交未能正确处理 AArch32 对计数器高32位的修改。

本周的新讨论中，Qiang Ma 提交了补丁，Marc Zyngier 随后确认已将该补丁应用于修复，并表示感谢。这表明该补丁得到了认可并已被纳入代码库中。

#### 📝 邮件列表

1. **[05-26 15:46]** [PATCH] KVM: arm64: PMU: Preserve AArch32 counter low bits
   - 发件人: Qiang Ma <maqianga@uniontech.com>
2. **[05-27 11:35]** Re: [PATCH] KVM: arm64: PMU: Preserve AArch32 counter low bits
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 21: [PATCH] KVM: arm64: Fix CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 20 May 2026 23:08:30 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，旨在修复 CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC 的问题。

1. **原始 patch/问题的内容**：Vincent Donnefort 提出了一个补丁，修复了在 __hyp_do_panic 函数中的一个拼写错误，该错误导致 stage-2 禁用功能失效，使得 pKVM 的回溯信息不可靠。补丁的目标是确保在系统发生 panic 时，能够正确禁用 stage-2。

2. **之前的讨论要点**：在历史讨论中，Vincent 详细描述了问题的根源，并提供了补丁的代码修改部分，指出该问题是由于之前的提交（9019e82c7e46）引入的拼写错误。

3. **本周的新讨论、进展或结论**：在本周的讨论中，Marc Zyngier 确认已将该补丁应用于修复，并表示感谢。这表明补丁已被接受并整合到代码库中，解决了之前讨论的问题。

总体而言，该邮件线程清晰地记录了一个重要的修复过程，从问题的识别到补丁的应用，展示了开发者之间的有效沟通与合作。

#### 📝 邮件列表

1. **[05-20 23:08]** [PATCH] KVM: arm64: Fix CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-27 11:35]** Re: [PATCH] KVM: arm64: Fix CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 22: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 22 May 2026 17:11:48 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），其内容为将 `arm_ffa` 注册为一个平台驱动。该补丁在 2026 年 5 月 8 日被提交，并在随后的开发版本中引发了一些问题。

在历史讨论中，Nathan Chancellor 报告说，在应用该补丁后，他的两台 arm64 测试机器出现了错误信息：“arm-ffa: probe with driver arm-ffa failed with error -95”。他询问这是否是预期行为，并建议可能需要对该错误信息进行静默处理。

在本周的新讨论中，Sudeep Holla 回复了 Nathan 的邮件，确认这个错误信息确实应该被静默处理，并表示他会研究如何实现这一点。此次讨论表明，开发者们正在积极解决补丁引发的问题，以提高系统的稳定性。

#### 📝 邮件列表

1. **[05-22 17:11]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Nathan Chancellor <nathan@kernel.org>
2. **[05-26 10:41]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 23: [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM guests

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 31 May 2026 16:45:48 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在解决 pKVM（paravirtualized KVM）环境中虚拟 SError（系统错误）未能正确传递给虚拟 CPU 的问题。

原始补丁的内容是修改 `flush_hyp_vcpu()` 函数，以确保 HCR_EL2.VSE（虚拟 SError 控制位）能够在主机注入时正确传递给 hyp vCPU。补丁指出，当前的实现仅将 TWI/TWE（触发中断和异常）流向运行的 hyp vCPU，导致 VSE 无法到达，进而未能交付已延迟的 SError。补丁通过在 HCR_EL2 中添加 VSE 的处理，确保其能够在 vCPU 进入时被正确同步。

在之前的讨论中，补丁的背景是基于一个已知问题，即在 pKVM 启用的情况下，主机无法有效地将虚拟 SError 注入到虚拟机中。补丁的修复旨在解决这一问题，并且是基于之前的提交（b56680de9c648）进行的。

本周的新讨论中，补丁的作者 Fuad Tabba 提到这并不是一个紧急修复，并表示应该停止运行 Sashiko（可能是指某种测试或环境）。补丁已在代码中实现了相关修改，增加了对 HCR_EL2.VSE 的处理，以确保虚拟 SError 能够被正确交付。

#### 📝 邮件列表

1. **[05-31 16:45]** [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM guests
   - 发件人: tabba@google.com

---

### Thread 24: [PATCH 09/17] KVM: arm64: Move VMA-related information to
 kvm_s2_fault_vma_info

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 30 May 2026 01:27:11 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，具体内容是将与虚拟内存区域（VMA）相关的信息移动到 `kvm_s2_fault_vma_info` 中。

在历史讨论中，虽然没有具体的补丁内容被提及，但可以推测该补丁旨在优化 KVM 在处理虚拟内存时的信息管理。

本周的新讨论中，参与者 Wei-Lin Chang 针对补丁提出了一个问题，询问在启用脏页日志记录的情况下，映射大小被限制为页面大小（PAGE_SIZE），并且透明大页（THP）调整不会发生的情况下，为什么仍然需要将规范的 IPA（Intermediate Physical Address）向下对齐。这个问题表明他对补丁的某些实现细节感到困惑，期待进一步的解释和澄清。

总结而言，本周的讨论主要集中在补丁实现的合理性和必要性上，特别是在特定条件下的行为。

#### 📝 邮件列表

1. **[05-30 01:27]** Re: [PATCH 09/17] KVM: arm64: Move VMA-related information to
 kvm_s2_fault_vma_info
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 25: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 29 May 2026 16:32:24 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中将 FFA_NOTIFICATION* 调用转发到 TrustZone 的补丁（patch）。该补丁旨在增强虚拟化环境中对 TrustZone 的支持。

在历史讨论中，尚未有具体的补丁或深入的讨论记录，因此本周的新讨论成为了主要内容。参与者 Sebastian Ene 提出了将每个调用结构化为单独的补丁的建议，以便在提交信息中详细说明每个调用特定的保留字段。同时，他强调了在处理 SBZ（保留位必须为零）和 MBZ（保留位必须为零）参数时的重要性，认为在寄存器级别进行检查过于粗糙。

Will Deacon 进一步支持这种观点，指出 FFA_NOTIFICATION_BITMAP_CREATE 调用中的 VM ID 参数的某些位是 MBZ，因此需要在每个函数的基础上进行检查，而不是仅依赖于寄存器级别的检查。他还提到了 Per 的系列补丁，作为实现这一目标的参考。

总的来说，本周的讨论集中在如何更细致地处理 FFA_NOTIFICATION 调用的参数检查上，并提出了将补丁拆分为多个部分的建议，以提高代码的可维护性和清晰度。

#### 📝 邮件列表

1. **[05-29 16:32]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 26: [PATCH] KVM: arm64: Remove @arch from __load_stage2()

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 28 May 2026 18:56:36 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，具体内容是移除 `__load_stage2()` 函数中的 `@arch` 参数。

在历史讨论中，未提供具体的背景信息，因此我们无法得知该补丁的详细原因或之前的讨论要点。

在本周的新讨论中，Marc Zyngier 提到该补丁已被应用到下一步的开发中，并感谢 Zenghui Yu 的贡献。补丁的提交信息为 `commit: e72b425f617edebf6f374fa39f2c763c9b3696ec`，表明该修改已正式纳入代码库。

总结来说，本周的讨论主要集中在确认补丁的应用上，未涉及其他新的问题或反馈。

#### 📝 邮件列表

1. **[05-28 18:56]** Re: [PATCH] KVM: arm64: Remove @arch from __load_stage2()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH v4 5/6] arm64/boot: Enable EL2 requirements for
 FEAT_Debugv8p9

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 28 May 2026 11:58:05 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM64 架构的补丁（PATCH v4 5/6），其目的是启用 EL2 对 FEAT_Debugv8p9 的要求。该补丁的具体内容尚未在邮件中详细列出，但其核心是与 ARM64 启动过程中的调试功能相关。

在之前的讨论中，虽然没有提供具体的历史邮件内容，但可以推测，参与者可能讨论了该补丁的必要性及其对现有系统配置的影响。特别是，补丁可能涉及对 ID 寄存器的检查，以及如何处理之前配置的陷阱设置。

在本周的新讨论中，Will Deacon 对补丁提出了质疑，询问为什么需要在此处检查 ID 寄存器，并指出该补丁可能会影响之前块的陷阱配置。这表明在补丁的实现过程中，存在对其潜在影响的关注，参与者对补丁的设计和实现细节提出了进一步的审查和讨论。

总结而言，本周的讨论集中在补丁的必要性和潜在影响上，反映出对 ARM64 启动过程中的调试功能实现的深入探讨。

#### 📝 邮件列表

1. **[05-28 11:58]** Re: [PATCH v4 5/6] arm64/boot: Enable EL2 requirements for
 FEAT_Debugv8p9
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 28: (subset) [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error propagation fixes

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 27 May 2026 14:35:46 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error propagation fixes”，涉及对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 EL2 同步和 pKVM 阶段二错误传播的修复。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁系列旨在解决在虚拟化环境中可能出现的同步和错误处理问题，以提高系统的稳定性和可靠性。

在本周的新讨论中，Marc Zyngier 对该补丁系列表示感谢，并确认已经将其应用到下一个开发版本中。补丁包括多个具体的修复和改进，例如：
- 防止在 VHE（Virtual Host Extensions）高优先级路径中出现 NULL vcpu 的情况。
- 修正了 __deactivate_fgt 宏参数的拼写错误。
- 为 pKVM 所有权自测的 vcpu 内存缓存进行了初始化。
- 对 vcpu 内存缓存进行主机与客户机共享和捐赠的预检查。

这些进展表明，补丁系列已获得认可并顺利推进，预计将增强 KVM 在 arm64 平台上的性能和可靠性。

#### 📝 邮件列表

1. **[05-27 14:35]** Re: (subset) [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error propagation fixes
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 29: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 26 May 2026 17:27:52 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于“guest_memfd”的直接映射移除支持的补丁（PATCH v12 00/16）。该补丁旨在改进虚拟化环境中内存管理的效率，具体内容尚未详细说明。

在历史讨论部分，没有提供相关的背景信息或之前的讨论内容，因此我们无法了解该补丁的详细背景或之前的争议。

本周的新讨论中，参与者Lorenzo Stoakes对补丁的进展表示感谢，并特别提到Nikitas的工作，表示会关注后续的版本更新。这表明该补丁在开发过程中得到了积极的反馈，并且参与者对未来的改进持乐观态度。

总体来看，本周的讨论主要是对补丁开发者工作的认可，并未涉及具体的技术细节或问题。

#### 📝 邮件列表

1. **[05-26 17:27]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Lorenzo Stoakes <ljs@kernel.org>

---

## 📌 RFC

共 3 个 thread

---

### Thread 1: [RFC PATCH 0/2] Optimize S2 page splitting

**📧 邮件数**: 15 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 15 May 2026 20:59:01 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于优化 S2 页分裂的补丁（RFC PATCH 0/2），主要由 Leonardo Bras 提出。补丁的核心内容是通过引入新的返回值来优化页表遍历，减少不必要的遍历步骤，从而提高性能。具体来说，补丁引入了 SKIP_CHILDREN 和 SKIP_SIBLINGS 返回值，以便在遍历时跳过某些节点。

在历史讨论中，参与者对补丁的有效性和方法提出了不同的看法。Marc Zyngier 指出，基于软件模型的性能测量并不可靠，建议在实际硬件上进行测试。Oliver Upton 和 Will Deacon 提出了使用新的遍历标志来替代返回值的建议，以简化逻辑并提高性能。

在本周的新讨论中，Leonardo Bras 汇报了在实际硬件（AmpereOne）上进行的测试结果，显示使用标志跳过整个层级的方案比使用返回值的方案更有效。测试结果表明，跳过层级的方案在不同页面大小下均有显著的性能提升，而跳过子节点的方案则导致了约1%的性能下降。基于这些结果，Leonardo 计划移除跳过子节点的补丁，并准备发送新的版本（v2），以进一步优化补丁的实现。参与者们对测试结果表示认可，并建议提供详细的测试参数和分析，以便其他人能够复现这些结果。

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
7. **[05-19 13:43]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Will Deacon <will@kernel.org>
8. **[05-19 13:56]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[05-19 14:15]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Will Deacon <will@kernel.org>
10. **[05-19 15:35]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[05-19 14:21]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return
 options
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[05-28 17:03]** Re: [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[05-28 18:00]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[05-29 13:25]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[05-29 13:56]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 2: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 13 May 2026 16:33:43 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 KVM 的命名 CPU 模型的 RFC 补丁（[RFC PATCH v1 00/13]），该补丁旨在为 KVM 客户机提供命名的 CPU 模型，以支持跨主机的实时迁移和对客户机特性的管理。

在历史讨论中，参与者们探讨了命名 CPU 模型的设计理念，特别是如何将 ARM64 的特性与 QEMU 的实现相结合。讨论中提到，虽然特性值是从内核中提取的，但用户在使用时可能会面临缺乏文档支持的问题，因此建议提供参考文档来帮助用户理解支持的特性及其含义。

在本周的新讨论中，Eric Auger 和 Khushit Shah 进一步探讨了补丁的实现细节，特别是如何在命名模型中设置 ID 寄存器的默认值和安全规则。Khushit 提出了在 v2 版本中引入新的 QMP 命令（如 `query-props-info`），以便更好地展示主机支持的属性值和不可用特性，从而帮助分层产品理解哪些模型可以在特定主机上实现。Eric 也表示对这些改进的认可，并强调需要对不可用特性进行详细文档说明。

总体而言，本周的讨论集中在补丁的细节完善和未来版本的规划上，显示出社区对该功能的积极反馈和进一步发展的期待。

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
6. **[05-27 15:18]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-28 06:19]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
8. **[05-28 11:36]** Re: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 3: [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback and
 IDE stream allocation support

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 27 May 2026 22:47:29 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为“coco: host: arm64: 添加主机 TSM 回调和 IDE 流分配支持”的 RFC PATCH（版本4的第1个补丁）。该补丁的主要目的是为 PCI-TSM 提供基础设施和框架支持，后续将会有关于 IDE 密钥管理的更详细实现。

在之前的讨论中，参与者 Dan Williams 提出了对该补丁的反馈，强调这是一个基础性补丁，主要处理 PCI-TSM 的骨架部分，后续的具体实现（如 IDE 密钥管理）将在后续补丁中提供。他建议补丁的结构可以进行调整，以便使其在与基础 CCA 系列的关系上更加独立。此外，他询问了补丁的合并策略，以及是否需要额外的帮助。

在本周的新讨论中，Dan Williams 对补丁的具体实现提出了一些小的建议和问题，包括设备是否需要 IDE 的判断、流 ID 的唯一性要求，以及在补丁中如何处理安全声明等。他还提到，在补丁的最终实现中，应该考虑到如何处理可能的错误情况，以确保代码的健壮性。

总体来看，本周的讨论主要集中在补丁的细节和后续实现的策略上，参与者对补丁的方向表示认可，但也提出了需要进一步澄清和优化的地方。

#### 📝 邮件列表

1. **[05-27 22:47]** Re: [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback and
 IDE stream allocation support
   - 发件人: Dan Williams (nvidia) <djbw@kernel.org>

---

## 📌 Bug Report

共 1 个 thread

---

### Thread 1: [RESEND v3 0/3] Fix __pkvm_init_vm error path

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 21 May 2026 15:36:23 +0100

#### 🤖 AI 总结

本邮件线程讨论了修复 `__pkvm_init_vm` 函数错误路径的问题，主要由 Vincent Donnefort 提出并提交了相关的补丁（patch）。

在历史讨论中，Vincent Donnefort 指出 Sashiko 报告了在 `insert_vm_table_entry` 失败时可能出现的引用计数泄漏问题。为了解决这个问题，他在补丁中添加了一个安全措施，以确保 `__pkvm_hyp_donate_host` 函数不会导致引用计数页面的泄漏。此外，他还对补丁进行了多次修改，确保外部页面的顺序为 order-0，并使 vmemmap 的 order 字段完全私有于 hyp_pool。

在本周的新讨论中，Marc Zyngier 确认已将这些补丁应用到下一个版本中，并列出了三个具体的提交：重置 pKVM hyp_pool 中的页面顺序、修复 `__pkvm_init_vm` 的错误路径，以及为 `__pkvm_hyp_donate_host` 中的引用计数页面添加安全措施。这表明该问题得到了积极的响应和解决。

#### 📝 邮件列表

1. **[05-21 15:36]** [RESEND v3 0/3] Fix __pkvm_init_vm error path
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-27 14:38]** Re: [RESEND v3 0/3] Fix __pkvm_init_vm error path
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #4

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 29 May 2026 11:54:05 +0100

#### 🤖 AI 总结

本邮件讨论主题为 KVM/arm64 在 7.1 版本中的修复，Marc Zyngier 提交了最新的修复补丁，标记为“take #4”。此次补丁主要解决了几个问题，包括新引入的追踪代码中的内存泄漏、一个配置符号拼写错误导致的永久禁用、PMU 模拟中的一个严重错误（允许写入任何值，只要是零），以及嵌套虚拟化中的 SVE 清理错误，导致来宾能够访问超出其权限的资源。

在之前的讨论中，Marc 提到他有意避免提交更多较小的问题修复，以免引起过多关注，表示这些问题将在 7.2 的拉取请求中处理。

本周的进展是，Marc 提交的补丁已被 Paolo Bonzini 接收并确认拉取，表明这些修复将被纳入即将发布的 7.1 版本中。补丁中涉及的具体修复包括恢复 CONFIG_PKVM_DISABLE_STAGE2_ON_PANIC 的正确拼写、修复 PMU 计数器的写入行为、修复追踪代码中的内存泄漏以及确保 L2 来宾对 ZCR_EL2 的访问被正确限制。

#### 📝 邮件列表

1. **[05-29 11:54]** [GIT PULL] KVM/arm64 fixes for 7.1, take #4
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-29 19:31]** Re: [GIT PULL] KVM/arm64 fixes for 7.1, take #4
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 3 个 thread

---

### Thread 1: [patch 00/24] timekeeping/ptp: Expand snapshot functionality

**📧 邮件数**: 77 | **👥 参与者**: 9 | **📅 开始时间**: Tue, 26 May 2026 19:13:28 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于扩展 Linux 内核时间戳功能的补丁系列，主要集中在时间保持（timekeeping）和精确时间协议（PTP）方面。

1. **原始补丁内容**：补丁系列的核心是引入 `ktime_get_snapshot_id()` 函数，允许捕获特定时钟 ID 的时间戳及其对应的时钟源计数值。这一功能的扩展旨在提高时间戳的准确性和灵活性，尤其是在处理硬件时间戳时。

2. **之前讨论要点**：在历史讨论中，参与者们探讨了如何捕获时钟值及提供核心基础设施，以便驱动程序开发者能够更好地利用这些功能。补丁的设计经过了多次修改和反馈，确保了与现有代码的兼容性。

3. **本周新讨论与进展**：本周的讨论集中在补丁的具体实现上，包括将 `system_time_snapshot::real` 和 `system_time_snapshot::boot` 替换为 `system_time_snapshot::sys`，并最终移除不再使用的代码。此外，补丁还添加了对 AUX 时钟的支持，并确保所有相关驱动程序都能正确使用新的时间戳功能。参与者对补丁的各个部分进行了审查和测试，整体反馈积极，认为补丁系列的实现良好。

总结而言，此次补丁系列通过引入新的时间戳捕获机制，显著增强了 Linux 内核在时间保持和 PTP 方面的能力，为未来的时间同步应用奠定了基础。

#### 📝 邮件列表

1. **[05-26 19:13]** [patch 00/24] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Thomas Gleixner <tglx@kernel.org>
2. **[05-26 19:13]** [patch 01/24] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[05-26 19:13]** [patch 02/24] timekeeping: Use system_time_snapshot::sys instead of
 ::real
   - 发件人: Thomas Gleixner <tglx@kernel.org>
4. **[05-26 19:13]** [patch 03/24] pps: generators: Use ktime_get_real_ts64() instead of
 ktime_get_snapshot()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
5. **[05-26 19:13]** [patch 04/24] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
6. **[05-26 19:13]** [patch 05/24] KVM: arm64: Use ktime_get_snapshot_id() to retrieve
 CLOCK_BOOTTIME
   - 发件人: Thomas Gleixner <tglx@kernel.org>
7. **[05-26 19:13]** [patch 06/24] KVM: arm64: Use ktime_get_snapshot_id() to snapshot
 CLOCK_REALTIME
   - 发件人: Thomas Gleixner <tglx@kernel.org>
8. **[05-26 19:14]** [patch 07/24] ptp: ptp_vmclock: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
9. **[05-26 19:14]** [patch 08/24] timekeeping: Remove system_time_snapshot::real/boot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
10. **[05-26 19:14]** [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
11. **[05-26 19:14]** [patch 10/24] timekeeping: Add system_counterval_t to struct
 system_device_crosststamp
   - 发件人: Thomas Gleixner <tglx@kernel.org>
12. **[05-26 19:14]** [patch 11/24] timekeeping: Add CLOCK ID to system_device_crosststamp
   - 发件人: Thomas Gleixner <tglx@kernel.org>
13. **[05-26 19:14]** [patch 12/24] wifi: iwlwifi: Adopt PTP cross timestamps to core
 changes
   - 发件人: Thomas Gleixner <tglx@kernel.org>
14. **[05-26 19:14]** [patch 13/24] ice/ptp: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
15. **[05-26 19:14]** [patch 14/24] igc: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
16. **[05-26 19:14]** [patch 15/24] net/mlx5: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
17. **[05-26 19:14]** [patch 16/24] virtio_rtc: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
18. **[05-26 19:14]** [patch 17/24] timekeeping: Remove ktime_get_snapshot()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
19. **[05-26 19:14]** [patch 18/24] timekeeping: Prepare for cross timestamps on arbitrary
 clock IDs
   - 发件人: Thomas Gleixner <tglx@kernel.org>
20. **[05-26 19:15]** [patch 19/24] ptp: Use system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
21. **[05-26 19:15]** [patch 20/24] wifi: iwlwifi: Use
 system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
22. **[05-26 19:15]** [patch 21/24] ALSA: hda/common: Use
 system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
23. **[05-26 19:15]** [patch 22/24] timekeeping: Remove
 system_device_crosststamp::sys_realtime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
24. **[05-26 19:15]** [patch 23/24] timekeeping: Add support for AUX clock cross
 timestamping
   - 发件人: Thomas Gleixner <tglx@kernel.org>
25. **[05-26 19:15]** [patch 24/24] ptp: Switch to ktime_get_snapshot_id() for pre/post
 timestamps
   - 发件人: Thomas Gleixner <tglx@kernel.org>
26. **[05-26 14:41]** Re: [patch 01/24] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
27. **[05-26 14:49]** Re: [patch 08/24] timekeeping: Remove system_time_snapshot::real/boot
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
28. **[05-26 14:51]** Re: [patch 13/24] ice/ptp: Use provided clock ID for history snapshot
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
29. **[05-26 14:51]** Re: [patch 14/24] igc: Use provided clock ID for history snapshot
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
30. **[05-26 14:52]** Re: [patch 08/24] timekeeping: Remove system_time_snapshot::real/boot
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
31. **[05-26 14:56]** Re: [patch 00/24] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
32. **[05-27 00:39]** Re: [patch 01/24] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
33. **[05-27 00:40]** Re: [PATCH 2/24] timekeeping: Use system_time_snapshot::sys instead
 of ::real
   - 发件人: David Woodhouse <dwmw2@infradead.org>
34. **[05-27 00:42]** Re: [PATCH 3/24] pps: generators: Use ktime_get_real_ts64() instead
 of ktime_get_snapshot()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
35. **[05-27 00:42]** Re: [PATCH 4/24] pps: Convert to ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
36. **[05-27 00:42]** Re: [PATCH 5/24] KVM: arm64: Use ktime_get_snapshot_id() to
 retrieve CLOCK_BOOTTIME
   - 发件人: David Woodhouse <dwmw2@infradead.org>
37. **[05-27 00:43]** Re: [PATCH 6/24] KVM: arm64: Use ktime_get_snapshot_id() to
 snapshot CLOCK_REALTIME
   - 发件人: David Woodhouse <dwmw2@infradead.org>
38. **[05-27 00:43]** Re: [PATCH 7/24] ptp: ptp_vmclock: Convert to
 ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
39. **[05-27 00:44]** Re: [PATCH 8/24] timekeeping: Remove system_time_snapshot::real/boot
   - 发件人: David Woodhouse <dwmw2@infradead.org>
40. **[05-27 00:44]** Re: [PATCH 9/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
41. **[05-27 00:45]** Re: [PATCH 10/24] timekeeping: Add system_counterval_t to struct
 system_device_crosststamp
   - 发件人: David Woodhouse <dwmw2@infradead.org>
42. **[05-27 00:46]** Re: [PATCH 11/24] timekeeping: Add CLOCK ID to
 system_device_crosststamp
   - 发件人: David Woodhouse <dwmw2@infradead.org>
43. **[05-27 00:47]** Re: [PATCH 12/24] wifi: iwlwifi: Adopt PTP cross timestamps to core
 changes
   - 发件人: David Woodhouse <dwmw2@infradead.org>
44. **[05-27 00:49]** Re: [PATCH 13/24] ice/ptp: Use provided clock ID for history
 snapshot
   - 发件人: David Woodhouse <dwmw2@infradead.org>
45. **[05-27 00:50]** Re: [PATCH 14/24] igc: Use provided clock ID for history snapshot
   - 发件人: David Woodhouse <dwmw2@infradead.org>
46. **[05-27 00:51]** Re: [PATCH 15/24] net/mlx5: Use provided clock ID for history
 snapshot
   - 发件人: David Woodhouse <dwmw2@infradead.org>
47. **[05-27 00:51]** Re: [PATCH 16/24] virtio_rtc: Use provided clock ID for history
 snapshot
   - 发件人: David Woodhouse <dwmw2@infradead.org>
48. **[05-27 00:52]** Re: [PATCH 17/24] timekeeping: Remove ktime_get_snapshot()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
49. **[05-27 00:54]** Re: [PATCH 18/24] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: David Woodhouse <dwmw2@infradead.org>
50. **[05-27 00:54]** Re: [PATCH 19/24] ptp: Use system_device_crosststamp::sys_systime
   - 发件人: David Woodhouse <dwmw2@infradead.org>
51. **[05-27 00:55]** Re: [PATCH 20/24] wifi: iwlwifi: Use
 system_device_crosststamp::sys_systime
   - 发件人: David Woodhouse <dwmw2@infradead.org>
52. **[05-27 00:55]** Re: [PATCH 21/24] ALSA: hda/common: Use
 system_device_crosststamp::sys_systime
   - 发件人: David Woodhouse <dwmw2@infradead.org>
53. **[05-27 00:56]** Re: [PATCH 22/24] timekeeping: Remove
 system_device_crosststamp::sys_realtime
   - 发件人: David Woodhouse <dwmw2@infradead.org>
54. **[05-27 00:56]** Re: [PATCH 23/24] timekeeping: Add support for AUX clock cross
 timestamping
   - 发件人: David Woodhouse <dwmw2@infradead.org>
55. **[05-27 00:57]** Re: [PATCH 24/24] ptp: Switch to ktime_get_snapshot_id() for
 pre/post timestamps
   - 发件人: David Woodhouse <dwmw2@infradead.org>
56. **[05-27 03:55]** Re: [PATCH 0/24] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Arthur Kiyanovski <akiyano@amazon.com>
57. **[05-27 08:56]** Re: [patch 01/24] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
58. **[05-27 08:58]** Re: [patch 02/24] timekeeping: Use system_time_snapshot::sys instead
 of ::real
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
59. **[05-27 09:00]** Re: [patch 03/24] pps: generators: Use ktime_get_real_ts64() instead
 of ktime_get_snapshot()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
60. **[05-27 09:02]** Re: [patch 04/24] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
61. **[05-27 09:02]** Re: [patch 05/24] KVM: arm64: Use ktime_get_snapshot_id() to
 retrieve CLOCK_BOOTTIME
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
62. **[05-27 09:03]** Re: [patch 06/24] KVM: arm64: Use ktime_get_snapshot_id() to
 snapshot CLOCK_REALTIME
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
63. **[05-27 09:10]** Re: [patch 07/24] ptp: ptp_vmclock: Convert to
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
64. **[05-27 09:17]** Re: [patch 08/24] timekeeping: Remove system_time_snapshot::real/boot
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
65. **[05-27 09:18]** Re: [patch 09/24] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
66. **[05-27 09:20]** Re: [patch 17/24] timekeeping: Remove ktime_get_snapshot()
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
67. **[05-27 09:23]** Re: [patch 18/24] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
68. **[05-27 09:24]** Re: [patch 22/24] timekeeping: Remove
 system_device_crosststamp::sys_realtime
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
69. **[05-27 09:24]** Re: [patch 23/24] timekeeping: Add support for AUX clock cross
 timestamping
   - 发件人: Thomas =?utf-8?Q?Wei=C3=9Fschuh?= <thomas.weissschuh@linutronix.de>
70. **[05-27 10:02]** Re: [patch 05/24] KVM: arm64: Use ktime_get_snapshot_id() to retrieve CLOCK_BOOTTIME
   - 发件人: Marc Zyngier <maz@kernel.org>
71. **[05-27 10:03]** Re: [patch 06/24] KVM: arm64: Use ktime_get_snapshot_id() to snapshot CLOCK_REALTIME
   - 发件人: Marc Zyngier <maz@kernel.org>
72. **[05-27 14:10]** Re: [patch 24/24] ptp: Switch to ktime_get_snapshot_id() for pre/post
 timestamps
   - 发件人: Vadim Fedorenko <vadim.fedorenko@linux.dev>
73. **[05-27 17:58]** Re: [patch 01/24] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
74. **[05-27 18:02]** Re: [patch 04/24] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
75. **[05-27 17:28]** Re: [patch 05/24] KVM: arm64: Use ktime_get_snapshot_id() to
 retrieve CLOCK_BOOTTIME
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
76. **[05-27 16:56]** Re: [patch 24/24] ptp: Switch to ktime_get_snapshot_id() for
 pre/post timestamps
   - 发件人: Jakub Kicinski <kuba@kernel.org>
77. **[05-28 15:55]** Re: [patch 24/24] ptp: Switch to ktime_get_snapshot_id() for
 pre/post timestamps
   - 发件人: Thomas Gleixner <tglx@kernel.org>

---

### Thread 2: [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality

**📧 邮件数**: 29 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 29 May 2026 21:59:47 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于扩展 Linux 内核时间戳功能的补丁系列，主题为“[patch V2 00/25] timekeeping/ptp: Expand snapshot functionality”。该补丁旨在增强 PTP（精确时间协议）相关的时间快照功能，主要包括捕获 CLOCK* 值及其对应的时钟源计数值。

**补丁内容**：
补丁系列的核心是实现时间快照机制，允许同时捕获 CLOCK 值和时钟源计数值，以支持非硬件采样和扩展硬件跨时间戳机制。此外，新增 AUX 时钟支持和派生时钟源的快照机制。

**历史讨论**：
在之前的讨论中，参与者探讨了如何捕获这些值以及如何为驱动程序开发者提供核心基础设施。补丁 V1 的反馈主要集中在命名、错误处理和代码清晰度等方面。

**本周新讨论**：
本周的讨论中，Thomas Gleixner 提出了补丁 V2，修复了 V1 中的错误，更新了结构体成员的命名，并引入了新的功能支持。参与者对补丁表示赞赏，并进行了多次测试和审查。此外，补丁系列的后续更新逐步替换了旧的时间快照函数，增加了对 AUX 时钟的支持，并最终清理了不再使用的成员，确保代码的整洁和功能的完整性。

总的来说，本周的讨论和补丁更新表明了对时间快照功能的持续改进和优化，旨在提升 Linux 内核在时间管理方面的能力。

#### 📝 邮件列表

1. **[05-29 21:59]** [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Thomas Gleixner <tglx@kernel.org>
2. **[05-29 21:59]** [patch V2 01/25] timekeeping: Provide ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[05-29 21:59]** [patch V2 02/25] timekeeping: Use
 system_time_snapshot::systime/monoraw instead of ::real/raw
   - 发件人: Thomas Gleixner <tglx@kernel.org>
4. **[05-29 21:59]** [patch V2 03/25] pps: generators: Use ktime_get_real_ts64() instead
 of ktime_get_snapshot()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
5. **[05-29 22:00]** [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
6. **[05-29 22:00]** [patch V2 05/25] KVM: arm64: Use ktime_get_snapshot_id() to retrieve
 CLOCK_BOOTTIME
   - 发件人: Thomas Gleixner <tglx@kernel.org>
7. **[05-29 22:00]** [patch V2 06/25] KVM: arm64: Use ktime_get_snapshot_id() to snapshot
 CLOCK_REALTIME
   - 发件人: Thomas Gleixner <tglx@kernel.org>
8. **[05-29 22:00]** [patch V2 07/25] ptp: ptp_vmclock: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
9. **[05-29 22:00]** [patch V2 08/25] timekeeping: Remove
 system_time_snapshot::real/boot/raw
   - 发件人: Thomas Gleixner <tglx@kernel.org>
10. **[05-29 22:00]** [patch V2 09/25] timekeeping: Add CLOCK_AUX support for
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
11. **[05-29 22:00]** [patch V2 10/25] timekeeping: Add system_counterval_t to struct
 system_device_crosststamp
   - 发件人: Thomas Gleixner <tglx@kernel.org>
12. **[05-29 22:00]** [patch V2 11/25] timekeeping: Add CLOCK ID to
 system_device_crosststamp
   - 发件人: Thomas Gleixner <tglx@kernel.org>
13. **[05-29 22:00]** [patch V2 12/25] wifi: iwlwifi: Adopt PTP cross timestamps to core
 changes
   - 发件人: Thomas Gleixner <tglx@kernel.org>
14. **[05-29 22:00]** [patch V2 13/25] ice/ptp: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
15. **[05-29 22:00]** [patch V2 14/25] igc: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
16. **[05-29 22:00]** [patch V2 15/25] net/mlx5: Use provided clock ID for history snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
17. **[05-29 22:00]** [patch V2 16/25] virtio_rtc: Use provided clock ID for history
 snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
18. **[05-29 22:00]** [patch V2 17/25] timekeeping: Remove ktime_get_snapshot()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
19. **[05-29 22:01]** [patch V2 18/25] timekeeping: Prepare for cross timestamps on
 arbitrary clock IDs
   - 发件人: Thomas Gleixner <tglx@kernel.org>
20. **[05-29 22:01]** [patch V2 19/25] ptp: Use system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
21. **[05-29 22:01]** [patch V2 20/25] wifi: iwlwifi: Use
 system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
22. **[05-29 22:01]** [patch V2 21/25] ALSA: hda/common: Use
 system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
23. **[05-29 22:01]** [patch V2 22/25] timekeeping: Remove
 system_device_crosststamp::sys_realtime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
24. **[05-29 22:01]** [patch V2 23/25] timekeeping: Add support for AUX clock cross
 timestamping
   - 发件人: Thomas Gleixner <tglx@kernel.org>
25. **[05-29 22:01]** [patch V2 24/25] ptp: Switch to ktime_get_snapshot_id() for pre/post
 timestamps
   - 发件人: Thomas Gleixner <tglx@kernel.org>
26. **[05-29 22:01]** [patch V2 25/25] timekeeping: Add clocksource read_snapshot() method
 and hw_cycles to snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
27. **[05-29 13:33]** Re: [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Jacob Keller <jacob.e.keller@intel.com>
28. **[05-30 13:04]** Re: [patch V2 03/25] pps: generators: Use ktime_get_real_ts64()
 instead of ktime_get_snapshot()
   - 发件人: Rodolfo Giometti <giometti@enneenne.com>
29. **[05-30 13:08]** Re: [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Rodolfo Giometti <giometti@enneenne.com>

---

### Thread 3: [kvm-unit-tests PATCH v2] arm: add wfx test case

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 27 May 2026 12:18:21 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是为 ARM 架构的 KVM 单元测试添加 WFX 测试用例。原始的补丁（PATCH v2）由 Alex Bennée 提交，目的是基于之前为 QEMU TCG 测试编写的类似测试案例，利用 kvm-unit-tests 的功能来处理 GIC 和 IRQ。

在之前的讨论中，补丁经过了初步审查，Richard Henderson 表示支持。补丁的主要改动包括：将超时设置为计算得出的 10ms、添加每个测试的注释、使用 SEVL 进行本地清除、根据当前 EL 设置 GIC IRQ、EOI GIC 以及修复一些代码风格问题。

在本周的新讨论中，Alex Bennée 提供了对测试用例的反馈，指出在运行测试时出现了意外失败，特别是在 WFET 测试中，WFI 可能会在本地中断启用之前完成。Alex 建议修改测试代码，调整中断启用的顺序，以确保 WFI 测试的有效性。此外，讨论中还提到，测试总结的输出可能会让用户感到困惑，尤其是在系统不支持 WFxT 指令时。

总体而言，本周的讨论集中在对补丁的细节审查和测试用例的改进建议上，旨在提高测试的准确性和用户体验。

#### 📝 邮件列表

1. **[05-27 12:18]** [kvm-unit-tests PATCH v2] arm: add wfx test case
   - 发件人: =?UTF-8?q?Alex=20Benn=C3=A9e?= <alex.bennee@linaro.org>
2. **[05-28 09:23]** Re: [kvm-unit-tests PATCH v2] arm: add wfx test case
   - 发件人: Richard Henderson <richard.henderson@linaro.org>
3. **[05-29 15:06]** Re: [kvm-unit-tests PATCH v2] arm: add wfx test case
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[05-29 15:12]** Re: [kvm-unit-tests PATCH v2] arm: add wfx test case
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

