# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-09-21 03:32:55

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 854
- **总 Thread 数**: 68
- **大型 Thread** (>20封): 16 个

### 分类分布

- **PATCH**: 62 threads (769 邮件)
- **RFC**: 4 threads (82 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Other**: 1 threads (1 邮件)

---

## 📌 PATCH

共 62 个 thread

---

### Thread 1: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL

**📧 邮件数**: 93 | **👥 参与者**: 9 | **📅 开始时间**: Mon, 14 Sep 2026 15:57:20 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:93, 61216 tokens)

#### 📝 邮件列表

1. **[09-14 15:57]** [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-14 15:57]** [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-14 15:57]** [PATCH v2 02/40] mm/vma: predicate setting mmap_prepare VMA fields
 on new vma alloc
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-14 15:57]** [PATCH v2 03/40] mm/vma: introduce and use vma_[flags_]can_merge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-14 15:57]** [PATCH v2 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-14 15:57]** [PATCH v2 05/40] mm/vma: ensure mmap_prepare doesn't set actions
 on a mergeable vma
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-14 15:57]** [PATCH v2 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-14 15:57]** [PATCH v2 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
9. **[09-14 15:57]** [PATCH v2 08/40] mm: add mmap action for discontiguous kernel page
 mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
10. **[09-14 15:57]** [PATCH v2 09/40] docs: filesystems: update mmap_prepare docs for
 discontig kernel pgs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
11. **[09-14 15:57]** [PATCH v2 10/40] drivers/usb/mon: update to use mmap_prepare + map
 kernel pages
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-14 15:57]** [PATCH v2 11/40] infiniband: update hfi1 to use
 remap_vmalloc_range()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-14 15:57]** [PATCH v2 12/40] selinux: reject writable opens of policy file,
 drop mmap shared/write check
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-14 15:57]** [PATCH v2 13/40] ALSA: pcm: use vm_insert_page() to map PCM status
 page
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-14 15:57]** [PATCH v2 14/40] bpf: arena: mark arena_map_mmap() mappings
 VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
