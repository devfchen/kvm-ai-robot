# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-04-06 00:36:10

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 260
- **总 Thread 数**: 28
- **大型 Thread** (>20封): 3 个

### 分类分布

- **PATCH**: 28 threads (260 邮件)

---

## 📌 PATCH

共 28 个 thread

---

### Thread 1: [PATCH v2 00/30] KVM: arm64: Combined user_mem_abort() rework

**📧 邮件数**: 45 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 27 Mar 2026 11:35:48 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 `user_mem_abort()` 函数的重构，主要通过一系列补丁（patch）来优化代码结构和性能。

1. **原始 patch/问题的内容**：
   Marc Zyngier 和 Fuad Tabba 提出了一个重构项目，旨在对 `user_mem_abort()` 函数进行大规模重构，目的是将其拆分为更小的、专注的辅助函数，以提高代码的可读性和可维护性。

2. **之前的讨论要点**：
   在历史邮件中，讨论了多个补丁的具体实现，包括提取 VMA 大小解析、引入 `kvm_s2_fault` 结构体、简化权限逻辑、优化早期退出检查等。这些补丁得到了参与者的认可和审查，标志着代码逐步走向更清晰的结构。

3. **本周的新讨论、进展或结论**：
   本周的讨论主要集中在对各个补丁的审查上，Anshuman Khandual 对所有补丁进行了审核并表示认可。最终，Marc Zyngier 确认所有补丁已被应用到下一个版本中，标志着重构工作的成功推进。

总的来说，此次讨论展示了对 KVM arm64 代码的持续改进，强调了代码结构的优化和性能提升的重要性。

#### 📝 邮件列表

1. **[03-27 11:35]** [PATCH v2 00/30] KVM: arm64: Combined user_mem_abort() rework
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-27 11:35]** [PATCH v2 01/30] KVM: arm64: Extract VMA size resolution in user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-27 11:35]** [PATCH v2 02/30] KVM: arm64: Introduce struct kvm_s2_fault to user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-27 11:35]** [PATCH v2 03/30] KVM: arm64: Extract PFN resolution in user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-27 11:35]** [PATCH v2 04/30] KVM: arm64: Isolate mmap_read_lock inside new kvm_s2_fault_get_vma_info() helper
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-27 11:35]** [PATCH v2 05/30] KVM: arm64: Extract stage-2 permission logic in user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-27 11:35]** [PATCH v2 06/30] KVM: arm64: Extract page table mapping in user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-27 11:35]** [PATCH v2 07/30] KVM: arm64: Simplify nested VMA shift calculation
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-27 11:35]** [PATCH v2 08/30] KVM: arm64: Remove redundant state variables from struct kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[03-27 11:35]** [PATCH v2 09/30] KVM: arm64: Simplify return logic in user_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[03-27 11:35]** [PATCH v2 10/30] KVM: arm64: Initialize struct kvm_s2_fault completely at declaration
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[03-27 11:35]** [PATCH v2 11/30] KVM: arm64: Optimize early exit checks in kvm_s2_fault_pin_pfn()
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[03-27 11:36]** [PATCH v2 12/30] KVM: arm64: Hoist MTE validation check out of MMU lock path
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[03-27 11:36]** [PATCH v2 13/30] KVM: arm64: Clean up control flow in kvm_s2_fault_map()
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[03-27 11:36]** [PATCH v2 14/30] KVM: arm64: Kill fault->ipa
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[03-27 11:36]** [PATCH v2 15/30] KVM: arm64: Make fault_ipa immutable
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[03-27 11:36]** [PATCH v2 16/30] KVM: arm64: Move fault context to const structure
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[03-27 11:36]** [PATCH v2 17/30] KVM: arm64: Replace fault_is_perm with a helper
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[03-27 11:36]** [PATCH v2 18/30] KVM: arm64: Constrain fault_granule to kvm_s2_fault_map()
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[03-27 11:36]** [PATCH v2 19/30] KVM: arm64: Kill write_fault from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[03-27 11:36]** [PATCH v2 20/30] KVM: arm64: Kill exec_fault from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[03-30 09:38]** Re: [PATCH v2 01/30] KVM: arm64: Extract VMA size resolution in
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
23. **[03-30 09:48]** Re: [PATCH v2 02/30] KVM: arm64: Introduce struct kvm_s2_fault to
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
24. **[03-30 10:03]** Re: [PATCH v2 03/30] KVM: arm64: Extract PFN resolution in
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
25. **[03-30 10:27]** Re: [PATCH v2 04/30] KVM: arm64: Isolate mmap_read_lock inside new
 kvm_s2_fault_get_vma_info() helper
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
26. **[03-31 09:00]** Re: [PATCH v2 05/30] KVM: arm64: Extract stage-2 permission logic in
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
27. **[03-31 09:15]** Re: [PATCH v2 06/30] KVM: arm64: Extract page table mapping in
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
28. **[03-31 09:26]** Re: [PATCH v2 07/30] KVM: arm64: Simplify nested VMA shift
 calculation
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
29. **[03-31 09:38]** Re: [PATCH v2 08/30] KVM: arm64: Remove redundant state variables
 from struct kvm_s2_fault
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
30. **[03-31 10:02]** Re: [PATCH v2 09/30] KVM: arm64: Simplify return logic in
 user_mem_abort()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
31. **[03-31 11:13]** Re: [PATCH v2 10/30] KVM: arm64: Initialize struct kvm_s2_fault
 completely at declaration
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
32. **[03-31 12:05]** Re: [PATCH v2 11/30] KVM: arm64: Optimize early exit checks in
 kvm_s2_fault_pin_pfn()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
33. **[03-31 12:27]** Re: [PATCH v2 12/30] KVM: arm64: Hoist MTE validation check out of
 MMU lock path
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
34. **[03-31 12:41]** Re: [PATCH v2 13/30] KVM: arm64: Clean up control flow in
 kvm_s2_fault_map()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
35. **[03-31 12:58]** Re: [PATCH v2 14/30] KVM: arm64: Kill fault->ipa
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
36. **[03-31 19:28]** Re: [PATCH v2 12/30] KVM: arm64: Hoist MTE validation check out of MMU lock path
   - 发件人: Marc Zyngier <maz@kernel.org>
37. **[04-01 07:48]** Re: [PATCH v2 12/30] KVM: arm64: Hoist MTE validation check out of
 MMU lock path
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
38. **[04-01 07:53]** Re: [PATCH v2 12/30] KVM: arm64: Hoist MTE validation check out of
 MMU lock path
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
39. **[04-01 08:14]** Re: [PATCH v2 15/30] KVM: arm64: Make fault_ipa immutable
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
40. **[04-01 08:23]** Re: [PATCH v2 16/30] KVM: arm64: Move fault context to const
 structure
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
41. **[04-01 08:48]** Re: [PATCH v2 17/30] KVM: arm64: Replace fault_is_perm with a helper
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
42. **[04-01 08:56]** Re: [PATCH v2 18/30] KVM: arm64: Constrain fault_granule to
 kvm_s2_fault_map()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
43. **[04-01 09:01]** Re: [PATCH v2 19/30] KVM: arm64: Kill write_fault from kvm_s2_fault
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
44. **[04-01 09:05]** Re: [PATCH v2 20/30] KVM: arm64: Kill exec_fault from kvm_s2_fault
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
45. **[04-01 16:34]** Re: [PATCH v2 00/30] KVM: arm64: Combined user_mem_abort() rework
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 2: [PATCH v5 00/38] KVM: arm64: Add support for protected guest memory with pKVM

**📧 邮件数**: 43 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 30 Mar 2026 15:48:01 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现受保护虚拟机（pKVM）内存支持的补丁集（PATCH v5 00/38）。以下是主要内容的总结：

1. **原始补丁内容**：补丁集的核心是为 pKVM 添加受保护的来宾内存支持，允许创建受保护的虚拟机（pVM），并通过超调用（hypercall）实现内存的捐赠和回收。

2. **历史讨论要点**：之前的版本（v1 到 v4）中，开发者针对补丁提出了多项改进建议，包括处理页面偏移、检查虚拟机状态、避免竞态条件等。开发者 Will Deacon 针对这些反馈进行了修正，并在 v5 中进行了更新。

