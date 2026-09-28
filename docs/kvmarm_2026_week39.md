# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-09-28 03:54:39

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 889
- **总 Thread 数**: 58
- **大型 Thread** (>20封): 15 个

### 分类分布

- **PATCH**: 50 threads (764 邮件)
- **RFC**: 7 threads (122 邮件)
- **GIT PULL**: 1 threads (3 邮件)

---

## 📌 PATCH

共 50 个 thread

---

### Thread 1: [PATCH v8 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 72 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 22 Sep 2026 13:12:33 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:72, 61907 tokens)

#### 📝 邮件列表

1. **[09-22 13:12]** [PATCH v8 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[09-22 13:12]** [PATCH v8 01/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[09-22 13:12]** [PATCH v8 02/25] iommu/arm-smmu-v3: Move Queue and STE functions to header
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[09-22 13:12]** [PATCH v8 03/25] iommu/arm-smmu-v3: Introduce RangeInval encoding helpers
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[09-22 13:12]** [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[09-22 13:12]** [PATCH v8 05/25] iommu/arm-smmu-v3: Move hitless machinery to common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[09-22 13:12]** [PATCH v8 06/25] KVM: arm64: iommu: Introduce IOMMU driver infrastructure
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[09-22 13:12]** [PATCH v8 07/25] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
9. **[09-22 13:12]** [PATCH v8 08/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>
10. **[09-22 13:12]** [PATCH v8 09/25] KVM: arm64: iommu: Support DABT for IOMMU
   - 发件人: Mostafa Saleh <smostafa@google.com>
11. **[09-22 13:12]** [PATCH v8 10/25] iommu/arm-smmu-v3-kvm: Add SMMUv3 driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[09-22 13:12]** [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
13. **[09-22 13:12]** [PATCH v8 12/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
14. **[09-22 13:12]** [PATCH v8 13/25] iommu/arm-smmu-v3-kvm: Add MMIO emulation
   - 发件人: Mostafa Saleh <smostafa@google.com>
15. **[09-22 13:12]** [PATCH v8 14/25] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
16. **[09-22 13:12]** [PATCH v8 15/25] iommu/arm-smmu-v3-kvm: Add CMDQ functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[09-22 13:12]** [PATCH v8 16/25] iommu/arm-smmu-v3-kvm: Emulate CMDQ for host
   - 发件人: Mostafa Saleh <smostafa@google.com>
18. **[09-22 13:12]** [PATCH v8 17/25] iommu/arm-smmu-v3-kvm: Shadow stream table
   - 发件人: Mostafa Saleh <smostafa@google.com>
19. **[09-22 13:12]** [PATCH v8 18/25] iommu/arm-smmu-v3-kvm: Shadow STEs
   - 发件人: Mostafa Saleh <smostafa@google.com>
20. **[09-22 13:12]** [PATCH v8 19/25] iommu/arm-smmu-v3-kvm: Share other queues
   - 发件人: Mostafa Saleh <smostafa@google.com>
21. **[09-22 13:12]** [PATCH v8 20/25] iommu/arm-smmu-v3-kvm: Emulate GBPA
   - 发件人: Mostafa Saleh <smostafa@google.com>
22. **[09-22 13:12]** [PATCH v8 21/25] iommu/io-pgtable-arm: Support io-pgtable-arm in the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
23. **[09-22 13:12]** [PATCH v8 22/25] iommu/arm-smmu-v3-kvm: Shadow the CPU stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
24. **[09-22 13:12]** [PATCH v8 23/25] iommu/arm-smmu-v3-kvm: Invalidate the SMMU TLBs
   - 发件人: Mostafa Saleh <smostafa@google.com>
25. **[09-22 13:12]** [PATCH v8 24/25] iommu/arm-smmu-v3-kvm: Enable nesting
   - 发件人: Mostafa Saleh <smostafa@google.com>
26. **[09-22 13:12]** [PATCH v8 25/25] KVM: arm64: Add documentation for pKVM DMA isolation
   - 发件人: Mostafa Saleh <smostafa@google.com>
27. **[09-22 13:22]** Re: [PATCH v8 13/25] iommu/arm-smmu-v3-kvm: Add MMIO emulation
   - 发件人: sashiko-bot@kernel.org
28. **[09-22 13:23]** Re: [PATCH v8 07/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: sashiko-bot@kernel.org
29. **[09-22 13:25]** Re: [PATCH v8 08/25] KVM: arm64: iommu: Add memory pool
   - 发件人: sashiko-bot@kernel.org
30. **[09-22 13:28]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: sashiko-bot@kernel.org
31. **[09-22 13:29]** Re: [PATCH v8 01/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: sashiko-bot@kernel.org
32. **[09-22 13:32]** Re: [PATCH v8 16/25] iommu/arm-smmu-v3-kvm: Emulate CMDQ for host
   - 发件人: sashiko-bot@kernel.org
33. **[09-22 13:32]** Re: [PATCH v8 14/25] iommu/arm-smmu-v3-kvm: Shadow the command
 queue
   - 发件人: sashiko-bot@kernel.org
34. **[09-22 13:33]** Re: [PATCH v8 17/25] iommu/arm-smmu-v3-kvm: Shadow stream table
   - 发件人: sashiko-bot@kernel.org
35. **[09-22 13:38]** Re: [PATCH v8 22/25] iommu/arm-smmu-v3-kvm: Shadow the CPU stage-2
 page table
   - 发件人: sashiko-bot@kernel.org
36. **[09-22 13:45]** Re: [PATCH v8 23/25] iommu/arm-smmu-v3-kvm: Invalidate the SMMU
 TLBs
   - 发件人: sashiko-bot@kernel.org
37. **[09-22 13:49]** Re: [PATCH v8 24/25] iommu/arm-smmu-v3-kvm: Enable nesting
   - 发件人: sashiko-bot@kernel.org
38. **[09-22 14:25]** Re: [PATCH v8 01/25] KVM: arm64: Donate MMIO to the hypervisor
   - 发件人: Mostafa Saleh <smostafa@google.com>
39. **[09-22 14:29]** Re: [PATCH v8 07/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
40. **[09-22 14:34]** Re: [PATCH v8 08/25] KVM: arm64: iommu: Add memory pool
   - 发件人: Mostafa Saleh <smostafa@google.com>
41. **[09-22 15:12]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
42. **[09-22 15:30]** Re: [PATCH v8 13/25] iommu/arm-smmu-v3-kvm: Add MMIO emulation
   - 发件人: Mostafa Saleh <smostafa@google.com>
43. **[09-22 15:34]** Re: [PATCH v8 14/25] iommu/arm-smmu-v3-kvm: Shadow the command queue
   - 发件人: Mostafa Saleh <smostafa@google.com>
44. **[09-22 15:48]** Re: [PATCH v8 16/25] iommu/arm-smmu-v3-kvm: Emulate CMDQ for host
   - 发件人: Mostafa Saleh <smostafa@google.com>
45. **[09-22 15:50]** Re: [PATCH v8 17/25] iommu/arm-smmu-v3-kvm: Shadow stream table
   - 发件人: Mostafa Saleh <smostafa@google.com>
46. **[09-22 15:52]** Re: [PATCH v8 22/25] iommu/arm-smmu-v3-kvm: Shadow the CPU stage-2
 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
47. **[09-22 15:55]** Re: [PATCH v8 23/25] iommu/arm-smmu-v3-kvm: Invalidate the SMMU TLBs
   - 发件人: Mostafa Saleh <smostafa@google.com>
48. **[09-22 15:57]** Re: [PATCH v8 24/25] iommu/arm-smmu-v3-kvm: Enable nesting
   - 发件人: Mostafa Saleh <smostafa@google.com>
49. **[09-22 11:07]** Re: [PATCH v8 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and
 emulate)
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
50. **[09-22 11:23]** Re: [PATCH v8 02/25] iommu/arm-smmu-v3: Move Queue and STE functions
 to header
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
51. **[09-22 11:45]** Re: [PATCH v8 03/25] iommu/arm-smmu-v3: Introduce RangeInval
 encoding helpers
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
52. **[09-22 12:45]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
53. **[09-22 12:59]** Re: [PATCH v8 05/25] iommu/arm-smmu-v3: Move hitless machinery to
 common code
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
54. **[09-22 18:48]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
55. **[09-22 15:39]** Re: [PATCH v8 10/25] iommu/arm-smmu-v3-kvm: Add SMMUv3 driver
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
56. **[09-22 17:22]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
57. **[09-22 18:43]** Re: [PATCH v8 12/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Nicolin Chen <nicolinc@nvidia.com>
58. **[09-23 08:52]** Re: [PATCH v8 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and
 emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
59. **[09-23 10:09]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
60. **[09-23 10:13]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
61. **[09-23 10:15]** Re: [PATCH v8 05/25] iommu/arm-smmu-v3: Move hitless machinery to
 common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
62. **[09-23 10:30]** Re: [PATCH v8 10/25] iommu/arm-smmu-v3-kvm: Add SMMUv3 driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
63. **[09-23 11:52]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
64. **[09-23 08:52]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
65. **[09-23 08:55]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
66. **[09-23 12:03]** Re: [PATCH v8 12/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
67. **[09-23 12:18]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
68. **[09-23 12:21]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
69. **[09-23 09:34]** Re: [PATCH v8 04/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
70. **[09-23 12:55]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
71. **[09-23 17:07]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Mostafa Saleh <smostafa@google.com>
72. **[09-23 14:22]** Re: [PATCH v8 11/25] iommu/arm-smmu-v3-kvm: Add the kernel driver
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>

---

### Thread 2: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL

**📧 邮件数**: 67 | **👥 参与者**: 6 | **📅 开始时间**: Thu, 17 Sep 2026 17:22:09 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:15 新:52, 13298 tokens)

#### 📝 邮件列表

1. **[09-17 17:22]** [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-17 17:22]** [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-17 17:22]** [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA fields
 on new vma alloc
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-17 17:22]** [PATCH v3 03/40] mm/vma: introduce and use vma_[flags_]can_merge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-17 17:22]** [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-17 17:22]** [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-17 17:22]** [PATCH v3 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-17 17:22]** [PATCH v3 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
9. **[09-17 17:22]** [PATCH v3 08/40] mm: add mmap action for discontiguous kernel page
 mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
10. **[09-17 17:22]** [PATCH v3 09/40] docs: filesystems: update mmap_prepare docs for
 discontig kernel pgs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
11. **[09-17 17:22]** [PATCH v3 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-17 17:22]** [PATCH v3 16/40] mm/vma: only allow mmap to clear VMA_MAYWRITE_BIT
 if kernel-owned
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-17 17:22]** [PATCH v3 17/40] mm/vma: add and use vma_[flags]_is_fixed_mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-17 17:22]** [PATCH v3 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT VMAs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-17 17:22]** [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
16. **[09-23 09:57]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
17. **[09-23 08:21]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove file_doesnt_need_get
   - 发件人: Suren Baghdasaryan <surenb@google.com>
18. **[09-23 08:32]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Suren Baghdasaryan <surenb@google.com>
19. **[09-23 16:46]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
20. **[09-23 16:53]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
21. **[09-23 08:59]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove file_doesnt_need_get
   - 发件人: Suren Baghdasaryan <surenb@google.com>
22. **[09-23 09:09]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Suren Baghdasaryan <surenb@google.com>
23. **[09-23 09:23]** Re: [PATCH v3 03/40] mm/vma: introduce and use vma_[flags_]can_merge()
   - 发件人: Suren Baghdasaryan <surenb@google.com>
24. **[09-23 09:47]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Suren Baghdasaryan <surenb@google.com>
25. **[09-23 18:00]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
26. **[09-23 18:07]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
27. **[09-23 18:33]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
28. **[09-23 16:06]** Re: [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Zi Yan <ziy@nvidia.com>
29. **[09-23 22:20]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Zi Yan <ziy@nvidia.com>
30. **[09-23 22:25]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: Zi Yan <ziy@nvidia.com>
31. **[09-23 22:27]** Re: [PATCH v3 03/40] mm/vma: introduce and use
 vma_[flags_]can_merge()
   - 发件人: Zi Yan <ziy@nvidia.com>
32. **[09-23 22:52]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Zi Yan <ziy@nvidia.com>
33. **[09-24 11:03]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
34. **[09-24 11:06]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
35. **[09-24 11:21]** Re: [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
36. **[09-24 11:50]** Re: [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Zi Yan <ziy@nvidia.com>
37. **[09-24 12:38]** Re: [PATCH v3 03/40] mm/vma: introduce and use
 vma_[flags_]can_merge()
   - 发件人: Gregory Price <gourry@gourry.net>
38. **[09-24 13:17]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Gregory Price <gourry@gourry.net>
39. **[09-24 14:00]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Gregory Price <gourry@gourry.net>
40. **[09-24 15:00]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Liam R. Howlett <liam@infradead.org>
41. **[09-24 15:28]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set
 actions on a mergeable vma
   - 发件人: Zi Yan <ziy@nvidia.com>
42. **[09-24 15:30]** Re: [PATCH v3 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: Zi Yan <ziy@nvidia.com>
43. **[09-24 15:30]** Re: [PATCH v3 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: Zi Yan <ziy@nvidia.com>
44. **[09-25 00:28]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Suren Baghdasaryan <surenb@google.com>
45. **[09-25 00:35]** Re: [PATCH v3 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: Suren Baghdasaryan <surenb@google.com>
46. **[09-25 00:37]** Re: [PATCH v3 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: Suren Baghdasaryan <surenb@google.com>
47. **[09-25 10:12]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
48. **[09-25 10:35]** Re: [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
49. **[09-25 10:51]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
50. **[09-25 10:53]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
51. **[09-25 10:55]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
52. **[09-25 13:51]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
53. **[09-25 16:53]** Re: [PATCH v3 08/40] mm: add mmap action for discontiguous kernel
 page mapping
   - 发件人: Zi Yan <ziy@nvidia.com>
54. **[09-25 17:01]** Re: [PATCH v3 09/40] docs: filesystems: update mmap_prepare docs
 for discontig kernel pgs
   - 发件人: Zi Yan <ziy@nvidia.com>
55. **[09-26 00:06]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Arnd Bergmann <arnd@arndb.de>
56. **[09-25 21:37]** Re: [PATCH v3 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: Zi Yan <ziy@nvidia.com>
57. **[09-25 22:07]** Re: [PATCH v3 16/40] mm/vma: only allow mmap to clear
 VMA_MAYWRITE_BIT if kernel-owned
   - 发件人: Zi Yan <ziy@nvidia.com>
58. **[09-25 22:17]** Re: [PATCH v3 16/40] mm/vma: only allow mmap to clear
 VMA_MAYWRITE_BIT if kernel-owned
   - 发件人: Zi Yan <ziy@nvidia.com>
59. **[09-25 22:27]** Re: [PATCH v3 17/40] mm/vma: add and use
 vma_[flags]_is_fixed_mapping
   - 发件人: Zi Yan <ziy@nvidia.com>
60. **[09-25 22:30]** Re: [PATCH v3 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT
 VMAs
   - 发件人: Zi Yan <ziy@nvidia.com>
61. **[09-26 10:40]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
62. **[09-26 11:03]** Re: [PATCH v3 17/40] mm/vma: add and use vma_[flags]_is_fixed_mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
63. **[09-26 11:06]** Re: [PATCH v3 16/40] mm/vma: only allow mmap to clear
 VMA_MAYWRITE_BIT if kernel-owned
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
64. **[09-26 15:06]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Arnd Bergmann <arnd@arndb.de>
65. **[09-26 14:22]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
66. **[09-26 19:14]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Arnd Bergmann <arnd@arndb.de>
67. **[09-27 14:44]** Re: [PATCH v3 08/40] mm: add mmap action for discontiguous kernel
 page mapping
   - 发件人: Suren Baghdasaryan <surenb@google.com>

---

### Thread 3: [PATCH v19 00/20] KVM: arm64: CCA: Add basic plumbing for Realms

**📧 邮件数**: 59 | **👥 参与者**: 4 | **📅 开始时间**: Sun, 20 Sep 2026 22:28:25 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:20 新:39, 10646 tokens)

#### 📝 邮件列表

1. **[09-20 22:28]** [PATCH v19 00/20] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-20 22:28]** [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes to CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-20 22:28]** [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-20 22:28]** [PATCH v19 03/20] KVM: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[09-20 22:28]** [PATCH v19 04/20] KVM: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-20 22:28]** [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-20 22:28]** [PATCH v19 06/20] KVM: arm64: Refactor the vcpu_load to allow for VM specific callbacks
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-20 22:28]** [PATCH v19 07/20] KVM: arm64: Add vcpu load/put call backs for flavors
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-20 22:28]** [PATCH v19 08/20] KVM: arm64: Reuse kvm_stage2_unmap_range in kvm_unmap_gfn_range
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[09-20 22:28]** [PATCH v19 09/20] KVM: arm64: Add VM specific callback for S2 MMU operations
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[09-20 22:28]** [PATCH v19 10/20] KVM: arm64: Abstract out memory abort handling
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[09-20 22:28]** [PATCH v19 11/20] KVM: arm64: Mandate VGIC v3 for for VMs running on hyp that don't trust the host
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[09-20 22:28]** [PATCH v19 12/20] KVM: arm64: CCA: Add a new mode for supporting Realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
14. **[09-20 22:28]** [PATCH v19 15/20] KVM: arm64: CCA: Introduce Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[09-20 22:28]** [PATCH v19 16/20] KVM: arm64: CCA: Don't expose unsupported capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[09-20 22:28]** [PATCH v19 17/20] KVM: arm64: CCA: WARN on injected undef exceptions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-20 21:38]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: sashiko-bot@kernel.org
18. **[09-20 21:38]** Re: [PATCH v19 04/20] KVM: arm64: Avoid including linux/kvm_host.h
 in kvm_pgtable.h
   - 发件人: sashiko-bot@kernel.org
19. **[09-20 21:44]** Re: [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for
 protected guests
   - 发件人: sashiko-bot@kernel.org
20. **[09-20 23:24]** Re: [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for
 protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-21 09:18]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-21 09:25]** Re: [PATCH v19 04/20] KVM: arm64: Avoid including linux/kvm_host.h in
 kvm_pgtable.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
23. **[09-22 00:07]** Re: [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for
 protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
24. **[09-22 12:25]** Re: [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes
 to CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
25. **[09-22 12:32]** Re: [PATCH v19 03/20] KVM: arm64: Include kvm_emulate.h in
 kvm/arm_psci.h
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
26. **[09-22 12:40]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
27. **[09-22 12:57]** Re: [PATCH v19 06/20] KVM: arm64: Refactor the vcpu_load to allow
 for VM specific callbacks
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
28. **[09-22 22:53]** Re: [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes to
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
29. **[09-22 23:04]** Re: [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes to
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
30. **[09-22 23:09]** Re: [PATCH v19 06/20] KVM: arm64: Refactor the vcpu_load to allow for
 VM specific callbacks
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
31. **[09-22 15:12]** Re: [PATCH v19 07/20] KVM: arm64: Add vcpu load/put call backs for
 flavors
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
32. **[09-22 15:15]** Re: [PATCH v19 08/20] KVM: arm64: Reuse kvm_stage2_unmap_range in
 kvm_unmap_gfn_range
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
33. **[09-22 15:29]** Re: [PATCH v19 09/20] KVM: arm64: Add VM specific callback for S2
 MMU operations
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
34. **[09-22 15:38]** Re: [PATCH v19 10/20] KVM: arm64: Abstract out memory abort
 handling
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
35. **[09-22 15:42]** Re: [PATCH v19 11/20] KVM: arm64: Mandate VGIC v3 for for VMs
 running on hyp that don't trust the host
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
36. **[09-22 15:43]** Re: [PATCH v19 12/20] KVM: arm64: CCA: Add a new mode for
 supporting Realm guests
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
37. **[09-22 15:49]** Re: [PATCH v19 15/20] KVM: arm64: CCA: Introduce Realms
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
38. **[09-22 15:53]** Re: [PATCH v19 16/20] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
39. **[09-22 15:54]** Re: [PATCH v19 17/20] KVM: arm64: CCA: WARN on injected undef
 exceptions
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
40. **[09-23 00:21]** Re: [PATCH v19 09/20] KVM: arm64: Add VM specific callback for S2 MMU
 operations
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
41. **[09-23 00:38]** Re: [PATCH v19 11/20] KVM: arm64: Mandate VGIC v3 for for VMs running
 on hyp that don't trust the host
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
42. **[09-23 00:55]** Re: [PATCH v19 10/20] KVM: arm64: Abstract out memory abort handling
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
43. **[09-23 16:05]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
44. **[09-23 16:19]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
45. **[09-23 11:24]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
46. **[09-23 23:23]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
47. **[09-23 23:29]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
48. **[09-23 14:54]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
49. **[09-23 17:27]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
50. **[09-23 09:48]** Re: [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes
 to CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
51. **[09-23 09:51]** Re: [PATCH v19 01/20] KVM: arm64: protected VM: Handle user writes
 to CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
52. **[09-23 09:54]** Re: [PATCH v19 09/20] KVM: arm64: Add VM specific callback for S2
 MMU operations
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
53. **[09-23 22:37]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
54. **[09-24 11:11]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
55. **[09-24 09:48]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
56. **[09-24 20:37]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Gavin Shan <gshan@redhat.com>
57. **[09-24 20:40]** Re: [PATCH v19 00/20] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Gavin Shan <gshan@redhat.com>
58. **[09-24 11:49]** Re: [PATCH v19 00/20] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
59. **[09-24 16:11]** Re: [PATCH v19 09/20] KVM: arm64: Add VM specific callback for S2 MMU
 operations
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 4: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support

**📧 邮件数**: 47 | **👥 参与者**: 5 | **📅 开始时间**: Wed, 23 Sep 2026 16:15:43 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:47, 26199 tokens)

#### 📝 邮件列表

1. **[09-23 16:15]** [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-23 16:15]** [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-23 16:15]** [PATCH v4 02/14] arm64: Add ESR fault helpers
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-23 16:15]** [PATCH v4 03/14] KVM: arm64: Use ESR helpers in guest abort
 handling
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-23 16:15]** [PATCH v4 04/14] KVM: arm64: Propagate and use esr in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-23 16:15]** [PATCH v4 05/14] KVM: arm64: Propagate and use mmu in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-23 16:15]** [PATCH v4 06/14] KVM: arm64: Propagate and use kvm_s2_fault_result
 on S2 fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-23 16:15]** [PATCH v4 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
9. **[09-23 16:15]** [PATCH v4 08/14] KVM: arm64: Propagate EHWPOISON in
 kvm_s2_fault_pin_pfn()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
10. **[09-23 16:15]** [PATCH v4 09/14] KVM: arm64: Pass walk flags to
 kvm_pgtable_get_leaf()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
11. **[09-23 16:15]** [PATCH v4 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-23 16:15]** [PATCH v4 11/14] Documentation: KVM: document arm64
 KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-23 16:15]** [PATCH v4 12/14] KVM: selftests: Enable pre_fault_memory_test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-23 16:15]** [PATCH v4 13/14] KVM: selftests: Add option for different backing
 in pre-fault tests
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-23 16:15]** [PATCH v4 14/14] KVM: selftests: Add nested pre-fault test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
16. **[09-23 15:21]** Re: [PATCH v4 09/14] KVM: arm64: Pass walk flags to
 kvm_pgtable_get_leaf()
   - 发件人: sashiko-bot@kernel.org
17. **[09-23 15:23]** Re: [PATCH v4 08/14] KVM: arm64: Propagate EHWPOISON in
 kvm_s2_fault_pin_pfn()
   - 发件人: sashiko-bot@kernel.org
18. **[09-23 15:24]** Re: [PATCH v4 04/14] KVM: arm64: Propagate and use esr in s2fd when
 handling guest aborts
   - 发件人: sashiko-bot@kernel.org
19. **[09-23 15:24]** Re: [PATCH v4 03/14] KVM: arm64: Use ESR helpers in guest abort
 handling
   - 发件人: sashiko-bot@kernel.org
20. **[09-23 15:24]** Re: [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: sashiko-bot@kernel.org
21. **[09-23 15:25]** Re: [PATCH v4 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: sashiko-bot@kernel.org
22. **[09-23 15:25]** Re: [PATCH v4 02/14] arm64: Add ESR fault helpers
   - 发件人: sashiko-bot@kernel.org
23. **[09-23 15:27]** Re: [PATCH v4 06/14] KVM: arm64: Propagate and use
 kvm_s2_fault_result on S2 fault
   - 发件人: sashiko-bot@kernel.org
24. **[09-23 15:29]** Re: [PATCH v4 05/14] KVM: arm64: Propagate and use mmu in s2fd when
 handling guest aborts
   - 发件人: sashiko-bot@kernel.org
25. **[09-23 15:29]** Re: [PATCH v4 12/14] KVM: selftests: Enable pre_fault_memory_test
 for arm64
   - 发件人: sashiko-bot@kernel.org
26. **[09-23 15:29]** Re: [PATCH v4 14/14] KVM: selftests: Add nested pre-fault test for
 arm64
   - 发件人: sashiko-bot@kernel.org
27. **[09-23 15:30]** Re: [PATCH v4 13/14] KVM: selftests: Add option for different
 backing in pre-fault tests
   - 发件人: sashiko-bot@kernel.org
28. **[09-23 15:31]** Re: [PATCH v4 11/14] Documentation: KVM: document arm64
 KVM_PRE_FAULT_MEMORY
   - 发件人: sashiko-bot@kernel.org
29. **[09-23 15:33]** Re: [PATCH v4 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: sashiko-bot@kernel.org
30. **[09-23 10:29]** Re: [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Sean Christopherson <seanjc@google.com>
31. **[09-23 19:23]** Re: [PATCH v4 03/14] KVM: arm64: Use ESR helpers in guest abort handling
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
32. **[09-23 19:24]** Re: [PATCH v4 04/14] KVM: arm64: Propagate and use esr in s2fd when
 handling guest aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
33. **[09-23 19:24]** Re: [PATCH v4 05/14] KVM: arm64: Propagate and use mmu in s2fd when
 handling guest aborts
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[09-23 19:24]** Re: [PATCH v4 02/14] arm64: Add ESR fault helpers
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
35. **[09-23 19:25]** Re: [PATCH v4 06/14] KVM: arm64: Propagate and use
 kvm_s2_fault_result on S2 fault
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
36. **[09-23 19:52]** Re: [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
37. **[09-24 07:08]** Re: [PATCH v4 12/14] KVM: selftests: Enable pre_fault_memory_test for arm64
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[09-24 07:08]** Re: [PATCH v4 11/14] Documentation: KVM: document arm64 KVM_PRE_FAULT_MEMORY
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
39. **[09-24 07:08]** Re: [PATCH v4 13/14] KVM: selftests: Add option for different backing
 in pre-fault tests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
40. **[09-24 07:09]** Re: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
41. **[09-24 09:22]** Re: [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
42. **[09-24 09:28]** Re: [PATCH v4 13/14] KVM: selftests: Add option for different
 backing in pre-fault tests
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
43. **[09-24 22:08]** Re: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Marc Zyngier <maz@kernel.org>
44. **[09-24 23:29]** Re: [PATCH v4 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Marc Zyngier <maz@kernel.org>
45. **[09-24 23:36]** Re: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Marc Zyngier <maz@kernel.org>
46. **[09-25 09:51]** Re: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
47. **[09-25 20:48]** Re: [PATCH v4 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 5: [PATCH v9 00/22] ARM64 PMU Partitioning

**📧 邮件数**: 46 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 24 Sep 2026 17:29:06 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:46, 51638 tokens)

#### 📝 邮件列表

1. **[09-24 17:29]** [PATCH v9 00/22] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[09-24 17:29]** [PATCH v9 01/22] arm64: cpufeature: Add cpucap for HPMN0
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[09-24 17:29]** [PATCH v9 02/22] KVM: arm64: Reorganize PMU includes
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[09-24 17:29]** [PATCH v9 03/22] KVM: arm64: Reorganize PMU functions
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[09-24 17:29]** [PATCH v9 04/22] perf: arm_pmuv3: Generalize counter bitmasks
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[09-24 17:29]** [PATCH v9 05/22] perf: arm_pmuv3: Move counter allocation mask to
 per-CPU struct pmu_hw_events
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[09-24 17:29]** [PATCH v9 06/22] perf: arm_pmuv3: Check cntr_mask before using pmccntr
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[09-24 17:29]** [PATCH v9 07/22] perf: arm_pmuv3: Allocate counter indices from high
 to low
   - 发件人: Colton Lewis <coltonlewis@google.com>
9. **[09-24 17:29]** [PATCH v9 08/22] KVM: arm64: Add initial scaffolding for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
10. **[09-24 17:29]** [PATCH v9 09/22] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
11. **[09-24 17:29]** [PATCH v9 10/22] KVM: arm64: Add Partitioned PMU register trap handlers
   - 发件人: Colton Lewis <coltonlewis@google.com>
12. **[09-24 17:29]** [PATCH v9 11/22] KVM: arm64: Set up MDCR_EL2 to handle a Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
13. **[09-24 17:29]** [PATCH v9 12/22] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>
14. **[09-24 17:29]** [PATCH v9 13/22] KVM: arm64: Enforce PMU event filter at vcpu_load()
   - 发件人: Colton Lewis <coltonlewis@google.com>
15. **[09-24 17:29]** [PATCH v9 14/22] perf: Add perf_pmu_resched_update()
   - 发件人: Colton Lewis <coltonlewis@google.com>
16. **[09-24 17:29]** [PATCH v9 15/22] KVM: arm64: Allow kvm_vcpu_pmu_resync_el0() to
 resync filters in process context
   - 发件人: Colton Lewis <coltonlewis@google.com>
17. **[09-24 17:29]** [PATCH v9 16/22] KVM: arm64: Apply dynamic guest counter reservations
   - 发件人: Colton Lewis <coltonlewis@google.com>
18. **[09-24 17:29]** [PATCH v9 17/22] KVM: arm64: Implement lazy PMU context swaps
   - 发件人: Colton Lewis <coltonlewis@google.com>
19. **[09-24 17:29]** [PATCH v9 18/22] perf: arm_pmuv3: Handle IRQs for Partitioned PMU
 guest counters
   - 发件人: Colton Lewis <coltonlewis@google.com>
20. **[09-24 17:29]** [PATCH v9 19/22] KVM: arm64: Detect overflows for the Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
21. **[09-24 17:29]** [PATCH v9 20/22] KVM: arm64: Add vCPU device attr to partition the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
22. **[09-24 17:29]** [PATCH v9 21/22] KVM: selftests: Add find_bit to KVM library
   - 发件人: Colton Lewis <coltonlewis@google.com>
23. **[09-24 17:29]** [PATCH v9 22/22] KVM: arm64: selftests: Add test case for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
24. **[09-24 17:30]** [PATCH] target/arm: Enable KVM PMU partitioning and counter limit
   - 发件人: Colton Lewis <coltonlewis@google.com>
25. **[09-24 17:37]** Re: [PATCH v9 04/22] perf: arm_pmuv3: Generalize counter bitmasks
   - 发件人: sashiko-bot@kernel.org
26. **[09-24 17:37]** Re: [PATCH v9 07/22] perf: arm_pmuv3: Allocate counter indices from
 high to low
   - 发件人: sashiko-bot@kernel.org
27. **[09-24 17:38]** Re: [PATCH v9 06/22] perf: arm_pmuv3: Check cntr_mask before using
 pmccntr
   - 发件人: sashiko-bot@kernel.org
28. **[09-24 17:38]** Re: [PATCH v9 02/22] KVM: arm64: Reorganize PMU includes
   - 发件人: sashiko-bot@kernel.org
29. **[09-24 17:44]** Re: [PATCH v9 08/22] KVM: arm64: Add initial scaffolding for
 Partitioned PMU
   - 发件人: sashiko-bot@kernel.org
30. **[09-24 17:44]** Re: [PATCH v9 05/22] perf: arm_pmuv3: Move counter allocation mask
 to per-CPU struct pmu_hw_events
   - 发件人: sashiko-bot@kernel.org
31. **[09-24 17:45]** Re: [PATCH v9 01/22] arm64: cpufeature: Add cpucap for HPMN0
   - 发件人: sashiko-bot@kernel.org
32. **[09-24 17:46]** Re: [PATCH v9 14/22] perf: Add perf_pmu_resched_update()
   - 发件人: sashiko-bot@kernel.org
33. **[09-24 17:47]** Re: [PATCH v9 13/22] KVM: arm64: Enforce PMU event filter at
 vcpu_load()
   - 发件人: sashiko-bot@kernel.org
34. **[09-24 17:49]** Re: [PATCH v9 03/22] KVM: arm64: Reorganize PMU functions
   - 发件人: sashiko-bot@kernel.org
35. **[09-24 17:50]** Re: [PATCH v9 10/22] KVM: arm64: Add Partitioned PMU register trap
 handlers
   - 发件人: sashiko-bot@kernel.org
36. **[09-24 17:51]** Re: [PATCH v9 15/22] KVM: arm64: Allow kvm_vcpu_pmu_resync_el0() to
 resync filters in process context
   - 发件人: sashiko-bot@kernel.org
37. **[09-24 17:52]** Re: [PATCH v9 21/22] KVM: selftests: Add find_bit to KVM library
   - 发件人: sashiko-bot@kernel.org
38. **[09-24 17:52]** Re: [PATCH v9 09/22] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: sashiko-bot@kernel.org
39. **[09-24 17:53]** Re: [PATCH v9 11/22] KVM: arm64: Set up MDCR_EL2 to handle a
 Partitioned PMU
   - 发件人: sashiko-bot@kernel.org
40. **[09-24 17:55]** Re: [PATCH v9 17/22] KVM: arm64: Implement lazy PMU context swaps
   - 发件人: sashiko-bot@kernel.org
41. **[09-24 17:55]** Re: [PATCH v9 12/22] KVM: arm64: Context swap Partitioned PMU guest
 registers
   - 发件人: sashiko-bot@kernel.org
42. **[09-24 17:55]** Re: [PATCH v9 22/22] KVM: arm64: selftests: Add test case for
 Partitioned PMU
   - 发件人: sashiko-bot@kernel.org
43. **[09-24 17:56]** Re: [PATCH v9 20/22] KVM: arm64: Add vCPU device attr to partition
 the PMU
   - 发件人: sashiko-bot@kernel.org
44. **[09-24 17:57]** Re: [PATCH v9 16/22] KVM: arm64: Apply dynamic guest counter
 reservations
   - 发件人: sashiko-bot@kernel.org
45. **[09-24 18:03]** Re: [PATCH v9 18/22] perf: arm_pmuv3: Handle IRQs for Partitioned
 PMU guest counters
   - 发件人: sashiko-bot@kernel.org
46. **[09-24 18:07]** Re: [PATCH v9 19/22] KVM: arm64: Detect overflows for the
 Partitioned PMU
   - 发件人: sashiko-bot@kernel.org

---

### Thread 6: [PATCH v19 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support

**📧 邮件数**: 44 | **👥 参与者**: 9 | **📅 开始时间**: Thu, 24 Sep 2026 14:51:54 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:44, 32675 tokens)

#### 📝 邮件列表

1. **[09-24 14:51]** [PATCH v19 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-24 14:51]** [PATCH v19 1/7] firmware: arm_rmm: Add SMC definitions for calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-24 14:51]** [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-24 14:51]** [PATCH v19 3/7] firmware: arm_rmm: Configure the RMM with the host's page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[09-24 14:51]** [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-24 14:51]** [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-24 14:52]** [PATCH v19 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-24 14:52]** [PATCH v19 7/7] firmware: arm_rmm: Add wrappers for Realm related RMI commands
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-24 14:00]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at
 init
   - 发件人: sashiko-bot@kernel.org
10. **[09-24 14:08]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: sashiko-bot@kernel.org
11. **[09-24 09:57]** Re: [PATCH v19 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
12. **[09-24 09:58]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at
 init
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
13. **[09-24 10:03]** Re: [PATCH v19 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
14. **[09-24 10:05]** Re: [PATCH v19 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Ackerley Tng <ackerleytng@google.com>
15. **[09-24 12:13]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
16. **[09-24 14:38]** Re: [PATCH v19 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
17. **[09-24 23:15]** Re: [PATCH v19 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-24 23:49]** Re: [PATCH v19 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-25 00:10]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-25 00:18]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-25 00:30]** Re: [PATCH v19 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-25 10:00]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
23. **[09-25 10:03]** Re: [PATCH v19 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Gavin Shan <gshan@redhat.com>
24. **[09-25 10:07]** Re: [PATCH v19 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Gavin Shan <gshan@redhat.com>
25. **[09-25 15:24]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
26. **[09-25 15:43]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
27. **[09-25 16:29]** Re: [PATCH v19 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support
   - 发件人: Gavin Shan <gshan@redhat.com>
28. **[09-25 09:50]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
29. **[09-25 09:51]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
30. **[09-25 10:03]** Re: [PATCH v19 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
31. **[09-25 11:42]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
32. **[09-25 12:50]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
33. **[09-25 12:56]** Re: [PATCH v19 7/7] firmware: arm_rmm: Add wrappers for Realm
 related RMI commands
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
34. **[09-25 13:17]** Re: [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
35. **[09-25 15:56]** Re: [PATCH v19 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
36. **[09-25 16:02]** Re: [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
37. **[09-25 16:11]** Re: [PATCH v19 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
38. **[09-25 16:23]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
39. **[09-25 08:30]** Re: [PATCH v19 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
40. **[09-25 08:34]** Re: [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Alper Gun <alpergun@google.com>
41. **[09-25 17:42]** Re: [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
42. **[09-25 18:50]** Re: [PATCH v19 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
43. **[09-26 19:08]** Re: [PATCH v19 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Venkata Rao Kakani <venkata.kakani@oss.qualcomm.com>
44. **[09-27 10:29]** Re: [PATCH v19 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 7: [PATCH v3 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support

**📧 邮件数**: 43 | **👥 参与者**: 5 | **📅 开始时间**: Tue, 22 Sep 2026 15:17:54 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:43, 27099 tokens)

#### 📝 邮件列表

1. **[09-22 15:17]** [PATCH v3 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-22 15:17]** [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-22 15:17]** [PATCH v3 02/14] arm64: Add ESR fault helpers
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-22 15:17]** [PATCH v3 03/14] KVM: arm64: Use ESR helpers in guest abort
 handling
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-22 15:17]** [PATCH v3 04/14] KVM: arm64: Propagate and use esr in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-22 15:17]** [PATCH v3 05/14] KVM: arm64: Propagate and use mmu in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-22 15:18]** [PATCH v3 06/14] KVM: arm64: Propagate and use kvm_s2_fault_result
 on S2 fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-22 15:18]** [PATCH v3 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
9. **[09-22 15:18]** [PATCH v3 08/14] KVM: arm64: Propagate EHWPOISON in
 kvm_s2_fault_pin_pfn()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
10. **[09-22 15:18]** [PATCH v3 09/14] KVM: arm64: Pass walk flags to
 kvm_pgtable_get_leaf()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
11. **[09-22 15:18]** [PATCH v3 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-22 15:18]** [PATCH v3 11/14] Documentation: KVM: document arm64
 KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-22 15:18]** [PATCH v3 12/14] KVM: selftests: Enable pre_fault_memory_test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-22 15:18]** [PATCH v3 13/14] KVM: selftests: Add option for different backing
 in pre-fault tests
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-22 15:18]** [PATCH v3 14/14] KVM: selftests: Add nested pre-fault test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
16. **[09-22 14:31]** Re: [PATCH v3 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: sashiko-bot@kernel.org
17. **[09-22 09:49]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Oliver Upton <oupton@kernel.org>
18. **[09-22 10:00]** Re: [PATCH v3 02/14] arm64: Add ESR fault helpers
   - 发件人: Oliver Upton <oupton@kernel.org>
19. **[09-22 10:23]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Sean Christopherson <seanjc@google.com>
20. **[09-22 18:30]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
21. **[09-22 18:31]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
22. **[09-22 10:36]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Sean Christopherson <seanjc@google.com>
23. **[09-22 18:45]** Re: [PATCH v3 02/14] arm64: Add ESR fault helpers
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
24. **[09-22 19:01]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
25. **[09-22 11:07]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Oliver Upton <oupton@kernel.org>
26. **[09-22 11:13]** Re: [PATCH v3 02/14] arm64: Add ESR fault helpers
   - 发件人: Oliver Upton <oupton@kernel.org>
27. **[09-22 19:35]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
28. **[09-22 11:40]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Sean Christopherson <seanjc@google.com>
29. **[09-22 11:46]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Sean Christopherson <seanjc@google.com>
30. **[09-22 19:52]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
31. **[09-22 19:54]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
32. **[09-22 13:42]** Re: [PATCH v3 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Oliver Upton <oupton@kernel.org>
33. **[09-23 11:03]** Re: [PATCH v3 00/14] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[09-23 11:54]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
35. **[09-23 12:00]** Re: [PATCH v3 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
36. **[09-23 12:05]** Re: [PATCH v3 08/14] KVM: arm64: Propagate EHWPOISON in kvm_s2_fault_pin_pfn()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
37. **[09-23 12:07]** Re: [PATCH v3 09/14] KVM: arm64: Pass walk flags to kvm_pgtable_get_leaf()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[09-23 12:18]** Re: [PATCH v3 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
39. **[09-23 14:26]** Re: [PATCH v3 01/14] KVM: Allow architectures to disallow pre-fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
40. **[09-23 14:28]** Re: [PATCH v3 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
41. **[09-23 14:30]** Re: [PATCH v3 07/14] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
42. **[09-23 14:32]** Re: [PATCH v3 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
43. **[09-23 14:33]** Re: [PATCH v3 10/14] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 8: [PATCH v18 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support

**📧 邮件数**: 37 | **👥 参与者**: 4 | **📅 开始时间**: Sat, 12 Sep 2026 09:36:03 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:15 新:22, 7620 tokens)

#### 📝 邮件列表

1. **[09-12 09:36]** [PATCH v18 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-12 09:36]** [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-12 09:36]** [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-12 09:36]** [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the host's page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[09-12 09:36]** [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-12 09:36]** [PATCH v18 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-12 09:36]** [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-14 11:27]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
9. **[09-16 11:23]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Alper Gun <alpergun@google.com>
10. **[09-18 18:27]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
11. **[09-18 18:27]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at
 init
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
12. **[09-18 18:27]** Re: [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
13. **[09-18 18:27]** Re: [PATCH v18 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
14. **[09-18 18:27]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
15. **[09-18 18:27]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
16. **[09-21 10:00]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-21 10:04]** Re: [PATCH v18 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-21 10:27]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-21 10:30]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-21 10:31]** Re: [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-21 10:32]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-21 11:02]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
23. **[09-21 11:14]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
24. **[09-21 13:42]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
25. **[09-21 14:38]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
26. **[09-21 14:27]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
27. **[09-21 14:29]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
28. **[09-21 14:33]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
29. **[09-21 14:37]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at
 init
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
30. **[09-21 14:46]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
31. **[09-21 14:53]** Re: [PATCH v18 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI
 support
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
32. **[09-21 14:58]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
33. **[09-21 23:38]** Re: [PATCH v18 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
34. **[09-22 23:55]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
35. **[09-23 09:46]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
36. **[09-23 23:31]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
37. **[09-23 23:34]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 9: [PATCH v9 00/26] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 30 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 16 Sep 2026 16:45:23 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:13 新:17, 4002 tokens)

#### 📝 邮件列表

1. **[09-16 16:45]** [PATCH v9 00/26] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[09-16 16:45]** [PATCH v9 01/26] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[09-16 16:45]** [PATCH v9 03/26] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[09-16 16:45]** [PATCH v9 04/26] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[09-16 16:45]** [PATCH v9 05/26] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[09-16 16:45]** [PATCH v9 06/26] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[09-16 16:45]** [PATCH v9 07/26] target/arm/cpu-idregs.h.inc: generate with script
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[09-16 16:45]** [PATCH v9 08/26] target/arm/cpu-idregs.h.inc: Generate enum values
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[09-16 16:45]** [PATCH v9 09/26] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[09-16 16:45]** [PATCH v9 10/26] target/arm/kvm: Retrieve writable ID reg map
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[09-16 16:45]** [PATCH v9 11/26] hw/arm/virt: Make sure virt_get_caches() keeps on reading CLIDR_EL1 as 0
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[09-16 16:45]** [PATCH v9 12/26] arm/kvm: Initialize isar.idregs[] with all writable host ID regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[09-16 16:45]** [PATCH v9 13/26] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[09-23 07:08]** Re: [PATCH v9 01/26] scripts: introduce
 scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
15. **[09-23 09:13]** Re: [PATCH v9 03/26] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
16. **[09-23 16:22]** Re: [PATCH v9 01/26] scripts: introduce
 scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[09-23 16:31]** Re: [PATCH v9 03/26] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[09-24 06:26]** Re: [PATCH v9 13/26] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
19. **[09-24 08:42]** Re: [PATCH v9 13/26] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
20. **[09-24 10:01]** Re: [PATCH v9 04/26] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
21. **[09-24 10:18]** Re: [PATCH v9 05/26] scripts: Introduce
 scripts/aarch64_sysreg_helpers module
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[09-24 10:23]** Re: [PATCH v9 05/26] scripts: Introduce
 scripts/aarch64_sysreg_helpers module
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
23. **[09-24 10:24]** Re: [PATCH v9 01/26] scripts: introduce
 scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[09-25 09:29]** Re: [PATCH v9 06/26] scripts: Introduce
 scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
25. **[09-25 11:19]** Re: [PATCH v9 07/26] target/arm/cpu-idregs.h.inc: generate with
 script
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
26. **[09-25 11:59]** Re: [PATCH v9 08/26] target/arm/cpu-idregs.h.inc: Generate enum
 values
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
27. **[09-25 12:16]** Re: [PATCH v9 09/26] target/arm/cpu_idregs: generate tables for Arm64
 ID registers and fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
28. **[09-25 12:37]** Re: [PATCH v9 10/26] target/arm/kvm: Retrieve writable ID reg map
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
29. **[09-25 12:46]** Re: [PATCH v9 11/26] hw/arm/virt: Make sure virt_get_caches() keeps
 on reading CLIDR_EL1 as 0
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
30. **[09-25 13:27]** Re: [PATCH v9 12/26] arm/kvm: Initialize isar.idregs[] with all
 writable host ID regs
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 10: [PATCH 01/22] KVM: arm64: nv: Introduce struct for stage-2 walk step

**📧 邮件数**: 28 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 21 Sep 2026 12:30:01 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:28, 5606 tokens)

#### 📝 邮件列表

1. **[09-21 12:30]** Re: [PATCH 01/22] KVM: arm64: nv: Introduce struct for stage-2 walk step
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[09-21 14:46]** Re: [PATCH 02/22] KVM: arm64: nv: Consolidate computation of stage-2 permissions
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[09-21 17:18]** Re: [PATCH 03/22] KVM: arm64: nv: Get rid of kvm_s2_trans*() accessors
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[09-21 17:51]** Re: [PATCH 04/22] KVM: arm64: nv: Only shadow writable-dirty guest descs as writable
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[09-21 18:28]** Re: [PATCH 05/22] KVM: arm64: nv: Pass an access descriptor for stage-2 walks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
6. **[09-21 14:28]** Re: [PATCH 02/22] KVM: arm64: nv: Consolidate computation of stage-2
 permissions
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[09-21 14:39]** Re: [PATCH 04/22] KVM: arm64: nv: Only shadow writable-dirty guest
 descs as writable
   - 发件人: Oliver Upton <oupton@kernel.org>
8. **[09-21 14:45]** Re: [PATCH 05/22] KVM: arm64: nv: Pass an access descriptor for
 stage-2 walks
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[09-22 15:24]** Re: [PATCH 05/22] KVM: arm64: nv: Pass an access descriptor for stage-2 walks
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[09-22 17:14]** Re: [PATCH 06/22] KVM: arm64: nv: Use a helper for stage-2 descriptor updates
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[09-22 09:31]** Re: [PATCH 06/22] KVM: arm64: nv: Use a helper for stage-2
 descriptor updates
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[09-23 15:09]** Re: [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Leonardo Bras <leo.bras@arm.com>
13. **[09-23 15:38]** Re: [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: Leonardo Bras <leo.bras@arm.com>
14. **[09-23 16:47]** Re: [PATCH 09/22] KVM: arm64: Compute S1 permissions as part of s1_walk()
   - 发件人: Leonardo Bras <leo.bras@arm.com>
15. **[09-23 17:21]** Re: [PATCH 10/22] KVM: arm64: Plumb through access descriptor for stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
16. **[09-23 09:46]** Re: [PATCH 07/22] KVM: arm64: nv: Set dirty state at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
17. **[09-23 18:03]** Re: [PATCH 11/22] KVM: arm64: Use a struct for stage-1 walk context
   - 发件人: Leonardo Bras <leo.bras@arm.com>
18. **[09-23 10:16]** Re: [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: Oliver Upton <oupton@kernel.org>
19. **[09-23 13:23]** Re: [PATCH 11/22] KVM: arm64: Use a struct for stage-1 walk context
   - 发件人: Oliver Upton <oupton@kernel.org>
20. **[09-23 13:37]** Re: [PATCH 10/22] KVM: arm64: Plumb through access descriptor for
 stage-1
   - 发件人: Oliver Upton <oupton@kernel.org>
21. **[09-24 18:22]** Re: [PATCH 08/22] KVM: arm64: nv: Treat DBM as writable at stage-2
   - 发件人: Leonardo Bras <leo.bras@arm.com>
22. **[09-25 12:10]** Re: [PATCH 10/22] KVM: arm64: Plumb through access descriptor for stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
23. **[09-25 12:20]** Re: [PATCH 11/22] KVM: arm64: Use a struct for stage-1 walk context
   - 发件人: Leonardo Bras <leo.bras@arm.com>
24. **[09-25 15:35]** Re: [PATCH 12/22] KVM: arm64: Create helper for stage-1 descriptor updates
   - 发件人: Leonardo Bras <leo.bras@arm.com>
25. **[09-25 16:07]** Re: [PATCH 13/22] KVM: arm64: Set dirty state at stage-1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
26. **[09-25 16:18]** Re: [PATCH 14/22] KVM: arm64: Grant write permission when DBM is set at S1
   - 发件人: Leonardo Bras <leo.bras@arm.com>
27. **[09-25 16:51]** Re: [PATCH 15/22] KVM: arm64: Don't update descriptors for "non-arch" access
   - 发件人: Leonardo Bras <leo.bras@arm.com>
28. **[09-25 16:53]** Re: [PATCH 16/22] KVM: arm64: nv: Expose FEAT_HAFDBS
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 11: [PATCH v7 00/10] mlx5 support for VFIO self test

**📧 邮件数**: 25 | **👥 参与者**: 5 | **📅 开始时间**: Mon, 21 Sep 2026 19:35:40 -0300

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:25, 34833 tokens)

#### 📝 邮件列表

1. **[09-21 19:35]** [PATCH v7 00/10] mlx5 support for VFIO self test
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
2. **[09-21 19:35]** [PATCH v7 01/10] net/mlx5: Add IFC structures for CQE and WQE
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
3. **[09-21 19:35]** [PATCH v7 02/10] net/mlx5: Move HW constant groups from device.h/cq.h to mlx5_ifc.h
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
4. **[09-21 19:35]** [PATCH v7 03/10] net/mlx5: Extract MLX5_SET/GET macros into mlx5_ifc_macros.h
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
5. **[09-21 19:35]** [PATCH v7 04/10] net/mlx5: Add ONCE and MMIO accessor variants to mlx5_ifc_macros.h
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
6. **[09-21 19:35]** [PATCH v7 05/10] selftests: Add additional kernel functions to tools/include/
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
7. **[09-21 19:35]** [PATCH v7 06/10] vfio: selftests: Allow drivers to specify required region size
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
8. **[09-21 19:35]** [PATCH v7 07/10] vfio: selftests: Add dev_dbg
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
9. **[09-21 19:35]** [PATCH v7 08/10] vfio: selftests: Add mlx5 driver - HW init and command interface
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
10. **[09-21 19:35]** [PATCH v7 09/10] vfio: selftests: Add mlx5 driver - data path and memcpy ops
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
11. **[09-21 19:35]** [PATCH v7 10/10] vfio: selftests: mlx5 driver - add send_msi support
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
12. **[09-22 22:38]** Re: [PATCH v7 05/10] selftests: Add additional kernel functions to
 tools/include/
   - 发件人: sashiko-bot@kernel.org
13. **[09-22 22:38]** Re: [PATCH v7 04/10] net/mlx5: Add ONCE and MMIO accessor variants
 to mlx5_ifc_macros.h
   - 发件人: sashiko-bot@kernel.org
14. **[09-22 22:38]** Re: [PATCH v7 01/10] net/mlx5: Add IFC structures for CQE and WQE
   - 发件人: sashiko-bot@kernel.org
15. **[09-22 22:38]** Re: [PATCH v7 02/10] net/mlx5: Move HW constant groups from
 device.h/cq.h to mlx5_ifc.h
   - 发件人: sashiko-bot@kernel.org
16. **[09-22 22:38]** Re: [PATCH v7 06/10] vfio: selftests: Allow drivers to specify
 required region size
   - 发件人: sashiko-bot@kernel.org
17. **[09-22 22:38]** Re: [PATCH v7 03/10] net/mlx5: Extract MLX5_SET/GET macros into
 mlx5_ifc_macros.h
   - 发件人: sashiko-bot@kernel.org
18. **[09-22 22:38]** Re: [PATCH v7 07/10] vfio: selftests: Add dev_dbg
   - 发件人: sashiko-bot@kernel.org
19. **[09-22 22:38]** Re: [PATCH v7 08/10] vfio: selftests: Add mlx5 driver - HW init and
 command interface
   - 发件人: sashiko-bot@kernel.org
20. **[09-22 22:38]** Re: [PATCH v7 09/10] vfio: selftests: Add mlx5 driver - data path
 and memcpy ops
   - 发件人: sashiko-bot@kernel.org
21. **[09-22 22:38]** Re: [PATCH v7 10/10] vfio: selftests: mlx5 driver - add send_msi
 support
   - 发件人: sashiko-bot@kernel.org
22. **[09-23 18:26]** Re: [PATCH v7 06/10] vfio: selftests: Allow drivers to specify
 required region size
   - 发件人: David Matlack <dmatlack@google.com>
23. **[09-23 18:30]** Re: [PATCH v7 00/10] mlx5 support for VFIO self test
   - 发件人: David Matlack <dmatlack@google.com>
24. **[09-23 15:42]** Re: [PATCH v7 06/10] vfio: selftests: Allow drivers to specify
 required region size
   - 发件人: Sean Christopherson <seanjc@google.com>
25. **[09-24 06:56]** Re: [PATCH v7 00/10] mlx5 support for VFIO self test
   - 发件人: Alex Williamson <alex@shazbot.org>

---

### Thread 12: [PATCH v20 00/22] KVM: arm64: CCA: Add basic plumbing for Realms

**📧 邮件数**: 24 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 24 Sep 2026 17:04:42 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:24, 29291 tokens)

#### 📝 邮件列表

1. **[09-24 17:04]** [PATCH v20 00/22] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-24 17:04]** [PATCH v20 01/22] KVM: arm64: protected VM: Handle user writes to CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-24 17:04]** [PATCH v20 02/22] KVM: arm64: Disable Steal time accounting for protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-24 17:04]** [PATCH v20 03/22] KVM: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[09-24 17:04]** [PATCH v20 04/22] KVM: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-24 17:04]** [PATCH v20 05/22] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-24 17:04]** [PATCH v20 06/22] KVM: arm64: Don't call vcpu_set_pauth_traps for pKVM host
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-24 17:04]** [PATCH v20 07/22] KVM: arm64: Refactor the vcpu_load to allow for VM specific callbacks
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-24 17:04]** [PATCH v20 08/22] KVM: arm64: Add vcpu load/put call backs for flavors
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[09-24 17:04]** [PATCH v20 09/22] KVM: arm64: Reuse kvm_stage2_unmap_range in kvm_unmap_gfn_range
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[09-24 17:04]** [PATCH v20 10/22] KVM: arm64: Add VM specific callback for S2 MMU operations
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[09-24 17:04]** [PATCH v20 11/22] KVM: arm64: Use a local kvm pointer in kvm_handle_guest_abort()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[09-24 17:04]** [PATCH v20 12/22] KVM: arm64: Abstract out memory abort handling
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
14. **[09-24 17:04]** [PATCH v20 13/22] KVM: arm64: Mandate VGIC v3 for pKVM VMs and Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[09-24 17:04]** [PATCH v20 14/22] KVM: arm64: CCA: Add a new mode for supporting Realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[09-24 17:04]** [PATCH v20 15/22] KVM: arm64: CCA: Add VCPU load/put for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-24 17:04]** [PATCH v20 16/22] KVM: arm64: CCA: Add bare minimal S2 operations for Realm
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-24 17:04]** [PATCH v20 17/22] KVM: arm64: CCA: Introduce Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-24 17:05]** [PATCH v20 18/22] KVM: arm64: CCA: Don't expose unsupported capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-24 17:05]** [PATCH v20 19/22] KVM: arm64: CCA: WARN on injected undef exceptions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-24 17:05]** [PATCH v20 20/22] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-24 17:05]** [PATCH v20 21/22] KVM: arm64: CCA: Expose SVE VL register before VCPU finalization
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
23. **[09-24 17:05]** [PATCH v20 22/22] KVM: arm64: CCA: Control user register access for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
24. **[09-24 16:25]** Re: [PATCH v20 18/22] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: sashiko-bot@kernel.org

---

### Thread 13: [PATCH 1/2] KVM: arm64: Report SMCCC_VERSION and SMCCC_ARCH_FEATURES as implemented

**📧 邮件数**: 19 | **👥 参与者**: 8 | **📅 开始时间**: Mon, 14 Sep 2026 13:58:26 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:4 新:15, 5679 tokens)

#### 📝 邮件列表

1. **[09-14 13:58]** [PATCH 1/2] KVM: arm64: Report SMCCC_VERSION and SMCCC_ARCH_FEATURES as implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-18 16:18]** [PATCH 0/2] Batch register access for live migration optimization
   - 发件人: Yize Wang <wangyize7@huawei.com>
3. **[09-18 13:08]** Re: [PATCH 0/2] Batch register access for live migration optimization
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[09-20 20:12]** Re: [RESEND][PATCH 0/2] Batch register access for live migration
 optimization
   - 发件人: Yize Wang <wangyize7@huawei.com>
5. **[09-21 17:20]** [PATCH 1/2] KVM: arm64: pvtime: Don't lose stolen time on failed
 updates
   - 发件人: Hao Zhang <hao_zhang_kdev@163.com>
6. **[09-21 17:27]** [PATCH 2/2] KVM: selftests: Test arm64 stolen time after failed
 updates
   - 发件人: Hao Zhang <hao_zhang_kdev@163.com>
7. **[09-21 16:47]** [PATCH 0/2] KVM: arm64: Support FFA_FN64_MEM_RECLAIM2 in host handler
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
8. **[09-21 16:47]** [PATCH 1/2] firmware: arm_ffa: Add FFA_FN64_MEM_RECLAIM2 function ID
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
9. **[09-21 16:47]** [PATCH 2/2] KVM: arm64: Support FFA_FN64_MEM_RECLAIM2 in host handler
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
10. **[09-21 16:58]** Re: [PATCH 1/2] firmware: arm_ffa: Add FFA_FN64_MEM_RECLAIM2
 function ID
   - 发件人: sashiko-bot@kernel.org
11. **[09-21 16:59]** Re: [PATCH 2/2] KVM: arm64: Support FFA_FN64_MEM_RECLAIM2 in host
 handler
   - 发件人: sashiko-bot@kernel.org
12. **[09-22 11:07]** Re: [PATCH 2/2] KVM: arm64: Support FFA_FN64_MEM_RECLAIM2 in host
 handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[09-22 11:16]** Re: [PATCH 1/2] firmware: arm_ffa: Add FFA_FN64_MEM_RECLAIM2 function ID
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
14. **[09-22 11:16]** Re: [PATCH 2/2] KVM: arm64: Support FFA_FN64_MEM_RECLAIM2 in host handler
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
15. **[09-22 13:15]** Re: [PATCH 1/2] firmware: arm_ffa: Add FFA_FN64_MEM_RECLAIM2
 function ID
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
16. **[09-23 15:57]** Re: [RESEND][PATCH 0/2] Batch register access for live migration
 optimization
   - 发件人: Yize Wang <wangyize7@huawei.com>
17. **[09-23 08:38]** Re: [PATCH 1/2] firmware: arm_ffa: Add FFA_FN64_MEM_RECLAIM2 function ID
   - 发件人: Snehal Koukuntla <snehalreddy@google.com>
18. **[09-24 19:23]** Re: [PATCH 1/2] KVM: arm64: pvtime: Don't lose stolen time on failed updates
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[09-27 17:35]** Re: [PATCH 1/2] KVM: arm64: Report SMCCC_VERSION and SMCCC_ARCH_FEATURES as implemented
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 14: [PATCH v3 00/18] KVM: arm64: Confine protected VM vCPU state to EL2

**📧 邮件数**: 19 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 14 Sep 2026 12:33:20 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:8 新:11, 5104 tokens)

#### 📝 邮件列表

1. **[09-14 12:33]** [PATCH v3 00/18] KVM: arm64: Confine protected VM vCPU state to EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 12:33]** [PATCH v3 04/18] KVM: arm64: Disable steal time for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-14 12:33]** [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-14 12:33]** [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-16 17:30]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-16 20:07]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-17 09:06]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[09-18 14:21]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Will Deacon <will@kernel.org>
9. **[09-22 15:34]** Re: [PATCH v3 04/18] KVM: arm64: Disable steal time for protected VMs
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
10. **[09-22 17:35]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
11. **[09-22 17:37]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
12. **[09-22 18:07]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
13. **[09-23 10:51]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
14. **[09-24 09:30]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Will Deacon <will@kernel.org>
15. **[09-24 12:26]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
16. **[09-24 13:14]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Will Deacon <will@kernel.org>
17. **[09-24 16:21]** Re: [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs
 at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[09-27 09:20]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[09-27 13:37]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 15: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers

**📧 邮件数**: 19 | **👥 参与者**: 4 | **📅 开始时间**: Fri, 18 Sep 2026 16:16:46 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:7 新:12, 3131 tokens)

#### 📝 邮件列表

1. **[09-18 16:16]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[09-18 17:23]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
3. **[09-18 12:36]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
4. **[09-18 17:39]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
5. **[09-18 17:52]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
6. **[09-18 13:53]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
7. **[09-18 13:57]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
8. **[09-21 12:27]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
9. **[09-21 11:07]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
10. **[09-21 08:51]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
11. **[09-21 14:05]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
12. **[09-21 09:17]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
13. **[09-21 14:24]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
14. **[09-21 09:37]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
15. **[09-21 20:56]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
16. **[09-22 16:38]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
17. **[09-23 10:31]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment
 for shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
18. **[09-23 10:35]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
19. **[09-23 12:58]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>

---

### Thread 16: [PATCH 0/3] KVM: arm64: timers: Program CVAL from the current count when the hardware won't apply the offset

**📧 邮件数**: 15 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 21 Sep 2026 15:04:24 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:15, 7908 tokens)

#### 📝 邮件列表

1. **[09-21 15:04]** [PATCH 0/3] KVM: arm64: timers: Program CVAL from the current count when the hardware won't apply the offset
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-21 15:04]** [PATCH 1/3] KVM: arm64: timers: Compute an offset-applied CVAL from the current count
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-21 15:04]** [PATCH 2/3] KVM: arm64: nv: Read a guest hypervisor's CNTV_CVAL_EL0 from memory on x1e
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-21 15:04]** [PATCH 3/3] KVM: arm64: selftests: Test a timer set past the counter's wrap
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-21 14:17]** Re: [PATCH 3/3] KVM: arm64: selftests: Test a timer set past the
 counter's wrap
   - 发件人: sashiko-bot@kernel.org
6. **[09-21 16:25]** Re: [PATCH 3/3] KVM: arm64: selftests: Test a timer set past the
 counter's wrap
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-22 22:42]** [PATCH 0/3] KVM: arm64: vgic-v3: Make LPI disabling robust
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[09-22 22:42]** [PATCH 1/3] KVM: arm64: vgic: Allow last_lr_irq to be NULL when LRs are not overflowing
   - 发件人: Marc Zyngier <maz@kernel.org>
9. **[09-22 22:42]** [PATCH 2/3] KVM: arm64: vgic: Take a refcount on IRQs referenced by last_lr_irq
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[09-22 22:42]** [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
11. **[09-22 22:01]** Re: [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: sashiko-bot@kernel.org
12. **[09-23 00:21]** Re: [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[09-23 09:41]** Re: [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[09-23 18:56]** Re: [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[09-23 11:21]** Re: [PATCH 3/3] KVM: arm64: vgic: Stop the VM when disabling LPIs
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 17: [PATCH v1 0/6] Fix guest_memfd and protected VMs on systems with
 pages larger than 4K

**📧 邮件数**: 14 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 22 Sep 2026 14:08:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:14, 8059 tokens)

#### 📝 邮件列表

1. **[09-22 14:08]** [PATCH v1 0/6] Fix guest_memfd and protected VMs on systems with
 pages larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-22 14:08]** [PATCH v1 1/6] KVM: arm64: Fix MMFR0 TGRAN advertisement for pVMs
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[09-22 14:08]** [PATCH v1 2/6] KVM: arm64: Pass kvm_s2_fault_desc to fault_supports_stage2_huge_mapping()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[09-22 14:08]** [PATCH v1 3/6] KVM: arm64: Move pkvm_mem_abort()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[09-22 14:08]** [PATCH v1 4/6] KVM: arm64: Move gmem_abort()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[09-22 14:08]** [PATCH v1 5/6] KVM: arm64: Use kvm_s2_fault_vma_info in gmem_abort()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
7. **[09-22 14:08]** [PATCH v1 6/6] KVM: arm64: Use kvm_s2_fault_vma_info in pkvm_mem_abort()
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
8. **[09-23 20:33]** Re: [PATCH v1 2/6] KVM: arm64: Pass kvm_s2_fault_desc to fault_supports_stage2_huge_mapping()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[09-23 20:38]** Re: [PATCH v1 3/6] KVM: arm64: Move pkvm_mem_abort()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[09-23 20:39]** Re: [PATCH v1 6/6] KVM: arm64: Use kvm_s2_fault_vma_info in pkvm_mem_abort()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[09-25 18:36]** Re: [PATCH v1 5/6] KVM: arm64: Use kvm_s2_fault_vma_info in
 gmem_abort()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
12. **[09-25 18:46]** Re: [PATCH v1 2/6] KVM: arm64: Pass kvm_s2_fault_desc to
 fault_supports_stage2_huge_mapping()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
13. **[09-27 17:30]** Re: [PATCH v1 5/6] KVM: arm64: Use kvm_s2_fault_vma_info in gmem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[09-27 17:31]** Re: [PATCH v1 3/6] KVM: arm64: Move pkvm_mem_abort()
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 18: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)

**📧 邮件数**: 14 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 13 Sep 2026 08:04:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:4 新:10, 3505 tokens)

#### 📝 邮件列表

1. **[09-13 08:04]** [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-16 17:39]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[09-17 10:03]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-17 11:36]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[09-22 09:16]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-22 14:21]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-22 15:49]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
8. **[09-22 16:14]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-22 18:15]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Will Deacon <will@kernel.org>
10. **[09-23 12:06]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
11. **[09-23 16:45]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Will Deacon <will@kernel.org>
12. **[09-23 17:04]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[09-24 16:43]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
14. **[09-25 18:07]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 19: [PATCH v11 00/21] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 14 | **👥 参与者**: 3 | **📅 开始时间**: Sun, 20 Sep 2026 20:15:41 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:6 新:8, 2405 tokens)

#### 📝 邮件列表

1. **[09-20 20:15]** [PATCH v11 00/21] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[09-20 20:15]** [PATCH v11 08/21] Revert "KVM: arm64: PMU: Reload when resetting"
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[09-20 20:15]** [PATCH v11 09/21] KVM: arm64: PMU: Recreate events after MDCR_EL2
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[09-20 20:16]** [PATCH v11 19/21] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[09-20 20:16]** [PATCH v11 20/21] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[09-20 11:40]** Re: [PATCH v11 19/21] KVM: arm64: PMU: Implement
 fixed-counters-only emulation
   - 发件人: sashiko-bot@kernel.org
7. **[09-22 14:59]** Re: [PATCH v11 19/21] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[09-21 23:43]** Re: [PATCH v11 08/21] Revert "KVM: arm64: PMU: Reload when resetting"
   - 发件人: Oliver Upton <oupton@kernel.org>
9. **[09-21 23:54]** Re: [PATCH v11 09/21] KVM: arm64: PMU: Recreate events after
 MDCR_EL2 changes
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[09-22 16:05]** Re: [PATCH v11 08/21] Revert "KVM: arm64: PMU: Reload when resetting"
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
11. **[09-22 00:11]** Re: [PATCH v11 20/21] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[09-22 00:13]** Re: [PATCH v11 19/21] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[09-22 17:51]** Re: [PATCH v11 09/21] KVM: arm64: PMU: Recreate events after MDCR_EL2
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
14. **[09-22 18:13]** Re: [PATCH v11 20/21] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>

---

### Thread 20: [PATCH v2 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable

**📧 邮件数**: 12 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 18 Sep 2026 12:02:13 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:9, 9177 tokens)

#### 📝 邮件列表

1. **[09-18 12:02]** [PATCH v2 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable
   - 发件人: zjamg <ndaugoing@gmail.com>
2. **[09-20 09:49]** [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
3. **[09-21 00:47]** Re: [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[09-22 18:16]** Re: [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
5. **[09-22 18:16]** [PATCH] KVM: selftests: arm64: Add test for cross-vCPU LPI disable race
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
6. **[09-22 10:29]** Re: [PATCH] KVM: selftests: arm64: Add test for cross-vCPU LPI
 disable race
   - 发件人: sashiko-bot@kernel.org
7. **[09-22 18:53]** Re: [PATCH] KVM: selftests: arm64: Add test for cross-vCPU LPI disable race
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
8. **[09-22 18:53]** [PATCH v2] KVM: selftests: arm64: Add test for cross-vCPU LPI disable race
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
9. **[09-22 11:03]** Re: [PATCH v2] KVM: selftests: arm64: Add test for cross-vCPU LPI
 disable race
   - 发件人: sashiko-bot@kernel.org
10. **[09-22 19:24]** Re: [PATCH v2] KVM: selftests: arm64: Add test for cross-vCPU LPI
 disable race
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
11. **[09-22 18:05]** Re: [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[09-22 18:08]** Re: [PATCH v2] KVM: selftests: arm64: Add test for cross-vCPU LPI disable race
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 21: [PATCH v1 0/4] KVM: arm64: Fix HCR_EL2 for non-protected VMs in pKVM

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 25 Sep 2026 10:06:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:9, 6132 tokens)

#### 📝 邮件列表

1. **[09-25 10:06]** [PATCH v1 0/4] KVM: arm64: Fix HCR_EL2 for non-protected VMs in pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-25 10:06]** [PATCH v1 1/4] KVM: arm64: Don't WARN on an unsupported TLBI OS from vEL1
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-25 10:06]** [PATCH v1 2/4] KVM: arm64: Clear HCR_EL2.RW for 32-bit non-protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-25 10:06]** [PATCH v1 3/4] KVM: arm64: Use the host's HCR_EL2 for non-protected VMs in pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-25 10:06]** [PATCH v1 4/4] KVM: arm64: selftests: Check a feature hidden in an ID register is UNDEF
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-25 16:01]** Re: [PATCH v1 2/4] KVM: arm64: Clear HCR_EL2.RW for 32-bit non-protected vCPUs
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[09-25 16:21]** Re: [PATCH v1 2/4] KVM: arm64: Clear HCR_EL2.RW for 32-bit
 non-protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[09-25 17:33]** Re: [PATCH v1 1/4] KVM: arm64: Don't WARN on an unsupported TLBI OS
 from vEL1
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[09-27 10:15]** Re: [PATCH v1 3/4] KVM: arm64: Use the host's HCR_EL2 for non-protected VMs in pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 22: [PATCH v2 0/2] KVM: arm64: Fix a vSError staying pending after delivery under pKVM

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 21 Sep 2026 11:10:28 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:9, 3202 tokens)

#### 📝 邮件列表

1. **[09-21 11:10]** [PATCH v2 0/2] KVM: arm64: Fix a vSError staying pending after delivery under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-21 11:10]** [PATCH v2 1/2] KVM: arm64: Sync HCR_EL2.VSE back to the host vCPU under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-21 11:10]** [PATCH v2 2/2] KVM: arm64: selftests: Check SError is not pending after delivery
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-22 08:19]** [PATCH v2 0/2] KVM: selftests: Fix incremental build dependencies
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-22 08:19]** [PATCH v2 1/2] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-22 08:19]** [PATCH v2 2/2] selftests/cgroup: Make the object directory an order-only prerequisite
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-22 15:44]** Re: [PATCH v2 2/2] selftests/cgroup: Make the object directory an
 order-only prerequisite
   - 发件人: Michal =?utf-8?Q?Koutn=C3=BD?= <mkoutny@suse.com>