16. **[09-14 15:57]** [PATCH v2 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
17. **[09-14 15:57]** [PATCH v2 16/40] mm/vma: only allow mmap to clear VMA_MAYWRITE_BIT
 if kernel-owned
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
18. **[09-14 15:57]** [PATCH v2 17/40] mm/vma: add and use vma_[flags]_is_fixed_mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
19. **[09-14 15:57]** [PATCH v2 18/40] scsi: sg: convert mmap hook to mmap_prepare and
 rework
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
20. **[09-14 15:57]** [PATCH v2 19/40] fbdev: defio: assert FBINFO_VIRTFB, drop VM_IO,
 add VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
21. **[09-14 15:57]** [PATCH v2 20/40] HSI: cmt_speech: convert mmap hook to
 mmap_prepare, refactor
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
22. **[09-14 15:57]** [PATCH v2 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT VMAs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
23. **[09-14 15:57]** [PATCH v2 22/40] uprobes: remove VM_IO, set VM_MIXEDMAP for mapped
 kernel pages
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
24. **[09-14 15:57]** [PATCH v2 23/40] mm/mlock: clear VMA_LOCKED_MASK over mmap
 callback
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
25. **[09-14 15:57]** [PATCH v2 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
26. **[09-14 15:57]** [PATCH v2 25/40] mm/vma: enforce that only kernel-owned mappings
 may set VMA_IO_BIT
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
27. **[09-14 15:57]** [PATCH v2 26/40] mm: remove VMA_IO_BIT check in
 vma[_flags]_is_kernel_owned()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
28. **[09-14 15:57]** [PATCH v2 27/40] mm: remove hugetlb_inline.h
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
29. **[09-14 15:57]** [PATCH v2 28/40] mm: rename is_vm_hugetlb_page() to
 vma_is_hugetlb()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
30. **[09-14 15:57]** [PATCH v2 29/40] mm: drop some redundant checks around hugetlb
 VMAs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
31. **[09-14 15:57]** [PATCH v2 30/40] mm/madvise: update is_valid_guard_vma() to use
 vma_can_merge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
32. **[09-14 15:57]** [PATCH v2 31/40] mm/vma: introduce vma[_flags]_is_persistent()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
33. **[09-14 15:57]** [PATCH v2 32/40] mm/uffd: use predicates for userfaultfd checks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
34. **[09-14 15:57]** [PATCH v2 33/40] mm/madvise: use predicates for madvise(...,
 MADV_DOFORK)
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
35. **[09-14 15:57]** [PATCH v2 34/40] mm: eliminate VMA_SPECIAL_FLAGS usage when
 hugetlb explicitly tested
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
36. **[09-14 15:57]** [PATCH v2 35/40] mm: eliminate VMA_SPECIAL_FLAGS check in
 lru_gen_look_around()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
37. **[09-14 15:57]** [PATCH v2 36/40] mm: avoid use of VMA_SPECIAL_FLAGS in
 migrate_vma_setup()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
38. **[09-14 15:57]** [PATCH v2 37/40] mm: eliminate VM_SPECIAL, VMA_SPECIAL_FLAGS
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
39. **[09-14 15:57]** [PATCH v2 38/40] fuse: dax: do not set VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
40. **[09-14 15:57]** [PATCH v2 39/40] mm/huge_memory: remove vma_is_special_huge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
41. **[09-14 15:58]** [PATCH v2 40/40] mm/vma: introduce and use vma[_flags]_can_gup()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
42. **[09-14 15:40]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: sashiko-bot@kernel.org
43. **[09-14 15:55]** Re: [PATCH v2 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: sashiko-bot@kernel.org
44. **[09-14 15:59]** Re: [PATCH v2 03/40] mm/vma: introduce and use
 vma_[flags_]can_merge()
   - 发件人: sashiko-bot@kernel.org
45. **[09-14 16:18]** Re: [PATCH v2 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: sashiko-bot@kernel.org
46. **[09-14 16:45]** Re: [PATCH v2 05/40] mm/vma: ensure mmap_prepare doesn't set
 actions on a mergeable vma
   - 发件人: sashiko-bot@kernel.org
47. **[09-14 16:47]** Re: [PATCH v2 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: sashiko-bot@kernel.org
48. **[09-14 16:50]** Re: [PATCH v2 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: sashiko-bot@kernel.org
49. **[09-14 17:03]** Re: [PATCH v2 08/40] mm: add mmap action for discontiguous kernel
 page mapping
   - 发件人: sashiko-bot@kernel.org
50. **[09-14 17:07]** Re: [PATCH v2 09/40] docs: filesystems: update mmap_prepare docs
 for discontig kernel pgs
   - 发件人: sashiko-bot@kernel.org
51. **[09-14 17:18]** Re: [PATCH v2 10/40] drivers/usb/mon: update to use mmap_prepare +
 map kernel pages
   - 发件人: sashiko-bot@kernel.org
52. **[09-14 17:39]** Re: [PATCH v2 11/40] infiniband: update hfi1 to use
 remap_vmalloc_range()
   - 发件人: sashiko-bot@kernel.org
53. **[09-14 17:57]** Re: [PATCH v2 12/40] selinux: reject writable opens of policy file,
 drop mmap shared/write check
   - 发件人: sashiko-bot@kernel.org
54. **[09-14 18:30]** Re: [PATCH v2 13/40] ALSA: pcm: use vm_insert_page() to map PCM
 status page
   - 发件人: sashiko-bot@kernel.org
55. **[09-14 18:46]** Re: [PATCH v2 14/40] bpf: arena: mark arena_map_mmap() mappings
 VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
56. **[09-14 18:50]** Re: [PATCH v2 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: sashiko-bot@kernel.org
57. **[09-14 19:14]** Re: [PATCH v2 16/40] mm/vma: only allow mmap to clear
 VMA_MAYWRITE_BIT if kernel-owned
   - 发件人: sashiko-bot@kernel.org
58. **[09-14 19:24]** Re: [PATCH v2 17/40] mm/vma: add and use
 vma_[flags]_is_fixed_mapping
   - 发件人: sashiko-bot@kernel.org
59. **[09-14 19:30]** Re: [PATCH v2 18/40] scsi: sg: convert mmap hook to mmap_prepare
 and rework
   - 发件人: sashiko-bot@kernel.org
60. **[09-14 19:44]** Re: [PATCH v2 19/40] fbdev: defio: assert FBINFO_VIRTFB, drop
 VM_IO, add VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
61. **[09-14 15:57]** Re: [PATCH v2 12/40] selinux: reject writable opens of policy file,
 drop mmap shared/write check
   - 发件人: Paul Moore <paul@paul-moore.com>
62. **[09-14 20:15]** Re: [PATCH v2 20/40] HSI: cmt_speech: convert mmap hook to
 mmap_prepare, refactor
   - 发件人: sashiko-bot@kernel.org
63. **[09-14 20:33]** Re: [PATCH v2 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT
 VMAs
   - 发件人: sashiko-bot@kernel.org
64. **[09-14 20:47]** Re: [PATCH v2 22/40] uprobes: remove VM_IO, set VM_MIXEDMAP for
 mapped kernel pages
   - 发件人: sashiko-bot@kernel.org
65. **[09-14 21:09]** Re: [PATCH v2 23/40] mm/mlock: clear VMA_LOCKED_MASK over mmap
 callback
   - 发件人: sashiko-bot@kernel.org
66. **[09-14 21:44]** Re: [PATCH v2 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: sashiko-bot@kernel.org
67. **[09-14 22:08]** Re: [PATCH v2 29/40] mm: drop some redundant checks around hugetlb
 VMAs
   - 发件人: sashiko-bot@kernel.org
68. **[09-14 22:09]** Re: [PATCH v2 27/40] mm: remove hugetlb_inline.h
   - 发件人: sashiko-bot@kernel.org
69. **[09-14 22:09]** Re: [PATCH v2 26/40] mm: remove VMA_IO_BIT check in
 vma[_flags]_is_kernel_owned()
   - 发件人: sashiko-bot@kernel.org
70. **[09-14 22:12]** Re: [PATCH v2 31/40] mm/vma: introduce vma[_flags]_is_persistent()
   - 发件人: sashiko-bot@kernel.org
71. **[09-14 22:14]** Re: [PATCH v2 30/40] mm/madvise: update is_valid_guard_vma() to use
 vma_can_merge()
   - 发件人: sashiko-bot@kernel.org
72. **[09-14 22:16]** Re: [PATCH v2 32/40] mm/uffd: use predicates for userfaultfd checks
   - 发件人: sashiko-bot@kernel.org
73. **[09-14 22:18]** Re: [PATCH v2 33/40] mm/madvise: use predicates for madvise(...,
 MADV_DOFORK)
   - 发件人: sashiko-bot@kernel.org
74. **[09-14 22:18]** Re: [PATCH v2 25/40] mm/vma: enforce that only kernel-owned
 mappings may set VMA_IO_BIT
   - 发件人: sashiko-bot@kernel.org
75. **[09-14 22:19]** Re: [PATCH v2 37/40] mm: eliminate VM_SPECIAL, VMA_SPECIAL_FLAGS
   - 发件人: sashiko-bot@kernel.org
76. **[09-14 22:21]** Re: [PATCH v2 34/40] mm: eliminate VMA_SPECIAL_FLAGS usage when
 hugetlb explicitly tested
   - 发件人: sashiko-bot@kernel.org
77. **[09-14 22:22]** Re: [PATCH v2 35/40] mm: eliminate VMA_SPECIAL_FLAGS check in
 lru_gen_look_around()
   - 发件人: sashiko-bot@kernel.org
78. **[09-14 22:23]** Re: [PATCH v2 36/40] mm: avoid use of VMA_SPECIAL_FLAGS in
 migrate_vma_setup()
   - 发件人: sashiko-bot@kernel.org
79. **[09-14 22:25]** Re: [PATCH v2 40/40] mm/vma: introduce and use
 vma[_flags]_can_gup()
   - 发件人: sashiko-bot@kernel.org
80. **[09-14 22:26]** Re: [PATCH v2 39/40] mm/huge_memory: remove vma_is_special_huge()
   - 发件人: sashiko-bot@kernel.org
81. **[09-14 22:30]** Re: [PATCH v2 38/40] fuse: dax: do not set VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
82. **[09-14 23:17]** Re: [PATCH v2 14/40] bpf: arena: mark arena_map_mmap() mappings VM_MIXEDMAP
   - 发件人: Emil Tsalapatis <linux-lists@etsalapatis.com>
83. **[09-14 18:08]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit,
 eliminate VM_SPECIAL
   - 发件人: Andrew Morton <akpm@linux-foundation.org>
84. **[09-17 12:33]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Mike Rapoport <rppt@kernel.org>
85. **[09-17 10:57]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
86. **[09-17 12:40]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
87. **[09-18 05:57]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Breno Leitao <leitao@debian.org>
88. **[09-18 14:20]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
89. **[09-18 07:28]** Re: [PATCH v2 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: Breno Leitao <leitao@debian.org>
90. **[09-18 22:20]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: David Hildenbrand (Arm) <david@kernel.org>
91. **[09-18 13:31]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate VM_SPECIAL
   - 发件人: Suren Baghdasaryan <surenb@google.com>
92. **[09-19 16:05]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
93. **[09-19 16:09]** Re: [PATCH v2 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 2: [PATCH v3 00/40] mm: make VMA flag semantics explicit, eliminate
 VM_SPECIAL

**📧 邮件数**: 82 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 17 Sep 2026 17:22:09 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:82, 61209 tokens)

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
11. **[09-17 17:22]** [PATCH v3 10/40] drivers/usb/mon: update to use mmap_prepare + map
 kernel pages
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-17 17:22]** [PATCH v3 11/40] infiniband: update hfi1 to use
 remap_vmalloc_range()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-17 17:22]** [PATCH v3 12/40] selinux: reject writable opens of policy file,
 drop mmap shared/write check
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-17 17:22]** [PATCH v3 13/40] ALSA: pcm: use vm_insert_page() to map PCM status
 page
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-17 17:22]** [PATCH v3 14/40] bpf: arena: mark arena_map_mmap() mappings
 VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
16. **[09-17 17:22]** [PATCH v3 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
17. **[09-17 17:22]** [PATCH v3 16/40] mm/vma: only allow mmap to clear VMA_MAYWRITE_BIT
 if kernel-owned
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
18. **[09-17 17:22]** [PATCH v3 17/40] mm/vma: add and use vma_[flags]_is_fixed_mapping
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
19. **[09-17 17:22]** [PATCH v3 18/40] scsi: sg: convert mmap hook to mmap_prepare and
 rework
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
20. **[09-17 17:22]** [PATCH v3 19/40] fbdev: defio: assert FBINFO_VIRTFB, drop VM_IO,
 add VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
21. **[09-17 17:22]** [PATCH v3 20/40] HSI: cmt_speech: convert mmap hook to
 mmap_prepare, refactor
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
22. **[09-17 17:22]** [PATCH v3 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT VMAs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
23. **[09-17 17:22]** [PATCH v3 22/40] uprobes: remove VM_IO, set VM_MIXEDMAP for mapped
 kernel pages
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
24. **[09-17 17:22]** [PATCH v3 23/40] mm/mlock: clear VMA_LOCKED_MASK over mmap
 callback
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
25. **[09-17 17:22]** [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
26. **[09-17 17:22]** [PATCH v3 25/40] mm/vma: enforce that only kernel-owned mappings
 may set VMA_IO_BIT
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
27. **[09-17 17:22]** [PATCH v3 26/40] mm: remove VMA_IO_BIT check in
 vma[_flags]_is_kernel_owned()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
28. **[09-17 17:22]** [PATCH v3 27/40] mm: remove hugetlb_inline.h
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
29. **[09-17 17:22]** [PATCH v3 28/40] mm: rename is_vm_hugetlb_page() to
 vma_is_hugetlb()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
30. **[09-17 17:22]** [PATCH v3 29/40] mm: drop some redundant checks around hugetlb
 VMAs
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
31. **[09-17 17:22]** [PATCH v3 30/40] mm/madvise: update is_valid_guard_vma() to use
 vma_can_merge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
32. **[09-17 17:22]** [PATCH v3 31/40] mm/vma: introduce vma[_flags]_is_persistent()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
33. **[09-17 17:22]** [PATCH v3 32/40] mm/uffd: use predicates for userfaultfd checks
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
34. **[09-17 17:22]** [PATCH v3 33/40] mm/madvise: use predicates for madvise(...,
 MADV_DOFORK)
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
35. **[09-17 17:22]** [PATCH v3 34/40] mm: eliminate VMA_SPECIAL_FLAGS usage when
 hugetlb explicitly tested
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
36. **[09-17 17:22]** [PATCH v3 35/40] mm: eliminate VMA_SPECIAL_FLAGS check in
 lru_gen_look_around()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
37. **[09-17 17:22]** [PATCH v3 36/40] mm: avoid use of VMA_SPECIAL_FLAGS in
 migrate_vma_setup()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
38. **[09-17 17:22]** [PATCH v3 37/40] mm: eliminate VM_SPECIAL, VMA_SPECIAL_FLAGS
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
39. **[09-17 17:22]** [PATCH v3 38/40] fuse: dax: do not set VM_MIXEDMAP
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
40. **[09-17 17:22]** [PATCH v3 39/40] mm/huge_memory: remove vma_is_special_huge()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
41. **[09-17 17:22]** [PATCH v3 40/40] mm/vma: introduce and use vma[_flags]_can_gup()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
42. **[09-17 16:54]** Re: [PATCH v3 01/40] mm/vma: fix mmap_prepare file handling, remove
 file_doesnt_need_get
   - 发件人: sashiko-bot@kernel.org
43. **[09-17 17:07]** Re: [PATCH v3 02/40] mm/vma: predicate setting mmap_prepare VMA
 fields on new vma alloc
   - 发件人: sashiko-bot@kernel.org
44. **[09-17 17:11]** Re: [PATCH v3 03/40] mm/vma: introduce and use
 vma_[flags_]can_merge()
   - 发件人: sashiko-bot@kernel.org
45. **[09-17 17:17]** Re: [PATCH v3 06/40] mm: make map_kernel_pages_[prepare,complete]
 internal and unexported
   - 发件人: sashiko-bot@kernel.org
46. **[09-17 17:17]** Re: [PATCH v3 07/40] mm/vma: tidy up map kernel pages enum values
   - 发件人: sashiko-bot@kernel.org
47. **[09-17 17:21]** Re: [PATCH v3 15/40] mm/vma: add vma[_flags]_is_kernel_owned()
 predicates
   - 发件人: sashiko-bot@kernel.org
48. **[09-17 17:25]** Re: [PATCH v3 14/40] bpf: arena: mark arena_map_mmap() mappings
 VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
49. **[09-17 17:25]** Re: [PATCH v3 12/40] selinux: reject writable opens of policy file,
 drop mmap shared/write check
   - 发件人: sashiko-bot@kernel.org
50. **[09-17 17:25]** Re: [PATCH v3 08/40] mm: add mmap action for discontiguous kernel
 page mapping
   - 发件人: sashiko-bot@kernel.org
51. **[09-17 17:27]** Re: [PATCH v3 17/40] mm/vma: add and use
 vma_[flags]_is_fixed_mapping
   - 发件人: sashiko-bot@kernel.org
52. **[09-17 17:27]** Re: [PATCH v3 19/40] fbdev: defio: assert FBINFO_VIRTFB, drop
 VM_IO, add VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
53. **[09-17 17:28]** Re: [PATCH v3 16/40] mm/vma: only allow mmap to clear
 VMA_MAYWRITE_BIT if kernel-owned
   - 发件人: sashiko-bot@kernel.org
54. **[09-17 17:29]** Re: [PATCH v3 10/40] drivers/usb/mon: update to use mmap_prepare +
 map kernel pages
   - 发件人: sashiko-bot@kernel.org
55. **[09-17 17:30]** Re: [PATCH v3 22/40] uprobes: remove VM_IO, set VM_MIXEDMAP for
 mapped kernel pages
   - 发件人: sashiko-bot@kernel.org
56. **[09-17 17:30]** Re: [PATCH v3 28/40] mm: rename is_vm_hugetlb_page() to
 vma_is_hugetlb()
   - 发件人: sashiko-bot@kernel.org
57. **[09-17 17:30]** Re: [PATCH v3 21/40] mm/gup: error out early on !VMA_MAYREAD_BIT
 VMAs
   - 发件人: sashiko-bot@kernel.org
58. **[09-17 17:31]** Re: [PATCH v3 20/40] HSI: cmt_speech: convert mmap hook to
 mmap_prepare, refactor
   - 发件人: sashiko-bot@kernel.org
59. **[09-17 17:31]** Re: [PATCH v3 27/40] mm: remove hugetlb_inline.h
   - 发件人: sashiko-bot@kernel.org
60. **[09-17 17:31]** Re: [PATCH v3 25/40] mm/vma: enforce that only kernel-owned
 mappings may set VMA_IO_BIT
   - 发件人: sashiko-bot@kernel.org
61. **[09-17 17:32]** Re: [PATCH v3 05/40] mm/vma: ensure mmap_prepare doesn't set
 actions on a mergeable vma
   - 发件人: sashiko-bot@kernel.org
62. **[09-17 17:32]** Re: [PATCH v3 29/40] mm: drop some redundant checks around hugetlb
 VMAs
   - 发件人: sashiko-bot@kernel.org
63. **[09-17 17:32]** Re: [PATCH v3 23/40] mm/mlock: clear VMA_LOCKED_MASK over mmap
 callback
   - 发件人: sashiko-bot@kernel.org
64. **[09-17 17:32]** Re: [PATCH v3 09/40] docs: filesystems: update mmap_prepare docs
 for discontig kernel pgs
   - 发件人: sashiko-bot@kernel.org
65. **[09-17 17:34]** Re: [PATCH v3 18/40] scsi: sg: convert mmap hook to mmap_prepare
 and rework
   - 发件人: sashiko-bot@kernel.org
66. **[09-17 17:34]** Re: [PATCH v3 13/40] ALSA: pcm: use vm_insert_page() to map PCM
 status page
   - 发件人: sashiko-bot@kernel.org
67. **[09-17 17:34]** Re: [PATCH v3 26/40] mm: remove VMA_IO_BIT check in
 vma[_flags]_is_kernel_owned()
   - 发件人: sashiko-bot@kernel.org
68. **[09-17 17:35]** Re: [PATCH v3 31/40] mm/vma: introduce vma[_flags]_is_persistent()
   - 发件人: sashiko-bot@kernel.org
69. **[09-17 17:36]** Re: [PATCH v3 11/40] infiniband: update hfi1 to use
 remap_vmalloc_range()
   - 发件人: sashiko-bot@kernel.org
70. **[09-17 17:36]** Re: [PATCH v3 40/40] mm/vma: introduce and use
 vma[_flags]_can_gup()
   - 发件人: sashiko-bot@kernel.org
71. **[09-17 17:37]** Re: [PATCH v3 30/40] mm/madvise: update is_valid_guard_vma() to use
 vma_can_merge()
   - 发件人: sashiko-bot@kernel.org
72. **[09-17 17:37]** Re: [PATCH v3 33/40] mm/madvise: use predicates for madvise(...,
 MADV_DOFORK)
   - 发件人: sashiko-bot@kernel.org
73. **[09-17 17:38]** Re: [PATCH v3 38/40] fuse: dax: do not set VM_MIXEDMAP
   - 发件人: sashiko-bot@kernel.org
74. **[09-17 17:38]** Re: [PATCH v3 04/40] mm: consistently validate VMA state after
 mmap[_prepare] hooks
   - 发件人: sashiko-bot@kernel.org
75. **[09-17 17:38]** Re: [PATCH v3 39/40] mm/huge_memory: remove vma_is_special_huge()
   - 发件人: sashiko-bot@kernel.org
76. **[09-17 17:38]** Re: [PATCH v3 32/40] mm/uffd: use predicates for userfaultfd checks
   - 发件人: sashiko-bot@kernel.org
77. **[09-17 17:40]** Re: [PATCH v3 36/40] mm: avoid use of VMA_SPECIAL_FLAGS in
 migrate_vma_setup()
   - 发件人: sashiko-bot@kernel.org
78. **[09-17 17:41]** Re: [PATCH v3 35/40] mm: eliminate VMA_SPECIAL_FLAGS check in
 lru_gen_look_around()
   - 发件人: sashiko-bot@kernel.org
79. **[09-17 17:43]** Re: [PATCH v3 24/40] mm/mlock: eliminate weird VMA_IO_BIT abuse and
 simplify
   - 发件人: sashiko-bot@kernel.org
80. **[09-17 17:44]** Re: [PATCH v3 37/40] mm: eliminate VM_SPECIAL, VMA_SPECIAL_FLAGS
   - 发件人: sashiko-bot@kernel.org
81. **[09-17 17:45]** Re: [PATCH v3 34/40] mm: eliminate VMA_SPECIAL_FLAGS usage when
 hugetlb explicitly tested
   - 发件人: sashiko-bot@kernel.org
82. **[09-17 14:23]** Re: [PATCH v3 00/40] mm: make VMA flag semantics explicit,
 eliminate VM_SPECIAL
   - 发件人: Andrew Morton <akpm@linux-foundation.org>

---

### Thread 3: [PATCH v8 00/29] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 60 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 18 Sep 2026 15:30:37 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:60, 60541 tokens)

#### 📝 邮件列表

1. **[09-18 15:30]** [PATCH v8 00/29] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[09-18 15:30]** [PATCH v8 01/29] KVM: Introduce file_to_kvm_<arch>() infrastructure
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[09-18 15:30]** [PATCH v8 02/29] KVM: Add file back-pointer to struct kvm
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[09-18 15:30]** [PATCH v8 03/29] KVM: x86: Use file_to_kvm_x86() in SEV
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[09-18 15:30]** [PATCH v8 04/29] KVM/vfio: Use file-based reference counting for KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
6. **[09-18 15:30]** [PATCH v8 05/29] KVM: Restrict kvm_get_kvm/kvm_put_kvm export to internal KVM modules
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[09-18 15:30]** [PATCH v8 06/29] KVM: Move export symbol check macros to Makefile.kvm
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
8. **[09-18 15:30]** [PATCH v8 07/29] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[09-18 15:30]** [PATCH v8 08/29] KVM: Move architecture capability Kconfigs to header defines
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[09-18 15:30]** [PATCH v8 09/29] KVM: Replace CONFIG_KVM_MMIO with KVM_NO_MMIO
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
11. **[09-18 15:30]** [PATCH v8 10/29] arm64: Use proper include variant
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
12. **[09-18 15:30]** [PATCH v8 11/29] arm64: ptrace: Use constants for compat register numbers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[09-18 15:30]** [PATCH v8 12/29] arm64: sysreg: Convert SPSR_ELx to automatic register generation
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[09-18 15:30]** [PATCH v8 13/29] KVM: arm64: Access elements of vcpu_gp_regs individually
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
15. **[09-18 15:30]** [PATCH v8 14/29] KVM: arm64: Use accessor functions for core regs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
16. **[09-18 15:30]** [PATCH v8 15/29] arm64: Prepare sharing arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
17. **[09-18 15:30]** [PATCH v8 16/29] arm64: Share arm64 headers with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
18. **[09-18 15:30]** [PATCH v8 17/29] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
19. **[09-18 15:30]** [PATCH v8 18/29] s390/tools: Use arm64 headers
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
20. **[09-18 15:30]** [PATCH v8 19/29] KVM: s390: Use arm64 code
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[09-18 15:30]** [PATCH v8 20/29] s390: Introduce Start Arm Execution instruction
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
22. **[09-18 15:30]** [PATCH v8 21/29] KVM: s390: arm64: Introduce host definitions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
23. **[09-18 15:30]** [PATCH v8 22/29] s390/hwcaps: Report SAE support as hwcap
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
24. **[09-18 15:31]** [PATCH v8 23/29] KVM: s390: Add basic arm64 kvm module
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
25. **[09-18 15:31]** [PATCH v8 24/29] KVM: s390: arm64: Implement required functions
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
26. **[09-18 15:31]** [PATCH v8 25/29] KVM: s390: arm64: Implement vm/vcpu create destroy.
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[09-18 15:31]** [PATCH v8 26/29] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[09-18 15:31]** [PATCH v8 27/29] KVM: s390: arm64: Implement basic page fault handler
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[09-18 15:31]** [PATCH v8 28/29] KVM: s390: arm64: Integrate arm on s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
30. **[09-18 15:31]** [PATCH v8 29/29] KVM: s390: Enforce no unexpected external symbol exports in s390 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
31. **[09-18 15:38]** Re: [PATCH v8 00/29] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
32. **[09-18 13:45]** Re: [PATCH v8 01/29] KVM: Introduce file_to_kvm_<arch>()
 infrastructure
   - 发件人: sashiko-bot@kernel.org
33. **[09-18 13:56]** Re: [PATCH v8 02/29] KVM: Add file back-pointer to struct kvm
   - 发件人: sashiko-bot@kernel.org
34. **[09-18 14:02]** Re: [PATCH v8 03/29] KVM: x86: Use file_to_kvm_x86() in SEV
   - 发件人: sashiko-bot@kernel.org
35. **[09-18 14:26]** Re: [PATCH v8 04/29] KVM/vfio: Use file-based reference counting
 for KVM
   - 发件人: sashiko-bot@kernel.org
36. **[09-18 14:30]** Re: [PATCH v8 05/29] KVM: Restrict kvm_get_kvm/kvm_put_kvm export
 to internal KVM modules
   - 发件人: sashiko-bot@kernel.org
37. **[09-18 14:37]** Re: [PATCH v8 06/29] KVM: Move export symbol check macros to
 Makefile.kvm
   - 发件人: sashiko-bot@kernel.org
38. **[09-18 14:58]** Re: [PATCH v8 07/29] KVM: Make device name configurable
   - 发件人: sashiko-bot@kernel.org
39. **[09-18 15:07]** Re: [PATCH v8 08/29] KVM: Move architecture capability Kconfigs to
 header defines
   - 发件人: sashiko-bot@kernel.org
40. **[09-18 15:15]** Re: [PATCH v8 09/29] KVM: Replace CONFIG_KVM_MMIO with KVM_NO_MMIO
   - 发件人: sashiko-bot@kernel.org
41. **[09-18 15:16]** Re: [PATCH v8 10/29] arm64: Use proper include variant
   - 发件人: sashiko-bot@kernel.org
42. **[09-18 15:20]** Re: [PATCH v8 11/29] arm64: ptrace: Use constants for compat
 register numbers
   - 发件人: sashiko-bot@kernel.org
43. **[09-18 15:24]** Re: [PATCH v8 12/29] arm64: sysreg: Convert SPSR_ELx to automatic
 register generation
   - 发件人: sashiko-bot@kernel.org
44. **[09-18 15:28]** Re: [PATCH v8 13/29] KVM: arm64: Access elements of vcpu_gp_regs
 individually
   - 发件人: sashiko-bot@kernel.org
45. **[09-18 15:32]** Re: [PATCH v8 14/29] KVM: arm64: Use accessor functions for core
 regs
   - 发件人: sashiko-bot@kernel.org
46. **[09-18 15:39]** Re: [PATCH v8 15/29] arm64: Prepare sharing arm64 headers with s390
   - 发件人: sashiko-bot@kernel.org
47. **[09-18 15:50]** Re: [PATCH v8 16/29] arm64: Share arm64 headers with s390
   - 发件人: sashiko-bot@kernel.org
48. **[09-18 16:02]** Re: [PATCH v8 17/29] KVM: arm64: Share arm64 code with s390
   - 发件人: sashiko-bot@kernel.org
49. **[09-18 16:09]** Re: [PATCH v8 18/29] s390/tools: Use arm64 headers
   - 发件人: sashiko-bot@kernel.org
50. **[09-18 16:14]** Re: [PATCH v8 19/29] KVM: s390: Use arm64 code
   - 发件人: sashiko-bot@kernel.org
51. **[09-18 16:28]** Re: [PATCH v8 20/29] s390: Introduce Start Arm Execution
 instruction
   - 发件人: sashiko-bot@kernel.org
52. **[09-18 16:44]** Re: [PATCH v8 21/29] KVM: s390: arm64: Introduce host definitions
   - 发件人: sashiko-bot@kernel.org
53. **[09-18 16:49]** Re: [PATCH v8 22/29] s390/hwcaps: Report SAE support as hwcap
   - 发件人: sashiko-bot@kernel.org
54. **[09-18 17:00]** Re: [PATCH v8 23/29] KVM: s390: Add basic arm64 kvm module
   - 发件人: sashiko-bot@kernel.org
55. **[09-18 17:13]** Re: [PATCH v8 24/29] KVM: s390: arm64: Implement required functions
   - 发件人: sashiko-bot@kernel.org
56. **[09-18 17:24]** Re: [PATCH v8 25/29] KVM: s390: arm64: Implement vm/vcpu create
 destroy.
   - 发件人: sashiko-bot@kernel.org
57. **[09-18 17:45]** Re: [PATCH v8 26/29] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: sashiko-bot@kernel.org
58. **[09-18 17:55]** Re: [PATCH v8 27/29] KVM: s390: arm64: Implement basic page fault
 handler
   - 发件人: sashiko-bot@kernel.org
59. **[09-18 18:11]** Re: [PATCH v8 28/29] KVM: s390: arm64: Integrate arm on s390
   - 发件人: sashiko-bot@kernel.org
60. **[09-18 18:19]** Re: [PATCH v8 29/29] KVM: s390: Enforce no unexpected external
 symbol exports in s390 KVM
   - 发件人: sashiko-bot@kernel.org

---

### Thread 4: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms

**📧 邮件数**: 52 | **👥 参与者**: 6 | **📅 开始时间**: Tue, 15 Sep 2026 17:01:18 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:52, 31305 tokens)

#### 📝 邮件列表

1. **[09-15 17:01]** [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-15 17:01]** [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-15 17:01]** [PATCH v18 02/23] KVM: arm64: Disable Steal time accounting for protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
4. **[09-15 17:01]** [PATCH v18 03/23] KVM: arm64: Include kvm_emulate.h in kvm/arm_psci.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
5. **[09-15 17:01]** [PATCH v18 04/23] KVM: arm64: Avoid including linux/kvm_host.h in kvm_pgtable.h
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-15 17:01]** [PATCH v18 05/23] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-15 17:01]** [PATCH v18 06/23] KVM: arm64: Refactor the vcpu_load to allow for VM specific callbacks
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-15 17:01]** [PATCH v18 07/23] KVM: arm64: Add vcpu load/put call backs for flavors
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-15 17:01]** [PATCH v18 08/23] KVM: arm64: Reuse kvm_stage2_unmap_range in kvm_unmap_gfn_range
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
10. **[09-15 17:01]** [PATCH v18 09/23] KVM: arm64: Add VM specific callback for S2 MMU operations
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
11. **[09-15 17:01]** [PATCH v18 10/23] KVM: arm64: Abstract out memory abort handling
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
12. **[09-15 17:01]** [PATCH v18 11/23] KVM: arm64: Use kvm_vm_is_unprotected() for !kvm_vm_is_protected()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
13. **[09-15 17:01]** [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
14. **[09-15 17:01]** [PATCH v18 13/23] KVM: arm64: Add a helper for VMs running on hyp that don't trust the host
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[09-15 17:01]** [PATCH v18 14/23] KVM: arm64: CCA: Add a new mode for supporting Realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[09-15 17:01]** [PATCH v18 15/23] KVM: arm64: CCA: Add VCPU load/put for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-15 17:01]** [PATCH v18 16/23] KVM: arm64: CCA: Add bare minimal S2 operations for Realm
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-15 17:01]** [PATCH v18 17/23] KVM: arm64: CCA: Introduce Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-15 17:01]** [PATCH v18 18/23] KVM: arm64: CCA: Mandate VGIC_V3 for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-15 17:01]** [PATCH v18 19/23] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-15 17:01]** [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-15 17:01]** [PATCH v18 21/23] KVM: arm64: CCA: WARN on injected undef exceptions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
23. **[09-15 17:01]** [PATCH v18 22/23] KVM: arm64: CCA: Expose SVE VL register before VCPU finalization
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
24. **[09-15 17:01]** [PATCH v18 23/23] KVM: arm64: CCA: Control user register access for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
25. **[09-15 16:18]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: sashiko-bot@kernel.org
26. **[09-15 16:43]** Re: [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: sashiko-bot@kernel.org
27. **[09-15 17:46]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Marc Zyngier <maz@kernel.org>
28. **[09-15 16:49]** Re: [PATCH v18 23/23] KVM: arm64: CCA: Control user register access
 for Realms
   - 发件人: sashiko-bot@kernel.org
29. **[09-15 18:48]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
30. **[09-15 18:51]** Re: [PATCH v18 23/23] KVM: arm64: CCA: Control user register access
 for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
31. **[09-15 18:55]** Re: [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
32. **[09-15 22:20]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
33. **[09-16 09:16]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Marc Zyngier <maz@kernel.org>
34. **[09-16 09:27]** Re: [PATCH v18 01/23] KVM: arm64: protected VM: Handle set_one_reg
 CNTVCT_EL0/CNTPCT_EL0
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
35. **[09-16 09:29]** Re: [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
36. **[09-16 13:23]** Re: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Mathieu Poirier <mathieu.poirier@linaro.org>
37. **[09-17 12:24]** Re: [PATCH v18 05/23] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[09-17 12:44]** Re: [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Marc Zyngier <maz@kernel.org>
39. **[09-17 12:47]** Re: [PATCH v18 11/23] KVM: arm64: Use kvm_vm_is_unprotected() for !kvm_vm_is_protected()
   - 发件人: Fuad Tabba <tabba@google.com>
40. **[09-17 12:51]** Re: [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Fuad Tabba <tabba@google.com>
41. **[09-17 12:55]** Re: [PATCH v18 13/23] KVM: arm64: Add a helper for VMs running on hyp
 that don't trust the host
   - 发件人: Fuad Tabba <tabba@google.com>
42. **[09-17 13:57]** Re: [PATCH v18 18/23] KVM: arm64: CCA: Mandate VGIC_V3 for Realms
   - 发件人: Fuad Tabba <tabba@google.com>
43. **[09-17 14:16]** Re: [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Fuad Tabba <tabba@google.com>
44. **[09-17 15:16]** Re: [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Joey Gouly <joey.gouly@arm.com>
45. **[09-17 15:32]** Re: [PATCH v18 00/23] KVM: arm64: CCA: Add basic plumbing for Realms
   - 发件人: Fuad Tabba <tabba@google.com>
46. **[09-17 15:56]** Re: [PATCH v18 20/23] KVM: arm64: CCA: Don't expose unsupported
 capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
47. **[09-17 17:47]** Re: [PATCH v18 11/23] KVM: arm64: Use kvm_vm_is_unprotected() for
 !kvm_vm_is_protected()
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
48. **[09-17 17:48]** Re: [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
49. **[09-17 18:06]** Re: [PATCH v18 12/23] KVM: arm64: Widen the scope of "protected" VMs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
50. **[09-18 09:59]** Re: [PATCH v18 05/23] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
51. **[09-18 10:14]** Re: [PATCH v18 05/23] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
52. **[09-18 10:47]** Re: [PATCH v18 05/23] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 5: [PATCH v3 00/18] KVM: arm64: Confine protected VM vCPU state to EL2

**📧 邮件数**: 39 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 14 Sep 2026 12:33:20 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:39, 36896 tokens)

#### 📝 邮件列表

1. **[09-14 12:33]** [PATCH v3 00/18] KVM: arm64: Confine protected VM vCPU state to EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 12:33]** [PATCH v3 01/18] KVM: arm64: Sync HCR_EL2.VSE back to the host vCPU under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-14 12:33]** [PATCH v3 02/18] KVM: arm64: Validate the host vCPU's VM before reading it under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-14 12:33]** [PATCH v3 03/18] KVM: arm64: Pin the host vCPU before adjusting its PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-14 12:33]** [PATCH v3 04/18] KVM: arm64: Disable steal time for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-14 12:33]** [PATCH v3 05/18] KVM: arm64: Introduce per-EC entry handlers for pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-14 12:33]** [PATCH v3 06/18] KVM: arm64: Skip fixed-feature state flush for protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[09-14 12:33]** [PATCH v3 07/18] KVM: arm64: Add {flush,sync}_hyp_timer_state() primitives
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[09-14 12:33]** [PATCH v3 08/18] KVM: arm64: Add system register reset framework for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
10. **[09-14 12:33]** [PATCH v3 09/18] KVM: arm64: Implement HVC handling for protected guests at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[09-14 12:33]** [PATCH v3 10/18] KVM: arm64: Handle PSCI calls for protected VMs at EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
12. **[09-14 12:33]** [PATCH v3 11/18] KVM: arm64: Restrict KVM_ARM_VCPU_INIT and PSCI version for protected VMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
13. **[09-14 12:33]** [PATCH v3 12/18] KVM: arm64: Prevent host PC adjustments for protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
14. **[09-14 12:33]** [PATCH v3 13/18] KVM: arm64: Inject an UNDEF at EL2 for unhandled protected guest exits
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
15. **[09-14 12:33]** [PATCH v3 14/18] KVM: arm64: Add per-EC entry/exit state marshalling for protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
16. **[09-14 12:33]** [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
17. **[09-14 12:33]** [PATCH v3 16/18] KVM: arm64: Reject host power-on of a vCPU that EL2 holds powered off
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[09-14 12:33]** [PATCH v3 17/18] KVM: arm64: Advertise the capabilities that protected VMs support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
19. **[09-14 12:33]** [PATCH v3 18/18] KVM: arm64: Document the protected VM userspace API
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[09-14 13:01]** Re: [PATCH v3 03/18] KVM: arm64: Pin the host vCPU before adjusting
 its PC under pKVM
   - 发件人: sashiko-bot@kernel.org
21. **[09-14 14:42]** Re: [PATCH v3 12/18] KVM: arm64: Prevent host PC adjustments for protected vCPUs
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[09-14 13:42]** Re: [PATCH v3 06/18] KVM: arm64: Skip fixed-feature state flush for
 protected vCPUs
   - 发件人: sashiko-bot@kernel.org
23. **[09-14 15:00]** Re: [PATCH v3 03/18] KVM: arm64: Pin the host vCPU before adjusting
 its PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
24. **[09-14 15:27]** Re: [PATCH v3 06/18] KVM: arm64: Skip fixed-feature state flush for
 protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
25. **[09-14 15:43]** Re: [PATCH v3 12/18] KVM: arm64: Prevent host PC adjustments for
 protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
26. **[09-14 16:23]** Re: [PATCH v3 17/18] KVM: arm64: Advertise the capabilities that
 protected VMs support
   - 发件人: sashiko-bot@kernel.org
27. **[09-14 19:01]** Re: [PATCH v3 17/18] KVM: arm64: Advertise the capabilities that
 protected VMs support
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
28. **[09-15 12:02]** Re: [PATCH v3 12/18] KVM: arm64: Prevent host PC adjustments for protected vCPUs
   - 发件人: Marc Zyngier <maz@kernel.org>
29. **[09-15 12:19]** Re: [PATCH v3 12/18] KVM: arm64: Prevent host PC adjustments for
 protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
30. **[09-16 17:27]** Re: [PATCH v3 14/18] KVM: arm64: Add per-EC entry/exit state marshalling for protected guests
   - 发件人: Marc Zyngier <maz@kernel.org>
31. **[09-16 17:30]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
32. **[09-16 17:43]** Re: [PATCH v3 16/18] KVM: arm64: Reject host power-on of a vCPU that EL2 holds powered off
   - 发件人: Marc Zyngier <maz@kernel.org>
33. **[09-16 20:05]** Re: [PATCH v3 14/18] KVM: arm64: Add per-EC entry/exit state
 marshalling for protected guests
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
34. **[09-16 20:07]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
35. **[09-16 20:08]** Re: [PATCH v3 16/18] KVM: arm64: Reject host power-on of a vCPU that
 EL2 holds powered off
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
36. **[09-17 09:06]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
37. **[09-17 19:42]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
38. **[09-18 14:21]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Will Deacon <will@kernel.org>
39. **[09-18 14:24]** Re: [PATCH v3 15/18] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Will Deacon <will@kernel.org>

---

### Thread 6: [PATCH v18 0/7] firmware: arm_rmm: Add RMM v2.0 base RMI support

**📧 邮件数**: 35 | **👥 参与者**: 5 | **📅 开始时间**: Sat, 12 Sep 2026 09:36:03 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:8 新:27, 8740 tokens)

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
8. **[09-12 09:36]** [PATCH v18 7/7] firmware: arm_rmm: Add wrappers for Realm related RMI commands
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
9. **[09-14 10:28]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Gavin Shan <gshan@redhat.com>
10. **[09-14 11:04]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Gavin Shan <gshan@redhat.com>
11. **[09-14 11:21]** Re: [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Gavin Shan <gshan@redhat.com>
12. **[09-14 15:04]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
13. **[09-14 15:06]** Re: [PATCH v18 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Gavin Shan <gshan@redhat.com>
14. **[09-14 15:41]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Gavin Shan <gshan@redhat.com>
15. **[09-14 15:46]** Re: [PATCH v18 7/7] firmware: arm_rmm: Add wrappers for Realm related
 RMI commands
   - 发件人: Gavin Shan <gshan@redhat.com>
16. **[09-14 07:22]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-14 07:34]** Re: [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-14 09:19]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-14 09:38]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-14 19:50]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
21. **[09-14 19:59]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Gavin Shan <gshan@redhat.com>
22. **[09-14 11:27]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at init
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
23. **[09-14 13:50]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
24. **[09-14 15:02]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
25. **[09-14 15:47]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
26. **[09-15 12:35]** Re: [PATCH v18 7/7] firmware: arm_rmm: Add wrappers for Realm related
 RMI commands
   - 发件人: Alper Gun <alpergun@google.com>
27. **[09-15 20:55]** Re: [PATCH v18 7/7] firmware: arm_rmm: Add wrappers for Realm related
 RMI commands
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
28. **[09-16 11:23]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT entries
 for memory
   - 发件人: Alper Gun <alpergun@google.com>
29. **[09-18 18:27]** Re: [PATCH v18 7/7] firmware: arm_rmm: Add wrappers for Realm
 related RMI commands
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
30. **[09-18 18:27]** Re: [PATCH v18 4/7] firmware: arm_rmm: Add support for SRO
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
31. **[09-18 18:27]** Re: [PATCH v18 2/7] firmware: arm_rmm: Check for RMI support at
 init
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
32. **[09-18 18:27]** Re: [PATCH v18 3/7] firmware: arm_rmm: Configure the RMM with the
 host's page size
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
33. **[09-18 18:27]** Re: [PATCH v18 5/7] firmware: arm_rmm: Activate the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
34. **[09-18 18:27]** Re: [PATCH v18 1/7] firmware: arm_rmm: Add SMC definitions for
 calling the RMM
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>
35. **[09-18 18:27]** Re: [PATCH v18 6/7] firmware: arm_rmm: Ensure the RMM has GPT
 entries for memory
   - 发件人: Jonathan Cameron <jonathan.cameron@oss.qualcomm.com>

---

### Thread 7: [PATCH v7 00/23] KVM: s390: Introduce arm64 KVM

**📧 邮件数**: 30 | **👥 参与者**: 6 | **📅 开始时间**: Mon, 31 Aug 2026 16:47:37 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:25 新:5, 4855 tokens)

#### 📝 邮件列表

1. **[08-31 16:47]** [PATCH v7 00/23] KVM: s390: Introduce arm64 KVM
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[08-31 16:47]** [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[08-31 16:47]** [PATCH v7 21/23] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
4. **[08-31 16:48]** [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig and Makefile
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
5. **[09-01 09:13]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-01 10:40]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
7. **[09-02 08:41]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[09-02 09:50]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
9. **[09-02 14:41]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
10. **[09-02 09:14]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
11. **[09-02 09:20]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig and Makefile
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[09-03 10:38]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig
 and Makefile
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
13. **[09-03 13:42]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
14. **[09-03 15:27]** Re: [PATCH v7 21/23] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Janosch Frank <frankja@linux.ibm.com>
15. **[09-03 07:30]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
16. **[09-03 07:32]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
17. **[09-03 07:43]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig and Makefile
   - 发件人: Sean Christopherson <seanjc@google.com>
18. **[09-03 07:45]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
19. **[09-03 16:55]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
20. **[09-03 17:43]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig
 and Makefile
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
21. **[09-03 08:54]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
22. **[09-03 09:33]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig and Makefile
   - 发件人: Sean Christopherson <seanjc@google.com>
23. **[09-03 21:13]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
24. **[09-03 13:58]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Sean Christopherson <seanjc@google.com>
25. **[09-12 12:43]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Marc Zyngier <maz@kernel.org>
26. **[09-15 17:12]** Re: [PATCH v7 02/23] KVM: Make device name configurable
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
27. **[09-15 17:17]** Re: [PATCH v7 11/23] KVM: arm64: Share arm64 code with s390
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
28. **[09-16 17:00]** Re: [PATCH v7 21/23] KVM: s390: arm64: Implement vCPU IOCTLs
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
29. **[09-17 13:07]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig and
 Makefile
   - 发件人: Christian Borntraeger <borntraeger@linux.ibm.com>
30. **[09-17 13:41]** Re: [PATCH v7 23/23] KVM: s390: arm64: Add KVM_S390_ARM64 Kconfig
 and Makefile
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>

---

### Thread 8: [PATCH v9 00/26] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 27 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 16 Sep 2026 16:45:23 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:27, 77962 tokens)

#### 📝 邮件列表

1. **[09-16 16:45]** [PATCH v9 00/26] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[09-16 16:45]** [PATCH v9 01/26] scripts: introduce scripts/update-aarch64-cpu-sysregs-header.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[09-16 16:45]** [PATCH v9 02/26] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[09-16 16:45]** [PATCH v9 03/26] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[09-16 16:45]** [PATCH v9 04/26] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[09-16 16:45]** [PATCH v9 05/26] scripts: Introduce scripts/aarch64_sysreg_helpers module
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[09-16 16:45]** [PATCH v9 06/26] scripts: Introduce scripts/update-aarch64-cpu-sysreg-properties.py
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[09-16 16:45]** [PATCH v9 07/26] target/arm/cpu-idregs.h.inc: generate with script
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[09-16 16:45]** [PATCH v9 08/26] target/arm/cpu-idregs.h.inc: Generate enum values
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[09-16 16:45]** [PATCH v9 09/26] target/arm/cpu_idregs: generate tables for Arm64 ID registers and fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[09-16 16:45]** [PATCH v9 10/26] target/arm/kvm: Retrieve writable ID reg map
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[09-16 16:45]** [PATCH v9 11/26] hw/arm/virt: Make sure virt_get_caches() keeps on reading CLIDR_EL1 as 0
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[09-16 16:45]** [PATCH v9 12/26] arm/kvm: Initialize isar.idregs[] with all writable host ID regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[09-16 16:45]** [PATCH v9 13/26] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
15. **[09-16 16:45]** [PATCH v9 14/26] target/arm/kvm: Implement SYSREG property setter and getter
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[09-16 16:45]** [PATCH v9 15/26] target/arm/kvm: Pass an Error handle to kvm_arch_init_vcpu
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[09-16 16:45]** [PATCH v9 16/26] target/arm/kvm: Apply SYSREG props to the final vcpu
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[09-16 16:45]** [PATCH v9 17/26] target/arm/kvm: Add consistency checking for SYSREG props
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[09-16 16:45]** [PATCH v9 18/26] target/arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
20. **[09-16 16:45]** [PATCH v9 19/26] target/arm/cpu-idregs.h.inc: Generate reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
21. **[09-16 16:45]** [PATCH v9 20/26] target/arm/kvm: Ignore and trace unexpected writable reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
22. **[09-16 16:45]** [PATCH v9 21/26] target/arm/kvm: add helper to test SYSREG props against a scratch vcpu
   - 发件人: Eric Auger <eric.auger@redhat.com>
23. **[09-16 16:45]** [PATCH v9 22/26] target/arm/kvm: Add an error handle to kvm_arm_create_scratch_host_vcpu
   - 发件人: Eric Auger <eric.auger@redhat.com>
24. **[09-16 16:45]** [PATCH v9 23/26] target/arm/kvm: Introduce kvm_arm_vcpu_prepare_init_features helper
   - 发件人: Eric Auger <eric.auger@redhat.com>
25. **[09-16 16:45]** [PATCH v9 24/26] target/arm/kvm: Introduce kvm_arm_create_init_scratch_vcpu()
   - 发件人: Eric Auger <eric.auger@redhat.com>
26. **[09-16 16:45]** [PATCH v9 25/26] arm-qmp-cmds: introspection for ID register props
   - 发件人: Eric Auger <eric.auger@redhat.com>
27. **[09-16 16:45]** [PATCH v9 26/26] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 9: [PATCH v19 00/20] KVM: arm64: CCA: Add basic plumbing for Realms

**📧 邮件数**: 25 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 20 Sep 2026 22:28:25 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:25, 26555 tokens)

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
14. **[09-20 22:28]** [PATCH v19 13/20] KVM: arm64: CCA: Add VCPU load/put for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
15. **[09-20 22:28]** [PATCH v19 14/20] KVM: arm64: CCA: Add bare minimal S2 operations for Realm
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
16. **[09-20 22:28]** [PATCH v19 15/20] KVM: arm64: CCA: Introduce Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
17. **[09-20 22:28]** [PATCH v19 16/20] KVM: arm64: CCA: Don't expose unsupported capabilities for realm guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
18. **[09-20 22:28]** [PATCH v19 17/20] KVM: arm64: CCA: WARN on injected undef exceptions
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
19. **[09-20 22:28]** [PATCH v19 18/20] KVM: arm64: CCA: Support timers in realm RECs
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
20. **[09-20 22:28]** [PATCH v19 19/20] KVM: arm64: CCA: Expose SVE VL register before VCPU finalization
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
21. **[09-20 22:28]** [PATCH v19 20/20] KVM: arm64: CCA: Control user register access for Realms
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
22. **[09-20 21:38]** Re: [PATCH v19 05/20] KVM: arm64: Track the type of VM in kvm_arch
   - 发件人: sashiko-bot@kernel.org
23. **[09-20 21:38]** Re: [PATCH v19 04/20] KVM: arm64: Avoid including linux/kvm_host.h
 in kvm_pgtable.h
   - 发件人: sashiko-bot@kernel.org
24. **[09-20 21:44]** Re: [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for
 protected guests
   - 发件人: sashiko-bot@kernel.org
25. **[09-20 23:24]** Re: [PATCH v19 02/20] KVM: arm64: Disable Steal time accounting for
 protected guests
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 10: [PATCH 0/4] KVM: arm64: Fix host access to the EL2 stacks

**📧 邮件数**: 23 | **👥 参与者**: 6 | **📅 开始时间**: Tue,  8 Sep 2026 12:07:09 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:20, 6643 tokens)

#### 📝 邮件列表

1. **[09-08 12:07]** [PATCH 0/4] KVM: arm64: Fix host access to the EL2 stacks
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-12 11:48]** [PATCH 0/4] KVM: arm64: Reduce overhead of full S2 teardown
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[09-12 11:48]** [PATCH 1/4] KVM: arm64: pgtable: Add Stage-2 unmap without TLBI primitive
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[09-14 14:44]** Re: [PATCH 0/4] KVM: arm64: Reduce overhead of full S2 teardown
   - 发件人: Shuai Xue <xueshuai@linux.alibaba.com>
5. **[09-14 09:14]** Re: [PATCH 0/4] KVM: arm64: Reduce overhead of full S2 teardown
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-14 09:48]** Re: [PATCH 1/4] KVM: arm64: pgtable: Add Stage-2 unmap without TLBI
 primitive
   - 发件人: Mark Rutland <mark.rutland@arm.com>
7. **[09-14 17:06]** Re: [PATCH 0/4] KVM: arm64: Reduce overhead of full S2 teardown
   - 发件人: Shuai Xue <xueshuai@linux.alibaba.com>
8. **[09-14 10:23]** Re: [PATCH 1/4] KVM: arm64: pgtable: Add Stage-2 unmap without TLBI
 primitive
   - 发件人: Mark Rutland <mark.rutland@arm.com>
9. **[09-15 15:25]** Re: [PATCH 0/4] KVM: arm64: Fix host access to the EL2 stacks
   - 发件人: Oliver Upton <oupton@kernel.org>
10. **[09-15 15:25]** Re: [PATCH 0/4] KVM: arm64: pKVM SVE vCPU init fixes
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[09-15 16:19]** Re: [PATCH 0/4] KVM: arm64: Reduce overhead of full S2 teardown
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[09-19 13:31]** [PATCH 0/4] KVM: arm64: vgic-v5: Random sparse fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[09-19 13:31]** [PATCH 1/4] KVM: arm64: vgic-v5: Drop __iomem attribute from {vmd,vpet}_base
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[09-19 13:31]** [PATCH 2/4] KVM: arm64: vgic-v5: Correctly reset h_lpi_ist to NULL
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[09-19 13:31]** [PATCH 3/4] KVM: arm64: vgic-v5: Tidy-up programming of vpe descriptor address
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[09-19 13:31]** [PATCH 4/4] KVM: arm64: vgic-v5: Correctly handle host ISTE __le32 conversion
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[09-19 12:39]** Re: [PATCH 4/4] KVM: arm64: vgic-v5: Correctly handle host ISTE
 __le32 conversion
   - 发件人: sashiko-bot@kernel.org
18. **[09-19 16:50]** Re: [PATCH 4/4] KVM: arm64: vgic-v5: Correctly handle host ISTE __le32 conversion
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[09-20 15:36]** Re: [PATCH 0/4] KVM: arm64: vgic-v5: Random sparse fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[09-20 15:42]** Re: [PATCH 4/4] KVM: arm64: vgic-v5: Correctly handle host ISTE
 __le32 conversion
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
21. **[09-20 15:42]** Re: [PATCH 3/4] KVM: arm64: vgic-v5: Tidy-up programming of vpe
 descriptor address
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
22. **[09-20 15:42]** Re: [PATCH 2/4] KVM: arm64: vgic-v5: Correctly reset h_lpi_ist to NULL
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
23. **[09-20 15:43]** Re: [PATCH 1/4] KVM: arm64: vgic-v5: Drop __iomem attribute from {vmd,vpet}_base
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 11: [PATCH v11 00/21] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 23 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 20 Sep 2026 20:15:41 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:23, 25635 tokens)

#### 📝 邮件列表

1. **[09-20 20:15]** [PATCH v11 00/21] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[09-20 20:15]** [PATCH v11 01/21] KVM: arm64: Serialize repeated vCPU
 initialization
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[09-20 20:15]** [PATCH v11 02/21] KVM: arm64: PMU: Stop updating MDCR_EL2.HPMN
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[09-20 20:15]** [PATCH v11 03/21] KVM: arm64: PMU: Freeze counter count after
 first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[09-20 20:15]** [PATCH v11 04/21] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[09-20 20:15]** [PATCH v11 05/21] KVM: arm64: PMU: Mask EL2-reserved bits on guest
 bitmap reads
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[09-20 20:15]** [PATCH v11 06/21] KVM: arm64: PMU: Keep implemented counter mask
 EL-independent
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[09-20 20:15]** [PATCH v11 07/21] KVM: arm64: PMU: Preserve EL2 bitmap state
 during migration
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[09-20 20:15]** [PATCH v11 08/21] Revert "KVM: arm64: PMU: Reload when resetting"
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
10. **[09-20 20:15]** [PATCH v11 09/21] KVM: arm64: PMU: Recreate events after MDCR_EL2
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
11. **[09-20 20:15]** [PATCH v11 10/21] KVM: arm64: PMU: Recreate events after PMCR_EL0
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
12. **[09-20 20:15]** [PATCH v11 11/21] KVM: arm64: PMU: Recreate events after userspace
 event writes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
13. **[09-20 20:15]** [PATCH v11 12/21] tools headers: Use u* types for bitfield helpers
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
14. **[09-20 20:15]** [PATCH v11 13/21] KVM: arm64: selftests: Cover PMU state in
 MDCR_EL2
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
15. **[09-20 20:15]** [PATCH v11 14/21] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
16. **[09-20 20:15]** [PATCH v11 15/21] KVM: arm64: Don't clear vcpu->cpu in
 kvm_arch_vcpu_put()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
17. **[09-20 20:15]** [PATCH v11 16/21] KVM: arm64: PMU: Protect the list of PMUs with
 RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
18. **[09-20 20:15]** [PATCH v11 17/21] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
19. **[09-20 20:15]** [PATCH v11 18/21] KVM: arm64: PMU: Pass the target CPU to
 kvm_pmu_probe_armpmu()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
20. **[09-20 20:16]** [PATCH v11 19/21] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
21. **[09-20 20:16]** [PATCH v11 20/21] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
22. **[09-20 20:16]** [PATCH v11 21/21] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
23. **[09-20 11:40]** Re: [PATCH v11 19/21] KVM: arm64: PMU: Implement
 fixed-counters-only emulation
   - 发件人: sashiko-bot@kernel.org

---

### Thread 12: [PATCH v10 00/20] KVM: arm64: PMU: Use multiple host PMUs

**📧 邮件数**: 23 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 14 Sep 2026 20:40:39 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:23, 24710 tokens)