3. **本周的新讨论与进展**：本周的讨论中，开发者提交了多项补丁，涵盖了受保护虚拟机的内存捐赠、回收、超调用处理、以及对受保护虚拟机的支持等功能。补丁中还包括对 pKVM 的文档说明，强调其实验性和开发性质。此外，针对内存共享和取消共享的超调用也进行了实现。最后，讨论中提到了一些测试结果和潜在的警告信息，开发者们对补丁进行了验证和调整。

整体来看，本周的讨论集中在完善 pKVM 的功能和稳定性上，确保其在实际应用中的可用性和安全性。

#### 📝 邮件列表

1. **[03-30 15:48]** [PATCH v5 00/38] KVM: arm64: Add support for protected guest memory with pKVM
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-30 15:48]** [PATCH v5 01/38] KVM: arm64: Remove unused PKVM_ID_FFA definition
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-30 15:48]** [PATCH v5 02/38] KVM: arm64: Don't leak stage-2 page-table if VM fails to init under pKVM
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-30 15:48]** [PATCH v5 03/38] KVM: arm64: Move handle check into pkvm_pgtable_stage2_destroy_range()
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-30 15:48]** [PATCH v5 04/38] KVM: arm64: Rename __pkvm_pgtable_stage2_unmap()
   - 发件人: Will Deacon <will@kernel.org>
6. **[03-30 15:48]** [PATCH v5 05/38] KVM: arm64: Don't advertise unsupported features for protected guests
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-30 15:48]** [PATCH v5 06/38] KVM: arm64: Expose self-hosted debug regs as RAZ/WI for protected guests
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-30 15:48]** [PATCH v5 07/38] KVM: arm64: Remove is_protected_kvm_enabled() checks from hypercalls
   - 发件人: Will Deacon <will@kernel.org>
9. **[03-30 15:48]** [PATCH v5 08/38] KVM: arm64: Ignore MMU notifier callbacks for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
10. **[03-30 15:48]** [PATCH v5 09/38] KVM: arm64: Prevent unsupported memslot operations on protected VMs
   - 发件人: Will Deacon <will@kernel.org>
11. **[03-30 15:48]** [PATCH v5 10/38] KVM: arm64: Ignore -EAGAIN when mapping in pages for the pKVM host
   - 发件人: Will Deacon <will@kernel.org>
12. **[03-30 15:48]** [PATCH v5 11/38] KVM: arm64: Split teardown hypercall into two phases
   - 发件人: Will Deacon <will@kernel.org>
13. **[03-30 15:48]** [PATCH v5 12/38] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Will Deacon <will@kernel.org>
14. **[03-30 15:48]** [PATCH v5 13/38] KVM: arm64: Hook up donation hypercall to pkvm_pgtable_stage2_map()
   - 发件人: Will Deacon <will@kernel.org>
15. **[03-30 15:48]** [PATCH v5 14/38] KVM: arm64: Handle aborts from protected VMs
   - 发件人: Will Deacon <will@kernel.org>
16. **[03-30 15:48]** [PATCH v5 15/38] KVM: arm64: Introduce __pkvm_reclaim_dying_guest_page()
   - 发件人: Will Deacon <will@kernel.org>
17. **[03-30 15:48]** [PATCH v5 16/38] KVM: arm64: Hook up reclaim hypercall to pkvm_pgtable_stage2_destroy()
   - 发件人: Will Deacon <will@kernel.org>
18. **[03-30 15:48]** [PATCH v5 17/38] KVM: arm64: Factor out pKVM host exception injection logic
   - 发件人: Will Deacon <will@kernel.org>
19. **[03-30 15:48]** [PATCH v5 18/38] KVM: arm64: Support translation faults in inject_host_exception()
   - 发件人: Will Deacon <will@kernel.org>
20. **[03-30 15:48]** [PATCH v5 19/38] KVM: arm64: Inject SIGSEGV on illegal accesses
   - 发件人: Will Deacon <will@kernel.org>
21. **[03-30 15:48]** [PATCH v5 20/38] KVM: arm64: Avoid pointless annotation when mapping host-owned pages
   - 发件人: Will Deacon <will@kernel.org>
22. **[03-30 15:48]** [PATCH v5 21/38] KVM: arm64: Generalise kvm_pgtable_stage2_set_owner()
   - 发件人: Will Deacon <will@kernel.org>
23. **[03-30 15:48]** [PATCH v5 22/38] KVM: arm64: Introduce host_stage2_set_owner_metadata_locked()
   - 发件人: Will Deacon <will@kernel.org>
24. **[03-30 15:48]** [PATCH v5 23/38] KVM: arm64: Change 'pkvm_handle_t' to u16
   - 发件人: Will Deacon <will@kernel.org>
25. **[03-30 15:48]** [PATCH v5 24/38] KVM: arm64: Annotate guest donations with handle and gfn in host stage-2
   - 发件人: Will Deacon <will@kernel.org>
26. **[03-30 15:48]** [PATCH v5 25/38] KVM: arm64: Introduce hypercall to force reclaim of a protected page
   - 发件人: Will Deacon <will@kernel.org>
27. **[03-30 15:48]** [PATCH v5 26/38] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Will Deacon <will@kernel.org>
28. **[03-30 15:48]** [PATCH v5 27/38] KVM: arm64: Return -EFAULT from VCPU_RUN on access to a poisoned pte
   - 发件人: Will Deacon <will@kernel.org>
29. **[03-30 15:48]** [PATCH v5 28/38] KVM: arm64: Add hvc handler at EL2 for hypercalls from protected VMs
   - 发件人: Will Deacon <will@kernel.org>
30. **[03-30 15:48]** [PATCH v5 29/38] KVM: arm64: Implement the MEM_SHARE hypercall for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
31. **[03-30 15:48]** [PATCH v5 30/38] KVM: arm64: Implement the MEM_UNSHARE hypercall for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
32. **[03-30 15:48]** [PATCH v5 31/38] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Will Deacon <will@kernel.org>
33. **[03-30 15:48]** [PATCH v5 32/38] KVM: arm64: Add some initial documentation for pKVM
   - 发件人: Will Deacon <will@kernel.org>
34. **[03-30 15:48]** [PATCH v5 33/38] KVM: arm64: Extend pKVM page ownership selftests to cover guest donation
   - 发件人: Will Deacon <will@kernel.org>
35. **[03-30 15:48]** [PATCH v5 34/38] KVM: arm64: Register 'selftest_vm' in the VM table
   - 发件人: Will Deacon <will@kernel.org>
36. **[03-30 15:48]** [PATCH v5 35/38] KVM: arm64: Extend pKVM page ownership selftests to cover forced reclaim
   - 发件人: Will Deacon <will@kernel.org>
37. **[03-30 15:48]** [PATCH v5 36/38] KVM: arm64: Extend pKVM page ownership selftests to cover guest hvcs
   - 发件人: Will Deacon <will@kernel.org>
38. **[03-30 15:48]** [PATCH v5 37/38] KVM: arm64: Rename PKVM_PAGE_STATE_MASK
   - 发件人: Will Deacon <will@kernel.org>
39. **[03-30 15:48]** [PATCH v5 38/38] drivers/virt: pkvm: Add Kconfig dependency on DMA_RESTRICTED_POOL
   - 发件人: Will Deacon <will@kernel.org>
40. **[03-31 20:15]** Re: [PATCH v5 11/38] KVM: arm64: Split teardown hypercall into two
 phases
   - 发件人: Mark Brown <broonie@kernel.org>
41. **[03-31 20:24]** Re: [PATCH v5 11/38] KVM: arm64: Split teardown hypercall into two
 phases
   - 发件人: Will Deacon <will@kernel.org>
42. **[04-01 14:35]** Re: [PATCH v5 11/38] KVM: arm64: Split teardown hypercall into two
 phases
   - 发件人: Mark Brown <broonie@kernel.org>
