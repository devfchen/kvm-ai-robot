# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-04-27 00:41:38

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 208
- **总 Thread 数**: 27
- **大型 Thread** (>20封): 3 个

### 分类分布

- **PATCH**: 21 threads (121 邮件)
- **RFC**: 3 threads (81 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Other**: 2 threads (5 邮件)

---

## 📌 PATCH

共 21 个 thread

---

### Thread 1: [PATCH v3 00/19] KVM: selftests: Use kernel-style integer and
 g[vp]a_t types

**📧 邮件数**: 21 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 20 Apr 2026 14:19:45 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 286329 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:21, 235815 tokens)

#### 📝 邮件列表

1. **[04-20 14:19]** [PATCH v3 00/19] KVM: selftests: Use kernel-style integer and
 g[vp]a_t types
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[04-20 14:19]** [PATCH v3 01/19] KVM: selftests: Use gva_t instead of vm_vaddr_t
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[04-20 14:19]** [PATCH v3 02/19] KVM: selftests: Use gpa_t instead of vm_paddr_t
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[04-20 14:19]** [PATCH v3 03/19] KVM: selftests: Use gpa_t for GPAs in Hyper-V selftests
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[04-20 14:19]** [PATCH v3 04/19] KVM: selftests: Use u64 instead of uint64_t
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[04-20 14:19]** [PATCH v3 05/19] KVM: selftests: Use s64 instead of int64_t
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[04-20 14:19]** [PATCH v3 06/19] KVM: selftests: Use u32 instead of uint32_t
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[04-20 14:19]** [PATCH v3 07/19] KVM: selftests: Use s32 instead of int32_t
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[04-20 14:19]** [PATCH v3 08/19] KVM: selftests: Use u16 instead of uint16_t
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[04-20 14:19]** [PATCH v3 09/19] KVM: selftests: Use s16 instead of int16_t
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[04-20 14:19]** [PATCH v3 10/19] KVM: selftests: Use u8 instead of uint8_t
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[04-20 14:19]** [PATCH v3 11/19] KVM: selftests: Drop "vaddr_" from APIs that
 allocate memory for a given VM
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[04-20 14:19]** [PATCH v3 12/19] KVM: selftests: Rename vm_vaddr_unused_gap() => vm_unused_gva_gap()
   - 发件人: Sean Christopherson <seanjc@google.com>
14. **[04-20 14:19]** [PATCH v3 13/19] KVM: selftests: Rename vm_vaddr_populate_bitmap() => vm_populate_gva_bitmap()
   - 发件人: Sean Christopherson <seanjc@google.com>
15. **[04-20 14:19]** [PATCH v3 14/19] KVM: selftests: Rename translate_to_host_paddr() => translate_hva_to_hpa()
   - 发件人: Sean Christopherson <seanjc@google.com>
16. **[04-20 14:20]** [PATCH v3 15/19] KVM: selftests: Clarify that arm64's inject_uer()
 takes a host PA, not a guest PA
   - 发件人: Sean Christopherson <seanjc@google.com>
17. **[04-20 14:20]** [PATCH v3 16/19] KVM: selftests: Replace "vaddr" with "gva" throughout
   - 发件人: Sean Christopherson <seanjc@google.com>
18. **[04-20 14:20]** [PATCH v3 17/19] KVM: selftests: Replace "u64 gpa" with "gpa_t" throughout
   - 发件人: Sean Christopherson <seanjc@google.com>
19. **[04-20 14:20]** [PATCH v3 18/19] KVM: selftests: Replace "u64 nested_paddr" with
 "gpa_t l2_gpa"
   - 发件人: Sean Christopherson <seanjc@google.com>
20. **[04-20 14:20]** [PATCH v3 19/19] KVM: selftests: Replace "paddr" with "gpa" throughout
   - 发件人: Sean Christopherson <seanjc@google.com>
21. **[04-23 11:34]** Re: [PATCH v3 00/19] KVM: selftests: Use kernel-style integer and
 g[vp]a_t types
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 2: [PATCH v7 0/4] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 16 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 18 Apr 2026 17:14:22 +0900

#### 🤖 AI 总结

本邮件线程讨论的主题是关于KVM在arm64架构下的性能监控单元（PMU）支持的补丁系列，主要涉及如何在异构系统中使用多个主机PMU。

**原始补丁内容**：
Akihiko Odaki提出了四个补丁，旨在解决KVM PMU仿真依赖单一主机PMU实例的问题。当前的实现导致当vCPU迁移到具有不兼容PMU的pCPU时，计数器停止递增，这在Windows系统中可能导致崩溃。补丁包括添加计数器掩码函数、保护PMU列表的RCU机制、引入固定计数器功能等。

**之前讨论要点**：
在历史讨论中，Marc Zyngier对补丁的描述和实现细节提出了建议，强调需要更清晰的实现说明和对潜在问题的考虑。同时，讨论了RCU保护机制的使用和可能的竞态条件。

**本周新讨论进展**：
本周的讨论集中在补丁的具体实现和文档改进上。Akihiko Odaki同意Marc Zyngier的建议，计划在下一个版本中更新补丁信息，确保互斥条件的实现，并对补丁的功能和复杂性进行更清晰的阐述。此外，双方讨论了如何处理PMU的选择和文档与实现之间的不一致性，确保代码的可维护性和一致性。整体来看，讨论推动了补丁的完善，增强了KVM对异构系统的支持能力。

#### 📝 邮件列表

