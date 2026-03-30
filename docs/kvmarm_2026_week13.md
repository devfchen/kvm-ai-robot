# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-03-30 00:35:38

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 366
- **总 Thread 数**: 35
- **大型 Thread** (>20封): 4 个

### 分类分布

- **PATCH**: 32 threads (344 邮件)
- **RFC**: 1 threads (13 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Other**: 1 threads (7 邮件)

---

## 📌 PATCH

共 32 个 thread

---

### Thread 1: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code

**📧 邮件数**: 73 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 13 Mar 2026 14:45:37 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 ARM MPAM（内存分区和监控）与 KVM/arm64 及 resctrl 代码集成的补丁系列（PATCH v6 00/40）。该补丁旨在增强 ARM 架构下的资源控制和监控功能。

**原始补丁内容**：补丁系列主要涉及 MPAM 的实现，包括对 L3 缓存的分区、内存带宽限制、以及与 resctrl 的集成。补丁中删除了一些复杂的功能，如内存带宽利用率的支持，以简化代码并为未来的流量过滤功能铺平道路。

**之前讨论要点**：历史讨论中，参与者们集中在补丁的各个部分上，讨论了如何确保在应用配置后，MPAM 的状态正确更新，以及如何处理不同配置下的重置逻辑。此外，补丁还涉及了对 CDP（Cache Allocation Technology）的模拟和相关功能的隐藏，以避免潜在的错误。

**本周新讨论与进展**：本周的讨论主要集中在对补丁的审查和测试反馈上。Gavin Shan 对多个补丁进行了测试，确认了 L3 缓存分区和内存带宽限制的正常工作，并对补丁中的一些代码一致性问题提出了建议。James Morse 也参与了讨论，确认了对补丁的接受，并表示将根据反馈进行必要的修改。整体来看，补丁系列在向 Linux v7.1 的推进中取得了积极进展，参与者对最终实现表示乐观。

#### 📝 邮件列表

1. **[03-13 14:45]** [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
2. **[03-13 14:45]** [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after applying configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
3. **[03-13 14:45]** [PATCH v6 02/40] arm_mpam: Reset when feature configuration bit unset
   - 发件人: Ben Horgan <ben.horgan@arm.com>
4. **[03-13 14:45]** [PATCH v6 08/40] arm64: mpam: Drop the CONFIG_EXPERT restriction
   - 发件人: Ben Horgan <ben.horgan@arm.com>
5. **[03-13 14:45]** [PATCH v6 11/40] arm64: mpam: Initialise and context switch the MPAMSM_EL1 register
   - 发件人: Ben Horgan <ben.horgan@arm.com>
6. **[03-13 14:45]** [PATCH v6 14/40] arm_mpam: resctrl: Add boilerplate cpuhp and domain allocation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
7. **[03-13 14:45]** [PATCH v6 15/40] arm_mpam: resctrl: Pick the caches we will use as resctrl resources
   - 发件人: Ben Horgan <ben.horgan@arm.com>
8. **[03-13 14:45]** [PATCH v6 16/40] arm_mpam: resctrl: Implement resctrl_arch_reset_all_ctrls()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[03-13 14:45]** [PATCH v6 17/40] arm_mpam: resctrl: Add resctrl_arch_get_config()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
10. **[03-13 14:45]** [PATCH v6 18/40] arm_mpam: resctrl: Implement helpers to update configuration
   - 发件人: Ben Horgan <ben.horgan@arm.com>
11. **[03-13 14:45]** [PATCH v6 19/40] arm_mpam: resctrl: Add plumbing against arm64 task and cpu hooks
   - 发件人: Ben Horgan <ben.horgan@arm.com>
12. **[03-13 14:45]** [PATCH v6 20/40] arm_mpam: resctrl: Add CDP emulation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
13. **[03-13 14:45]** [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind CONFIG_EXPERT
   - 发件人: Ben Horgan <ben.horgan@arm.com>
14. **[03-13 14:45]** [PATCH v6 22/40] arm_mpam: resctrl: Convert to/from MPAMs fixed-point formats
   - 发件人: Ben Horgan <ben.horgan@arm.com>
15. **[03-13 14:46]** [PATCH v6 23/40] arm_mpam: resctrl: Add rmid index helpers
   - 发件人: Ben Horgan <ben.horgan@arm.com>
16. **[03-13 14:46]** [PATCH v6 24/40] arm_mpam: resctrl: Wait for cacheinfo to be ready
   - 发件人: Ben Horgan <ben.horgan@arm.com>
17. **[03-13 14:46]** [PATCH v6 25/40] arm_mpam: resctrl: Add support for 'MB' resource
   - 发件人: Ben Horgan <ben.horgan@arm.com>
18. **[03-13 14:46]** [PATCH v6 26/40] arm_mpam: resctrl: Add kunit test for control format conversions
   - 发件人: Ben Horgan <ben.horgan@arm.com>
19. **[03-13 14:46]** [PATCH v6 27/40] arm_mpam: resctrl: Add monitor initialisation and domain boilerplate
   - 发件人: Ben Horgan <ben.horgan@arm.com>
20. **[03-13 14:46]** [PATCH v6 28/40] arm_mpam: resctrl: Add support for csu counters
   - 发件人: Ben Horgan <ben.horgan@arm.com>
21. **[03-13 14:46]** [PATCH v6 29/40] arm_mpam: resctrl: Allow resctrl to allocate monitors
   - 发件人: Ben Horgan <ben.horgan@arm.com>
22. **[03-13 14:46]** [PATCH v6 30/40] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
   - 发件人: Ben Horgan <ben.horgan@arm.com>
23. **[03-13 14:46]** [PATCH v6 31/40] arm_mpam: resctrl: Update the rmid reallocation limit
   - 发件人: Ben Horgan <ben.horgan@arm.com>
24. **[03-13 14:46]** [PATCH v6 32/40] arm_mpam: resctrl: Add empty definitions for assorted resctrl functions
   - 发件人: Ben Horgan <ben.horgan@arm.com>
25. **[03-13 14:46]** [PATCH v6 33/40] arm64: mpam: Select ARCH_HAS_CPU_RESCTRL
   - 发件人: Ben Horgan <ben.horgan@arm.com>
26. **[03-13 14:46]** [PATCH v6 34/40] arm_mpam: resctrl: Call resctrl_init() on platforms that can support resctrl
   - 发件人: Ben Horgan <ben.horgan@arm.com>
27. **[03-13 14:46]** [PATCH v6 35/40] arm_mpam: Add quirk framework
   - 发件人: Ben Horgan <ben.horgan@arm.com>
28. **[03-13 14:46]** [PATCH v6 36/40] arm_mpam: Add workaround for T241-MPAM-1
   - 发件人: Ben Horgan <ben.horgan@arm.com>
29. **[03-13 14:46]** [PATCH v6 37/40] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Ben Horgan <ben.horgan@arm.com>
30. **[03-13 14:46]** [PATCH v6 38/40] arm_mpam: Add workaround for T241-MPAM-6
   - 发件人: Ben Horgan <ben.horgan@arm.com>
31. **[03-13 14:46]** [PATCH v6 39/40] arm_mpam: Quirk CMN-650's CSU NRDY behaviour
   - 发件人: Ben Horgan <ben.horgan@arm.com>
32. **[03-13 14:46]** [PATCH v6 40/40] arm64: mpam: Add initial MPAM documentation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
33. **[03-23 14:37]** Re: [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after
 applying configuration
   - 发件人: Gavin Shan <gshan@redhat.com>
34. **[03-23 14:41]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Gavin Shan <gshan@redhat.com>
35. **[03-23 14:44]** Re: [PATCH v6 02/40] arm_mpam: Reset when feature configuration bit
 unset
   - 发件人: Gavin Shan <gshan@redhat.com>
36. **[03-23 16:31]** Re: [PATCH v6 14/40] arm_mpam: resctrl: Add boilerplate cpuhp and
 domain allocation
   - 发件人: Gavin Shan <gshan@redhat.com>
37. **[03-23 16:37]** Re: [PATCH v6 15/40] arm_mpam: resctrl: Pick the caches we will use
 as resctrl resources
   - 发件人: Gavin Shan <gshan@redhat.com>
38. **[03-23 16:41]** Re: [PATCH v6 16/40] arm_mpam: resctrl: Implement
 resctrl_arch_reset_all_ctrls()
   - 发件人: Gavin Shan <gshan@redhat.com>
39. **[03-23 16:47]** Re: [PATCH v6 17/40] arm_mpam: resctrl: Add resctrl_arch_get_config()
   - 发件人: Gavin Shan <gshan@redhat.com>
40. **[03-23 16:51]** Re: [PATCH v6 18/40] arm_mpam: resctrl: Implement helpers to update
 configuration
   - 发件人: Gavin Shan <gshan@redhat.com>
41. **[03-23 16:55]** Re: [PATCH v6 19/40] arm_mpam: resctrl: Add plumbing against arm64
 task and cpu hooks
   - 发件人: Gavin Shan <gshan@redhat.com>
42. **[03-23 10:13]** Re: [PATCH v6 14/40] arm_mpam: resctrl: Add boilerplate cpuhp and
 domain allocation
   - 发件人: Ben Horgan <ben.horgan@arm.com>
43. **[03-24 08:35]** Re: [PATCH v6 20/40] arm_mpam: resctrl: Add CDP emulation
   - 发件人: Gavin Shan <gshan@redhat.com>
44. **[03-24 08:36]** Re: [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind
 CONFIG_EXPERT
   - 发件人: Gavin Shan <gshan@redhat.com>
45. **[03-24 08:49]** Re: [PATCH v6 22/40] arm_mpam: resctrl: Convert to/from MPAMs
 fixed-point formats
   - 发件人: Gavin Shan <gshan@redhat.com>
46. **[03-24 08:50]** Re: [PATCH v6 23/40] arm_mpam: resctrl: Add rmid index helpers
   - 发件人: Gavin Shan <gshan@redhat.com>
47. **[03-24 08:53]** Re: [PATCH v6 24/40] arm_mpam: resctrl: Wait for cacheinfo to be
 ready
   - 发件人: Gavin Shan <gshan@redhat.com>
48. **[03-24 09:09]** Re: [PATCH v6 25/40] arm_mpam: resctrl: Add support for 'MB' resource
   - 发件人: Gavin Shan <gshan@redhat.com>
49. **[03-24 09:10]** Re: [PATCH v6 26/40] arm_mpam: resctrl: Add kunit test for control
 format conversions
   - 发件人: Gavin Shan <gshan@redhat.com>
50. **[03-24 13:40]** Re: [PATCH v6 27/40] arm_mpam: resctrl: Add monitor initialisation
 and domain boilerplate
   - 发件人: Gavin Shan <gshan@redhat.com>
51. **[03-24 13:40]** Re: [PATCH v6 28/40] arm_mpam: resctrl: Add support for csu counters
   - 发件人: Gavin Shan <gshan@redhat.com>
52. **[03-24 13:41]** Re: [PATCH v6 29/40] arm_mpam: resctrl: Allow resctrl to allocate
 monitors
   - 发件人: Gavin Shan <gshan@redhat.com>
53. **[03-24 13:41]** Re: [PATCH v6 30/40] arm_mpam: resctrl: Add resctrl_arch_rmid_read()
   - 发件人: Gavin Shan <gshan@redhat.com>
54. **[03-24 13:42]** Re: [PATCH v6 31/40] arm_mpam: resctrl: Update the rmid reallocation
 limit
   - 发件人: Gavin Shan <gshan@redhat.com>
55. **[03-24 13:42]** Re: [PATCH v6 32/40] arm_mpam: resctrl: Add empty definitions for
 assorted resctrl functions
   - 发件人: Gavin Shan <gshan@redhat.com>
56. **[03-24 13:42]** Re: [PATCH v6 33/40] arm64: mpam: Select ARCH_HAS_CPU_RESCTRL
   - 发件人: Gavin Shan <gshan@redhat.com>
57. **[03-24 13:43]** Re: [PATCH v6 34/40] arm_mpam: resctrl: Call resctrl_init() on
 platforms that can support resctrl
   - 发件人: Gavin Shan <gshan@redhat.com>
58. **[03-24 13:56]** Re: [PATCH v6 35/40] arm_mpam: Add quirk framework
   - 发件人: Gavin Shan <gshan@redhat.com>
59. **[03-24 14:16]** Re: [PATCH v6 36/40] arm_mpam: Add workaround for T241-MPAM-1
   - 发件人: Gavin Shan <gshan@redhat.com>
60. **[03-24 14:19]** Re: [PATCH v6 37/40] arm_mpam: Add workaround for T241-MPAM-4
   - 发件人: Gavin Shan <gshan@redhat.com>
61. **[03-24 14:20]** Re: [PATCH v6 38/40] arm_mpam: Add workaround for T241-MPAM-6
   - 发件人: Gavin Shan <gshan@redhat.com>
62. **[03-24 14:21]** Re: [PATCH v6 39/40] arm_mpam: Quirk CMN-650's CSU NRDY behaviour
   - 发件人: Gavin Shan <gshan@redhat.com>
63. **[03-24 16:04]** Re: [PATCH v6 40/40] arm64: mpam: Add initial MPAM documentation
   - 发件人: Gavin Shan <gshan@redhat.com>
64. **[03-24 10:09]** Re: [PATCH v6 00/40] arm_mpam: Add KVM/arm64 and resctrl glue code
   - 发件人: Ben Horgan <ben.horgan@arm.com>
65. **[03-26 12:20]** Re: [PATCH v6 14/40] arm_mpam: resctrl: Add boilerplate cpuhp and
 domain allocation
   - 发件人: James Morse <james.morse@arm.com>
66. **[03-27 15:42]** Re: [PATCH v6 01/40] arm_mpam: Ensure in_reset_state is false after
 applying configuration
   - 发件人: James Morse <james.morse@arm.com>
67. **[03-27 15:43]** Re: [PATCH v6 08/40] arm64: mpam: Drop the CONFIG_EXPERT restriction
   - 发件人: James Morse <james.morse@arm.com>
68. **[03-27 15:44]** Re: [PATCH v6 11/40] arm64: mpam: Initialise and context switch the
 MPAMSM_EL1 register
   - 发件人: James Morse <james.morse@arm.com>
69. **[03-27 15:44]** Re: [PATCH v6 21/40] arm_mpam: resctrl: Hide CDP emulation behind
 CONFIG_EXPERT
   - 发件人: James Morse <james.morse@arm.com>
70. **[03-27 15:47]** Re: [PATCH v6 22/40] arm_mpam: resctrl: Convert to/from MPAMs
 fixed-point formats
   - 发件人: James Morse <james.morse@arm.com>
71. **[03-27 15:47]** Re: [PATCH v6 25/40] arm_mpam: resctrl: Add support for 'MB' resource
   - 发件人: James Morse <james.morse@arm.com>
72. **[03-27 15:48]** Re: [PATCH v6 36/40] arm_mpam: Add workaround for T241-MPAM-1
   - 发件人: James Morse <james.morse@arm.com>
73. **[03-27 16:21]** Re: [PATCH v6 02/40] arm_mpam: Reset when feature configuration bit
 unset
   - 发件人: James Morse <james.morse@arm.com>

---

### Thread 2: [PATCH v4 00/38] KVM: arm64: Add support for protected guest memory with pKVM

**📧 邮件数**: 40 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 27 Mar 2026 13:59:59 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上添加受保护虚拟机（pKVM）内存支持的补丁（PATCH v4 00/38）。以下是讨论的主要内容：

1. **原始补丁内容**：补丁旨在为 KVM 添加对受保护虚拟机内存的支持，允许虚拟机在与主机隔离的情况下运行。补丁包括一系列功能的实现和修改，以确保受保护虚拟机的内存管理和访问控制。

2. **历史讨论要点**：之前的补丁版本（v1、v2、v3）已经提出了一些基础功能，但在本周的讨论中，开发者对补丁进行了重构和优化，包括去除未使用的定义、调整依赖关系、更新文档等。补丁还引入了新的超调用（hypercall）以支持内存捐赠和回收。

3. **本周新讨论和进展**：本周的讨论集中在补丁的多个方面，包括：
   - 引入新的超调用以支持受保护虚拟机的内存共享和取消共享。
   - 增强了内存回收机制，确保在虚拟机销毁时能够安全地回收内存。
   - 讨论了如何处理主机对受保护虚拟机内存的非法访问，确保在发生错误时能够返回合适的错误代码。
   - 增加了对受保护虚拟机的自测功能，以验证内存捐赠和回收的正确性。

总的来说，本周的讨论推动了 pKVM 功能的进一步完善，并为未来的开发奠定了基础。开发者计划在后续版本中解决一些生命周期相关的问题。

#### 📝 邮件列表

1. **[03-27 13:59]** [PATCH v4 00/38] KVM: arm64: Add support for protected guest memory with pKVM
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-27 14:00]** [PATCH v4 01/38] KVM: arm64: Remove unused PKVM_ID_FFA definition
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-27 14:00]** [PATCH v4 02/38] KVM: arm64: Don't leak stage-2 page-table if VM fails to init under pKVM
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-27 14:00]** [PATCH v4 03/38] KVM: arm64: Move handle check into pkvm_pgtable_stage2_destroy_range()
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-27 14:00]** [PATCH v4 04/38] KVM: arm64: Rename __pkvm_pgtable_stage2_unmap()
   - 发件人: Will Deacon <will@kernel.org>
6. **[03-27 14:00]** [PATCH v4 05/38] KVM: arm64: Don't advertise unsupported features for protected guests
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-27 14:00]** [PATCH v4 06/38] KVM: arm64: Expose self-hosted debug regs as RAZ/WI for protected guests
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-27 14:00]** [PATCH v4 07/38] KVM: arm64: Remove is_protected_kvm_enabled() checks from hypercalls
   - 发件人: Will Deacon <will@kernel.org>
