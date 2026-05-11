# KVMARM 邮件列表 AI 总结报告

**生成时间**: 2026-05-11 00:47:56

**分析周期**: 最近 7 天

## 📊 总体统计

- **总邮件数**: 251
- **总 Thread 数**: 26
- **大型 Thread** (>20封): 6 个

### 分类分布

- **PATCH**: 18 threads (181 邮件)
- **RFC**: 5 threads (65 邮件)
- **GIT PULL**: 1 threads (1 邮件)
- **Discussion**: 1 threads (2 邮件)
- **Other**: 1 threads (2 邮件)

---

## 📌 PATCH

共 18 个 thread

---

### Thread 1: [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)

**📧 邮件数**: 31 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  1 May 2026 11:19:02 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（Kernel-based Virtual Machine）在 ARM64 架构上实现 SMMUv3 驱动的补丁系列，主要聚焦于“捕获和仿真”功能的开发。

1. **原始补丁/问题的内容**：补丁系列的第六版（v6）旨在为 pKVM 提供 SMMUv3 支持，主要通过捕获和仿真机制来实现 DMA 隔离和其他功能。补丁包括多个方面的改进，如代码重用、TLB 范围失效的通用处理等。

2. **之前的讨论要点**：历史讨论中，参与者对补丁的不同部分进行了深入探讨，提出了代码重用的必要性，尤其是在将命令队列和 TLB 失效逻辑移至共享代码文件中，以便在主机内核和虚拟化环境中复用。此外，Jason Gunthorpe 提出了一些关于代码结构和功能实现的建议，以提高代码的可维护性。

3. **本周的新讨论、进展或结论**：本周的讨论中，Mostafa Saleh 和 Jason Gunthorpe 继续就补丁的具体实现进行交流，讨论了如何在不影响现有功能的情况下共享代码。Mostafa 提到将继续优化代码，并考虑在后续版本中实现更复杂的功能，如共享页面表等。同时，Jason 强调了在设计时应考虑的硬件限制和性能影响，提出了一些具体的实现建议，以确保代码的简洁性和可维护性。

总体而言，讨论围绕如何有效实现 SMMUv3 驱动的功能，确保代码的复用性和可维护性展开，参与者们积极交流，推动补丁的完善。

#### 📝 邮件列表