#### 📝 邮件列表

1. **[09-14 20:40]** [PATCH v10 00/20] KVM: arm64: PMU: Use multiple host PMUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
2. **[09-14 20:40]** [PATCH v10 01/20] KVM: arm64: Serialize repeated vCPU
 initialization
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
3. **[09-14 20:40]** [PATCH v10 02/20] KVM: arm64: PMU: Stop updating MDCR_EL2.HPMN
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
4. **[09-14 20:40]** [PATCH v10 03/20] KVM: arm64: PMU: Freeze counter count after
 first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
5. **[09-14 20:40]** [PATCH v10 04/20] KVM: arm64: selftests: Test SET_NR_COUNTERS
 after first run
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
6. **[09-14 20:40]** [PATCH v10 05/20] KVM: arm64: PMU: Keep implemented counter mask
 EL-independent
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
7. **[09-14 20:40]** [PATCH v10 06/20] KVM: arm64: PMU: Preserve EL2 bitmap state
 during migration
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
8. **[09-14 20:40]** [PATCH v10 07/20] KVM: arm64: PMU: Recreate events after reset
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
9. **[09-14 20:40]** [PATCH v10 08/20] KVM: arm64: PMU: Recreate events after MDCR_EL2
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
10. **[09-14 20:40]** [PATCH v10 09/20] KVM: arm64: PMU: Recreate events after PMCR_EL0
 changes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