9. **[03-27 14:00]** [PATCH v4 08/38] KVM: arm64: Ignore MMU notifier callbacks for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
10. **[03-27 14:00]** [PATCH v4 09/38] KVM: arm64: Prevent unsupported memslot operations on protected VMs
   - 发件人: Will Deacon <will@kernel.org>
11. **[03-27 14:00]** [PATCH v4 10/38] KVM: arm64: Ignore -EAGAIN when mapping in pages for the pKVM host
   - 发件人: Will Deacon <will@kernel.org>
12. **[03-27 14:00]** [PATCH v4 11/38] KVM: arm64: Split teardown hypercall into two phases
   - 发件人: Will Deacon <will@kernel.org>
13. **[03-27 14:00]** [PATCH v4 12/38] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Will Deacon <will@kernel.org>
14. **[03-27 14:00]** [PATCH v4 13/38] KVM: arm64: Hook up donation hypercall to pkvm_pgtable_stage2_map()
   - 发件人: Will Deacon <will@kernel.org>
15. **[03-27 14:00]** [PATCH v4 14/38] KVM: arm64: Handle aborts from protected VMs
   - 发件人: Will Deacon <will@kernel.org>
16. **[03-27 14:00]** [PATCH v4 15/38] KVM: arm64: Introduce __pkvm_reclaim_dying_guest_page()
   - 发件人: Will Deacon <will@kernel.org>
17. **[03-27 14:00]** [PATCH v4 16/38] KVM: arm64: Hook up reclaim hypercall to pkvm_pgtable_stage2_destroy()
   - 发件人: Will Deacon <will@kernel.org>
18. **[03-27 14:00]** [PATCH v4 17/38] KVM: arm64: Factor out pKVM host exception injection logic
   - 发件人: Will Deacon <will@kernel.org>
19. **[03-27 14:00]** [PATCH v4 18/38] KVM: arm64: Support translation faults in inject_host_exception()
   - 发件人: Will Deacon <will@kernel.org>
20. **[03-27 14:00]** [PATCH v4 19/38] KVM: arm64: Inject SIGSEGV on illegal accesses
   - 发件人: Will Deacon <will@kernel.org>
21. **[03-27 14:00]** [PATCH v4 20/38] KVM: arm64: Avoid pointless annotation when mapping host-owned pages
   - 发件人: Will Deacon <will@kernel.org>
22. **[03-27 14:00]** [PATCH v4 21/38] KVM: arm64: Generalise kvm_pgtable_stage2_set_owner()
   - 发件人: Will Deacon <will@kernel.org>
23. **[03-27 14:00]** [PATCH v4 22/38] KVM: arm64: Introduce host_stage2_set_owner_metadata_locked()
   - 发件人: Will Deacon <will@kernel.org>
24. **[03-27 14:00]** [PATCH v4 23/38] KVM: arm64: Change 'pkvm_handle_t' to u16
   - 发件人: Will Deacon <will@kernel.org>
25. **[03-27 14:00]** [PATCH v4 24/38] KVM: arm64: Annotate guest donations with handle and gfn in host stage-2
   - 发件人: Will Deacon <will@kernel.org>
26. **[03-27 14:00]** [PATCH v4 25/38] KVM: arm64: Introduce hypercall to force reclaim of a protected page
   - 发件人: Will Deacon <will@kernel.org>
27. **[03-27 14:00]** [PATCH v4 26/38] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Will Deacon <will@kernel.org>
28. **[03-27 14:00]** [PATCH v4 27/38] KVM: arm64: Return -EFAULT from VCPU_RUN on access to a poisoned pte
   - 发件人: Will Deacon <will@kernel.org>
29. **[03-27 14:00]** [PATCH v4 28/38] KVM: arm64: Add hvc handler at EL2 for hypercalls from protected VMs
   - 发件人: Will Deacon <will@kernel.org>
30. **[03-27 14:00]** [PATCH v4 29/38] KVM: arm64: Implement the MEM_SHARE hypercall for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
31. **[03-27 14:00]** [PATCH v4 30/38] KVM: arm64: Implement the MEM_UNSHARE hypercall for protected VMs
   - 发件人: Will Deacon <will@kernel.org>
32. **[03-27 14:00]** [PATCH v4 31/38] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Will Deacon <will@kernel.org>
33. **[03-27 14:00]** [PATCH v4 32/38] KVM: arm64: Add some initial documentation for pKVM
   - 发件人: Will Deacon <will@kernel.org>
34. **[03-27 14:00]** [PATCH v4 33/38] KVM: arm64: Extend pKVM page ownership selftests to cover guest donation
   - 发件人: Will Deacon <will@kernel.org>
35. **[03-27 14:00]** [PATCH v4 34/38] KVM: arm64: Register 'selftest_vm' in the VM table
   - 发件人: Will Deacon <will@kernel.org>
