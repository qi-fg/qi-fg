<div align="center">

<img src="assets/banner.svg" width="100%" alt="Li Yongqi · AI Researcher"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&duration=3200&pause=900&color=0E7490&center=true&vCenter=true&width=720&lines=Medical+Image+Analysis+%7C+Brain+Signal+Decoding;Remote+Sensing+%7C+Weakly-Supervised+Segmentation;Building+Agents+that+See%2C+Reason+and+Segment)](https://github.com/qi-fg)

<br/>

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.8-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-12.x-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Arch%20%7C%20Ubuntu-FCC624?style=flat-square&logo=linux&logoColor=black)
![China](https://img.shields.io/badge/Zhengzhou%2C%20China-河南工业大学-red?style=flat-square&logo=mapbox&logoColor=white)
![Open to Work](https://img.shields.io/badge/Open%20to-2027%20Algorithm%20Roles-2EA44F?style=flat-square)

</div>

---

## 👋 About Me

我是 **李永琪（Li Yongqi）**，河南工业大学人工智能方向在读硕士（研二），主要做 **医学图像分析、脑电信号解码与遥感视觉分割** 的交叉研究。我的工作主线是：把 **基础模型（SAM / Mamba / VLM）** 与 **任务先验** 结合起来，在数据稀缺、标注昂贵的真实场景里做出可落地的模型。

- 🔭 目前在做 **MedSAM-Agent** —— 用 LoRA SFT + GRPO 强化学习让分割模型具备「交互式推理」能力
- 🧠 关注 **Stroke Lesion Segmentation**（ISLES 2022，CT + MRI 多模态融合）与 **EEG 情感识别**（Mamba-FHPM，SEED / SEED-IV 上 **96.11%**）
- 🛰 也在推进 **HySAM**：在 ReSAM 上引入 HUD 双曲不确定解耦模块，做点监督遥感分割
- ✈️ 参与国家级项目「低空空域容量动态评估与智能流量协同调控关键技术研究及示范应用」，负责 **低空智能管控系统** 研制
- 📈 副业在折腾一个基金管理微信小程序 —— 「基智管家」，OCR 拍照识别持仓 + 收益看板

---

## 🔬 Research Interests

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>🏥 Medical Image Analysis</h3>
      <p>细粒度医学分割、多模态融合（CT / MRI）、标注高效学习。基于 SAM ViT-B 做 LoRA 微调与强化学习后训练，解决病灶边界模糊、样本极度不平衡的问题。</p>
      <p><code>SAM</code> <code>LoRA</code> <code>GRPO</code> <code>MONAI</code></p>
    </td>
    <td width="33%" valign="top">
      <h3>🧠 Brain Signal Decoding</h3>
      <p>EEG 情感识别与表征学习。以 Mamba / 状态空间模型为骨干，结合层级特征金字塔，在跨被试、跨会话设定下提升泛化。</p>
      <p><code>Mamba</code> <code>SSM</code> <code>SEED-IV</code> <code>Representation</code></p>
    </td>
    <td width="33%" valign="top">
      <h3>🛰 Remote Sensing Vision</h3>
      <p>点监督 / 弱监督遥感目标分割。在双曲空间做不确定性解耦，抑制点标注带来的歧义，面向 SAR 舰船、建筑物等场景。</p>
      <p><code>Point-supervised</code> <code>Hyperbolic</code> <code>SAR</code> <code>Segmentation</code></p>
    </td>
  </tr>
</table>

---

## 📚 Publications

> 二作身份参与，研究方向集中在医学 AI 与视觉基础模型。

| Year | Venue | Title | Role | Status |
| :--- | :---- | :---- | :--- | :----- |
| 2026 | **Information Sciences** (SCI Q1) | [填写论文标题] | 二作 | ✅ Published |
| 2026 | **Engineering Applications of Artificial Intelligence** | [填写论文标题] | 二作 | 🕐 Under Review |
| 2026 | **IEEE TGRS** | [填写论文标题] | 二作 | 🕐 Under Review |

**专利**：已受理发明专利 **2 项**（第一/主要发明人之一，具体名称待补充）

---

## 🚀 Selected Projects

<details open>
<summary><b>🧑‍⚕️ MedSAM-Agent</b> — 会「思考」的医学分割智能体</summary>

<br/>

以 **SAM ViT-B** 为骨干，先做指令微调（LoRA SFT），再用 **GRPO**（verl 框架）做强化学习后训练，让模型在交互式提示下逐步收敛到精确病灶区域。已完成 SFT 阶段（5 epochs，loss 0.018）。

- 技术要点：LoRA 低秩微调 · chat-template 注入 · `verl.trainer.main_ppo` 训练入口 · vLLM rollout
- 工程经验：H200 上 `gpu_memory_utilization=0.3` 是避免 OOM 的关键配置
</details>

<details>
<summary><b>🧠 Mamba-FHPM</b> — 层级特征金字塔 Mamba 情感识别</summary>

<br/>

面向 SEED / SEED-IV 的 EEG 情感识别框架，用状态空间模型捕获长程时序依赖，配合层级特征金字塔融合多尺度表征，准确率 **96.11%**（当前 SOTA 水平）。
</details>

<details>
<summary><b>🛰 HySAM</b> — 双曲不确定解耦的点监督遥感分割</summary>

<br/>

在 **ReSAM** 基础上加入 **HUD（Hyperbolic Uncertainty Disentanglement）** 模块，用双曲几何刻画点标注的语义歧义，在 NWPU VHR-10、HRSID-inshore、WHU 上做系统性对照实验，横向对比 PointSAM。
</details>

<details>
<summary><b>✈️ 低空智能管控系统</b> — 空域容量评估与流量协同调控</summary>

<br/>

国家级示范应用项目子课题。负责低空智能管控系统研制，覆盖空域容量动态评估、航路冲突检测与流量协同调度。
</details>

<details>
<summary><b>📱 基智管家</b> — 基金持仓管理小程序</summary>

<br/>

微信小程序（WXML + Vant + ECharts + 云开发）。支持百度 OCR 拍照识别持仓、天天基金行情接入、收益看板与基金对比。独立完成功能开发与两轮回归测试。
</details>

---

## 🛠 Tech Stack

<table>
  <tr><td width="110"><b>Languages</b></td><td><code>Python</code> <code>C/C++</code> <code>JavaScript</code> <code>MATLAB</code> <code>SQL</code></td></tr>
  <tr><td><b>Deep Learning</b></td><td><code>PyTorch</code> <code>MONAI</code> <code>Transformers</code> <code>PEFT / LoRA</code> <code>timm</code></td></tr>
  <tr><td><b>Foundation Models</b></td><td><code>SAM / SAM2</code> <code>Qwen-VL</code> <code>Mamba / SSM</code> <code>CLIP</code></td></tr>
  <tr><td><b>RL &amp; LLM</b></td><td><code>verl</code> <code>GRPO</code> <code>vLLM</code> <code>TRL</code> <code>DeepSpeed</code></td></tr>
  <tr><td><b>Engineering</b></td><td><code>Linux</code> <code>Docker</code> <code>Git</code> <code>Slurm / K8s</code> <code>WandB</code> <code>OpenCV</code></td></tr>
  <tr><td><b>Data</b></td><td><code>ISLES 2022</code> <code>SEED / SEED-IV</code> <code>NWPU VHR-10</code> <code>HRSID</code> <code>WHU</code></td></tr>
</table>

---

## 📊 GitHub Stats

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=qi-fg&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&rank_icon=percentile" alt="GitHub Stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=qi-fg&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages"/>
</div>

### 🐍 Contribution Snake

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/qi-fg/qi-fg/output/github-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/qi-fg/qi-fg/output/github-snake.svg"/>
    <img src="https://raw.githubusercontent.com/qi-fg/qi-fg/output/github-snake.svg" alt="Contribution Snake"/>
  </picture>
</div>

---

## 🏆 Honors & Extras

- 📄 已发表 SCI Q1 论文 1 篇 · 在投 2 篇（EAAI / TGRS，均二作）· 已受理发明专利 2 项
- 🎖 省级奖学金 · 三好学生 · 文明学生
- 🗣 CET-4 · 普通话二级甲等
- 💻 日常在 RTX 5090 / H200 上做实验，熟悉多机多卡与集群排队环境

---

## 📫 Get in Touch

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-%40qi--fg-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/qi-fg)
[![Issues](https://img.shields.io/badge/Discussions-Ask%20me%20anything-2EA44F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/qi-fg/qi-fg/discussions)
[![Email](https://img.shields.io/badge/Email-Me-1a73e8?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL)

<br/><br/>

<sub>📮 最方便的联系方式是邮件或 GitHub Discussions，看到就回。</sub>

</div>

<br/>

<div align="center">
  <sub>⭐ 如果你也在做医学图像 / 遥感分割 / 脑电解码，欢迎来找我聊，一起做点有意思的东西。</sub>
</div>

<!--
===========================================================
  发布前需要替换的占位符（全局搜索替换即可）：
  1. qi-fg  -> 你的 GitHub 用户名（共 6 处：typing svg 链接、stats、top-langs、snake 三处）
  2. YOUR_EMAIL     -> 你的邮箱（mailto 链接，不填就删掉这一行徽章）
  4. [填写论文标题]  -> 三篇论文的完整标题
  5. 专利名称        -> 2 项已受理发明专利的名称
  6. 「低空智能管控系统」若不希望公开项目细节，可删除该 details 块
===========================================================
-->