43. **[04-01 16:28]** Re: [PATCH v5 00/38] KVM: arm64: Add support for protected guest memory with pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 3: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 33 | **👥 参与者**: 5 | **📅 开始时间**: Thu,  2 Apr 2026 06:20:56 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 400 - {'error': {'message': "This model's maximum context length is 128000 tokens. However, your messages resulted in 159521 tokens. Please reduce the length of the messages.", 'type': 'invalid_request_error', 'param': 'messages', 'code': 'context_length_exceeded'}}]
策略: 完整 thread (历史:0 新:33, 119105 tokens)

#### 📝 邮件列表

1. **[04-02 06:20]** [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[04-02 06:20]** [PATCH v1 01/27] VFIO: take reference to the KVM module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[04-02 06:20]** [PATCH v1 02/27] KVM, vfio: remove symbol_get(kvm_get_kvm_safe) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[04-02 06:20]** [PATCH v1 03/27] KVM, vfio: remove symbol_get(kvm_put_kvm) from vfio
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[04-02 06:21]** [PATCH v1 04/27] arm64: Provide arm64 UAPI for other host architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[04-02 06:21]** [PATCH v1 05/27] arm64: Extract sysreg definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[04-02 06:21]** [PATCH v1 06/27] arm64: Provide arm64 API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[04-02 06:21]** [PATCH v1 07/27] KVM: arm64: Provide arm64 KVM API for non-native architectures
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[04-02 06:21]** [PATCH v1 08/27] arm64: Extract pstate definitions from ptrace
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[04-02 06:21]** [PATCH v1 09/27] KVM: arm64: Share kvm_emulate definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[04-02 06:21]** [PATCH v1 10/27] KVM: arm64: Make some arm64 KVM code shareable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[04-02 06:21]** [PATCH v1 11/27] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[04-02 06:21]** [PATCH v1 12/27] KVM: arm64: Share reset general register code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[04-02 06:21]** [PATCH v1 13/27] KVM: arm64: Extract & share ipa size shift calculation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[04-02 06:21]** [PATCH v1 14/27] KVM: s390: Move s390 kvm code into a subdirectory
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[04-02 06:21]** [PATCH v1 15/27] KVM: S390: Refactor gmap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[04-02 06:21]** [PATCH v1 16/27] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[04-02 06:21]** [PATCH v1 17/27] KVM: Remove KVM_MMIO as config option
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[04-02 06:21]** [PATCH v1 18/27] KVM: s390: Prepare kvm-s390 for a second kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[04-02 06:21]** [PATCH v1 19/27] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[04-02 06:21]** [PATCH v1 20/27] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[04-02 06:21]** [PATCH v1 21/27] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[04-02 06:21]** [PATCH v1 22/27] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[04-02 06:21]** [PATCH v1 23/27] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[04-02 06:21]** [PATCH v1 24/27] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[04-02 06:21]** [PATCH v1 25/27] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[04-02 06:21]** [PATCH v1 26/27] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[04-02 06:21]** [PATCH v1 27/27] KVM: s390: arm64: Enable KVM_ARM64 config and Kbuild
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[04-02 10:53]** Re: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
30. **[04-02 11:18]** Re: [PATCH v1 01/27] VFIO: take reference to the KVM module
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
31. **[04-02 12:07]** Re: [PATCH v1 00/27] KVM: s390: Introduce arm64 KVM
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>
32. **[04-02 11:08]** Re: [PATCH v1 07/27] KVM: arm64: Provide arm64 KVM API for non-native architectures
   - 发件人: Marc Zyngier <maz@kernel.org>
33. **[04-02 13:26]** Re: [PATCH v1 07/27] KVM: arm64: Provide arm64 KVM API for non-native
 architectures
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>

---

### Thread 4: [PATCH v2 00/16] KVM: arm64: First batch of vgic-v5 related fixes

**📧 邮件数**: 19 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  1 Apr 2026 11:35:55 +0100

#### 🤖 AI 总结

本邮件线程讨论的是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-v5（虚拟通用中断控制器版本5）相关修复的补丁系列。

**原始补丁内容**：
该补丁系列的目的是修复在 vgic-v5 PPI（私有中断）系列中报告的一些问题，包含16个补丁，主要涉及对 GICv5 的初始化、状态管理和寄存器处理等方面的修正。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 提到需要部分撤销对有效优先级掩码的修复，因为 GICv5 在处理 PCR（优先级控制寄存器）方面与 GICv[234] 存在关键差异。此外，还增加了对待处理的硬件支持的 PPI 的修复和对 set_id_regs 自测的解决方法。

**本周新讨论与进展**：
本周的讨论集中在补丁的具体实现上，Marc Zyngier 提交了多个补丁，修复了如不重置 CPU 接口和重分配地址、确保每个虚拟 CPU 的 NV 初始化、修正 ID_AA64PFR2_EL1 的可写掩码、以及在最终化 GICv5 PPI 状态时持有配置锁等问题。所有补丁均已获得 Sascha Bischoff 的审核并已应用到下一个版本中。Sascha 还指出在处理边缘触发状态时可能会丢失边缘信号的问题，并提出了进一步的补丁以解决该问题。

整体来看，本周的讨论和补丁提交为 KVM 在 arm64 架构下的 vgic-v5 实现提供了重要的修复和改进。

#### 📝 邮件列表

1. **[04-01 11:35]** [PATCH v2 00/16] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-01 11:35]** [PATCH v2 01/16] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-01 11:35]** [PATCH v2 02/16] KVM: arm64: Don't skip per-vcpu NV initialisation
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-01 11:35]** [PATCH v2 03/16] arm64: Fix field references for ICH_PPI_DVIR[01]_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-01 11:35]** [PATCH v2 04/16] KVM: arm64: Fix writeable mask for ID_AA64PFR2_EL1
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-01 11:36]** [PATCH v2 05/16] KVM: arm64: Account for RESx bits in __compute_fgt()
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[04-01 11:36]** [PATCH v2 06/16] KVM: arm64: vgic-v5: Hold config_lock while finalizing GICv5 PPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[04-01 11:36]** [PATCH v2 07/16] KVM: arm64: vgic-v5: Transfer edge pending state to ICH_PPI_PENDRx_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[04-01 11:36]** [PATCH v2 08/16] KVM: arm64: vgic-v5: Cast vgic_apr to u32 to avoid undefined behaviours
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[04-01 11:36]** [PATCH v2 09/16] KVM: arm64: vgic-v5: Make the effective priority mask a strict limit
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[04-01 11:36]** [PATCH v2 10/16] KVM: arm64: vgic-v5: Correctly set dist->ready once initialised
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[04-01 11:36]** [PATCH v2 11/16] KVM: arm64: Kill arch_timer_context::direct field
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[04-01 11:36]** [PATCH v2 12/16] KVM: arm64: Remove evaluation of timer state in kvm_cpu_has_pending_timer()
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[04-01 11:36]** [PATCH v2 13/16] KVM: arm64: Move GICv5 timer PPI validation into timer_irqs_are_valid()
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[04-01 11:36]** [PATCH v2 14/16] KVM: arm64: Correctly plumb ID_AA64PFR2_EL1 into pkvm idreg handling
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[04-01 11:36]** [PATCH v2 15/16] KVM: arm64: Don't advertises GICv3 in ID_PFR1_EL1 if AArch32 isn't supported
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[04-01 11:36]** [PATCH v2 16/16] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime
   - 发件人: Marc Zyngier <maz@kernel.org>
18. **[04-01 16:30]** Re: [PATCH v2 00/16] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[04-01 16:24]** Re: [PATCH v2 07/16] KVM: arm64: vgic-v5: Transfer edge pending state
 to ICH_PPI_PENDRx_EL2
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 5: [PATCH v7 00/17] kvmtool: arm64: Handle PSCI calls in userspace

**📧 邮件数**: 18 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 30 Mar 2026 15:23:17 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 工具的 ARM64 平台的 PSCI 调用处理的补丁系列（PATCH v7 00/17）。该补丁旨在实现用户空间对 PSCI 调用的支持，利用 SMCCC 过滤能力来处理这些调用。

在历史讨论中，补丁的初始版本由 Oliver Upton 提出，经过多次迭代，修复了构建错误，更新了头文件，并清理了代码。补丁的主要目标是将 PSCI 调用的处理从内核转移到用户空间，以提高灵活性和可扩展性。