36. **[03-27 14:00]** [PATCH v4 35/38] KVM: arm64: Extend pKVM page ownership selftests to cover forced reclaim
   - 发件人: Will Deacon <will@kernel.org>
37. **[03-27 14:00]** [PATCH v4 36/38] KVM: arm64: Extend pKVM page ownership selftests to cover guest hvcs
   - 发件人: Will Deacon <will@kernel.org>
38. **[03-27 14:00]** [PATCH v4 37/38] KVM: arm64: Rename PKVM_PAGE_STATE_MASK
   - 发件人: Will Deacon <will@kernel.org>
39. **[03-27 14:00]** [PATCH v4 38/38] drivers/virt: pkvm: Add Kconfig dependency on DMA_RESTRICTED_POOL
   - 发件人: Will Deacon <will@kernel.org>
40. **[03-27 18:13]** Re: [PATCH v4 00/38] KVM: arm64: Add support for protected guest
 memory with pKVM
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 3: [PATCH v2 00/30] KVM: arm64: Combined user_mem_abort() rework

**📧 邮件数**: 33 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 27 Mar 2026 11:35:48 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构上的 `user_mem_abort()` 函数的重构和优化，主要集中在将其拆分为多个更小的辅助函数，以提高代码的可读性和可维护性。

1. **原始 patch/问题的内容**：
   - 提出的补丁（PATCH v2 00/30）旨在重构 `user_mem_abort()` 函数，目的是将其复杂的逻辑分解为多个专注的辅助函数，以简化处理过程并减少代码重复。

2. **之前讨论要点**：
   - 早期讨论中提到，`user_mem_abort()` 函数的参数过多，导致函数难以理解和维护。参与者们一致认为通过引入结构体 `kvm_s2_fault` 和其他辅助函数，可以有效地管理状态和参数。

3. **本周的新讨论、进展或结论**：
   - 本周的讨论中，参与者们提交了多个补丁，逐步完成了重构工作，包括：
     - 将 VMA（虚拟内存区域）相关信息提取到新的结构体 `kvm_s2_fault_vma_info` 中。
     - 简化了权限计算逻辑，并将其移入辅助函数中。
     - 优化了错误处理逻辑，减少了不必要的状态变量。
     - 通过引入新的属性如 `max_map_size` 和 `map_non_cacheable`，进一步明确了内存映射的逻辑。
   - 参与者们还讨论了如何处理特定的边缘情况，以确保重构后的代码在功能上与原有实现一致。

总的来说，这一系列补丁和讨论旨在提升 KVM arm64 代码的质量，使其更加模块化和易于维护，同时确保在功能上不出现回归。

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
22. **[03-27 11:36]** [PATCH v2 21/30] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
23. **[03-27 11:36]** [PATCH v2 22/30] KVM: arm64: Move VMA-related information to kvm_s2_fault_vma_info
   - 发件人: Marc Zyngier <maz@kernel.org>
24. **[03-27 11:36]** [PATCH v2 23/30] KVM: arm64: Kill logging_active from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
25. **[03-27 11:36]** [PATCH v2 24/30] KVM: arm64: Restrict the scope of the 'writable' attribute
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[03-27 11:36]** [PATCH v2 25/30] KVM: arm64: Move kvm_s2_fault.{pfn,page} to kvm_s2_vma_info
   - 发件人: Marc Zyngier <maz@kernel.org>
27. **[03-27 11:36]** [PATCH v2 26/30] KVM: arm64: Replace force_pte with a max_map_size attribute
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[03-27 11:36]** [PATCH v2 27/30] KVM: arm64: Move device mapping management into kvm_s2_fault_pin_pfn()
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[03-27 11:36]** [PATCH v2 28/30] KVM: arm64: Directly expose mapping prot and kill kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
30. **[03-27 11:36]** [PATCH v2 29/30] KVM: arm64: Simplify integration of adjust_nested_*_perms()
   - 发件人: Marc Zyngier <maz@kernel.org>
31. **[03-27 11:36]** [PATCH v2 30/30] KVM: arm64: Convert gmem_abort() to struct kvm_s2_fault_desc
   - 发件人: Marc Zyngier <maz@kernel.org>
32. **[03-27 14:49]** Re: [PATCH v2 21/30] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Marc Zyngier <maz@kernel.org>
33. **[03-29 14:41]** Re: [PATCH v2 21/30] KVM: arm64: Kill topup_memcache from kvm_s2_fault
   - 发件人: Fuad Tabba <tabba@google.com>

---

### Thread 4: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 21 | **👥 参与者**: 5 | **📅 开始时间**: Wed, 18 Mar 2026 15:53:24 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 Arm Confidential Compute Architecture (CCA) 的 KVM 支持的补丁（PATCH v13 00/48）。该补丁系列旨在实现通过 KVM 运行受保护的虚拟机，涉及到 RMM（Realm Management Monitor）v2.0 的重大变更，包括页面大小配置和基于范围的 API。

在历史讨论中，Steven Price 提出了补丁的初步版本，并讨论了 RMM v2.0 的新特性和与 v1.0 的兼容性问题。参与者们对补丁的具体实现进行了技术细节的探讨，包括如何处理虚拟 CPU 的状态和内存分配等。

本周的新讨论中，Suzuki K Poulose 和其他参与者对补丁进行了进一步的审查和反馈，特别是关于如何标记代码中可能会变动的部分以便于审查。Gavin Shan 提出了在使用 QEMU 时遇到的 RMM 初始化问题，并询问了与 TF-A 兼容性相关的具体实现细节。Suzuki 也确认了正在进行的 QEMU 和 TF-RMM 支持工作，并表示将继续关注相关问题的解决。

总的来说，讨论集中在补丁的实现细节、兼容性问题以及如何优化代码审查流程上，参与者们积极交流以推动补丁的完善和实施。

#### 📝 邮件列表

