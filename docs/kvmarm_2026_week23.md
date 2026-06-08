# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-06-08 00:57:41

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 276
- **总 Thread 数**: 42
- **大型 Thread** (>20封): 4 个

### 分类分布

- **PATCH**: 37 threads (231 邮件)
- **RFC**: 2 threads (32 邮件)
- **Bug Report**: 1 threads (1 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Other**: 1 threads (10 邮件)

---

## 📌 PATCH

共 37 个 thread

---

### Thread 1: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT
 entries for memory

**📧 邮件数**: 52 | **👥 参与者**: 7 | **📅 开始时间**: Tue, 19 May 2026 11:25:20 +0530

#### 🤖 AI 总结

本邮件线程讨论的主题是针对 ARM64 架构的 RMI（Realm Management Interface）进行的一系列补丁（PATCH v14 08/44），主要目的是确保 RMM（Realm Management Monitor）能够为内存提供 GPT（Granule Page Table）条目。

**历史讨论：**
在之前的讨论中，参与者提出了对补丁的命名建议，讨论了 RMM 的功能和实现细节，包括如何处理错误返回值和内存跟踪的逻辑。特别是，Gavin Shan 指出 RMM_GRANULE_TRACKING_SIZE 在当前补丁系列中未被使用，并建议将某些逻辑合并到相关函数中。

**本周新讨论：**
本周的讨论集中在补丁的细节和实现进展上。Suzuki K Poulose 指出，由于 API 的更新，某些之前需要的跟踪大小现在已不再必要，因此建议删除相关代码。Steven Price 也确认了这一点，并表示将删除未使用的代码块。此外，参与者讨论了 RMM 和 KVM（Kernel-based Virtual Machine）之间的初始化顺序，以确保在 KVM 初始化之前调用 RMM 的初始化函数，以支持 Realm 客户端。

总体来看，讨论中强调了代码的清晰性和功能的准确性，同时也对未来的功能扩展进行了展望，如动态管理内存的支持。

#### 📝 邮件列表

1. **[05-19 11:25]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT
 entries for memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
2. **[05-19 11:32]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
3. **[05-19 15:10]** Re: [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
4. **[05-21 10:39]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
5. **[05-21 10:58]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Gavin Shan <gshan@redhat.com>
6. **[05-21 14:38]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
7. **[05-21 13:40]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[05-21 14:02]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[05-21 14:30]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's page size
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[05-21 14:47]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[05-21 14:59]** Re: [PATCH v14 09/44] arm64: RMI: Provide functions to delegate/undelegate ranges of memory
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[05-21 15:35]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[05-21 16:33]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Steven Price <steven.price@arm.com>
14. **[05-21 16:39]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[05-21 16:49]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
16. **[05-22 10:58]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the RMM
   - 发件人: Marc Zyngier <maz@kernel.org>
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
22. **[05-27 16:21]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[05-28 14:07]** Re: [PATCH v14 20/44] arm64: RMI: Support for the VGIC in realms
   - 发件人: Gavin Shan <gshan@redhat.com>
24. **[05-28 14:38]** Re: [PATCH v14 22/44] arm64: RMI: Handle realm enter/exit
   - 发件人: Gavin Shan <gshan@redhat.com>
25. **[05-28 08:10]** Re: [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[06-02 12:15]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
27. **[06-02 15:49]** Re: [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a
 realm.
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
28. **[06-03 11:15]** Re: [PATCH v14 04/44] arm64: RMI: Add SMC definitions for calling the
 RMM
   - 发件人: Steven Price <steven.price@arm.com>
29. **[06-03 11:57]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
30. **[06-03 11:57]** Re: [PATCH v14 06/44] arm64: RMI: Check for RMI support at init
   - 发件人: Steven Price <steven.price@arm.com>
31. **[06-03 16:48]** Re: [PATCH v14 07/44] arm64: RMI: Configure the RMM with the host's
 page size
   - 发件人: Steven Price <steven.price@arm.com>
32. **[06-03 16:48]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Steven Price <steven.price@arm.com>
33. **[06-03 16:48]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Steven Price <steven.price@arm.com>
34. **[06-03 16:48]** Re: [PATCH v14 08/44] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Steven Price <steven.price@arm.com>
35. **[06-04 15:43]** Re: [PATCH v14 09/44] arm64: RMI: Provide functions to
 delegate/undelegate ranges of memory
   - 发件人: Steven Price <steven.price@arm.com>
36. **[06-04 16:19]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
37. **[06-04 16:19]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
38. **[06-04 16:19]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
39. **[06-04 16:27]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
40. **[06-04 16:27]** Re: [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
41. **[06-04 16:55]** Re: [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a
 realm.
   - 发件人: Steven Price <steven.price@arm.com>
42. **[06-05 16:23]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
43. **[06-05 09:28]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
44. **[06-05 18:11]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
45. **[06-05 21:20]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Gavin Shan <gshan@redhat.com>
46. **[06-05 16:35]** Re: [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Lorenzo Pieralisi <lpieralisi@kernel.org>
47. **[06-05 16:01]** Re: [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
48. **[06-05 16:01]** Re: [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
49. **[06-05 16:02]** Re: [PATCH v14 19/44] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
50. **[06-05 16:02]** Re: [PATCH v14 20/44] arm64: RMI: Support for the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
51. **[06-05 16:02]** Re: [PATCH v14 22/44] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
52. **[06-05 16:02]** Re: [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 2: [PATCH v3 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups

**📧 邮件数**: 23 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  2 Jun 2026 16:11:32 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的 KVM 相关的 FPSIMD、SVE 和 SME 状态管理代码的清理工作。以下是本周讨论的主要内容：

1. **原始 Patch/问题内容**：Mark Rutland 提出的补丁系列（[PATCH v3 00/18]）旨在清理低级别的 FPSIMD/SVE/SME 状态管理代码，以简化维护和扩展（例如为 KVM 添加 SME 支持），并改善调试能力。

2. **之前讨论要点**：之前的讨论集中在如何减少 KVM 和内核其他部分之间的代码重复，简化状态保存/恢复的调用约定，以及通过引入不透明类型来减少内存状态管理的误用。此外，增加了显式的内存安全和并发问题检测工具，以便 KASAN 和 KCSAN 能够识别潜在问题。

3. **本周的新讨论与进展**：
   - 本周的补丁包括将 SVE 和 SME 的保存/恢复逻辑移至内联汇编，消除了对旧汇编宏的依赖，简化了代码结构。
   - 讨论中还提到了一些潜在的类型不匹配问题，特别是在处理 FFR 参数时，可能会导致错误的保存/恢复行为。Mark Rutland 表示将会在后续版本中修复这些问题。
   - 最后，删除了不再需要的 `<asm/fpsimdmacros.h>` 文件，进一步清理了代码。

总体而言，本周的讨论聚焦于通过清理和重构代码来提高 ARM64 KVM 的可维护性和可靠性。

#### 📝 邮件列表

1. **[06-02 16:11]** [PATCH v3 00/18] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[06-02 16:11]** [PATCH v3 01/18] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[06-02 16:11]** [PATCH v3 02/18] KVM: arm64: Don't override FFR save/restore argument
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[06-02 16:11]** [PATCH v3 03/18] KVM: arm64: pkvm: Save host FPMR in host cpu context
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[06-02 16:11]** [PATCH v3 04/18] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[06-02 16:11]** [PATCH v3 05/18] arm64: fpsimd: Fold sve_init_regs() into do_sve_acc()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[06-02 16:11]** [PATCH v3 06/18] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[06-02 16:11]** [PATCH v3 07/18] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
9. **[06-02 16:11]** [PATCH v3 08/18] arm64: fpsimd: Use assembler for baseline SME instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[06-02 16:11]** [PATCH v3 09/18] arm64: fpsimd: Move sve_get_vl() and sme_get_vl() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[06-02 16:11]** [PATCH v3 10/18] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[06-02 16:11]** [PATCH v3 11/18] arm64: fpsimd: Split FPSR/FPCR from SVE save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
13. **[06-02 16:11]** [PATCH v3 12/18] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
14. **[06-02 16:11]** [PATCH v3 13/18] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
15. **[06-02 16:11]** [PATCH v3 14/18] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
16. **[06-02 16:11]** [PATCH v3 15/18] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
17. **[06-02 16:11]** [PATCH v3 16/18] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
18. **[06-02 16:11]** [PATCH v3 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
19. **[06-02 16:11]** [PATCH v3 18/18] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
20. **[06-02 16:30]** Re: [PATCH v3 17/18] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Brown <broonie@kernel.org>
21. **[06-02 16:33]** Re: [PATCH v3 18/18] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Mark Brown <broonie@kernel.org>
22. **[06-02 16:36]** Re: [PATCH v3 02/18] KVM: arm64: Don't override FFR save/restore
 argument
   - 发件人: Mark Brown <broonie@kernel.org>
23. **[06-03 10:25]** Re: [PATCH v3 02/18] KVM: arm64: Don't override FFR save/restore
 argument
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 3: [PATCH v4 00/20] arm64+KVM: FPSIMD/SVE/SME cleanups

**📧 邮件数**: 22 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  3 Jun 2026 12:06:10 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构下 KVM 的 FPSIMD、SVE 和 SME 状态管理的清理工作，涉及一系列补丁（PATCH v4 00/20）。

1. **原始补丁内容**：该系列补丁旨在清理低级的 FPSIMD、SVE 和 SME 状态管理代码，以便于维护和扩展（例如为 KVM 添加 SME 支持），并提升调试能力。补丁包括修复潜在的类型不匹配问题、简化调用约定、减少代码重复、提高可读性和调试能力等。

2. **之前的讨论要点**：在历史讨论中，补丁逐步修复了多个潜在问题，如 SVE 和 SME 状态的管理、内存安全问题的检测等。参与者们讨论了如何通过使用不透明类型来简化状态管理，并消除了不必要的代码。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的应用和进一步的代码清理上。Mark Rutland 提交了多项补丁，涵盖了 SVE 和 SME 状态的保存/恢复逻辑的内联化、使用不透明类型、移除不再需要的宏等。最终，Will Deacon 确认了这些补丁的应用，并表示感谢。

通过这些补丁，代码的可维护性和可读性得到了显著提升，同时也为未来的扩展打下了基础。

#### 📝 邮件列表

1. **[06-03 12:06]** [PATCH v4 00/20] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[06-03 12:06]** [PATCH v4 01/20] arm64: fpsimd: Fix type mismatch in sve_{save,load}_state()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[06-03 12:06]** [PATCH v4 02/20] arm64: fpsimd: Fix type mismatch in sme_{save,load}_state()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
4. **[06-03 12:06]** [PATCH v4 03/20] KVM: arm64: Don't include <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[06-03 12:06]** [PATCH v4 04/20] KVM: arm64: Don't override FFR save/restore argument
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[06-03 12:06]** [PATCH v4 05/20] KVM: arm64: pkvm: Save host FPMR in host cpu context
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[06-03 12:06]** [PATCH v4 06/20] KVM: arm64: pkvm: Remove struct cpu_sve_state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[06-03 12:06]** [PATCH v4 07/20] arm64: fpsimd: Fold sve_init_regs() into do_sve_acc()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
9. **[06-03 12:06]** [PATCH v4 08/20] arm64: fpsimd: Remove sve_set_vq() and sme_set_vq()
   - 发件人: Mark Rutland <mark.rutland@arm.com>
10. **[06-03 12:06]** [PATCH v4 09/20] arm64: fpsimd: Use assembler for SVE instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[06-03 12:06]** [PATCH v4 10/20] arm64: fpsimd: Use assembler for baseline SME instructions
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[06-03 12:06]** [PATCH v4 11/20] arm64: fpsimd: Move sve_get_vl() and sme_get_vl() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
13. **[06-03 12:06]** [PATCH v4 12/20] arm64: sysreg: Add FPCR and FPSR
   - 发件人: Mark Rutland <mark.rutland@arm.com>
14. **[06-03 12:06]** [PATCH v4 13/20] arm64: fpsimd: Split FPSR/FPCR from SVE save/restore
   - 发件人: Mark Rutland <mark.rutland@arm.com>
15. **[06-03 12:06]** [PATCH v4 14/20] arm64: fpsimd: Move fpsimd save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
16. **[06-03 12:06]** [PATCH v4 15/20] arm64: fpsimd: Use opaque type for SVE state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
17. **[06-03 12:06]** [PATCH v4 16/20] arm64: fpsimd: Use opaque type for SME state
   - 发件人: Mark Rutland <mark.rutland@arm.com>
18. **[06-03 12:06]** [PATCH v4 17/20] arm64: fpsimd: Move SVE save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
19. **[06-03 12:06]** [PATCH v4 18/20] arm64: fpsimd: Move sve_flush_live() inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
20. **[06-03 12:06]** [PATCH v4 19/20] arm64: fpsimd: Move SME save/restore inline
   - 发件人: Mark Rutland <mark.rutland@arm.com>
21. **[06-03 12:06]** [PATCH v4 20/20] arm64: fpsimd: Remove <asm/fpsimdmacros.h>
   - 发件人: Mark Rutland <mark.rutland@arm.com>
22. **[06-03 22:06]** Re: [PATCH v4 00/20] arm64+KVM: FPSIMD/SVE/SME cleanups
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 4: [PATCH v2 0/2] KVM: arm64: nv: Fixes for FEAT_XNX (and the lack thereof)

**📧 邮件数**: 14 | **👥 参与者**: 5 | **📅 开始时间**: Tue,  2 Jun 2026 09:58:59 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上对 FEAT_XNX 特性的修复以及相关的 vCPU 处理改进。

1. **原始 patch/问题的内容**：本次讨论的补丁（PATCH v2 0/2）主要集中在修复 KVM 对 FEAT_XNX 特性的处理，具体包括修正 XN[0] 的处理逻辑以及正确识别 stage-2 的可执行 PTEs（Page Table Entries）。

2. **之前讨论要点**：在历史讨论中，参与者提出了对 v1 版本补丁的反馈，指出了在处理 XN[0] 时存在的逻辑错误，并建议改用更简洁的函数来减少重复代码。

3. **本周的新讨论、进展或结论**：本周的讨论中，Oliver Upton 提交了 v2 版本的补丁，解决了之前提到的问题，并得到了 Wei-Lin Chang 的认可和审查。Wei-Lin 还提出了进一步的优化建议，认为可以简化代码逻辑。Hyunwoo Kim 也提出了针对 vCPU 状态清理的补丁，确保在每次运行时清理特定字段，以避免潜在的错误。总体来看，讨论氛围积极，参与者们在不断完善补丁和提出改进建议。

#### 📝 邮件列表

1. **[06-02 09:58]** [PATCH v2 0/2] KVM: arm64: nv: Fixes for FEAT_XNX (and the lack thereof)
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-02 09:59]** [PATCH v2 1/2] KVM: arm64: nv: Fix handling of XN[0] when !FEAT_XNX
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-02 09:59]** [PATCH v2 2/2] KVM: arm64: Correctly identify executable PTEs at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-03 23:57]** Re: [PATCH v2 1/2] KVM: arm64: nv: Fix handling of XN[0] when
 !FEAT_XNX
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[06-03 16:06]** Re: [PATCH v2 1/2] KVM: arm64: nv: Fix handling of XN[0] when
 !FEAT_XNX
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-04 13:37]** Re: [PATCH v2 1/2] KVM: arm64: nv: Fix handling of XN[0] when
 !FEAT_XNX
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[06-04 13:41]** Re: [PATCH v2 2/2] KVM: arm64: Correctly identify executable PTEs at
 stage-2
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[06-05 00:12]** [PATCH v2 0/2] KVM: arm64: Sanitise host vCPU fields copied in flush_hyp_vcpu()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
9. **[06-05 00:12]** [PATCH v2 1/2] KVM: arm64: Clear __hyp_running_vcpu when flushing the pKVM hyp vCPU
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
10. **[06-05 00:12]** [PATCH v2 2/2] KVM: arm64: Bound used_lrs when flushing the pKVM hyp vCPU
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
11. **[06-04 16:29]** Re: [PATCH v2 0/2] KVM: arm64: Sanitise host vCPU fields copied in flush_hyp_vcpu()
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[06-05 09:58]** Re: [PATCH v2 2/2] KVM: arm64: Bound used_lrs when flushing the pKVM hyp vCPU
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[06-06 17:52]** Re: [PATCH v2 2/2] KVM: arm64: Bound used_lrs when flushing the pKVM
 hyp vCPU
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
14. **[06-06 11:52]** Re: [PATCH v2 2/2] KVM: arm64: Bound used_lrs when flushing the pKVM hyp vCPU
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 5: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 13 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 19 May 2026 15:27:14 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于引入一个可定制的 aarch64 KVM 主机模型的补丁系列（PATCH v5 00/18）。该补丁旨在增强当前的 KVM 主机模型，使用户能够设置可写的 ID 寄存器字段，从而在不同硬件之间迁移虚拟机时提供更大的灵活性。

在历史讨论中，Eric Auger 提出了多个补丁，主要包括对寄存器定义的排序、自动生成更新、以及处理生成的 ID 寄存器定义的基础设施等。这些补丁的目标是优化 KVM/arm 的功能，尤其是在 v6.7 内核之后，用户空间可以覆盖部分 ID 寄存器的值。

在本周的新讨论中，参与者对补丁进行了评审，Shameer Kolothum Thodi 对多个补丁表示认可，并提出了对某些补丁的建议和修正意见。此外，Jinqian Yang 进行了测试，确认补丁在 Hisilicon KunPeng HIP09 和 HIP12 芯片上能够正常工作，并分享了用于测试的 QEMU 命令行。这些进展表明补丁的实施正在顺利进行，并获得了积极的反馈。

#### 📝 邮件列表

1. **[05-19 15:27]** [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[05-19 15:27]** [PATCH v5 02/18] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-19 15:27]** [PATCH v5 03/18] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[05-19 15:27]** [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-19 15:27]** [PATCH v5 09/18] target/arm/kvm: Introduce kvm_get_writable_id_regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[06-01 14:07]** RE: [PATCH v5 02/18] target/arm/cpu-sysregs.h.inc: Sort by name
 alphabetical order
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
7. **[06-01 14:09]** RE: [PATCH v5 03/18] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
8. **[06-01 14:28]** RE: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
9. **[06-01 15:26]** RE: [PATCH v5 09/18] target/arm/kvm: Introduce
 kvm_get_writable_id_regs
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
10. **[06-04 14:08]** Re: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Jinqian Yang <yangjinqian1@huawei.com>
11. **[06-04 14:32]** Re: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Jinqian Yang <yangjinqian1@huawei.com>
12. **[06-04 10:31]** Re: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[06-04 20:00]** Re: [PATCH v5 00/18] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Jinqian Yang <yangjinqian1@huawei.com>

---

### Thread 6: [PATCH v1 00/26] KVM: arm64 on s390 System Register Handling

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 29 May 2026 17:55:33 +0200

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM/arm64 在 s390 上的系统寄存器处理的补丁（PATCH v1 00/26）。该补丁旨在重构和共享 KVM/arm64 代码，引入 ARM 客户端管理功能，并实现主机系统寄存器及异常处理。

在历史讨论中，补丁的主要内容包括对 arm64 特性检测和 ID 寄存器处理的重构，以便在不同架构间复用；将 ID 寄存器的存储结构进行重组；以及修复了 set_oslsr_el1 函数中的错误，使其正确写入 OSLAR_EL1 寄存器。此外，还增加了用于查询 ARM 客户端时间的函数。

本周的新讨论中，参与者对补丁的具体实现进行了深入探讨。Oliver Upton 提出了对某些寄存器处理的疑问，并建议将特定的实现细节限制在 s390 的代码中。Andreas Grapentin 也确认了之前的实现错误，并表示将在下一个版本中进行修正。同时，关于如何虚拟化客户机计数器的讨论也得到了进一步的澄清。

总体来看，本周的讨论集中在补丁的具体实现细节及其对不同架构的适应性上，参与者们对补丁的优化和修正提出了建设性的意见。

#### 📝 邮件列表

1. **[05-29 17:55]** [PATCH v1 00/26] KVM: arm64 on s390 System Register Handling
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[05-29 17:55]** [PATCH v1 09/26] KVM: arm64: Refactor idreg caching into dedicated structure
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[05-29 17:55]** [PATCH v1 10/26] KVM: arm64: Fix set_oslsr_el1 to write to OSLAR_EL1
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[05-29 17:55]** [PATCH v1 12/26] KVM: arm64: Add PVM_ prefix to avoid name collisions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[05-29 17:55]** [PATCH v1 15/26] s390: Add functions to query arm guest time
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[06-01 17:52]** Re: [PATCH v1 00/26] KVM: arm64 on s390 System Register Handling
   - 发件人: Claudio Imbrenda <imbrenda@linux.ibm.com>
7. **[06-01 15:21]** Re: [PATCH v1 10/26] KVM: arm64: Fix set_oslsr_el1 to write to
 OSLAR_EL1
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[06-01 15:23]** Re: [PATCH v1 12/26] KVM: arm64: Add PVM_ prefix to avoid name
 collisions
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[06-01 15:25]** Re: [PATCH v1 15/26] s390: Add functions to query arm guest time
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[06-01 15:28]** Re: [PATCH v1 09/26] KVM: arm64: Refactor idreg caching into
 dedicated structure
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[06-02 11:31]** Re: [PATCH v1 10/26] KVM: arm64: Fix set_oslsr_el1 to write to
 OSLAR_EL1
   - 发件人: Andreas Grapentin <gra@linux.ibm.com>
12. **[06-02 15:25]** Re: [PATCH v1 15/26] s390: Add functions to query arm guest time
   - 发件人: Andreas Grapentin <gra@linux.ibm.com>
13. **[06-02 14:33]** Re: [PATCH v1 15/26] s390: Add functions to query arm guest time
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 7: [PATCH 0/3] KVM: arm64: FEAT_{S1POE,ATS1A} support fixes

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue,  2 Jun 2026 16:54:26 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构中对 FEAT_{S1POE, ATS1A} 特性的支持修复的补丁。原始补丁包含三个部分，旨在解决 L2 客户端在主机启用 FEAT_S1POE 时无法启动的问题。经过调查，发现 AT S1E1A 的处理代码虽然已准备就绪，但未完全接入系统指令处理表，导致异常未被正确处理。

在之前的讨论中，Marc Zyngier 提到，L2 客户端无法向前推进，而 KVM 在 L1 层并未意识到存在问题。此外，还发现了 CPTR_EL2 处理中的一个拼写错误。

本周的新讨论中，Marc Zyngier 提出了三项补丁，分别修复了 CPTR_EL2.E0POE 的传播、将 AT S1E1A 插入系统指令处理表，以及向内核暴露 ID_AA64ISAR2_EL1.ATS1A，以确保 KVM 能正确处理相关特性。Oliver Upton 和 Joey Gouly 对补丁进行了审核并表示支持，确认了补丁的有效性和必要性。这些修复将有助于提升 KVM 在 arm64 架构下的稳定性和功能性。

#### 📝 邮件列表

1. **[06-02 16:54]** [PATCH 0/3] KVM: arm64: FEAT_{S1POE,ATS1A} support fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[06-02 16:54]** [PATCH 1/3] KVM: arm64: Key CPTR_EL2.E0POE propagation on FEAT_S1POE
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[06-02 16:54]** [PATCH 2/3] KVM: arm64: Wire AT S1E1A in the system instruction handling table
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-02 16:54]** [PATCH 3/3] arm64: cpufeature: Expose ID_AA64ISAR2_EL1.ATS1A to KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-02 10:49]** Re: [PATCH 0/3] KVM: arm64: FEAT_{S1POE,ATS1A} support fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-03 11:41]** Re: [PATCH 0/3] KVM: arm64: FEAT_{S1POE,ATS1A} support fixes
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 8: [PATCH 0/5] KVM: arm64: nv: MMU fixes for 7.2

**📧 邮件数**: 6 | **👥 参与者**: 1 | **📅 开始时间**: Tue,  2 Jun 2026 16:54:45 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 MMU（内存管理单元）修复补丁，旨在为 7.2 版本提供改进。Oliver Upton 提出了五个补丁，主要集中在解决嵌套 MMU 中的一些问题，这些问题在最近的代码审查和 AI 错误报告中被发现。

补丁内容包括：
1. **补丁 1**：修复了 `kvm_translate_vncr()` 函数在与 MMU 通知器竞争时未释放 PFN（页面帧号）引用的问题。
2. **补丁 2**：确保在 `kvm_translate_vncr()` 中完全更新 VNCR（虚拟网络控制寄存器）修复映射状态。
3. **补丁 3**：在描述符更新失败时注入 SEA（系统错误异常）TTW（触发写入）信号。
4. **补丁 4**：在 `__kvm_at_s12()` 函数中处理竞争条件时，确保正确传播返回值以重启指令。
5. **补丁 5**：在 `kvm_walk_nested_s2()` 返回 -EAGAIN 时，确保调用者能够重启翻译过程。

本周的讨论主要集中在这些补丁的具体实现和修复内容上，参与者一致认为这些修复是必要的，并且将有助于提高 KVM 的稳定性和性能。

#### 📝 邮件列表

1. **[06-02 16:54]** [PATCH 0/5] KVM: arm64: nv: MMU fixes for 7.2
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-02 16:54]** [PATCH 1/5] KVM: arm64: Don't leak PFN when kvm_translate_vncr() races MMU notifier
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-02 16:54]** [PATCH 2/5] KVM: arm64: nv: Fully update VNCR fixmap state in kvm_translate_vncr()
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-02 16:54]** [PATCH 3/5] KVM: arm64: nv: Inject SEA TTW when desc update can't write to GPA
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-02 16:54]** [PATCH 4/5] KVM: arm64: Restart instruction upon race in __kvm_at_s12()
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-02 16:54]** [PATCH 5/5] KVM: arm64: nv: Restart stage-1 walk if stage-2 desc update fails
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 9: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS

