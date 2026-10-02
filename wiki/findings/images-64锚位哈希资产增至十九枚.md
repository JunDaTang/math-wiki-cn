---
type: finding
title: images-64 锚位哈希资产增至十九枚
created: 2026-10-02
updated: 2026-10-02
tags: [数学手册, 图像资产, 资产计数]
related: [10-数学手册原书第10版--6-images--64-0f05d072a8a8ec918e5a99521ddc4ab9fbbafcae1621209ef683f7cc524e0d5e--hv9y04, images-64锚位哈希资产增至十八枚, 插图资产哈希入库法, hv9y04图像归属何章何节之辨]
sources: ["数学手册(原书第10版)/images/0f05d072a8a8ec918e5a99521ddc4ab9fbbafcae1621209ef683f7cc524e0d5e.jpg"]
source: "10-数学手册原书第10版--6-images--64-0f05d072a8a8ec918e5a99521ddc4ab9fbbafcae1621209ef683f7cc524e0d5e--hv9y04"
confidence: high
replicated: null
---
# images-64 锚位哈希资产增至十九枚

## 发现

images-64 锚位哈希资产计数由十八枚增至十九枚：本次入库的 hv9y04（`0f05d072a8a8ec918e5a99521ddc4ab9fbbafcae1621209ef683f7cc524e0d5e`，7.0 KB）为新增锚位资产，其哈希前缀 `0f05d072` 未见于既有索引（既有资产前缀覆盖 `00`–`0e` 段），按哈希序排于全部已入库资产之后。前一计数见 [[findings/images-64锚位哈希资产增至十八枚]]。

## 证据与置信

- 直接证据：文件名哈希、大小（7.0 KB）、目录路径（images 目录序号 64）均可在语料中直接核验，属 [[methodology/插图资产哈希入库法]] 的标准登记项。
- 本发现为账目性结论（资产清点），不涉及实验复现；计数可由索引枚举独立复核。
- 结论仅针对 `0f05d072…0d5e` 这一具体资产，不外推 images-64 目录其他资产的内容或归属。

## 后续

- hv9y04 内容与归属未鉴定，开放查询见 [[queries/hv9y04图像归属何章何节之辨]]。
- 全目录未鉴定资产总问题见 [[queries/images目录图像未鉴定之辨]]。