本周的新讨论中，Suzuki K Poulose 提出了多个补丁，涵盖了 PSCI 的多个功能实现，包括 CPU_SUSPEND、CPU_ON、AFFINITY_INFO 和 SYSTEM_{OFF,RESET} 等。每个补丁都经过了审查，并得到了 Marc Zyngier 的认可。补丁还引入了 SMCCC 过滤机制，以便将 PSCI 调用转发到用户空间进行处理。此外，补丁中还处理了 CPU 的状态管理，确保在调用 PSCI 时，虚拟 CPU 的状态能够正确反映。

总体而言，本周的讨论集中在完善 PSCI 功能的实现和确保用户空间能够有效处理这些调用，标志着 KVM 工具在 ARM64 平台上的进一步发展。

#### 📝 邮件列表

1. **[03-30 15:23]** [PATCH v7 00/17] kvmtool: arm64: Handle PSCI calls in userspace
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[03-30 15:23]** [PATCH v7 01/17] headers: Update linux/const.h from linux sources
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[03-30 15:23]** [PATCH v7 02/17] util/update_headers: Clean up header copying
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[03-30 15:23]** [PATCH v7 03/17] util/update_headers: Warn about missing header files
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[03-30 15:23]** [PATCH v7 04/17] update_headers: arm64: Track uapi/linux/psci.h for PSCI definitions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[03-30 15:23]** [PATCH v7 05/17] arm64: Sync headers from Linux v6.19 for psci.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[03-30 15:23]** [PATCH v7 06/17] Import arm-smccc.h from Linux v6.19
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[03-30 15:23]** [PATCH v7 07/17] arm64: Stash kvm_vcpu_init for later use
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[03-30 15:23]** [PATCH v7 08/17] arm64: Use KVM_SET_MP_STATE ioctl to power off non-boot vCPUs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[03-30 15:23]** [PATCH v7 09/17] arm64: Expose ARM64_CORE_REG() for general use
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[03-30 15:23]** [PATCH v7 10/17] arm64: Add support for finding vCPU for given MPIDR
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[03-30 15:23]** [PATCH v7 11/17] arm64: Add skeleton implementation for PSCI
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[03-30 15:23]** [PATCH v7 12/17] arm64: psci: Implement CPU_SUSPEND
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
14. **[03-30 15:23]** [PATCH v7 13/17] arm64: psci: Implement CPU_ON
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[03-30 15:23]** [PATCH v7 14/17] arm64: psci: Implement AFFINITY_INFO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[03-30 15:23]** [PATCH v7 15/17] arm64: psci: Implement MIGRATE_INFO_TYPE
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[03-30 15:23]** [PATCH v7 16/17] arm64: psci: Implement SYSTEM_{OFF,RESET}
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[03-30 15:23]** [PATCH v7 17/17] arm64: smccc: Start sending PSCI to userspace
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 6: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 16 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 18 Mar 2026 15:53:24 +0000

#### 🤖 AI 总结

本邮件线程讨论的主题是支持在 KVM 中运行受保护的虚拟机，特别是基于 Arm Confidential Compute Architecture (CCA) 的实现。原始的 patch（[PATCH v13 00/48]）旨在为 KVM 提供对 Arm CCA 的支持，允许在 KVM 下运行受保护的虚拟机。该系列补丁引入了新的 RMM v2.0 版本，允许配置与主机相同的页面大小，并引入基于范围的 API。

在历史讨论中，主要讨论了 RMM 的内存跟踪和域创建的基本基础设施，以及如何处理 PSCI 请求和异常注入等问题。Steven Price 提出了多个补丁，解决了 RMM 在启动时可能未跟踪所有内存的问题，并确保在处理 PSCI 调用时 RMM 能够正确响应。

在本周的新讨论中，Suzuki K Poulose 提出了对 PSCI_CPU_ON 请求的处理建议，认为可以在 REC_ENTER 之前隐式完成 PSCI 操作。此外，Mathieu Poirier 提出了关于内存对齐问题的修复建议，并与 Suzuki 讨论了如何在 RMM 规范中解决此问题。最后，Steven Price 确认了一个关于内存释放的 bug 修复，确保在处理 realm 时正确释放内存。

总体而言，本周的讨论集中在对补丁的细节调整和潜在问题的修复上，推动了对 Arm CCA 支持的进一步完善。

#### 📝 邮件列表