8. **[09-24 09:32]** Re: [PATCH v2 1/2] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Sean Christopherson <seanjc@google.com>
9. **[09-24 19:18]** Re: [PATCH v2 1/2] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 23: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL

**📧 邮件数**: 9 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 14 Sep 2026 15:57:20 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:6 新:3, 979 tokens)

#### 📝 邮件列表

1. **[09-14 15:57]** [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-14 18:08]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit,
 eliminate VM_SPECIAL
   - 发件人: Andrew Morton <akpm@linux-foundation.org>
3. **[09-18 22:20]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
4. **[09-18 13:31]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate VM_SPECIAL
   - 发件人: Suren Baghdasaryan <surenb@google.com>
5. **[09-19 16:05]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-19 16:09]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-23 09:13]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-23 10:39]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
9. **[09-23 07:31]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate VM_SPECIAL
   - 发件人: Suren Baghdasaryan <surenb@google.com>

---

### Thread 24: [PATCH] MAINTAINERS: name the kvmarm/kvmarm next branch

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 24 Sep 2026 11:35:36 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:7, 4660 tokens)

#### 📝 邮件列表

1. **[09-24 11:35]** [PATCH] MAINTAINERS: name the kvmarm/kvmarm next branch
   - 发件人: Matthias Goergens <matthias.goergens@gmail.com>