11. **[09-14 20:40]** [PATCH v10 10/20] KVM: arm64: PMU: Recreate events after userspace
 event writes
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
12. **[09-14 20:40]** [PATCH v10 11/20] tools headers: Use u* types for bitfield helpers
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
13. **[09-14 20:40]** [PATCH v10 12/20] KVM: arm64: selftests: Cover PMU state in
 MDCR_EL2
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
14. **[09-14 20:40]** [PATCH v10 13/20] arm64: errata: Require Apple IMPDEF PMUv3 traps
 on all CPUs
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
15. **[09-14 20:40]** [PATCH v10 14/20] KVM: arm64: Don't clear vcpu->cpu in
 kvm_arch_vcpu_put()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
16. **[09-14 20:40]** [PATCH v10 15/20] KVM: arm64: PMU: Protect the list of PMUs with
 RCU
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
17. **[09-14 20:40]** [PATCH v10 16/20] KVM: arm64: PMU: Pass the pPMU to
 kvm_map_pmu_event()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
18. **[09-14 20:40]** [PATCH v10 17/20] KVM: arm64: PMU: Pass the target CPU to
 kvm_pmu_probe_armpmu()
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
19. **[09-14 20:40]** [PATCH v10 18/20] KVM: arm64: PMU: Implement fixed-counters-only
 emulation
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
20. **[09-14 20:40]** [PATCH v10 19/20] KVM: arm64: PMU: Introduce FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
21. **[09-14 20:40]** [PATCH v10 20/20] KVM: arm64: selftests: Test
 PMU_V3_FIXED_COUNTERS_ONLY
   - 发件人: Akihiko Odaki <odaki@rsg.ci.i.u-tokyo.ac.jp>