**📧 邮件数**: 5 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 1 Jun 2026 08:50:22 +0800

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中添加对 FEAT_HDBSS 的支持的补丁（PATCH v3 3/5）。FEAT_HDBSS 是一种硬件特性，旨在提升虚拟化性能。

在之前的讨论中，参与者探讨了是否可以引入一个通用的能力（KVM_CAP_HW_DIRTY_STATE），以便其他架构也能复用这一特性。然而，Marc Zyngier 对此提出了质疑，认为现有的脏页日志/位图机制已经足够，不需要额外的特性来实现类似功能。他指出，若要保持通用性，性能可能会受到影响，而如果专注于架构特定的实现，则可以获得更好的性能。

在本周的新讨论中，Inochi Amaoto 最终同意了 Marc 的观点，认为保持 HDBSS 的架构特定性是更合适的选择。同时，他提到在即将发布的 v4 版本中，将完全移除 ioctl 接口，HDBSS 将在迁移设置期间自动启用，并在迁移完成后自动禁用，从而使能力命名问题不再重要。Inochi 计划尽快发布更新的补丁版本。

#### 📝 邮件列表

1. **[06-01 08:50]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Inochi Amaoto <inochiama@gmail.com>
2. **[06-01 09:58]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[06-01 17:05]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Inochi Amaoto <inochiama@gmail.com>
4. **[06-04 16:24]** Re: [PATCH v3 5/5] KVM: arm64: nv: Create nested IPA direct map to
 speed up reverse map removal
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
5. **[06-05 16:29]** Re: [PATCH v3 3/5] KVM: arm64: Add support for FEAT_HDBSS
   - 发件人: Tian Zheng <zhengtian10@huawei.com>