1. **[03-18 15:53]** [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[03-18 15:53]** [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries for memory
   - 发件人: Steven Price <steven.price@arm.com>
3. **[03-18 15:53]** [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Steven Price <steven.price@arm.com>
4. **[03-18 15:53]** [PATCH v13 30/48] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Steven Price <steven.price@arm.com>
5. **[03-18 15:53]** [PATCH v13 31/48] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
6. **[03-18 15:53]** [PATCH v13 32/48] arm64: Don't expose stolen time for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
7. **[03-18 15:53]** [PATCH v13 34/48] arm64: RMI: support RSI_HOST_CALL
   - 发件人: Steven Price <steven.price@arm.com>
8. **[03-21 16:34]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating
 a realm.
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[03-30 11:36]** Re: [PATCH v13 30/48] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[03-30 11:50]** Re: [PATCH v13 31/48] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[03-30 11:52]** Re: [PATCH v13 32/48] arm64: Don't expose stolen time for realm
 guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[03-30 11:58]** Re: [PATCH v13 34/48] arm64: RMI: support RSI_HOST_CALL
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[03-30 14:58]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT
 entries for memory
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
14. **[03-31 12:05]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[03-31 11:43]** Re: [PATCH v13 10/48] arm64: RMI: Ensure that the RMM has GPT
 entries for memory
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
16. **[04-01 11:54]** Re: [PATCH v13 12/48] arm64: RMI: Basic infrastructure for creating a
 realm.
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 7: [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 26 Mar 2026 15:35:15 +0000

#### 🤖 AI 总结

本邮件线程讨论了 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-v5（虚拟通用中断控制器 v5）相关的修复补丁，包含15个补丁的第一批。

**原始 patch/问题的内容**：
Marc Zyngier 提出了针对 vgic-v5 的一系列补丁，目的是修复在合并过程中发现的回归问题，尤其是与中断优先级和定时器状态评估相关的错误。

**之前讨论要点**：
在历史讨论中，Marc 指出了一些补丁引入了不当的逻辑，例如在优先级比较中未能正确处理 GICv5 的优先级掩码，导致了潜在的错误。此外，关于定时器状态的评估也被认为是不必要的，因为它与中断的处理逻辑存在冲突。

**本周的新讨论、进展或结论**：
本周的讨论中，参与者 Mark Brown 对补丁进行了测试，未发现重大问题。Sascha Bischoff 指出在优先级比较的补丁中，GICv5 的优先级处理与 GICv[23] 不同，强调了需要在逻辑中加入 `+1` 的必要性。对于定时器状态的评估，Sascha 也提出了新的实现方案，确保在 GICv5 中正确处理定时器中断。最终，Marc 和 Sascha 达成一致，确认了补丁的修正方向，并表示将继续处理其他标记的问题。

#### 📝 邮件列表

1. **[03-26 15:35]** [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-26 15:35]** [PATCH 09/15] KVM: arm64: vgic-v5: align priority comparison with other GICs
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-26 15:35]** [PATCH 12/15] KVM: arm64: Remove evaluation of timer state in kvm_cpu_has_pending_timer()
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-30 18:05]** Re: [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Mark Brown <broonie@kernel.org>
5. **[03-31 15:09]** Re: [PATCH 09/15] KVM: arm64: vgic-v5: align priority comparison with
 other GICs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[03-31 15:44]** Re: [PATCH 12/15] KVM: arm64: Remove evaluation of timer state in
 kvm_cpu_has_pending_timer()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[03-31 16:34]** Re: [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[03-31 18:02]** Re: [PATCH 12/15] KVM: arm64: Remove evaluation of timer state in kvm_cpu_has_pending_timer()
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-31 18:18]** Re: [PATCH 09/15] KVM: arm64: vgic-v5: align priority comparison with other GICs
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[04-01 08:18]** Re: [PATCH 09/15] KVM: arm64: vgic-v5: align priority comparison with
 other GICs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[04-01 08:21]** Re: [PATCH 12/15] KVM: arm64: Remove evaluation of timer state in
 kvm_cpu_has_pending_timer()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 8: [PATCH v4 0/9] KVM: selftests: Create KVM selftests runner

**📧 邮件数**: 10 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 31 Mar 2026 12:41:53 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 自测试运行器的补丁系列（PATCH v4 0/9），旨在增强 KVM 自测试的执行和输出管理。

**原始补丁内容**：
该补丁系列的核心是创建一个 KVM 自测试运行器，允许用户以更灵活和高效的方式运行自测试。运行器提供了并行执行、用户友好的输出、分层保存输出等功能，超越了默认的 kselftest 基础设施。

**之前的讨论要点**：
在之前的版本（v1 到 v3）中，开发者逐步增加了多个功能，如并行测试执行、输出到文件系统、命令行选项的改进等。每个版本都根据反馈进行了调整，最终形成了 v4 版本。

**本周的新讨论与进展**：
1. **新功能**：本周的补丁包括添加了多个命令行选项，如指定测试可执行文件路径、设置超时限制、保存测试输出到指定目录、并行运行测试等。
2. **输出控制**：引入了打印选项，允许用户根据测试状态选择输出内容的详细程度。
3. **状态显示**：在测试执行过程中，运行器会在底部显示当前状态，包括总测试数、已执行测试数及各状态的测试数量。
4. **默认测试生成**：新增的 `tests_install` 规则可以自动生成默认测试用例，简化了测试的执行过程。
5. **文档更新**：补丁系列最后添加了 README 文件，详细说明了如何使用 KVM 自测试运行器。

总体而言，这一系列补丁显著提升了 KVM 自测试的灵活性和可用性，适应了更复杂的测试需求。

#### 📝 邮件列表

1. **[03-31 12:41]** [PATCH v4 0/9] KVM: selftests: Create KVM selftests runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
2. **[03-31 12:41]** [PATCH v4 1/9] KVM: selftest: Create KVM selftest runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
3. **[03-31 12:41]** [PATCH v4 2/9] KVM: selftests: Provide executables path option to the
 KVM selftest runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
4. **[03-31 12:41]** [PATCH v4 3/9] KVM: selftests: Add timeout option in selftests runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
5. **[03-31 12:41]** [PATCH v4 4/9] KVM: selftests: Add option to save selftest runner
 output to a directory
   - 发件人: Vipin Sharma <vipinsh@google.com>
6. **[03-31 12:41]** [PATCH v4 5/9] KVM: selftests: Run tests concurrently in KVM
 selftests runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
7. **[03-31 12:41]** [PATCH v4 6/9] KVM: selftests: Add various print flags to KVM
 selftest runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
8. **[03-31 12:42]** [PATCH v4 7/9] KVM: selftests: Print sticky KVM selftests runner
 status at bottom
   - 发件人: Vipin Sharma <vipinsh@google.com>
9. **[03-31 12:42]** [PATCH v4 8/9] KVM: selftests: Add rule to generate default tests for
 KVM selftests runner
   - 发件人: Vipin Sharma <vipinsh@google.com>
10. **[03-31 12:42]** [PATCH v4 9/9] KVM: selftests: Provide README.rst for KVM selftests runner
   - 发件人: Vipin Sharma <vipinsh@google.com>

---

### Thread 9: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 25 Mar 2026 18:05:26 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上支持 HDBSS（Hypervisor Dirty Bit Set Support）功能的补丁（PATCH v3 4/5）。该补丁旨在启用 HDBSS 支持并处理 HDBSSF 事件。

在历史讨论中，参与者 Tian Zheng 和 Leonardo Bras 交流了补丁的实现细节和潜在问题。Tian 提到在进行实时迁移时，启用脏页日志记录会触发大页拆分路径，并且在测试中未发现重大问题。Leonardo 对补丁的处理方式表示认可，并指出之前测试中遗漏了一些边缘情况，Tian 的补丁正好解决了这些问题。

在本周的新讨论中，Leonardo 提出了将 HDBSS 和 HACDBS 相关代码集中到一个文件中的建议，以提高代码的可维护性。Tian 同意了这一提议，并表示将在下一个版本中实施这一更改。此外，Leonardo 还表示将按照这种方式进行 HACDBS 的启用工作。

总的来说，本周的讨论集中在代码结构优化和补丁的进一步完善上，参与者们达成了一致意见，计划在后续版本中实施这些改进。

#### 📝 邮件列表

1. **[03-25 18:05]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[03-27 15:35]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
3. **[03-27 15:00]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[03-28 14:05]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
5. **[03-30 12:31]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[03-31 15:13]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>
7. **[04-02 10:40]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
8. **[04-02 13:42]** Re: [PATCH v3 0/5] Support the FEAT_HDBSS introduced in Armv9.5
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 10: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  1 Apr 2026 12:32:01 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁（patch），该补丁旨在让 SMC（Secure Monitor Call）处理程序接受 64 位的函数标识符，以保持与代码其他部分的一致性，并避免在处理 PSCI（Power State Coordination Interface）时出现的 u64 到 u32 的转换问题。

在之前的讨论中，参与者 Marc Zyngier 对此补丁提出了质疑，指出根据 ARM 规范，函数标识符应始终为 32 位，任何 64 位的值都应当被修正，而不是简单地传播。他强调，传递一个已知不正确的值到安全侧是不被接受的。

在本周的新讨论中，Sebastian Ene 认可了 Marc 的观点，并表示将根据建议进行修改，确保在处理函数标识符时，若高 32 位不为零，则应返回不支持的错误，而不是将其转发到安全侧。Sebastian 计划根据这些反馈重新提交补丁版本。整体来看，本周的讨论集中在对补丁的合理性和合规性的审查上，推动了补丁的改进。

#### 📝 邮件列表

1. **[04-01 12:32]** [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[04-01 15:55]** Re: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[04-01 17:21]** Re: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[04-01 19:28]** Re: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[04-01 19:34]** Re: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[04-02 19:46]** Re: [PATCH] KVM: arm64: Pass a 64bit function-id in the SMC handlers
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 11: [PATCH 0/3] KVM: arm64: Fix teardown of non-protected VMs with pKVM

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 31 Mar 2026 16:50:52 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）在 arm64 架构下的一个补丁系列，主要目的是修复与 pKVM 相关的非保护虚拟机（VM）拆解问题。

**原始补丁内容**：
补丁系列的核心是修复在虚拟机处于“正在死亡”（is_dying）状态时，错误地阻止了对其的引用，进而影响了与非保护虚拟机共享页面的能力。补丁通过防止对已引用虚拟机的拆解和允许在拆解过程中对正在死亡的虚拟机进行有限引用来解决这一问题。

**之前讨论要点**：
在之前的讨论中，开发者 Will Deacon 提到，之前的修复措施导致了在特定情况下无法正确拆解虚拟机，特别是在通过 VM 文件描述符销毁虚拟机时。此问题引发了对补丁的进一步审查和讨论。

**本周的新讨论与进展**：
本周，Will Deacon 提出了三个新的补丁，分别是：
1. 防止对已引用的虚拟机进行拆解。
2. 允许在拆解过程中对正在死亡的虚拟机进行引用。
3. 在回收页面时不再持有全局锁，以简化锁定机制。

这些补丁得到了参与者的认可，Mark Brown 进行了测试并确认修复有效，Marc Zyngier 表示已将补丁应用到下一个版本中。这表明该系列补丁已成功推进，并解决了先前提到的问题。

#### 📝 邮件列表

1. **[03-31 16:50]** [PATCH 0/3] KVM: arm64: Fix teardown of non-protected VMs with pKVM
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-31 16:50]** [PATCH 1/3] KVM: arm64: Prevent teardown finalisation of referenced 'hyp_vm'
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-31 16:50]** [PATCH 2/3] KVM: arm64: Allow get_pkvm_hyp_vm() to take a reference to a dying VM
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-31 16:50]** [PATCH 3/3] KVM: arm64: Don't hold 'vm_table_lock' across guest page reclaim
   - 发件人: Will Deacon <will@kernel.org>
5. **[04-01 14:33]** Re: [PATCH 0/3] KVM: arm64: Fix teardown of non-protected VMs with
 pKVM
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[04-01 16:29]** Re: [PATCH 0/3] KVM: arm64: Fix teardown of non-protected VMs with pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 12: [PATCH 0/4] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 30 Mar 2026 11:06:29 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的嵌套二级页表（nested stage-2）反向映射的补丁系列，旨在优化 MMU 通知的性能。

1. **原始补丁/问题内容**：补丁系列的核心是实现嵌套二级页表的反向映射，以便在 MMU 通知时能够更精确地解除映射，而不是完全解除所有嵌套 MMU 的映射。这种方法可以显著提高性能，尤其是在频繁调用 MMU 通知的情况下。

2. **之前讨论要点**：在历史讨论中，参与者指出在非嵌套模式下，解除映射相对简单，但在嵌套模式下，由于缺乏对嵌套映射的跟踪，导致必须完全解除所有映射，影响性能。因此，提出了通过建立反向映射来优化这一过程的想法。

3. **本周的新讨论、进展或结论**：本周的讨论中，Wei-Lin Chang 提出了四个补丁，分别实现了避免完全解除嵌套映射、加速解除映射、在 TLBI 处理期间移除反向映射条目，以及创建嵌套 IPA 到规范 IPA 的直接映射。补丁的实现细节包括使用 maple tree 数据结构来存储映射关系，并在处理 TLBI 时提高效率。参与者还讨论了补丁的测试计划，并注意到在构建过程中出现了一些错误，需进一步修复。

总体来看，这些补丁旨在提升 KVM 在处理嵌套虚拟化时的性能和效率。

#### 📝 邮件列表

1. **[03-30 11:06]** [PATCH 0/4] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-30 11:06]** [PATCH 1/4] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[03-30 11:06]** [PATCH 2/4] KVM: arm64: nv: Accelerate canonical IPA unmapping with canonical s2 mmu maple tree
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[03-30 11:06]** [PATCH 3/4] KVM: arm64: nv: Remove reverse map entries during TLBI handling
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[03-30 11:06]** [PATCH 4/4] KVM: arm64: nv: Create nested IPA direct map to speed up reverse map removal
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[03-31 23:16]** Re: [PATCH 1/4] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: kernel test robot <lkp@intel.com>