22. **[09-14 12:14]** Re: [PATCH v10 07/20] KVM: arm64: PMU: Recreate events after reset
   - 发件人: sashiko-bot@kernel.org
23. **[09-14 12:24]** Re: [PATCH v10 06/20] KVM: arm64: PMU: Preserve EL2 bitmap state
 during migration
   - 发件人: sashiko-bot@kernel.org

---

### Thread 13: [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support

**📧 邮件数**: 22 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 14 Sep 2026 13:26:11 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:22, 22825 tokens)

#### 📝 邮件列表

1. **[09-14 13:26]** [PATCH v2 00/13] KVM: arm64: Add KVM_PRE_FAULT_MEMORY support
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-14 13:26]** [PATCH v2 01/13] arm64: Add ESR fault helpers
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
3. **[09-14 13:26]** [PATCH v2 02/13] KVM: arm64: Use ESR helpers in guest abort
 handling
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
4. **[09-14 13:26]** [PATCH v2 03/13] KVM: arm64: Propagate and use esr in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
5. **[09-14 13:26]** [PATCH v2 04/13] KVM: arm64: Propagate and use mmu in s2fd when
 handling guest aborts
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
6. **[09-14 13:26]** [PATCH v2 05/13] KVM: arm64: Propagate and use kvm_s2_fault_result
 on S2 fault
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
7. **[09-14 13:26]** [PATCH v2 06/13] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
8. **[09-14 13:26]** [PATCH v2 07/13] KVM: arm64: Propagate EHWPOISON in
 kvm_s2_fault_pin_pfn()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
9. **[09-14 13:26]** [PATCH v2 08/13] KVM: arm64: Pass walk flags to
 kvm_pgtable_get_leaf()
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
10. **[09-14 13:26]** [PATCH v2 09/13] KVM: arm64: Implement KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
11. **[09-14 13:26]** [PATCH v2 10/13] Documentation: KVM: document arm64
 KVM_PRE_FAULT_MEMORY
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
12. **[09-14 13:26]** [PATCH v2 11/13] KVM: selftests: Enable pre_fault_memory_test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
13. **[09-14 13:26]** [PATCH v2 12/13] KVM: selftests: Add option for different backing
 in pre-fault tests
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
14. **[09-14 13:26]** [PATCH v2 13/13] KVM: selftests: Add nested pre-fault test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
15. **[09-14 12:41]** Re: [PATCH v2 01/13] arm64: Add ESR fault helpers
   - 发件人: sashiko-bot@kernel.org
16. **[09-14 13:26]** Re: [PATCH v2 06/13] KVM: arm64: Size the stage-2 memcache from the
 fault MMU
   - 发件人: sashiko-bot@kernel.org
17. **[09-15 14:12]** Re: [PATCH v2 05/13] irqchip/gic-v3-its: Add support for the ITS
 emulation setup
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
18. **[09-15 15:24]** Re: [PATCH v2 06/13] KVM: arm64: Shadow the ITS command queue and
 setup emulation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
19. **[09-15 16:11]** Re: [PATCH v2 07/13] KVM: arm64: Restrict host access to the private
 ITS tables
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
20. **[09-15 16:27]** Re: [PATCH v2 08/13] KVM: arm64: Trap & emulate the ITS MAPD command
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
21. **[09-15 18:12]** Re: [PATCH v2 12/13] KVM: arm64: Prevent the host from programming
 new GITS_BASER tables
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
22. **[09-15 19:04]** Re: [PATCH v2 13/13] KVM: arm64: Implement HVC interface for ITS
 emulation setup
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 14: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 21 | **👥 参与者**: 5 | **📅 开始时间**: Tue, 15 Sep 2026 16:42:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:21, 11790 tokens)

#### 📝 邮件列表

1. **[09-15 16:42]** [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[09-15 16:42]** [PATCH v6 1/7] KVM: arm64: Use a variable for the canonical IPA in kvm_s2_fault_map()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[09-15 16:43]** [PATCH v6 2/7] KVM: arm64: nv: Introduce guest stage-2 tracking structures
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[09-15 16:43]** [PATCH v6 3/7] KVM: arm64: nv: Track guest stage-2 mapping creation
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[09-15 16:43]** [PATCH v6 4/7] KVM: arm64: nv: Track guest stage-2 mapping removal
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[09-15 16:43]** [PATCH v6 5/7] KVM: arm64: nv: Avoid full shadow stage-2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[09-15 16:43]** [PATCH v6 6/7] KVM: arm64: nv: Drop kvm_s2_mmu pointer from kvm_guest_s2_mapping
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[09-15 16:43]** [PATCH v6 7/7] KVM: arm64: Refactor kvm_unmap_gfn_range() with common variables
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[09-16 06:49]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
10. **[09-15 15:49]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Oliver Upton <oupton@kernel.org>
11. **[09-16 00:22]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
12. **[09-16 08:27]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
13. **[09-16 13:58]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
14. **[09-16 08:04]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[09-16 08:08]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[09-16 11:08]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
17. **[09-17 15:51]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
18. **[09-17 08:56]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[09-17 14:10]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
20. **[09-18 06:46]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
21. **[09-20 09:33]** Re: [PATCH v6 0/7] KVM: arm64: nv: Implement nested stage-2 reverse
 map
   - 发件人: Shuai Xue <xueshuai@linux.alibaba.com>

---

### Thread 15: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for shared buffers

**📧 邮件数**: 20 | **👥 参与者**: 6 | **📅 开始时间**: Fri,  4 Sep 2026 16:04:43 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:5 新:15, 4109 tokens)

#### 📝 邮件列表

1. **[09-04 16:04]** [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[09-04 16:04]** [PATCH v6 4/9] dma-direct: Align CoCo shared DMA allocations to the shared granule size
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[09-04 16:04]** [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
4. **[09-04 16:04]** [PATCH v6 8/9] arm64: realm: Add RHI helper to query IPA state change alignment
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
5. **[09-04 16:04]** [PATCH v6 9/9] arm64: realm: Expose the CCA shared granule size through mem_encrypt ops
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
6. **[09-16 17:12]** Re: [PATCH v6 8/9] arm64: realm: Add RHI helper to query IPA state
 change alignment
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
7. **[09-16 17:17]** Re: [PATCH v6 9/9] arm64: realm: Expose the CCA shared granule size
 through mem_encrypt ops
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
8. **[09-18 16:09]** Re: [PATCH v6 8/9] arm64: realm: Add RHI helper to query IPA state
 change alignment
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
9. **[09-18 15:16]** Re: [PATCH v6 4/9] dma-direct: Align CoCo shared DMA allocations to
 the shared granule size
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
10. **[09-18 16:16]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
11. **[09-18 17:23]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
12. **[09-18 12:36]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
13. **[09-18 17:39]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: =?UTF-8?Q?Christian_K=C3=B6nig?= <christian.koenig@amd.com>
14. **[09-18 17:52]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
15. **[09-18 13:53]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
16. **[09-18 13:57]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
17. **[09-18 18:10]** Re: [PATCH v6 0/9] coco: guest: Enforce host page-size alignment for
 shared buffers
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
18. **[09-19 20:27]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
19. **[09-19 18:35]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
20. **[09-20 12:54]** Re: [PATCH v6 7/9] dma-buf: system_heap: Enforce shared-granule
 alignment for cc-shared buffers
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

### Thread 16: [PATCH 0/7] KVM: arm64: pKVM host hypercall and GICv5 CPU interface fixes

**📧 邮件数**: 12 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 15 Sep 2026 13:38:39 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:12, 6822 tokens)

#### 📝 邮件列表

1. **[09-15 13:38]** [PATCH 0/7] KVM: arm64: pKVM host hypercall and GICv5 CPU interface fixes
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-15 13:38]** [PATCH 1/7] KVM: arm64: Reject the GICv5 CPU interface hypercalls under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-15 13:38]** [PATCH 2/7] KVM: arm64: Reject the stage-2 flush hypercalls under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-15 13:38]** [PATCH 3/7] KVM: arm64: Validate the host-provided vgic model in pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-15 13:38]** [PATCH 4/7] KVM: arm64: Validate the host vCPU's VM before reading it under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-15 13:38]** [PATCH 5/7] KVM: arm64: Pin the host vCPU before adjusting its PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-15 13:38]** [PATCH 6/7] KVM: arm64: vgic: Do not access the GICv5 CPU interface from EL1
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[09-15 13:38]** [PATCH 7/7] KVM: arm64: Fix stale VGICv3 comments in the nVHE world switch
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[09-15 15:02]** Re: [PATCH 1/7] KVM: arm64: Reject the GICv5 CPU interface hypercalls under pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[09-15 15:12]** Re: [PATCH 1/7] KVM: arm64: Reject the GICv5 CPU interface hypercalls
 under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
11. **[09-16 12:00]** Re: [PATCH 3/7] KVM: arm64: Validate the host-provided vgic model in
 pKVM
   - 发件人: Joey Gouly <joey.gouly@arm.com>
12. **[09-16 12:30]** Re: [PATCH 3/7] KVM: arm64: Validate the host-provided vgic model in pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 17: [PATCH v2 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable

**📧 邮件数**: 10 | **👥 参与者**: 5 | **📅 开始时间**: Fri, 18 Sep 2026 12:02:13 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:10, 8444 tokens)

