# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-06-22 00:59:56

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 373
- **总 Thread 数**: 41
- **大型 Thread** (>20封): 5 个

### 分类分布

- **PATCH**: 32 threads (306 邮件)
- **RFC**: 5 threads (60 邮件)
- **Discussion**: 2 threads (2 邮件)
- **Other**: 2 threads (5 邮件)

---

## 📌 PATCH

共 32 个 thread

---

### Thread 1: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 32 | **👥 参与者**: 6 | **📅 开始时间**: Mon,  8 Jun 2026 16:55:42 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁系列，主题为“将 FFA_NOTIFICATION* 调用转发到 TrustZone”。该补丁的主要目的是移除 pKVM FF-A 代理的阻止列表，以允许使用 Arm FF-A 规范定义的异步信号机制与安全服务进行通信。

在历史讨论中，参与者对补丁的安全性和必要性进行了深入探讨。Sebastian Ene 提出，当前的限制阻碍了功能的实现，而 Vincent Donnefort 和 Will Deacon 则关注于如何确保传递给 TrustZone 的参数的安全性，讨论了是否需要检查保留位（SBZ）参数的有效性。

本周的新讨论中，Sebastian Ene 表达了对强制检查 SBZ 参数的担忧，认为这可能会导致回归问题。他决定在补丁中不强制执行这一检查。Will Deacon 表示支持这一观点，并确认如果调用者未能正确传递零值，则问题在于调用者本身。最终，Sebastian 决定在补丁中加入对现有调用的 SBZ 参数检查，并计划重新提交补丁。

此外，Fuad Tabba 提出了另一个补丁系列，旨在修复 KVM 中 ESR_ELx.IL（异常状态寄存器）缺失的问题，确保在异常注入时正确设置 IL 位，以符合 ARM 架构的要求。该补丁系列包括多个针对不同异常类型的修复，确保在各种情况下都能正确处理 IL 位。

#### 📝 邮件列表