---

### Thread 10: [PATCH] KVM: arm64: Reallocate the nested_mmus array under the
 mmu_lock

**📧 邮件数**: 5 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 5 Jun 2026 03:30:00 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在重新分配 `nested_mmus` 数组，以确保在 `mmu_lock` 锁下进行操作。

**原始补丁内容**：
补丁提出在持有 `mmu_lock` 的情况下重新分配 `nested_mmus` 数组，以避免在 `kvm_vcpu_init_nested()` 函数中仅持有 `config_lock` 时可能导致的内存引用错误。补丁建议在锁外分配新数组，并在锁内进行数据复制和指针交换，确保在释放旧数组之前不会有其他线程访问它。

**之前讨论要点**：
在历史讨论中，未提及具体的补丁内容，但本周的讨论中提到，原补丁的描述可能引起误解，特别是“在锁后分配”的表述可能让人感到不安。参与者建议更改为“在 `mmu_lock` 后重新分配 `nested_mmus` 数组”，以更清晰地传达意图。

**本周的新讨论与进展**：
本周的讨论集中在补丁的细节和描述上。Hyunwoo Kim 提供了补丁的详细背景，解释了在 `mmu_lock` 下的并发问题，并表示将根据反馈修改补丁描述。Oliver Upton 和 Sean Christopherson 对补丁表示认可，并建议进行一些描述上的调整。最后，Marc Zyngier 也支持修改后的补丁，并鼓励发送新版本。

总的来说，本周的讨论主要围绕补丁的清晰性和准确性展开，参与者对补丁的方向表示支持，并期待进一步的改进。

#### 📝 邮件列表

1. **[06-05 03:30]** [PATCH] KVM: arm64: Reallocate the nested_mmus array under the
 mmu_lock
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-04 15:27]** Re: [PATCH] KVM: arm64: Reallocate the nested_mmus array under the
 mmu_lock
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-04 15:58]** Re: [PATCH] KVM: arm64: Reallocate the nested_mmus array under the mmu_lock
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[06-05 14:35]** Re: [PATCH] KVM: arm64: Reallocate the nested_mmus array under the
 mmu_lock
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
5. **[06-05 08:51]** Re: [PATCH] KVM: arm64: Reallocate the nested_mmus array under the mmu_lock
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 11: [PATCH] KVM: arm64: vgic-its: Drop the translation cache reference
 only for the erased entry

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 1 Jun 2026 23:53:26 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-its（虚拟通用中断控制器的中断翻译服务）中，针对翻译缓存的一个补丁。补丁的主要内容是修改 `vgic_its_invalidate_cache()` 函数，以确保在并发情况下仅对被删除的条目减少缓存引用，从而避免潜在的竞态条件。

在历史讨论中，补丁的背景是由于当前实现中，多个上下文可能同时访问同一缓存条目，导致对同一条目的引用计数被多次减少，从而可能在某些情况下导致条目被提前释放。补丁通过确保只有实际删除条目的上下文才会减少缓存引用，解决了这一问题。

在本周的新讨论中，Hyunwoo Kim 提交了补丁并得到了 Oliver Upton 的认可。Oliver 建议在处理无效化时使用 `its_lock` 锁，以进一步消除潜在的竞态条件。经过测试，Hyunwoo 确认了这种方法有效，并计划基于此修复提交补丁的第二版。最终，Oliver 对补丁进行了审核并表示支持。

总结而言，本周讨论集中在补丁的有效性和进一步的改进建议上，参与者积极互动，推动了补丁的完善。

#### 📝 邮件列表

1. **[06-01 23:53]** [PATCH] KVM: arm64: vgic-its: Drop the translation cache reference
 only for the erased entry
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-01 12:08]** Re: [PATCH] KVM: arm64: vgic-its: Drop the translation cache
 reference only for the erased entry
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-02 10:31]** Re: [PATCH] KVM: arm64: vgic-its: Drop the translation cache
 reference only for the erased entry
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
4. **[06-01 22:54]** Re: [PATCH] KVM: arm64: vgic-its: Drop the translation cache
 reference only for the erased entry
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-02 14:26]** Re: [PATCH] KVM: arm64: vgic-its: Drop the translation cache
 reference only for the erased entry
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 12: [PATCH] KVM: arm64: vgic: Use list_del_rcu() when flushing pending
 LPIs

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 5 Jun 2026 06:16:08 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的虚拟化中，如何在刷新待处理的 LPI（Local Peripheral Interrupts）时使用 `list_del_rcu()` 函数。原始的补丁旨在解决在 `vgic_flush_pending_lpis()` 函数中使用 `list_del()` 导致的节点指针损坏问题，从而避免在其他 vCPU 禁用 LPI 时出现不一致的状态。