1. **[05-01 11:19]** [PATCH v6 00/25] KVM: arm64: SMMUv3 driver for pKVM (trap and emulate)
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-01 11:19]** [PATCH v6 03/25] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Mostafa Saleh <smostafa@google.com>
3. **[05-01 11:19]** [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation into
 common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-01 11:19]** [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
5. **[05-01 11:19]** [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
6. **[05-01 11:19]** [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page table
   - 发件人: Mostafa Saleh <smostafa@google.com>
7. **[05-01 11:19]** [PATCH v6 13/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
8. **[05-01 09:24]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
9. **[05-01 09:41]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
10. **[05-01 09:44]** Re: [PATCH v6 03/25] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
11. **[05-01 09:47]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
12. **[05-01 09:51]** Re: [PATCH v6 13/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
13. **[05-01 10:00]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
14. **[05-04 12:13]** Re: [PATCH v6 03/25] iommu/arm-smmu-v3: Split code with hyp
   - 发件人: Mostafa Saleh <smostafa@google.com>
15. **[05-04 12:15]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
16. **[05-04 12:16]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
17. **[05-04 12:19]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Mostafa Saleh <smostafa@google.com>
18. **[05-04 12:28]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Mostafa Saleh <smostafa@google.com>
19. **[05-04 12:30]** Re: [PATCH v6 13/25] iommu/arm-smmu-v3-kvm: Probe SMMU HW
   - 发件人: Mostafa Saleh <smostafa@google.com>
20. **[05-05 13:17]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
21. **[05-05 13:27]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
22. **[05-05 16:43]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
23. **[05-05 16:48]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
24. **[05-06 06:53]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
25. **[05-06 06:56]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
26. **[05-07 09:40]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Mostafa Saleh <smostafa@google.com>
27. **[05-07 10:13]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Mostafa Saleh <smostafa@google.com>
28. **[05-09 20:21]** Re: [PATCH v6 06/25] iommu/io-pgtable-arm: Rework to use the
 iommu-pages API
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
29. **[05-09 20:27]** Re: [PATCH v6 08/25] KVM: arm64: iommu: Shadow host stage-2 page
 table
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
30. **[05-09 20:29]** Re: [PATCH v6 04/25] iommu/arm-smmu-v3: Move TLB range invalidation
 into common code
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>
31. **[05-09 20:34]** Re: [PATCH v6 05/25] iommu/arm-smmu-v3: Move IDR parsing to common
 functions
   - 发件人: Jason Gunthorpe <jgg@ziepe.ca>

---

### Thread 2: [PATCH 00/43] KVM: arm64: Add GICv5 IRS support

**📧 邮件数**: 30 | **👥 参与者**: 4 | **📅 开始时间**: Mon, 27 Apr 2026 16:06:01 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（内核虚拟机）在 arm64 架构下增加 GICv5 IRS（中断路由系统）支持的补丁系列。最初的补丁（PATCH 00/43）旨在扩展 GICv5 的功能，使其支持 SPI（共享中断）和 LPI（本地中断），从而允许在 Arm FVP 模型上启动完整的 Linux 客户机。

在历史讨论中，参与者主要集中在补丁的实现细节上，包括如何管理虚拟机状态表（VMT）和中断状态表（IST），以及如何确保中断的有效性和管理。讨论中提到了一些代码的重复和命名不清晰的问题，参与者提出了改进建议。

在本周的新讨论中，Marc Zyngier 和 Sascha Bischoff 继续对补丁进行审查，提出了关于补丁合并、代码风格和功能实现的具体建议。例如，Marc 建议将某些补丁合并以提高代码的清晰度，并讨论了中断门铃的管理是否必要。Sascha 对这些反馈进行了积极响应，表示已对代码进行了相应的修改和优化，确保了对 GICv5 的支持更加稳健。

总体来看，本周的讨论主要集中在补丁的细节修正和代码清理上，参与者们积极合作，推动补丁的完善。

#### 📝 邮件列表

1. **[04-27 16:06]** [PATCH 00/43] KVM: arm64: Add GICv5 IRS support
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
2. **[04-27 16:08]** [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
3. **[04-27 16:08]** [PATCH 08/43] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
4. **[04-27 16:09]** [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
5. **[04-27 16:09]** [PATCH 10/43] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
6. **[04-27 16:09]** [PATCH 11/43] KVM: arm64: gic-v5: Make VPEs valid in vgic_v5_reset()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
7. **[04-27 16:10]** [PATCH 13/43] KVM: arm64: gic-v5: Make VPEs (non-)resident in
 vgic_load/put
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
8. **[04-27 16:11]** [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and
 disable on teardown
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
9. **[04-27 16:12]** [PATCH 18/43] KVM: arm64: gic-v5: Define remaining IRS MMIO registers
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
10. **[04-27 16:20]** [PATCH 43/43] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
11. **[04-28 16:55]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Joey Gouly <joey.gouly@arm.com>
12. **[04-29 11:25]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE tables
   - 发件人: Marc Zyngier <maz@kernel.org>
13. **[04-29 13:50]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Joey Gouly <joey.gouly@arm.com>
14. **[04-29 15:29]** Re: [PATCH 08/43] KVM: arm64: gic-v5: Introduce guest IST alloc and management
   - 发件人: Marc Zyngier <maz@kernel.org>
15. **[04-29 17:04]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Marc Zyngier <maz@kernel.org>
16. **[04-30 09:46]** Re: [PATCH 10/43] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Marc Zyngier <maz@kernel.org>
17. **[04-30 09:57]** Re: [PATCH 43/43] Documentation: KVM: Add the VGICv5 IRS save/restore sequences
   - 发件人: Peter Maydell <peter.maydell@linaro.org>
18. **[04-30 10:37]** Re: [PATCH 11/43] KVM: arm64: gic-v5: Make VPEs valid in vgic_v5_reset()
   - 发件人: Marc Zyngier <maz@kernel.org>
19. **[04-30 11:26]** Re: [PATCH 13/43] KVM: arm64: gic-v5: Make VPEs (non-)resident in vgic_load/put
   - 发件人: Marc Zyngier <maz@kernel.org>
20. **[05-06 16:03]** Re: [PATCH 17/43] KVM: arm64: gic-v5: Enable VPE DBs on VPE reset and disable on teardown
   - 发件人: Marc Zyngier <maz@kernel.org>
21. **[05-07 16:10]** Re: [PATCH 18/43] KVM: arm64: gic-v5: Define remaining IRS MMIO registers
   - 发件人: Marc Zyngier <maz@kernel.org>
22. **[05-08 12:37]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
23. **[05-08 12:38]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
24. **[05-08 12:42]** Re: [PATCH 07/43] KVM: arm64: gic-v5: Create & manage VM and VPE
 tables
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
25. **[05-08 12:43]** Re: [PATCH 08/43] KVM: arm64: gic-v5: Introduce guest IST alloc and
 management
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
26. **[05-08 13:31]** Re: [PATCH 09/43] KVM: arm64: gic-v5: Implement VMT/vIST IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
27. **[05-08 17:07]** Re: [PATCH 13/43] KVM: arm64: gic-v5: Make VPEs (non-)resident in
 vgic_load/put
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
28. **[05-08 17:08]** Re: [PATCH 11/43] KVM: arm64: gic-v5: Make VPEs valid in
 vgic_v5_reset()
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
29. **[05-08 17:10]** Re: [PATCH 43/43] Documentation: KVM: Add the VGICv5 IRS save/restore
 sequences
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>
30. **[05-08 17:11]** Re: [PATCH 10/43] KVM: arm64: gic-v5: Implement VPE IRS MMIO Ops
   - 发件人: Sascha Bischoff <Sascha.Bischoff@arm.com>

---

### Thread 3: [PATCH v4 00/17] kvm/arm: Introduce a customizable aarch64 KVM host model

**📧 邮件数**: 22 | **👥 参与者**: 2 | **📅 开始时间**: Sun,  3 May 2026 09:33:20 +0200

#### 🤖 AI 总结

本邮件讨论的主题是关于为 KVM/ARM 引入可定制的 AArch64 主机模型的补丁系列（PATCH v4 00/17）。该补丁旨在增强当前的 KVM 主机模型，使其能够设置可写的 ID 寄存器字段，从而在不同硬件之间迁移虚拟机时提供更大的灵活性。

在历史讨论中，Eric Auger 提出了多个补丁，逐步实现了对可写 ID 寄存器的支持，包括对寄存器定义的自动生成、初始化函数的添加以及对 KVM 接口的扩展。这些补丁的目标是使 KVM 能够读取和写入所有可写的 ID 寄存器，并在主机 CPU 模型中暴露这些寄存器的属性。

在本周的新讨论中，参与者 Shameer Kolothum Thodi 针对多个补丁提出了具体的改进建议和问题，例如对补丁中某些宏的使用、返回值的处理、以及在特定情况下的错误处理等。他还指出了在 KVM 隐藏寄存器时可能出现的注册表不匹配问题，并询问该问题在当前系列中是否得到了修复。

总体来看，本周的讨论集中在补丁的细节改进和潜在问题的澄清上，参与者们积极提出反馈，以确保补丁的质量和功能的完整性。

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
7. **[05-03 09:33]** [PATCH v4 10/17] arm/kvm: Allow reading all the writable ID registers
   - 发件人: Eric Auger <eric.auger@redhat.com>
8. **[05-03 09:33]** [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Eric Auger <eric.auger@redhat.com>
9. **[05-03 09:33]** [PATCH v4 12/17] target/arm/kvm: Introduce kvm_arm_expose_idreg_properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
10. **[05-03 09:33]** [PATCH v4 15/17] arm/cpu: Expose writable ID reg field properties on the kvm host vcpu model
   - 发件人: Eric Auger <eric.auger@redhat.com>
11. **[05-03 09:33]** [PATCH v4 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Eric Auger <eric.auger@redhat.com>
12. **[05-06 16:10]** RE: [PATCH v4 02/17] target/arm/cpu-sysregs.h.inc: Sort by name
 alphabetical order
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
13. **[05-07 08:45]** RE: [PATCH v4 03/17] target/arm/cpu-sysregs.h.inc: Update with
 automatic generation
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
14. **[05-07 08:58]** RE: [PATCH v4 04/17] arm/cpu: Add infra to handle generated ID
 register definitions
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
15. **[05-07 10:07]** RE: [PATCH v4 08/17] target/arm/kvm: Introduce
 kvm_get_writable_id_regs
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
16. **[05-07 10:32]** RE: [PATCH v4 09/17] arm/cpu: accessors for writable id registers
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
17. **[05-07 11:50]** RE: [PATCH v4 10/17] arm/kvm: Allow reading all the writable ID
 registers
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
18. **[05-07 18:53]** RE: [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
19. **[05-07 19:10]** RE: [PATCH v4 12/17] target/arm/kvm: Introduce
 kvm_arm_expose_idreg_properties
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
20. **[05-07 19:22]** RE: [PATCH v4 15/17] arm/cpu: Expose writable ID reg field properties
 on the kvm host vcpu model
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
21. **[05-07 19:44]** RE: [PATCH v4 17/17] arm/cpu-features: document ID reg properties
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>
22. **[05-08 13:03]** RE: [PATCH v4 11/17] arm/kvm: write back modified ID regs to KVM
   - 发件人: Shameer Kolothum Thodi <skolothumtho@nvidia.com>

---

### Thread 4: [PATCH v7 00/20] ARM64 PMU Partitioning

**📧 邮件数**: 21 | **👥 参与者**: 1 | **📅 开始时间**: Mon,  4 May 2026 21:17:53 +0000

#### 🤖 AI 总结

本邮件线程讨论了关于 ARM64 PMU（性能监控单元）分区的补丁系列，主要集中在为虚拟机（VM）提供更高效的性能计数器访问。以下是讨论的要点：

1. **原始补丁内容**：补丁系列旨在创建一个新的 ARM64 PMU 分区方案，允许将部分计数器保留给虚拟机使用，从而显著降低性能开销。补丁包括动态计数器保留的实现和性能基准测试。

2. **历史讨论要点**：之前的讨论主要集中在如何实现动态计数器保留，以及如何在不干扰主机性能的情况下有效管理计数器的访问。补丁经过多次迭代，最终确定了通过 `perf_pmu_resched_update` 函数来动态更新可用计数器的方案。

3. **本周新讨论及进展**：本周的讨论包括多个补丁的提交，主要内容包括：
   - **动态计数器保留**：通过检查请求的虚拟机掩码与主机事件的冲突，调用 `perf_pmu_resched_update` 来更新可用计数器。
   - **懒惰的 PMU 上下文切换**：仅在虚拟机访问 PMU 寄存器时才进行上下文切换，以减少不必要的性能开销。
   - **处理溢出**：在处理 PMU 中断后，检测是否有虚拟机计数器溢出，并在必要时向虚拟机注入中断。
   - **分区 PMU 的测试用例**：为分区 PMU 添加自测用例，确保其在不同情况下的正确性。

整体来看，本周的讨论和补丁提交为 ARM64 的 PMU 分区功能的实现奠定了基础，旨在提升虚拟化环境中的性能监控能力。

#### 📝 邮件列表

1. **[05-04 21:17]** [PATCH v7 00/20] ARM64 PMU Partitioning
   - 发件人: Colton Lewis <coltonlewis@google.com>
2. **[05-04 21:17]** [PATCH v7 01/20] arm64: cpufeature: Add cpucap for HPMN0
   - 发件人: Colton Lewis <coltonlewis@google.com>
3. **[05-04 21:17]** [PATCH v7 02/20] KVM: arm64: Reorganize PMU includes
   - 发件人: Colton Lewis <coltonlewis@google.com>
4. **[05-04 21:17]** [PATCH v7 03/20] KVM: arm64: Reorganize PMU functions
   - 发件人: Colton Lewis <coltonlewis@google.com>
5. **[05-04 21:17]** [PATCH v7 04/20] perf: arm_pmuv3: Generalize counter bitmasks
   - 发件人: Colton Lewis <coltonlewis@google.com>
6. **[05-04 21:17]** [PATCH v7 05/20] perf: arm_pmuv3: Check cntr_mask before using pmccntr
   - 发件人: Colton Lewis <coltonlewis@google.com>
7. **[05-04 21:17]** [PATCH v7 06/20] perf: arm_pmuv3: Add method to partition the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
8. **[05-04 21:18]** [PATCH v7 07/20] KVM: arm64: Set up FGT for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
9. **[05-04 21:18]** [PATCH v7 08/20] KVM: arm64: Add Partitioned PMU register trap handlers
   - 发件人: Colton Lewis <coltonlewis@google.com>
10. **[05-04 21:18]** [PATCH v7 09/20] KVM: arm64: Set up MDCR_EL2 to handle a Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
11. **[05-04 21:18]** [PATCH v7 10/20] KVM: arm64: Context swap Partitioned PMU guest registers
   - 发件人: Colton Lewis <coltonlewis@google.com>
12. **[05-04 21:18]** [PATCH v7 11/20] KVM: arm64: Enforce PMU event filter at vcpu_load()
   - 发件人: Colton Lewis <coltonlewis@google.com>
13. **[05-04 21:18]** [PATCH v7 12/20] perf: Add perf_pmu_resched_update()
   - 发件人: Colton Lewis <coltonlewis@google.com>
14. **[05-04 21:18]** [PATCH v7 13/20] KVM: arm64: Apply dynamic guest counter reservations
   - 发件人: Colton Lewis <coltonlewis@google.com>
15. **[05-04 21:18]** [PATCH v7 14/20] KVM: arm64: Implement lazy PMU context swaps
   - 发件人: Colton Lewis <coltonlewis@google.com>
16. **[05-04 21:18]** [PATCH v7 15/20] perf: arm_pmuv3: Handle IRQs for Partitioned PMU
 guest counters
   - 发件人: Colton Lewis <coltonlewis@google.com>
17. **[05-04 21:18]** [PATCH v7 16/20] KVM: arm64: Detect overflows for the Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
18. **[05-04 21:18]** [PATCH v7 17/20] KVM: arm64: Add vCPU device attr to partition the PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
19. **[05-04 21:18]** [PATCH v7 18/20] KVM: selftests: Add find_bit to KVM library
   - 发件人: Colton Lewis <coltonlewis@google.com>
20. **[05-04 21:18]** [PATCH v7 19/20] KVM: arm64: selftests: Add test case for Partitioned PMU
   - 发件人: Colton Lewis <coltonlewis@google.com>
21. **[05-04 21:18]** [PATCH v7 20/20] KVM: arm64: selftests: Relax testing for exceptions
 when partitioned
   - 发件人: Colton Lewis <coltonlewis@google.com>

---

### Thread 5: [PATCH 0/5] KVM: Fix race conditions in kvm_arch_flush_shadow_all()

**📧 邮件数**: 16 | **👥 参与者**: 3 | **📅 开始时间**: Mon,  4 May 2026 22:42:07 +0000

#### 🤖 AI 总结

本邮件线程讨论了针对 KVM（内核虚拟机）中 `kvm_arch_flush_shadow_all()` 函数的多个补丁，以修复潜在的竞争条件和双重释放问题。

1. **原始问题**：在 KVM 的不同架构（如 arm64、loongarch 和 mips）中，`kvm_arch_flush_shadow_all()` 可能会被多个进程同时调用，导致内存缓存的双重释放。具体来说，当一个进程（P1）关闭虚拟机（VM），而另一个进程（P2）仍持有对该 VM 的引用时，可能会出现竞争条件。

2. **历史讨论要点**：之前的讨论集中在如何通过适当的锁机制来防止这些竞争条件。补丁的初步版本已经提出，针对每个受影响的架构进行了锁的调整，以确保在调用 `kvm_arch_flush_shadow_all()` 时持有 MMU 锁。

3. **本周新讨论与进展**：本周的讨论中，James Houghton 提出了五个补丁，分别针对 arm64、loongarch 和 mips 架构的修复，并建议在调用 `kvm_arch_flush_shadow_all()` 时独占持有 MMU 锁。补丁还包括一个自测用例，以可靠地展示双重释放的问题。讨论中还提到需要重新考虑内存缓存的管理，特别是在用户空间可能会异常关闭 VM 的情况下，确保不会导致内存泄漏或错误释放。

总结而言，本次讨论的重点在于通过补丁修复 KVM 中的竞争条件，确保不同架构在处理虚拟机内存时的安全性和稳定性。

#### 📝 邮件列表

1. **[05-04 22:42]** [PATCH 0/5] KVM: Fix race conditions in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
2. **[05-04 22:42]** [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
3. **[05-04 22:42]** [PATCH 2/5] KVM: loongarch: Grab MMU lock in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
4. **[05-04 22:42]** [PATCH 3/5] KVM: mips: Grab MMU lock in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
5. **[05-04 22:42]** [PATCH 4/5] KVM: Hold MMU lock exclusively when calling kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
6. **[05-04 22:42]** [PATCH 5/5] DO NOT MERGE: KVM: selftests: Reproducer for arm64 double-free
   - 发件人: James Houghton <jthoughton@google.com>
7. **[05-04 15:44]** Re: [PATCH 0/5] KVM: Fix race conditions in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
8. **[05-04 23:10]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
9. **[05-05 10:05]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: Sean Christopherson <seanjc@google.com>
10. **[05-05 11:01]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: James Houghton <jthoughton@google.com>
11. **[05-05 11:16]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: Sean Christopherson <seanjc@google.com>
12. **[05-05 13:14]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: Sean Christopherson <seanjc@google.com>
13. **[05-06 10:27]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in
 kvm_arch_flush_shadow_all()
   - 发件人: Bibo Mao <maobibo@loongson.cn>
14. **[05-06 06:55]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in kvm_arch_flush_shadow_all()
   - 发件人: Sean Christopherson <seanjc@google.com>
15. **[05-07 09:40]** Re: [PATCH 1/5] KVM: arm64: Grab KVM MMU write lock in
 kvm_arch_flush_shadow_all()
   - 发件人: Bibo Mao <maobibo@loongson.cn>
16. **[05-08 15:21]** Re: [PATCH 2/5] KVM: loongarch: Grab MMU lock in
 kvm_arch_flush_shadow_all()
   - 发件人: Bibo Mao <maobibo@loongson.cn>

---

### Thread 6: [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe

**📧 邮件数**: 8 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 08 May 2026 18:54:14 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于将 Arm FF-A 核心初始化移至平台驱动探测的补丁系列，共包含四个补丁。

首先，原始补丁的内容是将 Arm FF-A 核心的初始化过程转换为平台驱动的探测和移除流程，以便更好地融入驱动模型。补丁中提到，之前的 rootfs_initcall 变更被撤回，因为该解决方案不够妥当，并可能与 pKVM FF-A 代理的要求冲突。此外，补丁还引入了一个合成的 arm-ffa 平台设备，以便在 ACPI 和设备树能够直接描述 FF-A 核心设备之前，作为临时桥接。

在之前的讨论中，主要集中在如何处理 FF-A 核心的生命周期与驱动模型的兼容性，以及确保在启用保护 KVM 时，FF-A 的探测被延迟到 pKVM 初始化完成后进行。

本周的新讨论中，所有四个补丁都得到了参与者 Yeoreum Yun 的认可，表示“看起来很好”（LGTM），并没有提出进一步的修改建议。这表明补丁系列在技术上得到了共识，预计将会被合并到主线代码中。

#### 📝 邮件列表

1. **[05-08 18:54]** [PATCH 0/4] firmware: arm_ffa: Move core init to platform driver
 probe
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
2. **[05-08 18:54]** [PATCH 1/4] Revert "firmware: arm_ffa: Change initcall level of
 ffa_init() to rootfs_initcall"
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
3. **[05-08 18:54]** [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
4. **[05-08 18:54]** [PATCH 3/4] firmware: arm_ffa: Set the core device as FF-A device
 parent
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
5. **[05-08 18:54]** [PATCH 4/4] firmware: arm_ffa: Defer probe until pKVM is
 initialized
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
6. **[05-08 19:41]** Re: [PATCH 2/4] firmware: arm_ffa: Register core as a platform driver
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[05-08 19:42]** Re: [PATCH 3/4] firmware: arm_ffa: Set the core device as FF-A
 device parent
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[05-08 19:45]** Re: [PATCH 4/4] firmware: arm_ffa: Defer probe until pKVM is
 initialized
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>

---

### Thread 7: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone

**📧 邮件数**: 8 | **👥 参与者**: 3 | **📅 开始时间**: Fri,  1 May 2026 11:44:48 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下将 FFA_NOTIFICATION* 调用转发到 TrustZone 的补丁（patch）。该补丁旨在移除 pKVM FF-A 代理中的 FFA_NOTIFICATION* 调用黑名单，以允许使用 Arm FF-A 规范定义的异步信号机制与安全服务进行通信。

在历史讨论中，Sebastian Ene 提出了该补丁的背景，强调了主机作为唯一的非安全端点（VM ID 0）在安全世界中的角色，并指出当前的限制阻碍了异步信号的使用。

本周的新讨论中，Marc Zyngier 提出了对补丁的多个质疑，主要集中在如何确保主机请求总是被视为来自 VM ID 0，以及是否需要对某些寄存器进行清理（sanitization）。Sebastian 解释说，当前 hypervisor 中并没有强制执行这一点，因为只有主机作为非安全用户。Marc 进一步强调了需要严格遵循规范，避免潜在的安全隐患，并建议在补丁中加入对 SBZ（Should Be Zero）寄存器的检查。

最终，Sebastian 同意在补丁中加入对 SBZ 寄存器的检查，以确保实现的合规性。Sudeep Holla 也参与了讨论，确认了主机 FF-A 驱动实例在 pKVM FF-A 代理中的角色。整体来看，讨论围绕补丁的安全性和合规性展开，强调了对规范的严格遵循。

#### 📝 邮件列表

1. **[05-01 11:44]** [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
2. **[05-06 17:29]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Marc Zyngier <maz@kernel.org>
3. **[05-07 10:48]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
4. **[05-07 14:36]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Marc Zyngier <maz@kernel.org>
5. **[05-07 14:13]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
6. **[05-07 15:21]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Marc Zyngier <maz@kernel.org>
7. **[05-08 13:04]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sebastian Ene <sebastianene@google.com>
8. **[05-08 17:57]** Re: [PATCH] KVM: arm64: Forward FFA_NOTIFICATION* calls to TrustZone
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 8: [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse map

**📧 邮件数**: 6 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 10 May 2026 15:53:33 +0100

#### 🤖 AI 总结

本邮件主题为“[PATCH v3 0/5] KVM: arm64: nv: 实现嵌套阶段2反向映射”，主要讨论了针对KVM（Kernel-based Virtual Machine）在arm64架构下的嵌套虚拟化的优化补丁。

1. **原始补丁内容**：该补丁系列旨在优化在MMU（内存管理单元）通知期间的shadow S2 MMU反映射过程。补丁包括五个部分，涉及到减少kvm_s2_mmu中的空洞、重构代码、避免完全解除映射、在TLBI（Translation Lookaside Buffer Invalidate）处理期间移除反向映射条目，以及创建嵌套IPA（Intermediate Physical Address）直接映射以加速反向映射的移除。

2. **之前讨论要点**：在之前的讨论中，开发者们关注了如何有效管理嵌套虚拟化中的反向映射，尤其是在TLBI操作时，如何减少不必要的映射解除和提高性能。

3. **本周新讨论与进展**：本周的讨论中，Wei-Lin Chang 提出了补丁的更新，包括移除“污染”术语、使用xa_{mk, to}_value()存储和检索maple树中的值、避免使用maple树值的第63位、在TLBI处理期间添加反向映射移除功能等。补丁的整体结构和逻辑得到了进一步的优化和清晰化，增强了代码的可读性和性能。

总的来说，邮件讨论集中在如何通过补丁优化KVM在嵌套虚拟化中的内存管理，提升系统性能和稳定性。

#### 📝 邮件列表

1. **[05-10 15:53]** [PATCH v3 0/5] KVM: arm64: nv: Implement nested stage-2 reverse map
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-10 15:53]** [PATCH v3 1/5] KVM: arm64: Use a variable for the canonical GPA in kvm_s2_fault_map()
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
3. **[05-10 15:53]** [PATCH v3 2/5] KVM: arm64: Move shadow_pt_debugfs_dentry to reduce holes in kvm_s2_mmu
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
4. **[05-10 15:53]** [PATCH v3 3/5] KVM: arm64: nv: Avoid full shadow s2 unmap
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
5. **[05-10 15:53]** [PATCH v3 4/5] KVM: arm64: nv: Remove reverse map entries during TLBI handling
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
6. **[05-10 15:53]** [PATCH v3 5/5] KVM: arm64: nv: Create nested IPA direct map to speed up reverse map removal
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>

---

### Thread 9: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Thu, 30 Apr 2026 10:37:24 +0000

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的时钟硬化补丁，旨在增强 nvhe/pKVM 的稳定性。历史讨论中，Mostafa Saleh 提出了该补丁，指出在 `trace_clock_update()` 函数中可能存在除零和越界位移的问题，尽管时钟更新来自不可信的主机，但仍需基本检查以避免时钟值失去同步。

在本周的新讨论中，参与者对补丁的有效性进行了深入探讨。Vincent Donnefort 提出，尽管主机仍可能写入导致时钟失去同步的值，但补丁的目的是避免在主机出现错误时触发未定义行为，如除零或大位移。Mostafa 进一步建议修改补丁说明，以明确其目的在于防止主机引发的未定义行为，而非真正增强时钟的安全性。最终，Marc Zyngier 表示已将补丁应用于修复，并感谢参与者的贡献。

综上所述，该补丁虽然未能完全解决时钟同步问题，但通过预防潜在的未定义行为，为 KVM 的稳定性提供了一定保障。

#### 📝 邮件列表

1. **[04-30 10:37]** [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>
2. **[05-06 16:03]** Re: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-06 16:10]** Re: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Mostafa Saleh <smostafa@google.com>
4. **[05-06 16:23]** Re: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
5. **[05-06 16:34]** Re: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-06 17:14]** Re: [PATCH] KVM: arm64: Harden clock for nvhe/pKVM
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 10: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for protected guests

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Tue,  5 May 2026 17:52:03 +0100

#### 🤖 AI 总结

本邮件线程讨论了针对 C1-Pro 处理器的 erratum 4193714 的修复补丁，主要涉及 KVM（Kernel-based Virtual Machine）在 arm64 架构下的保护模式。

1. **原始补丁内容**：补丁旨在解决 C1-Pro 核心在使用 SME（Scalable Matrix Extension）时，TLBI（Translation Lookaside Buffer Invalidate）和 DSB（Data Synchronization Barrier）未能完成所有 SME 访问的问题。该问题影响了 pKVM（Protected KVM）的安全保证，因此需要在 EL3（Exception Level 3）中实施解决方案，以避免 EL1（Exception Level 1）屏蔽来自 EL2 的中断。

2. **之前讨论要点**：补丁的 v1 版本已经提出，主要讨论了如何在 KVM 的初始化过程中检查固件支持，并在缺失时拒绝初始化超管模式。参与者对补丁的实现细节进行了初步评估。

3. **本周新讨论与进展**：本周的讨论集中在补丁的细节和潜在问题上。参与者 Vincent Donnefort 提出，考虑到 pKVM 目前处于实验阶段，可能只需发出警告而非完全拒绝初始化。Marc Zyngier 表示希望在补丁中明确这一点，以免用户对不支持的行为产生误解。最终，Marc 确认已将补丁应用到修复中，并表示不需要重新提交。

综上所述，该补丁及其讨论旨在确保 KVM 在处理特定硬件错误时的稳定性和安全性，尽管目前仍存在一些实现和用户期望管理上的挑战。

#### 📝 邮件列表

1. **[05-05 17:52]** [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for protected guests
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
2. **[05-06 14:37]** Re: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for
 protected guests
   - 发件人: Vincent Donnefort <vdonnefort@google.com>
3. **[05-06 15:21]** Re: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for protected guests
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[05-06 16:48]** Re: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for
 protected guests
   - 发件人: Catalin Marinas <catalin.marinas@arm.com>
5. **[05-06 17:06]** Re: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for protected guests
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-06 17:14]** Re: [PATCH v2] KVM: arm64: Work around C1-Pro erratum 4193714 for protected guests
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 11: [PATCH v4 0/3] Enforce host page-size alignment for shared buffers

**📧 邮件数**: 6 | **👥 参与者**: 3 | **📅 开始时间**: Mon, 27 Apr 2026 12:01:05 +0530

#### 🤖 AI 总结

本邮件讨论主题为“强制共享缓冲区的主机页面大小对齐”，主要围绕一系列补丁（patch）进行。补丁的核心内容是确保在私有内存虚拟机中，分配与主机共享的缓冲区时，必须遵循主机的页面大小对齐要求。这是因为这些缓冲区不仅由虚拟机内核访问，还由主机内核访问，确保对齐可以提高系统的稳定性和性能。

在历史讨论中，Aneesh Kumar K.V 提出了补丁的初步版本，并解释了其必要性。Marc Zyngier 对补丁中的一些命名和实现细节提出了质疑，认为某些命名不够准确，且缺乏必要的文档支持。此外，讨论中还涉及到不同架构（如 Arm 和 x86）在处理共享内存时的对齐要求和实现差异。

在本周的新讨论中，Aneesh 针对 Marc 提出的命名问题进行了回应，并探讨了如何在多个 RMI 和 RSI 调用中保持一致性，尤其是在参数类型（如使用 unsigned long 或 u64）方面。此外，Aneesh 还询问了对接口更新的具体建议，显示出对改进补丁的开放态度。

总体来看，本周的讨论延续了对补丁细节的深入探讨，旨在确保补丁的准确性和有效性。

#### 📝 邮件列表

1. **[04-27 12:01]** [PATCH v4 0/3] Enforce host page-size alignment for shared buffers
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
2. **[04-27 12:01]** [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Aneesh Kumar K.V (Arm) <aneesh.kumar@kernel.org>
3. **[04-27 11:33]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Marc Zyngier <maz@kernel.org>
4. **[04-28 18:19]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>
5. **[04-28 14:49]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change alignment via RHI
   - 发件人: Marc Zyngier <maz@kernel.org>
6. **[05-06 19:53]** Re: [PATCH v4 3/3] coco: guest: arm64: Query host IPA-change
 alignment via RHI
   - 发件人: Aneesh Kumar K.V <aneesh.kumar@kernel.org>

---

### Thread 12: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd

**📧 邮件数**: 4 | **👥 参与者**: 3 | **📅 开始时间**: Tue, 21 Apr 2026 09:36:45 -0700

#### 🤖 AI 总结

本邮件线程讨论了针对 `guest_memfd` 的直接映射移除支持的补丁（PATCH v12 00/16）。该补丁旨在改进内存管理，允许在不使用直接映射的情况下处理虚拟机内存。

在历史讨论中，参与者们一致认为补丁应分为两个部分：内存管理（mm）相关的更改通过 mm 树合并，而 KVM 相关的更改则通过 KVM 树合并。Sean Christopherson 和 Frank van der Linden 提出了对补丁的具体实现建议，强调了清晰的 ABI 设计。

本周的新讨论中，Takahiro Itazuri 接手了该系列补丁的后续工作，并对补丁的分拆和合并策略进行了进一步探讨。他提出了两种路径：一种是先在 KVM 侧验证设计，然后再进行分拆；另一种是提前分拆并与 mm 子系统并行寻求共识。Takahiro 还详细说明了在补丁中采用文件映射级别的方法，强调了在不同路径下的内存处理逻辑。

总体而言，讨论集中在如何有效地推进补丁的合并和实现细节上，确保各方的需求和设计理念能够得到满足。

#### 📝 邮件列表

1. **[04-21 09:36]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Sean Christopherson <seanjc@google.com>
2. **[04-21 10:08]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from
 direct map
   - 发件人: Frank van der Linden <fvdl@google.com>
3. **[05-06 08:07]** Re: [PATCH v12 00/16] Direct Map Removal Support for guest_memfd
   - 发件人: Takahiro Itazuri <itazur@amazon.com>
4. **[05-08 08:18]** Re: [PATCH v12 10/16] KVM: guest_memfd: Add flag to remove from direct map
   - 发件人: Takahiro Itazuri <itazur@amazon.com>

---

### Thread 13: [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)

**📧 邮件数**: 4 | **👥 参与者**: 2 | **📅 开始时间**: Thu, 30 Apr 2026 12:14:04 +0100

#### 🤖 AI 总结

本邮件列表讨论的主题是关于KVM脏位清理加速器（HACDBS）的补丁集。该补丁集旨在为arm64架构创建一个特定的脏位清理加速器，依赖于HACDBS机制，并需要在架构通用的KVM代码中添加一些代码片段。

在历史讨论中，Leonardo Bras 提出了补丁集的初步内容，包括补丁1和补丁2，目的是为了使该功能可测试，并指出补丁1应包含在HDBSS补丁集中，而补丁2则是从其他补丁中收集的代码片段。Mark Brown 对补丁4进行了审查，并给予了认可，表示其符合相关文档的要求。

在本周的新讨论中，Leonardo Bras 对Mark Brown的审查表示感谢，表明补丁集的进展顺利。整体来看，补丁集的开发和审查过程正在推进，相关的技术细节也在不断完善中。

#### 📝 邮件列表

1. **[04-30 12:14]** [PATCH v1 00/12] KVM Dirty-bit cleaning accelerator (HACDBS)
   - 发件人: Leonardo Bras <leo.bras@arm.com>
2. **[04-30 12:14]** [PATCH v1 04/12] arm64/sysreg: Add HACDBS consumer and base registers
   - 发件人: Leonardo Bras <leo.bras@arm.com>
3. **[05-03 10:01]** Re: [PATCH v1 04/12] arm64/sysreg: Add HACDBS consumer and base
 registers
   - 发件人: Mark Brown <broonie@kernel.org>
4. **[05-05 12:03]** Re: [PATCH v1 04/12] arm64/sysreg: Add HACDBS consumer and base registers
   - 发件人: Leonardo Bras <leo.bras@arm.com>

---

### Thread 14: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field extracted from wrong value

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 24 Apr 2026 12:07:57 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的修复补丁，主要涉及 VGIC（虚拟通用中断控制器）中 IIDR（中断接口描述符寄存器）修订字段提取错误的问题。

**原始 patch/问题内容**：
补丁 [PATCH 1/3] 旨在修复从错误值提取 IIDR 修订字段的问题。该补丁已被应用于修复分支，确保在从旧内核版本升级时能够保持与来宾的兼容性。

**之前讨论要点**：
在历史讨论中，Marc Zyngier 提到该补丁不仅修复了 IIDR 值与实际行为之间的奇怪不一致，还指出了在从早期内核版本（pre-d53c2c29ae0d）升级时，保持来宾兼容性的问题。David Woodhouse 确认补丁已被应用，并感谢贡献者。

**本周的新讨论、进展或结论**：
在本周的讨论中，David Woodhouse 提出了一个问题，询问为何其他相关修复没有在 7.1 版本中发布。这表明在补丁系列中可能还有其他待解决的问题，期待后续的进一步讨论和解决方案。

#### 📝 邮件列表

1. **[04-24 12:07]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field extracted from wrong value
   - 发件人: Marc Zyngier <maz@kernel.org>
2. **[04-24 13:24]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>
3. **[05-10 22:28]** Re: (subset) [PATCH 1/3] KVM: arm64: vgic: Fix IIDR revision field
 extracted from wrong value
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

### Thread 15: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 8 May 2026 18:12:01 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于对 ARM64 架构中 SMIDR_EL1 寄存器的更新，具体是将其更新为 DDI0601 版本的补丁（PATCH v10 01/30）。该补丁的目的是确保 ARM 架构的系统寄存器与最新的 ARM 文档保持一致。

在之前的讨论中，参与者 Mark Brown 提出了对补丁的关注，询问是否有后续的补丁会依赖于这些更新的字段，以及当前的 RES0 字段定义是否足够。讨论中提到，HIP 的变化可能会导致向后不兼容，并探讨了是否需要将这些变化暴露给虚拟机（VM）。

在本周的新讨论中，Mark Rutland 进一步指出，当前并未向虚拟机暴露优先级支持，因此暂时不需要担心相关问题。他还讨论了 SMCR_ELx.LEN 和 ZCR_ELx.LEN 字段的状态性，质疑现有的清理逻辑是否正确或必要，并建议在处理有效值时进行更清晰的说明。此外，他提到在处理 SMCR_EL{1,2} 的陷阱时，可能需要对相关字段进行更具体的命名。

总体而言，本周的讨论围绕补丁的实现细节和潜在影响展开，参与者对如何处理寄存器字段的状态性和兼容性问题进行了深入探讨。

#### 📝 邮件列表

1. **[05-08 18:12]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Rutland <mark.rutland@arm.com>
2. **[05-08 18:20]** Re: [PATCH v10 15/30] KVM: arm64: Support SME control registers
   - 发件人: Mark Rutland <mark.rutland@arm.com>
3. **[05-09 09:43]** Re: [PATCH v10 01/30] arm64/sysreg: Update SMIDR_EL1 to DDI0601
 2025-06
   - 发件人: Mark Brown <broonie@kernel.org>

---

### Thread 16: [PATCH v2] KVM: arm64: Handle permission faults with guest_memfd

**📧 邮件数**: 3 | **👥 参与者**: 3 | **📅 开始时间**: Tue,  5 May 2026 10:49:13 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下处理与 `guest_memfd` 相关的权限故障的补丁（PATCH v2）。该补丁的主要目的是修复在处理权限故障时可能导致的无限循环问题。

在历史讨论中，补丁的初始版本（v1）已经提出，并进行了相关的修改和测试。补丁的核心内容是通过调用 `kvm_pgtable_stage2_relax_perms()` 来放宽权限，从而允许虚拟机继续执行，而不是在权限故障时陷入死循环。

本周的新讨论中，Alexandru Elisei 详细阐述了补丁的实现细节，指出在处理权限故障时，`gmem_abort()` 函数会调用 `kvm_pgtable_stage2_map()`，如果仅修改权限而不改变映射，可能会导致返回 -EAGAIN，从而使 KVM 返回到故障指令，造成无限循环。为了解决这个问题，补丁通过放宽权限来允许虚拟机继续执行。Fuad Tabba 对该补丁进行了审核并表示支持，而 Marc Zyngier 则确认已将补丁应用于修复中。

总结来说，该补丁有效解决了 KVM 在处理权限故障时的一个关键问题，并得到了社区成员的认可和支持。

#### 📝 邮件列表

1. **[05-05 10:49]** [PATCH v2] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[05-05 13:00]** Re: [PATCH v2] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Fuad Tabba <tabba@google.com>
3. **[05-06 17:14]** Re: [PATCH v2] KVM: arm64: Handle permission faults with guest_memfd
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 17: [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri,  1 May 2026 12:21:43 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 EL2 同步和 pKVM 阶段 2 错误传播修复的补丁（PATCH v2 0/6）。该补丁的主要目的是解决在虚拟化环境中可能出现的错误和同步问题。

在历史讨论中，Fuad Tabba 提出了补丁的第二版，主要修正了之前版本中的一些错误和不准确之处，包括对 SCTLR_EL2 的转换和自测试虚拟 CPU 的内存缓存流程的调整。补丁包含六个部分，涵盖了 EL2 异常的上下文同步、对 NULL 虚拟 CPU 的保护、宏参数的拼写错误修复等。

在本周的新讨论中，Marc Zyngier 确认已将这些补丁应用于修复分支，并列出了每个补丁的具体提交信息。这表明补丁已经获得了认可并进入了代码库，标志着该问题的解决进展。

总体来看，本次讨论集中在 KVM 的错误修复和同步问题上，补丁已成功应用，显示出社区对提升虚拟化稳定性的持续努力。

#### 📝 邮件列表

1. **[05-01 12:21]** [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error
 propagation fixes
   - 发件人: Fuad Tabba <tabba@google.com>
2. **[05-07 14:20]** Re: [PATCH v2 0/6] KVM: arm64: EL2 synchronisation and pKVM stage-2 error propagation fixes
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 18: [PATCH] KVM: arm64: nv: Consider the DS bit when translating TCR_EL2

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Tue,  5 May 2026 15:47:35 +0100

#### 🤖 AI 总结

本邮件讨论主题为“[PATCH] KVM: arm64: nv: 考虑在转换 TCR_EL2 时的 DS 位”。该补丁旨在解决在运行 nVHE L1 时，TCR_EL2 映射到 TCR_EL1 的问题。具体来说，补丁修复了在 52 位虚拟地址下启动 nVHE L1 时，由于忽略了由客户机设置的 DS 位，导致重复的级别 0 故障。

在历史讨论中并未提供具体内容，但本周的新讨论中，Wei-Lin Chang 提出了补丁，指出在转换函数中需要添加对 DS 位的考虑。补丁的代码修改了 `translate_tcr_el2_to_tcr_el1` 函数，以确保正确处理 DS 位。

Marc Zyngier 在随后的邮件中确认已将该补丁应用于修复列表，并表示感谢。这表明该补丁得到了认可并将被纳入后续的内核更新中。整体来看，本周的讨论集中在补丁的提出和确认上，标志着问题的解决进展。

#### 📝 邮件列表

1. **[05-05 15:47]** [PATCH] KVM: arm64: nv: Consider the DS bit when translating TCR_EL2
   - 发件人: Wei-Lin Chang <weilin.chang@arm.com>
2. **[05-06 17:14]** Re: [PATCH] KVM: arm64: nv: Consider the DS bit when translating TCR_EL2
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 RFC

共 5 个 thread

---

### Thread 1: [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue

**📧 邮件数**: 34 | **👥 参与者**: 7 | **📅 开始时间**: Fri, 24 Apr 2026 14:23:45 +0100

#### 🤖 AI 总结

本邮件线程讨论了一个关于 IMA（Integrity Measurement Architecture）与 TPM（Trusted Platform Module）初始化顺序的问题，主要通过一系列补丁进行修复。

1. **原始补丁内容**：Jonathan McDowell 提出的补丁系列（RFC PATCH v3 0/4）旨在解决 IMA 在 TPM 尚未完全注册时尝试初始化的问题，避免了 TPM 测量扩展失败的情况。补丁包括在 `late_initcall_sync` 阶段进行 IMA 初始化，并撤销了之前为解决该问题而对 FF-A 驱动所做的更改。

2. **之前讨论要点**：在历史讨论中，参与者们探讨了将 IMA 初始化推迟到 `late_initcall_sync` 是否会导致丢失测量记录的问题。Mimi Zohar 提出了在不同架构上进行测试的必要性，并对 TPM 初始化的顺序表示关注。

3. **本周新讨论与进展**：本周的讨论集中在 TPM 初始化与 IMA 的关系上。Paul Moore 强调在某些架构上，推迟 IMA 初始化可能会导致丢失测量记录。Yeoreum Yun 提出了一种可能的解决方案，通过 Kconfig 选项控制 IMA 的初始化时间，以便在 TPM 初始化延迟的情况下支持 `boot_aggregate_late`。此外，讨论还涉及到如何处理在 IMA 初始化之前的早期测量问题，参与者们认为需要找到一种方法来解决这一问题，以确保系统的完整性和安全性。

#### 📝 邮件列表

1. **[04-24 14:23]** [RFC PATCH v3 0/4] Fix IMA + TPM initialisation ordering issue
   - 发件人: Jonathan McDowell <noodles@earth.li>
2. **[04-24 14:24]** [RFC PATCH v3 4/4] Revert "firmware: arm_ffa: Change initcall level
 of ffa_init() to rootfs_initcall"
   - 发件人: Jonathan McDowell <noodles@earth.li>
3. **[04-29 16:01]** [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
4. **[04-30 10:48]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[04-30 17:39]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
6. **[04-30 18:35]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
7. **[04-30 21:51]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
8. **[05-01 12:52]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: David Safford <david.safford@gmail.com>
9. **[05-03 07:36]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
10. **[05-03 08:42]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
11. **[05-03 12:46]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
12. **[05-04 08:02]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
13. **[05-04 16:51]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
14. **[05-05 17:02]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
15. **[05-05 18:55]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
16. **[05-05 21:51]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
17. **[05-05 22:11]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Paul Moore <paul@paul-moore.com>
18. **[05-06 06:54]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
19. **[05-06 08:23]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
20. **[05-06 07:47]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
21. **[05-06 14:57]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
22. **[05-06 22:25]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
23. **[05-06 22:32]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
24. **[05-07 06:50]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
25. **[05-07 10:10]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Roberto Sassu <roberto.sassu@huaweicloud.com>
26. **[05-07 07:28]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
27. **[05-07 13:41]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
28. **[05-07 10:00]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
29. **[05-07 21:03]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
30. **[05-07 17:36]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
31. **[05-08 10:06]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
32. **[05-08 08:55]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Mimi Zohar <zohar@linux.ibm.com>
33. **[05-08 14:41]** Re: [PATCH] ima: debugging late_initcall_sync measurements
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
34. **[05-08 19:03]** Re: [RFC PATCH v3 4/4] Revert "firmware: arm_ffa: Change initcall
 level of ffa_init() to rootfs_initcall"
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 2: [RFC PATCH 0/3] initalise ff-a after finalising pKVM

**📧 邮件数**: 22 | **👥 参与者**: 3 | **📅 开始时间**: Tue,  5 May 2026 10:54:06 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在完成 pKVM 初始化后初始化 FF-A 的补丁（RFC PATCH 0/3）。该补丁旨在解决当 pKVM 启用时，FF-A 驱动必须在 pKVM 完成初始化后才能正常工作的问题。当前的实现中，pKVM 初始化在 device_initcall_sync 完成，而 FF-A 初始化则在 device_initcall 级别进行，这可能导致 FF-A 调用失败。

在历史讨论中，参与者强调了 pKVM 和 FF-A 之间的依赖关系，指出如果 FF-A 驱动在 pKVM 完成之前初始化，将无法进行版本协商，进而导致功能失效。因此，补丁提出了引入一个名为 ffa_root_dev 的根设备，以确保 FF-A 基础设施的初始化被推迟到 pKVM 完成后。

本周的新讨论中，参与者对补丁进行了细化和反馈。Yeoreum Yun 提出了将 load_uefi_certs() 函数的调用推迟到 late_initcall_sync 级别的建议，以解决在 FF-A 驱动未初始化时 EFI 变量服务失败的问题。此外，Sudeep Holla 提出了将 FF-A 核心作为平台驱动的建议，以简化设备的管理和初始化流程。最终，讨论达成了一致，Yeoreum Yun 将根据反馈进行补丁的修改和重发。

#### 📝 邮件列表

1. **[05-05 10:54]** [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
2. **[05-05 10:54]** [RFC PATCH 1/3] arm64: KVM: defer kvm_init() to finalise_pkvm() when pKVM is enabled
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
3. **[05-05 10:54]** [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
4. **[05-05 10:54]** [RFC PATCH 3/3] security: integrity: call load_uefi_certs() at late_initcall_sync
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
5. **[05-05 11:45]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Ben Horgan <ben.horgan@arm.com>
6. **[05-05 11:51]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
7. **[05-05 12:16]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
8. **[05-05 12:24]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Ben Horgan <ben.horgan@arm.com>
9. **[05-05 12:33]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
10. **[05-05 15:39]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
11. **[05-05 16:06]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
12. **[05-05 17:32]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
13. **[05-05 17:58]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
14. **[05-06 08:27]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
15. **[05-06 08:46]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
16. **[05-06 08:49]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
17. **[05-06 08:50]** Re: [RFC PATCH 1/3] arm64: KVM: defer kvm_init() to finalise_pkvm()
 when pKVM is enabled
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
18. **[05-06 09:14]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
19. **[05-06 09:58]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
20. **[05-06 10:11]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Yeoreum Yun <yeoreum.yun@arm.com>
21. **[05-06 10:58]** Re: [RFC PATCH 2/3] firmware: arm_ffa: initialise ff-a after
 finalising pKVM initialisation
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>
22. **[05-08 18:59]** Re: [RFC PATCH 0/3] initalise ff-a after finalising pKVM
   - 发件人: Sudeep Holla <sudeep.holla@kernel.org>

---

### Thread 3: [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes with documentation

**📧 邮件数**: 5 | **👥 参与者**: 2 | **📅 开始时间**: Wed,  6 May 2026 11:50:53 +0100

#### 🤖 AI 总结

本邮件讨论的主题是对 KVM_EXIT_MEMORY_FAULT 错误代码的对齐，以符合文档说明。Alexandru Elisei 提出了一个 RFC PATCH，旨在确保 KVM_EXIT_MEMORY_FAULT 在返回错误时，能够正确地将错误代码传递给用户空间。根据文档，KVM_EXIT_MEMORY_FAULT 的返回代码应为 -1，且 errno 应为 EFAULT 或 EHWPOISON，用户空间应假设其他错误代码的 kvm_run.exit_reason 是过时或未定义的。

在历史讨论中，Alexandru 详细描述了在处理内存故障时，如何通过 kvm_gmem_get_pfn() 函数将错误代码传递到用户空间，并指出当前实现可能导致用户空间无法正确检测到内存故障。Sean Christopherson 对此进行了回应，强调了 KVM 设计的初衷，并表示在特定情况下，KVM 可以“推测性”地设置 exit_reason。

本周的新讨论中，Alexandru 和 Sean 继续探讨了如何在不破坏用户空间的情况下，优化错误代码的传递。Alexandru 提出了避免在用户空间不应使用的情况下填充 KVM_EXIT_MEMORY_FAULT 信息的建议，以减少混淆。双方一致认为，尽量减少暴露给用户空间的信息是一个良好的防御策略。

总的来说，本周的讨论集中在如何确保 KVM 的错误处理与文档一致，并在实现中减少潜在的用户空间破坏风险。

#### 📝 邮件列表

1. **[05-06 11:50]** [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes with documentation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
2. **[05-06 05:44]** Re: [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes
 with documentation
   - 发件人: Sean Christopherson <seanjc@google.com>
3. **[05-07 09:45]** Re: [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes
 with documentation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>
4. **[05-07 06:33]** Re: [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes
 with documentation
   - 发件人: Sean Christopherson <seanjc@google.com>
5. **[05-08 09:55]** Re: [RFC PATCH] KVM: arm64: Align KVM_EXIT_MEMORY_FAULT error codes
 with documentation
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

### Thread 4: [RFC PATCH v2 00/28] KVM: s390: Introduce arm64 KVM - using symlinks

**📧 邮件数**: 3 | **👥 参与者**: 2 | **📅 开始时间**: Tue, 28 Apr 2026 18:04:57 +0200

#### 🤖 AI 总结

本邮件线程讨论了关于 KVM（Kernel-based Virtual Machine）在 s390 架构下引入 arm64 支持的补丁系列，主要是通过使用符号链接来处理 arm 头文件，而非移动它们。补丁系列的主要内容包括为其他主机架构提供 arm64 的用户空间 API，以及在 MAINTAINERS 文件中添加 Steffen Eiden 作为 KVM/arm64 的审阅者，以便于保持 s390 和 arm64 架构之间的代码同步。

在历史讨论中，Steffen Eiden 提出了这个补丁系列，并强调了与原始系列的差异，主要是通过符号链接的方式来处理头文件。第二封邮件则进一步确认了 Steffen Eiden 的审阅者身份，以便于跨架构的代码审查。

在本周的新讨论中，Marc Zyngier 对 Steffen Eiden 的审阅者补丁进行了确认，表示已将其应用于修复中，并对此表示感谢。这表明该补丁得到了认可，并将有助于未来的代码维护和协作。

#### 📝 邮件列表

1. **[04-28 18:04]** [RFC PATCH v2 00/28] KVM: s390: Introduce arm64 KVM - using symlinks
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
2. **[04-28 18:05]** [RFC PATCH v2 15/28] MAINTAINERS: Add Steffen as reviewer for KVM/arm64
   - 发件人: Steffen Eiden <seiden@linux.ibm.com>
3. **[05-06 17:36]** Re: (subset) [RFC PATCH v2 15/28] MAINTAINERS: Add Steffen as reviewer for KVM/arm64
   - 发件人: Marc Zyngier <maz@kernel.org>

---

### Thread 5: [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Sun, 10 May 2026 23:11:43 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于 KVM（Kernel-based Virtual Machine）在 arm64 架构下的 VGIC（虚拟通用中断控制器）相关的一个补丁，旨在优化在虚拟机创建时对预初始化寄存器的访问。

**原始补丁内容**：
补丁提出在虚拟机创建过程中，用户空间需要设置一些预初始化的分发器寄存器（如 GICD_IIDR），但由于设计要求 vCPU0 必须在创建后才能访问这些寄存器，导致在创建 vCPU 之前无法直接设置 IIDR。当前的 `kvm_trylock_all_vcpus()` 函数可能会导致不必要的 -EBUSY 错误，迫使用户空间必须先创建 vCPU0 并进行同步，增加了复杂性。补丁建议在 VGIC 尚未初始化时跳过对 vCPU 的尝试锁定，从而简化这一过程。

**之前讨论要点**：
在历史讨论中并没有相关的背景信息提供，因此无法总结之前的讨论要点。

**本周新讨论进展**：
本周的讨论主要集中在补丁的具体实现上，David Woodhouse 提出了补丁的详细代码修改，并解释了为什么在 VGIC 未初始化时不需要对 vCPU 进行锁定。此外，他还提出了其他可能的解决方案，例如在创建 vCPU 之前设置 IIDR 的新设备级属性，或者考虑废弃 `kvm_trylock_all_vcpus()` 函数。整体来看，本周的讨论进一步明确了补丁的必要性和实现细节。

#### 📝 邮件列表

1. **[05-10 23:11]** [RFC PATCH] KVM: arm64: vgic: Skip vCPU trylock for pre-init
 register access
   - 发件人: David Woodhouse <dwmw2@infradead.org>

---

## 📌 GIT PULL

共 1 个 thread

---

### Thread 1: [GIT PULL] KVM/arm64 fixes for 7.1, take #2

**📧 邮件数**: 1 | **👥 参与者**: 1 | **📅 开始时间**: Thu,  7 May 2026 16:42:21 +0100

#### 🤖 AI 总结

本周的邮件讨论主要围绕 KVM/arm64 在 7.1 版本中的修复补丁。Marc Zyngier 提交了第二组修复，内容包括针对 ARM 错误的解决方案和一系列小的 bug 修复。具体来说，这些修复涉及到 MMU 的权限故障处理、52 位虚拟地址的支持以及一些 AI 增强的修复。

在历史讨论中，虽然没有具体的邮件记录，但可以推测出之前的讨论可能集中在 KVM/arm64 的稳定性和功能改进上。此次补丁中提到的 ARM 错误处理（erratum 4193714）需要依赖固件的配合，表明该问题的复杂性和对系统稳定性的潜在影响。

本周的新进展包括修复了多个关键问题，如在运行 NV 模式下正确处理 52 位虚拟地址、确保 EL2 配置的正确性、以及修复了与 guest_memfd 相关的权限故障。此外，Steffen Eiden 被任命为 KVM/arm64 的审阅者，以支持未来 s390 和 arm64 的整合。这些修复和改进将有助于提升 KVM/arm64 的整体性能和可靠性。

#### 📝 邮件列表

1. **[05-07 16:42]** [GIT PULL] KVM/arm64 fixes for 7.1, take #2
   - 发件人: Marc Zyngier <maz@kernel.org>

---

## 📌 Discussion

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: add wfx test case

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Fri, 01 May 2026 15:21:19 +0100

#### 🤖 AI 总结

本邮件讨论主题为在 kvm-unit-tests 中为 ARM 架构添加 WFX 测试用例。历史讨论中，Alexandru Elisei 提到他正在使用 kvm-unit-test 来验证 QEMU 对指令的 TCG 模拟，特别是针对 WFxT 指令的建模。尽管他对当前的建模方式（将其视为 NOP）感到放心，但他希望确保不同模式的行为符合预期。

在本周的新讨论中，Alex Bennée 提出建议，要求在定时器中断处理程序中确认中断的处理，以符合软件的实际操作，并提供了相关代码示例（arm/timer.c::irq_handler()）供参考。这表明讨论的重点在于确保测试用例的准确性和完整性，以便更好地模拟和验证 ARM 架构的行为。整体来看，讨论围绕如何改进 WFX 测试用例的实现和验证展开。

#### 📝 邮件列表

1. **[05-01 15:21]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: =?utf-8?Q?Alex_Benn=C3=A9e?= <alex.bennee@linaro.org>
2. **[05-06 10:00]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

## 📌 Other

共 1 个 thread

---

### Thread 1: [kvm-unit-tests PATCH] arm: add wfx test case

**📧 邮件数**: 2 | **👥 参与者**: 2 | **📅 开始时间**: Mon, 27 Apr 2026 14:00:45 +0100

#### 🤖 AI 总结

本邮件讨论的主题是关于在 KVM 单元测试中为 ARM 架构添加 WFX 测试用例的补丁。该补丁由 Alex Bennée 提出，旨在利用 kvm-unit-tests 提供的额外功能，处理 GIC 和中断，类似于他为 QEMU 的 TCG 测试编写的测试用例。

在历史讨论中，Alex 提到了一种常见的中断处理方式，即在 GIC 层面确认中断。他举了一个例子，说明如果在处理中断后不正确地使用 WFI（等待中断），可能会导致 CPU 永远等待一个不会到来的中断。Alex 进一步阐述了在裸机环境下的正确做法，即在启用中断之前禁用本地中断，先设置定时器，然后再调用 WFI，以确保中断能够正确触发。

本周的新讨论没有新的进展或回复，邮件线程保持静默，未见进一步的反馈或修改建议。整体来看，该补丁的提出和讨论为 ARM 架构的 KVM 测试提供了重要的补充，但目前尚未有新的讨论动态。

#### 📝 邮件列表

1. **[04-27 14:00]** [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: =?UTF-8?q?Alex=20Benn=C3=A9e?= <alex.bennee@linaro.org>
2. **[05-01 14:15]** Re: [kvm-unit-tests PATCH] arm: add wfx test case
   - 发件人: Alexandru Elisei <alexandru.elisei@arm.com>

---