#### 📝 邮件列表

1. **[09-18 12:02]** [PATCH v2 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable
   - 发件人: zjamg <ndaugoing@gmail.com>
2. **[09-18 12:02]** [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from AP list on disable
   - 发件人: zjamg <ndaugoing@gmail.com>
3. **[09-18 08:22]** Re: [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from AP
 list on disable
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-18 19:50]** Re: [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from AP
 list on disable
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
5. **[09-18 12:58]** Re: [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from AP
 list on disable
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-18 12:15]** Re: [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from
 AP list on disable
   - 发件人: Oliver Upton <oupton@kernel.org>
7. **[09-20 09:49]** [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
8. **[09-20 09:49]** [PATCH v3] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Yuchao Zhang <ndaugoing@gmail.com>
9. **[09-21 00:47]** Re: [PATCH v3 0/1] KVM: arm64: vgic: Drop last_lr_irq and serialize overflow EOI replay
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[09-21 00:54]** Re: [PATCH v2] KVM: arm64: vgic: Do not remove in-flight LPIs from AP list on disable
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 18: [PATCH 1/2] KVM: arm64: Report SMCCC_VERSION and SMCCC_ARCH_FEATURES as implemented

**📧 邮件数**: 10 | **👥 参与者**: 5 | **📅 开始时间**: Mon, 14 Sep 2026 13:58:26 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:10, 5207 tokens)

#### 📝 邮件列表

1. **[09-14 13:58]** [PATCH 1/2] KVM: arm64: Report SMCCC_VERSION and SMCCC_ARCH_FEATURES as implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 13:58]** [PATCH 2/2] KVM: arm64: selftests: Check the mandatory SMCCC_ARCH_FEATURES queries
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-15 15:25]** Re: [PATCH 0/2] KVM: arm64: Return -EINVAL for an empty SMCCC filter range at base 0
   - 发件人: Oliver Upton <oupton@kernel.org>
4. **[09-18 16:18]** [PATCH 0/2] Batch register access for live migration optimization
   - 发件人: Yize Wang <wangyize7@huawei.com>
5. **[09-18 16:18]** [PATCH 1/2] KVM: arm64: Add batch group constant and data structure to UAPI header
   - 发件人: Yize Wang <wangyize7@huawei.com>
6. **[09-18 16:18]** [PATCH 2/2] KVM: arm64: Add VGIC v3 batch register access implementation
   - 发件人: Yize Wang <wangyize7@huawei.com>
7. **[09-18 08:27]** Re: [PATCH 1/2] KVM: arm64: Add batch group constant and data
 structure to UAPI header
   - 发件人: sashiko-bot@kernel.org
8. **[09-18 08:33]** Re: [PATCH 2/2] KVM: arm64: Add VGIC v3 batch register access
 implementation
   - 发件人: sashiko-bot@kernel.org
9. **[09-18 13:08]** Re: [PATCH 0/2] Batch register access for live migration optimization
   - 发件人: Marc Zyngier <maz@kernel.org>
10. **[09-20 20:12]** Re: [RESEND][PATCH 0/2] Batch register access for live migration
 optimization
   - 发件人: Yize Wang <wangyize7@huawei.com>

---

### Thread 19: [PATCH v3 0/2] KVM: arm64: Fix spurious warn, null ptr deref on S2
 teardown race

**📧 邮件数**: 10 | **👥 参与者**: 6 | **📅 开始时间**: Tue, 01 Sep 2026 18:28:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:9, 4279 tokens)

#### 📝 邮件列表

1. **[09-01 18:28]** [PATCH v3 0/2] KVM: arm64: Fix spurious warn, null ptr deref on S2
 teardown race
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>
2. **[09-15 15:25]** Re: [PATCH v3 0/2] KVM: arm64: Fix spurious warn, null ptr deref on S2 teardown race
   - 发件人: Oliver Upton <oupton@kernel.org>
3. **[09-17 00:03]** [PATCH v3 0/2] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[09-17 00:03]** [PATCH v3 1/2] KVM: arm64: ptdump: Check the page tables aren't freed when accessing
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[09-17 00:03]** [PATCH v3 2/2] KVM: arm64: ptdump: Fix shadow ptdump sleep-in-atomic-context problem
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[09-16 23:16]** Re: [PATCH v3 1/2] KVM: arm64: ptdump: Check the page tables aren't
 freed when accessing
   - 发件人: sashiko-bot@kernel.org
7. **[09-17 16:46]** Re: [PATCH v3 0/2] KVM: arm64: ptdump: Shadow ptdump fixes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
8. **[09-17 09:11]** Re: [PATCH v3 1/2] KVM: arm64: ptdump: Check the page tables aren't
 freed when accessing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
9. **[09-17 20:30]** Re: [PATCH v3 1/2] KVM: arm64: ptdump: Check the page tables aren't
 freed when accessing
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
10. **[09-18 09:12]** Re: [PATCH v3 1/2] KVM: arm64: ptdump: Check the page tables aren't
 freed when accessing
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 20: [PATCH 0/3] KVM: Replace VCPU_RUN with KVM_RUN in comments and docs

**📧 邮件数**: 10 | **👥 参与者**: 4 | **📅 开始时间**: Tue, 15 Sep 2026 09:44:38 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:10, 3731 tokens)

#### 📝 邮件列表

1. **[09-15 09:44]** [PATCH 0/3] KVM: Replace VCPU_RUN with KVM_RUN in comments and docs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-15 09:44]** [PATCH 1/3] KVM: Fix comments that refer to the non-existent VCPU_RUN ioctl
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-15 09:44]** [PATCH 2/3] KVM: arm64: Fix references to the non-existent VCPU_RUN ioctl
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-15 09:44]** [PATCH 3/3] KVM: PPC: Book3S HV: Fix comment naming a non-existent KVM_VCPU_RUN ioctl
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-15 18:57]** Re: [PATCH 3/3] KVM: PPC: Book3S HV: Fix comment naming a
 non-existent KVM_VCPU_RUN ioctl
   - 发件人: Gautam Menghani <gautam@linux.ibm.com>
6. **[09-15 21:33]** Re: [PATCH 3/3] KVM: PPC: Book3S HV: Fix comment naming a
 non-existent KVM_VCPU_RUN ioctl
   - 发件人: Amit Machhiwal <amachhiw@linux.ibm.com>
7. **[09-17 19:45]** [PATCH 0/3] KVM: selftests: access_tracking_perf_test fixes and cleanups
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
8. **[09-17 19:45]** [PATCH 1/3] KVM: selftests: Fix access_tracking_perf_test for larger host page size
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
9. **[09-17 19:45]** [PATCH 2/3] KVM: selftests: Add missing newline to access_tracking_perf_test help
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
10. **[09-17 19:45]** [PATCH 3/3] KVM: selftests: Remove destroy_cgroup() from access_tracking_perf_test
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>

---

### Thread 21: [PATCH v2 0/2] KVM: arm64: Validate host pointers in __kvm_adjust_pc() under pKVM

**📧 邮件数**: 10 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 15 Sep 2026 08:04:16 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:10, 3085 tokens)

#### 📝 邮件列表

1. **[09-15 08:04]** [PATCH v2 0/2] KVM: arm64: Validate host pointers in __kvm_adjust_pc() under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-15 08:04]** [PATCH v2 1/2] KVM: arm64: Validate the host vCPU's VM before reading it under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-15 08:04]** [PATCH v2 2/2] KVM: arm64: Pin the host vCPU before adjusting its PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-15 08:34]** Re: [PATCH v2 1/2] KVM: arm64: Validate the host vCPU's VM before
 reading it under pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[09-15 08:41]** Re: [PATCH v2 2/2] KVM: arm64: Pin the host vCPU before adjusting
 its PC under pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
6. **[09-15 11:03]** Re: [PATCH v2 1/2] KVM: arm64: Validate the host vCPU's VM before
 reading it under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
7. **[09-15 11:17]** Re: [PATCH v2 1/2] KVM: arm64: Validate the host vCPU's VM before
 reading it under pKVM
   - 发件人: Joey Gouly <joey.gouly@arm.com>
8. **[09-15 11:23]** Re: [PATCH v2 1/2] KVM: arm64: Validate the host vCPU's VM before
 reading it under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[09-15 11:47]** Re: [PATCH v2 2/2] KVM: arm64: Pin the host vCPU before adjusting
 its PC under pKVM
   - 发件人: Joey Gouly <joey.gouly@arm.com>
10. **[09-15 12:00]** Re: [PATCH v2 2/2] KVM: arm64: Pin the host vCPU before adjusting its
 PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 22: [PATCH kvmtool 0/7] Fix --vcpu-affinity

**📧 邮件数**: 9 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 17 Sep 2026 16:49:25 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:9, 13012 tokens)

#### 📝 邮件列表

1. **[09-17 16:49]** [PATCH kvmtool 0/7] Fix --vcpu-affinity
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[09-17 16:49]** [PATCH kvmtool 1/7] arm64: Pass the number of elements as the first argument to calloc()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
3. **[09-17 16:49]** [PATCH kvmtool 2/7] arm64: Consistently treat vcpu_affinity_cpuset as dynamically allocated
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[09-17 16:49]** [PATCH kvmtool 3/7] arm64: Free the temporary cpumask in vcpu_affinity_parser()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
5. **[09-17 16:49]** [PATCH kvmtool 4/7] arm64/pmu: Consider kvmtool's affinity when searching for a PMU
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
6. **[09-17 16:49]** [PATCH kvmtool 5/7] Correctly apply --vcpu-affinity to the VCPU threads
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
7. **[09-17 16:49]** [RFC PATCH kvmtool 6/7] Introduce kvm_create_thread()
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
8. **[09-17 16:49]** [RFC PATCH kvmtool 7/7] Don't apply --vcpu-affinity to threads spawned from VCPUs
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
9. **[09-18 13:22]** Re: [PATCH kvmtool 0/7] Fix --vcpu-affinity
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 23: [PATCH v2 00/16] KVM: arm64: Confine protected VM vCPU state to EL2

**📧 邮件数**: 9 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  7 Sep 2026 07:59:45 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:6 新:3, 1960 tokens)

#### 📝 邮件列表

1. **[09-07 07:59]** [PATCH v2 00/16] KVM: arm64: Confine protected VM vCPU state to EL2
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-07 07:59]** [PATCH v2 10/17] KVM: arm64: Prevent host PC adjustments for protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-07 07:59]** [PATCH v2 14/17] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-11 13:58]** Re: [PATCH v2 14/17] KVM: arm64: Reject host access to protected VM private state
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[09-11 14:23]** Re: [PATCH v2 10/17] KVM: arm64: Prevent host PC adjustments for
 protected vCPUs
   - 发件人: Joey Gouly <joey.gouly@arm.com>
6. **[09-11 14:58]** Re: [PATCH v2 10/17] KVM: arm64: Prevent host PC adjustments for protected vCPUs
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[09-14 07:15]** Re: [PATCH v2 10/17] KVM: arm64: Prevent host PC adjustments for
 protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
8. **[09-14 07:21]** Re: [PATCH v2 10/17] KVM: arm64: Prevent host PC adjustments for
 protected vCPUs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
9. **[09-14 07:32]** Re: [PATCH v2 14/17] KVM: arm64: Reject host access to protected VM
 private state
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 24: [PATCH v2 0/4] KVM: arm64: vgic-its: Make the ITS table save reliable

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 15 Sep 2026 15:25:36 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:8, 5356 tokens)

#### 📝 邮件列表

1. **[09-15 15:25]** Re: [PATCH v2 0/4] KVM: arm64: vgic-its: Make the ITS table save reliable
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[09-17 22:42]** [PATCH v2 0/4] KVM: arm64: Properly advertise !FEAT_LPA2 for NV
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[09-17 22:42]** [PATCH v2 1/4] KVM: arm64: nv: Don't advertise FEAT_LPA2 for guest stage-1
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[09-17 22:42]** [PATCH v2 2/4] arm64: sysreg: Add TCR_EL2 to sysreg infrastructure
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[09-17 22:42]** [PATCH v2 3/4] KVM: arm64: Reset TCR_EL2 according to guest's E2H mode
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[09-17 22:42]** [PATCH v2 4/4] KVM: arm64: Convert TCR_EL2 to config-driven sanitisation
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[09-17 21:51]** Re: [PATCH v2 1/4] KVM: arm64: nv: Don't advertise FEAT_LPA2 for
 guest stage-1
   - 发件人: sashiko-bot@kernel.org
8. **[09-17 22:00]** Re: [PATCH v2 4/4] KVM: arm64: Convert TCR_EL2 to config-driven
 sanitisation
   - 发件人: sashiko-bot@kernel.org

---

### Thread 25: [PATCH v2 0/3] arm64: fix typos in comments

**📧 邮件数**: 8 | **👥 参与者**: 4 | **📅 开始时间**: Mon,  7 Sep 2026 10:14:31 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:7, 5901 tokens)

#### 📝 邮件列表

1. **[09-07 10:14]** [PATCH v2 0/3] arm64: fix typos in comments
   - 发件人: Hemanth Selam <hemanth.selam@gmail.com>
2. **[09-14 16:30]** [PATCH v2 0/3] 52-bit VA guest mode ID support
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
3. **[09-14 16:30]** [PATCH v2 1/3] KVM: arm64: selftests: Support five-level stage-1
 page tables
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
4. **[09-14 16:30]** [PATCH v2 2/3] KVM: arm64: selftests: Add 52-bit VA guest modes
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
5. **[09-14 16:30]** [PATCH v2 3/3] KVM: arm64: selftests: Test 52-bit guest virtual
 addresses
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
6. **[09-14 07:44]** Re: [PATCH v2 1/3] KVM: arm64: selftests: Support five-level
 stage-1 page tables
   - 发件人: sashiko-bot@kernel.org
7. **[09-14 13:04]** Re: [PATCH v2 0/3] arm64: fix typos in comments
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[09-14 13:04]** Re: [PATCH v2 0/3] KVM: selftests: arm64: Make sea_to_user skip cleanly
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 26: [PATCH v6 00/49] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 4 Sep 2026 11:34:16 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:3 新:3, 2815 tokens)

#### 📝 邮件列表

1. **[09-04 11:34]** [PATCH v6 00/49] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[09-04 11:38]** [PATCH v6 09/49] KVM: arm64: gic-v5: Create and manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[09-04 11:52]** [PATCH v6 35/49] KVM: arm64: gic-v5: Implement save/restore
 mechanisms for ISTs
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[09-14 13:04]** Re: [PATCH v6 00/49] KVM: arm64: Add GICv5 IRS support
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[09-19 10:25]** Re: [PATCH v6 09/49] KVM: arm64: gic-v5: Create and manage VM and VPE tables
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-19 10:36]** Re: [PATCH v6 35/49] KVM: arm64: gic-v5: Implement save/restore mechanisms for ISTs
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 27: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)