2. **[09-24 07:59]** Re: [PATCH] MAINTAINERS: name the kvmarm/kvmarm next branch
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[09-24 16:30]** Re: [PATCH] MAINTAINERS: name the kvmarm/kvmarm next branch
   - 发件人: Matthias Goergens <matthias.goergens@gmail.com>
4. **[09-24 14:33]** Re: [PATCH] MAINTAINERS: name the kvmarm/kvmarm next branch
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[09-25 16:56]** [RFC PATCH] Documentation/process: Add a maintainer entry profile for KVM/arm64
   - 发件人: Matthias Goergens <matthias.goergens@gmail.com>
6. **[09-25 08:58]** Re: [RFC PATCH] Documentation/process: Add a maintainer entry
 profile for KVM/arm64
   - 发件人: sashiko-bot@kernel.org
7. **[09-27 11:22]** Re: [RFC PATCH] Documentation/process: Add a maintainer entry profile for KVM/arm64
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 25: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support

**📧 邮件数**: 7 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 14 Sep 2026 13:26:11 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:6, 1868 tokens)

#### 📝 邮件列表

1. **[09-14 13:26]** [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-22 15:28]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
3. **[09-22 13:52]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-22 18:37]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
5. **[09-22 14:53]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-22 19:52]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
7. **[09-22 15:26]** Re: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 26: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 21 Sep 2026 07:37:18 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:7, 2247 tokens)

