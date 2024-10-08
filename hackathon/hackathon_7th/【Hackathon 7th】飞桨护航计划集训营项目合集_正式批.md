此文档展示 **PaddlePaddle Hackathon 第七期活动——飞桨护航计划集训营（正式批）** 项目的详细介绍

## 赛题详情

### 项目一：框架 API 易用性提升

#### 项目介绍：

飞桨框架 API 中 **功能缺失、功能 Bug** 等地方，都将成为代码转换的堵点问题，为了扫清**框架 API 转换**的堵点问题，**降低模型迁移的成本**，需要对框架 API 的易用性进行提升。具体 API 升级任务包括：问题描述 + 修改方案，其中 **问题描述** 会给出该 API 存在的不合理问题，**修改方案** 会给出该 API 的建议修改思路（例如 功能增强、Bug 修复、实现优化等），你需要参考**修改方案** ，完成该 API 的升级工作。

除了对框架 API 本身的修改外，还需要完成 [PaConvert](https://github.com/PaddlePaddle/PaConvert)、[映射文档](https://github.com/PaddlePaddle/docs/blob/develop/docs/guides/model_convert/convert_from_pytorch/api_difference/pytorch_api_mapping_format_cn.md) 的对齐。因此你需要额外熟悉 [PaConvert](https://github.com/PaddlePaddle/PaConvert) 仓库，保证 API 转换对应的单测可以成功运行。一个 API 升级任务总计包括如下内容：（注意逐个核对是否完成）

1. **API 本身修改**：代码提交至 [Paddle 仓库](https://github.com/PaddlePaddle/Paddle)
2. **API 英文、中文文档修改**：代码提交至 [Paddle 仓库](https://github.com/PaddlePaddle/Paddle) 和 [docs 仓库](https://github.com/PaddlePaddle/docs)
3. **API 映射文档修改**：代码提交至 [映射文档目录](https://github.com/PaddlePaddle/docs/tree/develop/docs/guides/model_convert/convert_from_pytorch/api_difference/)
4. **PaConvert 转换规则修改**：代码提交至 [PaConvert 仓库](https://github.com/PaddlePaddle/PaConvert)
5. **PaConvert 单测修改**：代码提交至 [PaConvert 单侧目录](https://github.com/PaddlePaddle/PaConvert/tree/master/tests)

具体待升级的 API 任务名单，以内部实际发布为准，在结营时要求完成 10~20 个 API 升级任务。

#### 营员要求（1 人）：

- 熟悉 Python
- 熟悉 C++、CUDA
- 熟悉飞桨 API 算子开发，有 API 开发经验者优先
- 熟悉 Pytorch 框架的使用，有论文复现与模型迁移经验优先

### 项目二：模型迁移工具建设

#### 项目介绍：

为了实现高效的将 PyTorch 代码自动化的转写成 Paddle 代码，从而提升模型迁移的效率，我们建设了[**PaConvert 代码自动转换工具**](https://github.com/PaddlePaddle/PaConvert): **Pa**ddlePaddle Code **Convert** Toolkits。目前虽然已支持约 1300 个 Pytorch API 的自动转换与 90%的代码转换率，但在 单测规范化建设、文档规范化建设、机制建设 等方面仍然存在着很多的问题，仍有很多可以继续完善的地方。

本课题的工作任务包括转换工具建设的以下内容：

1. 单测规范化建设（总约 200 个） + 框架 API 问题的记录
2. API 易用性升级对应的转换工具升级
3. 新增 API 转换策略（约 200 个）
4. 文档规范化建设
5. 转换机制开发
6. 辅助函数策略开发

#### 营员要求（1 人）：

- 熟悉 Python
- 熟悉 Pytorch 框架的使用，有论文复现与模型迁移经验优先

### 项目三：PaddleMIX 套件能力建设

#### 项目介绍：

飞桨开源跨模态大模型套件，聚合图像、文本、视频等多种模态，覆盖视觉语言预训练，文生图，文生视频等丰富的跨模态任务。旨在提供开箱即用的开发体验，同时满足开发者灵活定制需求，探索通用人工智能。

目前我们已经完成了模型的训练、推理、应用等基础能力建设，但跨模态领域发展迅速，从数据流、模型、训练、推理等都要不断地跟进与丰富。本次护航计划参与的工作主要分为三个部分：

1. 前沿模型复现
2. 参与基础能力建设，包括 PPDiffusers 的 models、pipeline、训练等全流程能力建设与丰富
3. 进阶：推理、训练性能优化

#### 营员要求（1 人）：

- 熟悉 python
- 对深度学习有一定了解
- 有深度学习框架应用和研发经验
- 有跨模态大模型相关经验（加分项）

### 项目四：PaddleNLP 套件能力建设

#### 项目介绍：

飞桨开源大语言模型套件，通过极致的全流程优化，为开发者提供从组网开发、预训练、精调对齐、模型压缩以及推理部署的一站式解决方案。

目前 PaddleNLP 已经完成了大模型开发中的预训练、精调对齐、模型压缩以及推理部署的完整能力建设，但随着大语言模型的快速迭代更新，模型结构和 tokenizer 等基础工具需不断地迭代更新。本次护航计划参与的工作主要分为三个部分：

1. 前沿模型复现；
2. 基础能力建设，模型库接入 FastTokenizer，模型参数和结构自动转换功能等基础能力建设与丰富。
3. 进阶：模型并行策略优化。

#### 营员要求（1 人）：

- 熟悉 python
- 对深度学习有一定了解
- 有深度学习框架应用和研发经验
- 有大模型相关经验（加分项）

### 项目五：飞桨科学计算材料领域建设

#### 项目介绍：

当前生成式模型、图神经网络等模型发展迅速，越来越多的学者基于神经网络模型进行晶体材料的属性预测和结构生成。为了进一步增加飞桨在此领域上的支持能力，本次护航计划的工作主要包括：

1. 实现基于 VAE/Diffusion/GNN/Transformer 等前沿算法在晶体材料属性预测、结构生成等任务上的论文复现工作，参与材料领域案例建设、文档撰写、性能优化等；
2. 基础功能建设：包括套件接口丰富、接口设计、性能优化、科学计算领域数据集建设。最终目的是提升套件的易用能力，减少用户上手难度，吸引用户使用套件和 Paddle 框架进行科学计算项目开发。

#### 营员要求（1 人）：

- 熟悉 Python
- 对深度学习有一定了解
- 熟悉 Pytorch 框架的使用，有论文复现与模型迁移经验优先

### 项目六：组合机制算子专项和机制建设

#### 项目介绍：

深度学习框架算子数量多导致 **新硬件接入、高阶微分** 和 **编译器对接** 的成本增高和实现难度增大。而短期不可能大幅降低算子数量，所以可行思路是将算子分为基础算子和组合算子两类，并控制基础算子数量，其它算子均使用基础算子实现，使得 新硬件接入、高阶微分 和 编译器对接 只要在基础算子实现，即可实现预期功能。

目前组合机制的功能开发已经完成，并且在部分算子和模型上经过了初步验证。未来组合机制需要进一步拓展对动态 shape 的支持，并且选择一批算子集合进行组合机制的推全，本次护航计划参与的**工作主要包括**：

1. 组合算子拆解成基础算子；
2. PIR 中组合机制与其他模块的联调和问题解决；
3. 【进阶】动态 shape 的适配。

#### 营员要求（1 人）：

- 熟悉 python，C++
- 对深度学习有一定了解
- 有深度学习框架应用和研发经验

### 项目七：自动并行张量切分机制预研&建设

#### 项目介绍：

自动并行通过框架在计算图层编译的方式实现模型训练的并行化。当前业内主流自动并行实现过程中，对张量的切分有一些局限和问题：

1. 如何通用高效的支持张量在 mesh 上的不均切分
2. 如何支持张量的一个 axis 被 多个 mesh 的 dims 切分

这些问题限制了自动并行在更广泛业务中的应用，需要在框架层面提供一套方案来解决。目前业内对这两个问题在工程上并没有非常成熟的方案，需要调研学界(alpa、flexflow)、工业界(TF、Torch) 的技术路线，并结合 Paddle 框架实现，设计方案，完成工程实现。本次护航计划参与的**工作主要包括**：

1. 调研学界和工业界自动并行框架中对上述两个问题的解决方案，形成调研文档
2. 实现 Paddle 静态图 PIR 下 的《张量不均切分》功能
3. 【进阶】实现 Paddle 动静态图下 的《张量的一个 axis 被 多个 mesh 的 dims 切分》功能
4. 【进阶】将上述功能适配到具体业务问题

#### 营员要求（1 人）：

- 熟悉 python，C++
- 对深度学习、自动并行有一定了解
- 有深度学习框架应用和研发经验
- 了解 Collective 集合通信

### 项目八：自动并行在复杂模型结构下的能力摸底和技术储备

#### 项目介绍：

飞桨框架 3.x 版本推出了动静统一的半自动并行编程范式，开发者无需深入研究手动并行编程的复杂概念和 API，只需进行少量的张量切分标注，即可完成混合并行模型的构建，显著简化了编写分布式程序的复杂度。针对目前主流的 Transformer 网络结构，飞桨自动并行能力已充分验证。但业界模型结构和算法创新层出不穷，许多复杂的优化技术即使通过手动的方式也需要较高的专家经验才能进行分布式并行化，如何进行自动并行更是面临极大的技术挑战。本课题要求参与者学习飞桨自动并行相关技术，将基于手动并行实现的复杂模型结构改造成自动并行，借此摸底自动并行能力，梳理功能缺失点，开发补齐相关基础功能，在测试 demo 上跑通自动并行，并完成对应的自动并行功能完善和性能优化工作。

#### 营员要求（1 人）：

- 熟悉 python，C++
- 对深度学习、自动并行有一定了解
- 有深度学习框架应用和研发经验
- 了解 Collective 集合通信