1. **[03-18 15:53]** [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
2. **[03-18 15:53]** [PATCH v13 05/48] arm64: RMI: Temporarily add SMCs from RMM v1.0 spec
   - 发件人: Steven Price <steven.price@arm.com>
3. **[03-18 15:53]** [PATCH v13 17/48] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
4. **[03-18 15:53]** [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
5. **[03-18 15:53]** [PATCH v13 24/48] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
6. **[03-19 17:02]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
7. **[03-20 14:08]** Re: [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[03-20 16:32]** Re: [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
9. **[03-20 16:45]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Steven Price <steven.price@arm.com>
10. **[03-21 13:21]** Re: [PATCH v13 05/48] arm64: RMI: Temporarily add SMCs from RMM v1.0 spec
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[03-23 10:03]** Re: [PATCH v13 20/48] arm64: RMI: Handle realm enter/exit
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[03-23 10:30]** Re: [PATCH v13 05/48] arm64: RMI: Temporarily add SMCs from RMM v1.0
 spec
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[03-23 11:32]** Re: [PATCH v13 24/48] arm64: RMI: Allow populating initial contents
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
14. **[03-23 11:56]** Re: [PATCH v13 17/48] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[03-25 14:07]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Gavin Shan <gshan@redhat.com>
16. **[03-25 16:37]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Gavin Shan <gshan@redhat.com>
17. **[03-25 10:16]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[03-25 10:19]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[03-25 11:32]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[03-26 10:48]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Gavin Shan <gshan@redhat.com>
21. **[03-26 11:22]** Re: [PATCH v13 00/48] arm64: Support for Arm CCA in KVM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 5: [PATCH v11 00/16] Direct Map Removal Support for guest_memfd

**📧 邮件数**: 19 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 17 Mar 2026 14:10:32 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对虚拟机内存的直接映射移除支持的补丁（PATCH v11 00/16），主要目的是通过从主机内核的直接映射中解除虚拟机来缓解Spectre类的安全问题。补丁的核心在于引入了新的辅助函数，以便在处理guest_memfd时能够有效地移除直接映射。

在历史讨论中，主要内容包括多个补丁的提交，涉及到内存设置函数的改进、直接映射的辅助函数的添加，以及对现有代码的优化。特别是，补丁中引入了`GUEST_MEMFD_FLAG_NO_DIRECT_MAP`标志，以确保在创建guest_memfd时可以从直接映射中移除相应的内存区域。

在本周的新讨论中，参与者对补丁进行了细致的审查和讨论。David Hildenbrand提出了一些建议，如在某些补丁中添加更多描述、考虑是否需要检查hugetlb映射等。此外，Ackerley Tng也对补丁进行了审查，并提出了一些潜在的改进意见。整体来看，讨论集中在补丁的细节和潜在的优化上，参与者们对补丁的方向表示认可，并提出了进一步的建议和问题以供改进。

#### 📝 邮件列表

1. **[03-17 14:10]** [PATCH v11 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
2. **[03-17 14:10]** [PATCH v11 01/16] set_memory: set_direct_map_* to take address
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
3. **[03-17 14:10]** [PATCH v11 02/16] set_memory: add folio_{zap,restore}_direct_map
 helpers
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
4. **[03-17 14:11]** [PATCH v11 03/16] mm/secretmem: make use of
 folio_{zap,restore}_direct_map
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
5. **[03-17 14:11]** [PATCH v11 04/16] mm/gup: drop secretmem optimization from
 gup_fast_folio_allowed
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
6. **[03-17 14:11]** [PATCH v11 05/16] mm/gup: drop local variable in
 gup_fast_folio_allowed
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
7. **[03-17 14:12]** [PATCH v11 10/16] KVM: guest_memfd: Add flag to remove from direct
 map
   - 发件人: Kalyazin, Nikita <kalyazin@amazon.co.uk>
8. **[03-23 18:44]** Re: [PATCH v11 01/16] set_memory: set_direct_map_* to take address
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
9. **[03-23 18:51]** Re: [PATCH v11 02/16] set_memory: add folio_{zap,restore}_direct_map
 helpers
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
10. **[03-23 18:53]** Re: [PATCH v11 03/16] mm/secretmem: make use of
 folio_{zap,restore}_direct_map
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
11. **[03-23 18:55]** Re: [PATCH v11 05/16] mm/gup: drop local variable in
 gup_fast_folio_allowed
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
12. **[03-23 11:00]** Re: [PATCH v11 01/16] set_memory: set_direct_map_* to take address
   - 发件人: Ackerley Tng <ackerleytng@google.com>
13. **[03-23 19:05]** Re: [PATCH v11 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
14. **[03-23 19:31]** Re: [PATCH v11 04/16] mm/gup: drop secretmem optimization from
 gup_fast_folio_allowed
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
15. **[03-23 11:43]** Re: [PATCH v11 02/16] set_memory: add folio_{zap,restore}_direct_map helpers
   - 发件人: Ackerley Tng <ackerleytng@google.com>
16. **[03-23 11:46]** Re: [PATCH v11 03/16] mm/secretmem: make use of folio_{zap,restore}_direct_map
   - 发件人: Ackerley Tng <ackerleytng@google.com>
17. **[03-23 13:22]** Re: [PATCH v11 05/16] mm/gup: drop local variable in gup_fast_folio_allowed
   - 发件人: Ackerley Tng <ackerleytng@google.com>
18. **[03-23 13:47]** Re: [PATCH v11 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Ackerley Tng <ackerleytng@google.com>
19. **[03-23 14:15]** Re: [PATCH v11 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

### Thread 6: [PATCH v3 0/5] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)

**📧 邮件数**: 18 | **👥 参与者**: 5 | **📅 开始时间**: Mon, 23 Mar 2026 16:24:00 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 Arm C1-Pro 处理器的错误修复补丁（CVE-2026-0995），主要是为了解决该处理器在处理 SME（可扩展矩阵扩展）内存访问时的早期 DVMSync 确认问题。补丁的核心内容是通过在 TLB（转换后备页表）失效后对所有受影响的 CPU 执行 DSB（数据同步屏障）来确保 SME 访问的完成。

在历史讨论中，补丁的版本更新了配置选项的命名，并将 smp_processor_id() 函数嵌入到 sme_{set,clear}_active() 函数中，以确保在 TLB 失效后正确处理 SME 访问。补丁还更新了文档以反映这些更改。

本周的新讨论中，参与者们对补丁的各个部分进行了审查和确认，包括对 KVM（内核虚拟机）中 SME dvmsync 错误的处理。Catalin Marinas 提到补丁的整体结构良好，并获得了 Mark Rutland 和 Vincent Donnefort 的认可。James Morse 提出了在 EL3 中处理该错误的建议，以避免 EL2 和 EL1 共享安全状态带来的问题。

总体而言，本周的讨论集中在补丁的细节审查和确认上，推动了该补丁向合并的进展。

#### 📝 邮件列表

1. **[03-23 16:24]** [PATCH v3 0/5] arm64: Work around C1-Pro erratum 4193714 (CVE-2026-0995)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[03-23 16:24]** [PATCH v3 1/5] arm64: tlb: Introduce __tlbi_sync_s1ish_{kernel,batch}() for TLB maintenance
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[03-23 16:24]** [PATCH v3 2/5] arm64: tlb: Pass the corresponding mm to __tlbi_sync_s1ish()
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
4. **[03-23 16:24]** [PATCH v3 3/5] arm64: cputype: Add C1-Pro definitions
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-23 16:24]** [PATCH v3 4/5] arm64: errata: Work around early CME DVMSync acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
6. **[03-23 16:24]** [PATCH v3 5/5] KVM: arm64: Add SMC hook for SME dvmsync erratum
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
7. **[03-23 17:53]** Re: [PATCH v3 0/5] arm64: Work around C1-Pro erratum 4193714
 (CVE-2026-0995)
   - 发件人: Mark Rutland <mark.rutland@arm.com>
8. **[03-24 10:14]** Re: [PATCH v3 5/5] KVM: arm64: Add SMC hook for SME dvmsync erratum
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[03-24 12:56]** Re: [PATCH v3 5/5] KVM: arm64: Add SMC hook for SME dvmsync erratum
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
10. **[03-25 18:05]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[03-25 18:20]** [PATCH] arm64/kvm: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
12. **[03-26 14:31]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[03-27 15:35]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
14. **[03-27 15:40]** Re: [PATCH] arm64/kvm: Enable eager hugepage splitting if HDBSS is
 available
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
15. **[03-27 14:37]** Re: [PATCH] arm64/kvm: Enable eager hugepage splitting if HDBSS is available
   - 发件人: Leonardo Bras <leo.bras@arm.com>
16. **[03-27 15:00]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF events
   - 发件人: Leonardo Bras <leo.bras@arm.com>
17. **[03-27 19:15]** Re: [PATCH v3 4/5] arm64: errata: Work around early CME DVMSync
 acknowledgement
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
18. **[03-28 14:05]** Re: [PATCH v3 4/5] KVM: arm64: Enable HDBSS support and handle HDBSSF
 events
   - 发件人: Tian Zheng <zhengtian10@huawei.com>

---

### Thread 7: [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes

**📧 邮件数**: 16 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 26 Mar 2026 15:35:15 +0000

#### 🤖 AI 总结

本邮件线程讨论了 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-v5 相关修复的第一批补丁。Marc Zyngier 提出了 15 个补丁，旨在解决在合并 vgic-v5 补丁时发现的一些回归问题和潜在的错误。

历史讨论中未提供具体的补丁背景，但本周的新讨论中，Marc 提到合并初始补丁时遇到了一些回归问题，部分问题是由 AI 工具发现的，虽然并非所有反馈都有效，但确实有助于识别重要问题。Marc 表示他在紧急修复这些问题，并考虑是将这些补丁添加到当前系列中，还是等待下一个周期。

本周的进展包括多个补丁的具体内容，例如：
1. 修复了在最终化时不应重置 cpuif 和 redistributor 地址的问题。
2. 确保所有 vCPU 都能正确初始化 NV 寄存器。
3. 修正了 ID_AA64PFR2_EL1 的可写掩码。
4. 解决了 GICv5 PPI 状态最终化时未加锁的问题，以防止竞争条件。
5. 其他补丁则涉及对寄存器字段引用的修正、定时器状态的评估等。

这些补丁的目标是提高 KVM 在 arm64 架构下的稳定性和性能，确保 vgic-v5 的正确实现。

#### 📝 邮件列表

1. **[03-26 15:35]** [PATCH 00/15] KVM: arm64: First batch of vgic-v5 related fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-26 15:35]** [PATCH 01/15] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-26 15:35]** [PATCH 02/15] KVM: arm64: Don't skip per-vcpu NV initialisation
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-26 15:35]** [PATCH 03/15] arm64: Fix field references for ICH_PPI_DVIR[01]_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-26 15:35]** [PATCH 04/15] KVM: arm64: Fix writeable mask for ID_AA64PFR2_EL1
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-26 15:35]** [PATCH 05/15] KVM: arm64: Account for RESx bits in __compute_fgt()
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-26 15:35]** [PATCH 06/15] KVM: arm64: vgic-v5: Hold config_lock while finalizing GICv5 PPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-26 15:35]** [PATCH 07/15] KVM: arm64: vgic-v5: Transfer edge pending state to ICH_PPI_PENDRx_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-26 15:35]** [PATCH 08/15] KVM: arm64: vgic-v5: Cast vgic_apr to u32 to avoid undefined behaviours
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[03-26 15:35]** [PATCH 09/15] KVM: arm64: vgic-v5: align priority comparison with other GICs
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[03-26 15:35]** [PATCH 10/15] KVM: arm64: vgic-v5: Correctly set dist->ready once initialised
   - 发件人: Marc Zyngier <maz@kernel.org>
12. **[03-26 15:35]** [PATCH 11/15] KVM: arm64: Kill arch_timer_context::direct field
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[03-26 15:35]** [PATCH 12/15] KVM: arm64: Remove evaluation of timer state in kvm_cpu_has_pending_timer()
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[03-26 15:35]** [PATCH 13/15] KVM: arm64: Move GICv5 timer PPI validation into timer_irqs_are_valid()
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[03-26 15:35]** [PATCH 14/15] KVM: arm64: Correctly plumb ID_AA64PFR2_EL1 into pkvm idreg handling
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[03-26 15:35]** [PATCH 15/15] KVM: arm64: Don't advertises GICv3 in ID_PFR1_EL1 if AArch32 isn't supported
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 8: [PATCH v2] KVM: arm64: Prevent the host from using an smc with imm16
 != 0

**📧 邮件数**: 13 | **👥 参与者**: 6 | **📅 开始时间**: Wed, 25 Mar 2026 11:31:38 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM (Kernel-based Virtual Machine) 的补丁，旨在防止主机在执行 SMC (Secure Monitor Call) 指令时使用非零的 16 位立即数。补丁的核心内容是通过解码 ESR_EL2 中的 ISS 值，强制要求主机内核在 pKVM 环境下使用立即数 0，并在遇到非零立即数时返回不支持的错误代码。

在历史讨论中，补丁的初版提议在遇到非零立即数时注入 UNDEF 指令，但在版本更新中，开发者决定直接返回错误代码 SMCCC_RET_NOT_SUPPORTED，以简化处理逻辑。此外，补丁的标题也进行了相应更新。

本周的新讨论中，参与者们围绕补丁的实现细节展开了热烈的讨论。Sebastian Ene 提出了将错误处理逻辑移入 `handle_host_smc()` 函数的建议，以便更好地集中处理 SMC 指令。Marc Zyngier 和 Will Deacon 进一步探讨了处理非零立即数的安全性，强调了遵循 SMCCC 规范的重要性，并一致认为拒绝非零立即数是最安全的选择。最终，Sebastian 表示将根据讨论结果更新补丁内容，确保符合规范。

#### 📝 邮件列表

1. **[03-25 11:31]** [PATCH v2] KVM: arm64: Prevent the host from using an smc with imm16
 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-25 11:35]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-25 11:41]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[03-25 11:46]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with imm16 != 0
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-25 11:58]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with imm16 != 0
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-25 12:12]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-25 12:16]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Fuad Tabba <tabba@google.com>
8. **[03-25 13:15]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[03-25 13:16]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
10. **[03-25 13:28]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Mark Rutland <mark.rutland@arm.com>
11. **[03-25 13:33]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Mark Rutland <mark.rutland@arm.com>
12. **[03-25 14:33]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with imm16 != 0
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[03-25 16:02]** Re: [PATCH v2] KVM: arm64: Prevent the host from using an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 9: [PATCH 0/3] KVM: arm64: selftests: Basic nested guest support

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 25 Mar 2026 00:36:17 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的嵌套虚拟化支持的自测功能的补丁系列。该系列补丁包含三个主要部分：

1. **原始补丁内容**：补丁系列的目标是为 KVM 的自测框架添加基本的嵌套虚拟化支持。第一个补丁引入了一些库函数，用户空间可以通过这些函数设置状态以运行嵌套的 L2 虚拟机。具体功能包括设置 L2 堆栈、配置虚拟 EL2 寄存器、指定 L2 执行的函数指针等。

2. **之前讨论要点**：在之前的讨论中，参与者对补丁的设计提出了一些建议，包括使用符号常量而非硬编码值、确保 L2 上下文的保存与恢复等。Marc Zyngier 强调了在不同硬件配置下的兼容性问题，并建议开发一个独立于页面、IA 和 OA 大小的页表生成器。

3. **本周的新讨论与进展**：本周的讨论集中在补丁的具体实现细节上，Wei-Lin Chang 对补丁进行了多次更新，回应了关于堆栈大小、上下文保存和页表生成的建议。参与者 Itaru Kitayama 和 Marc Zyngier 对补丁的设计提出了进一步的改进建议，强调了在不同平台上保持兼容性的重要性。Wei-Lin Chang 表示将考虑这些建议，并在下一版本中进行调整。

总体而言，本周的讨论推动了补丁的进一步完善，确保了嵌套虚拟化功能的可靠性和兼容性。

#### 📝 邮件列表