1. **[04-18 17:14]** [PATCH v7 0/4] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[04-18 17:14]** [PATCH v7 1/4] KVM: arm64: PMU: Add kvm_pmu_enabled_counter_mask()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[04-18 17:14]** [PATCH v7 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[04-18 17:14]** [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[04-19 15:13]** Re: [PATCH v7 1/4] KVM: arm64: PMU: Add kvm_pmu_enabled_counter_mask()
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-19 15:34]** Re: [PATCH v7 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[04-19 18:19]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[04-20 14:27]** Re: [PATCH v7 1/4] KVM: arm64: PMU: Add
 kvm_pmu_enabled_counter_mask()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[04-20 15:21]** Re: [PATCH v7 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
10. **[04-20 08:01]** Re: [PATCH v7 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[04-20 16:17]** Re: [PATCH v7 2/4] KVM: arm64: PMU: Protect the list of PMUs with RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
12. **[04-20 17:36]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
13. **[04-20 10:51]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[04-20 21:07]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
15. **[04-20 14:53]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[04-22 16:02]** Re: [PATCH v7 3/4] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 3: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd

**📧 邮件数**: 10 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 10 Apr 2026 15:17:47 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于为 `guest_memfd` 提供直接映射移除支持的补丁（PATCH v12 00/16）。该补丁的主要目的是通过从主机内核的直接映射中解除虚拟机来宾内存的映射，以减轻类似 Spectre 的瞬态执行问题。

在历史讨论中，Nikita Kalyazin 提出了多个补丁，主要集中在如何有效地处理直接映射的解除和相关的内存管理功能。例如，补丁中引入了 `GUEST_MEMFD_FLAG_NO_DIRECT_MAP` 标志，以确保在准备后从直接映射中移除 `guest_memfd` 页框。

本周的新讨论中，参与者们关注补丁的合并过程和代码的清晰性。Lorenzo Stoakes 建议在合并时应将内存管理（mm）相关的更改通过 mm 树进行处理，以避免冲突。Sean Christopherson 则对当前的补丁提出了疑虑，认为将 `guest_memfd` 负责直接映射的管理可能导致不一致的使用规则，并建议在更高层次上自动处理直接映射的添加和移除，以简化 ABI（应用程序二进制接口）。

总体来看，讨论集中在补丁的实现细节、合并策略及其对内存管理的影响上，参与者们希望在确保性能的同时，保持代码的可维护性和一致性。

#### 📝 邮件列表

1. **[04-10 15:17]** [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
2. **[04-10 15:17]** [PATCH v12 01/16] set_memory: set_direct_map_* to take address
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
3. **[04-10 15:19]** [PATCH v12 09/16] KVM: arm64: define
 kvm_arch_gmem_supports_no_direct_map()
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
4. **[04-10 15:19]** [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from direct
 map
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
5. **[04-21 14:40]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Lorenzo Stoakes <ljs@kernel.org>
6. **[04-21 15:43]** Re: [PATCH v12 01/16] set_memory: set_direct_map_* to take address
   - 发件人: Lorenzo Stoakes <ljs@kernel.org>
7. **[04-21 09:31]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[04-21 09:36]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[04-21 17:55]** Re: [PATCH v12 09/16] KVM: arm64: define kvm_arch_gmem_supports_no_direct_map()
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[04-21 10:08]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Frank van der Linden <fvdl@google.com>

---

### Thread 4: [PATCH 0/6] KVM: arm64: pKVM init and feature detection fixes

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 24 Apr 2026 09:49:02 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM 初始化和特性检测的修复。Fuad Tabba 提出了六个独立的补丁，旨在解决之前讨论中提到的一些正确性问题，以确保在后续的 pKVM 基础设施系列中，vCPU 状态管理能够顺利进行。

在历史讨论中，补丁的主要内容包括修复特性检测的错误，例如 FEAT_Debugv8p9 和 FEAT_SPE_FnE 的检测逻辑不当，以及修复 vCPU 和 hypervisor 初始化路径中的一些潜在错误。这些修复确保了 KVM 在处理特定硬件特性时的正确性，避免了潜在的崩溃和资源泄漏。

本周的新讨论中，Fuad 提交的六个补丁得到了积极的反馈，Marc Zyngier 表示已将这些补丁应用到修复列表中，并标记为稳定版本，除了第二个补丁（注释中的拼写错误修复）外。所有补丁都已被接受并合并，确保了 KVM 的稳定性和功能的正确性。

#### 📝 邮件列表

1. **[04-24 09:49]** [PATCH 0/6] KVM: arm64: pKVM init and feature detection fixes
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[04-24 09:49]** [PATCH 1/6] KVM: arm64: Fix FEAT_Debugv8p9 to check DebugVer, not PMUVer
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[04-24 09:49]** [PATCH 2/6] KVM: arm64: Fix typo in feature check comments
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[04-24 09:49]** [PATCH 3/6] KVM: arm64: Fix FEAT_SPE_FnE to use PMSIDR_EL1.FnE, not PMSVer
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[04-24 09:49]** [PATCH 4/6] KVM: arm64: Fix kvm_vcpu_initialized() macro parameter
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[04-24 09:49]** [PATCH 5/6] KVM: arm64: Fix pin leak and publication ordering in __pkvm_init_vcpu()
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[04-24 09:49]** [PATCH 6/6] KVM: arm64: Fix initialisation order in __pkvm_init_finalise()
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[04-24 12:02]** Re: [PATCH 0/6] KVM: arm64: pKVM init and feature detection fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[04-24 12:08]** Re: [PATCH 0/6] KVM: arm64: pKVM init and feature detection fixes
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 5: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 22 Apr 2026 10:25:40 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM 的 arm64 架构中 FF-A 内存访问描述符放置的验证，相关的补丁（patch）旨在防止 pKVM 虚拟机监控程序对内存访问描述符（EMAD）位置的错误假设。补丁要求在验证 FF-A 内存借用/共享事务时，严格规定 EMAD 的放置位置，确保其紧跟在内存区域头部之后。

在历史讨论中，参与者们探讨了补丁的合理性，Marc Zyngier 提出，当前的实现可能违反了 FF-A 规范，因为规范允许在头部和 EMAD 之间存在间隙。Sebastian Ene 则指出，尽管规范允许间隙，但 arm ff-a 驱动程序在实现中选择了固定位置，这可能导致安全隐患。

本周的新讨论中，参与者们围绕补丁的合理性和实现细节展开了深入交流。Marc Zyngier 认为，强制固定偏移可能会限制实现的灵活性，而 Sebastian Ene 则强调，当前实现是为了防止潜在的安全风险，认为不应轻易假设主机是可信的。最终，讨论达成共识，可能需要对 `ffa_mem_desc_offset` 函数进行修改，以使用 `ep_mem_offset` 进行验证，而不是简单地依赖固定的结构体大小。整体来看，讨论推动了对补丁的理解和可能的改进方向。

#### 📝 邮件列表

1. **[04-22 10:25]** [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[04-22 13:24]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-22 13:35]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[04-22 20:17]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
5. **[04-22 20:29]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
6. **[04-23 09:08]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor placement
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[04-23 09:17]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[04-23 09:29]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[04-23 10:55]** Re: [PATCH] KVM: arm64: Validate the FF-A memory access descriptor
 placement
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 6: [PATCH 00/18] KVM: arm64: Second batch of vgic fixes for 7.1

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 15 Apr 2026 12:55:41 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM arm64 的第二批 vgic 修复补丁，主要集中在 GICv5 的改进上。

1. **原始 patch/问题的内容**：Marc Zyngier 提出的补丁系列（共18个）旨在提升 GICv5 的正确性和可维护性，特别是与 v3 版本的定时器相关的更改，以及 GICv5 主驱动程序的调整。这些补丁主要解决了 vgic-v5 中 struct irq_ops 的使用问题，并增加了缺失的 GIC CDEN 指令到自测中。

2. **之前讨论要点**：在历史讨论中，Marc 提出了多个补丁，强调了对 irq_ops 的 constify 处理和私有中断分配函数的合并，以消除重复代码并提高代码的整洁性。补丁的目标是确保 GICv5 的实现与 GICv3 保持一致，并增强自测的完整性。

3. **本周的新讨论、进展或结论**：在本周的讨论中，参与者 Joey Gouly 对 Marc 提出的补丁进行了审核，确认了补丁的有效性并给予了“Reviewed-by”标记。这表明补丁得到了认可，且在代码审查中没有问题，进一步推动了补丁的合并进程。

总的来说，本周的讨论表明补丁在审核中进展顺利，为后续的合并奠定了基础。

#### 📝 邮件列表

1. **[04-15 12:55]** [PATCH 00/18] KVM: arm64: Second batch of vgic fixes for 7.1
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-15 12:55]** [PATCH 05/18] KVM: arm64: vgic: Constify struct irq_ops usage
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-15 12:55]** [PATCH 06/18] KVM: arm64: vgic: Consolidate vgic_allocate_private_irqs_locked()
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-15 12:55]** [PATCH 12/18] KVM: arm64: selftests: Add missing GIC CDEN to no-vgic-v5 selftest
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-21 16:22]** Re: [PATCH 06/18] KVM: arm64: vgic: Consolidate
 vgic_allocate_private_irqs_locked()
   - 发件人: Joey Gouly <joey.gouly@arm.com>
6. **[04-21 16:54]** Re: [PATCH 05/18] KVM: arm64: vgic: Constify struct irq_ops usage
   - 发件人: Joey Gouly <joey.gouly@arm.com>
7. **[04-21 17:02]** Re: [PATCH 12/18] KVM: arm64: selftests: Add missing GIC CDEN to
 no-vgic-v5 selftest
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 7: [PATCH 0/1] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 11 Apr 2026 13:50:23 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下实现嵌套阶段2反向映射的补丁（patch）。补丁的目标是优化在 MMU 通知期间对影子阶段2 MMU 解除映射的过程。

在历史讨论中，Wei-Lin Chang 提出了补丁的第二版（v2），相较于第一版（v1），进行了多项改进，包括基于更新的 kvmarm/next 进行了重基、添加了 VALID_ENTRY 标志以处理非污染的反向映射条目，以及在使用 maple tree 时引入了锁机制。Marc Zyngier 提出了对术语的一些建议，并讨论了数据结构的优化。

在本周的新讨论中，Wei-Lin Chang 实验性地使用 RCU（读-复制-更新）机制来延迟释放树结构，并提出了一些观察结果。他建议将所有与嵌套阶段2相关的字段聚合到一个新的结构体中（kvm_s2_mmu_nested），并在 kvm_s2_mmu 中添加指向该结构的指针，以便在初始化嵌套阶段2 MMU 时动态分配。这一提议旨在简化当前的实现方式，提升代码的可读性和维护性。

#### 📝 邮件列表

1. **[04-11 13:50]** [PATCH 0/1] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[04-11 13:50]** [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[04-15 09:38]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-16 00:05]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[04-16 11:50]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-24 20:45]** Re: [PATCH 1/1] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 8: [PATCH v2 0/4] KVM: arm64: Don't perform vgic-v2 lazy init on timer injection

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 22 Apr 2026 11:02:06 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁系列，主要集中在优化 vgic-v2（虚拟通用中断控制器）和定时器的初始化过程。

**原始补丁内容**：
补丁的核心目的是避免在定时器注入时进行 vgic-v2 的懒惰初始化（lazy init），以解决在非抢占上下文中初始化 vgic-v2 的问题。补丁包括四个部分，涉及对定时器相关函数的重命名和优化，以及对 vgic-v2 初始化路径的调整。

**之前讨论要点**：
在之前的讨论中，Marc Zyngier 提出了第一版补丁，并在反馈中收集了改进意见，包括重命名函数以提高可读性和简化代码。补丁的目标是提高代码的正确性和可维护性。

**本周新讨论及进展**：
本周的讨论中，Marc Zyngier 提交了补丁的第二版，详细介绍了每个补丁的修改内容，包括重命名定时器函数、删除冗余的缓存机制、确保在用户空间或 irqfd 注入中强制执行 vgic 初始化等。此外，Joey Gouly 对其中一个补丁进行了审核并提出了小的改进建议。整体来看，本周的讨论集中在补丁的细节修改和代码优化上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[04-22 11:02]** [PATCH v2 0/4] KVM: arm64: Don't perform vgic-v2 lazy init on timer injection
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-22 11:02]** [PATCH v2 1/4] KVM: arm64: timer: Repaint kvm_timer_{should,irq_can}_fire() to kvm_timer_{pending,enabled}()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-22 11:02]** [PATCH v2 2/4] KVM: arm64: timer: Kill the per-timer level cache
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-22 11:02]** [PATCH v2 3/4] KVM: arm64: vgic-v2: Force vgic init on injection outside the run loop
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-22 11:02]** [PATCH v2 4/4] KVM: arm64: vgic-v2: Don't init the vgic on in-kernel interrupt injection
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-22 14:30]** Re: [PATCH v2 1/4] KVM: arm64: timer: Repaint
 kvm_timer_{should,irq_can}_fire() to kvm_timer_{pending,enabled}()
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 9: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 22 Apr 2026 07:55:56 +0100