#### 📝 邮件列表

1. **[09-21 07:37]** [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-21 00:09]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[09-21 08:24]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-21 12:42]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-21 14:34]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-21 11:39]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[09-22 08:31]** Re: [PATCH v2] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 27: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2

**📧 邮件数**: 6 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 22 Sep 2026 19:14:30 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:6, 1819 tokens)

#### 📝 邮件列表

1. **[09-22 19:14]** [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-22 12:47]** Re: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[09-22 22:09]** Re: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-22 15:31]** Re: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Oliver Upton <oupton@kernel.org>
5. **[09-23 12:07]** Re: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>
6. **[09-23 14:00]** Re: [PATCH v1] arm64/boot: Disable trapping of PMZR_EL0 writes to EL2
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 28: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Fri, 11 Sep 2026 11:47:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:2, 865 tokens)

#### 📝 邮件列表

1. **[09-11 11:47]** [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-13 11:00]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[09-15 19:51]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-24 11:21]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is
 implemented
   - 发件人: Will Deacon <will@kernel.org>
5. **[09-24 11:27]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 29: [PATCH v3 0/4] irqchip/gic-v4, KVM: arm64: Fix the vgic init error paths

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 21 Sep 2026 08:29:54 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:5, 3241 tokens)

#### 📝 邮件列表