1. **[06-08 16:55]** [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-10 10:26]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[06-10 11:15]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Will Deacon <will@kernel.org>
4. **[06-10 13:15]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[06-10 13:23]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Will Deacon <will@kernel.org>
6. **[06-10 14:56]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[06-14 10:29]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Will Deacon <will@kernel.org>
8. **[06-15 07:43]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-15 10:47]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Will Deacon <will@kernel.org>
10. **[06-16 09:57]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
11. **[06-16 09:59]** Re: [PATCH v2 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to
 TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
12. **[06-18 13:16]** [PATCH v2 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection
   - 发件人: Fuad Tabba <tabba@google.com>
13. **[06-18 13:16]** [PATCH v2 1/7] KVM: arm64: Set ESR_ELx.IL for injected undefined
 exceptions at EL2
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[06-18 13:16]** [PATCH v2 2/7] KVM: arm64: Unconditionally set IL for injected
 undefined exceptions
   - 发件人: Fuad Tabba <tabba@google.com>
15. **[06-18 13:16]** [PATCH v2 3/7] KVM: arm64: Unconditionally set IL for injected abort exceptions
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[06-18 13:16]** [PATCH v2 4/7] KVM: arm64: Set IL for injected FPAC exceptions during
 ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
17. **[06-18 13:16]** [PATCH v2 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
18. **[06-18 13:16]** [PATCH v2 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
19. **[06-18 13:16]** [PATCH v2 7/7] KVM: arm64: Set IL in fake ESR for pKVM memory sharing exit
   - 发件人: Fuad Tabba <tabba@google.com>
20. **[06-18 12:28]** Re: [PATCH v2 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: sashiko-bot@kernel.org
21. **[06-18 12:29]** Re: [PATCH v2 3/7] KVM: arm64: Unconditionally set IL for injected
 abort exceptions
   - 发件人: sashiko-bot@kernel.org
22. **[06-18 12:30]** Re: [PATCH v2 2/7] KVM: arm64: Unconditionally set IL for injected
 undefined exceptions
   - 发件人: sashiko-bot@kernel.org
23. **[06-18 12:32]** Re: [PATCH v2 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: sashiko-bot@kernel.org
24. **[06-18 12:33]** Re: [PATCH v2 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: sashiko-bot@kernel.org
25. **[06-18 13:39]** Re: [PATCH v2 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
26. **[06-18 13:48]** Re: [PATCH v2 4/7] KVM: arm64: Set IL for injected FPAC exceptions during ERET emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[06-18 15:24]** Re: [PATCH v2 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
28. **[06-18 15:41]** Re: [PATCH v2 2/7] KVM: arm64: Unconditionally set IL for injected
 undefined exceptions
   - 发件人: Fuad Tabba <tabba@google.com>
29. **[06-18 15:47]** Re: [PATCH v2 3/7] KVM: arm64: Unconditionally set IL for injected
 abort exceptions
   - 发件人: Fuad Tabba <tabba@google.com>
30. **[06-18 16:03]** Re: [PATCH v2 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
31. **[06-18 16:06]** Re: [PATCH v2 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
32. **[06-18 16:47]** Re: [PATCH v2 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 2: [PATCH v1 00/11] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 25 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 12 Jun 2026 07:59:14 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态同步的重构，包含 11 个补丁。补丁的主要内容是优化 vCPU 状态在宿主机和 EL2（异常级别 2）之间的传递，减少不必要的数据复制，尤其是在非保护性虚拟机的世界切换时。

历史讨论中，补丁的作者 Fuad Tabba 提出了通过引入新的原语（如 VGIC 状态的刷新和同步）来改进 pKVM 的实现，确保在状态传递时的效率和准确性。补丁还包括将一些代码重用的功能提取到共享头文件中，以便于后续的开发和维护。

在本周的新讨论中，参与者 Vincent Donnefort 对多个补丁提出了细节上的建议和改进意见，包括对代码可读性的关注和对某些函数的重命名建议。Fuad Tabba 对这些反馈表示认可，并承诺在后续版本中进行调整。此外，Marc Zyngier 对广泛的代码更改表示担忧，认为应在必要时进行，而不是为了变更而变更。总体来看，本周的讨论集中在代码的可读性和结构优化上，参与者们积极交流，推动补丁的完善。

#### 📝 邮件列表

1. **[06-12 07:59]** [PATCH v1 00/11] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: tabba@google.com
2. **[06-12 07:59]** [PATCH v1 02/11] KVM: arm64: Use guard(hyp_spinlock) in pKVM
 hypervisor code
   - 发件人: tabba@google.com
3. **[06-12 07:59]** [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64 KVM
 EL1 code
   - 发件人: tabba@google.com
4. **[06-12 07:59]** [PATCH v1 05/11] KVM: arm64: Make vcpu_{read,write}_sys_reg available
 to HYP code
   - 发件人: tabba@google.com
5. **[06-12 07:59]** [PATCH v1 06/11] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: tabba@google.com
6. **[06-12 07:59]** [PATCH v1 10/11] KVM: arm64: Add primitives to flush/sync the VGIC
 state at EL2
   - 发件人: tabba@google.com
7. **[06-12 07:59]** [PATCH v1 11/11] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: tabba@google.com
8. **[06-15 13:53]** Re: [PATCH v1 02/11] KVM: arm64: Use guard(hyp_spinlock) in pKVM
 hypervisor code
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[06-15 13:59]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64
 KVM EL1 code
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[06-15 14:11]** Re: [PATCH v1 05/11] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[06-15 14:11]** Re: [PATCH v1 02/11] KVM: arm64: Use guard(hyp_spinlock) in pKVM
 hypervisor code
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[06-15 14:16]** Re: [PATCH v1 06/11] KVM: arm64: Factor out reusable vCPU reset
 helpers
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[06-15 14:17]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64
 KVM EL1 code
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[06-15 14:29]** Re: [PATCH v1 05/11] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Fuad Tabba <tabba@google.com>
15. **[06-15 14:45]** Re: [PATCH v1 06/11] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[06-15 17:25]** Re: [PATCH v1 11/11] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[06-15 17:44]** Re: [PATCH v1 11/11] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
18. **[06-18 10:23]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64 KVM EL1 code
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[06-18 10:24]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64
 KVM EL1 code
   - 发件人: Fuad Tabba <tabba@google.com>
20. **[06-18 10:41]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64 KVM EL1 code
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[06-18 10:46]** Re: [PATCH v1 03/11] KVM: arm64: Use guard()/scoped_guard() in arm64
 KVM EL1 code
   - 发件人: Fuad Tabba <tabba@google.com>
22. **[06-18 11:10]** Re: [PATCH v1 10/11] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[06-18 11:16]** Re: [PATCH v1 11/11] KVM: arm64: Implement lazy vCPU state sync for non-protected guests
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[06-18 11:17]** Re: [PATCH v1 10/11] KVM: arm64: Add primitives to flush/sync the
 VGIC state at EL2
   - 发件人: Fuad Tabba <tabba@google.com>
25. **[06-18 11:18]** Re: [PATCH v1 11/11] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 3: [PATCH v2 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 23 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 19 Jun 2026 08:07:11 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态同步的重构，主要集中在如何优化非保护虚拟机的状态同步过程。

1. **原始 patch/问题的内容**：
   本次讨论的补丁系列（PATCH v2 0/8）旨在重构 pKVM vCPU 状态同步机制，减少在每次世界切换时对非保护客户机状态的复制。补丁通过引入懒惰同步机制，仅在必要时才进行状态复制，从而提高性能。

2. **之前的讨论要点**：
   在之前的版本中，补丁未能有效区分保护和非保护客户机的状态同步，导致每次切换时都进行不必要的状态复制。参与者们讨论了如何通过引入 PKVM_HOST_STATE_DIRTY 标志来优化这一过程。

3. **本周的新讨论、进展或结论**：
   本周的讨论中，参与者们逐一审查了各个补丁的实现，并提出了改进建议。补丁的结构得到了进一步的清晰化，特别是对 vCPU 状态的懒惰同步进行了详细讨论。Vincent Donnefort 和其他参与者对补丁的实现给予了积极的反馈，并提出了在处理异常时如何更好地管理状态同步的建议。整体来看，补丁系列得到了认可，并在讨论中形成了更为明确的方向，预计将会在后续版本中进行调整和完善。

#### 📝 邮件列表

1. **[06-19 08:07]** [PATCH v2 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-19 08:07]** [PATCH v2 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-19 08:07]** [PATCH v2 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available
 to HYP code
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-19 08:07]** [PATCH v2 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-19 08:07]** [PATCH v2 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[06-19 08:07]** [PATCH v2 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[06-19 08:07]** [PATCH v2 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state
 during world switch
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[06-19 08:07]** [PATCH v2 7/8] KVM: arm64: Add primitives to flush/sync the VGIC
 state at EL2
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[06-19 08:07]** [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[06-19 07:21]** Re: [PATCH v2 7/8] KVM: arm64: Add primitives to flush/sync the
 VGIC state at EL2
   - 发件人: sashiko-bot@kernel.org
11. **[06-19 07:25]** Re: [PATCH v2 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
12. **[06-19 07:28]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
13. **[06-19 08:38]** Re: [PATCH v2 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[06-19 08:41]** Re: [PATCH v2 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state at EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[06-19 08:45]** Re: [PATCH v2 7/8] KVM: arm64: Add primitives to flush/sync the VGIC
 state at EL2
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[06-19 08:54]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
17. **[06-19 14:12]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[06-19 14:24]** Re: [PATCH v2 1/8] KVM: arm64: Extract MPIDR computation into a
 shared header
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
19. **[06-19 14:26]** Re: [PATCH v2 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg
 available to HYP code
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
20. **[06-19 14:29]** Re: [PATCH v2 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
21. **[06-19 14:30]** Re: [PATCH v2 4/8] KVM: arm64: Move PSCI helper functions to a
 shared header
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
22. **[06-19 14:31]** Re: [PATCH v2 5/8] KVM: arm64: Add host and hypervisor vCPU lookup
 primitives
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
23. **[06-19 17:41]** Re: [PATCH v2 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 4: [PATCH v3 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 22 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 16 Jun 2026 10:54:07 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM (Kernel-based Virtual Machine) 在 arm64 架构下的补丁系列，主要集中在将 FFA_NOTIFICATION* 调用转发到 TrustZone 的实现上。

**原始补丁内容**：
补丁系列的目标是移除 pKVM FF-A 代理中的 FFA_NOTIFICATION* 调用的阻止列表，以支持 Arm FF-A 规范中定义的异步信号机制。这些调用被标记为可选，但由于主机是唯一的非安全端点，因此转发这些通知不会引入安全风险。

**之前讨论要点**：
在历史讨论中，开发者们探讨了如何确保在转发过程中严格检查未使用参数（SBZ）以防止潜在的安全问题。补丁的多个版本中，开发者根据反馈进行了多次修改，确保了代码的健壮性和符合规范。

**本周新讨论与进展**：
本周的讨论主要集中在对各个 FFA_NOTIFICATION 调用的实现细节上，包括 FFA_NOTIFICATION_BITMAP_CREATE、FFA_NOTIFICATION_BIND、FFA_NOTIFICATION_UNBIND 等。开发者们讨论了如何在处理这些调用时进行参数验证，并确保所有未使用的参数都符合 SBZ 的要求。此外，参与者 Vincent Donnefort 提出了对补丁中某些实现的建议和问题，Sebastian Ene 对此进行了回应并表示将进行相应的修改。这表明补丁仍在不断完善中，开发者们积极沟通以确保最终实现的正确性和安全性。

#### 📝 邮件列表

1. **[06-16 10:54]** [PATCH v3 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-16 10:54]** [PATCH v3 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-16 10:54]** [PATCH v3 1/7] KVM: arm64: Support FFA_NOTIFICATION_BITMAP_CREATE in
 host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-16 10:54]** [PATCH v3 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-16 10:54]** [PATCH v3 2/7] KVM: arm64: Support FFA_NOTIFICATION_BITMAP_DESTROY in
 host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-16 10:54]** [PATCH v3 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-16 10:54]** [PATCH v3 4/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-16 10:54]** [PATCH v3 5/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-16 10:54]** [PATCH v3 6/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
10. **[06-16 10:54]** [PATCH v3 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
11. **[06-16 13:40]** Re: [PATCH v3 1/7] KVM: arm64: Support
 FFA_NOTIFICATION_BITMAP_CREATE in host handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[06-16 13:42]** Re: [PATCH v3 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls
 to Trustzone
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[06-16 13:43]** Re: [PATCH v3 2/7] KVM: arm64: Support
 FFA_NOTIFICATION_BITMAP_DESTROY in host handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[06-16 13:47]** Re: [PATCH v3 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in
 host handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[06-16 14:00]** Re: [PATCH v3 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
16. **[06-16 14:06]** Re: [PATCH v3 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host
 handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
17. **[06-16 14:26]** Re: [PATCH v3 6/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host
 handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
18. **[06-16 14:24]** Re: [PATCH v3 6/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host
 handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
19. **[06-16 14:28]** Re: [PATCH v3 1/7] KVM: arm64: Support
 FFA_NOTIFICATION_BITMAP_CREATE in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
20. **[06-16 14:30]** Re: [PATCH v3 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host
 handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
21. **[06-16 14:32]** Re: [PATCH v3 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A
 proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
22. **[06-16 14:33]** Re: [PATCH v3 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls
 to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 5: [PATCH 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection

**📧 邮件数**: 17 | **👥 参与者**: 4 | **📅 开始时间**: Sun, 14 Jun 2026 17:33:29 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM/arm64 的一系列补丁，主要目的是修复在异常注入中缺失 ESR_ELx.IL 位的问题。历史讨论中，Fuad Tabba 提出了七个补丁，强调 ARM 架构要求在多种异常情况下设置 ESR_ELx.IL 为 1，尤其是在 FPAC 和 SError 异常中。补丁的内容包括在 ERET 模拟和 SError 注入时正确设置 IL 位，以确保符合架构规范。

在之前的讨论中，参与者们指出了一些潜在的问题，例如在嵌套异常注入时构造的 SError syndrome 被静默丢弃，导致异常处理不符合预期。Sashiko AI 也提出了一些高优先级的问题，提示需要进一步审查补丁的有效性。

本周的新讨论中，Oliver Upton 对补丁的某些假设提出了质疑，认为需要更深入的验证。同时，Fuad Tabba 也指出了在非法异常返回时 PSTATE 的构造应当遵循 ARM 架构手册的规定。Marc Zyngier 表示正在着手修复相关问题，并计划在补丁中保留源异常的信息，而不是随意添加位。整体来看，讨论集中在确保补丁的正确性和符合架构要求上，参与者们积极交流以推动问题的解决。

#### 📝 邮件列表

1. **[06-14 17:33]** [PATCH 0/7] KVM: arm64: Fix missing ESR_ELx.IL in syndrome injection
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-14 17:33]** [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions during
 ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-14 17:33]** [PATCH 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-14 17:33]** [PATCH 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-14 16:44]** Re: [PATCH 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: sashiko-bot@kernel.org
6. **[06-14 16:45]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: sashiko-bot@kernel.org
7. **[06-14 16:46]** Re: [PATCH 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: sashiko-bot@kernel.org
8. **[06-14 21:46]** Re: [PATCH 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[06-15 13:42]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[06-15 13:48]** Re: [PATCH 5/7] KVM: arm64: Set IL for emulated SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[06-15 14:12]** Re: [PATCH 6/7] KVM: arm64: Set IL for nested SError injection
   - 发件人: Fuad Tabba <tabba@google.com>
12. **[06-17 13:36]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions during ERET emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[06-17 13:39]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[06-17 15:34]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions during ERET emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[06-17 15:51]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[06-18 08:59]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions during ERET emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[06-18 09:18]** Re: [PATCH 4/7] KVM: arm64: Set IL for injected FPAC exceptions
 during ERET emulation
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 6: [PATCH 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation

**📧 邮件数**: 16 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 19 Jun 2026 08:05:00 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 pKVM vCPU 状态同步的重构，包含 8 个补丁的提交。

**原始补丁内容**：该系列补丁旨在优化 pKVM 在主机与 EL2 之间的 vCPU 状态传递，减少在每次世界切换时对非保护虚拟机状态的复制。补丁引入了懒惰复制机制，仅在主机需要时才将状态同步到主机，提升性能。

**历史讨论要点**：之前的讨论集中在如何改进 pKVM 的状态管理，确保在保护虚拟机和非保护虚拟机之间的状态隔离。补丁的结构包括准备性重构、vCPU 查找原语、VGIC 状态的同步和懒惰状态同步。

**本周新讨论与进展**：本周的讨论主要围绕补丁的具体实现细节和潜在问题。参与者对补丁进行了逐一审查，提出了多个建议和问题，包括对 VGIC 状态的处理、PSCI 辅助函数的共享、以及在非保护虚拟机中实现懒惰状态同步的必要性。部分补丁获得了积极反馈，但也有一些被指出存在潜在的安全隐患和功能缺失，需进一步修正。

总体而言，本周的讨论推动了补丁的完善，确保在实现性能优化的同时，保持系统的安全性和稳定性。

#### 📝 邮件列表

1. **[06-19 08:05]** [PATCH 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-19 08:05]** [PATCH 1/8] KVM: arm64: Extract MPIDR computation into a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-19 08:05]** [PATCH 2/8] KVM: arm64: Make vcpu_{read,write}_sys_reg available to
 HYP code
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-19 08:05]** [PATCH 3/8] KVM: arm64: Factor out reusable vCPU reset helpers
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-19 08:05]** [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[06-19 08:05]** [PATCH 5/8] KVM: arm64: Add host and hypervisor vCPU lookup primitives
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[06-19 08:05]** [PATCH 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC state
 during world switch
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[06-19 08:05]** [PATCH 7/8] KVM: arm64: Add primitives to flush/sync the VGIC state
 at EL2
   - 发件人: Fuad Tabba <tabba@google.com>
9. **[06-19 08:05]** [PATCH 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[06-19 08:06]** Re: [PATCH 0/8] KVM: arm64: Rework pKVM vCPU state synchronisation
   - 发件人: Fuad Tabba <tabba@google.com>
11. **[06-19 07:16]** Re: [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared
 header
   - 发件人: sashiko-bot@kernel.org
12. **[06-19 07:22]** Re: [PATCH 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: sashiko-bot@kernel.org
13. **[06-19 08:24]** Re: [PATCH 4/8] KVM: arm64: Move PSCI helper functions to a shared header
   - 发件人: Fuad Tabba <tabba@google.com>
14. **[06-19 07:24]** Re: [PATCH 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: sashiko-bot@kernel.org
15. **[06-19 08:29]** Re: [PATCH 6/8] KVM: arm64: Minimise EL2's exposure of host VGIC
 state during world switch
   - 发件人: Fuad Tabba <tabba@google.com>
16. **[06-19 08:55]** Re: [PATCH 8/8] KVM: arm64: Implement lazy vCPU state sync for
 non-protected guests
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 7: [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 15 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 17 Jun 2026 14:51:23 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 ARM FF-A（Firmware Framework for Arm）和 KVM（Kernel-based Virtual Machine）中的内存访问描述符（EMAD）偏移计算的修复。此次讨论包含七个补丁，旨在解决在 FF-A 1.1 版本之前，内存区域头部未明确指定 EMAD 偏移的问题。

**原始问题**：在 FF-A 版本 1.1 之前，EMAD 偏移的计算假设其紧随内存区域头部，但实际上应使用 `ep_mem_offset` 字段来确定 EMAD 的起始位置。

**之前讨论要点**：在历史讨论中，参与者们关注了 EMAD 偏移计算的准确性及其对内核安全性和稳定性的影响，特别是在 pKVM 超级管理程序中的实现。

**本周新讨论及进展**：本周的讨论集中在七个补丁的具体实现上，包括：
1. 修复 EMAD 偏移计算，确保符合 FF-A 规范。
2. 增强 pKVM 超级管理程序的验证逻辑，确保描述符的偏移在邮箱缓冲区范围内。
3. 解决了多个潜在的内存越界写入问题，确保内存操作的安全性。
4. 参与者提出了对补丁的审查意见，指出了一些潜在问题和改进建议。

整体来看，本次讨论强调了内存管理的安全性和合规性，确保在新版本的 FF-A 中，内存访问描述符的处理符合最新的规范要求。

#### 📝 邮件列表

1. **[06-17 14:51]** [PATCH v7 0/7] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-17 14:51]** [PATCH v7 1/7] optee: ffa: Add NULL check in optee_ffa_lend_protmem
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-17 14:51]** [PATCH v7 2/7] firmware: arm_ffa: Fix out-of-bound writes in ffa_setup_and_transmit()
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-17 14:51]** [PATCH v7 3/7] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-17 14:51]** [PATCH v7 4/7] KVM: arm64: Fix bounds checking in do_ffa_mem_reclaim()
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-17 14:51]** [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-17 14:51]** [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-17 14:51]** [PATCH v7 7/7] KVM: arm64: Zero out the stack initialized data in the
 FFA handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-17 15:07]** Re: [PATCH v7 1/7] optee: ffa: Add NULL check in
 optee_ffa_lend_protmem
   - 发件人: sashiko-bot@kernel.org
10. **[06-17 15:18]** Re: [PATCH v7 4/7] KVM: arm64: Fix bounds checking in
 do_ffa_mem_reclaim()
   - 发件人: sashiko-bot@kernel.org
11. **[06-17 15:29]** Re: [PATCH v7 7/7] KVM: arm64: Zero out the stack initialized data
 in the FFA handler
   - 发件人: sashiko-bot@kernel.org
12. **[06-18 17:19]** Re: [PATCH v7 4/7] KVM: arm64: Fix bounds checking in
 do_ffa_mem_reclaim()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[06-18 17:56]** Re: [PATCH v7 5/7] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
14. **[06-18 18:09]** Re: [PATCH v7 6/7] KVM: arm64: Ensure FFA ranges are page aligned
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
15. **[06-18 18:14]** Re: [PATCH v7 7/7] KVM: arm64: Zero out the stack initialized data
 in the FFA handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 8: [PATCH v7 00/20] KVM: selftests: Add eventfd+VFIO IRQ test

**📧 邮件数**: 14 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 12 Jun 2026 17:20:11 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM 的补丁系列，主要集中在添加 eventfd 和 VFIO IRQ 测试的自测功能。补丁的目标是验证通过 eventfd 和真实设备（通过 VFIO 连接）进行的中断传递。最初，Sean Christopherson 希望在 7.2 版本中合并该补丁，但由于时间原因，计划在 7.3 版本早期应用，以便后续开发。

在历史讨论中，David Matlack 提出了扩展 eventfd IRQ 测试的补丁，允许使用 VFIO 设备触发中断，这样可以验证真实设备的 IRQ 传递。Sashiko AI 评审时指出了两个潜在问题，涉及 IOMMU 类型探测和 DMA 区域的硬编码。

在本周的新讨论中，David Matlack 和 Sean Christopherson 针对 DMA 区域的设置进行了深入探讨，确认大多数设备需要设置描述符以触发中断。David 还提出了对代码的修改建议，以更好地解释 DMA 区域的必要性。Sean 赞同了这些修改，并表示将添加对 send_msi() 的检查，以确保与其他补丁的兼容性。

总体来看，本周的讨论集中在补丁的细节和潜在问题上，参与者们积极交流以优化代码实现。

#### 📝 邮件列表

1. **[06-12 17:20]** [PATCH v7 00/20] KVM: selftests: Add eventfd+VFIO IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[06-12 17:20]** [PATCH v7 09/20] KVM: selftests: Add VFIO device support to eventfd
 IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[06-13 00:35]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: sashiko-bot@kernel.org
4. **[06-15 08:56]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: David Matlack <dmatlack@google.com>
5. **[06-15 11:05]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
6. **[06-15 11:32]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: David Matlack <dmatlack@google.com>
7. **[06-15 12:22]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
8. **[06-15 13:04]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: David Matlack <dmatlack@google.com>
9. **[06-16 17:07]** Re: [PATCH v7 11/20] KVM: arm64: Enforce PMU event filter at
 vcpu_load()
   - 发件人: wuyifan <wuyifan50@huawei.com>
10. **[06-18 09:53]** Re: [PATCH v7 15/20] perf: arm_pmuv3: Handle IRQs for Partitioned PMU
 guest counters
   - 发件人: wuyifan <wuyifan50@huawei.com>
11. **[06-18 20:21]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: David Matlack <dmatlack@google.com>
12. **[06-18 14:42]** Re: [PATCH v7 09/20] KVM: selftests: Add VFIO device support to
 eventfd IRQ test
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[06-18 23:30]** Re: [PATCH v7 11/20] KVM: arm64: Enforce PMU event filter at vcpu_load()
   - 发件人: Colton Lewis <coltonlewis@google.com>
14. **[06-18 23:32]** Re: [PATCH v7 15/20] perf: arm_pmuv3: Handle IRQs for Partitioned PMU
 guest counters
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 9: [PATCH kvmtool 0/4] Add support for running protected VMs on arm64

**📧 邮件数**: 12 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 19 Jun 2026 12:54:10 +0100

#### 🤖 AI 总结

本邮件线程讨论了对 arm64 平台上运行受保护虚拟机的支持，主要由 Will Deacon 提出了一系列补丁（共四个）。这些补丁旨在为启用 pKVM 的系统提供支持，尽管该功能尚未完全实现，但对于开发和测试非常有用。

**原始补丁内容**：补丁包括添加一个新的命令行参数 `--protected`，用于请求创建受保护的虚拟机类型，并在设备树中宣传一个保留的 DMA 区域，以便通过共享内存窗口进行 virtio 传输。

**之前讨论要点**：邮件中并未有历史讨论的内容，但补丁的提出是基于对 pKVM 功能的需求，强调了在开发过程中对 kvmtool 支持的重要性。

**本周新讨论与进展**：在本周的讨论中，参与者对每个补丁进行了测试和审核。Fuad Tabba 对所有补丁进行了测试并给予了正面反馈，指出在使用旧内核时可能会无声地丢弃 `--protected` 参数，建议在此情况下使用 `die()` 函数来处理错误。此外，Suzuki K Poulose 也对补丁进行了审核，确认其在 CCA 环境下的有效性。整体来看，补丁得到了积极的响应，表明该功能的实现正在稳步推进。

#### 📝 邮件列表

1. **[06-19 12:54]** [PATCH kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Will Deacon <will@kernel.org>
2. **[06-19 12:54]** [PATCH kvmtool 1/4] Sync kernel UAPI headers with v7.1
   - 发件人: Will Deacon <will@kernel.org>
3. **[06-19 12:54]** [PATCH kvmtool 2/4] virtio: Factor out base features for modern virtio transports
   - 发件人: Will Deacon <will@kernel.org>
4. **[06-19 12:54]** [PATCH kvmtool 3/4] virtio: Add helper for enabling VIRTIO_F_ACCESS_PLATFORM
   - 发件人: Will Deacon <will@kernel.org>
5. **[06-19 12:54]** [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
6. **[06-19 14:04]** Re: [PATCH kvmtool 0/4] Add support for running protected VMs on arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[06-19 14:15]** Re: [PATCH kvmtool 1/4] Sync kernel UAPI headers with v7.1
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[06-19 14:15]** Re: [PATCH kvmtool 2/4] virtio: Factor out base features for modern
 virtio transports
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[06-19 14:21]** Re: [PATCH kvmtool 3/4] virtio: Add helper for enabling VIRTIO_F_ACCESS_PLATFORM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[06-19 14:49]** Re: [PATCH kvmtool 4/4] arm64: Add support for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[06-19 17:35]** Re: [PATCH kvmtool 2/4] virtio: Factor out base features for modern
 virtio transports
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[06-19 17:36]** Re: [PATCH kvmtool 3/4] virtio: Add helper for enabling
 VIRTIO_F_ACCESS_PLATFORM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 10: [PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 12 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 16 Jun 2026 15:41:42 +0000

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone”，主要涉及将FF-A通知调用转发到TrustZone。原始patch的目的是移除pKVM FF-A代理中的FFA_NOTIFICATION*调用的阻止列表，以支持根据Arm FF-A规范定义的异步信号机制。

在历史讨论中，参与者们关注了这些调用被阻止的原因，认为由于主机是唯一的非安全端点，并且这些调用不涉及内存指针或地址，因此没有必要阻止它们。之前的讨论还涉及了对参数的严格检查和对不同调用的处理。

本周的讨论中，Sebastian Ene提交了一系列补丁（共7个），逐步实现了对FF-A通知调用的支持，包括FFA_NOTIFICATION_BIND、FFA_NOTIFICATION_UNBIND、FFA_NOTIFICATION_SET、FFA_NOTIFICATION_GET等。每个补丁都强调了对参数的严格检查，确保遵循MBZ/SBZ字段的要求。此外，Sashiko AI的审查反馈指出了一些潜在问题，如MBZ检查不完整和参数验证错误，参与者对此进行了讨论和修正。

总体而言，本周的进展集中在增强FF-A通知的处理能力和确保安全性方面，同时也引入了对代码质量的审查和改进。

#### 📝 邮件列表

1. **[06-16 15:41]** [PATCH v4 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[06-16 15:41]** [PATCH v4 1/7] KVM: arm64: Enforce strict SBZ checks in the FF-A proxy
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[06-16 15:41]** [PATCH v4 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP calls to Trustzone
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[06-16 15:41]** [PATCH v4 3/7] KVM: arm64: Support FFA_NOTIFICATION_BIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[06-16 15:41]** [PATCH v4 4/7] KVM: arm64: Support FFA_NOTIFICATION_UNBIND in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[06-16 15:41]** [PATCH v4 5/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
7. **[06-16 15:41]** [PATCH v4 6/7] KVM: arm64: Support FFA_NOTIFICATION_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[06-16 15:41]** [PATCH v4 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in host handler
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[06-16 15:54]** Re: [PATCH v4 5/7] KVM: arm64: Support FFA_NOTIFICATION_SET in host
 handler
   - 发件人: sashiko-bot@kernel.org
10. **[06-16 15:58]** Re: [PATCH v4 2/7] KVM: arm64: Forward FFA_NOTIFICATION_BITMAP
 calls to Trustzone
   - 发件人: sashiko-bot@kernel.org
11. **[06-16 16:00]** Re: [PATCH v4 1/7] KVM: arm64: Enforce strict SBZ checks in the
 FF-A proxy
   - 发件人: sashiko-bot@kernel.org
12. **[06-16 16:03]** Re: [PATCH v4 7/7] KVM: arm64: Support FFA_NOTIFICATION_INFO_GET in
 host handler
   - 发件人: sashiko-bot@kernel.org

---

### Thread 11: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before
 migrating it

**📧 邮件数**: 10 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 5 Jun 2026 05:59:15 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的 VGIC（Virtual Generic Interrupt Controller）中，如何在迁移中检查中断是否仍属于当前 vCPU 的问题。最初的 patch 由 Hyunwoo Kim 提出，目的是在迁移中断到另一个 vCPU 之前，确保该中断仍然属于当前 vCPU，以避免潜在的竞态条件。

在历史讨论中，参与者们探讨了中断迁移过程中可能存在的竞态条件，特别是当一个 vCPU 修改另一个 vCPU 的中断状态时，可能导致中断状态不一致的问题。Marc Zyngier 提出了关于清除挂起状态的潜在问题，并讨论了如何处理这些状态以避免数据丢失。

在本周的新讨论中，Hyunwoo Kim 确认了之前的补丁修复了相关问题，并建议提交该补丁。Marc Zyngier 随后表示已将该补丁应用于修复列表，并感谢参与者的贡献。最终，该补丁成功提交并应用，标志着讨论的圆满结束。

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
5. **[06-10 22:52]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours
 before migrating it
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
6. **[06-10 17:00]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before migrating it
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[06-12 11:22]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours
 before migrating it
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
8. **[06-14 16:16]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before migrating it
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[06-15 14:43]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours
 before migrating it
   - 发件人: Hyunwoo Kim <imv4bel@gmail.com>
10. **[06-17 12:51]** Re: [PATCH] KVM: arm64: vgic: Check the interrupt is still ours before migrating it
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner

**📧 邮件数**: 10 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 10 Jun 2026 18:17:26 -0700

#### 🤖 AI 总结

本邮件线程讨论的主题是针对 KVM 自测工具的补丁（PATCH v4 1/9），旨在创建一个 KVM 自测运行器。补丁的核心内容是实现一个能够运行自测用例的工具，并在终端支持的情况下提供彩色输出。

在历史讨论中，参与者们主要关注如何处理测试用例的定义与执行。Ackerley Tng 和 Sean Christopherson 就测试用例的静态定义与动态发现进行了深入探讨，强调静态定义的优势在于能够清晰地显示测试跳过的情况，而动态定义可能导致测试用例的缺失。此外，讨论中还提到在不同环境下如何处理输出的颜色显示。

在本周的新讨论中，Ackerley Tng 对于输出颜色的处理提出了改进方案，包括根据环境变量控制是否打印颜色。Vipin Sharma 则建议参考 `grep` 的输出选项，进一步简化输出逻辑。此外，参与者们还讨论了使用函数式编程替代面向对象编程的可能性，以减少代码的复杂性和冗余。

总体来看，本周的讨论集中在如何优化测试运行器的设计与输出逻辑，确保其在不同环境下的兼容性和易用性。

#### 📝 邮件列表

1. **[06-10 18:17]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Ackerley Tng <ackerleytng@google.com>
2. **[06-11 12:08]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[06-11 13:16]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Ackerley Tng <ackerleytng@google.com>
4. **[06-11 18:07]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[06-12 12:45]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Ackerley Tng <ackerleytng@google.com>
6. **[06-12 16:56]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Sean Christopherson <seanjc@google.com>
7. **[06-16 09:15]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Ackerley Tng <ackerleytng@google.com>
8. **[06-16 11:29]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
9. **[06-16 14:43]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
10. **[06-16 16:04]** Re: [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

### Thread 13: [PATCH v3 0/5] KVM: arm64: nv: Even more VNCR fixes

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 18 Jun 2026 16:42:01 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上 VNCR（Virtual Nested Context Register）相关问题的修复补丁（PATCH v3 0/5）。该补丁主要解决了在处理 VNCR 时的一系列错误，特别是与权限和内存映射相关的问题。

历史讨论中，之前的版本（v2）已经提出了一些问题和反馈，但未能完全解决。例如，Sashiko 提到的 HWPOISON PFNs 未能正确信号用户空间的问题仍未处理。补丁的目标是通过改进 VNCR 的权限检查和错误处理来增强系统的稳定性。

在本周的新讨论中，Oliver Upton 提出了五个补丁，主要改进内容包括：
1. 修复 L1 VNCR 映射时对只读 PFN 的处理，确保 VNCR 只使用只读映射。
2. 在无法解析 PFN 时注入 SEA（Synchronous External Abort）。
3. 在注入中断之前重新翻译 VNCR，以满足 FEAT_ETS2/3 的顺序要求。
4. 拒绝非内存的 VNCR 映射，避免潜在的错误。
5. 对于意外的 VNCR 中断，将虚拟机标记为错误状态并退出到用户空间。

此外，Sashiko AI 也对补丁提出了一些潜在问题的反馈，强调了在处理内存故障和权限错误时的注意事项。整体来看，本周的讨论集中在进一步完善 VNCR 的错误处理机制和内存映射逻辑上。

#### 📝 邮件列表

1. **[06-18 16:42]** [PATCH v3 0/5] KVM: arm64: nv: Even more VNCR fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-18 16:42]** [PATCH v3 1/5] KVM: arm64: nv: Respect read-only PFN when mapping L1 VNCR
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-18 16:42]** [PATCH v3 2/5] KVM: arm64: nv: Inject SEA if kvm_translate_vncr() can't resolve PFN
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-18 16:42]** [PATCH v3 3/5] KVM: arm64: nv: Re-translate VNCR before injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-18 16:42]** [PATCH v3 4/5] KVM: arm64: nv: Inject SEA if guest VNCR isn't normal memory
   - 发件人: Oliver Upton <oupton@kernel.org>
6. **[06-18 16:42]** [PATCH v3 5/5] KVM: arm64: nv: Mark VM as bugged for unexpected VNCR abort
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[06-18 23:57]** Re: [PATCH v3 2/5] KVM: arm64: nv: Inject SEA if
 kvm_translate_vncr() can't resolve PFN
   - 发件人: sashiko-bot@kernel.org
8. **[06-19 00:00]** Re: [PATCH v3 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: sashiko-bot@kernel.org
9. **[06-19 00:07]** Re: [PATCH v3 1/5] KVM: arm64: nv: Respect read-only PFN when
 mapping L1 VNCR
   - 发件人: sashiko-bot@kernel.org

---

### Thread 14: [PATCH kvmtool v2 0/7] x86 compilation fixes and arm64 PMU improvements

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 18 Jun 2026 16:49:54 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 工具的多个补丁（PATCH），主要集中在 x86 编译修复和 arm64 PMU（性能监控单元）改进方面。

1. **原始补丁/问题的内容**：补丁 v2 的主要目的是修复编译错误，特别是在 `disk/core.c` 和 `x86/include/kvm/bios.h` 中出现的常量字符串修改问题，以及改进 PMU 的初始化和错误报告。

2. **之前的讨论要点**：在补丁 v1 中，主要修复了 `disk/core.c` 中的常量字符串问题。补丁 v2 进一步修复了 `bios.h` 中的 `regparm` 属性错误，并确保 PMU 的初始化在 GIC 初始化之后进行，以避免因编译顺序变化导致的错误。

3. **本周的新讨论、进展或结论**：本周的讨论中，Alexandru Elisei 提交了七个补丁，具体包括：
   - 修复了 x86 32 位模式下的 `bioscall` 定义问题。
   - 修改了 `virtio_9p_rootdir_parser` 和 `disk_img_name_parser` 函数，以避免对常量字符串的修改。
   - 改进了 arm64 的 PMU 初始化顺序，并在错误报告中提供更详细的信息。
   - 更新了 `die_perror` 函数，使其能够返回 errno，并允许格式化字符串输入。

此外，Oliver Upton 提出了对错误处理代码的清理建议，建议使用宏来简化重复的错误处理逻辑。整体来看，这些补丁旨在提高代码的稳定性和可维护性。

#### 📝 邮件列表

1. **[06-18 16:49]** [PATCH kvmtool v2 0/7] x86 compilation fixes and arm64 PMU improvements
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[06-18 16:49]** [PATCH kvmtool v2 1/7] x86: Define bioscall only in 32-bit mode
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[06-18 16:49]** [PATCH kvmtool v2 2/7] virtio: Do not modify const strings in virtio_9p_rootdir_parser()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[06-18 16:49]** [PATCH kvmtool v2 3/7] disk/core: Do not modify const strings in disk_img_name_parser()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
5. **[06-18 16:49]** [PATCH kvmtool v2 4/7] arm64: Initialise the PMU after the GIC
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
6. **[06-18 16:49]** [PATCH kvmtool v2 5/7] util: Set exit status to errno in die_perror()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
7. **[06-18 16:50]** [PATCH kvmtool v2 6/7] util: Allow die_perror() to take a variable list of argument
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
8. **[06-18 16:50]** [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL diagnostics
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
9. **[06-18 12:06]** Re: [PATCH kvmtool v2 7/7] arm64: Improve KVM_ARM_VCPU_PMU_V3_CTRL
 diagnostics
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 15: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 17 Jun 2026 15:49:07 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH] KVM: arm64: nv: 修复非法异常返回时的 PSTATE 构造”，主要讨论了在 KVM 的 ARM64 虚拟化环境中，如何正确处理非法异常返回时的 PSTATE（处理器状态寄存器）构造。

**原始 patch/问题的内容**：
该 patch 旨在修复在非法异常返回时，PSTATE 的构造不正确的问题。具体来说，现有实现从当前 PSTATE 中获取标志和掩码，而不是从返回的 SPSR（状态寄存器）中获取。修复后的实现将从 SPSR 中获取标志，同时保持当前 PSTATE 的某些字段不变。

**之前讨论要点**：
在之前的讨论中，参与者们对如何处理非法异常返回时 PSTATE 的各个字段进行了深入探讨，特别是关于哪些字段应被视为“未知”而不应保留。Marc Zyngier 和 Fuad Tabba 对 ARM 架构参考手册的解读达成一致，认为在非法返回时某些字段应被设置为 0。

**本周的新讨论、进展或结论**：
本周的讨论集中在对 patch 的修改和优化上。Fuad Tabba 提出了对 Marc Zyngier 提供的初始 patch 进行结构上的改进，采用了更清晰的两步掩码处理方式。最终，Marc Zyngier 表示满意，并将修改后的 patch 应用到代码库中，标记为修复提交。整体讨论显示出团队成员之间的良好协作和对代码质量的重视。

#### 📝 邮件列表

1. **[06-17 15:49]** [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-17 15:04]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal
 exception return
   - 发件人: sashiko-bot@kernel.org
3. **[06-17 16:29]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal
 exception return
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-17 17:23]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-17 17:45]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[06-17 18:19]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal
 exception return
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[06-17 18:32]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[06-17 18:36]** Re: [PATCH] KVM: arm64: nv: Fix PSTATE construction on illegal exception return
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 16: [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 12 Jun 2026 15:22:41 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于为 pKVM/nVHE 虚拟机监控器添加 `trace_hyp_printk()` 功能的补丁系列。该补丁旨在允许开发者将信息记录到虚拟机监控器的追踪缓冲区，类似于内核中的 `trace_printk()` 函数，从而增强调试能力，尤其是在 Android 的 pKVM 中。

在历史讨论中，Vincent Donnefort 提出了这一补丁系列，并进行了初步测试，确认在 QEMU 环境下的功能正常。Fuad Tabba 对补丁进行了审查，并提出了一些建议和改进意见，最终确认了补丁的有效性。

在本周的新讨论中，Vincent 和 Fuad 继续交流了对 hVHE 模式的测试结果，Vincent 表示他会再次尝试并反馈。Fuad 确认了之前的测试是由于用户错误导致的问题，并表示他的测试结果涵盖了整个补丁系列。Fuad 还提到将会在后续版本中添加一些小改动。

总体来看，本周的讨论主要集中在对补丁的进一步测试和确认上，参与者们对补丁的功能表示认可，并计划在未来的版本中进行改进。

#### 📝 邮件列表

1. **[06-12 15:22]** [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[06-12 15:22]** [PATCH v1 4/4] KVM: arm64: Add hyp_printk event to nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[06-14 13:57]** Re: [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-14 16:25]** Re: [PATCH v1 4/4] KVM: arm64: Add hyp_printk event to nVHE/pKVM hyp
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-15 09:27]** Re: [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[06-15 09:29]** Re: [PATCH v1 4/4] KVM: arm64: Add hyp_printk event to nVHE/pKVM hyp
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[06-15 09:30]** Re: [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[06-15 09:57]** Re: [PATCH v1 0/4] trace_hyp_printk() for pKVM/nVHE hypervisor
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 17: [PATCH v2 0/2] KVM: arm64: Fix MPIDR lookup for unreset vCPUs

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 11 Jun 2026 22:40:40 +0800

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在修复未重置虚拟 CPU（vCPU）时的 MPIDR（多处理器 ID 寄存器）查找问题。

**原始补丁内容**：
补丁的核心问题是，当创建支持 CPU 热插拔的虚拟机时，未重置的 vCPU 仍然具有零的 MPIDR_EL1 状态，这会导致 MPIDR 0 的查找返回错误的 vCPU，从而影响中断的正确传递，可能导致虚拟机启动缓慢。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 指出，KVM 并不支持 vCPU 热插拔，因此问题与热插拔无关，而是与未经过初始化的 vCPU 相关。此外，讨论中提到 MPIDR 值的检查可能存在问题，因为用户空间可以随意写入寄存器，这可能导致冲突。

**本周的新讨论与进展**：
本周的讨论中，Oliver Upton 和 Marc Zyngier 对补丁提出了进一步的建议，认为在处理 MPIDR 时，需要考虑用户空间可能引入的冲突。Fuqiang Wang 提出了在初始化函数中检测冲突并通知用户空间的想法，但 Marc Zyngier 指出，这种方式并不能有效地提醒用户。因此，讨论的重点转向如何更好地处理用户空间的非合规行为，以避免潜在的性能问题和系统不稳定。整体来看，讨论仍在探索最佳解决方案，以确保 KVM 的稳定性和性能。

#### 📝 邮件列表

1. **[06-11 22:40]** [PATCH v2 0/2] KVM: arm64: Fix MPIDR lookup for unreset vCPUs
   - 发件人: fuqiang wang <fuqiang.wng@gmail.com>
2. **[06-11 22:40]** [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup table
   - 发件人: fuqiang wang <fuqiang.wng@gmail.com>
3. **[06-14 10:26]** Re: [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup table
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-14 21:20]** Re: [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup
 table
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[06-15 11:08]** Re: [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup table
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[06-18 19:38]** Re: [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup
 table
   - 发件人: fuqiang wang <fuqiang.wng@gmail.com>
7. **[06-18 13:32]** Re: [PATCH v2 2/2] KVM: arm64: Skip unreset vCPUs in MPIDR lookup table
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 18: [PATCH 0/3] KVM: arm64: pKVM is_created cleanup

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 18 Jun 2026 10:01:25 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构下的 pKVM（保护 KVM）相关的代码清理工作，主要集中在 `is_created` 标志的处理上。

1. **原始 patch/问题的内容**：Fuad Tabba 提出了一个包含三个补丁的系列，旨在清理主机端的 `kvm->arch.pkvm.is_created` 标志，该标志用于跟踪虚拟机是否已在超管层（EL2）实例化。补丁的主要目的是移除与该标志相关的冗余或无用代码，而不影响任何功能路径。

2. **之前的讨论要点**：在历史讨论中并未提及具体的补丁或问题背景，但可以推测，此次清理工作是为了配合正在进行的 pKVM 上游工作，确保代码的整洁和可维护性。

3. **本周的新讨论、进展或结论**：本周的讨论中，Fuad 提出了三个具体的补丁，分别是：移除未使用的 EL2 端 `is_created` 写入、删除在 `pkvm_init_host_vm()` 中的不可达早期检查，以及去除 `pkvm_hyp_vm_is_created()` 中冗余的 `READ_ONCE()` 调用。参与者 Keir Fraser 对整个补丁系列进行了审核并表示认可。此外，Sashiko AI 发现了一个潜在的问题，但 Fuad 解释了内存回收的顺序，表明并不存在内存泄漏的问题。

总体而言，本周的讨论集中在代码清理和优化上，确保 pKVM 的实现更加高效和可靠。

#### 📝 邮件列表

1. **[06-18 10:01]** [PATCH 0/3] KVM: arm64: pKVM is_created cleanup
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-18 10:01]** [PATCH 1/3] KVM: arm64: Drop the unused EL2-side is_created write
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-18 10:01]** [PATCH 2/3] KVM: arm64: Remove unreachable early checks in pkvm_init_host_vm()
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-18 10:01]** [PATCH 3/3] KVM: arm64: Drop redundant READ_ONCE() in pkvm_hyp_vm_is_created()
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[06-18 09:22]** Re: [PATCH 3/3] KVM: arm64: Drop redundant READ_ONCE() in
 pkvm_hyp_vm_is_created()
   - 发件人: sashiko-bot@kernel.org
6. **[06-18 10:40]** Re: [PATCH 3/3] KVM: arm64: Drop redundant READ_ONCE() in pkvm_hyp_vm_is_created()
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[06-18 10:06]** Re: [PATCH 0/3] KVM: arm64: pKVM is_created cleanup
   - 发件人: Keir Fraser <keirf@google.com>

---

### Thread 19: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception into a pVM

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 12 Jun 2026 12:34:14 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主要目的是在向受保护的虚拟机（pVM）注入异常时同步 SPSR_EL1 寄存器。

**原始补丁内容**：Fuad Tabba 提出的补丁旨在解决在 pKVM 向受保护的虚拟机注入同步异常时，未能将 SPSR_EL1 寄存器的值写入硬件的问题。补丁建议在处理异常时，除了写入 ESR_EL1 和 ELR_EL1 外，也应同步 SPSR_EL1，以避免虚拟机读取到过时的 PSTATE。

**之前讨论要点**：在历史讨论中，Fuad 指出当前的实现仅在内存中设置 SPSR_EL1，而未能将其写入硬件，可能导致虚拟机在异常处理时恢复错误的状态。Will Deacon 对此表示担忧，并询问是否在异常注入路径中未初始化 SPSR_EL1。

**本周新讨论与进展**：在本周的讨论中，Fuad 和 Will 进一步澄清了补丁的必要性，确认了在异常注入过程中，虽然其他寄存器的值会被正确写入硬件，但 SPSR_EL1 的更新仍然被遗漏。最终，Will 表示认可补丁，并确认了其有效性。Marc Zyngier 最后表示已将补丁应用于修复中，标志着该问题的解决。

#### 📝 邮件列表

1. **[06-12 12:34]** [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception into a pVM
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-15 11:05]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception
 into a pVM
   - 发件人: Will Deacon <will@kernel.org>
3. **[06-15 11:52]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception
 into a pVM
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[06-15 15:41]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception
 into a pVM
   - 发件人: Will Deacon <will@kernel.org>
5. **[06-15 16:03]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception
 into a pVM
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[06-15 16:10]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception
 into a pVM
   - 发件人: Will Deacon <will@kernel.org>
7. **[06-17 13:41]** Re: [PATCH] KVM: arm64: Sync SPSR_EL1 when injecting an exception into a pVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 20: [PATCH v2 0/3] Optimize S2 page splitting

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 18 Jun 2026 14:14:41 +0100

#### 🤖 AI 总结

本邮件讨论的主题是针对 S2 页面拆分的优化，包含三个补丁（patch），旨在提升 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的性能。

1. **原始 patch/问题的内容**：补丁的主要目的是通过引入新的遍历标志，优化页面表的遍历过程，跳过不必要的页面表级别，从而提高性能。具体来说，当遍历到某一层级的条目时，可以推断出其父级条目已经被拆分，从而避免对所有条目的逐一遍历。

2. **之前讨论要点**：在之前的讨论中，开发者发现即使某些条目已经拆分，系统仍会遍历所有条目，导致性能下降。优化的方向是减少不必要的遍历，特别是在处理脏位跟踪时，能够显著提升性能。

3. **本周的新讨论、进展或结论**：本周的讨论中，Leonardo Bras 提出了三个补丁，分别是避免重复测试遍历、引入新的遍历标志以跳过特定级别的条目，以及在拆分过程中跳过不必要的遍历。测试结果显示，优化后的补丁在多种场景下都显著降低了运行时间，最高可达 44% 的性能提升。此外，开发者对补丁进行了细致的修改和测试，确保其在实际硬件上的有效性。

总的来说，本周的讨论集中在如何通过优化页面表的遍历来提升 KVM 的性能，补丁的实施和测试结果均表明了其有效性。

#### 📝 邮件列表

1. **[06-18 14:14]** [PATCH v2 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[06-18 14:14]** [PATCH v2 1/3] KVM: arm64: Avoid re-testing walk_continue
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[06-18 14:14]** [PATCH v2 2/3] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[06-18 14:14]** [PATCH v2 3/3] KVM: arm64: Make stage2_split_walker() skip unnecessary walks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[06-18 15:38]** Re: [PATCH v2 0/3] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 21: [PATCH] KVM: arm64: Handle race between interrupt affinity change and LPI disabling

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 15 Jun 2026 19:16:25 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构下处理中断亲和性变化与 LPI（Local Peripheral Interrupt）禁用之间的竞争条件的补丁。原始补丁由 Marc Zyngier 提交，旨在解决在特定情况下可能出现的严重竞争问题，例如当一个虚拟 CPU（vcpu）正在禁用另一个 vcpu 的 LPIs 时，可能导致中断被意外释放，从而引发使用后释放（Use-After-Free）错误。

在之前的讨论中，Marc 提出了补丁的两项主要修复措施：在释放锁之前对中断进行引用计数，并避免在锁释放期间处理待处理位的迁移。此补丁的目的是确保在安全移除中断时，它仍然存在。

本周的新讨论中，参与者们对补丁进行了进一步的审查和讨论。Sashiko AI 机器人指出了潜在的并发中断注入问题，Oliver Upton 认为需要在现有补丁基础上增加 Hyunwoo 的补丁，以防止三方竞争条件的发生。Marc 也表示需要考虑使用类似于 MMU 通知序列号的机制，以检查在两个锁定区域之间 AP 列表是否发生变化。最终，Marc 确认该补丁已被应用于修复中。

#### 📝 邮件列表

1. **[06-15 19:16]** [PATCH] KVM: arm64: Handle race between interrupt affinity change and LPI disabling
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[06-15 18:33]** Re: [PATCH] KVM: arm64: Handle race between interrupt affinity
 change and LPI disabling
   - 发件人: sashiko-bot@kernel.org
3. **[06-16 11:51]** Re: [PATCH] KVM: arm64: Handle race between interrupt affinity
 change and LPI disabling
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-17 11:35]** Re: [PATCH] KVM: arm64: Handle race between interrupt affinity change and LPI disabling
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[06-17 12:51]** Re: [PATCH] KVM: arm64: Handle race between interrupt affinity change and LPI disabling
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 22: [PATCH RESEND v2 0/5] KVM: arm64: nv: Even more VNCR fixes

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  9 Jun 2026 11:55:09 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下 VNCR（Virtual Non-Canonical Register）相关问题的修复补丁，特别是针对 VNCR 的错误处理和映射问题。

在历史讨论中，Oliver Upton 提出了多个补丁，主要包括：在主机的 stage-1 映射 VNCR 时，需要在写入之前将 PFN（Page Frame Number）故障引入；防止 KVM 映射非内存 PFN 的缓存映射；以及在 VNCR 发生中断时重新翻译 VNCR，以满足 FEAT_ETS2 的顺序要求。Wei-Lin Chang 也提到，代码的复杂性使得理解和处理错误变得困难，尤其是在 kvm_translate_vncr 函数中。

在本周的新讨论中，Oliver 对 Wei-Lin 的评论进行了回应，表示对于“正常”行为返回错误代码的方式非常难以处理。他建议进一步重构软件的页表查找（PTW）机制，使其仅在需要向用户空间报告时返回错误，而在由于来宾行为导致的中断情况下，理想情况下应返回 1，并检查查找结果以区分成功与中断的翻译。

总体来看，本周的讨论集中在如何简化错误处理和提高代码可读性上，反映了对 KVM VNCR 处理的持续关注和改进。

#### 📝 邮件列表

1. **[06-09 11:55]** [PATCH RESEND v2 0/5] KVM: arm64: nv: Even more VNCR fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-09 11:55]** [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-10 14:46]** Re: [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[06-18 14:52]** Re: [PATCH RESEND v2 3/5] KVM: arm64: nv: Re-translate VNCR before
 injecting abort
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 23: [PATCH v1 1/2] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 10 Jun 2026 21:21:08 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中为 arm64 架构引入新的页表遍历标志 KVM_PGTABLE_WALK_SKIP_LEVEL* 的补丁（patch）。该补丁的目的是允许在遍历页表时跳过较低级别的页表，从而提高性能。

在历史讨论中，Leonardo Bras 提出了该补丁，并在后续的反馈中，Sashiko AI 机器人指出了几个潜在问题，包括：组合跳过标志可能导致忽略更严格的跳过级别、跳过页表级别会破坏预处理和后处理回调的对称性，以及跳过根级别的逻辑无法有效防止访问根级别。

在本周的新讨论中，Leonardo Bras 针对 Sashiko AI 的反馈进行了回应，确认了需要将代码中的 fls() 替换为 ffs()，以确保选择最低级别而非最高级别。他还提出了修复方案，以确保在启用跳过级别时，仍然能够调用后处理回调。此外，他对 SKIP_LEVEL0 的实用性提出了疑问，认为如果根级别为 -1，跳过根级别的意义不大。

总体而言，本周的讨论集中在对补丁的细节修正和潜在问题的解决方案上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[06-10 21:21]** [PATCH v1 1/2] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[06-10 20:30]** Re: [PATCH v1 1/2] KVM: arm64: Introduce
 KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: sashiko-bot@kernel.org
3. **[06-17 14:30]** Re: [PATCH v1 1/2] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[06-18 15:38]** Re: [PATCH v1 1/2] KVM: arm64: Introduce KVM_PGTABLE_WALK_SKIP_LEVEL* walk flags
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 24: [PATCH] KVM: arm64: Add Fuad Tabba as a reviewer

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 17 Jun 2026 14:12:36 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于将 Fuad Tabba 添加为 KVM/arm64 的审阅者。Fuad Tabba 表示他在 KVM/arm64 领域工作多年，主要集中在 pKVM 上，目前正在上游支持受保护的客户机，并希望以官方身份继续审查 KVM/arm64 的补丁。因此，他提交了一个补丁，将自己添加到 KVM/arm64 的审阅者列表中。

在之前的讨论中，参与者 Oliver Upton 和 Marc Zyngier 对此补丁表示支持，Oliver 给予了确认（Ack），并期待 Fuad 能尽快参与审查工作。Marc 也指出该补丁在当前的 kvmarm/fixes 树中未能应用，因为缺少 Steffen 的信息，并表示已对此进行了修复。

在本周的新讨论中，Marc Zyngier 最终确认该补丁已被应用到 fixes 中，并感谢 Fuad 的贡献。这一进展标志着 Fuad Tabba 正式成为 KVM/arm64 的审阅者，进一步增强了该项目的审查能力。

#### 📝 邮件列表

1. **[06-17 14:12]** [PATCH] KVM: arm64: Add Fuad Tabba as a reviewer
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-17 10:29]** Re: [PATCH] KVM: arm64: Add Fuad Tabba as a reviewer
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-17 18:42]** Re: [PATCH] KVM: arm64: Add Fuad Tabba as a reviewer
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[06-17 18:43]** Re: [PATCH] KVM: arm64: Add Fuad Tabba as a reviewer
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 25: [PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in kvm_hyp_handle_mops()

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 16 Jun 2026 19:49:44 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构上处理嵌套虚拟化时的补丁，主题为“[PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in kvm_hyp_handle_mops()”。

**原始补丁内容**：
补丁旨在修复在嵌套虚拟化环境中，处理 MOPS（Memory Operation Exception）异常时，未能将虚拟 EL2（vEL2）的 PSTATE 正确转换为 EL1 的问题。具体来说，kvm_hyp_handle_mops() 函数在快速重入路径中直接将 vcpu_cpsr() 的值写入硬件 SPSR_EL2，而未进行必要的转换，可能导致安全漏洞。

**之前讨论要点**：
在历史讨论中，未提及具体的补丁或问题，但可以推测该问题的背景与 KVM 的嵌套虚拟化实现有关，尤其是在处理异常时的状态管理。

**本周的新讨论与进展**：
本周的讨论中，Weiming Shi 提出了补丁，并详细描述了问题的重现步骤和潜在的安全风险。Oliver Upton 对补丁进行了审查，建议简化补丁的变更日志，并提出直接操作 SPSR_EL2 的方法，以避免使用合成状态。最后，Weiming Shi 表示将根据反馈更新补丁版本。整体来看，本周的讨论集中在对补丁的细节审查和改进建议上，显示出对安全性的高度关注。

#### 📝 邮件列表

1. **[06-16 19:49]** [PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in kvm_hyp_handle_mops()
   - 发件人: Weiming Shi <bestswngs@gmail.com>
2. **[06-16 20:03]** Re: [PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in
 kvm_hyp_handle_mops()
   - 发件人: Weiming Shi <bestswngs@gmail.com>
3. **[06-16 13:14]** Re: [PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in
 kvm_hyp_handle_mops()
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[06-17 10:52]** Re: [PATCH] KVM: arm64: nv: Translate vEL2 PSTATE to EL1 in kvm_hyp_handle_mops()
   - 发件人: swing sze <bestswngs@gmail.com>

---

### Thread 26: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 1 Jun 2026 14:28:34 +0000

#### 🤖 AI 总结

本邮件线程讨论的是一个针对 ARM CPU 的补丁（PATCH v5 04/18），其目的是增加处理生成的 ID 寄存器定义的基础设施。

在历史讨论中，Shameer Kolothum Thodi 指出该补丁缺少必要的文件 `target/arm/cpu-sysreg-properties.c`，并请求 Eric Auger 进行检查。Eric 随后回应，表示补丁的提交描述已过时，因为他已经迁移到 Khushit 对 ID 寄存器及其字段的描述，指出不再需要某些列表和函数，并提到相关数组将在后续的补丁（PATCH v5 08/18）中生成。

在本周的新讨论中，Shameer 对之前的讨论表示理解，并感谢 Eric 的解释。Eric 也在另一封邮件中提到他已修复了与 ID 寄存器属性相关的代码，添加了写入部分，显示出对补丁的进一步完善。

总体来看，本周的讨论主要是对之前问题的确认与修正，补丁的内容和背景逐渐清晰，开发者之间的沟通也在持续推进。

#### 📝 邮件列表

1. **[06-01 14:28]** RE: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
2. **[06-12 09:38]** Re: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[06-15 13:20]** RE: [PATCH v5 04/18] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
4. **[06-16 10:02]** Re: [PATCH v5 17/18] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 27: [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 17 Jun 2026 10:52:38 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 ARM64 架构中处理系统寄存器（sysreg）时缺失的 hyp_enter 调用。Vincent Donnefort 提出的补丁（patch）旨在修复这一问题，添加了一个新的超管事件调用，以确保 hyp_enter 和 hyp_exit 的平衡。补丁中还包括了对枚举类型 hyp_enter_exit_reason 的更新，增加了 HYP_REASON_SYS 以表示系统寄存器的处理。

在之前的讨论中，Vincent 提到此补丁修复了一个特定的提交（696dfec22b8e），该提交引入了 hyp_enter/hyp_exit 事件，但未能覆盖 sysreg 的情况。Fuad Tabba 对补丁进行了审查，并提出了一个潜在的问题：在字符串数组与枚举之间的对应关系缺乏编译时检查，可能导致未来的维护问题。他建议在未来的补丁中引入更严格的检查机制。

本周的讨论中，Vincent 和 Fuad 继续交流了关于补丁的细节，Fuad 表示将来可能会考虑使用更安全的定义方式来避免潜在的错误。整体来看，此次讨论集中在补丁的有效性及其对系统稳定性的影响上。

#### 📝 邮件列表

1. **[06-17 10:52]** [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[06-17 11:28]** Re: [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[06-17 14:31]** Re: [PATCH] KVM: arm64: Add missing hyp_enter when trapping sysreg
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 28: [PATCH v14 10/44] arm64: RMI: Add support for SRO

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 4 Jun 2026 16:19:39 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 arm64 架构下为 RMI 添加 SRO（Static Resource Ownership）支持的补丁（PATCH v14 10/44）。该补丁旨在改善内存管理，尤其是在处理小型动态内存分配时。

在历史讨论中，参与者们主要探讨了 SRO 机制的实现细节及其与 TDX（Trusted Domain Extensions）补丁的比较。Steven Price 提到，尽管 SRO 机制在内存分配上存在一些局限性，但它的设计意图是为了优化硬件页表的使用。Dan Williams 也指出，当前的 RMM（Resource Management Module）设计可能无法有效处理内存回收的问题，尤其是在多线程环境下。

在本周的新讨论中，Steven Price 进一步阐述了 SRO 机制的局限性，特别是关于内存回收的预期与实际情况之间的差异。他指出，尽管规范期望在操作失败时能够返回所有提供的内存，但在实际操作中，由于竞争条件的存在，这一预期可能无法实现。此外，他还提到，当前的设计并没有强制要求在虚拟机销毁时返回所有捐赠的内存，这可能影响内存的有效管理。

总体而言，讨论集中在 SRO 机制的实现挑战及其对内存管理的影响，参与者们对如何改进当前设计提出了不同的看法和建议。

#### 📝 邮件列表

1. **[06-04 16:19]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>
2. **[06-12 16:07]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Dan Williams (nvidia) <djbw@kernel.org>
3. **[06-15 12:45]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 29: [PATCH] KVM: arm64: nv: Write ESR_EL2 for injected nested SError exceptions

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 15 Jun 2026 14:11:16 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下处理嵌套 SError 异常的补丁。补丁的主要内容是修改 `kvm_inject_el2_exception()` 函数，使其在处理 SError 异常时能够正确写入 ESR_EL2 寄存器，以避免在嵌套 L2 虚拟机中出现过时的 ESR_EL2 值。

在之前的讨论中，提到 `enter_exception64()` 函数并未为任何异常类型写入 ESR_ELx，导致构造的异常综合信息被丢弃。这一问题影响了 `kvm_inject_nested_serror()` 和 `kvm_inject_nested_sea()` 的正常运行。补丁通过在处理 SError 异常时添加一行代码，确保 ESR_EL2 被正确写入，从而修复了该问题。

在本周的新讨论中，Fuad Tabba 提交了补丁，并详细说明了其修复的内容。Marc Zyngier 随后确认已将该补丁应用于修复分支，并表示感谢。这表明该补丁已获得认可并成功合并。

#### 📝 邮件列表

1. **[06-15 14:11]** [PATCH] KVM: arm64: nv: Write ESR_EL2 for injected nested SError exceptions
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[06-17 13:04]** Re: [PATCH] KVM: arm64: nv: Write ESR_EL2 for injected nested SError exceptions
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 30: [PATCH] KVM: arm64: nv: Drop bogus WARN for write to ZCR_EL2

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 14 Jun 2026 22:13:24 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，主要针对 ZCR_EL2 寄存器的写入操作。原始补丁的目的是删除一个错误的警告（WARN），该警告在嵌套上下文中写入 ZCR_EL2 时会导致系统崩溃（hyp_panic），而这在启用 FEAT_NV2 的情况下是合法的。

在之前的讨论中，补丁的背景并未详细说明，但可以推测出该问题与 KVM 的功能实现有关，尤其是与处理虚拟机上下文相关的寄存器操作。

在本周的新讨论中，Oliver Upton 提出了补丁并解释了其必要性。Marc Zyngier 随后确认已将该补丁应用于修复分支，并表示感谢。这表明该补丁得到了认可并将被纳入未来的版本中，解决了之前存在的警告问题。整体来看，本周的讨论进展顺利，补丁得到了及时的处理和应用。

#### 📝 邮件列表

1. **[06-14 22:13]** [PATCH] KVM: arm64: nv: Drop bogus WARN for write to ZCR_EL2
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[06-17 12:51]** Re: [PATCH] KVM: arm64: nv: Drop bogus WARN for write to ZCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 31: [PATCH v2] KVM: arm64: nv: Fix SPSR_EL2 restore in kvm_hyp_handle_mops()

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 17 Jun 2026 12:08:21 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的 SPSR_EL2 恢复问题，具体涉及到 `kvm_hyp_handle_mops()` 函数的处理。原始的补丁（patch）旨在解决在嵌套虚拟化情况下，`vcpu_cpsr()` 返回的合成值未能正确转换为硬件值的问题，导致 SPSR_EL2 的恢复不准确。

在历史讨论中，补丁的背景是由 Zhong Wang 和 Xuanqing Shi 提出的报告，指出了在处理 MOPS 异常时，未能正确处理 SPSR_EL2 的问题。补丁通过直接修改 SPSR_EL2，避免了合成状态的使用，从而确保在返回 KVM 时能够正确同步状态。

在本周的新讨论中，Weiming Shi 提交了补丁的第二版，明确了补丁的修改内容，并根据审查意见进行了调整。Marc Zyngier 随后确认已将该补丁应用于修复集，并表示感谢。这表明该补丁得到了认可，并将解决相关问题。

#### 📝 邮件列表

1. **[06-17 12:08]** [PATCH v2] KVM: arm64: nv: Fix SPSR_EL2 restore in kvm_hyp_handle_mops()
   - 发件人: Weiming Shi <bestswngs@gmail.com>
2. **[06-17 12:50]** Re: [PATCH v2] KVM: arm64: nv: Fix SPSR_EL2 restore in kvm_hyp_handle_mops()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 32: [PATCH] KVM: arm64: account pKVM reclaim against the VM mm

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 21 Jun 2026 21:31:55 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，主要涉及 pKVM（Protected KVM）回收机制对虚拟机内存管理的影响。

**原始补丁内容**：该补丁的目的是修复在处理受保护的来宾故障时，错误地将长期固定的内存页计入当前进程的内存管理（mm）。补丁建议在内存回收时，直接从虚拟机的内存管理中进行计费，而不是从当前进程的内存管理中进行。

**之前讨论要点**：在历史讨论中，未提及具体的补丁或问题，因此没有相关的背景信息。

**本周的新讨论与进展**：本周的讨论中，Bradley Morgan 提交了补丁，明确指出了问题的根源，并提出了修复方案。补丁中修改了 `pkvm.c` 文件，调整了内存计费的逻辑，确保在进行内存回收时，使用虚拟机的内存管理（kvm->mm）而非当前进程的内存管理（current->mm）。此补丁旨在解决之前提交的补丁（4e6e03f9eadd）引发的问题，确保内存管理的准确性和一致性。

#### 📝 邮件列表

1. **[06-21 21:31]** [PATCH] KVM: arm64: account pKVM reclaim against the VM mm
   - 发件人: Bradley Morgan <include@grrlz.net>

---

## 📌 RFC

共 5 个 thread

---

### Thread 1: [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 26 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 16 Jun 2026 15:16:47 +0200

#### 🤖 AI 总结

本邮件线程讨论了一个关于增强 KVM/ARM 的补丁系列，主要目的是引入一个可定制的 AArch64 KVM 主机模型。该补丁系列的核心在于允许用户空间覆盖部分 ID 寄存器的字段值，从而在不同的主机硬件之间迁移虚拟机时提供更大的灵活性。

在历史讨论中，补丁的版本从 v5 更新到 v6，主要改进包括：
1. 增加了对枚举值的支持，确保在设置属性时检查值的有效性。
2. 引入了新的脚本来自动生成 ID 寄存器的定义和属性，简化了代码的维护。
3. 处理了可写字段的初始化问题，确保在 KVM 中能够正确读取和写入这些字段。

本周的新讨论中，Eric Auger 和 Cornelia Huck 提出了多个补丁，主要包括：
1. 实现了一个新的辅助函数，用于从主机获取所有可写 ID 寄存器的值，并将其存储在虚拟机的状态中。
2. 讨论了如何通过 QMP 命令查询可用的 ID 寄存器值，并实现了相关的功能。
3. 增加了对保留字段的处理，确保在生成 ID 寄存器定义时考虑到这些字段。

整体来看，该补丁系列旨在提升 KVM/ARM 的功能，使其能够更好地支持虚拟化环境中的 CPU 特性配置。

#### 📝 邮件列表

1. **[06-16 15:16]** [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[06-16 15:16]** [RFC PATCH v6 01/17] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[06-16 15:16]** [RFC PATCH v6 02/17] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[06-16 15:16]** [RFC PATCH v6 03/17] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[06-16 15:16]** [RFC PATCH v6 04/17] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[06-16 15:16]** [RFC PATCH v6 05/17] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[06-16 15:16]** [RFC PATCH v6 06/17] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[06-16 15:16]** [RFC PATCH v6 07/17] target/arm/cpu-idregs.h.inc: generate with script
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[06-16 15:16]** [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum values
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[06-16 15:16]** [RFC PATCH v6 09/17] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[06-16 15:16]** [RFC PATCH v6 10/17] target/arm/kvm: Retrieve writable ID reg map
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[06-16 15:16]** [RFC PATCH v6 11/17] arm/kvm: Initialize all writable ID registers from host
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[06-16 15:16]** [RFC PATCH v6 12/17] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[06-16 15:17]** [RFC PATCH v6 13/17] target/arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[06-16 15:17]** [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[06-16 15:17]** [RFC PATCH v6 15/17] target/arm/cpu-idregs.h.inc: Generate reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[06-16 15:17]** [RFC PATCH v6 16/17] target/arm/kvm: Ignore and trace unexpected writable reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[06-16 15:17]** [RFC PATCH v6 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[06-17 09:31]** Re: [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64
 KVM host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[06-17 13:18]** Re: [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64
 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
21. **[06-17 11:39]** Re: [RFC PATCH v6 00/17] kvm/arm: Introduce a customizable aarch64
 KVM host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[06-18 11:26]** Re: [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Eric Auger <eric.auger@redhat.com>
23. **[06-19 06:05]** Re: [RFC PATCH v6 14/17] arm-qmp-cmds: introspection for ID register
 props
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[06-19 06:09]** Re: [RFC PATCH v6 04/17] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
25. **[06-19 06:10]** Re: [RFC PATCH v6 15/17] target/arm/cpu-idregs.h.inc: Generate
 reserved fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
26. **[06-19 06:28]** Re: [RFC PATCH v6 08/17] target/arm/cpu-idregs.h.inc: Generate enum
 values
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 2: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots

**📧 邮件数**: 15 | **👥 参与者**: 6 | **📅 开始时间**: Mon, 15 Jun 2026 16:52:44 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM 的 RFC 补丁，主题为“忽略仅限于 guest_memfd 的内存插槽的 MMU 通知器”。该补丁的目的是在处理仅使用 guest_memfd 的内存插槽时，避免 MMU 通知器对二级 MMU 页表的修改，因为这些内存不需要进行常规的内存回收、迁移或脏页跟踪。

在历史讨论中，Alexandru Elisei 提出了补丁的背景，指出对于 guest_memfd 仅限的内存插槽，内存的分配和释放都依赖于用户空间的操作，而不应受到 MMU 通知器的影响。讨论中提到，当前的实现可能导致性能问题，且在某些情况下会引发错误。

本周的新讨论中，参与者们对补丁的潜在问题进行了深入探讨。Sashiko-bot 提出了一个关键问题，指出跳过 MMU 通知器可能会导致主机级的使用后释放（Use-After-Free）错误。Sean Christopherson 和其他参与者讨论了如何确保在不影响性能的情况下，正确处理 MMU 通知器的无效化跟踪。最终，Alexandru 对补丁的思路表示认同，但也承认需要解决当前的缺陷。

总的来说，尽管补丁的初衷是合理的，但在实现过程中需要仔细考虑其对系统稳定性和性能的影响。

#### 📝 邮件列表

1. **[06-15 16:52]** [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[06-15 16:09]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: sashiko-bot@kernel.org
3. **[06-15 10:47]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
4. **[06-15 11:09]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[06-15 21:07]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
6. **[06-17 14:07]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
7. **[06-17 14:23]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
8. **[06-17 15:41]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: David Hildenbrand <david.hildenbrand@arm.com>
9. **[06-17 14:50]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
10. **[06-17 14:21]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[06-17 14:22]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only memslots
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[06-18 11:19]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
13. **[06-18 12:09]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
14. **[06-18 13:26]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
15. **[06-21 08:02]** Re: [RFC PATCH] KVM: Ignore MMU notifiers for guest_memfd-only
 memslots
   - 发件人: XIAO WU <xiaowu.417@qq.com>

---

### Thread 3: [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on KVM

**📧 邮件数**: 10 | **👥 参与者**: 4 | **📅 开始时间**: Fri,  5 Jun 2026 08:33:29 +0000

#### 🤖 AI 总结

本邮件讨论主题为“[RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on KVM”，主要涉及为 KVM 上的 Arm64 提供命名 CPU 模型的支持。

**原始 patch/问题内容**：
该补丁旨在解决当前 QEMU 仅支持 `-cpu host/max` 的问题，这限制了不同 CPU 特性的主机之间的虚拟机实时迁移。补丁提出了分层命名模型的概念，以便更好地管理和迁移虚拟机。

**之前讨论要点**：
在历史讨论中，Khushit Shah 提供了补丁的背景和实现细节，Eric Auger 提出补丁在主线应用时遇到的问题，并请求提供一个可以应用的分支。

**本周的新讨论、进展或结论**：
本周，Khushit Shah 分享了 v2 分支的链接，并表示将在下周发送 v6 版本。Eric Auger 提出了一些关于 ID 注册字段描述的简化建议。Daniel 和 Andrea Bolognani 讨论了是否将 API 扩展到 x86 和 RISC-V 架构，建议将其设计为架构无关的类型。Khushit Shah 最终同意将相关命令重命名为 `query-cpu-props-info`，并将声明移动到 `machine.json` 中，显示出对讨论反馈的积极响应。

#### 📝 邮件列表

1. **[06-05 08:33]** [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
2. **[06-05 08:33]** [RFC PATCH v2 02/29] target/arm: Add ID Register field descriptions in cpu-idregs.h.inc
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
3. **[06-05 08:33]** [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
4. **[06-12 16:50]** Re: [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on
 KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[06-15 05:45]** Re: [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on
 KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
6. **[06-15 18:15]** Re: [RFC PATCH v2 00/29] target/arm: Named CPU models for Arm64 on
 KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[06-17 08:32]** Re: [RFC PATCH v2 02/29] target/arm: Add ID Register field
 descriptions in cpu-idregs.h.inc
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[06-19 10:51]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Daniel =?utf-8?B?UC4gQmVycmFuZ8Op?= <berrange@redhat.com>
9. **[06-19 04:06]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Andrea Bolognani <abologna@redhat.com>
10. **[06-19 12:04]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 4: [RFC] arm: property and value naming summary between named CPU models
 vs customizable host model

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 10 Jun 2026 12:31:37 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM 架构中命名 CPU 模型的属性和值的总结，主要涉及命名 CPU 模型与可定制主机模型之间的差异。

**原始 patch/问题的内容**：
Khushit Shah 提出了一个关于命名 CPU 模型与可定制主机模型属性和值命名差异的总结，旨在明确两者在属性和类型上的不同，以便于更好地管理和使用这些属性。

**之前讨论要点**：
在历史讨论中，Eric Auger 提出了对某些特性的建议，例如是否应同时暴露 feat_PMULL 和 feat_AES，强调了 ARM 规范中这些特性之间的关系。Cornelia Huck 则提到可以通过映射相关寄存器来同时保留人性化的属性名称和原始系统寄存器。

**本周的新讨论、进展或结论**：
本周的讨论中，Khushit Shah 表达了对管理属性复杂性的担忧，认为应优先采用字段级属性。Eric Auger 提出了建立一个属性层，以便通过 `/proc/cpuinfo` 显示特性，并建议将现有属性与 SYSREG 层结合。Khushit 进一步探讨了如何程序化生成 FEAT_ 属性，并表示希望找到一种简便的方法将 ARM 规范中的特性以布尔开关的形式暴露给用户。整体来看，讨论围绕如何平衡人性化命名与系统复杂性展开，尚未达成明确结论。

#### 📝 邮件列表

1. **[06-10 12:31]** [RFC] arm: property and value naming summary between named CPU models
 vs customizable host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
2. **[06-11 20:09]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[06-12 13:24]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Cornelia Huck <cohuck@redhat.com>
4. **[06-15 05:22]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
5. **[06-15 05:43]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
6. **[06-16 16:27]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[06-18 08:56]** Re: [RFC] arm: property and value naming summary between named CPU
 models vs customizable host model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 5: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 19 Jun 2026 11:25:33 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于一个名为“query-arm-cpu-props-info”的补丁（patch），该补丁旨在为 ARM 架构的 QEMU 提供 CPU 属性信息查询功能。

在历史讨论中，未提供具体内容，因此我们只能依据本周的新讨论进行分析。

本周的讨论主要集中在补丁的具体实现细节上。参与者 Markus Armbruster 对补丁的描述提出了一些问题，主要关注属性值的类型和编译时的可知性。他询问了属性名称是否在编译时已知，并对补丁中提到的“字符串列表”表示关注，认为如果值不是字符串，接口用户需要解析字符串，这与 QAPI/QMP 的设计初衷相悖。

Khushit Shah 对这些问题进行了回应，确认属性名称在编译时是已知的，并提出了一种新的数据结构设计方案，使用扁平联合体（flat union）来区分不同类型的属性（布尔值、字符串和数字范围）。他表示将根据讨论中的反馈进行修正，并明确补丁在读取主机值之前无法计算支持的值。

总体而言，本周的讨论推动了补丁的细化和完善，参与者之间的互动有效地解决了技术细节问题。

#### 📝 邮件列表

1. **[06-19 11:25]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Markus Armbruster <armbru@redhat.com>
2. **[06-19 11:54]** Re: [RFC PATCH v2 23/29] target/arm/qmp: add query-arm-cpu-props-info
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

## 📌 Discussion

共 2 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI initialization

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 18 Jun 2026 23:51:42 +0000

#### 🤖 AI 总结

本邮件主题为 “[kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI initialization”，主要讨论了在 ACPI 初始化过程中设置 is_pl011_uart 标志的补丁。

在本周的新讨论中，参与者 Colton Lewis 对 Alexandru Elisei 的建议表示赞同，并表示之前并不知道这些内容。他承诺将根据建议对补丁进行修改并重新提交。这表明补丁的内容得到了积极的反馈，并且正在进行必要的调整以提高一致性。

由于历史讨论部分为空，因此没有之前的讨论要点。本周的讨论主要集中在对补丁的反馈和改进建议上，显示出参与者之间的良好沟通和合作。

#### 📝 邮件列表

1. **[06-18 23:51]** Re: [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI initialization
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 2: [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI
 initialization

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 18 Jun 2026 17:16:41 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM 单元测试的补丁，内容是设置 ACPI 初始化中的 `is_pl011_uart` 标志。

在历史讨论中，邮件列表并未提供具体的补丁内容或之前的讨论记录，因此我们无法详细了解补丁的背景或之前的争论要点。

本周的新讨论中，参与者 Alexandru Elisei 对补丁表示支持，并提到可以使用 Linux 源代码树中的定义，特别是 `include/acpi/actbl1.h` 中的内容。他指出了对某个值的困惑，认为其在 Debug Port Table 2 中的定义与 32 位 16550 UART 可能不匹配，但并未否定补丁的有效性。最终，他确认补丁是合理的，并给予了审核通过的反馈。

总结来看，本周的讨论主要集中在补丁的合理性和对 ACPI 定义的使用上，尽管存在一些命名上的疑问，但整体上对补丁的接受度较高。

#### 📝 邮件列表

1. **[06-18 17:16]** Re: [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI
 initialization
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

## 📌 Other

共 2 个 thread

---

### Thread 1: Sashiko review emails to the list

**📧 邮件数**: 4 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 19 Jun 2026 15:19:05 +0100

#### 🤖 AI 总结

本邮件讨论围绕 Sashiko 这个工具的邮件审查功能展开。Sashiko 被认为是一个非常有用的工具，能够识别出代码中的真实错误，但最近其发送的审查邮件数量过多，引发了参与者的关注。

在历史讨论中，参与者们指出 Sashiko 的审查邮件中存在较高的噪声比率，主要包括虚假警报和重复报告的问题。Fuad Tabba 提到，Roman 正在改进虚假警报的检测，并且他自己也在努力减少 ARM 架构相关的错误报告。

本周的新讨论中，Fuad 提出了一些可能的解决方案，包括暂停邮件通知或提高报告的信心阈值。Oliver Upton 表示支持在质量得到改善后重新启用邮件通知。Roman Gushchin 认为，审查质量受限于模型能力和代码架构，且对每个问题的单独验证可能会增加处理时间。Marc Zyngier 则强调了处理报告时的管理问题，认为需要更好地聚焦于初始补丁系列，而不是被大量相关问题分散注意力。

总体来看，参与者们一致认为需要改进 Sashiko 的邮件审查机制，以降低噪声并提高效率，同时也期待未来的改进能带来更好的结果。

#### 📝 邮件列表

1. **[06-19 15:19]** Sashiko review emails to the list
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[06-19 09:45]** Re: Sashiko review emails to the list
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[06-19 11:05]** Re: Sashiko review emails to the list
   - 发件人: Roman Gushchin <roman.gushchin@linux.dev>
4. **[06-21 12:03]** Re: Sashiko review emails to the list
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in ACPI initialization

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 19 Jun 2026 00:25:04 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 ARM64 系统的 ACPI 初始化过程中设置 `is_pl011_uart` 标志的补丁（PATCH v2）。该补丁旨在解决在通过 ACPI 启动时，代码未能正确设置此标志的问题，导致 `__getchar()` 函数将 UART 视为 16550A 设备，从而在 PL011 系统上出现失败，导致等待串行输入的测试（如 `its-migration`）无限挂起。

在之前的讨论中，补丁的初版（v1）已被提交，并提供了相关链接以供参考。经过审查后，补丁在 v2 版本中进行了更新，主要是将宏名称与 Linux 内核的 DBG2 定义对齐。

本周的新讨论中，Colton Lewis 提出了补丁的详细内容，强调了在 `uart0_init_acpi()` 函数中检查 SPCR 的 `interface_type` 字段，并相应地设置 `is_pl011_uart` 标志。此外，还在 `lib/acpi.h` 中定义了 DBG2 宏以支持不同的接口类型。这一补丁的实施将有效解决之前提到的问题，确保系统在启动时能够正确识别和初始化 UART 设备。

#### 📝 邮件列表

1. **[06-19 00:25]** [kvm-unit-tests PATCH v2] arm: io: Set is_pl011_uart flag in ACPI initialization
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

