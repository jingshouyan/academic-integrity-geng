# 耿同学·学术论文造假分析Skill

> 「孩子，爹今天要教你什么叫学术打假。」

**academic-integrity-geng** 是一个面向 [Reasonix](https://reasonix.ai) 的 **subagent skill**，以「耿同学」——学术圈最严厉的父亲——的人设，从 5 大维度系统扫描学术论文，识别数据造假、图片操纵、方法学缺陷、引用不当及期刊信誉等问题。

## 快速安装

```bash
# 方案一：自动安装
reasonix skill install jingshouyan/academic-integrity-geng

# 方案二：手动安装
git clone git@github.com:jingshouyan/academic-integrity-geng.git
# 将 .reasonix/skills/academic-integrity-geng/ 复制到你的项目 .reasonix/skills/ 下
```

## 使用方法

```bash
# 在当前会话中
/run academic-integrity-geng 分析这篇论文的摘要：...

# 或通过 Tool Call
run_skill({
  name: "academic-integrity-geng",
  arguments: "请分析以下论文：\n\n{论文标题}\n{论文内容/链接/DOI}"
})
```

## 五维检测体系

| 维度 | 核心检查项 | 图标 |
|------|------------|------|
| 数据与结果 | 数字自洽、p值分布、样本量、Benford法则、基线特征、伦理审查 | 🔬 |
| 图片与图表 | WB条带复用/拼接、流式图、显微镜图、坐标轴操纵、误差棒 | 🎨 |
| 方法论Rigor | 实验设计、Power Analysis、多重比较校正、抗体/细胞系 | 🧪 |
| 结构与引用 | 过度自引、引文填充、撤稿引用、DOI可检索、语言包装 | 📚 |
| 作者与期刊 | 期刊预警、Scope匹配、邮箱域名、投稿周期、评审操纵 | 🏛️ |

## License

Apache License 2.0