1. **[09-21 08:29]** [PATCH v3 0/4] irqchip/gic-v4, KVM: arm64: Fix the vgic init error paths
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-21 08:29]** [PATCH v3 1/4] irqchip/gic-v4: Clear the domain and fwnode pointers after freeing them
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-21 08:29]** [PATCH v3 2/4] irqchip/gic-v4: Unwind what its_alloc_vcpu_irqs() allocated on failure
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-21 08:29]** [PATCH v3 3/4] KVM: arm64: vgic: Tear down what vgic_init() created when it fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-21 08:29]** [PATCH v3 4/4] KVM: arm64: vgic-v4: Restore nr_vpes before freeing the vPE resources
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 30: [PATCH] KVM: arm64: Remove PAGE_SIZE alignment for hyp event ELF sections

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 24 Sep 2026 10:51:54 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:4, 803 tokens)

#### 📝 邮件列表

1. **[09-24 10:51]** [PATCH] KVM: arm64: Remove PAGE_SIZE alignment for hyp event ELF sections
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-24 17:14]** Re: [PATCH] KVM: arm64: Remove PAGE_SIZE alignment for hyp event ELF sections
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-27 09:40]** Re: [PATCH] KVM: arm64: Remove PAGE_SIZE alignment for hyp event ELF sections
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[09-27 17:35]** Re: [PATCH] KVM: arm64: Remove PAGE_SIZE alignment for hyp event ELF sections
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 31: [PATCH v2 00/22] Huge mapping support for protected VMs

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 11 Sep 2026 14:50:31 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:2, 706 tokens)

