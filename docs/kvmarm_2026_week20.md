# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-05-18 00:50:26

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 246
- **总 Thread 数**: 25
- **大型 Thread** (>20封): 5 个

### 分类分布

- **PATCH**: 20 threads (208 邮件)
- **RFC**: 3 threads (35 邮件)
- **GIT PULL**: 1 threads (2 邮件)
- **Other**: 1 threads (1 邮件)

---

## 📌 PATCH

共 20 个 thread

---

### Thread 1: [PATCH v14 00/44] arm64: Support for Arm CCA in KVM

**📧 邮件数**: 47 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 13 May 2026 14:17:08 +0100

#### 🤖 AI 总结

本邮件线程讨论的主题是对 ARM64 架构下 KVM 的一系列补丁，主要集中在支持 Arm CCA（Confidential Compute Architecture）和相关的 RMI（Realm Management Interface）功能。以下是讨论的主要内容总结：

1. **原始补丁内容**：
   该补丁系列（PATCH v14 00/44）旨在为 KVM 添加对 Arm CCA 的支持，允许在 KVM 中运行受保护的虚拟机。补丁内容包括对 RMM（Realm Management Monitor）和 RMI API 的更新，以支持新的特性和功能。

2. **历史讨论要点**：
   之前的讨论主要集中在如何实现 RMM v2.0 的功能，包括对 RMI 的支持、状态管理、内存管理等。补丁中提到的主要变化包括更新 RMI 定义、简化用户 API、支持状态 RMI 操作（SRO）等。

3. **本周的新讨论与进展**：
   - 本周的讨论中，补丁更新了 RMM 的接口，增加了对 SRO 的支持，允许在多个 SMC 调用中完成操作。
   - 讨论中还提到，RMM 现在能够处理对 VGIC（虚拟通用中断控制器）的支持，并且在处理 MMIO（内存映射输入输出）时进行了相应的调整。
   - 还增加了对 Realm VCPU 的加载和状态管理的支持，确保在进入和退出 Realm 时能够正确处理相关的寄存器和状态。
   - 讨论中强调了对用户空间的支持，包括如何通过 ioctl 进行内存的填充和状态的管理。

总的来说，本周的讨论和补丁更新进一步完善了 KVM 在 ARM64 架构下对 Arm CCA 的支持，增强了虚拟机的安全性和功能性。

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
12. **[05-13 14:17]** [PATCH v14 11/44] arm64: RMI: Check for RMI support at KVM init
   - 发件人: Steven Price <steven.price@arm.com>
13. **[05-13 14:17]** [PATCH v14 12/44] arm64: RMI: Check for LPA2 support
   - 发件人: Steven Price <steven.price@arm.com>
14. **[05-13 14:17]** [PATCH v14 13/44] arm64: RMI: Define the user ABI
   - 发件人: Steven Price <steven.price@arm.com>
15. **[05-13 14:17]** [PATCH v14 14/44] arm64: RMI: Basic infrastructure for creating a realm.
   - 发件人: Steven Price <steven.price@arm.com>
16. **[05-13 14:17]** [PATCH v14 15/44] kvm: arm64: Don't expose unsupported capabilities for realm guests
   - 发件人: Steven Price <steven.price@arm.com>
17. **[05-13 14:17]** [PATCH v14 16/44] KVM: arm64: Allow passing machine type in KVM creation
   - 发件人: Steven Price <steven.price@arm.com>
18. **[05-13 14:17]** [PATCH v14 17/44] arm64: RMI: RTT tear down
   - 发件人: Steven Price <steven.price@arm.com>
19. **[05-13 14:17]** [PATCH v14 18/44] arm64: RMI: Activate realm on first VCPU run
   - 发件人: Steven Price <steven.price@arm.com>
20. **[05-13 14:17]** [PATCH v14 19/44] arm64: RMI: Allocate/free RECs to match vCPUs
   - 发件人: Steven Price <steven.price@arm.com>
21. **[05-13 14:17]** [PATCH v14 20/44] arm64: RMI: Support for the VGIC in realms
   - 发件人: Steven Price <steven.price@arm.com>
22. **[05-13 14:17]** [PATCH v14 21/44] KVM: arm64: Support timers in realm RECs
   - 发件人: Steven Price <steven.price@arm.com>
23. **[05-13 14:17]** [PATCH v14 22/44] arm64: RMI: Handle realm enter/exit
   - 发件人: Steven Price <steven.price@arm.com>
24. **[05-13 14:17]** [PATCH v14 23/44] arm64: RMI: Handle RMI_EXIT_RIPAS_CHANGE
   - 发件人: Steven Price <steven.price@arm.com>
25. **[05-13 14:17]** [PATCH v14 24/44] KVM: arm64: Handle realm MMIO emulation
   - 发件人: Steven Price <steven.price@arm.com>
26. **[05-13 14:17]** [PATCH v14 25/44] KVM: arm64: Expose support for private memory
   - 发件人: Steven Price <steven.price@arm.com>
27. **[05-13 14:17]** [PATCH v14 26/44] arm64: RMI: Allow populating initial contents
   - 发件人: Steven Price <steven.price@arm.com>
28. **[05-13 14:17]** [PATCH v14 27/44] arm64: RMI: Set RIPAS of initial memslots
   - 发件人: Steven Price <steven.price@arm.com>
29. **[05-13 14:17]** [PATCH v14 28/44] arm64: RMI: Create the realm descriptor
   - 发件人: Steven Price <steven.price@arm.com>
30. **[05-13 14:17]** [PATCH v14 29/44] arm64: RMI: Runtime faulting of memory
   - 发件人: Steven Price <steven.price@arm.com>
31. **[05-13 14:17]** [PATCH v14 30/44] KVM: arm64: Handle realm VCPU load
   - 发件人: Steven Price <steven.price@arm.com>
32. **[05-13 14:17]** [PATCH v14 31/44] KVM: arm64: Validate register access for a Realm VM
   - 发件人: Steven Price <steven.price@arm.com>
33. **[05-13 14:17]** [PATCH v14 32/44] KVM: arm64: Handle Realm PSCI requests
   - 发件人: Steven Price <steven.price@arm.com>
34. **[05-13 14:17]** [PATCH v14 33/44] KVM: arm64: WARN on injected undef exceptions
   - 发件人: Steven Price <steven.price@arm.com>
35. **[05-13 14:17]** [PATCH v14 34/44] arm64: RMI: allow userspace to inject aborts
   - 发件人: Steven Price <steven.price@arm.com>
36. **[05-13 14:17]** [PATCH v14 35/44] arm64: RMI: support RSI_HOST_CALL
   - 发件人: Steven Price <steven.price@arm.com>
37. **[05-13 14:17]** [PATCH v14 36/44] arm64: RMI: Allow checking SVE on VM instance
   - 发件人: Steven Price <steven.price@arm.com>
38. **[05-13 14:17]** [PATCH v14 37/44] arm64: RMI: Prevent Device mappings for Realms
   - 发件人: Steven Price <steven.price@arm.com>
39. **[05-13 14:17]** [PATCH v14 38/44] arm64: RMI: Propagate number of breakpoints and watchpoints to userspace
   - 发件人: Steven Price <steven.price@arm.com>
40. **[05-13 14:17]** [PATCH v14 39/44] arm64: RMI: Set breakpoint parameters through SET_ONE_REG
   - 发件人: Steven Price <steven.price@arm.com>