**📧 邮件数**: 6 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 13 Sep 2026 08:04:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:5, 1300 tokens)

#### 📝 邮件列表

1. **[09-13 08:04]** [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
2. **[09-16 17:39]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
3. **[09-16 17:56]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
4. **[09-17 08:58]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[09-17 10:03]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
6. **[09-17 11:36]** Re: [PATCH v18] arm64: mm: Handle Granule Protection Faults (GPFs)
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>

---

### Thread 28: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls under pKVM

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 14 Sep 2026 18:45:21 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:6, 1774 tokens)

#### 📝 邮件列表

1. **[09-14 18:45]** [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 17:58]** Re: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls
 under pKVM
   - 发件人: sashiko-bot@kernel.org
3. **[09-14 19:11]** Re: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls
 under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-15 10:20]** Re: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls under pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[09-15 10:24]** Re: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls under pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-15 10:30]** Re: [PATCH] KVM: arm64: Reject the stage-2 MMU pointer hypercalls
 under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 29: [PATCH v2] KVM: arm64: Fix protected VM fault on system with pages
 larger than 4K

**📧 邮件数**: 6 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 14 Sep 2026 08:58:39 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:6, 1550 tokens)

#### 📝 邮件列表

1. **[09-14 08:58]** [PATCH v2] KVM: arm64: Fix protected VM fault on system with pages
 larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-14 08:13]** Re: [PATCH v2] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: sashiko-bot@kernel.org
3. **[09-14 09:19]** Re: [PATCH v2] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[09-14 09:32]** Re: [PATCH v2] KVM: arm64: Fix protected VM fault on system with pages larger than 4K
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[09-14 09:40]** Re: [PATCH v2] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
6. **[09-14 09:41]** Re: [PATCH v2] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 30: [PATCH v1 0/4] KVM: arm64: Honour KVM_VM_TYPE_ARM_IPA_SIZE under pKVM

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 17 Sep 2026 10:18:22 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:5, 3796 tokens)

#### 📝 邮件列表

1. **[09-17 10:18]** [PATCH v1 0/4] KVM: arm64: Honour KVM_VM_TYPE_ARM_IPA_SIZE under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-17 10:18]** [PATCH v1 1/4] KVM: arm64: Move the IPA limit rule into kvm_get_ipa_max()
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-17 10:18]** [PATCH v1 2/4] KVM: arm64: Check PGD alignment when creating a pVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-17 10:18]** [PATCH v1 3/4] KVM: arm64: Honour the requested IPA size under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-17 10:18]** [PATCH v1 4/4] KVM: arm64: selftests: Free the VM when the GIC device probe fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 31: [PATCH v7 1/3] KVM: arm64: Block host-initiated FF-A direct responses

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 14 Sep 2026 17:23:19 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:5, 960 tokens)

#### 📝 邮件列表

1. **[09-14 17:23]** Re: [PATCH v7 1/3] KVM: arm64: Block host-initiated FF-A direct responses
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 17:32]** Re: [PATCH v7 2/3] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ in
 host handler
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-14 18:41]** Re: [PATCH v7 3/3] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ2 in
 host handler
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-14 20:22]** Re: [PATCH v7 0/3] KVM: arm64: Support FF-A direct messaging interfaces
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
5. **[09-15 10:24]** Re: [PATCH v7 2/3] KVM: arm64: Support FFA_MSG_SEND_DIRECT_REQ in
 host handler
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 32: [PATCH v5 00/15] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 10 Sep 2026 19:34:53 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:2, 804 tokens)

#### 📝 邮件列表

1. **[09-10 19:34]** [PATCH v5 00/15] coco/TSM: Host-side Arm CCA IDE setup via connect/disconnect callbacks
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[09-10 19:35]** [PATCH v5 11/15] coco: host: arm64: Connect RMM pdev streams for IDE devices
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[09-18 02:55]** Re: [PATCH v5 11/15] coco: host: arm64: Connect RMM pdev streams for
 IDE devices
   - 发件人: Ankit Agrawal <ankita@nvidia.com>
4. **[09-18 11:37]** Re: [PATCH v5 11/15] coco: host: arm64: Connect RMM pdev streams
 for IDE devices
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

### Thread 33: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 11 Sep 2026 11:47:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:2 新:2, 708 tokens)

#### 📝 邮件列表

1. **[09-11 11:47]** [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-13 11:00]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[09-15 19:51]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
4. **[09-17 11:59]** Re: [PATCH v3] KVM: arm64: Trap guest MPAM accesses whenever MPAM is implemented
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 34: [PATCH v3] KVM: arm64: Fix protected VM fault on system with pages
 larger than 4K

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 15 Sep 2026 10:16:06 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:4, 1899 tokens)

#### 📝 邮件列表

1. **[09-15 10:16]** [PATCH v3] KVM: arm64: Fix protected VM fault on system with pages
 larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-15 12:17]** Re: [PATCH v3] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
3. **[09-17 09:25]** Re: [PATCH v3] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
4. **[09-17 09:49]** Re: [PATCH v3] KVM: arm64: Fix protected VM fault on system with
 pages larger than 4K
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>

---

### Thread 35: [PATCH 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 18 Sep 2026 10:46:19 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 2084 tokens)

#### 📝 邮件列表

1. **[09-18 10:46]** [PATCH 0/1] KVM: arm64: vgic: fix UAF/crash on remote LPI disable
   - 发件人: zjamg <ndaugoing@gmail.com>
2. **[09-18 10:46]** [PATCH 1/1] KVM: arm64: vgic: Do not remove in-flight LPIs from AP list on disable
   - 发件人: zjamg <ndaugoing@gmail.com>
3. **[09-18 02:58]** Re: [PATCH 1/1] KVM: arm64: vgic: Do not remove in-flight LPIs from
 AP list on disable
   - 发件人: sashiko-bot@kernel.org

---

### Thread 36: [PATCH v2] arm64: clear_page[s] using memset

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 16 Sep 2026 12:03:56 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 2166 tokens)

#### 📝 邮件列表

1. **[09-16 12:03]** [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Linus Walleij <linusw@kernel.org>
2. **[09-16 16:28]** Re: [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[09-16 16:54]** Re: [PATCH v2] arm64: clear_page[s] using memset
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 37: [PATCH v2] KVM: selftests: fix steal_time for arm64 with host page size > 4K

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 14 Sep 2026 15:10:13 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 1225 tokens)

#### 📝 邮件列表

1. **[09-14 15:10]** [PATCH v2] KVM: selftests: fix steal_time for arm64 with host page size > 4K
   - 发件人: Sebastian Ott <sebott@redhat.com>
2. **[09-15 09:50]** Re: [PATCH v2] KVM: selftests: fix steal_time for arm64 with host
 page size > 4K
   - 发件人: Zenghui Yu <zenghui.yu@linux.dev>
3. **[09-15 15:25]** Re: [PATCH v2] KVM: selftests: fix steal_time for arm64 with host page size > 4K
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 38: [PATCH] KVM: arm64: Don't WARN on an unknown VM ioctl in protected mode

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 14 Sep 2026 10:38:38 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 577 tokens)

#### 📝 邮件列表

1. **[09-14 10:38]** [PATCH] KVM: arm64: Don't WARN on an unknown VM ioctl in protected mode
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 10:42]** Re: [PATCH] KVM: arm64: Don't WARN on an unknown VM ioctl in
 protected mode
   - 发件人: Suzuki K Poulose <suzuki.poulose@arm.com>
3. **[09-15 15:25]** Re: [PATCH] KVM: arm64: Don't WARN on an unknown VM ioctl in protected mode
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 39: [PATCH] KVM: arm64: Pin the host vCPU before adjusting its PC under pKVM

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 14 Sep 2026 07:51:36 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:3, 1098 tokens)

#### 📝 邮件列表

1. **[09-14 07:51]** [PATCH] KVM: arm64: Pin the host vCPU before adjusting its PC under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 07:05]** Re: [PATCH] KVM: arm64: Pin the host vCPU before adjusting its PC
 under pKVM
   - 发件人: sashiko-bot@kernel.org
3. **[09-14 09:13]** Re: [PATCH] KVM: arm64: Pin the host vCPU before adjusting its PC
 under pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 40: [PATCH] KVM: arm64: Fix AArch32 DBGBXVR<n> handling

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 19 Sep 2026 11:11:14 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 211 tokens)

#### 📝 邮件列表

1. **[09-19 11:11]** Re: [PATCH] KVM: arm64: Fix AArch32 DBGBXVR<n> handling
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[09-19 11:16]** Re: [PATCH] KVM: arm64: Fix AArch32 DBGBXVR<n> handling
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 41: [PATCH] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 18 Sep 2026 13:05:53 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 1794 tokens)

#### 📝 邮件列表

1. **[09-18 13:05]** [PATCH] KVM: arm64: Restore the VM's feature bitmap when kvm_setup_vcpu() fails
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-18 17:10]** Re: [PATCH] KVM: arm64: Restore the VM's feature bitmap when
 kvm_setup_vcpu() fails
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 42: [PATCH v1] KVM: arm64: Disable stage-2 ptdump of pKVM

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 17 Sep 2026 09:15:10 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 506 tokens)

#### 📝 邮件列表

1. **[09-17 09:15]** [PATCH v1] KVM: arm64: Disable stage-2 ptdump of pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-17 11:13]** Re: [PATCH v1] KVM: arm64: Disable stage-2 ptdump of pKVM
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 43: [PATCH v4 0/2] KVM: arm64: nv: Shadow S2 life-cycle fixes

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 11 Sep 2026 17:22:01 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 354 tokens)

#### 📝 邮件列表

1. **[09-11 17:22]** [PATCH v4 0/2] KVM: arm64: nv: Shadow S2 life-cycle fixes
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[09-15 15:25]** Re: [PATCH v4 0/2] KVM: arm64: nv: Shadow S2 life-cycle fixes
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 44: [PATCH v20 02/14] KVM: arm64: Fix FGT mapping for
 HFGITR_EL2.nGCSEPP

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 01 Sep 2026 22:47:00 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 327 tokens)

#### 📝 邮件列表

1. **[09-01 22:47]** [PATCH v20 02/14] KVM: arm64: Fix FGT mapping for
 HFGITR_EL2.nGCSEPP
   - 发件人: Mark Brown <broonie@kernel.org>
2. **[09-15 15:25]** Re: (subset) [PATCH v20 02/14] KVM: arm64: Fix FGT mapping for HFGITR_EL2.nGCSEPP
   - 发件人: Oliver Upton <oupton@kernel.org>

---

### Thread 45: [PATCH v1] KVM: arm64: Advertise MMFR0 TGRAN for pVMs

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 13 Sep 2026 21:31:08 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 464 tokens)

#### 📝 邮件列表

1. **[09-13 21:31]** [PATCH v1] KVM: arm64: Advertise MMFR0 TGRAN for pVMs
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[09-14 14:25]** Re: [PATCH v1] KVM: arm64: Advertise MMFR0 TGRAN for pVMs
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 46: [PATCH] KVM: selftests: Fix VM leak in early return

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sun,  6 Sep 2026 03:41:43 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 317 tokens)

#### 📝 邮件列表

1. **[09-06 03:41]** [PATCH] KVM: selftests: Fix VM leak in early return
   - 发件人: Tharit Tangkijwanichakul <tharitt97@gmail.com>
2. **[09-14 13:04]** Re: [PATCH] KVM: selftests: Fix VM leak in early return
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 47: [PATCH v9 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon,  7 Sep 2026 17:19:22 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 530 tokens)

#### 📝 邮件列表

1. **[09-07 17:19]** [PATCH v9 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[09-14 13:04]** Re: [PATCH v9 0/7] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 48: [PATCH v2] KVM: arm64: Fix kvm_get_vtcr() kernel-doc

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 10 Sep 2026 21:05:28 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 313 tokens)

#### 📝 邮件列表

1. **[09-10 21:05]** [PATCH v2] KVM: arm64: Fix kvm_get_vtcr() kernel-doc
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>
2. **[09-14 13:04]** Re: [PATCH v2] KVM: arm64: Fix kvm_get_vtcr() kernel-doc
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 49: [PATCH] Documentation: KVM: Fix the struct kvm_arm_device_addr name

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat,  5 Sep 2026 11:06:55 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 330 tokens)

#### 📝 邮件列表

1. **[09-05 11:06]** [PATCH] Documentation: KVM: Fix the struct kvm_arm_device_addr name
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>
2. **[09-14 13:04]** Re: [PATCH] Documentation: KVM: Fix the struct kvm_arm_device_addr name
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 50: [PATCH] Documentation: KVM: Fix the event_source sysfs path in the PMU attribute description

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Sat,  5 Sep 2026 10:58:49 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 358 tokens)

#### 📝 邮件列表

1. **[09-05 10:58]** [PATCH] Documentation: KVM: Fix the event_source sysfs path in the PMU attribute description
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>
2. **[09-14 13:04]** Re: [PATCH] Documentation: KVM: Fix the event_source sysfs path in the PMU attribute description
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 51: [PATCH v4 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  1 Sep 2026 15:03:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 692 tokens)

#### 📝 邮件列表

1. **[09-01 15:03]** [PATCH v4 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 13:04]** Re: [PATCH v4 00/11] KVM: arm64: Restore type-checking across the host/hyp hypercall boundary
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 52: [PATCH] KVM: arm64: Fix the KVM_ARM_PREFERRED_TARGET documentation

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 31 Aug 2026 17:28:15 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 326 tokens)

#### 📝 邮件列表

1. **[08-31 17:28]** [PATCH] KVM: arm64: Fix the KVM_ARM_PREFERRED_TARGET documentation
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>
2. **[09-14 13:03]** Re: [PATCH] KVM: arm64: Fix the KVM_ARM_PREFERRED_TARGET documentation
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 53: [PATCH 6/8] KVM: selftests: Enable pre_fault_memory_test for arm64

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 10 Sep 2026 19:52:35 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 279 tokens)

#### 📝 邮件列表

1. **[09-10 19:52]** Re: [PATCH 6/8] KVM: selftests: Enable pre_fault_memory_test for arm64
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[09-14 12:17]** Re: [PATCH 6/8] KVM: selftests: Enable pre_fault_memory_test for
 arm64
   - 发件人: Lorenzo Stoakes (ARM) <ljs@kernel.org>

---

### Thread 54: [PATCH] KVM: arm64: Fix AArch32 DBGBXVR<n> handling

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 19 Sep 2026 07:18:32 +0200

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 107 tokens)

#### 📝 邮件列表

1. **[09-19 07:18]** Re: [PATCH] KVM: arm64: Fix AArch32 DBGBXVR<n> handling
   - 发件人: Karl Mehltretter <kmehltretter@gmail.com>

---

### Thread 55: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 18 Sep 2026 15:55:03 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 170 tokens)