#### 🤖 AI 总结

本邮件讨论围绕一个补丁（PATCH v4 35/49），其内容是将 L1 LR 同步集成到 GICv3 的去激活原语中，主要涉及 KVM 在 arm64 架构下的实现。

在历史讨论中，未提供具体背景信息，因此我们无法得知补丁的详细历史讨论内容。

本周的新讨论中，Marc Zyngier 提出了对补丁的关注，并询问是否有进展。Vishnu Pajjuri 反馈说，问题在于当定时器中断（IRQ 27）被去激活时触发，防止 IRQ 27 在嵌套 VGIC 状态转换期间去激活可以避免问题重现。他正在追踪执行路径并检查 VGIC 状态，以确定禁用该中断如何导致观察到的行为。

Darren Hart 表示他将为 Vishnu 提供必要的资源，以推动问题的解决。Marc Zyngier 进一步询问去激活的具体级别，并建议尝试一种禁用陷阱的黑客方法，以帮助诊断问题。

总体来看，本周的讨论集中在对补丁的具体实现和问题的深入分析上，参与者们积极寻求解决方案并进行技术交流。

#### 📝 邮件列表

1. **[04-22 07:55]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-22 20:27]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive
   - 发件人: Vishnu Pajjuri <vishnu@os.amperecomputing.com>
3. **[04-23 17:02]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive
   - 发件人: Darren Hart <darren@os.amperecomputing.com>
4. **[04-26 10:14]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-26 15:07]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 10: [PATCH 0/3] KVM: arm64: vgic: Fix IIDR revision handling and add revision 1

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  7 Apr 2026 21:27:01 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的虚拟化中，针对 VGIC（虚拟通用中断控制器）修复 IIDR（中断接口描述符寄存器）修订版处理的问题。