#### 📝 邮件列表

1. **[09-11 14:50]** [PATCH v2 00/22] Huge mapping support for protected VMs
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-11 14:50]** [PATCH v2 01/22] KVM: arm64: Prefault host stage-2 entries on block split
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[09-24 17:38]** Re: [PATCH v2 01/22] KVM: arm64: Prefault host stage-2 entries on
 block split
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[09-25 16:02]** Re: [PATCH v2 01/22] KVM: arm64: Prefault host stage-2 entries on
 block split
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 32: [PATCH v4 0/2] KVM: arm64: ptdump: Shadow ptdump fixes

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 24 Sep 2026 10:49:49 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:4, 3478 tokens)

#### 📝 邮件列表

1. **[09-24 10:49]** [PATCH v4 0/2] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[09-24 10:49]** [PATCH v4 1/2] KVM: arm64: ptdump: Check the page tables aren't freed when accessing
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[09-24 10:49]** [PATCH v4 2/2] KVM: arm64: ptdump: Fix shadow ptdump sleep-in-atomic-context problem
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[09-24 21:41]** Re: [PATCH v4 0/2] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 33: [PATCH v2] arm64: clear_page[s] using memset

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 16 Sep 2026 12:03:56 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:1, 730 tokens)

#### 📝 邮件列表

