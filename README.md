<!-- Banner slot: add a local image here when ready. -->
<!-- Optional future badges: repository stars, Issues, website, and survey paper. -->

<h1 align="center">Awesome Remote Sensing Image Generation</h1>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
</p>

<p align="center">Papers · Datasets · Benchmarks · Resources</p>

> **Sample / 示例阶段**：先从 `all_investigated_literature.xlsx` 中选取 8 篇论文展示填表效果。数据集、评测、图片及作者信息继续留空；分类仍可调整，不代表最终收录范围。条目来源及字段修订见 [Sample Sources](docs/sample-sources.md)。

<!-- Project introduction and survey scope go here. -->

Contributions are welcome. Use the [paper submission template](.github/ISSUE_TEMPLATE/new-paper.md) or [dataset submission template](.github/ISSUE_TEMPLATE/new-dataset.md). See [CONTRIBUTING.md](CONTRIBUTING.md) for maintenance and publishing notes.

<a id="inclusion-criteria"></a>
## Inclusion Criteria / 收录标准

- 收录与遥感图像生成相关、具有研究价值的期刊论文及领域认可的优质会议论文。
- 不收录一般低质量 EI 会议论文；EI 检索本身不作为收录依据，也不据此排除领域认可的优质会议。
- 允许收录相关 arXiv 预印本，并明确标注为 arXiv，不将其写成已正式发表的会议或期刊论文。

<a id="news"></a>
## 🥳 News

<!-- Add dated updates here, newest first. -->

- **2026-10-12**: Added 8 sample papers from the literature workbook, with paper links, available author repositories, and source-row references.

<a id="overview"></a>
## 🌍 Overview

<!-- Reserve this area for the survey taxonomy / summary figure / timeline. -->

_Overview figure and scope description to be added._

<a id="usage"></a>
## 🔎 Usage

<!-- After publishing, add repository-specific Issue links and label-count badges here. -->

_Issue navigation and statistics badges to be added after repository setup._

<a id="contents"></a>
## 📑 Summary of Contents