---

### Thread 13: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Wed,  1 Apr 2026 18:00:17 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中添加对 ID_AA64PFR2_EL1.GCIE 特性的支持。

1. **原始 patch/问题的内容**：Marc Zyngier 提出了一项补丁，目的是在内核特性集中添加 ID_AA64PFR2_EL1.GCIE 字段，以便用户空间能够在 GICv5 主机上正确设置该特性。

2. **之前的讨论要点**：本周的讨论没有涉及历史背景，所有邮件均为本周内的回复和进展。

3. **本周的新讨论、进展或结论**：本周的讨论中，Catalin Marinas 对补丁表示认可，并确认已应用。随后，Nathan Chancellor 在测试中发现该补丁导致启动时出现警告，提示特性重叠。Marc Zyngier 随后意识到字段顺序错误，并提出了修正方案，计划将修正合并到原始补丁中。整体来看，补丁的初步实现得到了认可，但仍需解决警告问题。

#### 📝 邮件列表

1. **[04-01 18:00]** [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-01 18:09]** Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[04-02 14:37]** Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-04 20:13]** Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Nathan Chancellor <nathan@kernel.org>
5. **[04-04 22:07]** Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 14: [PATCH v3] KVM: arm64: Prevent the host from using an smc with imm16
 != 0

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 30 Mar 2026 10:54:41 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构下的补丁，旨在防止主机在执行 SMC（Secure Monitor Call）指令时使用非零的 16 位立即数（imm16）。

**原始补丁内容**：
该补丁的核心是确保在 pKVM 环境下，主机内核只能使用值为 0 的立即数进行 SMC 调用，以符合 ARM 服务调用约定（SMCCC），并避免与不合规软件的冲突。补丁通过修改 `handle_host_smc` 函数来实现这一点，增加了对立即数的检查，并在不符合条件时返回错误。

**之前的讨论要点**：
在历史讨论中，补丁经历了多个版本的迭代，主要改进包括：
- 将立即数的解码逻辑移至正确的位置。
- 修改提交信息以更清晰地解释不对 HVC（Hypervisor Call）进行相同处理的原因。
- 从注入 UNDEF 改为返回 SMCCC_RET_NOT_SUPPORTED 错误。

**本周的新讨论与进展**：
本周的讨论中，参与者 Vincent Donnefort 对补丁进行了审核并表示支持，随后 Marc Zyngier 确认已将该补丁应用到下一个版本中。这表明该补丁已获得认可并进入实施阶段。

#### 📝 邮件列表

1. **[03-30 10:54]** [PATCH v3] KVM: arm64: Prevent the host from using an smc with imm16
 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-31 03:41]** Re: [PATCH v3] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-31 10:28]** Re: [PATCH v3] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[04-02 14:35]** Re: [PATCH v3] KVM: arm64: Prevent the host from using an smc with imm16 != 0
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 15: [PATCH v2 01/11] arm64: Skip update of an idreg field affected
 by an override

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 19 Mar 2026 15:34:47 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构中 CPU 特性覆盖（override）处理的补丁（patch）问题。原始补丁旨在跳过对受覆盖影响的 idreg 字段的更新，以确保系统在处理 CPU 特性时的安全性。

在历史讨论中，参与者探讨了 CPU 特性覆盖的机制，特别是当主 CPU 和次级 CPU 的特性值不同时，如何合理地管理和更新这些特性。Catalin Marinas 和 Suzuki K Poulose 提出了对覆盖值的优先级和安全性进行审查的建议，认为在某些情况下，次级 CPU 应该能够修改特性值，以确保系统能够选择最安全的特性值。

在本周的新讨论中，Suzuki K Poulose 提出了一个新的补丁，旨在确保当应用覆盖时，次级 CPU 也能正确应用这些覆盖，从而限制特性。这一补丁增加了对 CPU 本地能力的覆盖处理，确保在更新 CPU 特性时，能够考虑到已应用的覆盖值，从而提高系统的安全性和一致性。

总体而言，讨论集中在如何有效管理 ARM64 架构中 CPU 特性的覆盖问题，以确保系统的安全和稳定性。

#### 📝 邮件列表

1. **[03-19 15:34]** Re: [PATCH v2 01/11] arm64: Skip update of an idreg field affected
 by an override
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[03-25 14:54]** Re: [PATCH v2 01/11] arm64: Skip update of an idreg field affected by
 an override
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[03-25 17:51]** Re: [PATCH v2 01/11] arm64: Skip update of an idreg field affected
 by an override
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
4. **[03-31 12:20]** Re: [PATCH v2 01/11] arm64: Skip update of an idreg field affected by
 an override
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 16: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 30 Mar 2026 17:21:51 +0530

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（内核虚拟机）在 arm64 架构上 GICv3 的补丁（PATCH v4 35/49），该补丁旨在将 L1 LR（负载寄存器）同步集成到去激活原语中。

在历史讨论中，补丁的目的主要是优化 GICv3 的中断处理，特别是在虚拟化环境中对 L1 和 L0 的影响。然而，具体的历史讨论内容未在邮件中提供。

在本周的新讨论中，参与者 Vishnu Pajjuri 报告了在应用该补丁后，嵌套虚拟机（Nested VMs）无法启动，并导致 L0 和 L1 发生软锁死（soft lockup）。他通过回归测试确定问题源于该补丁，并询问其他开发者是否也遇到类似情况。Marc Zyngier 对此表示怀疑，并指出他在过去六个月内没有遇到此类问题，认为补丁解决了实际的错误，并不打算撤回。

Vishnu 进一步确认在回退该补丁后，能够成功启动 L2 客户机，表明补丁可能存在问题。Marc 则要求 Vishnu 提供更详细的调试信息，以帮助分析问题。

总体来看，本周的讨论集中在补丁引发的问题上，开发者们对补丁的有效性和潜在的错误进行了深入探讨。

#### 📝 邮件列表

1. **[03-30 17:21]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive
   - 发件人: Vishnu Pajjuri <vishnu@os.amperecomputing.com>