#### 📝 邮件列表

1. **[09-18 15:55]** Re: [PATCH 00/22] KVM: arm64: nv: Implement FEAT_HAFDBS, FEAT_HAFT
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 56: [PATCH] KVM: arm64: vgic-its: Update GITS_CTLR.Enabled under its_lock

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu, 17 Sep 2026 17:20:20 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 849 tokens)

#### 📝 邮件列表

1. **[09-17 17:20]** [PATCH] KVM: arm64: vgic-its: Update GITS_CTLR.Enabled under its_lock
   - 发件人: Fuad Tabba <fuad.tabba@linux.dev>

---

### Thread 57: [PATCH v4] arm64: errata: Add NXP iMX8QM workaround for A53
 cache coherency issue

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 15 Sep 2026 23:04:18 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 119 tokens)

#### 📝 邮件列表

1. **[09-15 23:04]** Re: [PATCH v4] arm64: errata: Add NXP iMX8QM workaround for A53
 cache coherency issue
   - 发件人: Peng Fan <peng.fan@oss.nxp.com>

---

### Thread 58: [PATCH v4] arm64: errata: Add NXP iMX8QM workaround for A53
 cache coherency issue

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 15 Sep 2026 23:02:54 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 112 tokens)

#### 📝 邮件列表

1. **[09-15 23:02]** Re: [PATCH v4] arm64: errata: Add NXP iMX8QM workaround for A53
 cache coherency issue
   - 发件人: Peng Fan <peng.fan@oss.nxp.com>

---

### Thread 59: [PATCH v16 44/45] KVM: arm64: CCA: Require ICH_HCR_EL2.TDIR for
 realms

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 15 Sep 2026 21:23:49 +0900

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 670 tokens)

#### 📝 邮件列表

1. **[09-15 21:23]** Re: [PATCH v16 44/45] KVM: arm64: CCA: Require ICH_HCR_EL2.TDIR for
 realms
   - 发件人: Kohei Enju <enju.kohei@fujitsu.com>

---

### Thread 60: [PATCH v2] KVM: arm64: Advertise MMFR0 TGRAN for pVMs

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Tue, 15 Sep 2026 09:44:38 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 489 tokens)

#### 📝 邮件列表

1. **[09-15 09:44]** [PATCH v2] KVM: arm64: Advertise MMFR0 TGRAN for pVMs
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 61: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 14 Sep 2026 15:13:30 +0200 (CEST)

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 141 tokens)

#### 📝 邮件列表

1. **[09-14 15:13]** Re: [PATCH] KVM: selftests: fix steal_time for arm64 with host page
 size > 4K
   - 发件人: Sebastian Ott <sebott@redhat.com>

---

### Thread 62: [PATCH] KVM: arm64: vgic-its: Reword the comment on a collection-less ITE

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 14 Sep 2026 13:03:58 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 142 tokens)

#### 📝 邮件列表

1. **[09-14 13:03]** Re: [PATCH] KVM: arm64: vgic-its: Reword the comment on a collection-less ITE
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 RFC

共 4 个 thread

---

### Thread 1: [RFC PATCH 00/46] Orphaned Virtual Machines

**📧 邮件数**: 40 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 20 Sep 2026 15:36:04 -0400

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:40, 127892 tokens)

#### 📝 邮件列表

1. **[09-20 15:36]** [RFC PATCH 00/46] Orphaned Virtual Machines
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
2. **[09-20 15:36]** [RFC PATCH 01/46] KVM: luo: Delegate VM creation type to kvm_arch_vm_luo_preserve
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
3. **[09-20 15:36]** [RFC PATCH 02/46] KVM: arm64: Split demux_c15_{get,set}_val from userspace accessors
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
4. **[09-20 15:36]** [RFC PATCH 03/46] KVM: arm64: Split kvm_sys_reg_{get,set}_user from kernel accessors
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
5. **[09-20 15:36]** [RFC PATCH 04/46] x86/mm/ident_map: Add force_pte to support 4K PTE identity mappings
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
6. **[09-20 15:36]** [RFC PATCH 05/46] arm64: mm: Add trans_pgd_map_range() support
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
7. **[09-20 15:36]** [RFC PATCH 06/46] x86/smp: Skip offline CPUs for REBOOT_VECTOR in native_stop_other_cpus()
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
8. **[09-20 15:36]** [RFC PATCH 07/46] KVM: luo: Support vCPU file preservation across live updates
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
9. **[09-20 15:36]** [RFC PATCH 08/46] KVM: x86: Add x86 vCPU LUO preservation ABI and register helpers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
10. **[09-20 15:36]** [RFC PATCH 09/46] KVM: x86: Implement architectural vCPU state preservation via LUO
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
11. **[09-20 15:36]** [RFC PATCH 10/46] KVM: arm64: Implement architectural vCPU state preservation via LUO
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
12. **[09-20 15:36]** [RFC PATCH 11/46] liveupdate: Define CPU preservation linker sections
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
13. **[09-20 15:36]** [RFC PATCH 12/46] liveupdate: Add liveupdate_session_name() helper
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
14. **[09-20 15:36]** [RFC PATCH 13/46] cpu_preserve: Add physical CPU preservation ABI and core API headers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
15. **[09-20 15:36]** [RFC PATCH 14/46] cpu_preserve: Add core physical CPU preservation state and park loop
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
16. **[09-20 15:36]** [RFC PATCH 15/46] cpu_preserve: Add physical CPU preservation lifecycle and build rules
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
17. **[09-20 15:36]** [RFC PATCH 16/46] liveupdate: cpu_preserve: Add sysfs interface
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
18. **[09-20 15:36]** [RFC PATCH 17/46] liveupdate: cpu_preserve: Add isolated address space management API
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
19. **[09-20 15:36]** [RFC PATCH 18/46] liveupdate: cpu_preserve: Add LUO file handler for preserved physical CPUs
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
20. **[09-20 15:36]** [RFC PATCH 19/46] x86: liveupdate: Add low-level physical CPU preservation assembly
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
21. **[09-20 15:36]** [RFC PATCH 20/46] x86: liveupdate: Add physical CPU preservation context and page table support
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
22. **[09-20 15:36]** [RFC PATCH 21/46] selftests: liveupdate: Add physical CPU preservation unit tests
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
23. **[09-20 15:36]** [RFC PATCH 22/46] selftests: liveupdate: Add physical CPU preservation live update tests
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
24. **[09-20 15:36]** [RFC PATCH 23/46] Documentation: liveupdate: Add physical CPU preservation documentation
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
25. **[09-20 15:36]** [RFC PATCH 24/46] MAINTAINERS: Add entry for KVM Caretaker
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
26. **[09-20 15:36]** [RFC PATCH 25/46] arm64: liveupdate: Add support for physical CPU preservation
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
27. **[09-20 15:36]** [RFC PATCH 26/46] oncore: Add on-core KHO ABI and public framework headers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
28. **[09-20 15:36]** [RFC PATCH 27/46] oncore: Implement on-core session lifecycle and scheduling loop
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
29. **[09-20 15:36]** [RFC PATCH 28/46] KVM: caretaker: Add Caretaker control block and architecture ops headers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
30. **[09-20 15:36]** [RFC PATCH 29/46] KVM: caretaker: Implement Caretaker session memory mapping helpers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
31. **[09-20 15:36]** [RFC PATCH 30/46] KVM: caretaker: Integrate Caretaker vCPU detach, attach, and cancel with KVM
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
32. **[09-20 15:36]** [RFC PATCH 31/46] KVM: caretaker: Add generic KHO ABI telemetry and debugfs reporting
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
33. **[09-20 15:36]** [RFC PATCH 32/46] KVM: x86: Add TDP MMU KHO preservation helpers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
34. **[09-20 15:36]** [RFC PATCH 33/46] KVM: x86: Add Caretaker x86 KHO ABI and runtime context headers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
35. **[09-20 15:36]** [RFC PATCH 34/46] KVM: x86: Implement Caretaker LAPIC timer and interrupt injection
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
36. **[09-20 15:36]** [RFC PATCH 35/46] KVM: x86: Implement Caretaker VM-exit dispatch and instruction decoders
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
37. **[09-20 15:36]** [RFC PATCH 36/46] KVM: x86: Implement Caretaker run loop and LUO detach/attach lifecycle
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
38. **[09-20 15:36]** [RFC PATCH 37/46] KVM: VMX: Add Caretaker VMX assembly guest entry/exit routine and helpers
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
39. **[09-20 15:36]** [RFC PATCH 38/46] KVM: VMX: Implement Caretaker VMX VMCS lifecycle and exit dispatch
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>
40. **[09-20 15:36]** [RFC PATCH 39/46] KVM: VMX: Integrate Caretaker VMX detach serialization and KVM registration
   - 发件人: Pasha Tatashin <pasha.tatashin@soleen.com>

---

### Thread 2: [RFC PATCH 0/5] KVM: arm64: New PTE dirty-page encoding, HAFDBS new usage

**📧 邮件数**: 23 | **👥 参与者**: 4 | **📅 开始时间**: Tue,  1 Sep 2026 18:15:51 +0100

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:7 新:16, 7167 tokens)

#### 📝 邮件列表

1. **[09-01 18:15]** [RFC PATCH 0/5] KVM: arm64: New PTE dirty-page encoding, HAFDBS new usage
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[09-01 18:15]** [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[09-01 18:15]** [RFC PATCH 2/5] KVM: arm64: Add KVM_PGTABLE_PROT_DIRTY
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[09-01 18:15]** [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on migration
   - 发件人: Leonardo Bras <leo.bras@arm.com>
5. **[09-12 13:24]** Re: [RFC PATCH 0/5] KVM: arm64: New PTE dirty-page encoding, HAFDBS new usage
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[09-13 10:00]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[09-13 10:09]** Re: [RFC PATCH 2/5] KVM: arm64: Add KVM_PGTABLE_PROT_DIRTY
   - 发件人: Marc Zyngier <maz@kernel.org>
8. **[09-15 16:31]** Re: [RFC PATCH 0/5] KVM: arm64: New PTE dirty-page encoding, HAFDBS new usage
   - 发件人: Leonardo Bras <leo.bras@arm.com>
9. **[09-15 18:12]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
10. **[09-15 18:33]** Re: [RFC PATCH 2/5] KVM: arm64: Add KVM_PGTABLE_PROT_DIRTY
   - 发件人: Leonardo Bras <leo.bras@arm.com>
11. **[09-15 17:10]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on
 migration
   - 发件人: Oliver Upton <oupton@kernel.org>
12. **[09-15 17:37]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from
 S2AP_W to DBM
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[09-16 09:30]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Marc Zyngier <maz@kernel.org>
14. **[09-16 12:22]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
15. **[09-16 13:20]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[09-16 14:03]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
17. **[09-16 14:25]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from S2AP_W to DBM
   - 发件人: Leonardo Bras <leo.bras@arm.com>
18. **[09-16 15:00]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on migration
   - 发件人: Leonardo Bras <leo.bras@arm.com>
19. **[09-16 16:27]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on
 migration
   - 发件人: Oliver Upton <oupton@kernel.org>
20. **[09-17 14:40]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on migration
   - 发件人: Leonardo Bras <leo.bras@arm.com>
21. **[09-18 17:39]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from
 S2AP_W to DBM
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
22. **[09-18 19:43]** Re: [RFC PATCH 1/5] KVM: arm64: pgtables: Change write bit from
 S2AP_W to DBM
   - 发件人: Tian Zheng <zhengtian10@huawei.com>
23. **[09-18 19:58]** Re: [RFC PATCH 5/5] KVM: arm64: Enable HAFDBS for guests not on
 migration
   - 发件人: Tian Zheng <zhengtian10@huawei.com>

---

### Thread 3: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing

**📧 邮件数**: 17 | **👥 参与者**: 4 | **📅 开始时间**: Wed, 02 Sep 2026 18:45:42 +0530

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:11 新:6, 4480 tokens)

#### 📝 邮件列表

1. **[09-02 18:45]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
2. **[09-02 22:09]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
3. **[09-02 20:56]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
4. **[09-03 11:18]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
5. **[09-03 14:17]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
6. **[09-07 15:15]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
7. **[09-07 09:52]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
8. **[09-09 15:39]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
9. **[09-09 09:46]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
10. **[09-10 09:52]** RE: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Tian, Kevin <kevin.tian@intel.com>
11. **[09-10 09:46]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
12. **[09-15 07:13]** RE: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Tian, Kevin <kevin.tian@intel.com>
13. **[09-15 10:43]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
14. **[09-16 05:54]** RE: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Tian, Kevin <kevin.tian@intel.com>
15. **[09-16 09:39]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
16. **[09-17 02:25]** RE: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Tian, Kevin <kevin.tian@intel.com>
17. **[09-18 13:54]** Re: [RFC PATCH v4 03/16] iommu/arm-smmu-v3: Add initial pSMMU realm
 viommu plumbing
   - 发件人: Baolu Lu <baolu.lu@linux.intel.com>

---

### Thread 4: [RFC PATCH v8 15/20] target/arm/kvm: Ignore and trace unexpected
 writable reserved fields

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 11 Sep 2026 13:50:53 +0000

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:1 新:1, 232 tokens)

#### 📝 邮件列表

1. **[09-11 13:50]** RE: [RFC PATCH v8 15/20] target/arm/kvm: Ignore and trace unexpected
 writable reserved fields
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
2. **[09-14 09:54]** Re: [RFC PATCH v8 15/20] target/arm/kvm: Ignore and trace unexpected
 writable reserved fields
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.3, round #1

**📧 邮件数**: 2 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 19 Sep 2026 11:33:44 -0700

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:2, 1743 tokens)

#### 📝 邮件列表

1. **[09-19 11:33]** [GIT PULL] KVM/arm64 fixes for 7.3, round #1
   - 发件人: Oliver Upton <oupton@kernel.org>
2. **[09-19 11:36]** Re: [GIT PULL] KVM/arm64 fixes for 7.3, round #1
   - 发件人: Oliver Upton <oupton@kernel.org>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvmarm:next 31/83]
 arch/arm64/kvm/vgic/vgic-irs-v5.c:1016:8: warning: variable 'addr' set but
 not used

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 16 Sep 2026 05:48:32 +0800

#### 🤖 AI 总结

[AI 总结失败: Error code: 429 - {'error': {'message': 'You have no credits remaining. Add credits to continue using the API at https://platform.openai.com/settings/organization/billing/.', 'type': 'insufficient_quota', 'param': None, 'code': 'credit_balance_exhausted'}}]
策略: 完整 thread (历史:0 新:1, 643 tokens)

#### 📝 邮件列表

1. **[09-16 05:48]** [kvmarm:next 31/83]
 arch/arm64/kvm/vgic/vgic-irs-v5.c:1016:8: warning: variable 'addr' set but
 not used
   - 发件人: kernel test robot <lkp@intel.com>

---

