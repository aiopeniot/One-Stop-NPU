# 🚀 Open NPU Hub (一站式开源 NPU 知识与实践库)

> 一站式、面向实战的 NPU（神经处理单元）知识与工程实践资源库。涵盖微架构演进、硬件算力横向对比、官方文档索引、BKC/BKM 部署与性能调优指南。

---

## ⚖️ 公开资料与合规声明 (Public Information Disclaimer)

1. **严格公开来源**：本项目中所有架构说明、硬件规格、驱动源码解析、性能数据与技术指南，完全来源于厂商官方公开文档及开发者公开发布内容。
2. **非保密 (Non-NDA)**：本项目严禁且绝不包含任何受 NDA（保密协议）限制的未公开规格、专有数据或敏感内部工程物料。
3. **社区中立**：本项目为独立开源社区倡议，所引用的商标与官方链接归各自厂商所有。

详细公开信息来源清单请参阅 [公开资料声明与来源归档](docs/disclaimer.md)。

---

## 🎯 首发聚焦：Intel NPU 平台矩阵

**Intel NPU**（Core Ultra 系列）从驱动到底层算子的完整工程链路：

| 平台代号 | 典型代表 / 产品系列 | NPU 代际 | 架构与微结构亮点 | 公开算力 (TOPS) | 核心驱动与软件栈 |
|---|---|---|---|---|---|
| **Meteor Lake (MTL)** | Core Ultra 100 系列 | **NPU 3720** | 2x NCE, 专用 Scratchpad SRAM, 独立 DMA 引擎 | ~10 - 11.5 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| **Arrow Lake (ARL)** | Core Ultra 200S / 200H 系列 | **NPU 3720 变体** | 桌面级与性能移动端优化，沿用成熟 NPU 3 架构 | ~13 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| **Lunar Lake (LNL)** | Core Ultra 200V 系列 | **NPU 4000** | 扩展计算阵列 (6x NCE)，集成更大本地带宽与增强型向量单元 | 40 - 48 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| **Panther Lake (PTL)** | Core Ultra 300 系列 | **NPU 5000 (NPU 5)** | 全新 NPU 5 架构，算子吞吐进一步翻倍，强化端侧 Generative AI / Transformer 硬件加速 | ~50+ TOPS (INT8) | Linux NPU Driver /  OpenVINO |
---

## 💡 核心知识模块速览

- 📦 [硬件规格对比 (Specs Matrix)](docs/specifications/compare-matrix.md)：各大平台 TOPS、位宽支持与功耗速查。
- 🏆 [BKC 黄金环境配置 (Best Known Configurations)](docs/deployment-bkc/intel-bkc-matrix.md)：验证通过的 OS、内核版本、固件与 SDK 组合。
- 🛠️ [BKM 调优最佳实践 (Best Known Methods)](docs/optimization-bkm/)：量化选型、内存零拷贝、算子回退排查。
- 📊 [调试与性能度量 (Profiling & Tools)](docs/profiling-tools/)：驱动监控、指标解读与瓶颈诊断（含 `nputop`、sysfs 剖析）。
- 💡 [端侧端到端实操 (Case Studies)](docs/case-studies/)：轻量化大语言模型、端侧视觉模型真机推理。

---

## 🤝 贡献与交流

欢迎提交各 NPU 平台的部署经验与实测案例！
- 发现新驱动或公开技术参数？请提交 [Spec Update Issue](../../issues)。
- 拥有经过验证的优化手法或踩坑记录？请按 [BKM Template](.github/ISSUE_TEMPLATE/bkm_submission.md) 提交 PR。
