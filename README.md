# 🚀 Open NPU Hub (一站式开源 NPU 知识与实践库)

> 一站式、面向实战的 NPU（神经处理单元）知识与工程实践资源库。涵盖微架构演进、硬件算力横向对比、官方文档索引、BKC/BKM 部署与性能调优指南。

---

## ⚖️ [公开资料与合规声明 (Public Information Disclaimer)](docs/disclaimer.md)
---

## 🎯 首发聚焦：Intel NPU 平台矩阵

**Intel NPU**（Core Ultra 系列）从驱动到底层算子的完整工程链路：

| 平台代号 | 典型代表 | NPU 代际 | 架构与微结构亮点 | 公开算力 (TOPS) | 核心驱动与软件栈 |
|---|---|---|---|---|---|
| Meteor Lake (MTL) | Core Ultra 100 系列 | NPU 3720 | 2x NCE, 专用 Scratchpad SRAM, 独立 DMA 引擎 | ~10 - 11.5 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| Arrow Lake (ARL) | Core Ultra 200S / 200H 系列 | NPU 3720 变体 | 桌面级与性能移动端优化，沿用成熟 NPU 3 架构 | ~13 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| Lunar Lake (LNL) | Core Ultra 200V 系列 | NPU 4000 | 扩展计算阵列 (6x NCE)，集成更大本地带宽与增强型向量单元 | 40 - 48 TOPS (INT8) | `linux-npu-driver`, OpenVINO |
| Panther Lake (PTL) | Core Ultra 300 系列 | NPU 5000 | 全新 NPU 5 架构，算子吞吐进一步翻倍，强化端侧 Generative AI / Transformer 硬件加速 | ~50+ TOPS (INT8) | Linux NPU Driver /  OpenVINO |
---

## 💡 核心知识模块速览


---

## 🤝 贡献与交流

欢迎提交各 NPU 平台的部署经验与实测案例！
- 发现新驱动或公开技术参数？请提交 [Spec Update Issue](../../issues)。
- 拥有经过验证的优化手法或踩坑记录？请按 [BKM Template](.github/ISSUE_TEMPLATE/bkm_submission.md) 提交 PR。