在之前的讨论中，参与者指出 `vgic_v3_fold_lr_state()` 函数在遍历 `ap_list` 时没有持有 `ap_list_lock`，可能导致在遍历过程中其他路径对 `ap_list` 的修改引发问题。Oliver Upton 提到，仅更改一个写入路径并不能使 `ap_list` 成为 RCU 安全的列表，强调了锁的必要性。

本周的新讨论中，Hyunwoo Kim 和 Marc Zyngier 进一步探讨了使用 `ap_list_lock` 的方法，认为这样可以避免死锁问题，并修复事件通知的锁嵌套问题。Hyunwoo 还提出了对 `vgic_v3_fold_lr_state()` 和 `vgic_v2_fold_lr_state()` 函数的修改建议，以确保在遍历时不会释放节点，增强了整体的安全性和稳定性。

总的来说，本周的讨论集中在如何通过适当的锁机制和 RCU 方法来提高 KVM ARM64 虚拟化的稳定性，确保在处理 LPI 时的安全性和一致性。

#### 📝 邮件列表

1. **[06-05 06:16]** [PATCH] KVM: arm64: vgic: Use list_del_rcu() when flushing pending
 LPIs
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-04 22:47]** Re: [PATCH] KVM: arm64: vgic: Use list_del_rcu() when flushing
 pending LPIs
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-05 09:17]** Re: [PATCH] KVM: arm64: vgic: Use list_del_rcu() when flushing pending LPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-08 07:25]** Re: [PATCH] KVM: arm64: vgic: Use list_del_rcu() when flushing
 pending LPIs
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>

---

### Thread 13: [PATCH] KVM: arm64: nv: Skip vCPUs without a pseudo-TLB in
 invalidate_vncr_va()

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 7 Jun 2026 17:43:53 +0900

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“跳过没有伪 TLB 的 vCPU 在 invalidate_vncr_va() 中的处理”。补丁的主要内容是，在调用 invalidate_vncr_va() 函数时，迭代 vCPU 时需要跳过那些尚未分配伪 TLB 的 vCPU，因为这些 vCPU 的 vncr_tlb 为 NULL。

在历史讨论中，补丁的背景是由于在 vCPU 首次运行前，vncr_tlb 并未分配，因此在处理时需要确保不对未分配的 vCPU 进行操作。补丁通过在迭代过程中添加条件判断来避免对 NULL 指针的解引用，从而修复潜在的错误。

在本周的新讨论中，参与者 Marc Zyngier 对补丁表示认可，并指出该补丁虽然修复了当前问题，但可能错过了处理类似问题的机会。他建议可以引入一个新的宏来更优雅地处理所有有效的 VNCR 伪 TLB。Hyunwoo Kim 也确认了补丁的有效性，并表示将提交这个补丁。最终，Marc Zyngier 和 Hyunwoo Kim 达成一致，Hyunwoo 将负责提交补丁。

#### 📝 邮件列表

1. **[06-07 17:43]** [PATCH] KVM: arm64: nv: Skip vCPUs without a pseudo-TLB in
 invalidate_vncr_va()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-07 14:05]** Re: [PATCH] KVM: arm64: nv: Skip vCPUs without a pseudo-TLB in invalidate_vncr_va()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[06-07 22:36]** Re: [PATCH] KVM: arm64: nv: Skip vCPUs without a pseudo-TLB in
 invalidate_vncr_va()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
4. **[06-07 19:00]** Re: [PATCH] KVM: arm64: nv: Skip vCPUs without a pseudo-TLB in invalidate_vncr_va()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 14: [PATCH] KVM: arm64: Set a linux errno on SMCCC error in kvm_call_hyp_nvhe()

**📧 邮件数**: 4 | **👥 参与者**: 4 | **📅 开始时间**: Wed,  3 Jun 2026 12:03:12 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在处理在 `kvm_call_hyp_nvhe()` 函数中遇到的 SMCCC（Secure Monitor Call Convention）错误。补丁的核心内容是当 HVC（Hypervisor Call）调用失败时，设置一个默认的错误码 `-EPERM`，以确保调用者能够正确接收到错误信息，而不是得到未初始化的返回值。

在之前的讨论中，Vincent Donnefort 提到这个问题在他进行超监视器追踪的后续贡献时导致了内核崩溃，因此他认为这个补丁虽然增强了函数的健壮性，但并不修复现有的具体错误，因此没有添加 "Fixes:" 标签。Fuad Tabba 和 Will Deacon 对补丁进行了审查，Fuad 建议去掉某些代码对齐的修改，以避免影响 `git blame` 的可读性，而 Will 则提出可能使用 `-EOPNOTSUPP` 作为更合适的错误码。

本周的新进展包括对补丁的积极反馈，Fuad 和 Will 都表示支持，并且 Will 提到他已经对补丁进行了修改以反映更合适的错误处理。Marc Zyngier 也表示赞同并进行了相应的调整。整体来看，讨论氛围积极，补丁得到了认可并即将被应用。

#### 📝 邮件列表

1. **[06-03 12:03]** [PATCH] KVM: arm64: Set a linux errno on SMCCC error in kvm_call_hyp_nvhe()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[06-03 12:22]** Re: [PATCH] KVM: arm64: Set a linux errno on SMCCC error in kvm_call_hyp_nvhe()
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-05 12:23]** Re: [PATCH] KVM: arm64: Set a linux errno on SMCCC error in
 kvm_call_hyp_nvhe()
   - 发件人: Will Deacon <will@kernel.org>
4. **[06-07 15:01]** Re: [PATCH] KVM: arm64: Set a linux errno on SMCCC error in kvm_call_hyp_nvhe()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 15: [PATCH v3 0/2] KVM: arm64: Sanitise host vCPU fields copied in flush_hyp_vcpu()

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Sun,  7 Jun 2026 02:56:09 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁系列，主要针对 `flush_hyp_vcpu()` 函数中复制的主机 vCPU 字段进行清理和边界限制。

1. **原始补丁内容**：
   - 补丁系列包括两个主要部分：清除 `__hyp_running_vcpu` 字段和限制 `used_lrs` 字段的值。`flush_hyp_vcpu()` 函数在每次运行时会将主机 vCPU 上下文和 vGIC 状态复制到 hyp 的私有 vCPU 中。当前实现中，这两个字段的复制没有进行适当的清理和限制，可能导致安全性问题。

2. **之前讨论要点**：
   - 在之前的讨论中，参与者提出了对补丁的反馈，建议将补丁分为两个部分以便于审查。补丁的 v2 版本已经根据反馈进行了调整，分为两个独立的补丁。

3. **本周的新讨论与进展**：
   - 本周的讨论中，Hyunwoo Kim 提交了补丁的 v3 版本，详细说明了每个补丁的改动。补丁 1 清除了 `__hyp_running_vcpu` 字段，确保在客人上下文中该字段为 NULL；补丁 2 则在复制后将 `used_lrs` 限制在实现的列表寄存器数量之内。参与者 Fuad Tabba 对该系列补丁表示认可，并进行了测试，给予了审核通过的反馈。

总体来看，此次讨论集中在确保 KVM arm64 实现的安全性和稳定性上，通过清理和限制关键字段，提升了代码的可靠性。

#### 📝 邮件列表

1. **[06-07 02:56]** [PATCH v3 0/2] KVM: arm64: Sanitise host vCPU fields copied in flush_hyp_vcpu()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-07 02:56]** [PATCH v3 1/2] KVM: arm64: Clear __hyp_running_vcpu when flushing the pKVM hyp vCPU
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
3. **[06-07 02:56]** [PATCH v3 2/2] KVM: arm64: Bound used_lrs when flushing the pKVM hyp vCPU
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
4. **[06-07 08:05]** Re: [PATCH v3 0/2] KVM: arm64: Sanitise host vCPU fields copied in flush_hyp_vcpu()
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 16: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before
 migrating it

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 5 Jun 2026 05:59:15 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 的 ARM64 虚拟化中 VGIC（虚拟通用中断控制器）在中断迁移时的处理问题。Hyunwoo Kim 提出的补丁旨在确保在迁移中断之前，检查该中断是否仍然分配给当前的 vCPU。补丁的核心在于修复在迁移过程中可能出现的竞态条件，特别是在释放和重新获取锁的过程中，可能导致中断状态不一致。

在之前的讨论中，参与者们关注到在中断迁移时，VGIC 的处理逻辑可能存在问题，特别是中断可能在锁释放期间被移除，导致后续检查失败。Hyunwoo Kim 提出的补丁通过增加对中断分配状态的检查（即 irq->vcpu == vcpu），来确保只有在中断仍然属于当前 vCPU 时才进行迁移。

本周的讨论中，Oliver Upton 提出了对补丁的进一步思考，询问是否考虑了 vCPU 之间的状态竞争问题，并建议在处理过程中引入 RCU 保护，以避免中断在锁释放和重新获取之间被错误处理。Marc Zyngier 也对此表示关注，讨论了在处理中断迁移时可能出现的状态不一致问题，并建议在删除 LPI（本地中断）时同时使其状态无效。

总体来看，本周的讨论集中在如何增强补丁的鲁棒性和确保中断状态一致性的问题上，参与者们提出了多种建议以改进当前的实现。

#### 📝 邮件列表

1. **[06-05 05:59]** [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before
 migrating it
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-04 23:00]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours
 before migrating it
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-05 08:42]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before migrating it
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-05 01:43]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours
 before migrating it
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 17: [PATCH] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 1 Jun 2026 19:39:54 +0000

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中暴露 PMMIR_EL1.SLOTS 寄存器给客户机的补丁。该补丁旨在解决当前 perf 工具在读取性能监控数据时遇到的问题，特别是当 PMMIR_EL1 被视为只读且返回值为 0 时，导致 perf stat 无法正常工作。

在历史讨论中，补丁的背景是基于之前的提交（46081078feb4），该提交将 PMMIR_EL1 寄存器设置为 RAZ/WI，以防止客户机依赖无法读取的寄存器。补丁通过添加一个 access_pmmir() 处理程序，使客户机能够读取 PMMIR_EL1.SLOTS 字段，同时保持其他字段为 RAZ，以限制信息泄露。

本周的新讨论中，参与者 Oliver Upton 对补丁提出了一些修改建议，认为该补丁不应被视为稳定版本或错误修复，并建议将 PMCEID1 的更改与 PMMIR_EL1 的更改分开处理。同时，他指出不需要某些检查，因为 PMMIR_EL1 在 EL0 状态下是未定义的，用户空间不应触发异常。此外，内核测试机器人报告了构建错误，建议在修复问题时使用单独的补丁。