**原始 patch/问题内容**：
David Woodhouse 提出的补丁主要解决了 GICD_IIDR 的 uaccess 写处理程序从错误的变量中提取修订字段的问题，导致用户空间无法更改实现修订。此外，补丁还允许用户空间选择 IIDR 修订版 1，以恢复在某个提交之前的行为。

**之前讨论要点**：
在历史讨论中，补丁 1/3 详细说明了问题的根源，即 uaccess 写处理程序在 GICv2 和 GICv3 中错误地从当前 IIDR 值中提取修订字段，而不是用户空间试图写入的值。这使得用户空间无法实际改变实现修订。

**本周的新讨论、进展或结论**：
在本周的讨论中，Marc Zyngier 确认已将补丁应用于修复，并表示感谢。同时，David Woodhouse 提到补丁系列的 v2 版本进一步清理了 IIDR 值与实际行为之间的奇怪不一致，并解决了从旧内核升级到新内核时维护客户兼容性的问题。这些讨论表明，补丁的实施将有助于改善 KVM 的功能和兼容性。

#### 📝 邮件列表

1. **[04-07 21:27]** [PATCH 0/3] KVM: arm64: vgic: Fix IIDR revision handling and add revision 1
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[04-07 21:27]** [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>
3. **[04-24 12:07]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field extracted from wrong value
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-24 13:24]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 11: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 23 Apr 2026 17:36:07 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM (Kernel-based Virtual Machine) 的补丁，主题为“当 iqrchip 在用户空间时从 WFI (Wait For Interrupt) 唤醒”。该补丁的主要目的是修复一个存在了约四年的问题，即在用户空间的 irqchip 支持中，唤醒路径没有评估内核中的中断是否待处理，导致该功能无法正常工作。

在历史讨论中，Marc Zyngier 提到，用户空间 irqchip 的支持自引入以来就存在缺陷，且在过去的十年中，这一设计被认为是一个糟糕的主意。补丁的具体实现包括在 `kvm_arch_vcpu_runnable` 函数中增加了对用户空间中断的检查，以确保在适当的情况下能够唤醒虚拟 CPU。

在本周的新讨论中，Yao Yuan 提出了一个建议，建议引入一个新的辅助函数 `kvm_should_notify_us_irqchip()` 来替代重复的代码。对此，Marc Zyngier 表达了反对意见，认为引入辅助函数会使得后续的回溯工作变得复杂，并表示他有计划进一步简化相关功能。最终，Marc 确认已将补丁应用于修复分支，表示感谢。

总结来说，本周的讨论集中在补丁的实现细节及其对现有代码的影响上，Marc Zyngier 强调了保持代码简洁和可维护的重要性。

#### 📝 邮件列表

1. **[04-23 17:36]** [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-24 14:33]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
3. **[04-24 08:24]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-24 12:08]** Re: [PATCH] KVM: arm64: Wake-up from WFI when iqrchip is in userspace
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH] arm64: KVM: Initialize vGIC before preempt-disabled section in kvm_reset_vcpu()

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 12 Apr 2026 13:34:37 +0530

#### 🤖 AI 总结

本邮件讨论的主题是关于在 `kvm_reset_vcpu()` 函数中初始化 vGIC 的补丁（patch）。历史讨论中，Deepanshu Kartikey 提出了该补丁，指出在禁用抢占的代码段中调用 `kvm_timer_vcpu_reset()` 可能会导致问题，因为该函数最终会调用 `kvm_vgic_inject_irq()`，而后者在 vGIC 未初始化时会触发 `vgic_lazy_init()`，这可能导致在禁止抢占的情况下发生睡眠，从而引发调度错误。

Marc Zyngier 对此补丁提出了批评，认为强制在 vcpu 的计时器重置时初始化 vGIC（一个全局资源）是不合理的，建议开发者应关注问题的根本原因，而不是仅仅修复表面症状。

在本周的新讨论中，Deepanshu Kartikey 感谢 Marc 的反馈，并承认他的补丁确实未能解决根本问题，表示将根据建议进行修改并准备提交 v2 版本。同时，Marc 也提到他会发布自己的解决方案，并邀请 Deepanshu 进行审阅。整体来看，讨论的焦点在于如何合理地处理 vGIC 和计时器之间的关系，以避免潜在的错误。

#### 📝 邮件列表

1. **[04-12 13:34]** [PATCH] arm64: KVM: Initialize vGIC before preempt-disabled section in kvm_reset_vcpu()
   - 发件人: Deepanshu Kartikey <kartikey406@gmail.com>
2. **[04-16 15:20]** Re: [PATCH] arm64: KVM: Initialize vGIC before preempt-disabled section in kvm_reset_vcpu()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-21 07:18]** Re: [PATCH] arm64: KVM: Initialize vGIC before preempt-disabled
 section in kvm_reset_vcpu()
   - 发件人: Deepanshu Kartikey <kartikey406@gmail.com>
4. **[04-21 08:42]** Re: [PATCH] arm64: KVM: Initialize vGIC before preempt-disabled section in kvm_reset_vcpu()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 13: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Apr 2026 13:32:03 +0530

#### 🤖 AI 总结

本邮件线程讨论了一个关于KVM（Kernel-based Virtual Machine）在arm64架构上支持保护来宾内存的补丁（PATCH 00/30），该补丁旨在与pKVM（Protected KVM）配合使用。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁的目标是增强KVM对保护内存的支持，以提高虚拟机的安全性。

在本周的新讨论中，Pavan Kondeti和Will Deacon进行了深入交流。Pavan提到，Qualcomm正在努力将Gunyah项目的上游工作与此补丁结合，但由于guest_memfd与KVM紧密耦合，重用的路径并不简单。Will则指出，pKVM内部处理阶段2故障的接口存在问题，特别是异常处理和超调用的标准化问题。他们一致认为不应在故障处理代码中添加Gunyah特定的检查，以避免未来的维护复杂性。

Pavan进一步讨论了在处理内存借用时，用户空间和内核访问的不同情况，提出了借用内存时需要解除映射的方案，并希望能借鉴guest_memfd的相关工作。最后，他澄清了之前提到的内存损坏问题，实际上是指在VCPU_RUN ioctl中返回-EFAULT，可能导致虚拟机被杀死。

总体来看，本周的讨论集中在如何有效整合pKVM与Gunyah的功能，同时保持代码的清晰和可维护性。

#### 📝 邮件列表

1. **[04-20 13:32]** Re: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM
   - 发件人: Pavan Kondeti <pavan.kondeti@oss.qualcomm.com>
2. **[04-20 11:00]** Re: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM
   - 发件人: Will Deacon <will@kernel.org>
3. **[04-20 16:56]** Re: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM
   - 发件人: Pavan Kondeti <pavan.kondeti@oss.qualcomm.com>