41. **[05-13 14:17]** [PATCH v14 40/44] arm64: RMI: Propagate max SVE vector length from RMM
   - 发件人: Steven Price <steven.price@arm.com>
42. **[05-13 14:17]** [PATCH v14 41/44] arm64: RMI: Configure max SVE vector length for a Realm
   - 发件人: Steven Price <steven.price@arm.com>
43. **[05-13 14:17]** [PATCH v14 42/44] arm64: RMI: Provide register list for unfinalized RMI RECs
   - 发件人: Steven Price <steven.price@arm.com>
44. **[05-13 14:17]** [PATCH v14 43/44] arm64: RMI: Provide accurate register list
   - 发件人: Steven Price <steven.price@arm.com>
45. **[05-13 14:17]** [PATCH v14 44/44] arm64: RMI: Enable realms to be created
   - 发件人: Steven Price <steven.price@arm.com>
46. **[05-14 13:31]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
47. **[05-14 10:33]** Re: [PATCH v14 10/44] arm64: RMI: Add support for SRO
   - 发件人: Steven Price <steven.price@arm.com>

---

### Thread 2: [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 36 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  1 May 2026 11:19:02 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM 的 arm64 SMMUv3 驱动的补丁系列，主要关注如何实现 pKVM 的支持，包括“捕获和模拟”功能。

1. **原始补丁/问题内容**：最初的补丁（PATCH v6 00/25）旨在为 pKVM 提供完整的 SMMUv3 支持，包含多个版本的迭代，逐步实现了不同的功能，如全功能的 PV 接口、DMA 隔离和捕获模拟等。

2. **之前讨论要点**：历史讨论中，参与者主要集中在如何优化代码共享和维护性上。Jason Gunthorpe 提出了一些关于代码结构和共享逻辑的建议，认为应避免过度复杂化，同时保持与主驱动的兼容性。Mostafa Saleh 则强调了在设计中应考虑硬件契约和架构规范。

3. **本周的新讨论、进展或结论**：在本周的讨论中，Mostafa 和 Jason 继续探讨了如何处理页表共享、TLB 失效和 ATS（地址转换服务）的问题。Mostafa 提到当前补丁系列不处理 ATS，可能需要在未来的版本中进行改进。同时，Jason 强调了在不影响主驱动代码的情况下，尽量重用代码的重要性，认为通过简单的宏定义可以实现更好的代码复用，而不必进行复杂的结构拆分。

整体来看，讨论围绕如何在保持代码清晰和可维护性的前提下，优化 pKVM 的 SMMUv3 驱动实现，涉及到多个技术细节和设计选择。

#### 📝 邮件列表

1. **[05-01 11:19]** [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-01 11:19]** [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation into
 common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-01 11:19]** [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-01 11:19]** [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-01 11:19]** [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-01 09:24]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
7. **[05-01 09:41]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
8. **[05-01 09:47]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
9. **[05-01 10:00]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
10. **[05-04 12:15]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
11. **[05-04 12:16]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
12. **[05-04 12:19]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
13. **[05-04 12:28]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
14. **[05-05 13:17]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
15. **[05-05 13:27]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
16. **[05-05 16:43]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[05-05 16:48]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
18. **[05-06 06:53]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
19. **[05-06 06:56]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
20. **[05-07 09:40]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
21. **[05-07 10:13]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
22. **[05-09 20:21]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
23. **[05-09 20:27]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
24. **[05-09 20:29]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
25. **[05-09 20:34]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
26. **[05-11 11:16]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
27. **[05-11 11:24]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
28. **[05-11 11:45]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
29. **[05-11 12:53]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
30. **[05-11 11:18]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
31. **[05-11 11:22]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
32. **[05-11 11:24]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
33. **[05-11 11:30]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
34. **[05-12 10:42]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
35. **[05-12 09:36]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
36. **[05-13 21:54]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>

---

### Thread 3: [PATCH v7 00/20] ARM64 PMU Partitioning

**📧 邮件数**: 26 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  4 May 2026 21:17:53 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 ARM64 PMU（性能监控单元）分区的补丁系列，主要由 Colton Lewis 提出。该补丁旨在创建一个新的 PMU 方案，通过将计数器分区来允许更直接的访客访问，从而显著降低开销。补丁系列包括多个部分，涉及如何设置 PMU 的分区、处理寄存器的访问以及动态分配访客计数器等。

在历史讨论中，Colton Lewis 提出了多个补丁，详细描述了如何实现 PMU 的分区，包括对 PMUv3 的支持、设置 FGT（细粒度陷阱）以优化性能，以及如何处理被访客访问的寄存器。讨论中还提到了一些实现细节和性能基准。

在本周的新讨论中，参与者 James Clark 和 Oliver Upton 提出了对补丁的具体反馈和建议。例如，James 提到在使用 `arm_pmuv3.reserved_host_counters` 时遇到的问题，认为需要调整计数器的分配方式。Oliver 则对代码的可读性和结构提出了改进建议，强调了在处理分区 PMU 时应避免复杂的条件编译。Colton Lewis 对这些反馈表示感谢，并承诺将进行相应的修正。

总体而言，本周的讨论集中在补丁的细节和代码优化上，参与者们积极交流，推动补丁的完善。

#### 📝 邮件列表