- [Inclusion Criteria / 收录标准](#inclusion-criteria)
- [News](#news)
- [Overview](#overview)
- [Usage](#usage)
- [Datasets](#datasets)
  - [Comprehensive Datasets](#comprehensive-datasets)
  - [Task-Specific Datasets](#task-specific-datasets)
- [Benchmarks and Evaluation](#benchmarks)
- [Papers](#papers)
  - [Text-to-Image Generation](#text-to-image)
  - [Layout- and Structure-Conditioned Generation](#layout-conditioned)
  - [Reference-Guided Generation and Editing](#reference-guided)
  - [Unconditional Generation and Data Synthesis](#data-synthesis)
  - [Cross-Modal Image Generation](#cross-modal)
  - [Restoration and Reconstruction](#restoration)
  - [Other Generation Tasks](#other-tasks)
- [Surveys](#surveys)
- [Awesome Lists and Resources](#resources)
- [Citation](#citation)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

<a id="datasets"></a>
## 📚 Datasets

<a id="comprehensive-datasets"></a>
### Comprehensive Datasets

| Year | Venue | Name | Task / Modality | Paper | Download | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |

<!-- Add dataset rows here. -->

<a id="task-specific-datasets"></a>
### Task-Specific Datasets

| Year | Venue | Name | Task / Modality | Paper | Download | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |

<!-- Add dataset rows here. -->

<a id="benchmarks"></a>
## 📊 Benchmarks and Evaluation

| Year | Venue | Name | Task | Metrics / Protocol | Paper | Code / Data |
| :---: | :---: | --- | --- | --- | :---: | :---: |

<!-- Add benchmark rows here. -->

<!-- Add an evaluation-metric summary here when ready. -->

<a id="papers"></a>
## 📄 Papers

<a id="text-to-image"></a>
### Text-to-Image Generation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | IEEE GRSM | Text-to-image; foundation model | Text2Earth: Unlocking Text-driven Remote Sensing Image Generation with a Global-Scale Dataset and a Foundation Model | [Paper](https://doi.org/10.1109/MGRS.2025.3560455) | [Code](https://github.com/Chen-Yang-Liu/Text2Earth) | [Source](docs/sample-sources.md#text2earth) |

<!-- Add paper rows here. -->

<a id="layout-conditioned"></a>
### Layout- and Structure-Conditioned Generation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | CVPR | Layout control; diffusion; object detection | AeroGen: Enhancing Remote Sensing Object Detection with Diffusion-Driven Data Generation | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Tang_AeroGen_Enhancing_Remote_Sensing_Object_Detection_with_Diffusion-Driven_Data_Generation_CVPR_2025_paper.html) | [Code](https://github.com/Sonettoo/AeroGen) | [Source](docs/sample-sources.md#aerogen) |
| 2024 | ICLR | Geospatial metadata; diffusion; foundation model | DiffusionSat: A Generative Foundation Model for Satellite Imagery | [Paper](https://arxiv.org/abs/2312.03606) | [Code](https://github.com/samar-khanna/DiffusionSat) | [Source](docs/sample-sources.md#diffusionsat) |

<!-- Add paper rows here. -->

<a id="reference-guided"></a>
### Reference-Guided Generation and Editing

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |

<!-- Add paper rows here. -->

<a id="data-synthesis"></a>
### Unconditional Generation and Data Synthesis

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2024 | arXiv | Change detection; semantic control; latent diffusion | ChangeAnywhere: Sample Generation for Remote Sensing Change Detection via Semantic Latent Diffusion Model | [Paper](https://arxiv.org/abs/2404.08892) | [Repository](https://github.com/tangkai-RS/ChangeAnywhere) | [Source](docs/sample-sources.md#changeanywhere) |

<!-- Add paper rows here. -->

<a id="cross-modal"></a>
### Cross-Modal Image Generation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | ICCV | Any-to-any generation; multimodal foundation model | TerraMind: Large-Scale Generative Multimodality for Earth Observation | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Jakubik_TerraMind_Large-Scale_Generative_Multimodality_for_Earth_Observation_ICCV_2025_paper.html) | [Code](https://github.com/IBM/terramind) | [Source](docs/sample-sources.md#terramind) |
| 2022 | IJCAI | SAR-to-optical; neural PDE | SAR-to-Optical Image Translation via Neural Partial Differential Equations | [Paper](https://www.ijcai.org/proceedings/2022/229) | — | [Source](docs/sample-sources.md#s2o-npde) |

<!-- Add paper rows here. -->

<a id="restoration"></a>
### Restoration and Reconstruction

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2024 | CVPR | Hyperspectral restoration; diffusion; low-rank prior | HIR-Diff: Unsupervised Hyperspectral Image Restoration Via Improved Diffusion Models | [Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Pang_HIR-Diff_Unsupervised_Hyperspectral_Image_Restoration_Via_Improved_Diffusion_Models_CVPR_2024_paper.html) | [Code](https://github.com/LiPang/HIRDiff) | [Source](docs/sample-sources.md#hir-diff) |

<!-- Add paper rows here. -->

<a id="other-tasks"></a>
### Other Generation Tasks

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2024 | IEEE TGRS | Hyperspectral synthesis; unmixing; diffusion | UnmixDiff: Unmixing-Based Diffusion Model for Hyperspectral Image Synthesis | [Paper](https://doi.org/10.1109/TGRS.2024.3425517) | [Code](https://github.com/yuyang95/UnmixingDM) | [Source](docs/sample-sources.md#unmixdiff) |

<!-- Add paper rows here. -->

<a id="surveys"></a>
## 📝 Surveys

| Year | Venue | Keywords | Name | Paper | Resources |
| :---: | :---: | --- | --- | :---: | :---: |

<!-- Add survey rows here. -->

<a id="resources"></a>
## 🔗 Awesome Lists and Resources

<!-- Add relevant repositories, tools, and resource links here. -->

_To be added._

<a id="citation"></a>
## 📖 Citation

<!-- Add the actual survey / repository citation when its metadata is available. -->

_Citation information to be added._

<a id="contact"></a>
## 📬 Contact

<!-- Add maintainer names, affiliations, and contact details here. -->

_Maintainer information to be added._

<a id="acknowledgements"></a>
## 🙏 Acknowledgements

Repository organization and maintenance workflow are adapted from [VisionXLab/Awesome-RS-VL-Data](https://github.com/VisionXLab/Awesome-RS-VL-Data). The upstream MIT copyright notice is retained in [LICENSE](LICENSE).

Issue statistics use [madderscientist/issueStat](https://github.com/madderscientist/issueStat). See [CONTRIBUTING.md](CONTRIBUTING.md) for workflow behavior and permissions.