4. **[04-21 09:45]** Re: [PATCH 00/30] KVM: arm64: Add support for protected guest memory
 with pKVM
   - 发件人: Pavan Kondeti <pavan.kondeti@oss.qualcomm.com>

---

### Thread 14: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Apr 2026 15:18:28 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上支持 HDBSS（Hardware Debugging and Breakpoint Support System）的补丁（patch）。该补丁的主要目的是启用 HDBSS 支持并处理 HDBSSF（HDBSS Fault）事件。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁的提出是为了增强 KVM 的调试能力，尤其是在处理特定硬件事件时的支持。

在本周的新讨论中，参与者 Leonardo Bras 和 Tian Zheng 进行了关于 HACDBS（Hardware Aware Control Debug Breakpoint Support）和 HACDBSIRQ（HACDBS 中断请求）的讨论。Leonardo 提出 HACDBS 依赖于 HACDBSIRQ，并询问是否可以暂时仅通过 ACPI（高级配置与电源接口）来实现 HACDBSIRQ。Tian 表示对此没有问题，并鼓励 Leonardo 在实现 HACDBS 时随时提问。最终，Leonardo 表示他已经在自己的环境中成功实现了相关功能，并计划发送一个独立的补丁，以满足 HDBSS 的需求。

总的来说，本周的讨论主要集中在补丁的实现细节和对 HACDBSIRQ 的依赖关系上，参与者之间的沟通顺畅，进展积极。

#### 📝 邮件列表

1. **[04-21 15:18]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[04-24 14:48]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[04-24 11:08]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 15: [PATCH v2 01/10] KVM: selftests: Use gva_t instead of vm_vaddr_t

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Apr 2026 13:06:21 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 自测的补丁，主题为“[PATCH v2 01/10] KVM: selftests: Use gva_t instead of vm_vaddr_t”。补丁的主要内容是将现有的虚拟地址类型 `vm_vaddr_t` 替换为 `gva_t`，以改进代码的可读性和一致性。

在历史讨论中，参与者对现有的 API 命名提出了批评，认为 `vm_vaddr_alloc()` 和 `gva_alloc()` 的命名不够清晰，且容易引起混淆。讨论中提到，这些 API 不仅仅是分配虚拟地址，还涉及到分配物理内存、查找可用的虚拟地址和创建映射。因此，建议将这些 API 的命名更改为更具描述性的 `vm_alloc()`，并将此更改分离到单独的补丁中，以避免在一个补丁中进行多个逻辑更改。

在本周的新讨论中，Sean Christopherson 和 David Matlack 进行了进一步的交流，确认了将 API 重命名的建议，并一致同意将其拆分为独立的补丁。Sean 还指出了在 `kvm_util_types.h` 中需要包含 `types.h` 的问题，以避免潜在的错误。

总体而言，本周的讨论集中在补丁的命名和代码结构的清晰性上，达成了将 API 重命名与其他更改分开的共识。

#### 📝 邮件列表

1. **[04-20 13:06]** Re: [PATCH v2 01/10] KVM: selftests: Use gva_t instead of vm_vaddr_t
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[04-20 13:15]** Re: [PATCH v2 01/10] KVM: selftests: Use gva_t instead of vm_vaddr_t
   - 发件人: David Matlack <dmatlack@google.com>
3. **[04-20 13:43]** Re: [PATCH v2 04/10] KVM: selftests: Use u64 instead of uint64_t
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 16: [PATCH v2] KVM: arm64: Reject non compliant SMCCC function calls in pKVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  8 Apr 2026 11:41:18 +0000

#### 🤖 AI 总结

在本邮件线程中，讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下对不符合 SMCCC（SMC Calling Convention）规范的函数调用的处理。历史讨论中，Sebastian Ene 提出了一个补丁（patch），目的是防止传播具有高位设置的函数 ID，因为这不符合 SMCCC 规范，可能与已知的函数 ID 解码器重叠。例如，调用一个带有特定高位的 SMC（Secure Monitor Call）可能会被错误解码为 PSCI（Power State Coordination Interface）重置调用。补丁的核心在于明确表示不支持这些不合规的调用，并返回错误。

在本周的新讨论中，Marc Zyngier 对该补丁表示感谢，并确认已将其应用于修复列表中，标记为提交（commit）480ea48cad873b49a1fabd07c0847c3cf1c32286。这表明该补丁已获得认可并正式纳入代码库中，进一步推动了对 SMCCC 规范的遵循。

#### 📝 邮件列表

1. **[04-08 11:41]** [PATCH v2] KVM: arm64: Reject non compliant SMCCC function calls in pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[04-24 12:08]** Re: [PATCH v2] KVM: arm64: Reject non compliant SMCCC function calls in pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 17: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 20 Apr 2026 11:57:38 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在 KVM 中引入 arm64 支持的补丁（PATCH v1 00/27）。该补丁旨在将 arm64 特定的代码和定义引入 s390 架构，以便实现更好的架构间兼容性。

在历史讨论中，补丁的背景和目的已被明确，但并未提供具体的历史讨论内容。

本周的新讨论中，Marc Zyngier 和 Steffen Eiden 进行了深入的交流。Marc 表达了对补丁工作的支持，并提出了一些改进建议，包括代码的组织和维护性问题。他指出，当前的实现可能会导致维护困难，并建议使用符号链接或相对路径来访问 arm64 特定文件。此外，他强调了用户空间 API 和来宾 API 的兼容性问题，尤其是在处理错误和设备分配方面。

Steffen 对 Marc 的反馈表示感谢，并承诺会考虑使用符号链接来简化维护工作。他还确认了将重用 arm64 的超调用代码，并表示将确保 s390 不会阻碍 arm64 的进展。两位参与者还讨论了测试和文档的需求，以确保双方在开发过程中不会出现误解。

总体而言，本周的讨论集中在如何优化补丁的实现、确保架构间的兼容性以及建立有效的沟通和测试机制上。双方均表现出合作的意愿，计划在未来的会议中进一步讨论。

#### 📝 邮件列表

1. **[04-20 11:57]** Re: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-23 14:25]** Re: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 18: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Apr 2026 21:51:45 +0800

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v13 00/48] arm64: 支持 KVM 中的 Arm CCA”，主要涉及对 ARM CCA 的支持及其在 KVM 中的实现问题。

在历史讨论中，未提供具体的背景信息，但本周的新讨论中，Jiahao Zheng 提出了在 nVHE 模式下运行 Realm VM 时遇到的启动问题。他指出，当前在 `kvm_ioctl_vcpu_run()` 中，Realm VM 的执行绕过了标准的 nVHE EL2 stub，导致 VGIC 状态未被保存，可能导致不确定行为。为此，他提出了两个解决方案：一是如果不支持在 nVHE 模式下运行 Realm，则应在初始化时明确拒绝；二是如果支持，则需要在 KVM 中添加特定逻辑，以确保 VGIC 状态能够正确保存。