1. **[09-16 12:03]** [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Linus Walleij <linusw@kernel.org>
2. **[09-16 16:28]** Re: [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[09-16 16:54]** Re: [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[09-23 17:14]** Re: [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 34: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 15 Sep 2026 17:01:18 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:2, 632 tokens)

#### 📝 邮件列表

1. **[09-15 17:01]** [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-16 13:23]** Re: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
3. **[09-22 14:52]** Re: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
4. **[09-23 08:32]** Re: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>

---

### Thread 35: [PATCH v5 00/15] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 10 Sep 2026 19:34:53 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 647 tokens)

#### 📝 邮件列表

1. **[09-10 19:34]** [PATCH v5 00/15] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[09-10 19:35]** [PATCH v5 11/15] coco: host: arm64: Connect RMM pdev streams for IDE devices
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[09-26 11:33]** Re: [PATCH v5 11/15] coco: host: arm64: Connect RMM pdev streams for
 IDE devices
   - 发件人: Ankit Agrawal <ankita@nvidia.com>

---

### Thread 36: [PATCH 0/7] KVM: arm64: pKVM host hypercall and GICv5 CPU interface fixes

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 15 Sep 2026 13:38:39 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 620 tokens)

#### 📝 邮件列表

1. **[09-15 13:38]** [PATCH 0/7] KVM: arm64: pKVM host hypercall and GICv5 CPU interface fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-15 13:38]** [PATCH 6/7] KVM: arm64: vgic: Do not access the GICv5 CPU interface from EL1
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-22 08:38]** Re: [PATCH 6/7] KVM: arm64: vgic: Do not access the GICv5 CPU interface from EL1
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 37: [PATCH] KVM: selftests: Fix arm64 sysreg header dependencies

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 21 Sep 2026 08:10:23 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 340 tokens)

#### 📝 邮件列表

1. **[09-21 08:10]** Re: [PATCH] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-21 13:20]** Re: [PATCH] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[09-22 08:09]** Re: [PATCH] KVM: selftests: Fix arm64 sysreg header dependencies
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 38: [PATCH kvmtool 0/7] Fix --vcpu-affinity

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 17 Sep 2026 16:49:25 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 393 tokens)

#### 📝 邮件列表

1. **[09-17 16:49]** [PATCH kvmtool 0/7] Fix --vcpu-affinity
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[09-18 13:22]** Re: [PATCH kvmtool 0/7] Fix --vcpu-affinity
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[09-21 09:59]** Re: [PATCH kvmtool 0/7] Fix --vcpu-affinity
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 39: [PATCH v8 00/29] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 3 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 18 Sep 2026 15:30:37 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 485 tokens)

#### 📝 邮件列表

1. **[09-18 15:30]** [PATCH v8 00/29] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[09-18 15:30]** [PATCH v8 08/29] KVM: Move architecture capability Kconfigs to header defines
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[09-21 09:09]** Re: [PATCH v8 08/29] KVM: Move architecture capability Kconfigs to
 header defines
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 40: [PATCH] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 18 Sep 2026 13:05:53 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 668 tokens)

#### 📝 邮件列表

1. **[09-18 13:05]** [PATCH] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-18 17:10]** Re: [PATCH] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-21 07:03]** Re: [PATCH] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 41: [PATCH v2] KVM: arm64: Disable stage-2 ptdump of pKVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 24 Sep 2026 11:04:59 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 509 tokens)

#### 📝 邮件列表

1. **[09-24 11:04]** [PATCH v2] KVM: arm64: Disable stage-2 ptdump of pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-27 17:35]** Re: [PATCH v2] KVM: arm64: Disable stage-2 ptdump of pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 42: [PATCH v4] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 24 Sep 2026 17:53:29 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 1549 tokens)

#### 📝 邮件列表

1. **[09-24 17:53]** [PATCH v4] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-25 10:22]** Re: [PATCH v4] KVM: arm64: Trap guest MPAM accesses whenever MPAM is
 implemented
   - 发件人: Ben Horgan <ben.horgan@arm.com>

---

### Thread 43: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 15 Sep 2026 16:42:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 527 tokens)

#### 📝 邮件列表

1. **[09-15 16:42]** [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[09-24 21:41]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 44: [PATCH v3] KVM: arm64: Clear the VM's feature bitmap when kvm_setup_vcpu() fails

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 21 Sep 2026 20:08:43 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 1366 tokens)

#### 📝 邮件列表

1. **[09-21 20:08]** [PATCH v3] KVM: arm64: Clear the VM's feature bitmap when kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-22 17:01]** Re: [PATCH v3] KVM: arm64: Clear the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 45: [PATCH v4 0/5] Stop returning struct page from guest_memfd PFN lookup

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 24 Sep 2026 14:51:51 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 281 tokens)

#### 📝 邮件列表

1. **[09-24 14:51]** Re: [PATCH v4 0/5] Stop returning struct page from guest_memfd PFN lookup
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 46: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 24 Sep 2026 16:10:46 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 299 tokens)

#### 📝 邮件列表

1. **[09-24 16:10]** Re: [PATCH 35/60] kvm: Add VCPU plane-scheduling state and helpers
   - 发件人: =?utf-8?B?SsO2cmcgUsO2ZGVs?= <joro@8bytes.org>

---

### Thread 47: [PATCH] KVM: arm64: Use consistent type for pool size

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 22 Sep 2026 15:35:38 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 136 tokens)

#### 📝 邮件列表

1. **[09-22 15:35]** Re: [PATCH] KVM: arm64: Use consistent type for pool size
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 48: [PATCH v2 00/20] KVM: selftests: PPC pre-enabling

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 21 Sep 2026 07:05:44 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 892 tokens)

#### 📝 邮件列表

1. **[09-21 07:05]** Re: [PATCH v2 00/20] KVM: selftests: PPC pre-enabling
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 49: [PATCH v2] KVM: selftests: Replace ulong with unsigned long

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 21 Sep 2026 07:05:34 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 133 tokens)

#### 📝 邮件列表

1. **[09-21 07:05]** Re: [PATCH v2] KVM: selftests: Replace ulong with unsigned long
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 50: [PATCH] KVM: Never clear KVM_REQ_VM_DEAD from a vCPU's requests

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 21 Sep 2026 07:05:02 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 137 tokens)

#### 📝 邮件列表

1. **[09-21 07:05]** Re: [PATCH] KVM: Never clear KVM_REQ_VM_DEAD from a vCPU's requests
   - 发件人: Sean Christopherson <seanjc@google.com>

---

## 📌 RFC

共 7 个 thread

---

### Thread 1: [RFC PATCH v7 00/13] coco: guest: Add a shared-granule allocator for host-shared memory

**📧 邮件数**: 39 | **👥 参与者**: 9 | **📅 开始时间**: Mon, 21 Sep 2026 20:18:34 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:39, 36082 tokens)

#### 📝 邮件列表

1. **[09-21 20:18]** [RFC PATCH v7 00/13] coco: guest: Add a shared-granule allocator for host-shared memory
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[09-21 20:18]** [RFC PATCH v7 01/13] arm64: realm: Add RHI helper to query IPA state change alignment
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[09-21 20:18]** [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[09-21 20:18]** [RFC PATCH v7 03/13] arm64: realm: Expose the CCA shared granule size through mem_encrypt ops
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[09-21 20:18]** [RFC PATCH v7 04/13] irqchip/gic-v3-its: Resolve the default NUMA node explicitly
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[09-21 20:18]** [RFC PATCH v7 05/13] irqchip/gic-v3-its: Allocate shared tables using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[09-21 20:18]** [RFC PATCH v7 06/13] dma-contiguous: Accept an explicit minimum alignment
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[09-21 20:18]** [RFC PATCH v7 07/13] dma-pool: Allocate CoCo atomic pools using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[09-21 20:18]** [RFC PATCH v7 08/13] dma-direct: Align CoCo shared DMA allocations to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[09-21 20:18]** [RFC PATCH v7 09/13] swiotlb: Align shared IO TLB pools to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[09-21 20:18]** [RFC PATCH v7 10/13] swiotlb: Reject misaligned restricted DMA pools for CoCo guests
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[09-21 20:18]** [RFC PATCH v7 11/13] dma-buf: system_heap: Limit scatterlist entries to the buffer size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
13. **[09-21 20:18]** [RFC PATCH v7 12/13] dma-buf: system_heap: Allocate shared buffers using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
14. **[09-21 20:18]** [RFC PATCH v7 13/13] swiotlb: Make rounded shared pool capacity allocatable
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
15. **[09-22 17:25]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
16. **[09-22 17:39]** Re: [RFC PATCH v7 12/13] dma-buf: system_heap: Allocate shared
 buffers using CoCo shared memory allocator
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
17. **[09-22 13:51]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
18. **[09-23 01:33]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-23 11:23]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
20. **[09-23 14:01]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
21. **[09-23 14:02]** Re: [RFC PATCH v7 12/13] dma-buf: system_heap: Allocate shared
 buffers using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
22. **[09-23 10:46]** Re: [RFC PATCH v7 12/13] dma-buf: system_heap: Allocate shared
 buffers using CoCo shared memory allocator
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
23. **[09-23 10:42]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
24. **[09-23 15:29]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
25. **[09-23 11:10]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
26. **[09-23 15:58]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
27. **[09-23 11:35]** Re: [RFC PATCH v7 06/13] dma-contiguous: Accept an explicit minimum
 alignment
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
28. **[09-23 11:40]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
29. **[09-23 17:19]** Re: [RFC PATCH v7 06/13] dma-contiguous: Accept an explicit minimum
 alignment
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
30. **[09-23 10:00]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
31. **[09-23 10:06]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
32. **[09-23 14:49]** Re: [RFC PATCH v7 06/13] dma-contiguous: Accept an explicit minimum
 alignment
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
33. **[09-23 20:28]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
34. **[09-23 16:11]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
35. **[09-23 15:20]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Mostafa Saleh <smostafa@google.com>
36. **[09-23 12:21]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
37. **[09-23 09:28]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Kameron Carr <kameroncarr@linux.microsoft.com>
38. **[09-23 14:23]** Re: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
39. **[09-23 18:36]** RE: [RFC PATCH v7 02/13] mm: Add an allocator for CoCo shared memory
   - 发件人: Michael Kelley <mhklinux@outlook.com>