1. **[03-25 00:36]** [PATCH 0/3] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-25 00:36]** [PATCH 1/3] KVM: arm64: selftests: Add library functions for NV
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[03-25 00:36]** [PATCH 2/3] KVM: arm64: sefltests: Add basic NV selftest
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[03-25 00:36]** [PATCH 3/3] KVM: arm64: selftests: Enable stage-2 in NV preparation functions
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[03-25 15:23]** Re: [PATCH 3/3] KVM: arm64: selftests: Enable stage-2 in NV
 preparation functions
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
6. **[03-25 17:00]** Re: [PATCH 0/3] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
7. **[03-25 09:03]** Re: [PATCH 1/3] KVM: arm64: selftests: Add library functions for NV
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[03-25 09:18]** Re: [PATCH 3/3] KVM: arm64: selftests: Enable stage-2 in NV preparation functions
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-26 14:28]** Re: [PATCH 1/3] KVM: arm64: selftests: Add library functions for NV
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
10. **[03-26 21:16]** Re: [PATCH 3/3] KVM: arm64: selftests: Enable stage-2 in NV
 preparation functions
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
11. **[03-26 21:34]** Re: [PATCH 3/3] KVM: arm64: selftests: Enable stage-2 in NV
 preparation functions
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 10: [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support

**📧 邮件数**: 11 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 19 Mar 2026 15:49:42 +0000

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构中引入 vGIC-v5（虚拟通用中断控制器 v5）及其对 PPI（私有中断）的支持。历史讨论中，Sascha Bischoff 提出了一个补丁系列（PATCH v7），旨在实现 vGIC-v5 的初步功能，当前版本仅支持 PPI，未来将扩展支持 SPI（共享中断）和 LPI（本地中断）等。

在之前的讨论中，补丁的主要变化包括对 GICv5 主机的架构定时器代码进行了调整，并引入了对 ID_AA64PFR2_EL1.GCIE 字段的清理功能，以确保在创建非 GICv5 GIC 时该字段被正确处理。

本周的新讨论中，Mark Brown 报告了在多个平台（包括物理设备）上出现的回归问题，特别是在使用 GICv3 的情况下，导致自测失败。Marc Zyngier 和其他参与者讨论了可能的解决方案，并确认了在 TX2 平台上的测试结果。最终，Mark 提出了一个修复建议，并得到了确认，表明该修复在 TX2 上有效。

总结来说，本周的讨论集中在解决补丁引入的回归问题上，参与者们积极探讨并测试了不同的解决方案，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[03-19 15:49]** [PATCH v7 00/41] KVM: arm64: Introduce vGIC-v5 with PPI support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[03-19 15:52]** [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[03-23 13:37]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[03-23 13:50]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-23 14:08]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Mark Brown <broonie@kernel.org>
6. **[03-23 17:59]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-24 12:47]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[03-24 14:48]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[03-24 14:53]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Mark Brown <broonie@kernel.org>
10. **[03-24 15:25]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize ID_AA64PFR2_EL1.GCIE
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[03-24 18:16]** Re: [PATCH v7 12/41] KVM: arm64: gic-v5: Sanitize
 ID_AA64PFR2_EL1.GCIE
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 11: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc with
 imm16 != 0

**📧 邮件数**: 10 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 24 Mar 2026 13:57:28 +0000

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为在主机执行带有非零立即数的 SMC（Secure Monitor Call）时注入未定义指令（UNDEF）。补丁的目的是确保在 pKVM 环境中，主机内核只能使用立即数为 0 的 SMC，以避免不符合 ARM 服务调用约定（SMCCC）的软件行为。

在历史讨论中，补丁的提出者 Sebastian Ene 指出，当前的 pKVM 处理程序忽略了 SMC 指令的立即数，这可能导致依赖于实现定义行为的软件出现问题。因此，他建议通过解码 ESR_EL2 中的 ISS 值来强制执行这一限制，并在遇到非零立即数时注入未定义指令异常。

在本周的新讨论中，参与者们对补丁进行了深入的技术讨论。Vincent Donnefort 提出了一些代码优化建议，建议使用现有的掩码函数来提高代码可读性。Marc Zyngier 则指出，SMC 不应简单地生成 UNDEF，而是应返回错误代码，Sebastian 随后同意这一观点，并表示将更新补丁以反映这一更改。整体上，本周的讨论集中在补丁的实现细节和代码优化上，推动了补丁的进一步完善。

#### 📝 邮件列表

1. **[03-24 13:57]** [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc with
 imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-24 14:06]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-24 14:09]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[03-24 14:18]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[03-24 14:41]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[03-24 14:43]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc with imm16 != 0
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[03-24 15:04]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[03-24 15:05]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[03-24 15:13]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Fuad Tabba <tabba@google.com>
10. **[03-25 10:01]** Re: [PATCH] KVM: arm64: Inject UNDEF when host is executing an smc
 with imm16 != 0
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

### Thread 12: [PATCH v3 11/36] KVM: arm64: Introduce __pkvm_host_donate_guest()

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 20 Mar 2026 12:38:07 +0000

#### 🤖 AI 总结

本邮件线程讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下引入的补丁，特别是 `__pkvm_host_donate_guest()` 函数的实现。

**1. 原始补丁内容：**  
补丁 `PATCH v3 11/36` 旨在引入 `__pkvm_host_donate_guest()` 函数，以支持在 KVM 环境中更好地管理来宾虚拟机的资源捐赠。

**2. 之前讨论要点：**  
在历史讨论中，Marc Zyngier 和 Will Deacon 讨论了与 `KVM_MAX_OWNER_ID` 和 `PKVM_ID_GUEST` 相关的设置，提出了是否应该将一个定义基于另一个定义的建议。此外，关于 PKVM_ID_FFA 的使用情况也进行了探讨，Marc 表达了对增加配置选项的反对意见，认为这会增加复杂性。

**3. 本周的新讨论与进展：**  
本周的讨论中，Will Deacon 对补丁进行了进一步的澄清，确认了 `KVM_MAX_OWNER_ID` 的调整是为了避免拒绝 `PKVM_ID_GUEST`。他还提到将移除未使用的 `PKVM_ID_FFA`。在处理故障页面回收的讨论中，Will 提出了一种优化方案，通过在主机 KVM 结构中设置标志来减少对每个故障的页面表遍历，从而提高性能。此外，关于允许用户空间创建受保护虚拟机的讨论中，Will 表达了对减少配置选项的支持，认为过多的选项会导致不必要的复杂性。整体来看，本周的讨论集中在补丁的细节优化和配置简化上。

#### 📝 邮件列表

1. **[03-20 12:38]** Re: [PATCH v3 11/36] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-20 13:22]** Re: [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected VMs when pKVM is enabled
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-20 16:20]** Re: [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-20 16:35]** Re: [PATCH v3 26/36] KVM: arm64: Return -EFAULT from VCPU_RUN on access to a poisoned pte
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-21 09:39]** Re: [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in spurious fault handler
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-23 14:55]** Re: [PATCH v3 11/36] KVM: arm64: Introduce __pkvm_host_donate_guest()
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-23 14:58]** Re: [PATCH v3 25/36] KVM: arm64: Reclaim faulting page from pKVM in
 spurious fault handler
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-23 14:58]** Re: [PATCH v3 26/36] KVM: arm64: Return -EFAULT from VCPU_RUN on
 access to a poisoned pte
   - 发件人: Will Deacon <will@kernel.org>
9. **[03-23 15:00]** Re: [PATCH v3 30/36] KVM: arm64: Allow userspace to create protected
 VMs when pKVM is enabled
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 13: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  9 Mar 2026 15:56:24 +0530

#### 🤖 AI 总结

本邮件线程讨论的主题是关于在共享缓冲区中强制执行主机页面大小对齐的补丁（PATCH v3 2/3），由Aneesh Kumar K.V提出。该补丁旨在解决在私有内存虚拟机中，来宾内核在与虚拟机监控器（hypervisor）共享缓冲区时，必须遵循主机页面大小对齐的限制。历史讨论中提到，当前的实现可能导致内存属性的不匹配，尤其是在非安全主机上。

在本周的新讨论中，Aneesh Kumar K.V回应了先前的构建错误，并表示将通过修改相关头文件来解决这些问题。此外，Will Deacon提交了关于KVM的多个补丁，主要集中在处理nVHE（非虚拟化高效）世界切换时的SPE（统计性能扩展）和TRBE（跟踪缓冲单元）的问题。他提出的补丁确保在切换到来宾上下文时，正确禁用这些功能，以防止潜在的内存访问错误和数据损坏。

总体来看，本周的讨论主要集中在补丁的修正和优化上，以确保在虚拟化环境中更好地管理资源和防止错误。

#### 📝 邮件列表

1. **[03-09 15:56]** [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[03-09 23:55]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: kernel test robot <lkp@intel.com>
3. **[03-23 19:22]** Re: [PATCH v3 2/3] swiotlb: dma: its: Enforce host page-size
 alignment for shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
4. **[03-26 14:12]** [PATCH v3 0/3] KVM: arm64: Fix SPE and TRBE nVHE world switch
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-26 14:12]** [PATCH v3 1/3] KVM: arm64: Disable TRBE Trace Buffer Unit when running in guest context
   - 发件人: Will Deacon <will@kernel.org>
6. **[03-26 14:12]** [PATCH v3 2/3] KVM: arm64: Disable SPE Profiling Buffer when running in guest context
   - 发件人: Will Deacon <will@kernel.org>
7. **[03-26 14:12]** [PATCH v3 3/3] KVM: arm64: Don't pass host_debug_state to BRBE world-switch routines
   - 发件人: Will Deacon <will@kernel.org>
8. **[03-26 18:21]** Re: [PATCH v3 3/3] KVM: arm64: Don't pass host_debug_state to BRBE
 world-switch routines
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 14: [PATCH kvmtool v7 0/6] arm64: Nested virtualization support

**📧 邮件数**: 7 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 23 Mar 2026 17:47:11 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 架构的嵌套虚拟化支持的第七版补丁（PATCH kvmtool v7 0/6）。该补丁系列旨在解决之前报告的字节序问题，并为 KVM 工具提供相应的支持。

在历史讨论中，补丁的主要内容包括引入了新的命令行选项“--nested”，允许 VCPU 在 EL2 模式下启动，同时增加了 VGIC 支持以设置维护 IRQ。补丁还包括对架构计时器偏移的设置、非 VHE 客户端的启用、虚拟 EL2 定时器 IRQ 的广告，以及在检测客户机字节序时考虑正确的系统寄存器。

本周的新讨论中，Andre Przywara 提出了补丁的具体实现，包括：
1. **补丁 1**：添加了“--nested”选项，允许在 EL2 启动客户机。
2. **补丁 2**：支持设置维护 IRQ，确保与 SBSA 推荐一致。
3. **补丁 3**：添加了计数器偏移控制选项“--counter-offset”。
4. **补丁 4**：引入了“--e2h0”选项以支持不使用 VHE 的旧版客户机。
5. **补丁 5**：生成 HYP 定时器中断说明，适应嵌套虚拟化的需求。
6. **补丁 6**：处理在 EL2 客户机运行时的 virtio 字节序重置问题。

这些补丁经过测试并得到了参与者的审查，标志着嵌套虚拟化支持的进一步完善。

#### 📝 邮件列表

1. **[03-23 17:47]** [PATCH kvmtool v7 0/6] arm64: Nested virtualization support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
2. **[03-23 17:47]** [PATCH kvmtool v7 1/6] arm64: Initial nested virt support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
3. **[03-23 17:47]** [PATCH kvmtool v7 2/6] arm64: nested: Add support for setting maintenance IRQ
   - 发件人: Andre Przywara <andre.przywara@arm.com>
4. **[03-23 17:47]** [PATCH kvmtool v7 3/6] arm64: Add counter offset control
   - 发件人: Andre Przywara <andre.przywara@arm.com>
5. **[03-23 17:47]** [PATCH kvmtool v7 4/6] arm64: Add FEAT_E2H0 support
   - 发件人: Andre Przywara <andre.przywara@arm.com>
6. **[03-23 17:47]** [PATCH kvmtool v7 5/6] arm64: Generate HYP timer interrupt specifiers
   - 发件人: Andre Przywara <andre.przywara@arm.com>