2. **[03-30 13:17]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-31 12:01]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into
 deactivation primitive
   - 发件人: Vishnu Pajjuri <vishnu@os.amperecomputing.com>
4. **[03-31 10:42]** Re: [PATCH v4 35/49] KVM: arm64: GICv3: nv: Plug L1 LR sync into deactivation primitive
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 17: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 31 Mar 2026 17:58:00 -0500

#### 🤖 AI 总结

本邮件讨论的主题是关于在 ARM64 架构中启用 FEAT_Debugv8p9 的补丁（PATCH V3 7/7），主要涉及硬件断点的实现。

在历史讨论中，补丁的目的在于增强 ARM64 的调试能力，特别是通过硬件断点来提升调试效率。补丁的实现涉及对 `hw_breakpoint_control()` 函数的 NOKPROBE_SYMBOL() 注解，以确保在特定情况下不会触发断点。

本周的新讨论集中在如何正确实现这一补丁的细节上。Rob Herring 和 Mark Rutland 讨论了在 `arch_install_hw_breakpoint()` 和 `arch_uninstall_hw_breakpoint()` 中是否需要禁用中断，以及如何处理 NOKPROBE_SYMBOL() 的注解。Rob 提到，x86 架构的实现并未使用该注解，而 Mark 则认为在 ARM64 中可能需要对某些函数进行相应的处理，以避免在不安全的上下文中设置硬件断点。

讨论中还提到，可能需要在操作相关硬件寄存器时暂时禁用断点和观察点，以确保操作的原子性和安全性。此外，双方同意需要在 `arch_build_bp_info()` 函数中增加对内核断点的限制，以防止在不适合的地方设置断点。

总体而言，本周的讨论推动了补丁的细化，明确了在实现过程中需要考虑的安全性和性能问题。

#### 📝 邮件列表

1. **[03-31 17:58]** Re: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9
   - 发件人: Rob Herring <robh@kernel.org>
2. **[04-02 11:37]** Re: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[04-02 12:46]** Re: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9
   - 发件人: Rob Herring <robh@kernel.org>

---

### Thread 18: [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare error

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 24 Mar 2026 17:27:57 +0000

#### 🤖 AI 总结