---

### Thread 2: [RFC PATCH v4 00/25] named CPU models for Arm64 on KVM

**📧 邮件数**: 36 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 21 Sep 2026 12:32:24 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:36, 38908 tokens)

#### 📝 邮件列表

1. **[09-21 12:32]** [RFC PATCH v4 00/25] named CPU models for Arm64 on KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
2. **[09-21 12:32]** [RFC PATCH v4 01/25] target/arm: expose SYSREG_ props for REVIDR_EL1 and AIDR_EL1
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
3. **[09-21 12:32]** [RFC PATCH v4 02/25] target/arm: expose all non-res ID reg fields as properties
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
4. **[09-21 12:32]** [RFC PATCH v4 03/25] target/arm: move SYSREG_ prop infra to cpu64.c
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
5. **[09-21 12:32]** [RFC PATCH v4 04/25] target/arm/kvm: enable writable implementation ID registers
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
6. **[09-21 12:32]** [RFC PATCH v4 05/25] target/arm/kvm: read all ID registers from KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
7. **[09-21 12:32]** [RFC PATCH v4 06/25] target/arm/kvm: handle special ID registers when reading from KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
8. **[09-21 12:32]** [RFC PATCH v4 07/25] target/arm/kvm: process ID register writeback per field
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
9. **[09-21 12:32]** [RFC PATCH v4 08/25] target/arm/kvm: handle writeback for special ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
10. **[09-21 12:32]** [RFC PATCH v4 09/25] target/arm: introduce named CPU model infrastructure
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
11. **[09-21 12:32]** [RFC PATCH v4 10/25] target/arm: fix SVE and PAuth finalize for named CPU models
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
12. **[09-21 12:32]** [RFC PATCH v4 11/25] target/arm: disable PMU support for named CPU models
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
13. **[09-21 12:32]** [RFC PATCH v4 12/25] target/arm: add arm-v9.0-a-v1 named CPU model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
14. **[09-21 12:32]** [RFC PATCH v4 13/25] target/arm: add neoverse-v2-v1 named CPU model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
15. **[09-21 12:32]** [RFC PATCH v4 14/25] target/arm: add neoverse-v2-v2 named CPU model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
16. **[09-21 12:32]** [RFC PATCH v4 15/25] target/arm: add graviton4-v1 named CPU model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
17. **[09-21 12:32]** [RFC PATCH v4 16/25] target/arm: add grace-v1 named CPU model
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
18. **[09-21 12:32]** [RFC PATCH v4 17/25] target/arm: fail named CPU models on unknown non-zero feature ID regs
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
19. **[09-21 12:32]** [RFC PATCH v4 18/25] target/arm: add cpu-models-stub.c
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[09-21 12:32]** [RFC PATCH v4 19/25] target/arm/qmp: allow named CPU models on cpu-model-expansion
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
21. **[09-21 12:32]** [RFC PATCH v4 20/25] target/arm/kvm: compute host-supported values for ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[09-21 12:32]** [RFC PATCH v4 21/25] target/arm: report 0 as supported for ID fields gated by vCPU init flags
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
23. **[09-21 12:32]** [RFC PATCH v4 22/25] target/arm/kvm: add kvm_arm_get_host_isar helper
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[09-21 12:32]** [RFC PATCH v4 23/25] qmp: add query-cpu-props-info command
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
25. **[09-21 12:32]** [RFC PATCH v4 24/25] target/arm/qmp: implement query-cpu-props-info for KVM
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
26. **[09-21 12:32]** [RFC PATCH v4 25/25] target/arm/qmp: hook blockers in query-cpu-definitions
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
27. **[09-23 18:22]** Re: [RFC PATCH v4 01/25] target/arm: expose SYSREG_ props for
 REVIDR_EL1 and AIDR_EL1
   - 发件人: Eric Auger <eric.auger@redhat.com>
28. **[09-23 18:37]** Re: [RFC PATCH v4 02/25] target/arm: expose all non-res ID reg fields
 as properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
29. **[09-24 08:46]** Re: [RFC PATCH v4 02/25] target/arm: expose all non-res ID reg fields
 as properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
30. **[09-24 08:54]** Re: [RFC PATCH v4 03/25] target/arm: move SYSREG_ prop infra to
 cpu64.c
   - 发件人: Eric Auger <eric.auger@redhat.com>
31. **[09-24 09:52]** Re: [RFC PATCH v4 05/25] target/arm/kvm: read all ID registers from
 KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
32. **[09-24 11:41]** Re: [RFC PATCH v4 07/25] target/arm/kvm: process ID register
 writeback per field
   - 发件人: Eric Auger <eric.auger@redhat.com>
33. **[09-24 11:57]** Re: [RFC PATCH v4 08/25] target/arm/kvm: handle writeback for special
 ID register fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
34. **[09-24 10:21]** Re: [RFC PATCH v4 08/25] target/arm/kvm: handle writeback for special
 ID register fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
35. **[09-24 13:47]** Re: [RFC PATCH v4 08/25] target/arm/kvm: handle writeback for special
 ID register fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
36. **[09-24 15:35]** Re: [RFC PATCH v4 09/25] target/arm: introduce named CPU model
 infrastructure
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 3: [RFC PATCH v8 00/14] coco: guest: Add a shared-granule allocator for host-shared memory

**📧 邮件数**: 24 | **👥 参与者**: 5 | **📅 开始时间**: Thu, 24 Sep 2026 15:35:15 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:24, 27787 tokens)

#### 📝 邮件列表

1. **[09-24 15:35]** [RFC PATCH v8 00/14] coco: guest: Add a shared-granule allocator for host-shared memory
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[09-24 15:35]** [RFC PATCH v8 01/14] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[09-24 15:35]** [RFC PATCH v8 02/14] mm: Zero memory during shared memory transitions
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[09-24 15:35]** [RFC PATCH v8 03/14] irqchip/gic-v3-its: Resolve the default NUMA node explicitly
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[09-24 15:35]** [RFC PATCH v8 04/14] irqchip/gic-v3-its: Allocate shared tables using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[09-24 15:35]** [RFC PATCH v8 05/14] dma-contiguous: Derive shared alignment from DMA attributes
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
7. **[09-24 15:35]** [RFC PATCH v8 06/14] dma-pool: Allocate CoCo atomic pools using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
8. **[09-24 15:35]** [RFC PATCH v8 07/14] dma-direct: Align CoCo shared DMA allocations to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
9. **[09-24 15:35]** [RFC PATCH v8 08/14] swiotlb: Align shared IO TLB pools to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
10. **[09-24 15:35]** [RFC PATCH v8 09/14] swiotlb: Reject misaligned restricted DMA pools for CoCo guests
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
11. **[09-24 15:35]** [RFC PATCH v8 10/14] dma-buf: system_heap: Limit scatterlist entries to the buffer size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
12. **[09-24 15:35]** [RFC PATCH v8 11/14] dma-buf: system_heap: Allocate shared buffers using CoCo shared memory allocator
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
13. **[09-24 15:35]** [RFC PATCH v8 12/14] swiotlb: Make rounded shared pool capacity allocatable
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
14. **[09-24 15:35]** [RFC PATCH v8 13/14] mm: Assert CoCo shared allocations may sleep
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
15. **[09-24 15:35]** [RFC PATCH v8 14/14] irqchip/gic-v3-its: Preallocate VPE L1 tables
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
16. **[09-24 10:19]** Re: [RFC PATCH v8 01/14] mm: Add an allocator for CoCo shared
 memory
   - 发件人: sashiko-bot@kernel.org
17. **[09-24 10:19]** Re: [RFC PATCH v8 04/14] irqchip/gic-v3-its: Allocate shared tables
 using CoCo shared memory allocator
   - 发件人: sashiko-bot@kernel.org
18. **[09-24 10:19]** Re: [RFC PATCH v8 03/14] irqchip/gic-v3-its: Resolve the default
 NUMA node explicitly
   - 发件人: sashiko-bot@kernel.org
19. **[09-24 10:19]** Re: [RFC PATCH v8 06/14] dma-pool: Allocate CoCo atomic pools using
 CoCo shared memory allocator
   - 发件人: sashiko-bot@kernel.org
20. **[09-24 10:22]** Re: [RFC PATCH v8 02/14] mm: Zero memory during shared memory
 transitions
   - 发件人: sashiko-bot@kernel.org
21. **[09-24 10:22]** Re: [RFC PATCH v8 08/14] swiotlb: Align shared IO TLB pools to the
 shared granule size
   - 发件人: sashiko-bot@kernel.org
22. **[09-24 19:52]** Re: [RFC PATCH v8 01/14] mm: Add an allocator for CoCo shared memory
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
23. **[09-24 15:26]** Re: [RFC PATCH v8 01/14] mm: Add an allocator for CoCo shared memory
   - 发件人: Jason Gunthorpe <jgg@nvidia.com>
24. **[09-25 13:08]** Re: [RFC PATCH v8 02/14] mm: Zero memory during shared memory
 transitions
   - 发件人: Kiryl Shutsemau <kas@kernel.org>

---

### Thread 4: [RFC PATCH 00/46] Orphaned Virtual Machines

**📧 邮件数**: 10 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 20 Sep 2026 15:36:04 -0400

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:9, 31568 tokens)

#### 📝 邮件列表

1. **[09-20 15:36]** [RFC PATCH 00/46] Orphaned Virtual Machines
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
2. **[09-21 07:42]** Re: [RFC PATCH 00/46] Orphaned Virtual Machines
   - 发件人: Graf (AWS), Alexander <graf@amazon.de>
3. **[09-21 17:00]** [RFC PATCH 39/46] KVM: VMX: Integrate Caretaker VMX detach serialization and KVM registration
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
4. **[09-21 17:00]** [RFC PATCH 40/46] KVM: SVM: Add Caretaker SVM assembly guest entry/exit routine
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
5. **[09-21 17:00]** [RFC PATCH 41/46] KVM: SVM: Implement Caretaker SVM VMCB lifecycle and exit dispatch
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
6. **[09-21 17:00]** [RFC PATCH 42/46] KVM: arm64: Add Caretaker arm64 KHO ABI and runtime context headers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
7. **[09-21 17:00]** [RFC PATCH 43/46] KVM: arm64: Add Caretaker EL2 exception vectors and guest entry/exit assembly
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
8. **[09-21 17:00]** [RFC PATCH 44/46] KVM: arm64: Implement Caretaker GICv3 CPU interface and arch timer emulation
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
9. **[09-21 17:00]** [RFC PATCH 45/46] KVM: arm64: Implement Caretaker system register trap and exception handlers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
10. **[09-21 17:00]** [RFC PATCH 46/46] KVM: arm64: Implement Caretaker vCPU run loop and LUO detach/attach lifecycle
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>

---

### Thread 5: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM

**📧 邮件数**: 6 | **👥 参与者**: 4 | **📅 开始时间**: Sun, 13 Sep 2026 10:00:40 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:5 新:1, 1264 tokens)

#### 📝 邮件列表

1. **[09-13 10:00]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[09-15 18:12]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[09-15 17:37]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from
 S2AP_W to DBM
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[09-16 12:22]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[09-18 17:39]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from
 S2AP_W to DBM
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
6. **[09-21 15:15]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 6: [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL save/reload when ptimer is used

**📧 邮件数**: 5 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 21 Sep 2026 19:18:40 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:5, 1889 tokens)

#### 📝 邮件列表

1. **[09-21 19:18]** [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL save/reload when ptimer is used
   - 发件人: Zhou Wang <wangzhou1@hisilicon.com>
2. **[09-21 11:41]** Re: [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL
 save/reload when ptimer is used
   - 发件人: sashiko-bot@kernel.org
3. **[09-21 14:22]** Re: [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL save/reload when ptimer is used
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[09-22 18:16]** Re: [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL save/reload
 when ptimer is used
   - 发件人: Zhou Wang <wangzhou1@hisilicon.com>
5. **[09-24 18:58]** Re: [RFC PATCH] KVM: arm64: Restrict CNTP_CVAL/CNTHP_CVAL save/reload when ptimer is used
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 7: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on
 migration

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 18 Sep 2026 19:58:43 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 445 tokens)

#### 📝 邮件列表

1. **[09-18 19:58]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on
 migration
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
2. **[09-21 15:28]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on migration
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.3, round #1

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Sat, 19 Sep 2026 11:33:44 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:1, 405 tokens)

#### 📝 邮件列表

1. **[09-19 11:33]** [GIT PULL] KVM/arm64 fixes for 7.3, round #1
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[09-19 11:36]** Re: [GIT PULL] KVM/arm64 fixes for 7.3, round #1
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[09-21 12:10]** Re: [GIT PULL] KVM/arm64 fixes for 7.3, round #1
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

