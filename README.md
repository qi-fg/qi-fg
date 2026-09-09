<div align="center">

<img src="assets/banner.svg" width="100%" alt="Li Yongqi · Remote Sensing & Agentic Vision"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&duration=3200&pause=900&color=0E7490&center=true&vCenter=true&width=720&lines=Hyperspectral+Classification+%7C+Remote+Sensing+Segmentation;Agentic+Vision+%7C+Interactive+Reasoning;Final-Year+M.Sc.+%40+HUT+%7C+Open+to+Algorithm+Roles)](https://github.com/qi-fg)

<br/>

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.8-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-12.x-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Arch+%7C+Ubuntu-FCC624?style=flat-square&logo=linux&logoColor=black)
![HUT](https://img.shields.io/badge/Henan+University+of+Technology-Zhengzhou-1a73e8?style=flat-square&logoColor=white)
![Open to Work](https://img.shields.io/badge/Open+to-2027+Algorithm+Roles-2EA44F?style=flat-square)

</div>

---

## 👋 About Me

I am **Li Yongqi**, a final-year M.Sc. candidate at **Henan University of Technology**, working on **remote sensing image understanding**. My research lives at the intersection of two concrete threads:

- 🛰️ **Hyperspectral image classification** — exploiting the joint spectral–spatial structure of high-dimensional remote sensing data for robust scene and material recognition under limited labels.
- 🌐 **Remote sensing image segmentation** — building point-supervised / weakly-supervised segmentation frameworks (e.g., hyperbolic-geometry–based uncertainty disentanglement) that learn from cheap annotations without sacrificing boundary precision.

Beyond that, I'm actively exploring **agentic vision** — building models that can perceive, self-prompt, and reason iteratively about visual inputs. My current focus is on interactive segmentation agents built on SAM-family backbones, post-trained with LoRA SFT + GRPO.

- 📄 1 SCI Q1 paper published · 2 under review (EAAI / TGRS) · 2 invention patents pending
- 💻 Day-to-day on RTX 5090 (32 GB) for fast iteration and H200 (143 GB) for large-scale runs

---

## 🔬 Research Interests

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>🛰️ Hyperspectral Classification</h3>
      <p>Exploit the joint spectral–spatial structure of high-dimensional remote sensing data for robust scene and material recognition. Focus on label-efficient regimes (semi-/self-/few-shot) and foundation-model adaptation to multi- and hyperspectral inputs.</p>
      <p><code>Spectral-Spatial</code> <code>Self-supervised</code> <code>Cross-scene</code> <code>Foundation Models</code></p>
    </td>
    <td width="33%" valign="top">
      <h3>🌐 Remote Sensing Segmentation</h3>
      <p>Point- and weakly-supervised segmentation for SAR, optical, and aerial imagery. Plug-in modules in hyperbolic space to disentangle aleatoric / epistemic uncertainty and tame label ambiguity, with systematic side-by-side comparison to PointSAM, ReSAM, and SAM2.</p>
      <p><code>Point-supervised</code> <code>Hyperbolic</code> <code>Uncertainty</code> <code>SAR</code></p>
    </td>
    <td width="33%" valign="top">
      <h3>🤖 Agentic Vision</h3>
      <p>Vision agents that perceive, self-prompt, and reason iteratively. Combine SAM-family backbones with LoRA SFT + GRPO post-training (verl framework) to enable interactive, prompt-driven segmentation that converges under few-shot user feedback.</p>
      <p><code>SAM</code> <code>LoRA</code> <code>GRPO</code> <code>verl</code> <code>vLLM</code></p>
    </td>
  </tr>
</table>

---

## 📚 Publications

> Research output centers on remote sensing vision and agentic foundation models.

| Year | Venue | Title | Role | Status |
| :--- | :---- | :---- | :--- | :----- |
| 2026 | **Information Sciences** (SCI Q1) | [填写论文标题] | 二作 | ✅ Published |
| 2026 | **Engineering Applications of Artificial Intelligence** | [填写论文标题] | 二作 | 🕐 Under Review |
| 2026 | **IEEE TGRS** | [填写论文标题] | 二作 | 🕐 Under Review |

**Patents**: 2 invention patents pending (primary co-inventor; titles TBD)

---

## 🚀 Selected Projects

<details open>
<summary><b>🤖 Agentic Segmentation Framework</b> — interactive vision agents via SFT + GRPO</summary>

<br/>

A vision agent that turns a frozen SAM backbone into an iterative, prompt-driven segmenter. Stage 1: instruction-tuning with LoRA SFT (5 epochs, loss 0.018). Stage 2: GRPO post-training via the `verl` framework to refine prompt strategy under few-shot user feedback.

- Stack: SAM ViT-B · LoRA · GRPO · `verl.trainer.main_ppo` · vLLM rollout
- Engineering: `gpu_memory_utilization=0.3` is critical on H200 to avoid OOM at long context

</details>

<details>
<summary><b>🛰️ HySAM</b> — hyperbolic uncertainty disentanglement for point-supervised segmentation</summary>

<br/>

A plug-in module on top of **ReSAM** that disentangles aleatoric / epistemic uncertainty in hyperbolic space, suppressing ambiguity inherent to point-level supervision. Systematic benchmarks on NWPU VHR-10, HRSID-inshore, and WHU, with side-by-side comparison to PointSAM.

</details>

<details>
<summary><b>🌈 Hyperspectral Benchmarks</b> — spectral–spatial pipelines on benchmark scenes</summary>

<br/>

Ongoing work on hyperspectral scene classification. Building spectral–spatial encoders with masked self-supervision to handle cross-sensor / cross-scene shifts. Detailed results will be updated once the manuscript is in preparation.

</details>

---

## 🛠 Tech Stack

<table>
  <tr><td width="110"><b>Languages</b></td><td><code>Python</code> <code>C/C++</code> <code>MATLAB</code> <code>SQL</code></td></tr>
  <tr><td><b>Deep Learning</b></td><td><code>PyTorch</code> <code>timm</code> <code>Transformers</code> <code>PEFT / LoRA</code> <code>MMSegmentation</code></td></tr>
  <tr><td><b>Foundation Models</b></td><td><code>SAM / SAM2</code> <code>Qwen-VL</code> <code>CLIP</code> <code>Mamba / SSM</code></td></tr>
  <tr><td><b>RL &amp; Agents</b></td><td><code>verl</code> <code>GRPO</code> <code>vLLM</code> <code>TRL</code> <code>DeepSpeed</code></td></tr>
  <tr><td><b>Geo / RS</b></td><td><code>GDAL / Rasterio</code> <code>GeoTIFF</code> <code>QGIS</code></td></tr>
  <tr><td><b>Engineering</b></td><td><code>Linux</code> <code>Docker</code> <code>Git</code> <code>Slurm / K8s</code> <code>WandB</code></td></tr>
  <tr><td><b>Data</b></td><td><code>NWPU VHR-10</code> <code>HRSID</code> <code>WHU</code> <code>Indian Pines</code> <code>Houston 2018</code></td></tr>
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

- 📄 1 SCI Q1 paper published · 2 under review (EAAI / TGRS) · 2 patents pending
- 🎖 Provincial scholarship · Three-good Student · Civilization Honor
- 🗣 CET-4 · Mandarin Level 2A
- 💻 Daily experiments on RTX 5090 (32 GB) + H200 (143 GB); comfortable with multi-GPU and cluster scheduling

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
  <sub>⭐ 如果你也在做 <b>遥感视觉 / Agentic Vision / SAM 后训练</b>，欢迎来找我聊，一起做点有意思的东西。</sub>
</div>

<!--
===========================================================
  发布前需要替换的占位符（全局搜索替换即可）：
  1. YOUR_EMAIL     -> 你的邮箱（mailto 链接，不填就删掉这一行徽章）
  2. [填写论文标题]  -> 三篇论文的完整标题
  3. 专利名称        -> 2 项已受理发明专利的名称
  4. 「Hyperspectral Benchmarks」项目当前为占位描述，待论文/代码准备就绪后替换
===========================================================
-->