在本次邮件讨论中，主题为“[PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare error”的补丁旨在解决在进行 HVC（Hypervisor Call）操作时，如果出现错误，能够回滚引用计数，从而确保 hyp_shared_pfns 的跟踪状态与实际共享状态一致。该补丁由 Vincent Donnefort 提出。

在历史讨论中，Vincent 提到如果 HVC 操作失败，可能会导致多页范围的 kvm_{un}share_hyp() 函数出现问题，进而可能会泄露处于不良状态的页面。他认为，虽然失败的 HVC 操作是一个更大的问题，但仍需改进 kvm_share_hyp() 函数的错误处理。

在本周的新讨论中，Quentin Perret 对补丁提出了建议，认为在处理错误时需要更加小心，尤其是 kvm_unshare_hyp() 的处理可能会更复杂。他表示，虽然目前 HVC 失败的可能性较小，但补丁的目的是为了未来的安全性。Vincent 对此表示认可，并承认在提交信息中未能清晰表达这一点。

总体来看，本周讨论集中在补丁的错误处理和未来的安全性上，参与者达成了一致意见，认为补丁是朝着正确方向的改进。

#### 📝 邮件列表

1. **[03-24 17:27]** [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare error
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[03-30 09:41]** Re: [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare
 error
   - 发件人: Quentin Perret <qperret@google.com>
3. **[04-01 04:01]** Re: [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare
 error
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 19: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 5 Apr 2026 12:08:34 +0000

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE”，主要涉及对 ARM64 架构下 KVM 的 CPU 特性进行更新。

在历史讨论中，未提及具体的历史背景或之前的讨论内容，因此可以推测这是一个新的补丁提案。该补丁的主要内容是向 `arch/arm64/kernel/cpufeature.c` 文件中添加对 `ID_AA64PFR2_EL1.GCIE` 特性的声明，以解决在 RZ/G3L SMARC EVK 上出现的警告信息。

在本周的新讨论中，Biju Das 提出了补丁的具体代码修改，并指出该修改修复了特定的启动警告。此外，Biju Das 还对补丁进行了测试，并确认其有效性，表示“测试通过”。这表明补丁在功能上得到了验证，且没有其他参与者对此进行进一步的讨论或质疑。

总结来看，本周的讨论主要集中在补丁的代码实现和测试结果上，显示出对 ARM64 KVM 特性更新的积极推进。

#### 📝 邮件列表

1. **[04-05 12:08]** Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Biju Das <biju.das.jz@bp.renesas.com>
2. **[04-05 12:11]** RE: Re: [PATCH] KVM: arm64: Advertise ID_AA64PFR2_EL1.GCIE
   - 发件人: Biju Das <biju.das.jz@bp.renesas.com>

---

### Thread 20: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 1 Apr 2026 16:56:08 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch）——“[PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code”，旨在为 KVM/arm64 和 resctrl 提供支持。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁涉及到 ARM 架构下的多处理器资源管理，特别是与 KVM（内核虚拟机）和 resctrl（资源控制）相关的功能。

在本周的新讨论中，参与者 Fenghua Yu 和 Charles Rose 对该补丁进行了测试。Fenghua Yu 表示他在测试中确认了补丁的有效性，并标记为“测试通过”。Charles Rose 也在他的测试中验证了缓存占用和内存带宽分配功能在 Dell PowerEdge XE8712 服务器上正常工作，并同样标记为“测试通过”。这表明该补丁在实际硬件环境中得到了积极的反馈，显示出其功能的可靠性。

总体来看，本周的讨论集中在对补丁的测试结果上，参与者们对其表现表示满意，为补丁的进一步应用奠定了基础。

#### 📝 邮件列表

1. **[04-01 16:56]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Fenghua Yu <fenghuay@nvidia.com>
2. **[04-02 23:38]** RE: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Rose, Charles <Charles.Rose@dell.com>

---

### Thread 21: [PATCH] KVM: arm64: vgic-v5: Fold PPI state for all exposed PPIs

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 1 Apr 2026 16:21:57 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-v5（虚拟通用中断控制器版本5）中对 PPI（私有中断）的状态管理进行优化的补丁。

原始补丁的内容是为了减少对 GICv5 中多达 128 个 PPI 的状态跟踪开销，提议仅跟踪前 64 个架构化的 PPI，并且通常只向虚拟机暴露 4 个 PPI（SW_PPI、PMUIRQ 和定时器）。补丁通过简化 PPI 状态的跟踪方式，避免了在退出虚拟机时可能丢失边缘中断的问题。

在之前的讨论中，参与者指出了在处理边缘中断时，跟踪状态的方式可能导致中断丢失，因此需要重新设计 PPI 状态的管理。

本周的新讨论中，Sascha Bischoff 提交了补丁，Marc Zyngier 随后确认并表示已将该补丁应用到下一个版本中。这表明该补丁得到了认可并将继续推进。整体来看，此次讨论集中在优化 PPI 状态管理的实现上，以提高系统的稳定性和性能。

#### 📝 邮件列表

1. **[04-01 16:21]** [PATCH] KVM: arm64: vgic-v5: Fold PPI state for all exposed PPIs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[04-02 14:37]** Re: [PATCH] KVM: arm64: vgic-v5: Fold PPI state for all exposed PPIs
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 22: [PATCH] KVM: arm64: selftests: Avoid testing the IMPDEF behavior

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 17 Mar 2026 21:15:58 +0800

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试的补丁，主题为“避免测试 IMPDEF 行为”。

在历史讨论中，Zenghui Yu 提出了一个补丁，指出在模拟 AT 指令时，KVM 无法强制使用“慢路径”，因此应该避免测试 IMPDEF 行为（即 TEST_ACCESS_FLAG——地址转换指令可以更新 AF，但不是必须的）。该补丁旨在移除相关测试并改善注释，以提高代码的清晰度。

在本周的新讨论中，Marc Zyngier 回复确认已将该补丁应用到下一个版本中，并表示感谢。这表明补丁得到了认可并将继续推进。

总结而言，补丁的核心是优化 KVM 的自测试，避免不必要的 IMPDEF 行为测试，历史讨论提供了背景信息，而本周的进展则是补丁的成功应用。

#### 📝 邮件列表

1. **[03-17 21:15]** [PATCH] KVM: arm64: selftests: Avoid testing the IMPDEF behavior
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
2. **[04-02 14:37]** Re: [PATCH] KVM: arm64: selftests: Avoid testing the IMPDEF behavior
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 23: [PATCH 0/2] KVM: arm64: Tentative fixes for page-table lifetime issues

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 27 Mar 2026 19:27:55 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的页表生命周期问题的修复补丁。历史讨论中，Will Deacon 提出了两个潜在的页表生命周期问题，这些问题是在审查 pKVM 保护内存系列时被 Sashiko 指出。Will 对这些问题进行了分析，并尝试修复，同时在提交信息中详细描述了问题的背景。他还通过强制通知注册失败的方式进行了测试，以观察在尝试创建虚拟机时 `/proc/meminfo` 中 SecPageTables 的变化。

在本周的新讨论中，Marc Zyngier 回复确认将 Will 提出的补丁应用到下一个版本中，并列出了两个具体的补丁：第一个补丁修复了在 `kvm_init_stage2_mmu()` 错误时不应留下 `mmu->pgt` 的问题，第二个补丁则确保在 `kvm_arch_destroy_vm()` 中销毁阶段二页表。这表明补丁已获得认可并将被纳入后续开发中。

#### 📝 邮件列表

1. **[03-27 19:27]** [PATCH 0/2] KVM: arm64: Tentative fixes for page-table lifetime issues
   - 发件人: Will Deacon <will@kernel.org>
2. **[04-02 14:36]** Re: [PATCH 0/2] KVM: arm64: Tentative fixes for page-table lifetime issues
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 24: [PATCH] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 30 Mar 2026 16:29:26 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 在 arm64 架构下的一个补丁，主要内容是移除在 `finalise_el2()` 函数中对 `TPIDR_EL2` 的冗余初始化。

**原始补丁内容**：
补丁提议删除 `finalise_el2()` 中对 `TPIDR_EL2` 的初始化，因为在使用 VHE（虚拟化扩展）时，`TPIDR_EL2` 仅在检测到 `ARM64_HAS_VIRT_HOST_EXTN` 能力后由 `cpu_copy_el2regs()` 从 `TPIDR_EL1` 中填充。因此，`finalise_el2()` 中的初始化是多余的。

**之前的讨论要点**：
在之前的讨论中，补丁的必要性和实现方式并未详细阐述。参与者 Will Deacon 通过代码检查发现了这一冗余，并提出了补丁。

**本周的新讨论与进展**：
在本周的讨论中，Mark Rutland 对补丁的提交信息提出了建议，认为需要更详细地解释 `TPIDR_EL2` 在引导 CPU 和次级 CPU 中的工作机制。他建议补充说明 `finalise_el2()` 不需要初始化 `TPIDR_EL2` 的原因，包括对引导 CPU 和次级 CPU 的处理逻辑。Mark 还表示支持该补丁，并给予了审核意见。

总结来看，本周的讨论主要集中在补丁的描述和逻辑清晰度上，确保补丁的意图和实现细节能够被更好地理解。

#### 📝 邮件列表

1. **[03-30 16:29]** [PATCH] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-31 11:18]** Re: [PATCH] KVM: arm64: Don't populate TPIDR_EL2 in finalise_el2()
   - 发件人: Mark Rutland <mark.rutland@arm.com>

---

### Thread 25: (subset) [PATCH v10 00/30] KVM: arm64: Implement support for SME

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu,  2 Apr 2026 22:12:18 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构上实现对 SME（Scalable Matrix Extension）的支持。当前邮件是本周的新讨论，涉及到一个补丁系列的进展。

原始的补丁（PATCH v10 00/30）旨在为 arm64 架构的 KVM 实现对 SME 的支持，具体补丁内容包括更新 SMIDR_EL1 寄存器，以符合 DDI0601 版本的规范。

在之前的讨论中，参与者 Mark Brown 提到已经将补丁应用到 arm64 的 for-next/sysreg 分支，并表示他查看了更多核心架构的补丁，发现它们大多是为后续的 KVM 支持做准备。他对后续补丁的审查表示关注，尤其是前几条补丁在后续审查中是否会有变动。

本周的新进展是补丁已经被应用，且参与者在讨论中确认了对后续补丁的关注，表明整个补丁系列的开发仍在进行中，且对其稳定性和一致性保持警惕。

#### 📝 邮件列表

1. **[04-02 22:12]** Re: (subset) [PATCH v10 00/30] KVM: arm64: Implement support for SME
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 26: [PATCH] arm64: clear_page[s] using memset

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 2 Apr 2026 21:57:08 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 arm64 架构中使用 memset 函数来实现 clear_page 和 clear_pages 的补丁（patch）。该补丁旨在优化内存清零操作。

在历史讨论中，尚未有其他邮件记录，因此没有提供具体的背景信息或之前的讨论要点。

在本周的新讨论中，参与者 Catalin Marinas 对 Linus Walleij 的提议进行了回应。Walleij 提出是否可以将该功能移至通用代码中，只有少数需要自定义实现的平台才进行覆盖。他还询问是否可以对 copy_page() 进行类似处理。Marinas 指出，当前的自定义 clear_page() 函数虽然增加了工作量，但有一个小优势，即可以跳过长度和对齐检查，因为这些操作始终是以页面大小为单位的。此外，他还确认了基准测试是在真实硬件上进行的，而不是在 qemu 上。

总体来看，本周的讨论集中在是否将该补丁的实现移至更通用的代码层面，以及自定义实现的利弊分析上。

#### 📝 邮件列表

1. **[04-02 21:57]** Re: [PATCH] arm64: clear_page[s] using memset
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 27: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 31 Mar 2026 18:02:13 -0500

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM64 架构的补丁，旨在启用 FEAT_Debugv8p9 功能，具体为 `arm64/hw_breakpoint` 的改进。

在本周的新讨论中，参与者 Rob Herring 对补丁提出了反馈。他指出，当前补丁的实现位置不当，导致相关代码在每次启用时都会执行，而不仅仅是在首次启用内核或用户模式的断点时。Herring 建议将相关代码移动到适当的位置，以确保其仅在需要时执行。

由于本邮件线程没有历史讨论的上下文，因此没有之前的讨论要点可供参考。整体来看，本周的讨论集中在补丁的代码逻辑和执行时机的优化上，强调了代码位置对功能实现的重要性。

#### 📝 邮件列表

1. **[03-31 18:02]** Re: [PATCH V3 7/7] arm64/hw_breakpoint: Enable FEAT_Debugv8p9
   - 发件人: Rob Herring <robh@kernel.org>

---

### Thread 28: [PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to
 fault-in on !mmap()'d memory

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 30 Mar 2026 14:21:50 +0800

#### 🤖 AI 总结

本邮件主题为“[PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to fault-in on !mmap()'d memory”，主要讨论了一个针对 KVM 的自测试补丁。

1. **原始 patch/问题的内容**：该补丁旨在为 KVM 添加一个新的自测试用例，测试在未通过 mmap() 映射的内存上进行 fault-in 操作的功能。具体来说，它涉及到 guest_memfd 测试用例的实现。

2. **之前的讨论要点**：本邮件没有提供历史讨论的内容，因此无法总结之前的讨论要点。

3. **本周的新讨论、进展或结论**：在本周的讨论中，Zenghui Yu 提到该测试在 arm64 架构下失败，具体表现为在页面大小为 4K 的虚拟机与 64K 的主机之间存在不兼容问题。测试运行时出现了无效参数的错误，导致 KVM_CREATE_GUEST_MEMFD 调用失败。Zenghui Yu 提供了详细的错误信息和堆栈跟踪，表明该问题需要进一步调查和修复。

总体来看，本周的讨论集中在补丁的测试失败问题上，强调了不同页面大小之间的兼容性问题。

#### 📝 邮件列表

1. **[03-30 14:21]** Re: [PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to
 fault-in on !mmap()'d memory
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