7. **[03-23 17:47]** [PATCH kvmtool v7 6/6] arm64: Handle virtio endianness reset when running nested
   - 发件人: Andre Przywara <andre.przywara@arm.com>

---

### Thread 15: [PATCH v4 0/3] KVM: arm64: Fix SPE and TRBE nVHE world switch

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 27 Mar 2026 13:00:43 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 nVHE（Non-Virtual Hypervisor Extension）世界切换中，修复 SPE（Statistical Profiling Extension）和 TRBE（Trace Buffer Extension）相关的问题。

**原始 patch/问题的内容**：
本次讨论的补丁（PATCH v4 0/3）旨在修复在虚拟机上下文中运行时，SPE 和 TRBE 的状态管理问题，确保在切换到来宾上下文时，相关的追踪和分析功能被正确禁用，以防止出现数据损坏和硬件锁死等问题。

**之前讨论要点**：
在之前的版本中，开发者发现 TRBE 和 SPE 的状态在切换过程中未能正确清零，导致可能的错误和不稳定性。开发者们讨论了如何确保在切换到来宾上下文时，相关寄存器被正确处理。

**本周的新讨论、进展或结论**：
本周的讨论中，Will Deacon 提交了 v4 版本的补丁，主要包括：
1. 禁用在来宾上下文中运行的 TRBE 追踪缓冲单元。
2. 禁用在来宾上下文中运行的 SPE 分析缓冲区。
3. 统一 BRBE 相关的状态处理，确保一致性。

补丁已获得多位开发者的测试和审核，Marc Zyngier 表示已将其应用到下一个版本中，标志着该问题的修复工作取得了实质性进展。

#### 📝 邮件列表

1. **[03-27 13:00]** [PATCH v4 0/3] KVM: arm64: Fix SPE and TRBE nVHE world switch
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-27 13:00]** [PATCH v4 1/3] KVM: arm64: Disable TRBE Trace Buffer Unit when running in guest context
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-27 13:00]** [PATCH v4 2/3] KVM: arm64: Disable SPE Profiling Buffer when running in guest context
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-27 13:00]** [PATCH v4 3/3] KVM: arm64: Don't pass host_debug_state to BRBE world-switch routines
   - 发件人: Will Deacon <will@kernel.org>
5. **[03-27 13:23]** Re: [PATCH v4 3/3] KVM: arm64: Don't pass host_debug_state to BRBE
 world-switch routines
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[03-28 17:13]** Re: [PATCH v4 0/3] KVM: arm64: Fix SPE and TRBE nVHE world switch
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 16: [PATCH 0/2] KVM: arm64: Tentative fixes for page-table lifetime issues

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 27 Mar 2026 19:27:55 +0000

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的页表生命周期问题的修复。Will Deacon 提出了两个补丁，旨在解决在创建虚拟机时可能出现的页表泄漏和悬空指针问题。

第一个补丁（PATCH 1/2）解决了在 `kvm_init_stage2_mmu()` 函数中，如果分配失败，导致的 `mmu->pgt` 悬空指针问题。补丁确保在返回错误时清除该指针，以避免潜在的双重释放错误。

第二个补丁（PATCH 2/2）则针对 `kvm_arch_destroy_vm()` 函数，确保在虚拟机创建失败时，显式销毁分配的阶段二页表，避免依赖 MMU 通知器的释放机制，从而防止内存泄漏。

本周的讨论中，Wei-Lin Chang 提出了对阶段二 MMU 清理过程的小幅重构，主要包括函数重命名和代码重构，以提高代码可读性和维护性。他将 `kvm_free_stage2_pgd()` 重命名为 `kvm_free_stage2()`，以更准确地反映其功能，并对 MMU 的反初始化函数进行了调整，使其能够同时处理标准和嵌套的 MMU。

总体来看，本周的讨论集中在对页表管理的清理和修复上，确保 KVM 在 arm64 架构下的稳定性和内存管理的有效性。

#### 📝 邮件列表

1. **[03-27 19:27]** [PATCH 0/2] KVM: arm64: Tentative fixes for page-table lifetime issues
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-27 19:27]** [PATCH 1/2] KVM: arm64: Don't leave mmu->pgt dangling on kvm_init_stage2_mmu() error
   - 发件人: Will Deacon <will@kernel.org>
3. **[03-27 19:27]** [PATCH 2/2] KVM: arm64: Destroy stage-2 page-table in kvm_arch_destroy_vm()
   - 发件人: Will Deacon <will@kernel.org>
4. **[03-28 14:54]** [PATCH 0/2] KVM: arm64: Small cleanups for stage-2 mmu teardown
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[03-28 14:54]** [PATCH 1/2] KVM: arm64: Rename kvm_free_stage2_pgd()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[03-28 14:54]** [PATCH 2/2] KVM: arm64: Refactor stage2 mmu tear down functions
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 17: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 24 Mar 2026 15:08:11 +0000

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned”，主要涉及对 KVM 在 arm64 架构下的性能监控单元（PMU）版本的处理。

1. **原始 patch/问题的内容**：该补丁系列包括三个部分，主要目的是将 PMUVer 和性能监控相关的功能设置为无符号类型，以提高代码的可读性和稳定性。补丁还涉及在虚拟机上下文中禁用某些性能分析功能，以避免潜在的冲突。

2. **之前的讨论要点**：在历史讨论中，参与者们对补丁的必要性和实现方式进行了探讨，强调了在虚拟化环境中处理性能监控的重要性。补丁的设计旨在确保在不同的上下文中，性能监控功能的正确性和安全性。

3. **本周的新讨论、进展或结论**：本周的讨论中，Will Deacon 表示已将补丁应用到他的开发分支，并感谢参与者的贡献。Alexandru Elisei 和 Fuad Tabba 对补丁进行了测试并给予了积极的反馈，确认了其在实际应用中的有效性。Fuad 还提出了代码简化的建议，Will 计划根据反馈进行补丁的进一步优化，准备发布 v3 版本。

整体来看，本周的讨论显示出对补丁的广泛支持和积极的测试反馈，为后续的代码改进奠定了基础。

#### 📝 邮件列表

1. **[03-24 15:08]** Re: [PATCH v2 0/3] KVM: arm64: Read PMUVer as unsigned
   - 发件人: Will Deacon <will@kernel.org>
2. **[03-25 16:34]** Re: [PATCH v2 2/3] KVM: arm64: Disable SPE Profiling Buffer when
 running in guest context
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[03-25 19:27]** Re: [PATCH v2 1/3] KVM: arm64: Disable TRBE Trace Buffer Unit when
 running in guest context
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[03-25 19:28]** Re: [PATCH v2 2/3] KVM: arm64: Disable SPE Profiling Buffer when
 running in guest context
   - 发件人: Fuad Tabba <tabba@google.com>
5. **[03-25 19:28]** Re: [PATCH v2 3/3] KVM: arm64: Don't pass host_debug_state to BRBE
 world-switch routines
   - 发件人: Fuad Tabba <tabba@google.com>