Steven Price 对此进行了回应，承认这是一个疏忽，并表示将采取第一个方案。他指出，虽然 nVHE 模式的支持并不紧迫，但在 pKVM 的情况下，需要进行更多工作以确保 EL2 hypervisor 理解 RMM 通信，防止潜在的安全问题。他的重点仍然是确保基本支持的合并，而对 nVHE 的支持将来可能会考虑。

综上所述，本周的讨论主要集中在 nVHE 模式下 Realm VM 的问题及其解决方案，参与者对未来的支持方向进行了初步探讨。

#### 📝 邮件列表

1. **[04-21 21:51]** [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Jiahao zheng <jahao.zheng@gmail.com>
2. **[04-22 16:38]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 19: [PATCH] KVM: arm64: Treat ID_AA64DFR0_EL1.PMUVer as an unsigned field

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 21 Apr 2026 09:41:12 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 在 arm64 架构下如何处理 ID_AA64DFR0_EL1.PMUVer 字段。原始的 patch 提出了将该字段视为无符号字段的建议，因为它实际上是一个无符号的 4 位字段，但在 cpufeature 表中历史上被标记为有符号。这导致在某些系统上（如 PMUv3p8 或更新版本）无法正确检测 PMUv3 实现，从而影响了 kvm_init_host_debug_data() 的功能。

在之前的讨论中，参与者们关注了这一问题的根源以及如何修复。Jing Zhang 提出通过在 ftr_id_aa64dfr0 表中将该字段标记为无符号，并更新 KVM 初始化代码以使用无符号提取，从而解决问题。同时，确保正确处理 '未实现'（0b0000）和 '实现定义'（0b1111）值，以指示缺少标准 PMUv3。

本周的新讨论中，Jing Zhang 发送了修复的 patch，并详细描述了修改内容，包括对相关代码的具体更改。Marc Zyngier 对此进行了回应，表示关注并提供了相关链接以供进一步讨论。整体来看，本周的进展主要集中在 patch 的具体实现和潜在的后续讨论上。

#### 📝 邮件列表

1. **[04-21 09:41]** [PATCH] KVM: arm64: Treat ID_AA64DFR0_EL1.PMUVer as an unsigned field
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[04-21 17:45]** Re: [PATCH] KVM: arm64: Treat ID_AA64DFR0_EL1.PMUVer as an unsigned field
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 20: [PATCH v10 14/30] KVM: arm64: Implement SME vector length
 configuration

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 23 Apr 2026 19:34:59 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中实现 SME（Scalable Matrix Extension）向量长度配置的补丁（patch）。该补丁旨在允许虚拟机（guest）在多个可用向量长度（VL）之间进行选择，甚至可以选择一个小于在虚拟机监控器（hypervisor）中配置的向量长度。

在历史讨论中，虽然没有提供具体的上下文，但可以推测出该补丁的提出是为了增强虚拟机的灵活性，使其能够根据需求调整向量长度。这一功能的实现对于优化性能和资源利用率具有重要意义。

在本周的新讨论中，参与者 Mark Brown 对补丁进行了回复，强调了虚拟机在运行于 EL1（Exception Level 1）时，可以在 ZCR_EL1 或 SMCR_EL1 寄存器中设置一个低于 EL2（Exception Level 2）寄存器中配置的向量长度。这一细节的澄清显示出对补丁功能的深入理解，并指出了在实现过程中需要注意的事项。

总体来看，本周的讨论进一步明确了补丁的功能及其在虚拟化环境中的应用，推动了对该补丁的理解和实施。

#### 📝 邮件列表

1. **[04-23 19:34]** Re: [PATCH v10 14/30] KVM: arm64: Implement SME vector length
 configuration
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 21: [PATCH] tracing: Make undefsyms_base.c a first-class citizen

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 21 Apr 2026 10:54:46 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），其内容为将 `undefsyms_base.c` 文件提升为 Git 树中的“第一公民”。Marc Zyngier 提出这一补丁，回应了 Linus Torvalds 的意见，认为在 Makefile 中处理 `undefsyms_base.c` 的方式显得不够优雅，建议将其直接纳入 Git 树中。

在之前的讨论中，Linus 指出当前的处理方式较为冗杂，且存在清理 Makefile 的空间。补丁的实施将简化 Makefile，并允许删除 `kernel/trace` 目录下的 `.gitignore` 文件。

本周的讨论中，Marc Zyngier 提交了该补丁，并详细列出了对 Makefile 和 `undefsyms_base.c` 文件的具体修改。补丁中移除了对 `undefsyms_base.c` 的生成命令，并将其内容直接写入新文件中，增强了代码的整洁性和可维护性。此补丁的实施预计将改善内核追踪功能的代码结构。

#### 📝 邮件列表

1. **[04-21 10:54]** [PATCH] tracing: Make undefsyms_base.c a first-class citizen
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 RFC

共 3 个 thread

---

### Thread 1: [RFC PATCH v2 0/4] fix FF-A call failed with pKVM when ff-a driver is built-in

**📧 邮件数**: 37 | **👥 参与者**: 7 | **📅 开始时间**: Wed, 22 Apr 2026 17:24:45 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于修复在 pKVM 环境下 FF-A 驱动作为内置模块时调用失败的问题。Yeoreum Yun 提出了一个补丁集（RFC PATCH v2），主要包含四个补丁，旨在确保 IMA（Integrity Measurement Architecture）能够在 TPM（Trusted Platform Module）设备可用时正确初始化。

**历史讨论**：
在之前的讨论中，补丁的背景是由于将 `ffa_init()` 的初始化级别更改为 `rootfs_initcall`，导致 pKVM 无法处理 FF-A 调用。为了确保 TPM 设备被识别，建议在后期阶段再次调用 `ima_init()`。补丁的目标是通过将 `ffa_init()` 的级别恢复为 `device_initcall`，并在初始化时检查 pKVM 是否已准备好，从而解决此问题。

**本周新讨论**：
本周的讨论集中在补丁的具体实现上。Yeoreum Yun 提出了在 `late_initcall_sync` 阶段再次调用 `ima_init()` 的必要性，以确保 TPM 设备在 IMA 初始化时可用。Mimi Zohar 对补丁的复杂性表示担忧，建议简化补丁，只需在 `late_initcall_sync` 阶段调用 `ima_init()`。讨论中还涉及到如何处理 TPM 设备未能及时初始化的问题，以及是否有必要在两个不同的初始化阶段调用 `ima_init()`。最终，参与者达成共识，补丁需要进一步简化，并确保在 TPM 可用时尽早初始化 IMA。

总结而言，本周的讨论围绕如何有效地处理 TPM 初始化与 IMA 之间的依赖关系展开，提出了多种解决方案，并对补丁的简化和逻辑性进行了深入探讨。

#### 📝 邮件列表

1. **[04-22 17:24]** [RFC PATCH v2 0/4] fix FF-A call failed with pKVM when ff-a driver is built-in
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[04-22 17:24]** [RFC PATCH v2 1/4] security: ima: call ima_init() again at late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[04-22 17:24]** [RFC PATCH v2 2/4] tpm: tpm_crb_ffa: revert defered_probed when tpm_crb_ffa is built-in
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[04-22 17:24]** [RFC PATCH v2 3/4] firmware: arm_ffa: revert ffa_init() initcall level to device_initcall
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[04-22 17:24]** [RFC PATCH v2 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[04-22 13:20]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
7. **[04-22 19:46]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[04-22 20:41]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[04-22 17:20]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
10. **[04-23 06:55]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
11. **[04-23 09:34]** Re: [RFC PATCH v2 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[04-23 10:13]** Re: [RFC PATCH v2 3/4] firmware: arm_ffa: revert ffa_init() initcall
 level to device_initcall
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
13. **[04-23 13:17]** Re: [RFC PATCH v2 2/4] tpm: tpm_crb_ffa: revert defered_probed when
 tpm_crb_ffa is built-in
   - 发件人: Jarkko Sakkinen <jarkko@kernel.org>
14. **[04-23 11:29]** Re: [RFC PATCH v2 4/4] firmware: arm_ffa: check pkvm initailised
 when initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
15. **[04-23 07:01]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
16. **[04-23 12:20]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
17. **[04-23 13:34]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
18. **[04-23 13:53]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
19. **[04-23 14:07]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
20. **[04-23 09:43]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
21. **[04-23 14:55]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
22. **[04-23 15:03]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
23. **[04-23 15:33]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
24. **[04-23 10:48]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
25. **[04-23 18:02]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
26. **[04-23 13:13]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
27. **[04-23 14:01]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
28. **[04-23 19:13]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
29. **[04-23 21:27]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
30. **[04-24 06:57]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
31. **[04-24 16:15]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
32. **[04-24 16:57]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
33. **[04-24 17:08]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
34. **[04-24 18:00]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
35. **[04-24 18:10]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Paul Moore <paul@paul-moore.com>
36. **[04-24 18:49]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
37. **[04-25 05:53]** Re: [RFC PATCH v2 1/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 2: [RFC PATCH 0/4] fix FF-A call failed with pKVM when ff-a driver is built-in

**📧 邮件数**: 33 | **👥 参与者**: 7 | **📅 开始时间**: Fri, 17 Apr 2026 18:57:55 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 pKVM 和 FF-A 驱动初始化顺序的问题，特别是如何确保 FF-A 驱动在 pKVM 初始化后正确工作。

1. **原始 patch/问题的内容**：Yeoreum Yun 提出了一个补丁（RFC PATCH 0/4），旨在解决当 FF-A 驱动作为内置模块时，pKVM 无法处理 FF-A 调用的问题。补丁的关键在于确保 FF-A 驱动的初始化在 pKVM 初始化之后进行，以避免调用失败。

2. **之前的讨论要点**：在历史讨论中，Marc Zyngier 指出，pKVM 的初始化状态在 `finalize_pkvm()` 完成之前并不可靠，因此需要一种机制来确保 FF-A 驱动在 pKVM 完成初始化后再进行初始化。Yeoreum 提出了一些可能的解决方案，包括引入状态检查函数或事件通知机制。

3. **本周的新讨论、进展或结论**：本周的讨论集中在如何实现这一依赖关系。Will Deacon 建议将 FF-A 初始化分为两个步骤，以便更好地处理依赖关系。Yeoreum 则认为，即使分步初始化，早期的版本协商仍需在 pKVM 初始化之后进行。最终，Yeoreum 提出引入通知机制作为解决方案，并计划在后续版本中实现。此外，Jonathan McDowell 对另一个补丁（RFC PATCH 1/4）表示了支持，认为它解决了 TPM 设备初始化的问题。

整体来看，讨论强调了在内核模块初始化中处理依赖关系的重要性，并探索了多种可能的实现方案。

#### 📝 邮件列表

1. **[04-17 18:57]** [RFC PATCH 0/4] fix FF-A call failed with pKVM when ff-a driver is built-in
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[04-17 18:57]** [RFC PATCH 1/4] security: ima: move ima_init into late_initcall_sync
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[04-17 18:57]** [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[04-18 10:24]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-18 11:34]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[04-19 11:41]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[04-19 12:12]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[04-20 09:55]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Will Deacon <will@kernel.org>
9. **[04-20 10:25]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
10. **[04-20 11:32]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Jonathan McDowell <noodles@earth.li>
11. **[04-20 11:42]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Will Deacon <will@kernel.org>
12. **[04-20 11:56]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
13. **[04-20 12:32]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sebastian Ene <sebastianene@google.com>
14. **[04-20 13:46]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when initailise ffa driver
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[04-20 14:00]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
16. **[04-20 14:05]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sebastian Ene <sebastianene@google.com>
17. **[04-20 14:20]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sebastian Ene <sebastianene@google.com>
18. **[04-20 15:47]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
19. **[04-20 16:04]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
20. **[04-20 16:47]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
21. **[04-20 17:50]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
22. **[04-20 18:04]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
23. **[04-21 07:57]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
24. **[04-21 09:51]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
25. **[04-21 10:12]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
26. **[04-21 10:37]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
27. **[04-21 08:00]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
28. **[04-21 13:50]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
29. **[04-21 09:26]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
30. **[04-21 15:09]** Re: [RFC PATCH 1/4] security: ima: move ima_init into
 late_initcall_sync
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
31. **[04-22 14:32]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
32. **[04-23 09:57]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Will Deacon <will@kernel.org>
33. **[04-23 11:56]** Re: [RFC PATCH 4/4] firmware: arm_ffa: check pkvm initailised when
 initailise ffa driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 3: [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue

**📧 邮件数**: 11 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 24 Apr 2026 14:23:45 +0100

#### 🤖 AI 总结

本邮件讨论主题为修复 IMA（完整性测量架构）与 TPM（受信任的平台模块）初始化顺序问题。原始的补丁系列（RFC PATCH v3 0/4）旨在确保 IMA 在 TPM 完全注册之前不会初始化，从而避免在某些 ARM FF-A 和 SPI 连接的 TPM 设置中出现错误。

在之前的讨论中，参与者们提到了一些 TPM 驱动在常规的 initcall_late 阶段可能无法可靠初始化的问题，因此需要在 IMA 初始化时考虑 TPM 的可用性。补丁系列经过几轮修改，最终决定在 late_initcall_sync 阶段重新调用 IMA 初始化，以确保 TPM 可用。

本周的新讨论中，Jonathan McDowell 提出了补丁的具体实现，主要包括：
1. 在 IMA 初始化时增加了对 TPM 的重试机制。
2. 取消了之前对 FF-A 驱动和 arm_ffa 初始化调用级别的更改，因为现在 IMA 可以在 TPM 不可用时延迟初始化。
3. 多位参与者对补丁表示认可，并提出了小的修改建议。

整体来看，本周的讨论集中在补丁的实现细节和确认其有效性上，参与者们对补丁的方向表示支持，预计将进一步推动该补丁的合并。

#### 📝 邮件列表

1. **[04-24 14:23]** [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue
   - 发件人: Jonathan McDowell <noodles@earth.li>
2. **[04-24 14:24]** [RFC PATCH v3 1/4] lsm: Allow LSMs to register for
 late_initcall_sync init
   - 发件人: Jonathan McDowell <noodles@earth.li>
3. **[04-24 14:24]** [RFC PATCH v3 2/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
4. **[04-24 14:24]** [RFC PATCH v3 3/4] Revert "tpm: tpm_crb_ffa: try to probe
 tpm_crb_ffa when it's built-in"
   - 发件人: Jonathan McDowell <noodles@earth.li>
5. **[04-24 14:24]** [RFC PATCH v3 4/4] Revert "firmware: arm_ffa: Change initcall level
 of ffa_init() to rootfs_initcall"
   - 发件人: Jonathan McDowell <noodles@earth.li>
6. **[04-24 17:09]** Re: [RFC PATCH v3 4/4] Revert "firmware: arm_ffa: Change initcall
 level of ffa_init() to rootfs_initcall"
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
7. **[04-24 17:10]** Re: [RFC PATCH v3 3/4] Revert "tpm: tpm_crb_ffa: try to probe
 tpm_crb_ffa when it's built-in"
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
8. **[04-24 17:55]** Re: [RFC PATCH v3 2/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[04-24 16:25]** Re: [RFC PATCH v3 2/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
10. **[04-25 10:10]** Re: [RFC PATCH v3 2/4] security: ima: call ima_init() again at
 late_initcall_sync for defered TPM
   - 发件人: Jonathan McDowell <noodles@earth.li>
11. **[04-25 17:19]** Re: [RFC PATCH v3 4/4] Revert "firmware: arm_ffa: Change initcall
 level of ffa_init() to rootfs_initcall"
   - 发件人: Jarkko Sakkinen <jarkko@kernel.org>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #1

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 24 Apr 2026 16:14:43 +0100

#### 🤖 AI 总结

本邮件讨论了 KVM/arm64 在 7.1 版本中的修复补丁，这是首次提交的修复集。该补丁主要针对 IDREG 处理、长期存在的回归问题、SMCCC 合规性等进行了广泛的修复，同时也包含了一些代码清理。

在历史讨论中没有提供具体的背景信息，但本周的邮件由 Marc Zyngier 提出，概述了补丁的主要内容和目的。补丁包括以下几个关键修复：恢复对非 pKVM 的跟踪支持、规范化 pKVM 超级调用范围的定义、确保 pKVM 代理传递的 SMCCC 函数号符合规范、修复 IDREG 映射中的错误、修正 GICD_IIDR 版本号字段的写入问题等。此外，还修复了多个拼写错误和其他小问题。

本周的讨论没有涉及新的争议或问题，主要是对补丁的确认和请求合并。整体来看，此次修复集旨在提升 KVM/arm64 的稳定性和功能性，为用户提供更好的支持。

#### 📝 邮件列表

1. **[04-24 16:14]** [GIT PULL] KVM/arm64 fixes for 7.1, take #1
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Other

共 2 个 thread

---

### Thread 1: [kvm-unit-tests PATCH v2 0/7] arm64: Add Stage-2 MMU and Nested Guest Framework

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 13 Apr 2026 13:46:23 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM64 的补丁系列，旨在为 KVM 单元测试引入 Stage-2 MMU 和嵌套虚拟机框架。该补丁系列的核心内容包括一个轻量级的基础设施，用于管理 ARM64 的 Stage-2 转换表和执行嵌套虚拟机，这对于测试嵌套虚拟化（NV）和 GICv4 直接中断注入等高级虚拟化特性至关重要。

在之前的讨论中，Jing Zhang 提出了补丁的基本结构，包括一个通用的 Stage-2 MMU 库和一个处理虚拟机生命周期管理的执行框架。Joey Gouly 对补丁提出了一些初步的反馈，指出了代码中的一些潜在问题和改进建议，例如直接使用特定的汇编指令和缺少对空指针的检查。

在本周的新讨论中，Joey Gouly 进一步确认了补丁中某些内容的必要性，并指出了具体的修正建议，特别是 SYS_SCTLR_EL12 应该替代 SYS_SCTLR_EL1 的使用。这表明讨论正在朝着修正和完善补丁的方向发展。整体来看，补丁的目标是增强 KVM 在 ARM64 平台上的虚拟化能力，相关讨论也在不断推动其进展。

#### 📝 邮件列表

1. **[04-13 13:46]** [kvm-unit-tests PATCH v2 0/7] arm64: Add Stage-2 MMU and Nested Guest Framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[04-13 13:46]** [kvm-unit-tests PATCH v2 4/7] lib: arm64: Add foundational guest
 execution framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
3. **[04-16 17:16]** Re: [kvm-unit-tests PATCH v2 4/7] lib: arm64: Add foundational guest
 execution framework
   - 发件人: Joey Gouly <joey.gouly@arm.com>
4. **[04-23 16:30]** Re: [kvm-unit-tests PATCH v2 4/7] lib: arm64: Add foundational guest
 execution framework
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

### Thread 2: [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to match Linux kernel

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 22 Apr 2026 14:08:20 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于更新 ARM64 架构下的 ESR_ELx 定义，以使其与 Linux 内核保持一致。该补丁由 Joey Gouly 提出，目的是支持 EL2 阶段的 MMU 系列操作，具体是将 ESR_EL1* 的名称替换为 ESR_ELx。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁是对之前讨论的延续，旨在提高 KVM 单元测试的兼容性和一致性。补丁的主要内容包括在多个文件中替换异常处理程序中的 ESR_EL1_* 定义为 ESR_ELx_*，以反映新的定义。

在本周的新讨论中，Joey Gouly 提交了该补丁，并指出这是对之前补丁的替代，强调了其在 EL2 阶段的必要性。补丁涉及到多个文件的修改，具体包括对异常处理程序和相关常量的更新，确保其与 Linux 内核中的定义一致。邮件中没有其他参与者的回复或评论，表明讨论尚处于初步阶段。

#### 📝 邮件列表

1. **[04-22 14:08]** [kvm-unit-tests PATCH v1] arm64: update ESR_ELx definitions to match Linux kernel
   - 发件人: Joey Gouly <joey.gouly@arm.com>

---