总体来看，尽管补丁的初衷是改善性能监控的可用性，但仍需进一步讨论和修改以确保兼容性和稳定性。

#### 📝 邮件列表

1. **[06-01 19:39]** [PATCH] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Congkai Tan <congkai@amazon.com>
2. **[06-01 13:06]** Re: [PATCH] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-01 13:13]** Re: [PATCH] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-02 12:14]** Re: [PATCH] KVM: arm64: Expose PMMIR_EL1.SLOTS to guests
   - 发件人: kernel test robot <lkp@intel.com>

---

### Thread 18: [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM guests

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 31 May 2026 16:45:48 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在通过刷新 HCR_EL2.VSE 来将 SError（系统错误）传递给 pKVM（嵌套虚拟化）客户机。

在历史讨论中，Fuad Tabba 提出了这个补丁，指出在启用 pKVM 时，主机通过设置 HCR_EL2.VSE 来注入虚拟 SError，但由于 flush_hyp_vcpu() 仅将 TWI/TWE 流向运行的 hyp vCPU，导致 VSE 无法到达，从而未能传递被延迟的 SError。他建议在进入时进行流动处理，以确保错误能够被正确传递。

在本周的新讨论中，Oliver Upton 对补丁进行了审查并提出了建议，指出 flush_hyp_vcpu() 还应转发 VSESR_EL2。Fuad Tabba 随后询问是否需要重新提交补丁，Oliver 表示目前由 Marc 处理代码树，希望他能将补丁合并。

整体来看，讨论围绕如何确保 SError 能够正确传递给 pKVM 客户机展开，参与者之间的互动表明补丁得到了积极的审查和支持。

#### 📝 邮件列表

1. **[05-31 16:45]** [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM guests
   - 发件人: tabba@google.com
2. **[06-01 12:16]** Re: [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM
 guests
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-01 20:17]** Re: [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM guests
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-01 12:19]** Re: [PATCH] KVM: arm64: Flush HCR_EL2.VSE to deliver SErrors to pKVM
 guests
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 19: [PATCH 0/2] KVM: arm64: Small dirty logging fixes/cleanups

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Fri,  5 Jun 2026 16:32:46 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的两个小型脏页日志修复和清理的补丁。

1. **原始补丁内容**：本次补丁包含两个部分：
   - 第一个补丁替换了 `memslot_is_logging()` 函数为 `kvm_slot_dirty_track_enabled()`，以更准确地检查内存槽是否启用了脏页日志。之前的实现未能考虑脏页环的情况，可能导致脏信息丢失。
   - 第二个补丁则移除了对脏日志启用时的 gfn（Guest Frame Number）对齐操作，因为在启用脏日志时，映射大小已被强制为 PAGE_SIZE。

2. **之前讨论要点**：在历史讨论中，未提及具体的补丁内容，但可以推测出对脏页日志的准确性和性能影响的关注。补丁的提出旨在解决现有实现中的潜在问题，确保在特定情况下不会丢失脏信息。

3. **本周的新讨论与进展**：本周的讨论主要围绕补丁的具体实现细节。Wei-Lin Chang 提到，新的实现方法能够更好地处理内存槽的脏日志状态，并且在性能上不会对实际工作负载产生显著影响。参与者对补丁的必要性和实现逻辑进行了详细说明，并请求反馈以确认其理解的准确性。

总体而言，这些补丁旨在提高 KVM 在 arm64 架构下的脏页日志处理的准确性和效率。

#### 📝 邮件列表

1. **[06-05 16:32]** [PATCH 0/2] KVM: arm64: Small dirty logging fixes/cleanups
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[06-05 16:32]** [PATCH 1/2] KVM: arm64: Replace memslot_is_logging() with kvm_slot_dirty_track_enabled()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[06-05 16:32]** [PATCH 2/2] KVM: arm64: Remove superfluous aligning of gfn for dirty logging
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 20: [PATCH v5 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 26 May 2026 15:19:28 +0000

#### 🤖 AI 总结

本邮件讨论主题为修复 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）中 Endpoint Memory Access Descriptor（EMAD）偏移计算的问题。历史讨论中，Mostafa Saleh 提出了一个包含六个补丁的系列，主要修复了 EMAD 偏移计算，并为核心 FF-A 驱动和 pKVM 虚拟机监控器添加了必要的边界检查。补丁指出，在 FF-A 版本 1.1 之前，内存区域头部未明确指定 EMAD 的偏移量，导致错误假设 EMAD 紧随其后，而从版本 1.1 开始，规范要求使用 `ep_mem_offset` 字段来确定内存访问数组的起始位置。

在本周的新讨论中，Sebastian Ene 对其中一个补丁（补丁 1/6）进行了审查，确认了 Mostafa 提出的 NULL 检查修复，并表示感谢，同时表示已将其其他补丁纳入系列中。Sebastian 的反馈表明该补丁得到了认可，推动了补丁的进一步发展。整体来看，本周讨论的进展主要集中在对补丁的审查和确认上。

#### 📝 邮件列表

1. **[05-26 15:19]** [PATCH v5 0/6] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-26 15:19]** [PATCH v5 1/6] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[06-05 12:01]** Re: [PATCH v5 1/6] optee: ffa: Add NULL check in
 optee_ffa_lend_protmem
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 21: [PATCH v2] KVM/arm64: vgic-its: Make ABI commit helpers return void

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Thu,  4 Jun 2026 15:51:47 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM/arm64 中 vgic-its 的一个补丁，目的是将 ABI 提交助手的返回值类型改为 void。补丁的具体内容是修改 `vgic_its_set_abi()` 和 `vgic_its_commit_v0()` 函数的返回类型，从 int 改为 void，因为这两个函数的返回值总是 0，且并不携带有用的错误信息。

在之前的讨论中，未提及具体的争议或问题，主要是对补丁的必要性进行了简单的说明。

在本周的新讨论中，参与者 Jackie Liu 提交了补丁，并得到了 Eric Auger 和 Oliver Upton 的审核确认，表示支持该补丁的修改。两位审核者均表示感谢，确认了补丁的合理性和必要性。

总结来看，此次补丁旨在简化代码，去除无用的返回值，得到了社区成员的积极反馈。

#### 📝 邮件列表

1. **[06-04 15:51]** [PATCH v2] KVM/arm64: vgic-its: Make ABI commit helpers return void
   - 发件人: Jackie Liu <liu.yun@linux.dev>
2. **[06-04 10:27]** Re: [PATCH v2] KVM/arm64: vgic-its: Make ABI commit helpers return
 void
   - 发件人: Eric Auger <eauger@redhat.com>
3. **[06-04 23:01]** Re: [PATCH v2] KVM/arm64: vgic-its: Make ABI commit helpers return
 void
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 22: [PATCH] KVM: arm64: Sanitise host vCPU fields in flush_hyp_vcpu()

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 4 Jun 2026 20:18:16 +0900

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为「清理 flush_hyp_vcpu() 中的主机 vCPU 字段」。

**原始补丁内容**：
补丁的目的是修复 flush_hyp_vcpu() 函数中对主机 vCPU 上下文和 vGIC 状态的复制，确保在复制后清除 __hyp_running_vcpu 字段并限制 used_lrs 的值，以满足特定的预期条件。

**之前讨论要点**：
本线程没有历史讨论，所有内容均为本周新讨论。

**本周的新讨论与进展**：
1. Hyunwoo Kim 提交了补丁并解释了其必要性，指出 flush_hyp_vcpu() 函数在复制主机 vCPU 字段时没有遵循预期的条件，这可能导致潜在问题。
2. Fuad Tabba 对补丁进行了审查，认为修复是正确的，但建议将补丁拆分为两个独立的补丁，以便更清晰地处理每个字段的修复。Fuad 还建议在提交信息中说明这两个修复都是从主机到 EL2 的。
3. Hyunwoo Kim 同意了 Fuad 的建议，并表示将会将补丁拆分并重新提交。

整体来看，讨论集中在补丁的修复内容及其结构优化上，参与者达成了一致意见，准备进行后续的补丁提交。

#### 📝 邮件列表

1. **[06-04 20:18]** [PATCH] KVM: arm64: Sanitise host vCPU fields in flush_hyp_vcpu()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-04 14:01]** Re: [PATCH] KVM: arm64: Sanitise host vCPU fields in flush_hyp_vcpu()
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-04 22:35]** Re: [PATCH] KVM: arm64: Sanitise host vCPU fields in flush_hyp_vcpu()
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>

---

### Thread 23: [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 21 May 2026 14:49:07 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于为 KVM（Kernel-based Virtual Machine）在 arm64 架构中添加 GICv5 IRS（中断重映射服务）支持的补丁系列。历史讨论中，Sascha Bischoff 提出了一个补丁系列，旨在扩展 KVM 对 GICv5 的支持，使得 GICv5 虚拟机不再局限于使用 PPI（私有中断），而可以使用 SPI（共享中断）和 LPI（本地中断），从而能够在 Arm FVP 模型上启动完整的 Linux 客户机。

在本周的新讨论中，Vladimir Murzin 针对补丁中的一些检查提出了问题。他询问了在不同情况下 `nr_spis`（共享中断数量）为 0 时的潜在影响，以及是否应该将相同的验证逻辑应用于非 GICv5 的情况。此外，他还提到核心已经强制执行 KVM_MAX_IRQ_ROUTES 的限制，质疑是否应该直接拒绝通过 KVM_DEV_ARM_VGIC_GRP_NR_IRQS 提供的 `nr_spis` 值，而不是允许后续进行范围限制。

总体来看，本周的讨论主要集中在补丁逻辑的合理性和潜在的改进建议上。

#### 📝 邮件列表

1. **[05-21 14:49]** [PATCH v2 00/39] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[05-21 14:59]** [PATCH v2 31/39] KVM: arm64: gic-v5: Add GICv5 SPI injection to irqfd
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[06-04 11:51]** Re: [PATCH v2 31/39] KVM: arm64: gic-v5: Add GICv5 SPI injection to
 irqfd
   - 发件人: Vladimir Murzin <vladimir.murzin@arm.com>

---

### Thread 24: [PATCH] KVM/arm64: vgic-its: Fix memory leak when vgic_its_set_abi() fails

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  4 Jun 2026 11:14:26 +0800

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM/arm64 中 vgic-its 组件的一个补丁，旨在修复在 vgic_its_set_abi() 失败时可能导致的内存泄漏问题。

补丁内容：在 vgic_its_create() 函数中，如果 vgic_its_set_abi() 调用失败，之前分配的 'its' 结构体将不会被释放，从而造成内存泄漏。补丁通过在出错时回滚 KVM 状态标志并释放 'its' 结构体来解决这一问题。