1. **[05-04 21:17]** [PATCH v7 00/20] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[05-04 21:17]** [PATCH v7 06/20] perf: arm_pmuv3: Add method to partition the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[05-04 21:18]** [PATCH v7 07/20] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[05-04 21:18]** [PATCH v7 08/20] KVM: arm64: Add Partitioned PMU register trap handlers
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[05-04 21:18]** [PATCH v7 09/20] KVM: arm64: Set up MDCR_EL2 to handle a Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[05-04 21:18]** [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[05-04 21:18]** [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter reservations
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[05-11 15:47]** Re: [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter
 reservations
   - 发件人: James Clark <james.clark@linaro.org>
9. **[05-11 15:49]** Re: [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest
 registers
   - 发件人: James Clark <james.clark@linaro.org>
10. **[05-11 15:51]** Re: [PATCH v7 06/20] perf: arm_pmuv3: Add method to partition the PMU
   - 发件人: James Clark <james.clark@linaro.org>
11. **[05-11 15:57]** Re: [PATCH v7 00/20] ARM64 PMU Partitioning
   - 发件人: James Clark <james.clark@linaro.org>
12. **[05-13 00:34]** Re: [PATCH v7 07/20] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: Oliver Upton <oupton@kernel.org>
13. **[05-13 00:45]** Re: [PATCH v7 08/20] KVM: arm64: Add Partitioned PMU register trap
 handlers
   - 发件人: Oliver Upton <oupton@kernel.org>
14. **[05-13 00:57]** Re: [PATCH v7 09/20] KVM: arm64: Set up MDCR_EL2 to handle a
 Partitioned PMU
   - 发件人: Oliver Upton <oupton@kernel.org>
15. **[05-13 02:18]** Re: [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest
 registers
   - 发件人: Oliver Upton <oupton@kernel.org>
16. **[05-13 16:10]** Re: [PATCH v7 00/20] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
17. **[05-13 16:13]** Re: [PATCH v7 06/20] perf: arm_pmuv3: Add method to partition the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
18. **[05-13 16:38]** Re: [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>
19. **[05-13 16:45]** Re: [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter reservations
   - 发件人: Colton Lewis <coltonlewis@google.com>
20. **[05-14 10:10]** Re: [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter
 reservations
   - 发件人: James Clark <james.clark@linaro.org>
21. **[05-14 17:49]** Re: [PATCH v7 07/20] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
22. **[05-14 18:18]** Re: [PATCH v7 08/20] KVM: arm64: Add Partitioned PMU register trap handlers
   - 发件人: Colton Lewis <coltonlewis@google.com>
23. **[05-14 18:43]** Re: [PATCH v7 09/20] KVM: arm64: Set up MDCR_EL2 to handle a
 Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
24. **[05-14 18:59]** Re: [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>
25. **[05-14 19:05]** Re: [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter reservations
   - 发件人: Colton Lewis <coltonlewis@google.com>
26. **[05-15 09:28]** Re: [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter
 reservations
   - 发件人: James Clark <james.clark@linaro.org>

---

### Thread 4: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 21 | **👥 参与者**: 4 | **📅 开始时间**: Sun,  3 May 2026 09:33:20 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于引入可定制的 AArch64 KVM 主机模型的补丁系列（[PATCH v4 00/17]）。该补丁旨在增强当前的 KVM 主机模型，允许用户空间覆盖部分 ID 寄存器的值，以便在不同硬件之间迁移虚拟机时提供更大的灵活性。

在历史讨论中，Eric Auger 提出了多个补丁，涉及 ID 寄存器的排序、自动生成、以及处理生成的 ID 寄存器定义的基础设施等。参与者 Shameer Kolothum Thodi 对补丁提出了一些问题和建议，主要集中在寄存器的可写性和功能性上。

在本周的新讨论中，Eric Auger 针对 Shameer 的反馈进行了回应，确认了一些补丁的修改和删除，并讨论了 ID 寄存器的自动生成问题。Peter Maydell 和 Marc Zyngier 也参与了讨论，提出了关于用户请求设置无效 ID 寄存器组合时的处理方式，指出当前的实现并未在 QEMU 层面进行一致性检查，主要依赖 KVM 的检查。

总体而言，本周的讨论进一步明确了补丁的细节和潜在问题，推动了补丁系列的进展。

#### 📝 邮件列表

1. **[05-03 09:33]** [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Eric Auger <eric.auger@redhat.com>
2. **[05-03 09:33]** [PATCH v4 02/17] target/arm/cpu-sysregs.h.inc: Sort by name alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
3. **[05-03 09:33]** [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
4. **[05-03 09:33]** [PATCH v4 04/17] arm/cpu: Add infra to handle generated ID register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
5. **[05-03 09:33]** [PATCH v4 08/17] target/arm/kvm: Introduce kvm_get_writable_id_regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
6. **[05-03 09:33]** [PATCH v4 09/17] arm/cpu: accessors for writable id registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
7. **[05-06 16:10]** RE: [PATCH v4 02/17] target/arm/cpu-sysregs.h.inc: Sort by name
 alphabetical order
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
8. **[05-07 08:45]** RE: [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
9. **[05-07 08:58]** RE: [PATCH v4 04/17] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
10. **[05-07 10:07]** RE: [PATCH v4 08/17] target/arm/kvm: Introduce
 kvm_get_writable_id_regs
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
11. **[05-07 10:32]** RE: [PATCH v4 09/17] arm/cpu: accessors for writable id registers
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
12. **[05-12 08:24]** Re: [PATCH v4 02/17] target/arm/cpu-sysregs.h.inc: Sort by name
 alphabetical order
   - 发件人: Eric Auger <eric.auger@redhat.com>
13. **[05-12 08:38]** Re: [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
14. **[05-12 09:41]** RE: [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
15. **[05-12 16:11]** Re: [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[05-12 16:52]** Re: [PATCH v4 04/17] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[05-12 17:12]** Re: [PATCH v4 08/17] target/arm/kvm: Introduce
 kvm_get_writable_id_regs
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[05-12 17:33]** Re: [PATCH v4 09/17] arm/cpu: accessors for writable id registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[05-15 09:31]** Re: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Peter Maydell <peter.maydell@linaro.org>
20. **[05-15 10:04]** Re: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[05-15 18:41]** Re: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM
 host model
   - 发件人: Eric Auger <eric.auger@redhat.com>

---

### Thread 5: [PATCH] ima: debugging late_initcall_sync measurements

**📧 邮件数**: 12 | **👥 参与者**: 2 | **📅 开始时间**: Wed, 6 May 2026 14:57:12 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 Linux 内核 IMA（Integrity Measurement Architecture）模块的补丁，旨在调试 `late_initcall_sync` 测量的相关问题。

**原始补丁内容**：
补丁的主要目的是解决在 IMA 初始化之前发生的测量事件，特别是在 `boot_aggregate` 和 `boot_aggregate_late` 之间的测量差异。

**之前讨论要点**：
历史讨论中，参与者 Yeoreum Yun 和 Mimi Zohar 进行了深入的技术交流，探讨了 IMA 初始化时机对测量的影响。Yeoreum 提出了一些关于测量在初始化之前的疑问，并发现内核自测可能导致了这些测量。Mimi 也指出，早期测量在 TPM（可信任的平台模块）初始化之前是一个需要解决的问题。

**本周新讨论进展**：
在本周的讨论中，Yeoreum 询问了关于解决早期测量和延迟 TPM 初始化的问题。Mimi 表示，支持“缺失的早期 IMA 测量”可能被视为新特性，并指出排队早期测量可能会破坏“使用前测量”的原则。她提出了一种替代方案，即基于内置 IMA 策略拒绝对任何将被测量的内容的访问，但尚不清楚这是否会影响现有系统的启动。

总体而言，讨论围绕如何在不影响系统安全性的前提下，合理处理 IMA 初始化与测量事件之间的关系展开。

#### 📝 邮件列表

1. **[05-06 14:57]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[05-06 22:32]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
3. **[05-07 06:50]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[05-07 07:28]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
5. **[05-07 13:41]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
6. **[05-07 21:03]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[05-07 17:36]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
8. **[05-08 10:06]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
9. **[05-08 08:55]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
10. **[05-08 14:41]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
11. **[05-14 13:42]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
12. **[05-14 10:53]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>

---

### Thread 6: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations

**📧 邮件数**: 12 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 11 May 2026 09:57:27 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）文档的补丁，主要目的是明确 KVM 在主机内核升级和回滚时对客户机可见的兼容性期望。

**原始补丁内容**：
David Woodhouse 提出的补丁文档化了 KVM 需要维护的客户机可见兼容性，包括：
1. 通过 KVM ioctl 保存和恢复的状态必须足以支持不同内核版本之间的实时迁移。
2. 新内核引入的客户机可见变化应提供机制让用户空间选择之前的行为，以支持向前和向后的迁移。

**之前讨论要点**：
在历史讨论中，参与者一致认为在 x86 架构上这些兼容性要求隐含存在，但并未明确记录。讨论中提到，x86 在 CPUID 处理上表现良好，而 ARM 架构在供应商行为一致性方面存在更多挑战。

**本周新讨论进展**：
本周的讨论集中在补丁的必要性和实现细节上。Paolo Bonzini 和其他参与者讨论了 x86 和 ARM 在兼容性处理上的差异，强调了 KVM 在 ARM 上需要改进的地方。Marc Zyngier 提到，KVM 不能简单地恢复旧行为，而是需要在架构允许的范围内进行调整。David Woodhouse 则坚持认为，KVM 应该提供机制使用户空间能够选择旧的行为，以确保兼容性。整体上，讨论显示出对补丁的支持，但也暴露了 ARM 平台在兼容性方面的不足。

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
5. **[05-11 18:53]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
6. **[05-13 09:42]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-13 10:24]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
8. **[05-13 14:43]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
9. **[05-13 15:03]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility
 expectations
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[05-13 14:57]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>
11. **[05-13 18:24]** Re: [PATCH] Documentation: KVM: Document guest-visible compatibility expectations
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>
12. **[05-13 19:26]** Re: [PATCH] Documentation: KVM: Document guest-visible
 compatibility expectations
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 7: [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support

**📧 邮件数**: 10 | **👥 参与者**: 1 | **📅 开始时间**: Sat, 16 May 2026 19:29:54 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构上实现基本嵌套虚拟机支持的补丁（PATCH v3 0/9）。该补丁的主要目标是为 KVM 的自测试框架添加对嵌套客户机（L2）的基本支持，包括启用阶段 2 的框架、相关数据结构和页面表生成器。

在历史讨论中，补丁的前版本（v2）提出了一些基础功能，但未能完全实现阶段 2 的支持。本周的讨论中，Wei-Lin Chang 提出了多个补丁，重点包括：
1. **补丁内容**：补丁包括对 GPR（通用寄存器）的保存和恢复功能、嵌套客户机的测试、以及增强的 hello_nested 测试。
2. **之前讨论要点**：之前的讨论集中在如何实现嵌套虚拟化的基本功能，特别是如何管理 L2 的虚拟 CPU 和内存。
3. **本周新进展**：新增了 shadow_stage2 测试，测试了影子页面表管理代码，并实现了对嵌套客户机的阶段 2 转换支持。此外，还创建了用于分配 L2 堆栈的专用内存池，以及检查支持的阶段 2 粒度大小的功能。

整体来看，本周的讨论和补丁推进了 KVM 在 ARM64 上的嵌套虚拟化能力，为后续的功能扩展奠定了基础。

#### 📝 邮件列表

1. **[05-16 19:29]** [PATCH v3 0/9] KVM: arm64: selftests: Basic nested guest support
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-16 19:29]** [PATCH v3 1/9] KVM: arm64: selftests: Add GPR save/restore functions for NV
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[05-16 19:29]** [PATCH v3 2/9] KVM: arm64: selftests: Add helpers for guest hypervisors
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[05-16 19:29]** [PATCH v3 3/9] KVM: arm64: selftests: Add hello_nested basic NV selftest
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[05-16 19:29]** [PATCH v3 4/9] KVM: arm64: selftests: Enhance hello_nested test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[05-16 19:29]** [PATCH v3 5/9] KVM: arm64: selftests: Add shadow_stage2 test
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
7. **[05-16 19:30]** [PATCH v3 6/9] KVM: arm64: selftests: shadow_stage2: Allocate L2 stack from dedicated pool
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
8. **[05-16 19:30]** [PATCH v3 7/9] KVM: arm64: selftests: shadow_stage2: Check supported stage-2 granule size
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
9. **[05-16 19:30]** [PATCH v3 8/9] KVM: arm64: selftests: Add infrastructure for using stage-2 in guest
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
10. **[05-16 19:30]** [PATCH v3 9/9] KVM: arm64: selftests: shadow_stage2: Turn on stage-2 translation for the nested guest
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 8: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 8 May 2026 18:12:01 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于更新 ARM64 架构中的 SMIDR_EL1 寄存器，以符合 DDI0601 规范的补丁（PATCH v10 01/30）。补丁的主要内容是更新系统寄存器以支持新的架构特性。

在历史讨论中，参与者 Mark Rutland 和 Mark Brown 讨论了补丁的必要性及其对虚拟机（VM）和主机的影响。他们关注到更新后的字段是否会影响后续的补丁，以及是否会向虚拟机暴露优先级支持等问题。Rutland 指出当前并未向虚拟机暴露优先级支持，因此暂时不需要担心相关问题。

在本周的新讨论中，参与者们进一步探讨了补丁的合理性和动机。Mark Brown 询问更新这些定义的具体原因，是否计划在主机或虚拟机中以特定方式使用这些字段。Rutland 表示，更新的直接动机是为了确保与当前系列的兼容性，并提到需要评估硬件实现的优先级支持，以便决定是否以及如何向主机或虚拟机暴露这些特性。

总体而言，本周的讨论集中在补丁的合理性、潜在影响及未来的计划上，参与者们一致认为需要更深入的理解和评估。

#### 📝 邮件列表

1. **[05-08 18:12]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-08 18:20]** Re: [PATCH v10 15/30] KVM: arm64: Support SME control registers
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[05-09 09:43]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[05-11 11:32]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-11 11:40]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Rutland <mark.rutland@arm.com>
6. **[05-11 21:31]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Brown <broonie@kernel.org>
7. **[05-11 21:42]** Re: [PATCH v10 04/30] arm64/fpsimd: Determine maximum virtualisable
 SME vector length
   - 发件人: Mark Brown <broonie@kernel.org>
8. **[05-11 23:17]** Re: [PATCH v10 15/30] KVM: arm64: Support SME control registers
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 9: [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations

**📧 邮件数**: 7 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 12 May 2026 12:44:40 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 ARM FF-A（Firmware Framework for Arm）中的端点内存访问描述符（EMAD）偏移计算的问题。Sebastian Ene 提出了两个补丁（patch），旨在更新核心 FF-A 驱动和 pKVM 虚拟化管理程序的偏移计算逻辑，以符合 FF-A 规范。

在历史讨论中，之前的版本未能正确处理 FF-A 规范中 EMAD 的偏移，导致假设 EMAD 紧随内存区域头部。此问题在 FF-A 1.1 版本后变得明显，因为新规范引入了 `ep_mem_offset` 字段来指示内存访问数组的起始位置。

本周的新讨论中，Sebastian 提出了两个补丁：
1. 第一个补丁修复了 `arm_ffa` 驱动中的 EMAD 偏移计算，确保使用 `ep_mem_offset` 而不是默认的结构大小，并添加了边界检查。
2. 第二个补丁增强了 pKVM 的验证逻辑，确保 EMAD 的偏移在邮箱缓冲区的边界内。

参与者 Mostafa Saleh 和 Sudeep Holla 对补丁进行了审查，提出了一些小的改进建议，并表示支持这些更改。整体来看，讨论集中在确保补丁的正确性和兼容性上，未发现明显的冲突。

#### 📝 邮件列表

1. **[05-12 12:44]** [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[05-12 12:44]** [PATCH v3 1/2] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sebastian Ene <sebastianene@google.com>
3. **[05-12 12:44]** [PATCH v3 2/2] KVM: arm64: Validate the offset to the mem access descriptor
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[05-13 13:34]** Re: [PATCH v3 1/2] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-13 13:53]** Re: [PATCH v3 2/2] KVM: arm64: Validate the offset to the mem access
 descriptor
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-13 18:19]** Re: [PATCH v3 1/2] firmware: arm_ffa: Fix Endpoint Memory Access
 Descriptor offset calculation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
7. **[05-13 18:23]** Re: [PATCH v3 0/2] arm_ffa, KVM: Fix FF-A emad offset calculations
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 10: [PATCH 0/2] KVM: arm64: nv: Reduce FP/SVE overhead on exception/exception return

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 12 May 2026 15:07:53 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构下优化 FP/SVE（浮点/SVE 寄存器）在异常处理和返回过程中的开销。Marc Zyngier 提出了两个补丁，旨在减少在 EL1 和 EL2 之间切换时的性能损失。

第一个补丁添加了一个新的 vcpu 状态标志，用于跟踪从 L2 到 L1 的嵌套异常。这使得在处理嵌套异常时能够更有效地管理状态。第二个补丁则提出在嵌套的 ERET 或异常处理过程中，避免保存和恢复 FP/SVE 寄存器，从而消除不必要的开销。Marc 指出，这种优化在运行 I/O 密集型工作负载时可提升 10%-20% 的性能。

在本周的新讨论中，Mark Rutland 对第二个补丁的描述提出了一些建议，认为可以简化语言并增加注释以解释为何这种做法是安全的。Marc 对此表示赞同，并计划在下周重新发布补丁以反映这些修改。

总体而言，本周的讨论集中在补丁的细节和改进建议上，显示出对优化 KVM 性能的持续关注。

#### 📝 邮件列表

1. **[05-12 15:07]** [PATCH 0/2] KVM: arm64: nv: Reduce FP/SVE overhead on exception/exception return
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-12 15:07]** [PATCH 1/2] KVM: arm64: nv: Track L2 to L1 exception emulation
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-12 15:07]** [PATCH 2/2] KVM: arm64: nv: Don't save/restore FP register during a nested ERET or exception
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-13 13:28]** Re: [PATCH 2/2] KVM: arm64: nv: Don't save/restore FP register
 during a nested ERET or exception
   - 发件人: Mark Rutland <mark.rutland@arm.com>
5. **[05-13 13:49]** Re: [PATCH 2/2] KVM: arm64: nv: Don't save/restore FP register during a nested ERET or exception
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 11: [PATCH v3 0/4] KVM: arm64: vgic: Fix IGROUPR writability and IIDR revision control

**📧 邮件数**: 5 | **👥 参与者**: 1 | **📅 开始时间**: Mon, 11 May 2026 12:30:42 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VGIC（虚拟通用中断控制器）修复，主要集中在 IGROUPR 可写性和 IIDR（中断接口描述符寄存器）版本控制的问题。

**原始 patch/问题的内容**：
此次补丁系列旨在修复 GICv2/v3 的 IGROUPR 可写性模型，使其能够根据 GICD_IIDR 的实现版本进行一致控制，替代之前的 v2_groups_user_writable 标志。之前的实现使得 IGROUPR 在 GICv2 和 GICv3 上都是可写的，但未提供用户空间恢复旧行为的机制。

**之前讨论要点**：
在之前的讨论中，提到在某些情况下，用户空间无法恢复 IGROUPR 的状态，导致不一致性。特别是 QEMU 在处理 GICD_IIDR 时未能正确保存和恢复 IGROUPR 的状态。

**本周的新讨论、进展或结论**：
本周的讨论中，David Woodhouse 提出了四个补丁：
1. 允许用户空间设置 IIDR 版本为 1，以恢复 GICv2 和 GICv3 的原始只读 IGROUPR 行为。
2. 移除 v2_groups_user_writable 标志，使得 IGROUPR 的可写性直接跟随 IIDR 版本。
3. 添加自测试，验证 IIDR 版本语义及 QEMU 风格的保存/恢复场景。
4. 进一步测试 GICv2 IGROUPR 的可写性，确保其行为与 IIDR 版本一致。

这些补丁已在 EC2 c7g.metal 和 QEMU-TCG 上进行了测试，确保在不同版本的内核之间保持精确的客户机兼容性。

#### 📝 邮件列表

1. **[05-11 12:30]** [PATCH v3 0/4] KVM: arm64: vgic: Fix IGROUPR writability and IIDR revision control
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[05-11 12:30]** [PATCH v3 1/4] KVM: arm64: vgic: Allow userspace to set IIDR revision 1
   - 发件人: David Woodhouse <dwmw2@infradead.org>
3. **[05-11 12:30]** [PATCH v3 2/4] KVM: arm64: selftests: Add vgic IIDR revision test
   - 发件人: David Woodhouse <dwmw2@infradead.org>
4. **[05-11 12:30]** [PATCH v3 3/4] KVM: arm64: vgic: Remove v2_groups_user_writable and use IIDR revision directly
   - 发件人: David Woodhouse <dwmw2@infradead.org>
5. **[05-11 12:30]** [PATCH v3 4/4] KVM: arm64: selftests: Add GICv2 IGROUPR writability test
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 12: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe

**📧 邮件数**: 4 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 08 May 2026 18:54:14 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于将 Arm FF-A 核心初始化移至平台驱动探测的补丁系列（[PATCH 0/4]）。历史讨论中，Sudeep Holla 提出了这一补丁系列，目的是将 Arm FF-A 的核心引导路径转换为平台驱动的探测/移除流程。第一个补丁回退了之前对 `rootfs_initcall` 的更改，指出这种初始化顺序的解决方案并不恰当，可能与 pKVM FF-A 代理的需求冲突。

在本周的新讨论中，Sudeep Holla 更新了补丁的状态，确认已将补丁应用到他的代码库中，并感谢参与者的贡献。补丁包括四个部分：回退 `ffa_init()` 的初始化调用级别、将核心注册为平台驱动、将核心设备设置为 FF-A 设备的父级，以及在 pKVM 初始化之前延迟探测。此外，Sudeep Holla 在最后一封邮件中指出，之前的一些邮件内容是错误的，并请求忽略。

总体来看，本周的进展主要集中在补丁的应用和确认上，同时也纠正了之前的错误信息。

#### 📝 邮件列表

1. **[05-08 18:54]** [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
2. **[05-17 12:36]** Re: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
3. **[05-17 12:44]** Re: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
4. **[05-17 12:54]** Re: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 13: [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 14 May 2026 17:26:24 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于修复 KVM 在 arm64 架构下 nVHE/pKVM 模式下的 hyp 跟踪错误。原始的 patch 由 Vincent Donnefort 提出，主要内容是确保 pKVM 验证主机提供的跟踪缓冲区描述符。如果发现错误，之前的实现仅返回 0，而修复后将在验证失败时返回 -EINVAL。此外，函数名称也进行了更改，从 hyp_trace_desc_validate() 改为 hyp_trace_desc_is_valid()，并在 nVHE 模式下跳过验证，因为在该模式下可以信任主机提供的数据。

在之前的讨论中，Marc Zyngier 提出了对 patch 的建议，询问是否需要添加 "Fixes:" 标签以及是否应考虑将其作为稳定版本的补丁。Vincent Donnefort 随后确认了需要添加 "Fixes:" 标签，并指出该问题源于特定的提交，但由于该功能仅在 7.1 版本中引入，因此不需要对稳定版本进行修复。

本周的讨论主要集中在 patch 的细节和修复的必要性上，参与者对 patch 的内容表示认可，并讨论了其对稳定版本的影响。整体来看，讨论进展顺利，参与者对修复方案达成了一致。

#### 📝 邮件列表

1. **[05-14 17:26]** [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
2. **[05-15 11:21]** Re: [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid desc
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-15 13:58]** Re: [PATCH] KVM: arm64: Fix nVHE/pKVM hyp tracing error on invalid
 desc
   - 发件人: Vincent Donnefort <vdonnefort@google.com>

---

### Thread 14: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 10 May 2026 22:28:50 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic（虚拟通用中断控制器）修复补丁，主要针对 IIDR（中断识别寄存器）修订字段提取错误的问题。

在历史讨论中，David Woodhouse 提出了一个问题，询问为何其他相关修复没有包含在 7.1 版本中。这表明在之前的讨论中，存在对多个修复的关注，但并未详细展开。

在本周的新讨论中，Marc Zyngier 和 David Woodhouse 进行了深入的辩论。Marc 表示，KVM/arm64 需要支持在不改变来宾环境的情况下升级内核，并且在必要时能够回滚升级。他强调，来宾可见的变化应是可选的，IIDR 的修复正是为了确保能够设置为先前版本。David 则反驳称这些更改并非必要，且可能会重新引入已解决的错误。他仅选择了针对影响用户空间的 bug 的修复，认为其他更改不值得。

综上所述，本周的讨论集中在对补丁必要性及其潜在影响的分歧上，双方对 KVM 的兼容性和稳定性有不同的看法。

#### 📝 邮件列表

1. **[05-10 22:28]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[05-11 08:56]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field extracted from wrong value
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-11 09:13]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 15: [PATCH] Enable stage 2 translation in L2

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 15 May 2026 10:48:05 +0900

#### 🤖 AI 总结

本邮件讨论的主题是关于在 L2 启用第二阶段地址转换的补丁（PATCH）。该补丁由 Itaru Kitayama 提交，主要内容是使得第二阶段转换在 L2 中可用，同时保持第一阶段关闭，以符合 Wei Lin 的偏好。补丁中涉及的代码修改包括更新了多个文件，添加了新的结构体和函数，以支持可配置的 IPA 大小和起始级别。

在之前的讨论中，尚未有相关补丁被接受，因此 Itaru 的补丁在某种程度上依赖于未被接受的代码。此外，Wei Lin 指出补丁的提交信息过于简略，未能充分说明变更的复杂性，并指出了代码中的一些格式问题，如使用空格而非制表符进行缩进。

本周的新讨论中，Wei Lin 对补丁提出了一些具体问题和建议，包括对 4K 页大小的保证、oa_bits 的使用以及代码格式问题。同时，他提到自己已发布了一个不同的版本（v3），在该版本中，所有的第二阶段设置都是由客体虚拟机自身完成的，并邀请 Itaru 对其进行反馈。

#### 📝 邮件列表

1. **[05-15 10:48]** [PATCH] Enable stage 2 translation in L2
   - 发件人: Itaru Kitayama <itaru.kitayama@fujitsu.com>
2. **[05-16 20:03]** Re: [PATCH] Enable stage 2 translation in L2
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 16: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from direct map

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 8 May 2026 08:18:10 +0000

#### 🤖 AI 总结

在本次邮件讨论中，主题为“[PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from direct map”的补丁旨在为 KVM 的 guest_memfd 添加一个标志，以便从直接映射中移除相应的内存页。

**历史讨论**中，参与者们一致同意采用文件映射级别的方法，计划将 zap/restore 钩子从 guest_memfd 移动到 filemap_add_folio() 和 filemap_remove_folio() 中，并加强 AS_NO_DIRECT_MAP 的语义，以确保在页面缓存中存在的 folio 期间，直接映射始终无效。此外，决定放弃在 folio->p 中的 KVM_GMEM_FOLIO_NO_DIRECT_MAP 书籍管理。

**本周新讨论**中，Ackerley Tng 提出了对补丁的进一步讨论，特别是关于 TDX 和 SNP 的支持。他表示对补丁中某些表述感到不安，认为可能未充分考虑 TDX 和 SNP 的情况。他讨论了在非就地填充的情况下，源物理页与目标物理页不同的情况，并询问 mermap 是否可以替代 kmap_local_page，以及 guest_memfd 是否需要在使用 mermap 和 memcpy 后强制进行 TLB 刷新。此外，Vlastimil 提到当前 mm-tree 的临时限制，可能会影响稳定分支的共享。Ackerley 建议继续推进新版本的补丁，以充分解决评论意见，或者等待转换完成后再进行更多工作。

#### 📝 邮件列表

1. **[05-08 08:18]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from direct map
   - 发件人: Takahiro Itazuri <itazur@amazon.com>
2. **[05-14 09:45]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Ackerley Tng <ackerleytng@google.com>

---

### Thread 17: [PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to
 fault-in on !mmap()'d memory

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 12 May 2026 15:28:15 +0800

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM 的自测试补丁（patch）——“添加 guest_memfd 测试用例以在未 mmap 的内存上进行故障注入”。该补丁旨在增强 KVM 的内存管理能力，特别是在处理未映射内存时的测试。

在历史讨论中，参与者 Sean Christopherson 提到在执行测试时出现了错误，具体表现为在调用 `vm_set_user_memory_region2` 函数时返回了无效参数的错误（errno=22）。这表明在设置用户内存区域时存在问题，导致测试失败。

在本周的新讨论中，Zenghui Yu 和 Sean Christopherson 继续探讨这个问题。Zenghui Yu 提供了具体的错误信息，并指出了测试失败的原因。Sean Christopherson 随后确认，内存槽的大小需要是主机页面大小的倍数，并表示将会提交新的补丁以解决这个问题。

总结来说，本周的讨论集中在修复 KVM 测试中的内存设置错误，参与者们正在积极寻求解决方案，以确保补丁的有效性和测试的成功。

#### 📝 邮件列表

1. **[05-12 15:28]** Re: [PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to
 fault-in on !mmap()'d memory
   - 发件人: Zenghui Yu <yuzenghui@huawei.com>
2. **[05-12 08:53]** Re: [PATCH v17 24/24] KVM: selftests: Add guest_memfd testcase to
 fault-in on !mmap()'d memory
   - 发件人: Sean Christopherson <seanjc@google.com>

---

### Thread 18: [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 17 May 2026 14:13:31 -0400

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的虚拟化管理，特别是 vGIC（虚拟通用中断控制器）在初始化失败时的资源释放问题。

**原始 patch/问题的内容**：
本周的 patch 提出了在 `kvm_vgic_vcpu_init()` 函数中，如果分配的每个 vCPU 的私有 IRQ 失败，应该调用 `kvm_vgic_vcpu_destroy()` 来释放这些资源。之前的实现没有处理这一情况，导致内存泄漏。

**之前讨论要点**：
在历史讨论中并未提及具体的讨论内容，但 patch 是对之前提交的补丁（commit 250f25367b58）的补充，旨在确保在 vCPU 创建失败时能够正确清理资源，避免内存泄漏。

**本周的新讨论、进展或结论**：
本周的邮件由 Michael Bommarito 提交，详细描述了 patch 的必要性和实现方式，指出在特定情况下（如 MMIO-bus 槽位耗尽），会导致私有 IRQ 分配失败而未能释放资源。通过使用 kmemleak 工具，确认在未应用此 patch 的情况下，存在未引用的内存块，而应用此 patch 后，内存泄漏问题得到解决。此 patch 旨在提升系统的稳定性和安全性，并已被标记为需要在稳定版本中应用。

#### 📝 邮件列表

1. **[05-17 14:13]** [PATCH] KVM: arm64: vgic: free private_irqs when init fails after allocation
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>

---

### Thread 19: [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 17 May 2026 13:49:55 -0400

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 vgic-its 组件的一个补丁，主要目的是拒绝恢复的设备表项（DTE）中包含超出范围的 num_eventid_bits 值。

在历史讨论中，补丁的背景是，用户空间可以通过 KVM_DEV_ARM_ITS_RESTORE_TABLES 触发主机端的拒绝服务（DoS）攻击。当设备表项的 Size 字段编码的 num_eventid_bits 大于 VITS_TYPER_IDBITS 时，会导致 scan_its_table() 函数在持有 per-ITS 互斥锁的情况下进入一个长时间的循环，从而阻塞主机 CPU。此问题的根源在于 vgic_its_restore_dte() 函数未能对 num_eventid_bits 应用相应的限制，导致用户空间可以安装不被 MAPD 路径拒绝的设备状态。

在本周的新讨论中，Michael Bommarito 提出了补丁，旨在通过在 vgic_its_restore_dte() 函数中添加检查，确保如果 num_eventid_bits 超出 VITS_TYPER_IDBITS 的范围，则立即返回 -EINVAL 错误。这一修复措施可以有效防止超出范围的 DTE 安装，从而避免触发潜在的拒绝服务攻击。补丁的实现包括在代码中添加了相应的条件判断，以确保设备表项的有效性。

总的来说，本周的讨论集中在补丁的具体实现及其对系统安全性的影响上，强调了对设备状态恢复过程中的边界检查的重要性。

#### 📝 邮件列表

1. **[05-17 13:49]** [PATCH] KVM: arm64: vgic-its: reject restored DTE with out-of-range num_eventid_bits
   - 发件人: Michael Bommarito <michael.bommarito@gmail.com>

---

### Thread 20: [PATCH] KVM: arm64: Remove @arch from __load_stage2()

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Fri, 15 May 2026 11:18:53 +0530

#### 🤖 AI 总结

本邮件主题为「[PATCH] KVM: arm64: Remove @arch from __load_stage2()」，涉及对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的一个函数进行修改。该补丁的主要内容是移除 `__load_stage2()` 函数中的 `@arch` 参数，以简化函数接口。

在历史讨论中，未提供具体的补丁或讨论内容，因此无法总结之前的讨论要点。

本周的新讨论中，参与者 Anshuman Khandual 对该补丁进行了审核，并表示支持，标记为“Reviewed-by”。这表明该补丁得到了认可，可能会在后续的版本中被合并。

总结而言，本周的讨论主要集中在对该补丁的审核上，表明该补丁在社区中获得了积极的反馈。

#### 📝 邮件列表

1. **[05-15 11:18]** Re: [PATCH] KVM: arm64: Remove @arch from __load_stage2()
   - 发件人: Anshuman Khandual <anshuman.khandual@arm.com>

---

## 📌 RFC

共 3 个 thread

---

### Thread 1: [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM

**📧 邮件数**: 28 | **👥 参与者**: 3 | **📅 开始时间**: Wed, 13 May 2026 16:33:43 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 ARM64 KVM 客户机的命名 CPU 模型的 RFC 补丁（版本 1），该补丁旨在为 ARM64 KVM 客户机引入“命名” CPU 模型。这一补丁的主要目标是实现跨主机的实时迁移，以及对暴露给客户机的各个 CPU 特性的管理控制。

**原始补丁内容**：
补丁引入了命名 CPU 模型，允许用户通过 QEMU 启动时指定特定的 CPU 模型及其特性，例如 `qemu-system-aarch64 -cpu grace-v1`。补丁还解决了 ARM64 KVM 客户机在特性定义上的复杂性，提供了一个三层设计，包括 ID 寄存器字段表、ARM 属性层和 CPU 模型层。

**历史讨论要点**：
之前的讨论集中在如何定义和实现这些命名 CPU 模型的细节，包括如何处理不同的特性和寄存器，以及如何确保这些模型在未来的内核版本中向后兼容。参与者讨论了与现有代码的兼容性以及如何利用现有的 SYSREG 属性系列。

**本周新讨论和进展**：
本周的讨论主要集中在补丁的具体实现上，包括对 ID 寄存器字段的定义、属性的生成、以及如何将这些属性注册到 CPU 模型中。参与者还讨论了如何处理特性值的验证和默认值的设置。Eric Auger 提出了对补丁设计的反馈，建议可以利用现有的 `Registers.json` 文件来简化某些字段的定义，并对补丁的实现细节提出了质疑和建议。Khushit Shah 则回应了这些问题，并表示会在后续版本中进行调整。

整体来看，本周的讨论推动了补丁的具体实现进展，并对未来的版本提出了改进建议。

#### 📝 邮件列表

1. **[05-13 16:33]** [RFC PATCH v1 00/13] named CPU models for ARM64 on KVM
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
2. **[05-13 16:33]** [RFC PATCH v1 01/13] target/arm: named_cpu_model: define containers for ID registers and fields
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
3. **[05-13 16:33]** [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register Fields
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
4. **[05-13 16:33]** [RFC PATCH v1 03/13] target/arm: named_cpu_model: initialise additional sysregs
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
5. **[05-13 16:33]** [RFC PATCH v1 04/13] target/arm: named_cpu_model: generate tables for Arm64 ID registers and fields
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
6. **[05-13 16:33]** [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD macro with IDREG_FIELD
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
7. **[05-13 16:33]** [RFC PATCH v1 06/13] target/arm: named_cpu_model: data-structures required for the ARM property layer.
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
8. **[05-13 16:33]** [RFC PATCH v1 07/13] target/arm: named_cpu_model: define ARM properties
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
9. **[05-13 16:33]** [RFC PATCH v1 08/13] target/arm: named_cpu_model: generate arm_cpu_props[] table
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
10. **[05-13 16:33]** [RFC PATCH v1 09/13] target/arm: named_cpu_model: Add ID register field helper functions
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
11. **[05-13 16:33]** [RFC PATCH v1 10/13] target/arm: named_cpu_model: Register Arm64 properties for host model
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
12. **[05-13 16:33]** [RFC PATCH v1 11/13] target/arm: named_cpu_model: introduce named CPU models for selected CPUs
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
13. **[05-13 16:33]** [RFC PATCH v1 12/13] target/arm: named_cpu_model: writeback modified ID registers to KVM
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
14. **[05-13 16:33]** [RFC PATCH v1 13/13] target/arm/kvm: enable writable implementation ID registers
   - 发件人: Shaju Abraham <shaju.abraham@nutanix.com>
15. **[05-15 16:20]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
16. **[05-15 16:20]** Re: [RFC PATCH v1 03/13] target/arm: named_cpu_model: initialise
 additional sysregs
   - 发件人: Eric Auger <eric.auger@redhat.com>
17. **[05-15 16:36]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
18. **[05-15 17:25]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
19. **[05-15 15:27]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
20. **[05-15 17:28]** Re: [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD
 macro with IDREG_FIELD
   - 发件人: Eric Auger <eric.auger@redhat.com>
21. **[05-15 15:31]** Re: [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD
 macro with IDREG_FIELD
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
22. **[05-15 15:36]** Re: [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD
 macro with IDREG_FIELD
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
23. **[05-15 15:37]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
24. **[05-15 17:46]** Re: [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD
 macro with IDREG_FIELD
   - 发件人: Eric Auger <eric.auger@redhat.com>
25. **[05-15 17:54]** Re: [RFC PATCH v1 02/13] target/arm: named_cpu_model: Add ID Register
 Fields
   - 发件人: Eric Auger <eric.auger@redhat.com>
26. **[05-15 17:59]** Re: [RFC PATCH v1 06/13] target/arm: named_cpu_model: data-structures
 required for the ARM property layer.
   - 发件人: Eric Auger <eric.auger@redhat.com>
27. **[05-15 16:04]** Re: [RFC PATCH v1 05/13] target/arm: named_cpu_model: replace FIELD
 macro with IDREG_FIELD
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>
28. **[05-15 16:13]** Re: [RFC PATCH v1 06/13] target/arm: named_cpu_model: data-structures
 required for the ARM property layer.
   - 发件人: Khushit Shah <khushit.shah@nutanix.com>

---

### Thread 2: [RFC PATCH 0/2] Optimize S2 page splitting

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 15 May 2026 20:59:01 +0100

#### 🤖 AI 总结

本邮件线程讨论了优化 S2 页拆分的提案，主要由 Leonardo Bras 提出。原始的补丁（RFC PATCH 0/2）旨在通过引入新的返回值来优化页表遍历机制，从而提高拆分性能。具体来说，补丁建议在遍历过程中，如果发现某个节点的父节点已经被拆分，则可以跳过其兄弟节点的遍历；如果子节点已经被拆分，则可以跳过对该节点子节点的遍历。

在之前的讨论中，Leonardo 提出了优化的初步想法，并分享了在不同虚拟机上进行的性能测试结果，显示出显著的运行时间减少（例如，4K 页的拆分运行时间减少了97.33%）。他还考虑了不同的实现方式和返回值的使用。

本周的新讨论中，Leonardo 进一步细化了补丁内容，具体引入了两个新的返回值：SKIP_CHILDREN 和 SKIP_SIBLINGS，以便在遍历时更有效地跳过不必要的节点。同时，Marc Zyngier 对此提出了质疑，认为在软件模型上进行的性能测量并不可靠，建议在实际硬件上进行测试以获得更准确的结果，并指出应避免在内核中添加控制台输出，以免影响性能测量。

#### 📝 邮件列表

1. **[05-15 20:59]** [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[05-15 20:59]** [RFC PATCH 1/2] KVM: arm64: Introduce S2 walker SKIP return options
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[05-15 20:59]** [RFC PATCH 2/2] KVM: arm64: Improve splitting performance by using SKIP return values
   - 发件人: Leonardo Bras <leo.bras@arm.com>
4. **[05-16 10:15]** Re: [RFC PATCH 0/2] Optimize S2 page splitting
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 3: [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Sun, 10 May 2026 23:11:43 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个针对 KVM（Kernel-based Virtual Machine）在 arm64 架构下的补丁，主题为“跳过 vCPU 尝试锁定以进行预初始化寄存器访问”。该补丁旨在解决在创建虚拟机时，用户空间需要在 VGIC（虚拟通用中断控制器）初始化之前设置一些寄存器的问题。

在历史讨论中，David Woodhouse 提出了补丁的背景，指出在虚拟机创建过程中，用户空间需要在 vCPU0 创建之前设置一些寄存器，但现有设计要求 vCPU0 必须存在。这导致在启动时无法直接设置 IIDR（中断标识符寄存器）。

在本周的新讨论中，Yao Yuan 提出了一个问题，询问是否可以在获取配置锁后进行 vgic_initialized 和 reg_allowed_pre_init 的检查，以决定是否尝试锁定所有 vCPU。对此，David Woodhouse 表示不赞同，因为在持有配置锁的情况下尝试获取 vCPU 锁可能会导致死锁。最终，他认为长远的解决方案是完全移除 kvm_trylock_all_vcpus() 的调用，而不仅仅是在 !vgic_initialized() 的情况下进行处理。

总体而言，本周的讨论集中在补丁的实现细节及其潜在的锁定问题上，参与者们对如何优化代码提出了不同的见解。

#### 📝 邮件列表

1. **[05-10 23:11]** [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access
   - 发件人: David Woodhouse <dwmw2@infradead.org>
2. **[05-11 19:03]** Re: [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access
   - 发件人: Yao Yuan <yaoyuan@linux.alibaba.com>
3. **[05-11 12:52]** Re: [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #2

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Thu,  7 May 2026 16:42:21 +0100

#### 🤖 AI 总结

本邮件线程讨论了 KVM/arm64 在 7.1 版本中的修复补丁，主要由 Marc Zyngier 提出。

**原始 patch/问题的内容**：
Marc 在历史邮件中提交了第二组 KVM/arm64 的修复补丁，指出此次补丁主要包含一些小的 bug 修复，特别是涉及到内存管理单元（MMU）的权限故障处理和 52 位虚拟地址（VA）的问题。此外，还提到了一项与 ARM 错误相关的变通方案，虽然对 KVM 的影响不大，但需要依赖某些固件来处理。

**之前讨论要点**：
在历史讨论中，Marc 强调了补丁的相对简单性，除了 ARM 错误的变通方案外，其他修复主要集中在 MMU 的几个小问题上，并提到了一些来自 Fuad 的 AI 增强修复。

**本周的新讨论、进展或结论**：
在本周的讨论中，Paolo Bonzini 对 Marc 的补丁表示感谢，并确认已完成相关工作。这表明补丁已被接受并将继续推进。

总体来看，本邮件线程主要集中在 KVM/arm64 的修复补丁上，经过讨论后，补丁已得到确认并准备实施。

#### 📝 邮件列表

1. **[05-07 16:42]** [GIT PULL] KVM/arm64 fixes for 7.1, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[05-12 23:15]** Re: [GIT PULL] KVM/arm64 fixes for 7.1, take #2
   - 发件人: Paolo Bonzini <pbonzini@redhat.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI initialization

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Wed, 13 May 2026 21:16:24 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于在 ARM64 平台上通过 ACPI 启动时，设置 `is_pl011_uart` 标志的补丁。该补丁旨在解决在解析 SPCR 表时未正确设置该标志的问题，导致 `__getchar()` 函数错误地将 UART 视为 16550A 设备，从而在使用 PL011 UART 的系统上出现输入挂起的情况。

在历史讨论中没有相关的背景信息，邮件中直接提出了问题和补丁的解决方案。本周的讨论由 Colton Lewis 提出，补丁更新了 `uart0_init_acpi()` 函数，以检查 SPCR 的 `interface_type` 并相应地设置 `is_pl011_uart`。此外，还在 `lib/acpi.h` 中定义了前四种 SPCR 接口类型的宏，以符合微软规范。

本周的进展主要集中在补丁的实现细节上，包括对相关文件的修改和宏定义的添加，确保了在 ARM64 系统中正确初始化 UART，从而避免了因 UART 类型错误导致的系统挂起问题。

#### 📝 邮件列表

1. **[05-13 21:16]** [kvm-unit-tests PATCH] arm: io: Set is_pl011_uart flag in ACPI initialization
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