6. **[03-26 12:49]** Re: [PATCH v2 1/3] KVM: arm64: Disable TRBE Trace Buffer Unit when
 running in guest context
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 18: [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Sat, 21 Mar 2026 21:24:14 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 PSCI（Power State Coordination Interface）中继的重构工作，共包含五个补丁。

**原始补丁内容**：
Marc Zyngier 提出了一个补丁系列，旨在对 PSCI 中继代码进行清理和重构，主要包括错误处理的移动、简化 CPU 启动时的 BTI（Branch Target Identification）处理，以及使用直接函数指针来替代布尔值，以提高代码的可读性。

**之前讨论要点**：
在历史讨论中，Fuad Tabba 对补丁中的一个小错误进行了修正，并给予了“审核通过”的反馈，表明补丁在某些方面得到了认可。

**本周的新讨论与进展**：
本周，Marc Zyngier 确认已将补丁应用到下一步开发中，并列出了所有补丁的提交记录。此外，Mostafa Saleh 提到他已在 pKVM（包括 nvhe 和 hvhe）上进行了测试，确认系统能够正常启动、关机和通过 sysfs 进行热插拔操作，进一步验证了补丁的有效性。整体来看，讨论进展顺利，补丁已成功推进至下一阶段。

#### 📝 邮件列表

1. **[03-21 21:24]** [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-21 21:24]** [PATCH 4/5] KVM: arm64: pkvm: Use direct function pointers for cpu_{on,resume}
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[03-22 15:49]** Re: [PATCH 4/5] KVM: arm64: pkvm: Use direct function pointers for cpu_{on,resume}
   - 发件人: Fuad Tabba <tabba@google.com>
4. **[03-23 08:43]** Re: [PATCH 4/5] KVM: arm64: pkvm: Use direct function pointers for cpu_{on,resume}
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[03-23 11:05]** Re: [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[03-23 12:33]** Re: [PATCH 0/5] KVM: arm64: pkvm; Rework aspects of the PSCI relay
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 19: [PATCH v17 0/8] support FEAT_LSUI

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 14 Mar 2026 17:51:25 +0000

#### 🤖 AI 总结

本邮件讨论的主题是支持 Arm 架构中的 FEAT_LSUI 特性，主要涉及对内核的补丁集（PATCH v17 0/8）。FEAT_LSUI 允许特权级别的加载/存储指令访问用户内存，而无需清除 PSTATE.PAN 位。该补丁集主要应用于 futex 原子操作等功能。

在历史讨论中，Yeoreum Yun 提出了该补丁集的背景，说明了其基于之前版本的改进，包括去除某些循环和修改注释等。补丁集的目标是增强对 FEAT_LSUI 的支持。

在本周的新讨论中，Catalin Marinas 确认已将补丁应用于 arm64 的开发分支，并决定放弃第 6 个补丁（禁用 SWP 模拟），因为当前的 FEAT_LSUI 支持仍然能够正常工作。尽管 Yeoreum Yun 表示支持 SWP 模拟的理由不足，但他同意放弃该补丁，并表示如果需要，可以重新提交以支持 SWP 模拟。此外，讨论中提到可能在禁用 PAN 的函数中添加警告，以确保严格的无 PAN 状态。

总体来看，本周的讨论集中在对补丁的应用和对 SWP 模拟支持的合理性上，推动了对 FEAT_LSUI 特性的进一步完善。

#### 📝 邮件列表

1. **[03-14 17:51]** [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[03-27 13:16]** Re: (subset) [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[03-27 13:56]** Re: (subset) [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[03-27 17:18]** Re: (subset) [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[03-27 19:21]** Re: (subset) [PATCH v17 0/8] support FEAT_LSUI
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 20: [PATCH v5 0/5] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 17 Mar 2026 20:10:33 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM 自测试中 arm64 架构的 `set_id_regs` 函数的改进，主要集中在提高诊断信息的准确性和处理特定寄存器的测试问题。

**原始 patch/问题的内容**：
Mark Brown 提出的补丁（PATCH v5 0/5）旨在改善在 aarch64 系统中执行寄存器读取和重置值保留测试时，缺乏详细结果报告的问题。原测试在出现错误时未能指明具体的寄存器，导致调试困难。

**之前讨论要点**：
在历史邮件中，Mark 还提出了一个补丁（PATCH v5 4/5），指出在 aarch64 系统上，32 位 ID 寄存器的值为未定义，因此在测试时应跳过这些寄存器的设置。这一处理方式可能导致后续测试出现误报，因为未记录这些寄存器的预期值。

**本周的新讨论、进展或结论**：
在本周的讨论中，Marc Zyngier 对跳过 32 位 ID 寄存器的做法表示反对，认为应修复 KVM 以确保在存在 NV 的情况下，这些寄存器的值为 RAZ（读取为零）。Mark 也确认了在实际使用中遇到的问题，并计划在 `kvm_finalize_sys_regs()` 中进行相应的更新，同时也会在 `set_id_regs` 中进行调整，以确保在运行时正确处理这些寄存器的值。整体来看，本周的讨论推动了对补丁的进一步完善和对问题的深入分析。

#### 📝 邮件列表

1. **[03-17 20:10]** [PATCH v5 0/5] KVM: selftests: arm64: Improve diagnostics from
 set_id_regs
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[03-17 20:10]** [PATCH v5 4/5] KVM: selftests: arm64: Skip all 32 bit IDs when
 set_id_regs is aarch64 only
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[03-24 16:47]** Re: [PATCH v5 4/5] KVM: selftests: arm64: Skip all 32 bit IDs when set_id_regs is aarch64 only
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[03-24 17:39]** Re: [PATCH v5 4/5] KVM: selftests: arm64: Skip all 32 bit IDs when
 set_id_regs is aarch64 only
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 21: [PATCH v2 01/11] arm64: Skip update of an idreg field affected
 by an override

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 19 Mar 2026 15:34:47 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 ARM64 架构的补丁（PATCH v2 01/11），该补丁旨在跳过对受覆盖影响的 idreg 字段的更新。补丁的核心问题在于，当主 CPU 的特征字段被覆盖时，如何处理次级 CPU 的特征值。

在历史讨论中，Marc Zyngier 提出了对 cpufeature 框架的困惑，讨论了在主 CPU 特征值被覆盖的情况下，次级 CPU 如何处理其特征值的问题。Catalin Marinas 指出，次级 CPU 应该能够修改这些值，以便系统能够选择覆盖值和其他值中最安全的一个。

在本周的新讨论中，Suzuki K Poulose 和 Catalin Marinas 进一步探讨了覆盖值的优先级问题，强调需要对次级 CPU 的不合理覆盖值发出警告，并建议在读取系统寄存器时对值进行清理。Suzuki 还提到，可能需要在代码中添加注释，说明覆盖不应适用于某些允许差异的特征。

总体来看，本周的讨论集中在如何处理覆盖值的安全性和警告机制上，推动了补丁的进一步完善。

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

---

### Thread 22: [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 23 Mar 2026 17:46:42 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，旨在允许在运行时设置 GICv3（通用中断控制器版本3）的支持。

1. **原始补丁内容**：补丁的核心是修改 `set_id_regs` 函数，使其能够在运行时创建 GICv3 虚拟机，并正确处理 ID 寄存器的写入。补丁的实现考虑到用户空间（如 QEMU）可能会写入不合理的值，因此在处理寄存器时需要对可变字段进行特别处理。

2. **之前讨论要点**：在历史讨论中并没有具体的内容记录，但可以推测，之前可能讨论过 KVM 对 GIC 支持的实现细节及其对虚拟机性能和稳定性的影响。

3. **本周的新讨论与进展**：在本周的讨论中，Marc Zyngier 提交了补丁并指出该补丁解决了他在 -next 分支中遇到的问题。Mark Brown 也对补丁进行了测试，并确认其有效性。最终，Marc Zyngier 表示该补丁已被应用到下一个版本中，标志着这一功能的正式集成。

综上所述，此次讨论集中在 KVM 对 GICv3 支持的运行时设置功能上，补丁经过测试并已成功合并。

#### 📝 邮件列表

1. **[03-23 17:46]** [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-24 02:14]** Re: [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set
 at runtime
   - 发件人: Mark Brown <broonie@kernel.org>
3. **[03-24 10:17]** Re: [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 23: [PATCH] tracing: Adjust cmd_check_undefined to show unexpected
 undefined symbols

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 20 Mar 2026 14:29:33 -0700

#### 🤖 AI 总结

本邮件讨论的主题是关于一个补丁（patch），旨在调整 Linux 内核中的 `cmd_check_undefined` 命令，以便在检测到未定义符号时能够输出相关信息，帮助开发者更好地理解构建失败的原因。该补丁的提出者是 Nathan Chancellor，补丁的背景是之前的提交 a717943d8ecc，旨在检查 `simple_ring_buffer` 中的未定义符号。

在历史讨论中，Nathan 指出当前的 `check_undefined` 命令在失败时没有输出，导致开发者难以诊断问题。因此，他提出通过捕获 `$(NM) + grep` 命令的输出并在失败时打印出来，以提高问题的可理解性。

在本周的新讨论中，参与者 Vincent Donnefort 对该补丁进行了审核并表示支持，确认了补丁的有效性。随后，Marc Zyngier 也表示该补丁已被应用到下一个版本中，感谢 Nathan 的贡献。这表明该补丁得到了认可并顺利推进。

#### 📝 邮件列表

1. **[03-20 14:29]** [PATCH] tracing: Adjust cmd_check_undefined to show unexpected
 undefined symbols
   - 发件人: Nathan Chancellor <nathan@kernel.org>
2. **[03-23 09:15]** Re: [PATCH] tracing: Adjust cmd_check_undefined to show unexpected
 undefined symbols
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[03-23 09:23]** Re: [PATCH] tracing: Adjust cmd_check_undefined to show unexpected undefined symbols
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 24: [PATCH] KVM: arm64: ptdump: Initialize parser_state before pgtable walk

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 28 Mar 2026 13:31:55 +0800

#### 🤖 AI 总结

本邮件讨论的主题是针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 ptdump 功能进行的补丁更新。补丁的主要内容是确保在进行页表遍历之前初始化 `parser_state`，以避免在调用 `kvm_pgtable_walk()` 时使用上一次运行时的状态，从而导致输出结果不正确。

在历史讨论中并没有提供具体的背景信息，但本周的讨论中，Zenghui Yu 提出了该补丁，指出在执行 `seq_read_iter()` 时可能会遇到需要更大缓冲区的情况，这会导致 `parser_state` 未被正确初始化。为了解决这个问题，补丁中移除了未使用的 `st::range`，并在开始新的页表遍历之前初始化 `parser_state`。

本周的进展是，Marc Zyngier 对该补丁表示认可，并已将其应用到下一个版本中，确认了补丁的有效性。整体来看，此次讨论有效地解决了页表遍历中的状态管理问题，提升了 KVM 的稳定性和准确性。

#### 📝 邮件列表

1. **[03-28 13:31]** [PATCH] KVM: arm64: ptdump: Initialize parser_state before pgtable walk
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
2. **[03-28 11:13]** Re: [PATCH] KVM: arm64: ptdump: Initialize parser_state before pgtable walk
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 25: [PATCH v10 28/30] KVM: arm64: selftests: Skip impossible invalid
 value tests

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 24 Mar 2026 14:54:54 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的自测试补丁（PATCH v10 28/30），其主要目的是跳过那些不可能的无效值测试。

在历史讨论中，Mark Brown 提到他对该函数进行了快速的循环检查，发现当掩码为 0x1 时，返回了一些超出掩码范围的值。这些测试结果显示了不同情况下的返回值，包括一些标记为“超出范围”的情况，表明在某些条件下测试可能不适用。

在本周的新讨论中，Ben Horgan 对 Mark 的检查结果表示感谢，并询问是否仍然可以获取相关数据。Mark 也对 Ben 的反馈表示了感谢，显示出双方在这一补丁讨论中的积极互动。

总体来看，本周的讨论主要集中在补丁的具体实现和测试结果上，参与者们在探讨如何更好地处理无效值测试的问题。

#### 📝 邮件列表

1. **[03-24 14:54]** Re: [PATCH v10 28/30] KVM: arm64: selftests: Skip impossible invalid
 value tests
   - 发件人: Ben Horgan <ben.horgan@arm.com>
2. **[03-24 14:56]** Re: [PATCH v10 28/30] KVM: arm64: selftests: Skip impossible invalid
 value tests
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 26: [PATCH] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 23 Mar 2026 17:47:13 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VGIC（虚拟通用中断控制器）实现的一个补丁，标题为“[PATCH] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time”。

原始补丁的内容是建议在虚拟机运行时，不要重置 guest 的 cpuif（GICv3）或 redistributor（GICv3）地址，而是将这些初始化操作移回到 VGIC 创建时进行。此补丁的目的是修复之前的一个问题，具体是针对提交 a258a383b9177 的修正。

在之前的讨论中，Marc Zyngier 提到重写 ID 寄存器在最终化时是可以接受的，但在虚拟机开始运行时重置地址则是一个不好的做法。因此，补丁的核心是确保在创建 VGIC 时就完成必要的初始化，以避免在运行时出现问题。

在本周的新讨论中，Marc Zyngier 确认了补丁的应用，并表示已将其纳入下一步的开发中。这表明该补丁得到了认可并将会在未来的版本中实施。

#### 📝 邮件列表

1. **[03-23 17:47]** [PATCH] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-24 10:17]** Re: [PATCH] KVM: arm64: vgic: Don't reset cpuif/redist addresses at finalize time
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 17 Mar 2026 18:26:36 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM（Kernel-based Virtual Machine）中为 arm64 架构暴露阴影页表（shadow page tables）到 debugfs 的补丁（patch）。历史讨论中，Wei-Lin Chang 提出了 v2 版本的补丁，主要改进包括将 debugfs_nv_dentry 移动到 CONFIG_PTDUMP_STAGE2_DEBUGFS 后面，使用宏定义阴影页转储的文件名，并增加了来自 Sebastian 的 Reviewed-by 标签。

在本周的新讨论中，Marc Zyngier 确认已将该补丁应用到下一个版本中，并感谢 Wei-Lin Chang 的贡献。补丁的两个主要提交分别是使 KVM 页转储代码支持 s2 MMU 以及在 debugfs 中暴露阴影页表。整体来看，讨论进展顺利，补丁已获得认可并被纳入后续版本中。

#### 📝 邮件列表

1. **[03-17 18:26]** [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[03-23 10:30]** Re: [PATCH v2 0/2] KVM: arm64: nv: Expose shadow page tables in debugfs
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 28: [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 28 Mar 2026 11:21:39 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构下的一个补丁，旨在允许在运行时设置 GICv3（通用中断控制器版本3）的支持。

**原始补丁内容**：
补丁主要修改了 `set_id_regs` 函数，使其能够在可能的情况下创建 GICv3 客户端，并在写入 ID 寄存器时考虑 GIC 的存在。补丁指出，KVM 现在会向客户机暴露 GIC 支持，无论用户空间（如 QEMU）如何配置。

**之前讨论要点**：
本邮件线程没有历史讨论记录，因此没有相关的背景信息。

**本周的新讨论与进展**：
本周的讨论由 Marc Zyngier 提出，补丁的主要内容是对 `set_id_regs` 函数的改进，增加了对可变字段的处理，确保在写入寄存器时只比较经过重新清理的寄存器。补丁还修正了编码和寄存器值的顺序。此外，补丁中新增了对可变字段的支持，使得在运行时可以强制设置 GICv3 支持。补丁的更新版本（v2）对编码顺序进行了正确的调整，确保了功能的准确性。

总的来说，此补丁旨在提升 KVM 在处理 GICv3 支持时的灵活性和准确性。

#### 📝 邮件列表

1. **[03-28 11:21]** [PATCH] KVM: arm64: set_id_regs: Allow GICv3 support to be set at runtime
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 29: [PATCH V2 0/2] arm64/mm: Drop TTBR_CNP_BIT and TTBR_ASID_MASK

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 27 Mar 2026 19:20:31 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 架构下内存管理的补丁，具体是删除 TTBR_CNP_BIT 和 TTBR_ASID_MASK 这两个宏定义。补丁的目的是简化代码，直接使用 TTBRx_EL1_ASID_MASK 和 TTBRx_EL1_CnP。

在历史讨论中，虽然没有详细的邮件记录，但可以推测出该补丁的提出是为了优化 ARM64 的内存管理相关代码，减少不必要的宏定义，提高代码的可读性和维护性。

在本周的新讨论中，参与者 Catalin Marinas 确认已将该补丁应用到 arm64 的开发分支（for-next/ttbr-macros-cleanup），表示感谢。这表明补丁得到了认可并已进入开发流程，预示着相关代码的清理和优化工作正在推进中。

#### 📝 邮件列表

1. **[03-27 19:20]** Re: [PATCH V2 0/2] arm64/mm: Drop TTBR_CNP_BIT and TTBR_ASID_MASK
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 30: [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare error

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 24 Mar 2026 17:27:57 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个补丁，主要涉及在 hyp（Hypervisor）共享和取消共享过程中处理引用计数的问题。

**原始 patch/问题内容**：
补丁的核心是确保在调用 `__pkvm_host_share_hyp` 或 `__pkvm_host_unshare_hyp` 函数失败时，能够回滚引用计数。这是为了保证 `hyp_shared_pfns` 的跟踪状态与实际共享状态一致。

**之前讨论要点**：
本次邮件没有提供历史讨论的上下文，因此无法总结之前的讨论要点。

**本周的新讨论、进展或结论**：
本周的讨论由 Vincent Donnefort 提出，具体补丁代码中增加了对共享和取消共享操作失败时的处理逻辑。若共享或取消共享操作失败，补丁将相应地回滚引用计数，以确保系统状态的一致性。补丁已被签署并准备提交，显示出对系统稳定性和可靠性的关注。

#### 📝 邮件列表

1. **[03-24 17:27]** [PATCH] KVM: arm64: pkvm: Rollback refcount on hyp share/unshare error
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 31: [PATCH] KVM: Remove subtle "struct kvm_stats_desc" pseudo-overlay

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 24 Mar 2026 06:07:28 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于一个针对 KVM 的补丁，旨在移除 "struct kvm_stats_desc" 的伪叠加（pseudo-overlay）。该补丁的目的是简化 KVM 代码，提升可读性和维护性。

在历史讨论中，虽然没有具体的邮件记录，但可以推测该补丁是基于对 KVM 代码结构的优化需求而提出的。参与者可能讨论了该结构的复杂性以及移除它所带来的潜在好处。

在本周的新讨论中，补丁已被应用到 riscv/linux.git 的 for-next 分支，表明该补丁得到了认可并已进入开发流程。Sean Christopherson 对此表示感谢，并确认了补丁的应用情况。整体来看，此次讨论表明了社区对 KVM 代码优化的持续关注和支持。

#### 📝 邮件列表

1. **[03-24 06:07]** Re: [PATCH] KVM: Remove subtle "struct kvm_stats_desc" pseudo-overlay
   - 发件人: patchwork-bot+linux-riscv@kernel.org

---

### Thread 32: [PATCH kvmtool v6 6/6] arm64: Handle virtio endianness reset when
 running nested

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 23 Mar 2026 16:31:27 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH kvmtool v6 6/6] arm64: Handle virtio endianness reset when running nested”，讨论内容主要集中在处理在嵌套运行时的 virtio 字节序重置问题。

在本周的新讨论中，Andre Przywara 回复了 Marc Zyngier，确认了之前的 patch 可能被忽视，Marc 表示这是一个显而易见的问题，但他未能及时修复。Andre 随后表示已经完成了修复，并将此更改应用到代码中，预告将会发布第七版（v7）。

总结来看，原始 patch 旨在解决在嵌套虚拟化环境中 virtio 的字节序重置问题。之前的讨论并未详细记录，但可以推测出该问题的解决被认为是简单且必要的。本周的进展是确认了修复的完成，并且即将发布更新版本，显示出开发者之间的积极沟通与协作。

#### 📝 邮件列表

1. **[03-23 16:31]** Re: [PATCH kvmtool v6 6/6] arm64: Handle virtio endianness reset when
 running nested
   - 发件人: Andre Przywara <andre.przywara@arm.com>

---

## 📌 RFC

共 1 个 thread

---

### Thread 1: [RFC PATCH 00/14] KVM: ITS hardening for pKVM

**📧 邮件数**: 13 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 10 Mar 2026 12:49:19 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 pKVM 的 KVM ITS 硬化的补丁系列（RFC PATCH 00/14）。该补丁旨在增强 GIC/ITS 控制器的安全性，防止攻击者通过设备访问篡改虚拟机监控器（hypervisor）保护的内存。补丁包括多个方面，如捐赠 MMIO（内存映射输入输出）给 hypervisor、跟踪未映射的 MMIO 区域，以及支持未映射设备的 MMIO 陷阱处理等。

在历史讨论中，参与者们探讨了补丁的实现细节和潜在问题。例如，Mostafa Saleh 提到在 Lenovo 设备上测试时遇到内核启动挂起的问题，并分享了相关日志。Sebastian Ene 和 Fuad Tabba 也讨论了补丁中使用的术语和设计选择，特别是关于“shadow”结构的命名。

在本周的新讨论中，Vincent Donnefort 提出了对补丁的具体改进建议，强调了 MMIO 和内存之间的区分，以及在 hypervisor 中早期映射区域的可能性。此外，Fuad Tabba 提出了两种改进方案，以减少在执行超慢 hypercall 时的锁持有时间，确保不会丢失命令或触发阶段二数据中止（Stage-2 Data Abort）。Sebastian Ene 也在继续调查之前提到的启动挂起问题，尝试在 Qemu 环境中重现该问题。

总体来看，讨论集中在补丁的实现细节、性能优化和安全性增强上，参与者们积极提出改进建议并解决遇到的问题。

#### 📝 邮件列表

1. **[03-10 12:49]** [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[03-10 12:49]** [PATCH 01/14] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[03-10 12:49]** [PATCH 02/14] KVM: arm64: Track host-unmapped MMIO regions in a
 static array
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[03-10 12:49]** [PATCH 03/14] KVM: arm64: Support host MMIO trap handlers for
 unmapped devices
   - 发件人: Sebastian Ene <sebastianene@google.com>
5. **[03-10 12:49]** [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for KVM
 host deprivilege
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[03-13 11:26]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Fuad Tabba <tabba@google.com>
7. **[03-13 15:18]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[03-20 15:11]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Sebastian Ene <sebastianene@google.com>
9. **[03-24 10:39]** Re: [PATCH 01/14] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[03-24 10:46]** Re: [PATCH 02/14] KVM: arm64: Track host-unmapped MMIO regions in a
 static array
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[03-24 10:59]** Re: [PATCH 03/14] KVM: arm64: Support host MMIO trap handlers for
 unmapped devices
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[03-24 14:36]** Re: [PATCH 05/14] irqchip/gic-v3-its: Prepare shadow structures for
 KVM host deprivilege
   - 发件人: Fuad Tabba <tabba@google.com>
13. **[03-25 16:26]** Re: [RFC PATCH 00/14] KVM: ITS hardening for pKVM
   - 发件人: Sebastian Ene <sebastianene@google.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.0, take #4

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 20 Mar 2026 09:41:51 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM/arm64 的修复补丁，主要集中在版本 7.0 的更新中。

1. **原始补丁内容**：Marc Zyngier 提出了两个修复补丁，主要针对嵌套虚拟化时可能出现的问题。第一个问题是虚拟 CPU 从重置状态恢复时，可能会跳过初始程序计数器（PC）的第一条指令。第二个问题涉及地址转换模拟中的指针运算错误，导致访问位在随机位置被设置。这两个问题被认为是稳定的候选修复。

2. **之前讨论要点**：在历史讨论中，Marc Zyngier 提出这些修复是针对 KVM/arm64 的重要更新，旨在解决在嵌套虚拟化环境中观察到的具体问题。

3. **本周的新讨论与进展**：在本周的讨论中，Paolo Bonzini 确认已将这些补丁合并，表示感谢。这表明补丁得到了认可并已被纳入代码库中。

综上所述，本次讨论主要围绕 KVM/arm64 的两个修复补丁，经过确认后已成功合并，标志着该领域的持续改进。

#### 📝 邮件列表

1. **[03-20 09:41]** [GIT PULL] KVM/arm64 fixes for 7.0, take #4
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[03-24 17:32]** Re: [GIT PULL] KVM/arm64 fixes for 7.0, take #4
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH v1 0/3] arm64: Add Stage-2 MMU and Nested Guest Framework

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 16 Mar 2026 15:43:46 -0700

#### 🤖 AI 总结

本邮件线程讨论了一个针对 ARM64 的 KVM 单元测试补丁系列，主要目的是引入 Stage-2 MMU 和嵌套来宾框架，以支持更复杂的虚拟化特性，如嵌套虚拟化（NV）和 GICv4 直接中断注入。

在历史讨论中，Jing Zhang 提出了三个补丁：
1. **Stage-2 页表管理库**：提供对 ARM64 Stage-2 转换表的管理，支持多种转换粒度（4K、16K、64K）和动态页表管理。
2. **裸金属来宾执行框架**：允许 KVM 单元测试作为 L1 虚拟机监控器运行，管理其 L2 来宾，支持来宾的生命周期管理。
3. **补充功能**：包括对来宾执行的支持和相关 API 的实现。

在本周的新讨论中，参与者 Joey Gouly 和 Wei-Lin Chang 对补丁提出了一些初步意见和建议。Joey 表示希望将他的测试与新框架兼容，并指出缺少在 EL0 执行的支持。Wei-Lin 则建议将某些代码分割成多个提交，以便更清晰地管理和审查，同时提出了一些代码优化建议，如宏定义和代码位置调整。

总体来看，讨论围绕补丁的细节和结构展开，参与者们积极提供反馈，以推动补丁的完善和合并。

#### 📝 邮件列表

1. **[03-16 15:43]** [kvm-unit-tests PATCH v1 0/3] arm64: Add Stage-2 MMU and Nested Guest Framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
2. **[03-16 15:43]** [kvm-unit-tests PATCH v1 1/3] lib: arm64: Add stage2 page table
 management library
   - 发件人: Jing Zhang <jingzhangos@google.com>
3. **[03-16 15:43]** [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest
 execution framework
   - 发件人: Jing Zhang <jingzhangos@google.com>
4. **[03-24 11:43]** Re: [kvm-unit-tests PATCH v1 0/3] arm64: Add Stage-2 MMU and Nested
 Guest Framework
   - 发件人: Joey Gouly <joey.gouly@arm.com>
5. **[03-24 15:04]** Re: [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest
 execution framework
   - 发件人: Joey Gouly <joey.gouly@arm.com>
6. **[03-24 15:12]** Re: [kvm-unit-tests PATCH v1 1/3] lib: arm64: Add stage2 page table
 management library
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[03-24 15:44]** Re: [kvm-unit-tests PATCH v1 2/3] lib: arm64: Add bare-metal guest
 execution framework
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