历史讨论要点：虽然没有明确的历史讨论，但补丁的背景是与之前的提交（71afe470e20d）相关，该提交引入了迁移 ABI 基础设施。

本周的新讨论中，参与者 Oliver Upton 提出，vgic_its_set_abi() 函数总是成功，因此实际上并不存在内存泄漏问题，他建议去掉返回值。对此，Jackie Liu 表示虽然最初也有类似想法，但保留防御性清理逻辑可以为未来扩展提供便利。他同意 Oliver 的观点，认为去掉返回值是合理且更简洁的做法，并表示将会提交一个新的版本（V2）以反映这一修改。

#### 📝 邮件列表

1. **[06-04 11:14]** [PATCH] KVM/arm64: vgic-its: Fix memory leak when vgic_its_set_abi() fails
   - 发件人: Jackie Liu <liu.yun@linux.dev>
2. **[06-03 23:41]** Re: [PATCH] KVM/arm64: vgic-its: Fix memory leak when
 vgic_its_set_abi() fails
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-04 06:59]** Re: [PATCH] KVM/arm64: vgic-its: Fix memory leak when
 vgic_its_set_abi() fails
   - 发件人: Jackie Liu <liu.yun@linux.dev>

---

### Thread 25: [PATCH] KVM: arm64: Take the SRCU lock for page table walks in fault
 injection and AT emulation

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 3 Jun 2026 01:04:20 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在为故障注入和 AT 仿真中的页表遍历引入 SRCU（Sleepable Read-Copy Update）锁。

原始补丁的内容是，补丁通过在 `inject_abt64()` 和 `__kvm_at_s12()` 函数中添加对 `kvm->srcu` 读锁的获取，确保在进行页表遍历时，能够防止内存槽（memslot）变化带来的问题。这是因为这些函数在执行页表查找时需要读取描述符并更新访问标志，因此必须持有 SRCU 锁。

在之前的讨论中，Hyunwoo Kim 提出了补丁的初衷，并解释了在调用页表遍历函数时未持有 SRCU 锁的潜在风险。Oliver Upton 对补丁进行了审查，建议简化描述，并强调应将关键区间限制在相关的页表遍历调用中。

本周的新讨论中，Hyunwoo Kim 对 Oliver 的反馈表示感谢，并同意调整补丁的方向，计划进行更多测试后提交补丁的第二个版本（v2）。整体来看，讨论围绕如何安全地处理页表遍历中的并发问题展开，确保系统的稳定性和可靠性。

#### 📝 邮件列表

1. **[06-03 01:04]** [PATCH] KVM: arm64: Take the SRCU lock for page table walks in fault
 injection and AT emulation
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-02 23:44]** Re: [PATCH] KVM: arm64: Take the SRCU lock for page table walks in
 fault injection and AT emulation
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-03 20:05]** Re: [PATCH] KVM: arm64: Take the SRCU lock for page table walks in
 fault injection and AT emulation
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>

---

### Thread 26: [PATCH] KVM: arm64: Fix order of arguments to ktime_get_snapshot_id()

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  4 Jun 2026 11:27:13 +0200

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: 修复 ktime_get_snapshot_id() 的参数顺序”，主要讨论了在 KVM 的 arm64 架构中，调用 `ktime_get_snapshot_id()` 函数时参数顺序错误的问题。

在历史讨论中，未提供具体的背景信息，但可以推测该问题源于之前的提交（d09439210441），该提交使用了 `ktime_get_snapshot_id()` 来获取系统启动时间（CLOCK_BOOTTIME），而在调用时参数顺序被错误地反转，导致编译错误。

在本周的新讨论中，Uwe Kleine-König 提出了修复补丁，明确指出应将时钟 ID 作为第一个参数，输出参数作为第二个参数。补丁对 `arch/arm64/kvm/hyp_trace.c` 文件进行了修改，修正了参数顺序。此补丁已被 Thomas Gleixner 确认，并提到他在同一天内已合并了一个相关的修复。

总结来说，本周的讨论集中在修复 KVM arm64 中的一个参数顺序错误，相关补丁已提交并得到确认，表明该问题正在得到解决。

#### 📝 邮件列表

1. **[06-04 11:27]** [PATCH] KVM: arm64: Fix order of arguments to ktime_get_snapshot_id()
   - 发件人: =?UTF-8?q?Uwe=20Kleine-K=C3=B6nig?= <ukleinek@kernel.org>
2. **[06-04 11:49]** Re: [PATCH] KVM: arm64: Fix order of arguments to
 ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>

---

### Thread 27: [PATCH v2] KVM: arm64: Take the SRCU lock for page table walks in
 fault injection and AT emulation

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 3 Jun 2026 21:09:33 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的一个补丁（PATCH v2），旨在解决在故障注入和地址转换（AT）仿真过程中，页面表遍历时未正确获取 SRCU 锁的问题。

补丁的核心内容是，`walk_s1()` 和 `kvm_walk_nested_s2()` 函数在调用时需要持有 `kvm->srcu` 锁，以防止内存插槽的变化。然而，之前的实现中，`__kvm_at_s12()` 和 `__kvm_find_s1_desc_level()` 函数在调用这些遍历函数时并未获取该锁。为了解决这个问题，补丁建议在这两个函数中进行锁的获取。

在之前的讨论中，Hyunwoo Kim 提出了补丁的初步版本，并根据 Oliver Upton 的建议进行了修改，确保在调用遍历函数时使用 `scoped_guard()` 来正确管理锁的获取和释放，并更新了提交信息。

本周的新进展包括 Hyunwoo Kim 提交了补丁的 v2 版本，Oliver Upton 对该补丁进行了审核并表示认可。这表明补丁在社区中得到了积极的反馈，预计将进一步推动其合并进主线代码。

#### 📝 邮件列表

1. **[06-03 21:09]** [PATCH v2] KVM: arm64: Take the SRCU lock for page table walks in
 fault injection and AT emulation
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-03 16:07]** Re: [PATCH v2] KVM: arm64: Take the SRCU lock for page table walks
 in fault injection and AT emulation
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 28: [PATCH v2 0/3] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 29 May 2026 13:17:52 +0100

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于修复 KVM (Kernel-based Virtual Machine) 在 arm64 架构下的共享和取消共享 hypercall 失败时的主机/超管（hyp）跟踪问题。原始的补丁（PATCH v2 0/3）由 tabba 提出，主要针对 `share_pfn_hyp()` 和 `unshare_pfn_hyp()` 函数，这两个函数在处理与 EL2 共享的页面时，未能正确处理 hypercall 失败的情况，导致主机侧的 RB-tree 跟踪节点未能清理。

在历史讨论中，tabba 详细描述了问题的背景，指出在进行 hypercall 时可能出现的失败情况（如页面状态不匹配、EL2 引用计数仍然持有等），并强调了现有代码在失败时的清理不足。

在本周的新讨论中，Vincent Donnefort 对整个补丁系列进行了审查，并表示认可，给予了“Reviewed-by”的标记。这表明该补丁得到了积极的反馈，可能会进一步推进到代码库中。整体来看，本周的讨论进展顺利，补丁得到了审查者的支持。

#### 📝 邮件列表

1. **[05-29 13:17]** [PATCH v2 0/3] KVM: arm64: Fix host/hyp tracking on share/unshare
 hypercall failure
   - 发件人: tabba@google.com
2. **[06-03 11:12]** Re: [PATCH v2 0/3] KVM: arm64: Fix host/hyp tracking on
 share/unshare hypercall failure
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 29: [PATCH v2] KVM: arm64: vgic-its: Serialize translation cache
 invalidation under its_lock

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 2 Jun 2026 16:52:18 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-its（虚拟通用中断控制器）中，针对翻译缓存失效的序列化问题的补丁（PATCH v2）。该补丁旨在确保在其锁（its_lock）下进行翻译缓存失效操作，以避免在并发上下文中对同一缓存条目的引用计数进行多次释放，从而导致潜在的内存错误。

在历史讨论中，补丁的初始版本（v1）未能有效地处理并发访问的问题，导致可能的竞态条件。补丁的作者 Hyunwoo Kim 在 v2 中根据 Oliver Upton 的建议，修改了代码以确保在所有失效操作中持有 its_lock，从而确保每个条目只被单一上下文处理。

在本周的新讨论中，Hyunwoo Kim 提交了补丁 v2，并解释了具体的实现细节和修改内容。Oliver Upton 对此表示感谢，并指出在某些情况下可能会持有 vcpu->mutex，存在排序错误的问题。他提议可以将锁的清理延后作为长期解决方案，并建议回退到 v1 的某些实现，以解决当前问题。

总体而言，本周的讨论集中在补丁的细节和潜在的并发问题上，强调了在多线程环境中对资源管理的谨慎处理。

#### 📝 邮件列表

1. **[06-02 16:52]** [PATCH v2] KVM: arm64: vgic-its: Serialize translation cache
 invalidation under its_lock
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
2. **[06-02 14:26]** Re: [PATCH v2] KVM: arm64: vgic-its: Serialize translation cache
 invalidation under its_lock
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 30: [PATCH] KVM: arm64: nv: Fix handling of XN[0] when !FEAT_XNX

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  2 Jun 2026 00:27:59 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主要目的是修复在不支持 FEAT_XNX 特性的情况下对 XN[0] 的处理问题。补丁的具体内容是修正了在处理 XN[0] 时使用 FIELD_PREP() 函数的错误，导致无条件授予执行权限的情况。修复方法是直接操作正确的位。

在之前的讨论中，补丁的背景是由于先前的提交（d93febe2ed2e）引入了对 FEAT_XNX 权限的转发，但在实现中存在明显的逻辑错误。此补丁通过修改代码，确保在不支持 XNX 的情况下，正确清除 XN[0]。

在本周的新讨论中，Oliver Upton 提出了补丁并进行了详细说明，强调了修复的必要性。Wei-Lin Chang 对该补丁进行了审查，并表示支持，认为使用 0b10 可以稍微改善代码风格一致性。整体来看，本周的讨论集中在补丁的有效性和代码风格的审查上，未出现新的争议或问题。

#### 📝 邮件列表

1. **[06-02 00:27]** [PATCH] KVM: arm64: nv: Fix handling of XN[0] when !FEAT_XNX
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-02 11:05]** Re: [PATCH] KVM: arm64: nv: Fix handling of XN[0] when !FEAT_XNX
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 31: [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 29 May 2026 00:01:44 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM 在 arm64 架构下如何处理 ZCR_EL2.LEN 值的补丁（PATCH v2）。该补丁旨在确保在客人虚拟机写入 ZCR_EL2 时，能够保留所有的 ZCR_EL2.LEN 值，而不是将其限制为最大可配置的向量长度。这一行为与架构文档中对 ZCR_EL2.LEN 的描述不完全一致，文档暗示应按写入值读取。

在历史讨论中，Mark Brown 提出了该补丁的背景，指出自特定提交以来，KVM 对 ZCR_EL2 的处理存在一定的模糊性，可能未能准确反映架构的预期行为。

在本周的新讨论中，Oliver Upton 对补丁表示支持，并确认了之前的讨论内容，表示他同意 Marc 的变更日志建议，并给予了补丁“Reviewed-by”的标记。这表明补丁得到了积极的反馈，可能会在后续版本中被采纳。

#### 📝 邮件列表

1. **[05-29 00:01]** [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[06-01 15:34]** Re: [PATCH v2] KVM: arm64: Preserve all guest ZCR_EL2.LEN values
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 32: [PATCH] KVM: arm64: Add kvm_for_each_vncr_tlb() helper

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun,  7 Jun 2026 18:57:45 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下引入一个新的辅助函数 `kvm_for_each_vncr_tlb()` 的补丁。该补丁旨在解决 VNCR TLB（Translation Lookaside Buffer）失效时可能出现的竞争条件，特别是在 MMU 通知器或 TLBI 指令执行时，可能会与尚未上线的 vcpu 发生冲突（此时未分配伪 TLB）。

在历史讨论中，补丁的背景并未详细说明，但可以推测该问题与之前的补丁有关，特别是修复了一个与 VNCR_EL2 相关的 TLB 失效原语的缺陷（Fixes: 4ffa72ad8f37）。补丁通过引入一个新的迭代器，确保在进行 TLB 失效时检查 vcpu 是否有效，并避免在无效情况下进行失效操作。

本周的讨论中，Marc Zyngier 提出了补丁的具体实现，详细描述了新迭代器的功能和目的，并修改了相关代码以使用该迭代器。补丁的实现包括对 `kvm_invalidate_vncr_ipa()` 和 `invalidate_vncr_va()` 函数的更新，以确保在 TLB 失效时只处理有效的 vcpu。这一改动旨在提高 KVM 的稳定性和性能，避免潜在的错误。

#### 📝 邮件列表

1. **[06-07 18:57]** [PATCH] KVM: arm64: Add kvm_for_each_vncr_tlb() helper
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 33: [PATCH 6.18 000/315] 6.18.35-rc1 review

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun,  7 Jun 2026 19:04:40 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于 Linux 内核 6.18.35-rc1 的审查，主要集中在对 ARM64 架构的 KVM（虚拟机监控器）相关代码的测试和问题反馈。

在本周的讨论中，参与者 Miguel Ojeda 提到他在 QEMU 环境下对 Rust x86_64、arm64 和 riscv64 进行了启动测试，并对 loongarch64 进行了构建测试，结果显示 arm32 构建正常。然而，在 arm64 的测试中，他发现了几个未声明标识符 `resx` 的错误，这些错误出现在 `arch/arm64/kvm/nested.c` 文件中。根据他分析，这些问题是由于之前的提交（commit 10206eaad1b9）引入的更改导致的，而 `resx` 结构体是由后续的提交（0879478913dd 等）引入的，这些提交在 7.0 版本中。因此，他建议要么进行有针对性的回溯，要么回溯一些相关的提交，以解决当前的问题。

总结来说，本周的讨论主要集中在对 ARM64 KVM 代码的错误反馈及其可能的解决方案上，显示出在新版本审查过程中遇到的兼容性问题。

#### 📝 邮件列表

1. **[06-07 19:04]** Re: [PATCH 6.18 000/315] 6.18.35-rc1 review
   - 发件人: Miguel Ojeda <ojeda@kernel.org>

---

### Thread 34: [PATCH] KVM: arm64: Fix block mapping validity check in stage-1 walker

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri,  5 Jun 2026 19:52:55 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: 修复阶段1 walker 中的块映射有效性检查”，由 Wei-Lin Chang 提交。该补丁旨在修复在处理 64K 粒度大小时，FEAT_LPA（大物理地址扩展）对一级映射的有效性检查。之前的实现过于严格，使用了 has_52bit_pa() 的结果，这也检查了 TCR 中选择的输出地址大小。补丁通过仅检查 FEAT_LPA 来简化这一过程。

在历史讨论中，没有提供具体的上下文或先前的讨论内容，因此我们无法得知该补丁的背景信息。

在本周的新讨论中，Wei-Lin Chang 提交了该补丁，并详细说明了修复的内容和原因。补丁修改了 `arch/arm64/kvm/at.c` 文件，增加了对 64K 粒度的有效性检查逻辑，以确保在满足 FEAT_LPA 的情况下，级别1的映射是有效的。此补丁为 KVM 的 arm64 架构提供了更好的兼容性和灵活性。

#### 📝 邮件列表

1. **[06-05 19:52]** [PATCH] KVM: arm64: Fix block mapping validity check in stage-1 walker
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 35: [PATCH v2] KVM: arm64: Reassign nested_mmus array behind mmu_lock

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 5 Jun 2026 17:27:01 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，主要涉及对 `nested_mmus` 数组的重新分配，以确保在多线程环境下的安全性。

### 原始补丁内容
补丁的目的是在持有 `mmu_lock` 时重新分配 `kvm->arch.nested_mmus[]` 数组。当前实现中，`kvm_vcpu_init_nested()` 函数在仅持有 `config_lock` 的情况下重新分配数组并释放旧的缓冲区，这可能导致在 `mmu_lock` 被持有时，其他线程访问已释放的数组。

### 之前讨论要点
在历史讨论中，补丁的背景是为了修复在多线程环境中可能出现的竞态条件，确保在重新分配 `nested_mmus` 数组时不会导致内存访问错误。

### 本周新讨论与进展
本周的讨论中，Hyunwoo Kim 提交了补丁的第二版，主要修改了补丁的短日志和变更日志，以回应审查意见。补丁的核心逻辑保持不变，仍然是在 `mmu_lock` 下进行数组的复制和重新分配，确保在分配新数组时不会阻塞。补丁得到了 Oliver Upton 的审查确认，显示出社区对该补丁的认可。

总体来看，此次讨论聚焦于提升 KVM 在 arm64 架构下的稳定性和安全性，确保在并发环境中对内存的安全管理。

#### 📝 邮件列表

1. **[06-05 17:27]** [PATCH v2] KVM: arm64: Reassign nested_mmus array behind mmu_lock
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>

---

### Thread 36: [PATCH v1] KVM: arm64: Restore POR_EL0 access to host EL0

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu,  4 Jun 2026 11:54:34 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在恢复对主机 EL0 的 POR_EL0 访问。

1. **原始 patch/问题的内容**：
   本次补丁由 Joey Gouly 提出，主要解决了一个问题：在函数 `__deactivate_cptr_traps_vhe()` 中，CPTR_EL2.E0POE 被清除，导致从主机 EL0 访问 POR_EL0 时会触发异常，并向用户空间报告为非法指令。这种情况在运行任何虚拟机后都会发生，无论该虚拟机是否使用 POE（Privilege Override Enable）。

2. **之前的讨论要点**：
   由于本邮件列表中没有历史讨论部分，因此没有相关的背景信息或之前的讨论要点。

3. **本周的新讨论、进展或结论**：
   本周的讨论中，Joey Gouly 提交了补丁，并进行了测试，结果显示在执行 `read_por_el0` 和运行 KVM 单元测试时，访问 POR_EL0 仍然会返回“非法指令”错误。补丁中增加了对 CPACR_EL1_E0POE 的设置，以恢复对 POR_EL0 的访问。补丁已包含在代码中，并对相关文件进行了修改，具体为在 `switch.h` 文件中新增了两行代码。

总体来看，此补丁的提出是为了修复 KVM 在 arm64 架构下的一个关键访问问题，确保主机 EL0 能够正确访问 POR_EL0。

#### 📝 邮件列表

1. **[06-04 11:54]** [PATCH v1] KVM: arm64: Restore POR_EL0 access to host EL0
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 37: [PATCH] KVM: arm64: Drop pointless check for EL0 access to PMINTEN*_EL1

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon,  1 Jun 2026 13:24:56 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中对 PMINTEN*_EL1 寄存器的访问检查的优化。原始的 patch 提出了删除对 EL0 访问 PMINTEN*_EL1 寄存器的无意义检查，因为这些寄存器在 EL0 状态下是未定义的，KVM 不应从来宾的 EL0 状态捕获到此类异常。

在之前的讨论中，虽然没有具体的历史邮件记录，但可以推测出参与者对现有代码中对 EL0 访问的检查表示了疑虑，认为这些检查是多余的，可能导致不必要的复杂性。

在本周的新讨论中，Oliver Upton 提出了具体的代码修改，重构了相关的检查函数，并将其重新命名为更具描述性的名称，以提高代码的可读性和维护性。此次修改涉及到对多个函数的更新，减少了冗余代码，并确保了在 EL0 状态下的访问处理逻辑更加清晰。整体来看，此次 patch 旨在简化 KVM 的实现，同时保持系统的正确性。

#### 📝 邮件列表

1. **[06-01 13:24]** [PATCH] KVM: arm64: Drop pointless check for EL0 access to PMINTEN*_EL1
   - 发件人: Oliver Upton <oupton@kernel.org>

---

## 📌 RFC

共 2 个 thread

---

### Thread 1: [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on KVM

**📧 邮件数**: 30 | **👥 参与者**: 1 | **📅 开始时间**: Fri,  5 Jun 2026 08:33:29 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 上 Arm64 的命名 CPU 模型支持的 RFC PATCH v2，主要内容包括以下几个方面：

1. **原始 Patch/问题内容**：
   提出的补丁旨在为 KVM 上的 Arm64 提供命名 CPU 模型支持，以解决当前 QEMU 仅支持 `-cpu host/max` 的问题，导致不同 CPU 特性之间的虚拟机无法进行实时迁移。该补丁设计了一个分层的命名模型结构，允许用户自定义 CPU 特性，并通过 QMP 命令查询主机支持的模型和特性。

2. **之前讨论要点**：
   在之前的讨论中，补丁系列的 v1 版本提出了基本的设计思路，讨论了如何实现 CPU 特性层的结构和 QMP 命令的设计。参与者们关注了如何确保模型的向后兼容性，以及如何处理与现有可定制主机模型系列的重叠。

3. **本周的新讨论和进展**：
   本周的讨论集中在补丁的具体实现细节上，包括对 ID 寄存器的处理、特性验证、以及如何在 KVM 中写回修改后的 ID 寄存器。新增了对缓存信息的支持，定义了复合属性类型以简化多个子属性的管理。此外，讨论还涉及了如何在 QMP 中添加新的命令以查询 CPU 属性信息，以及如何处理与 KVM 的交互，确保在不同主机间迁移时的兼容性。

总的来说，本次讨论强调了命名 CPU 模型的实现细节和与 KVM 的集成，确保了对 CPU 特性的灵活管理和更好的虚拟化支持。

#### 📝 邮件列表

1. **[06-05 08:33]** [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
2. **[06-05 08:33]** [RFC PATCH v2 01/29] target/arm: named_cpu_model: define containers for ID registers and fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
3. **[06-05 08:33]** [RFC PATCH v2 02/29] target/arm: Add ID Register field descriptions in cpu-idregs.h.inc
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
4. **[06-05 08:33]** [RFC PATCH v2 03/29] target/arm: Add MIDR, REVIDR, AIDR and extra ID regs to cpu-sysregs
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
5. **[06-05 08:33]** [RFC PATCH v2 04/29] target/arm: Generate ARM64 ID registers and field tables
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
6. **[06-05 08:33]** [RFC PATCH v2 05/29] target/arm: Replace FIELD() macros with IDREG_FIELD expansion
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
7. **[06-05 08:33]** [RFC PATCH v2 06/29] target/arm: Introduce data-structures for the ARM property layer
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
8. **[06-05 08:33]** [RFC PATCH v2 07/29] target/arm: Define ARM properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
9. **[06-05 08:33]** [RFC PATCH v2 08/29] target/arm: Add ID register field helper functions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
10. **[06-05 08:33]** [RFC PATCH v2 09/29] target/arm: Add all ARM64 properties to host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
11. **[06-05 08:33]** [RFC PATCH v2 10/29] target/arm: Add named cpu model infra + graviton3 named model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
12. **[06-05 08:33]** [RFC PATCH v2 11/29] target/arm: Add Nvidia Grace named model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
13. **[06-05 08:33]** [RFC PATCH v2 12/29] target/arm/kvm: Writeback modified ID registers to KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
14. **[06-05 08:33]** [RFC PATCH v2 13/29] target/arm/kvm: enable writable implementation ID registers
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
15. **[06-05 08:33]** [RFC PATCH v2 14/29] target/arm: Validate cpu->isar.idregs[] before writeback
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
16. **[06-05 08:33]** [RFC PATCH v2 15/29] target/arm/kvm: handle DCZID_EL0 specially
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
17. **[06-05 08:33]** [RFC PATCH v2 16/29] target/arm: skip GIC, COPDBG and PMU fields during KVM writeback
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
18. **[06-05 08:33]** [RFC PATCH v2 17/29] target/arm: Add composite property type to model definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
19. **[06-05 08:33]** [RFC PATCH v2 18/29] target/arm: define pauth composite property
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[06-05 08:33]** [RFC PATCH v2 19/29] target/arm: define sve composite property
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
21. **[06-05 08:33]** [RFC PATCH v2 20/29] target/arm: Introduce stub files required for qmp support
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[06-05 08:33]** [RFC PATCH v2 21/29] target/arm/qmp: add named models and properties to cpu-model-expansion
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
23. **[06-05 08:33]** [RFC PATCH v2 22/29] target/arm/kvm: introduce kvm_arm_get_host_isar helper
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[06-05 08:33]** [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
25. **[06-05 08:33]** [RFC PATCH v2 24/29] target/arm: Report "off" for ID fields gated by vCPU init flags
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
26. **[06-05 08:33]** [RFC PATCH v2 25/29] target/arm/qmp: hook blockers in query-cpu-definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
27. **[06-05 08:33]** [RFC PATCH v2 26/29] target/arm: Support exposing cache information for named cpu models
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
28. **[06-05 08:33]** [RFC PATCH v2 27/29] target/arm: Provide default cache hierarchy
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
29. **[06-05 08:33]** [RFC PATCH v2 28/29] target/arm: supported-values and blockers for CCSIDR cache properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
30. **[06-05 08:33]** [RFC PATCH v2 29/29] target/arm/kvm: fix host model writeback when kernel supports EL2
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 2: [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback and
 IDE stream allocation support

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 27 May 2026 22:47:29 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个名为“[RFC PATCH v4 01/14] coco: host: arm64: 添加主机 TSM 回调和 IDE 流分配支持”的补丁。该补丁的主要目的是为 PCI-TSM 提供基础设施和框架，后续将涉及 IDE 密钥管理等更复杂的功能。

在历史讨论中，Dan Williams 提出了对补丁的反馈，强调该补丁作为基础设施补丁的重要性，并建议在提交信息中更清晰地说明补丁的背景。此外，他还询问是否可以将补丁中的某些部分拆分，以便使其在 CCA 系列中独立存在。

在本周的新讨论中，Aneesh Kumar K.V 对 Dan 的建议做出了积极回应，表示将更新提交信息并将补丁拆分为独立部分。他还确认将在最终补丁中调用 tsm_register()，并表示会根据之前的讨论进行相应的更新。这表明该补丁正在朝着更清晰和结构化的方向发展。

#### 📝 邮件列表

1. **[05-27 22:47]** Re: [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback and
 IDE stream allocation support
   - 发件人: Dan Williams (nvidia) <djbw@kernel.org>
2. **[06-02 14:12]** Re: [RFC PATCH v4 01/14] coco: host: arm64: Add host TSM callback
 and IDE stream allocation support
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

## 📌 Bug Report

共 1 个 thread

---

### Thread 1: [syzbot] [kvmarm?] [kvm?] BUG: unable to handle kernel paging
 request in kvm_vgic_destroy

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 4 Jun 2026 16:47:36 +0200

#### 🤖 AI 总结

本邮件主题为“[syzbot] [kvmarm?] [kvm?] BUG: unable to handle kernel paging request in kvm_vgic_destroy”，主要讨论了在 KVM（Kernel-based Virtual Machine）环境下出现的内核分页请求处理错误。

在本周的新讨论中，参与者 Dmitry Vyukov 提到，Marc Zyngier 已经在 GitHub 上提交了一个相关的问题报告（issue #7450），以便进一步跟踪和解决该错误。邮件中并未提供关于此问题的详细技术背景或之前的讨论内容，显示出这是一个新的问题报告，尚未有深入的历史讨论。

总结来说，本周的讨论主要集中在 KVM 环境下的一个内核错误上，相关问题已被记录并提交至 GitHub，以便开发者们进行后续的分析和修复。

#### 📝 邮件列表

1. **[06-04 16:47]** Re: [syzbot] [kvmarm?] [kvm?] BUG: unable to handle kernel paging
 request in kvm_vgic_destroy
   - 发件人: Dmitry Vyukov <dvyukov@google.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #5

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  5 Jun 2026 17:45:16 +0100

#### 🤖 AI 总结

本邮件讨论主题为 KVM/arm64 在 7.1 版本中的修复，Marc Zyngier 提交了一系列补丁以解决发现的多个问题。

1. **原始 patch/问题的内容**：本次补丁主要针对 KVM/arm64 的多个架构性和用户空间的错误，包括修复 ITS 翻译缓存引用、SW 页表遍历时的 SRCU 锁定、恢复 POR_EL0 访问权限、确保 vcpu 初始化与 MMU 通知器互斥等问题。

2. **之前讨论要点**：在历史讨论中，Marc 提到上周的拉取请求是最后一次，但由于持续发现问题，决定再次提交修复补丁。补丁中涉及的错误包括竞争条件、用户空间破坏和架构性缺陷。

3. **本周的新讨论、进展或结论**：本周，Marc Zyngier 提交了新的拉取请求，详细列出了修复内容，并请求 Paolo Bonzini 进行合并。Paolo 对此表示感谢并确认已成功合并这些修复。此次补丁的合并将有助于提升 KVM/arm64 的稳定性和性能。

#### 📝 邮件列表

1. **[06-05 17:45]** [GIT PULL] KVM/arm64 fixes for 7.1, take #5
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[06-05 18:57]** Re: [GIT PULL] KVM/arm64 fixes for 7.1, take #5
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality

**📧 邮件数**: 10 | **👥 参与者**: 6 | **📅 开始时间**: Fri, 29 May 2026 21:59:47 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于扩展时间keeping和PTP（精确时间协议）快照功能的补丁（patch V2 00/25）。该补丁旨在提供捕获的CLOCK*值及其底层时钟源计数器值，以增强PTP的快照功能。

在历史讨论中，Thomas Gleixner 提出了补丁的更新版本，并详细描述了如何捕获这些值以及为驱动程序开发者提供核心基础设施的相关讨论。补丁中涉及的多个具体修改，如将 PPS 转换为 `ktime_get_snapshot_id()`，以及使用提供的时钟 ID 进行历史快照等，均未引入功能变化。

在本周的新讨论中，Michael S. Tsirkin 对补丁表示认可。Rodolfo Giometti 提出了对补丁构建失败的担忧，David Woodhouse 建议删除 `struct pps_event_time`，并提出在 `system_time_snapshot` 中添加 `ntp_error` 字段，以解决 NOHZ 模式下的时钟抖动问题。Peter Hilber 和 Takashi Iwai 也对其他补丁部分表示认可。

总体来看，本周的讨论集中在补丁的具体实现细节及其潜在影响上，参与者们积极反馈并提出改进建议。

#### 📝 邮件列表

1. **[05-29 21:59]** [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Thomas Gleixner <tglx@kernel.org>
2. **[05-29 22:00]** [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
3. **[05-29 22:00]** [patch V2 16/25] virtio_rtc: Use provided clock ID for history
 snapshot
   - 发件人: Thomas Gleixner <tglx@kernel.org>
4. **[05-29 22:01]** [patch V2 21/25] ALSA: hda/common: Use
 system_device_crosststamp::sys_systime
   - 发件人: Thomas Gleixner <tglx@kernel.org>
5. **[05-30 13:08]** Re: [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Rodolfo Giometti <giometti@enneenne.com>
6. **[06-01 06:59]** Re: [patch V2 00/25] timekeeping/ptp: Expand snapshot functionality
   - 发件人: Michael S. Tsirkin <mst@redhat.com>
7. **[06-02 11:31]** Re: [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: Thomas Gleixner <tglx@kernel.org>
8. **[06-02 11:56]** Re: [patch V2 04/25] pps: Convert to ktime_get_snapshot_id()
   - 发件人: David Woodhouse <dwmw2@infradead.org>
9. **[06-02 16:44]** Re: [patch V2 16/25] virtio_rtc: Use provided clock ID for history
 snapshot
   - 发件人: Peter Hilber <peter.hilber@oss.qualcomm.com>
10. **[06-02 19:46]** Re: [patch V2 21/25] ALSA: hda/common: Use system_device_crosststamp::sys_systime
   - 发件人: Takashi Iwai <tiwai@suse.de>

---

