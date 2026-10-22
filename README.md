<!-- Banner slot: add a local image here when ready. -->
<!-- Optional future badges: repository stars, Issues, website, and survey paper. -->

<h1 align="center">Awesome Remote Sensing Image Generation</h1>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
</p>

<p align="center">Papers · Datasets · Benchmarks · Resources</p>

> 保留 **341 篇独立文献与资源记录**。按综述三大类、十二子类展示：第一类 **64** 条、第二类核心 **81** 条、第三类 **39** 条；第二类另有 **119** 条补充和 **6** 条口径待确认记录移至[独立清单](docs/observation-supplementary.md)。第一类、第三类本轮未按同样渠道标准重筛。另保留原有对照、相关 3D、数据、评测与背景资源；当前 README 共 **218** 个表格条目，加上独立清单的 **125** 条，共保留原有 343 个展示条目。统计不等于稿件中的 262 篇方法。见 [来源](docs/literature-sources.md)、[分类](docs/taxonomy.md)和[第二类筛选依据](docs/observation-screening.md)。

A curated collection of condition-driven, observation-driven, and image-formation-driven remote sensing image generation, with datasets, benchmarks, and clearly separated supporting literature.

Contributions are welcome. Use the [paper submission template](.github/ISSUE_TEMPLATE/new-paper.md) or [dataset submission template](.github/ISSUE_TEMPLATE/new-dataset.md). See [CONTRIBUTING.md](CONTRIBUTING.md) for maintenance and publishing notes.

<a id="inclusion-criteria"></a>
## Inclusion Criteria / 收录标准

- 收录与遥感图像生成相关、具有研究价值的期刊论文及领域认可的优质会议论文。
- 不收录一般低质量 EI 会议论文；EI 检索本身不作为收录依据，也不据此排除领域认可的优质会议。
- 允许收录相关 arXiv 预印本，并明确标注为 arXiv，不将其写成已正式发表的会议或期刊论文。
- **第二类主列表采用更严格的顶刊 / A 会标准**；仅预印本、其他渠道和口径待确认条目保留在补充清单。该标准不追溯应用到第一类、第三类或资源栏目；详见[筛选政策](docs/observation-screening.md#policy)。

<a id="news"></a>
## 🥳 News

- **2026-10-22**: Published the screened observation-driven core: 81 papers (22 / 14 / 34 / 11). Archived 119 supplementary and 6 pending records with source links; preserved all 341 records and left the other two families unchanged.

- **2026-10-16**: Reorganized the collection into three generation families and twelve subclasses. Preserved all 341 source records and existing paper/code links; separated restoration/enhancement comparators and related 3D work.

- **2026-10-14**: Expanded the seed list to 341 unique source records from the literature workbook; kept arXiv preprints and field-recognized conferences including IGARSS. Added dataset, benchmark, evaluation-metric, and survey entries.

- **2026-10-12**: Added 8 sample papers from the literature workbook, with paper links, available author repositories, and source-row references.

<a id="overview"></a>
## 🌍 Overview

<!-- Reserve this area for the survey taxonomy / summary figure / timeline. -->

The primary input-output relation determines the family; backbone names and downstream uses do not. Detection, segmentation, change analysis, mapping, and data augmentation are application tags rather than primary method families.

| Family | Primary input → generated product | README method entries | Subclasses |
| --- | --- | :---: | :---: |
| [Condition-Driven](#condition-driven) | Text, layout, map, metadata, or task control → RS imagery | 64 | 4 |
| [Observation-Driven](#observation-driven) | Existing RS observation → translated, restored, enhanced, or temporal imagery | 81 | 4 |
| [Image-Formation-Driven](#image-formation-driven) | Operational geometry, acquisition, or sensor mechanism → RS imagery | 39 | 4 |

Counts describe the current README method tables, not a newly full-text-verified method census. Only the observation-driven family received this venue filter; its source index still contains 206 records, with 125 moved to the [supplementary/pending list](docs/observation-supplementary.md). [Supporting comparators and related 3D work](#supporting-literature), generic metrics, and workflow resources remain separate. See [definitions and source-index counts](docs/taxonomy.md).

_Overview figure to be added._

<a id="usage"></a>
## 🔎 Usage

Browse the task tables below. `Paper` points to the publication or preprint; `More → Source` records the Excel row. A `—` means the field has not been confirmed, not that the resource does not exist.

[Submit a paper or dataset](https://github.com/VVGgao/Awesome-RS-Image-Generation/issues/new/choose) · [Browse Issues](https://github.com/VVGgao/Awesome-RS-Image-Generation/issues)

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
  - [Evaluation Metrics](#evaluation-metrics)
- [Papers](#papers)
  - [Condition-Driven Image Generation](#condition-driven)
    - [Text, Caption, and Foundation Generation](#text-to-image)
    - [Layout, Mask, Object, and Semantic Control](#layout-conditioned)
    - [Map, Vector, and Geospatial Metadata Control](#map-metadata)
    - [Task-Oriented Synthesis](#data-synthesis)
  - [Observation-Driven Image Generation](#observation-driven)
    - [Cross-Modal and Cross-Sensor Translation](#cross-modal)
    - [Image Editing, Restoration, and Completion](#reference-guided)
    - [Spatial-Spectral Resolution Enhancement](#spatial-spectral)
    - [Temporal, Change, and Future Generation](#temporal)
  - [Image-Formation-Driven Generation](#image-formation-driven)
    - [Differentiable Rendering and Simulation](#rendering)
    - [Geometry, View, and Acquisition Control](#geometry)
    - [Scattering, Polarimetric, and Sensor Priors](#scattering)
    - [Radiative, Atmospheric, and Spectral Physics](#spectral-physics)
- [Supporting and Related Literature](#supporting-literature)
  - [Observation-Driven Supplementary and Pending Records](#observation-supplementary)
  - [Restoration and Enhancement Comparators](#comparators)
  - [Related 3D Generation and View Synthesis](#related-3d)
- [Surveys](#surveys)
- [Awesome Lists and Resources](#resources)
- [Citation](#citation)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

<a id="datasets"></a>
## 📚 Datasets

These include generation-training data, translation data, and downstream supervision/evaluation resources. They are not all datasets designed specifically for generation. Dataset entries extracted from a method paper share that paper's source row.

<a id="comprehensive-datasets"></a>
### Comprehensive Datasets

| Year | Venue | Name | Task / Modality | Paper | Download | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | IEEE GRSM | Git-10M | Text / image / geospatial metadata; text-to-image training | [Paper](https://doi.org/10.1109/mgrs.2025.3560455) | [Project / Data](https://github.com/Chen-Yang-Liu/Text2Earth) | [Source](docs/literature-sources.md#r89) |
| 2019 | arXiv | SEN12MS | Paired SAR / multispectral / land-cover data | [Paper](https://arxiv.org/abs/1906.07789) | [Project / Data](https://github.com/zhu-xlab/SEN12MS) | [Source](docs/literature-sources.md#r32) |

<a id="task-specific-datasets"></a>
### Task-Specific Datasets

| Year | Venue | Name | Task / Modality | Paper | Download | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | IEEE JSTARS | A Large-Scale Aerial and Satellite Image Dataset for Deep Learning-Based Image Super-Resolution of Very High-Resolution Remote Sensing Imagery | Very-high-resolution image super-resolution | [Paper](https://doi.org/10.1109/jstars.2025.3610081) | — | [Source](docs/literature-sources.md#r10) |
| 2024 | arXiv | ChangeAnywhere-100K | Synthetic bi-temporal optical image pairs; change detection | [Paper](https://arxiv.org/abs/2404.08892) | [Project / Data](https://github.com/tangkai-RS/ChangeAnywhere) | [Source](docs/literature-sources.md#r77) |
| 2023 | Journal of Remote Sensing | AVIID | Aerial visible-to-infrared translation | [Paper](https://doi.org/10.34133/remotesensing.0096) | [Project / Data](https://github.com/silver-hzh/Averial-visible-to-infrared-image-translation) | [Source](docs/literature-sources.md#r24) |
| 2020 | Remote Sensing | LEVIR-CD | Optical image-pair change detection; downstream evaluation | [Paper](https://doi.org/10.3390/rs12101662) | — | [Source](docs/literature-sources.md#r30) |
| 2018 | CVPR | DOTA | Aerial object detection; layout supervision | [Paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Xia_DOTA_A_Large-Scale_CVPR_2018_paper.html) | — | [Source](docs/literature-sources.md#r34) |

<a id="benchmarks"></a>
## 📊 Benchmarks and Evaluation

| Year | Venue | Name | Task | Metrics / Protocol | Paper | Code / Data | More |
| :---: | :---: | --- | --- | --- | :---: | :---: | :---: |
| 2026 | AAAI | Pansharpening for Thin-Cloud Contaminated Remote Sensing Images: A Unified Framework and Benchmark Dataset | Pansharpening under thin clouds | — | [Paper](https://doi.org/10.1609/aaai.v40i5.37369) | — | [Source](docs/literature-sources.md#r7) |
| 2026 | arXiv | RS-RIE-Bench: Benchmarking Reasoning-Guided Remote Sensing Image Editing | Reasoning-guided remote sensing editing | Plausibility / preservation / image consistency | [Paper](https://arxiv.org/abs/2607.20197) | — | [Source](docs/literature-sources.md#r8) |
| 2025 | IEEE TGRS | Real-World Remote Sensing Image Dehazing: Benchmark and Baseline | Real-world image dehazing | — | [Paper](https://doi.org/10.1109/tgrs.2025.3584234) | — | [Source](docs/literature-sources.md#r16) |

Download links and numerical benchmark results are not inferred.

<a id="evaluation-metrics"></a>
### Evaluation Metrics

These are original papers for general-purpose evaluation metrics, not remote-sensing generation methods or dedicated remote-sensing benchmarks. Metric applicability depends on the task and protocol.

| Year | Venue | Metric | Original Paper | Paper | More |
| :---: | :---: | --- | --- | :---: | :---: |
| 2021 | EMNLP | CLIPScore | CLIPScore: A Reference-Free Evaluation Metric for Image Captioning | [Paper](https://doi.org/10.18653/v1/2021.emnlp-main.595) | [Source](docs/literature-sources.md#r29) |
| 2018 | CVPR | LPIPS | The Unreasonable Effectiveness of Deep Features as a Perceptual Metric | [Paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Zhang_The_Unreasonable_Effectiveness_CVPR_2018_paper.html) | [Source](docs/literature-sources.md#r35) |
| 2017 | NeurIPS | FID | GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium | [Paper](https://proceedings.neurips.cc/paper/2017/hash/8a1d694707eb0fefe65871369074926d-Abstract.html) | [Source](docs/literature-sources.md#r36) |
| 2004 | IEEE TIP | SSIM | Image Quality Assessment: From Error Visibility to Structural Similarity | [Paper](https://doi.org/10.1109/TIP.2003.819861) | [Source](docs/literature-sources.md#r38) |

<a id="papers"></a>
## 📄 Papers

Organized by three primary input-output relations and twelve subclasses. Entries retain their existing source-subclass assignments; this reorganization is not a new full-text eligibility audit. See [taxonomy and boundary rules](docs/taxonomy.md).

<a id="condition-driven"></a>
### Condition-Driven Image Generation

Non-target-image controls specify the requested scene: text, layouts, masks, maps, metadata, or task feedback. Check condition compliance as well as visual realism.

<a id="text-to-image"></a>
#### Text, Caption, and Foundation Generation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | AAAI | Text / caption / foundation model | Any2RSI: Controllable Remote Sensing Text-to-Image Generation via Any Control and Enriched Description | [Paper](https://doi.org/10.1609/aaai.v40i15.38283) | — | [Source](docs/literature-sources.md#r80) |
| 2026 | arXiv | Text / caption / foundation model | Contrastive Parameter Disentanglement for Multi-Modal Remote Sensing Image Generation | [Paper](https://arxiv.org/abs/2607.23673) | — | [Source](docs/literature-sources.md#r81) |
| 2026 | IEEE TGRS | Text / caption / foundation model | Language-Informed Hyperspectral Image Synthesis for Imbalanced-Small Sample Classification via Semi-Supervised Conditional Diffusion Model | [Paper](https://doi.org/10.1109/tgrs.2026.3651679) | — | [Source](docs/literature-sources.md#r82) |
| 2026 | IEEE JSTARS | Text / caption / foundation model | Multiple Conditions-Guided Diffusion Model for Remote Sensing Image Generation | [Paper](https://ieeexplore.ieee.org/document/11415370/) | — | [Source](docs/literature-sources.md#r83) |
| 2026 | ISPRS JPRS | Text / caption / foundation model | Quantitative Comparison of Fine-Tuning Techniques for Pretrained Latent Diffusion Models in the Generation of Unseen SAR Images | [Paper](https://doi.org/10.1016/j.isprsjprs.2026.02.018) | — | [Source](docs/literature-sources.md#r84) |
| 2025 | ICASSP | Text / caption / foundation model | DiffRS: An Extensible Diffusion Model for Remote Sensing Image Generation | [Paper](https://doi.org/10.1109/icassp49660.2025.10887825) | — | [Source](docs/literature-sources.md#r85) |
| 2025 | IEEE JSTARS | Text / caption / foundation model | HDP-Net: Hierarchical Dynamic Prototype Learning for Text-Based Remote Sensing Image Generation | [Paper](https://doi.org/10.1109/jstars.2025.3626406) | — | [Source](docs/literature-sources.md#r86) |
| 2025 | Remote Sensing | Text / caption / foundation model | IFADiff: Training-Free Hyperspectral Image Generation via Integer--Fractional Alternating Diffusion Sampling | [Paper](https://doi.org/10.3390/rs17233867) | — | [Source](docs/literature-sources.md#r87) |
| 2025 | IPOL | Text / caption / foundation model | Latent Diffusion Approaches for Conditional Generation of Aerial Imagery: A Study | [Paper](https://doi.org/10.5201/ipol.2025.580) | — | [Source](docs/literature-sources.md#r3001) |
| 2025 | IEEE TPAMI | Text / caption / foundation model | MetaEarth: A Generative Foundation Model for Global-Scale Remote Sensing Image Generation | [Paper](https://doi.org/10.1109/tpami.2024.3507010) | — | [Source](docs/literature-sources.md#r88) |
| 2025 | IEEE GRSM | Text / caption / foundation model | Text2Earth: Unlocking text-driven remote sensing image generation with a global-scale dataset and a foundation model | [Paper](https://doi.org/10.1109/mgrs.2025.3560455) | [Code](https://github.com/Chen-Yang-Liu/Text2Earth) | [Source](docs/literature-sources.md#r89) |
| 2024 | IEEE TGRS | Text / caption / foundation model | CRS-Diff: Controllable Remote Sensing Image Generation With Diffusion Model | [Paper](https://doi.org/10.1109/tgrs.2024.3453414) | — | [Source](docs/literature-sources.md#r90) |
| 2024 | IEEE TGRS | Text / caption / foundation model | Manifold Constraint Regularization for Remote Sensing Image Generation | [Paper](https://doi.org/10.1109/tgrs.2024.3441631) | — | [Source](docs/literature-sources.md#r91) |
| 2024 | Neural Computing and Applications | Text / caption / foundation model | RSDiff: remote sensing image generation from text using diffusion model | [Paper](https://doi.org/10.1007/s00521-024-10363-3) | — | [Source](docs/literature-sources.md#r92) |
| 2023 | Remote Sensing | Text / caption / foundation model | Gradient Structure Information-Guided Attention Generative Adversarial Networks for Remote Sensing Image Generation | [Paper](https://doi.org/10.3390/rs15112827) | — | [Source](docs/literature-sources.md#r93) |
| 2023 | Remote Sensing | Text / caption / foundation model | Synthesis of Synthetic Hyperspectral Images with Controllable Spectral Variability Using a Generative Adversarial Network | [Paper](https://doi.org/10.3390/rs15163919) | — | [Source](docs/literature-sources.md#r3021) |
| 2022 | IEEE GRSL | Text / caption / foundation model | Text-to-Remote-Sensing-Image Generation With Structured Generative Adversarial Networks | [Paper](https://doi.org/10.1109/lgrs.2021.3068391) | — | [Source](docs/literature-sources.md#r94) |
| 2021 | Remote Sensing | Text / caption / foundation model | DisasterGAN: Generative Adversarial Networks for Remote Sensing Disaster Image Generation | [Paper](https://doi.org/10.3390/rs13214284) | — | [Source](docs/literature-sources.md#r95) |
| 2019 | IGARSS | Text / caption / foundation model | Remote Sensing Image Synthesis via Graphical Generative Adversarial Networks | [Paper](https://doi.org/10.1109/igarss.2019.8898915) | — | [Source](docs/literature-sources.md#r96) |

<a id="layout-conditioned"></a>
#### Layout, Mask, Object, and Semantic Control

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | IEEE JSTARS | Layout / mask / object control | CondFusionSAR: A Bidirectional MultiConditional Fusion Network for Generating High-Resolution SAR Images With Complex Backgrounds | [Paper](https://doi.org/10.1109/jstars.2026.3677792) | — | [Source](docs/literature-sources.md#r39) |
| 2026 | IEEE JSTARS | Layout / mask / object control | Controllable Remote Sensing Image Generation With Semantic Consistency via Diffusion Models | [Paper](https://doi.org/10.1109/jstars.2026.3689363) | — | [Source](docs/literature-sources.md#r40) |
| 2026 | arXiv | Layout / mask / object control | RSGen: Enhancing Layout-Driven Remote Sensing Image Generation with Diverse Edge Guidance | [Paper](https://arxiv.org/abs/2603.15484) | — | [Source](docs/literature-sources.md#r41) |
| 2026 | IEEE TGRS | Layout / mask / object control | TerraGen: A Unified Multi-Task Layout Generation Framework for Remote Sensing Data Augmentation | [Paper](https://doi.org/10.1109/tgrs.2026.3695344) | — | [Source](docs/literature-sources.md#r42) |
| 2026 | IEEE TGRS | Layout / mask / object control | Wildfire-Diff: A Controllable Diffusion Framework for Synchronized Generation of Remote Sensing Wildfire Images and Masks | [Paper](https://doi.org/10.1109/tgrs.2026.3690189) | — | [Source](docs/literature-sources.md#r43) |
| 2025 | CVPR | Layout / mask / object control | AeroGen: Enhancing Remote Sensing Object Detection with Diffusion-Driven Data Generation | [Paper](https://doi.org/10.1109/cvpr52734.2025.00342) | [Code](https://github.com/Sonettoo/AeroGen) | [Source](docs/literature-sources.md#r44) |
| 2025 | IEEE TGRS | Layout / mask / object control | Cascaded Autoregressive Diffusion Models for Remote Sensing Scene Generation | [Paper](https://doi.org/10.1109/tgrs.2025.3622225) | — | [Source](docs/literature-sources.md#r45) |
| 2025 | IEEE TGRS | Layout / mask / object control | CC-Diff++: Spatially Controllable Text-to-Image Synthesis for Remote Sensing With Enhanced Contextual Coherence | [Paper](https://doi.org/10.1109/tgrs.2025.3616376) | — | [Source](docs/literature-sources.md#r46) |
| 2025 | IEEE GRSL | Layout / mask / object control | Diverse Instance Generation via Diffusion Models for Enhanced Few-Shot Object Detection in Remote Sensing Images | [Paper](https://doi.org/10.1109/lgrs.2025.3624148) | — | [Source](docs/literature-sources.md#r47) |
| 2025 | ICCV | Layout / mask / object control | FICGen: Frequency-Inspired Contextual Disentanglement for Layout-driven Degraded Image Generation | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_FICGen_Frequency-Inspired_Contextual_Disentanglement_for_Layout-driven_Degraded_Image_Generation_ICCV_2025_paper.html) | — | [Source](docs/literature-sources.md#r48) |
| 2025 | IEEE GRSL | Layout / mask / object control | Multi-Grained Guided Diffusion for Quantity-Controlled Remote Sensing Object Generation | [Paper](https://doi.org/10.1109/lgrs.2025.3565817) | — | [Source](docs/literature-sources.md#r49) |
| 2025 | arXiv | Layout / mask / object control | Object Fidelity Diffusion for Remote Sensing Image Generation | [Paper](https://arxiv.org/abs/2508.10801) | — | [Source](docs/literature-sources.md#r50) |
| 2025 | IEEE TGRS | Layout / mask / object control | Reconciling Semantic Controllability and Diversity for Remote Sensing Image Synthesis With Hybrid Semantic Embedding | [Paper](https://doi.org/10.1109/tgrs.2025.3552802) | — | [Source](docs/literature-sources.md#r51) |
| 2025 | Remote Sensing | Layout / mask / object control | Remote Sensing Image Semantic Segmentation Sample Generation Using a Decoupled Latent Diffusion Framework | [Paper](https://doi.org/10.3390/rs17132143) | — | [Source](docs/literature-sources.md#r52) |
| 2025 | IGARSS | Layout / mask / object control | Remote Sensing Image Synthesis via Semantic Class-Specific Generative Adversarial Networks | [Paper](https://doi.org/10.1109/igarss55030.2025.11243533) | — | [Source](docs/literature-sources.md#r1805) |
| 2025 | IEEE GRSM | Layout / mask / object control | Satellite Image Synthesis From Street View With Fine-Grained Spatial Textual Guidance: A Novel Framework | [Paper](https://doi.org/10.1109/mgrs.2025.3585358) | — | [Source](docs/literature-sources.md#r53) |
| 2025 | Remote Sensing | Layout / mask / object control | Synthesizing Remote Sensing Images from Land Cover Annotations via Graph Prior Masked Diffusion | [Paper](https://doi.org/10.3390/rs17132254) | — | [Source](docs/literature-sources.md#r54) |
| 2024 | arXiv | Layout / mask / object control | CC-Diff: Enhancing Contextual Coherence in Remote Sensing Image Synthesis | [Paper](https://arxiv.org/abs/2412.08464) | — | [Source](docs/literature-sources.md#r55) |
| 2024 | CVPR | Layout / mask / object control | SatSynth: Augmenting Image-Mask Pairs Through Diffusion Models for Aerial Semantic Segmentation | [Paper](https://doi.org/10.1109/cvpr52733.2024.02615) | — | [Source](docs/literature-sources.md#r56) |
| 2023 | IGARSS | Layout / mask / object control | Multi-Task Generative Adversarial Networks for Semantic-Guided Remote Sensing Image Generation | [Paper](https://doi.org/10.1109/igarss52108.2023.10282185) | — | [Source](docs/literature-sources.md#r1812) |
| 2023 | IEEE TGRS | Layout / mask / object control | Remote Sensing Image Synthesis via Semantic Embedding Generative Adversarial Networks | [Paper](https://doi.org/10.1109/tgrs.2023.3279663) | — | [Source](docs/literature-sources.md#r57) |
| 2023 | Remote Sensing | Layout / mask / object control | Semantic-Layout-Guided Image Synthesis for High-Quality Synthetic-Aperature Radar Detection Sample Generation | [Paper](https://doi.org/10.3390/rs15245654) | — | [Source](docs/literature-sources.md#r58) |
| 2021 | Remote Sensing | Layout / mask / object control | SSSGAN: Satellite Style and Structure Generative Adversarial Networks | [Paper](https://doi.org/10.3390/rs13193984) | — | [Source](docs/literature-sources.md#r59) |

<a id="map-metadata"></a>
#### Map, Vector, and Geospatial Metadata Control

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | arXiv | Map / geospatial metadata control | D2-CDIG: Controlled Diffusion Remote Sensing Image Generation with Dual Priors of DEM and Cloud-Fog | [Paper](https://arxiv.org/abs/2605.14326) | — | [Source](docs/literature-sources.md#r60) |
| 2026 | IEEE TGRS | Map / geospatial metadata control | EarthMapper: Visual Autoregressive Models for Controllable Bidirectional Satellite-Map Translation | [Paper](https://doi.org/10.1109/tgrs.2026.3678241) | — | [Source](docs/literature-sources.md#r61) |
| 2026 | arXiv | Map / geospatial metadata control | Efficient Geometry-Controlled High-Resolution Satellite Image Synthesis | [Paper](https://arxiv.org/abs/2605.04557) | — | [Source](docs/literature-sources.md#r62) |
| 2026 | arXiv | Map / geospatial metadata control | TerraDiT-Omega: Unified Spatial Control for Satellite Image Synthesis with Any Geospatial Primitive | [Paper](https://arxiv.org/abs/2606.31029) | — | [Source](docs/literature-sources.md#r63) |
| 2026 | arXiv | Map / geospatial metadata control | TerraDiT: Point-Conditioned Diffusion Transformer for Satellite Image Synthesis | [Paper](https://arxiv.org/abs/2603.02172) | — | [Source](docs/literature-sources.md#r1841) |
| 2026 | WACV | Map / geospatial metadata control | VectorSynth: Fine-Grained Satellite Image Synthesis with Structured Semantics | [Paper](https://doi.org/10.1109/wacv61042.2026.00678) | — | [Source](docs/literature-sources.md#r64) |
| 2025 | arXiv | Map / geospatial metadata control | Environment-Aware Satellite Image Generation with Diffusion Models | [Paper](https://arxiv.org/abs/2509.24875) | — | [Source](docs/literature-sources.md#r65) |
| 2025 | Remote Sensing | Map / geospatial metadata control | OP-Gen: A High-Quality Remote Sensing Image Generation Algorithm Guided by OSM Images and Textual Prompts | [Paper](https://doi.org/10.3390/rs17071226) | — | [Source](docs/literature-sources.md#r66) |
| 2025 | arXiv | Map / geospatial metadata control | OSMGen: Highly Controllable Satellite Image Synthesis using OpenStreetMap Data | [Paper](https://arxiv.org/abs/2511.00345) | — | [Source](docs/literature-sources.md#r67) |
| 2024 | ICLR | Map / geospatial metadata control | DiffusionSat: A Generative Foundation Model for Satellite Imagery | [Paper](https://arxiv.org/abs/2312.03606) | [Code](https://github.com/samar-khanna/DiffusionSat) | [Source](docs/literature-sources.md#r68) |
| 2023 | arXiv | Map / geospatial metadata control | Generate Your Own Scotland: Satellite Image Generation Conditioned on Maps | [Paper](https://arxiv.org/abs/2308.16648) | — | [Source](docs/literature-sources.md#r1849) |
| 2022 | IEEE TGRS | Map / geospatial metadata control | Synthesizing Optical and SAR Imagery From Land Cover Maps and Auxiliary Raster Data | [Paper](https://doi.org/10.1109/tgrs.2021.3068532) | — | [Source](docs/literature-sources.md#r69) |

<a id="data-synthesis"></a>
#### Task-Oriented Synthesis

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | CVPR | Task-oriented data synthesis | Task-Oriented Data Synthesis and Control-Rectify Sampling for Remote Sensing Semantic Segmentation | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Yang_Task-Oriented_Data_Synthesis_and_Control-Rectify_Sampling_for_Remote_Sensing_Semantic_CVPR_2026_paper.html) | — | [Source](docs/literature-sources.md#r70) |
| 2026 | arXiv | Task-oriented data synthesis | Towards Realistic Remote Sensing Dataset Distillation with Discriminative Prototype-Guided Diffusion | [Paper](https://arxiv.org/abs/2601.15829) | — | [Source](docs/literature-sources.md#r71) |
| 2025 | IEEE TGRS | Task-oriented data synthesis | Annotation-Free, High-Fidelity SAR Oil-Spill Image Synthesis via Classification-Guided Diffusion Model | [Paper](https://doi.org/10.1109/tgrs.2025.3612298) | — | [Source](docs/literature-sources.md#r72) |
| 2025 | IEEE JSTARS | Task-oriented data synthesis | DiffuSAR: Frequency Domain-Aware Diffusion Model for SAR Image Generation | [Paper](https://doi.org/10.1109/jstars.2025.3563798) | — | [Source](docs/literature-sources.md#r73) |
| 2025 | IEEE TGRS | Task-oriented data synthesis | Diffusion-Noise-Based Augmentation for Long-Tailed Remote Sensing Image Classification | [Paper](https://doi.org/10.1109/tgrs.2025.3568812) | — | [Source](docs/literature-sources.md#r74) |
| 2025 | arXiv | Task-oriented data synthesis | EarthSynth: Generating Informative Earth Observation with Diffusion Models | [Paper](https://arxiv.org/abs/2505.12108) | — | [Source](docs/literature-sources.md#r75) |
| 2024 | Remote Sensing | Task-oriented data synthesis | A Two-Stage SAR Image Generation Algorithm Based on GAN with Reinforced Constraint Filtering and Compensation Techniques | [Paper](https://doi.org/10.3390/rs16111963) | — | [Source](docs/literature-sources.md#r76) |
| 2024 | arXiv | Task-oriented data synthesis | ChangeAnywhere: Sample Generation for Remote Sensing Change Detection via Semantic Latent Diffusion Model | [Paper](https://arxiv.org/abs/2404.08892) | [Repository](https://github.com/tangkai-RS/ChangeAnywhere) | [Source](docs/literature-sources.md#r77) |
| 2024 | Remote Sensing | Task-oriented data synthesis | Coarse-to-Fine Structure and Semantic Learning for Single-Sample SAR Image Generation | [Paper](https://doi.org/10.3390/rs16173326) | — | [Source](docs/literature-sources.md#r78) |
| 2023 | IEEE TGRS | Task-oriented data synthesis | Efficient and Controllable Remote Sensing Fake Sample Generation Based on Diffusion Model | [Paper](https://doi.org/10.1109/tgrs.2023.3268331) | — | [Source](docs/literature-sources.md#r79) |

<a id="restoration"></a>
<a id="observation-driven"></a>
### Observation-Driven Image Generation

Existing remote-sensing observations constrain translated, edited, restored, completed, enhanced, or temporal products. Restoration and reconstruction are part of the main scope; preserve source evidence and report uncertainty where applicable.

**Core list: 81 papers** after venue/publication screening of 206 indexed records (2026-10-21 snapshot; published here 2026-10-22). Subclasses contain **22 / 14 / 34 / 11** papers. [119 supplementary and 6 venue-scope-pending records](docs/observation-supplementary.md) remain traceable; see the [screening policy and per-paper evidence](docs/observation-screening.md). This is not a new full-text method audit; recent additions remain candidates outside this list.

<a id="cross-modal"></a>
#### Cross-Modal and Cross-Sensor Translation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | ICML | Cross-modal / cross-sensor translation | Any2Any: Unified Arbitrary Modality Translation for Remote Sensing | [Paper](https://proceedings.mlr.press/v306/chen26go.html) | — | [Source](docs/literature-sources.md#r132) |
| 2026 | IEEE TGRS | Cross-modal / cross-sensor translation | CycleMamba: Cycle-Consistent Learning for Aerial Visible-to-Infrared Image Translation | [Paper](https://doi.org/10.1109/tgrs.2026.3656650) | — | [Source](docs/literature-sources.md#r134) |
| 2026 | IEEE TGRS | Cross-modal / cross-sensor translation | Diffusion Bridge Generation of Visible Light-to-Infrared Images Based on Multiscale Enhancement From Aerial Photography Perspective | [Paper](https://doi.org/10.1109/tgrs.2026.3677822) | — | [Source](docs/literature-sources.md#r137) |
| 2026 | IEEE TIP | Cross-modal / cross-sensor translation | KeypointDiff: Keypoints-Guided Diffusion Model for Unpaired Object-Level SAR-to-Optical Aircraft Image Translation | [Paper](https://doi.org/10.1109/TIP.2026.3703726) | — | [Source](docs/literature-sources.md#r156) |
| 2025 | IEEE TGRS | Cross-modal / cross-sensor translation | Cross-Modal Visible-to-Infrared Image Translation in Remote Sensing Guided by Thermal Features | [Paper](https://doi.org/10.1109/tgrs.2025.3579267) | — | [Source](docs/literature-sources.md#r143) |
| 2025 | IEEE TGRS | Cross-modal / cross-sensor translation | DOGAN: DINO-Based Optical-Prior-Driven GAN for SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2025.3606979) | — | [Source](docs/literature-sources.md#r144) |
| 2025 | IEEE TGRS | Cross-modal / cross-sensor translation | HVT-cGAN: Hybrid Vision Transformer cGAN for SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2024.3523040) | — | [Source](docs/literature-sources.md#r147) |
| 2025 | ICCV | Cross-modal / cross-sensor translation | Leveraging BEV Paradigm for Ground-to-Aerial Image Synthesis | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Ye_Leveraging_BEV_Paradigm_for_Ground-to-Aerial_Image_Synthesis_ICCV_2025_paper.html) | — | [Source](docs/literature-sources.md#r149) |
| 2025 | IEEE TGRS | Cross-modal / cross-sensor translation | RLI-DM: Robust Layout-Based Iterative Diffusion Model for SAR-to-RGB Image Translation | [Paper](https://doi.org/10.1109/tgrs.2025.3613938) | — | [Source](docs/literature-sources.md#r150) |
| 2025 | IEEE TIP | Cross-modal / cross-sensor translation | S3OIL: Semi-Supervised SAR-to-Optical Image Translation via Multi-Scale and Cross-Set Matching | [Paper](https://doi.org/10.1109/tip.2025.3616576) | — | [Source](docs/literature-sources.md#r151) |
| 2025 | ICCV | Cross-modal / cross-sensor translation | TerraMind: Large-Scale Generative Multimodality for Earth Observation | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Jakubik_TerraMind_Large-Scale_Generative_Multimodality_for_Earth_Observation_ICCV_2025_paper.html) | [Code](https://github.com/IBM/terramind) | [Source](docs/literature-sources.md#r155) |
| 2025 | IEEE TGRS | Cross-modal / cross-sensor translation | USTNet: A U-Net Swin Transformer Network for Aerial Visible-to-Infrared Image Translation | [Paper](https://doi.org/10.1109/tgrs.2025.3604474) | — | [Source](docs/literature-sources.md#r157) |
| 2024 | IEEE TGRS | Cross-modal / cross-sensor translation | Conditional Diffusion Model With Spatial-Frequency Refinement for SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2024.3491826) | — | [Source](docs/literature-sources.md#r161) |
| 2024 | IEEE TGRS | Cross-modal / cross-sensor translation | DR-AVIT: Toward Diverse and Realistic Aerial Visible-to-Infrared Image Translation | [Paper](https://doi.org/10.1109/tgrs.2024.3405989) | — | [Source](docs/literature-sources.md#r163) |
| 2024 | IEEE TGRS | Cross-modal / cross-sensor translation | Integrating Multitemporal SAR and Optical Information for Missing Optical Imagery Generation | [Paper](https://doi.org/10.1109/tgrs.2024.3451558) | — | [Source](docs/literature-sources.md#r166) |
| 2023 | IEEE TGRS | Cross-modal / cross-sensor translation | CFCA-SET: Coarse-to-Fine Context-Aware SAR-to-EO Translation With Auxiliary Learning of SAR-to-NIR Translation | [Paper](https://doi.org/10.1109/tgrs.2023.3318980) | — | [Source](docs/literature-sources.md#r179) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | Cloud removal in remote sensing images using generative adversarial networks and SAR-to-optical image translation | [Paper](https://doi.org/10.1109/tgrs.2021.3131035) | — | [Source](docs/literature-sources.md#r180) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | FG-GAN: A Fine-Grained Generative Adversarial Network for Unsupervised SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2022.3165371) | — | [Source](docs/literature-sources.md#r181) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | Hybrid cGAN: Coupling Global and Local Features for SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2022.3212208) | — | [Source](docs/literature-sources.md#r182) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | Multiscale Generative Adversarial Network Based on Wavelet Feature Learning for SAR-to-Optical Image Translation | [Paper](https://doi.org/10.1109/tgrs.2022.3211415) | — | [Source](docs/literature-sources.md#r183) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | SAR-to-Optical Image Translation With Hierarchical Latent Features | [Paper](https://doi.org/10.1109/tgrs.2022.3200996) | — | [Source](docs/literature-sources.md#r187) |
| 2022 | IEEE TGRS | Cross-modal / cross-sensor translation | Basis Pursuit Denoising via Recurrent Neural Network Applied to Super-Resolving SAR Tomography | [Paper](https://doi.org/10.1109/tgrs.2022.3221185) | — | [Source](docs/literature-sources.md#r4784) |

<a id="reference-guided"></a>
#### Image Editing, Restoration, and Completion

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2025 | IEEE TGRS | Editing / restoration / completion | A Dual-Stage Residual Diffusion Model With Perceptual Decoding for Remote Sensing Image Dehazing | [Paper](https://doi.org/10.1109/tgrs.2025.3600540) | — | [Source](docs/literature-sources.md#r201) |
| 2025 | IEEE TGRS | Editing / restoration / completion | DBD-CR: Dual-Branch Diffusion Residual Reconstruction for Cloud Removal in Optical Remote Sensing Images | [Paper](https://doi.org/10.1109/tgrs.2025.3550422) | — | [Source](docs/literature-sources.md#r204) |
| 2025 | IEEE TGRS | Editing / restoration / completion | Dehazing-DiffGAN: Sequential Fusion of Diffusion Models and GANs for High-Fidelity Remote Sensing Image Dehazing | [Paper](https://doi.org/10.1109/tgrs.2025.3603430) | — | [Source](docs/literature-sources.md#r205) |
| 2025 | IEEE TGRS | Editing / restoration / completion | DFG-DDM: Deep Frequency-Guided Denoising Diffusion Model for Remote Sensing Image Dehazing | [Paper](https://doi.org/10.1109/tgrs.2025.3585894) | — | [Source](docs/literature-sources.md#r206) |
| 2025 | IEEE TGRS | Editing / restoration / completion | Diffusion Posterior Sampling for SAR Despeckling | [Paper](https://doi.org/10.1109/tgrs.2025.3541013) | — | [Source](docs/literature-sources.md#r207) |
| 2025 | CVPR | Editing / restoration / completion | Effective Cloud Removal for Remote Sensing Images by an Improved Mean-Reverting Denoising Model with Elucidated Design Space | [Paper](https://doi.org/10.1109/cvpr52734.2025.01663) | — | [Source](docs/literature-sources.md#r209) |
| 2025 | IEEE TGRS | Editing / restoration / completion | KAO: Kernel-Adaptive Optimization in Diffusion for Satellite Image | [Paper](https://doi.org/10.1109/tgrs.2025.3621738) | — | [Source](docs/literature-sources.md#r213) |
| 2025 | IEEE TGRS | Editing / restoration / completion | Multimodal Diffusion Bridge With Attention-Based SAR Fusion for Satellite Image Cloud Removal | [Paper](https://doi.org/10.1109/tgrs.2025.3604654) | — | [Source](docs/literature-sources.md#r215) |
| 2024 | NeurIPS | Editing / restoration / completion | COSMIC: Compress Satellite Images Efficiently via Diffusion Compensation | [Paper](https://doi.org/10.52202/079017-2918) | — | [Source](docs/literature-sources.md#r221) |
| 2024 | IEEE TGRS | Editing / restoration / completion | Despeckling SAR Images With Log-Yeo--Johnson Transformation and Conditional Diffusion Models | [Paper](https://doi.org/10.1109/tgrs.2024.3419083) | — | [Source](docs/literature-sources.md#r222) |
| 2024 | IEEE TGRS | Editing / restoration / completion | DiffCR: A Fast Conditional Diffusion Framework for Cloud Removal From Optical Satellite Images | [Paper](https://doi.org/10.1109/tgrs.2024.3365806) | — | [Source](docs/literature-sources.md#r223) |
| 2023 | IEEE TGRS | Editing / restoration / completion | Transformer Meets GAN: Cloud-Free Multispectral Image Reconstruction via Multisensor Data Fusion in Satellite Images | [Paper](https://doi.org/10.1109/tgrs.2023.3326545) | — | [Source](docs/literature-sources.md#r230) |
| 2022 | IEEE TGRS | Editing / restoration / completion | Dehaze-AGGAN: Unpaired Remote Sensing Image Dehazing Using Enhanced Attention-Guide Generative Adversarial Networks | [Paper](https://doi.org/10.1109/tgrs.2022.3204890) | — | [Source](docs/literature-sources.md#r231) |
| 2022 | IEEE TGRS | Editing / restoration / completion | PLFM: Pixel-Level Merging of Intermediate Feature Maps by Disentangling and Fusing Spatial and Temporal Data for Cloud Removal | [Paper](https://doi.org/10.1109/tgrs.2022.3208694) | — | [Source](docs/literature-sources.md#r232) |

<a id="spatial-spectral"></a>
#### Spatial-Spectral Resolution Enhancement

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | ICML | Spatial–spectral resolution enhancement | AnyBand-Diff: A Unified Remote Sensing Image Generation and Band Repair Framework with Spectral Priors | [Paper](https://proceedings.mlr.press/v306/zuopeng26a.html) | — | [Source](docs/literature-sources.md#r237) |
| 2026 | ICML | Spatial–spectral resolution enhancement | Degradation-Aware Metric Prompting for Hyperspectral Image Restoration | [Paper](https://proceedings.mlr.press/v306/wang26hr.html) | — | [Source](docs/literature-sources.md#r5474) |
| 2026 | CVPR | Spatial–spectral resolution enhancement | EMR-Diff: Edge-Aware Multimodal Residual Diffusion Model for Hyperspectral Image Super-Resolution | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_EMR-Diff_Edge-aware_Multimodal_Residual_Diffusion_Model_for_Hyperspectral_Image_Super-resolution_CVPR_2026_paper.html) | — | [Source](docs/literature-sources.md#r239) |
| 2026 | RSE | Spatial–spectral resolution enhancement | PGDM: Physically Guided Diffusion Model for Land Surface Temperature Downscaling | [Paper](https://doi.org/10.1016/j.rse.2026.115432) | — | [Source](docs/literature-sources.md#r243) |
| 2026 | CVPR | Spatial–spectral resolution enhancement | Remote Sensing Image Super-Resolution for Imbalanced Textures: A Texture-Aware Diffusion Framework | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_Remote_Sensing_Image_Super-Resolution_for_Imbalanced_Textures_A_Texture-Aware_Diffusion_CVPR_2026_paper.html) | — | [Source](docs/literature-sources.md#r245) |
| 2026 | IEEE TGRS | Spatial–spectral resolution enhancement | Spatiotemporal Dual Priors Guided Diffusion for Remote Sensing Spatiotemporal Fusion | [Paper](https://doi.org/10.1109/tgrs.2026.3664495) | — | [Source](docs/literature-sources.md#r248) |
| 2026 | CVPR | Spatial–spectral resolution enhancement | Spectral Super-Resolution via Adversarial Unfolding and Data-Driven Spectrum Regularization: From Multispectral Satellite Data to NASA Hyperspectral Image | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Young_Spectral_Super-Resolution_via_Adversarial_Unfolding_and_Data-Driven_Spectrum_Regularization_From_CVPR_2026_paper.html) | — | [Source](docs/literature-sources.md#r249) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | DiffFuSR: Super-Resolution of all Sentinel-2 Multispectral Bands using Diffusion Models | [Paper](https://doi.org/10.1109/tgrs.2025.3638896) | — | [Source](docs/literature-sources.md#r253) |
| 2025 | IEEE TMM | Spatial–spectral resolution enhancement | FrDiff: Framelet-Based Conditional Diffusion Model for Multispectral and Panchromatic Image Fusion | [Paper](https://doi.org/10.1109/tmm.2025.3565985) | — | [Source](docs/literature-sources.md#r254) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | HyperKING: Quantum-Classical Generative Adversarial Networks for Hyperspectral Image Restoration | [Paper](https://doi.org/10.1109/tgrs.2025.3561951) | — | [Source](docs/literature-sources.md#r255) |
| 2025 | CVPR | Spatial–spectral resolution enhancement | Hyperspectral Pansharpening via Diffusion Models with Iteratively Zero-Shot Guidance | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Xiao_Hyperspectral_Pansharpening_via_Diffusion_Models_with_Iteratively_Zero-Shot_Guidance_CVPR_2025_paper.html) | — | [Source](docs/literature-sources.md#r256) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | Learning Diffusion High-Quality Priors for Pan-Sharpening: A Two-Stage Approach With Time-Aware Adapter Fine-Tuning | [Paper](https://doi.org/10.1109/tgrs.2025.3538744) | — | [Source](docs/literature-sources.md#r257) |
| 2025 | ICCV | Spatial–spectral resolution enhancement | NeurOp-Diff: Continuous Remote Sensing Image Super-Resolution via Neural Operator Diffusion | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Xu_NeurOp-Diff_Continuous_Remote_Sensing_Image_Super-Resolution_via_Neural_Operator_Diffusion_ICCV_2025_paper.html) | [Code](https://github.com/zerono000/NeurOp-Diff) | [Source](docs/literature-sources.md#r259) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | PanDiT: A Few-Step Diffusion Transformer for High-Fidelity and Efficient Pansharpening | [Paper](https://doi.org/10.1109/tgrs.2025.3630637) | — | [Source](docs/literature-sources.md#r260) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | SeG-SR: Integrating Semantic Knowledge Into Remote Sensing Image Super-Resolution via Vision-Language Model | [Paper](https://doi.org/10.1109/tgrs.2025.3612420) | — | [Source](docs/literature-sources.md#r5529) |
| 2025 | CVPR | Spatial–spectral resolution enhancement | Self-Learning Hyperspectral and Multispectral Image Fusion via Adaptive Residual Guided Subspace Diffusion Model | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Zhu_Self-Learning_Hyperspectral_and_Multispectral_Image_Fusion_via_Adaptive_Residual_Guided_CVPR_2025_paper.html) | — | [Source](docs/literature-sources.md#r264) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | Super-Resolved 3-D Satellite Lidar Imaging of Earth via Generative Diffusion Models | [Paper](https://doi.org/10.1109/tgrs.2025.3543670) | — | [Source](docs/literature-sources.md#r266) |
| 2025 | IEEE TGRS | Spatial–spectral resolution enhancement | TTRD3: Texture Transfer Residual Denoising Dual Diffusion Model for Remote Sensing Image Super-Resolution | [Paper](https://doi.org/10.1109/TGRS.2025.3626248) | — | [Source](docs/literature-sources.md#r270) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | A Conditional Diffusion Model With Fast Sampling Strategy for Remote Sensing Image Super-Resolution | [Paper](https://doi.org/10.1109/tgrs.2024.3458009) | — | [Source](docs/literature-sources.md#r272) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | A Spectral Diffusion Prior for Unsupervised Hyperspectral Image Super-Resolution | [Paper](https://doi.org/10.1109/tgrs.2024.3449073) | — | [Source](docs/literature-sources.md#r273) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | Empower Generalizability for Pansharpening Through Text-Modulated Diffusion Model | [Paper](https://doi.org/10.1109/tgrs.2024.3434431) | — | [Source](docs/literature-sources.md#r275) |
| 2024 | AAAI | Spatial–spectral resolution enhancement | Enhancing Hyperspectral Images via Diffusion Model and Group-Autoencoder Super-Resolution Network | [Paper](https://doi.org/10.1609/aaai.v38i6.28392) | — | [Source](docs/literature-sources.md#r276) |
| 2024 | CVPR | Spatial–spectral resolution enhancement | HIR-Diff: Unsupervised Hyperspectral Image Restoration Via Improved Diffusion Models | [Paper](https://doi.org/10.1109/cvpr52733.2024.00290) | [Code](https://github.com/LiPang/HIRDiff) | [Source](docs/literature-sources.md#r277) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | ISPDiff: Interpretable Scale-Propelled Diffusion Model for Hyperspectral Image Super-Resolution | [Paper](https://doi.org/10.1109/tgrs.2024.3407967) | — | [Source](docs/literature-sources.md#r278) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | PromptHSI: Universal Hyperspectral Image Restoration With Vision-Language Modulated Frequency Adaptation | [Paper](https://doi.org/10.1109/tgrs.2026.3660506) | — | [Source](docs/literature-sources.md#r5546) |
| 2024 | NeurIPS | Spatial–spectral resolution enhancement | SSDiff: Spatial-spectral Integrated Diffusion Model for Remote Sensing Pansharpening | [Paper](https://doi.org/10.52202/079017-2478) | — | [Source](docs/literature-sources.md#r282) |
| 2024 | CVPR | Spatial–spectral resolution enhancement | Unmixing before Fusion: A Generalized Paradigm for Multi-Source-Based Hyperspectral Image Synthesis | [Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Yu_Unmixing_Before_Fusion_A_Generalized_Paradigm_for_Multi-Source-based_Hyperspectral_Image_CVPR_2024_paper.html) | — | [Source](docs/literature-sources.md#r283) |
| 2024 | CVPR | Spatial–spectral resolution enhancement | Unmixing Diffusion for Self-Supervised Hyperspectral Image Denoising | [Paper](https://doi.org/10.1109/cvpr52733.2024.02628) | — | [Source](docs/literature-sources.md#r284) |
| 2024 | IEEE TGRS | Spatial–spectral resolution enhancement | VSDM: Variable-Scale Diffusion Model Based on Dynamic Condition Guidance for Pansharpening | [Paper](https://doi.org/10.1109/tgrs.2024.3504857) | — | [Source](docs/literature-sources.md#r286) |
| 2023 | ICCV | Spatial–spectral resolution enhancement | DDS2M: Self-Supervised Denoising Diffusion Spatio-Spectral Model for Hyperspectral Image Restoration | [Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Miao_DDS2M_Self-Supervised_Denoising_Diffusion_Spatio-Spectral_Model_for_Hyperspectral_Image_Restoration_ICCV_2023_paper.html) | — | [Source](docs/literature-sources.md#r287) |
| 2023 | IEEE TGRS | Spatial–spectral resolution enhancement | EDiffSR: An Efficient Diffusion Probabilistic Model for Remote Sensing Image Super-Resolution | [Paper](https://doi.org/10.1109/tgrs.2023.3341437) | — | [Source](docs/literature-sources.md#r288) |
| 2023 | ICCV | Spatial–spectral resolution enhancement | HSR-Diff: Hyperspectral Image Super-Resolution via Conditional Diffusion Models | [Paper](https://doi.org/10.1109/iccv51070.2023.00652) | — | [Source](docs/literature-sources.md#r289) |
| 2023 | IEEE TGRS | Spatial–spectral resolution enhancement | PanDiff: A Novel Pansharpening Method Based on Denoising Diffusion Probabilistic Model | [Paper](https://doi.org/10.1109/tgrs.2023.3279864) | — | [Source](docs/literature-sources.md#r290) |
| 2021 | IEEE TGRS | Spatial–spectral resolution enhancement | Remote Sensing Image Spatiotemporal Fusion Using a Generative Adversarial Network | [Paper](https://doi.org/10.1109/tgrs.2020.3010530) | — | [Source](docs/literature-sources.md#r291) |

<a id="temporal"></a>
#### Temporal, Change, and Future Generation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | CVPR | Temporal / change / future generation | ChangeBridge: Spatiotemporal Image Generation with Multimodal Controls for Remote Sensing | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Zhao_ChangeBridge_Spatiotemporal_Image_Generation_with_Multimodal_Controls_for_Remote_Senisng_CVPR_2026_paper.html) | — | [Source](docs/literature-sources.md#r292) |
| 2026 | IEEE TPAMI | Temporal / change / future generation | Generating Any Changes in the Noise Domain | [Paper](https://doi.org/10.1109/tpami.2025.3643733) | — | [Source](docs/literature-sources.md#r293) |
| 2026 | ICLR | Temporal / change / future generation | TAMMs: Change Understanding and Forecasting in Satellite Image Time Series with Temporal-Aware Multimodal Models | [Paper](https://proceedings.iclr.cc/paper_files/paper/2026/hash/2ce4f0b8e24c45318352068603153590-Abstract-Conference.html) | — | [Source](docs/literature-sources.md#r297) |
| 2025 | AAAI | Temporal / change / future generation | ChangeDiff: A Multi-Temporal Change Detection Data Generator with Flexible Text Prompts via Diffusion Model | [Paper](https://doi.org/10.1609/aaai.v39i9.33058) | — | [Source](docs/literature-sources.md#r299) |
| 2025 | IEEE TGRS | Temporal / change / future generation | HyperMM: Satellite Image Sequence Prediction via Hypergraph-Enhanced Motion Matrix | [Paper](https://doi.org/10.1109/tgrs.2025.3598612) | — | [Source](docs/literature-sources.md#r300) |
| 2025 | IEEE TGRS | Temporal / change / future generation | Ringmo-SenseV2: Remote Sensing Foundation Model for Spatiotemporal Prediction Based on Multisource Heterogeneous Time-Series Data | [Paper](https://doi.org/10.1109/tgrs.2025.3565203) | — | [Source](docs/literature-sources.md#r301) |
| 2025 | CVPR | Temporal / change / future generation | The Change You Want to Detect: Semantic Change Detection in Earth Observation with Hybrid Data Generation | [Paper](https://doi.org/10.1109/cvpr52734.2025.00211) | — | [Source](docs/literature-sources.md#r303) |
| 2024 | IEEE TPAMI | Temporal / change / future generation | Changen2: Multi-Temporal Remote Sensing Generative Change Foundation Model | [Paper](https://doi.org/10.1109/tpami.2024.3475824) | — | [Source](docs/literature-sources.md#r305) |
| 2023 | IEEE TGRS | Temporal / change / future generation | Learning Spatial--Temporal Consistency for Satellite Image Sequence Prediction | [Paper](https://doi.org/10.1109/tgrs.2023.3303947) | — | [Source](docs/literature-sources.md#r5619) |
| 2023 | ICCV | Temporal / change / future generation | Scalable Multi-Temporal Remote Sensing Change Data Generation via Simulating Stochastic Change Process | [Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Zheng_Scalable_Multi-Temporal_Remote_Sensing_Change_Data_Generation_via_Simulating_Stochastic_ICCV_2023_paper.html) | — | [Source](docs/literature-sources.md#r307) |
| 2022 | IEEE TGRS | Temporal / change / future generation | MSTCGAN: Multiscale Time Conditional Generative Adversarial Network for Long-Term Satellite Image Sequence Prediction | [Paper](https://doi.org/10.1109/tgrs.2022.3181279) | — | [Source](docs/literature-sources.md#r5622) |


<a id="other-tasks"></a>
<a id="physics"></a>
<a id="image-formation-driven"></a>
### Image-Formation-Driven Generation

Geometry, acquisition parameters, scattering, polarization, radiative processes, rendering, or sensor mechanisms operationally constrain generation. A SAR or hyperspectral output alone does not establish formation-aware generation.

<a id="rendering"></a>
#### Differentiable Rendering and Simulation

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | ISPRS JPRS | Differentiable rendering / simulation | A Differentiable Method for Novel View SAR Image Generation via 3D Gaussian Splatting | [Paper](https://doi.org/10.1016/j.isprsjprs.2025.10.034) | — | [Source](docs/literature-sources.md#r97) |
| 2026 | ACM MM (accepted) | Differentiable rendering / simulation | G-MAD: A Game-Based Data Generation Framework for Multi-View RGB-T Aerial Object Detection | [Paper](https://doi.org/10.1145/3767308.3834743) | — | [Source](docs/literature-sources.md#r98) |
| 2026 | IEEE JSTARS | Differentiable rendering / simulation | SAR-3DGS: 3-D Gaussian Splatting for Synthetic Aperture Radar Novel View Synthesis and Target Reconstruction | [Paper](https://doi.org/10.1109/jstars.2026.3673407) | — | [Source](docs/literature-sources.md#r99) |
| 2026 | IEEE TGRS | Differentiable rendering / simulation | Splatting SA: Direct Rendering of Synthetic Aperture Imagery | [Paper](https://doi.org/10.1109/tgrs.2026.3653637) | — | [Source](docs/literature-sources.md#r100) |
| 2025 | IGARSS | Differentiable rendering / simulation | Generating SAR Images from Optical Data: A Hybrid AI and Physics-Based Approach | [Paper](https://doi.org/10.1109/igarss55030.2025.11243598) | — | [Source](docs/literature-sources.md#r101) |
| 2025 | IGARSS | Differentiable rendering / simulation | SAR Image Generation via a Differentiable Framework Leveraging 3D Gaussian Splatting | [Paper](https://doi.org/10.1109/igarss55030.2025.11243095) | — | [Source](docs/literature-sources.md#r3305) |
| 2025 | IEEE TGRS | Differentiable rendering / simulation | SAR-GS: Gaussian Splatting-Based SAR Image Rendering and Target Reconstruction | [Paper](https://doi.org/10.1109/tgrs.2025.3639636) | — | [Source](docs/literature-sources.md#r102) |
| 2025 | Remote Sensing | Differentiable rendering / simulation | TerrAInav Sim: An Open-Source Simulation of UAV Aerial Imaging from Map-Based Data | [Paper](https://doi.org/10.3390/rs17081454) | — | [Source](docs/literature-sources.md#r103) |
| 2024 | IEEE TGRS | Differentiable rendering / simulation | Synthetic Aperture Radar Deep Statistical Imaging Through Diffusion Generative Model Conditional Inference | [Paper](https://ieeexplore.ieee.org/document/10754635/) | — | [Source](docs/literature-sources.md#r104) |
| 2023 | Remote Sensing | Differentiable rendering / simulation | Fast SAR Image Simulation Based on Echo Matrix Cell Algorithm Including Multiple Scattering | [Paper](https://doi.org/10.3390/rs15143637) | — | [Source](docs/literature-sources.md#r105) |
| 2023 | IGARSS | Differentiable rendering / simulation | SAR Image Generation by Integrating Differentiable SAR Renderer with Neural Networks | [Paper](https://doi.org/10.1109/igarss52108.2023.10283368) | — | [Source](docs/literature-sources.md#r106) |
| 2021 | Remote Sensing | Differentiable rendering / simulation | SAR Image Simulation of Complex Target including Multiple Scattering | [Paper](https://doi.org/10.3390/rs13234854) | — | [Source](docs/literature-sources.md#r107) |

<a id="geometry"></a>
#### Geometry, View, and Acquisition Control

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | Remote Sensing | Geometry / view / acquisition control | Dual-Branch Feature Decoupling GAN with Wavelet Constraint for Azimuth-Controllable SAR Image Simulation | [Paper](https://doi.org/10.3390/rs18111784) | — | [Source](docs/literature-sources.md#r108) |
| 2026 | arXiv | Geometry / view / acquisition control | GeoDiff-SAR II: 3D-Driven Foundation Diffusion Models for SAR Generation via Decoupled Control | [Paper](https://arxiv.org/abs/2605.21116) | — | [Source](docs/literature-sources.md#r110) |
| 2026 | arXiv | Geometry / view / acquisition control | GeoDiff-SAR: A Geometric-Prior-Guided Diffusion Model for SAR Image Generation | [Paper](https://arxiv.org/abs/2601.03499) | — | [Source](docs/literature-sources.md#r109) |
| 2025 | Remote Sensing | Geometry / view / acquisition control | An Azimuth-Continuously Controllable SAR Image Generation Algorithm Based on GAN | [Paper](https://doi.org/10.3390/rs17223763) | — | [Source](docs/literature-sources.md#r111) |
| 2025 | IGARSS | Geometry / view / acquisition control | Multi-View Approach for Physically-Guided SAR Image Generation Based on StyleGAN2 | [Paper](https://doi.org/10.1109/igarss55030.2025.11242603) | — | [Source](docs/literature-sources.md#r112) |
| 2025 | IGARSS | Geometry / view / acquisition control | SAR Image Generation Algorithm Based on Azimuth Partition Directed Generative Adversarial Network | [Paper](https://doi.org/10.1109/igarss55030.2025.11242751) | — | [Source](docs/literature-sources.md#r113) |
| 2024 | IEEE JSTARS | Geometry / view / acquisition control | ATGAN: A SAR Target Image Generation Method for Automatic Target Recognition | [Paper](https://doi.org/10.1109/jstars.2024.3370185) | — | [Source](docs/literature-sources.md#r114) |
| 2024 | IET RSN | Geometry / view / acquisition control | Circular Synthetic Aperture Radar Sub-Aperture Angle Information Complementation Based on Azimuth-Controllable Generative Adversarial Network | [Paper](https://doi.org/10.1049/rsn2.12616) | — | [Source](docs/literature-sources.md#r115) |
| 2022 | IEEE JSTARS | Geometry / view / acquisition control | SAR Target Image Generation Method Using Azimuth-Controllable Generative Adversarial Network | [Paper](https://doi.org/10.1109/jstars.2022.3218369) | — | [Source](docs/literature-sources.md#r116) |

<a id="scattering"></a>
#### Scattering, Polarimetric, and Sensor Priors

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | arXiv | Scattering / polarimetric / sensor priors | HuiYanEarth-SAR: A Foundation Model for High-Fidelity and Low-Cost Global Remote Sensing Imagery Generation | [Paper](https://arxiv.org/abs/2604.11444) | — | [Source](docs/literature-sources.md#r123) |
| 2026 | AAAI | Scattering / polarimetric / sensor priors | SAR-DisentDM: A Semantic-Disentangled Diffusion Model for Limited-Data SAR Image Synthesis | [Paper](https://doi.org/10.1609/aaai.v40i14.38165) | — | [Source](docs/literature-sources.md#r124) |
| 2026 | Remote Sensing | Scattering / polarimetric / sensor priors | Scattering Center Prior-Guided Diffusion for Unknown-Azimuth SAR Image Generation | [Paper](https://doi.org/10.3390/rs18142417) | — | [Source](docs/literature-sources.md#r126) |
| 2026 | IEEE TGRS | Scattering / polarimetric / sensor priors | Scattering-Aware Diffusion Model: Enforcing Polarimetric Fidelity for PolSAR Data Generation | [Paper](https://doi.org/10.1109/tgrs.2026.3693640) | — | [Source](docs/literature-sources.md#r125) |
| 2026 | JKSUCIS | Scattering / polarimetric / sensor priors | Ship-SAR: an improved ship image generation framework of synthetic aperture radar via denoising diffusion probabilistic model | [Paper](https://doi.org/10.1007/s44443-026-00713-7) | — | [Source](docs/literature-sources.md#r3855) |
| 2025 | IGARSS | Scattering / polarimetric / sensor priors | A Fast SAR Image Generation Method Based on System Transfer Function Convolution | [Paper](https://doi.org/10.1109/igarss55030.2025.11243294) | — | [Source](docs/literature-sources.md#r127) |
| 2025 | IEEE JSTARS | Scattering / polarimetric / sensor priors | ESF-GAN: Physics-Driven Electromagnetic Scattering Feature Fusion-Based GAN for SAR Image Augmentation | [Paper](https://doi.org/10.1109/jstars.2025.3601055) | — | [Source](docs/literature-sources.md#r128) |
| 2025 | IGARSS | Scattering / polarimetric / sensor priors | One Polarimetric Mechanism-Guide Network for PolSAR False Sea Scene Generation | [Paper](https://doi.org/10.1109/igarss55030.2025.11242740) | — | [Source](docs/literature-sources.md#r129) |
| 2025 | ICCV | Scattering / polarimetric / sensor priors | Ph-GAN: Physics-Inspired GAN for Generating SAR Images Under Limited Data | [Paper](https://arxiv.org/abs/2503.02242) | — | [Source](docs/literature-sources.md#r130) |
| 2025 | arXiv | Scattering / polarimetric / sensor priors | Physics-Informed Diffusion Models for SAR Ship Wake Generation from Text Prompts | [Paper](https://arxiv.org/abs/2504.20241) | — | [Source](docs/literature-sources.md#r3866) |
| 2024 | IEEE GRSL | Scattering / polarimetric / sensor priors | PolSAR Ship Targets Generation via the Polarimetric Feature Guided Denoising Diffusion Probabilistic Model | [Paper](https://doi.org/10.1109/lgrs.2024.3407147) | — | [Source](docs/literature-sources.md#r131) |
| 2024 | arXiv | Scattering / polarimetric / sensor priors | SAR-AE-SFP: SAR Imagery Adversarial Example in Real Physics domain with Target Scattering Feature Parameters | [Paper](https://arxiv.org/abs/2403.01210) | — | [Source](docs/literature-sources.md#r3874) |

<a id="spectral-physics"></a>
#### Radiative, Atmospheric, and Spectral Physics

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2024 | Remote Sensing | Radiative / atmospheric / spectral physics | High-Fidelity Infrared Remote Sensing Image Generation Method Coupled with the Global Radiation Scattering Mechanism and Pix2PixGAN | [Paper](https://doi.org/10.3390/rs16234350) | — | [Source](docs/literature-sources.md#r117) |
| 2024 | IEEE TGRS | Radiative / atmospheric / spectral physics | UnmixDiff: Unmixing-Based Diffusion Model for Hyperspectral Image Synthesis | [Paper](https://doi.org/10.1109/tgrs.2024.3425517) | [Code](https://github.com/yuyang95/UnmixingDM) | [Source](docs/literature-sources.md#r118) |
| 2023 | IEEE TGRS | Radiative / atmospheric / spectral physics | Hyperspectral Remote Sensing Image Synthesis Based on Implicit Neural Spectral Mixing Models | [Paper](https://doi.org/10.1109/tgrs.2022.3232705) | — | [Source](docs/literature-sources.md#r119) |
| 2023 | IEEE TGRS | Radiative / atmospheric / spectral physics | Physics Guided Remote Sensing Image Synthesis Network for Ship Detection | [Paper](https://doi.org/10.1109/tgrs.2023.3248106) | — | [Source](docs/literature-sources.md#r120) |
| 2022 | IEEE TGRS | Radiative / atmospheric / spectral physics | Physics-Informed Hyperspectral Remote Sensing Image Synthesis With Deep Conditional Generative Adversarial Networks | [Paper](https://doi.org/10.1109/tgrs.2022.3173532) | — | [Source](docs/literature-sources.md#r121) |
| 2017 | IEEE JSTARS | Radiative / atmospheric / spectral physics | DIRSIG5: Next-Generation Remote Sensing Data and Image Simulation Framework | [Paper](https://doi.org/10.1109/jstars.2017.2758964) | — | [Source](docs/literature-sources.md#r122) |

<a id="supporting-literature"></a>
## 📎 Supporting and Related Literature

Comparators and related 3D work are kept for scope context rather than promoted to core generators. Observation-driven supplementary records retain their original source-subclass assignments.

<a id="observation-supplementary"></a>
### Observation-Driven Supplementary and Pending Records

[119 supplementary and 6 venue-scope-pending papers](docs/observation-supplementary.md) remain available with their original paper/code/source links. They are not included in the 81-paper observation-driven core. A venue decision is not a judgment that an individual paper lacks research value.

<a id="comparators"></a>
### Restoration and Enhancement Comparators

These nine existing records have no generation subclass assigned in the source table. They remain available as restoration/enhancement context rather than being inferred to be generative from their titles.

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | IEEE TGRS | Restoration and Reconstruction | DSCH-Net: Diffusion-State-Contextual Hybrid Network for Physics-Inspired and Direction-Aware Dehazing of Remote Sensing Imagery | [Paper](https://doi.org/10.1109/tgrs.2026.3685508) | — | [Source](docs/literature-sources.md#r3) |
| 2026 | IEEE JSTARS | Restoration and Reconstruction | Synthetic Abundance Maps for Unsupervised Super-Resolution of Hyperspectral Remote Sensing Images | [Paper](https://doi.org/10.1109/jstars.2026.3682469) | — | [Source](docs/literature-sources.md#r9) |
| 2025 | ICCV | Restoration and Reconstruction | Hipandas: Hyperspectral Image Joint Denoising and Super-Resolution by Image Fusion with the Panchromatic Image | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Xu_Hipandas_Hyperspectral_Image_Joint_Denoising_and_Super-Resolution_by_Image_Fusion_ICCV_2025_paper.html) | — | [Source](docs/literature-sources.md#r14) |
| 2025 | IEEE JSTARS | Restoration and Reconstruction | Winscaleformer: Diffusion-Attention-Based Single Remote Sensing Image Dehazing | [Paper](https://doi.org/10.1109/jstars.2025.3623240) | — | [Source](docs/literature-sources.md#r19) |
| 2024 | Remote Sensing | Restoration and Reconstruction | Activated Sparsely Sub-Pixel Transformer for Remote Sensing Image Super-Resolution | [Paper](https://doi.org/10.3390/rs16111895) | — | [Source](docs/literature-sources.md#r20) |
| 2024 | arXiv | Restoration and Reconstruction | Cross-sensor Super-resolution of Irregularly Sampled Sentinel-2 Time Series | [Paper](https://arxiv.org/abs/2404.16409) | — | [Source](docs/literature-sources.md#r21) |
| 2023 | ICCV | Restoration and Reconstruction | ESSAformer: Efficient Transformer for Hyperspectral Image Super-resolution | [Paper](https://arxiv.org/abs/2307.14010) | — | [Source](docs/literature-sources.md#r25) |
| 2023 | CVPR | Restoration and Reconstruction | Toward Stable, Interpretable, and Lightweight Hyperspectral Super-Resolution | [Paper](https://doi.org/10.1109/CVPR52729.2023.02133) | — | [Source](docs/literature-sources.md#r26) |
| 2022 | IEEE TGRS | Restoration and Reconstruction | Permutation Invariance and Uncertainty in Multitemporal Image Super-Resolution | [Paper](https://doi.org/10.1109/tgrs.2021.3130673) | — | [Source](docs/literature-sources.md#r28) |

<a id="related-3d"></a>
### Related 3D Generation and View Synthesis

Adjacent work whose principal output is a 3D asset or ground-view product is kept separate from remote-sensing-view image generation.

| Year | Venue | Keywords | Name | Paper | Code | More |
| :---: | :---: | --- | --- | :---: | :---: | :---: |
| 2026 | arXiv | Related 3D Generation and View Synthesis | MetaEarth3D: Unlocking World-Scale 3D Generation With Spatially Scalable Generative Modeling | [Paper](https://arxiv.org/abs/2604.22828) | — | [Source](docs/literature-sources.md#r6) |
| 2025 | CVPR | Related 3D Generation and View Synthesis | AerialMegaDepth: Learning Aerial-Ground Reconstruction and View Synthesis | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Vuong_AerialMegaDepth_Learning_Aerial-Ground_Reconstruction_and_View_Synthesis_CVPR_2025_paper.html) | — | [Source](docs/literature-sources.md#r12) |
| 2025 | ICCV | Related 3D Generation and View Synthesis | MagicCity: Geometry-Aware 3D City Generation from Satellite Imagery with Multi-View Consistency | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Yao_MagicCity_Geometry-Aware_3D_City_Generation_from_Satellite_Imagery_with_Multi-View_ICCV_2025_paper.html) | — | [Source](docs/literature-sources.md#r15) |
| 2025 | ICCV | Related 3D Generation and View Synthesis | Sat2City: 3D City Generation from A Single Satellite Image with Cascaded Latent Diffusion | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Hua_Sat2City_3D_City_Generation_from_A_Single_Satellite_Image_with_ICCV_2025_paper.html) | — | [Source](docs/literature-sources.md#r17) |
| 2024 | CVPR | Related 3D Generation and View Synthesis | Sat2Scene: 3D Urban Scene Generation from Satellite Images with Diffusion | [Paper](https://doi.org/10.1109/cvpr52733.2024.00682) | — | [Source](docs/literature-sources.md#r23) |

<a id="surveys"></a>
## 📝 Surveys

Includes the directly relevant SAR-generative survey and broader remote-sensing foundation-model surveys for context.

| Year | Venue | Keywords | Name | Paper | Resources |
| :---: | :---: | --- | --- | :---: | :---: |
| 2025 | IEEE GRSM | Remote sensing foundation models; context | Foundation Models for Remote Sensing and Earth Observation: A Survey | [Paper](https://doi.org/10.1109/MGRS.2025.3576766) | [Source](docs/literature-sources.md#r13) |
| 2025 | IEEE GRSM | Remote sensing foundation models; context | Vision Foundation Models in Remote Sensing: A Survey | [Paper](https://doi.org/10.1109/MGRS.2025.3541952) | [Source](docs/literature-sources.md#r18) |
| 2024 | IEEE GRSM | SAR generative AI | Generative Artificial Intelligence Meets Synthetic Aperture Radar: A Survey | [Paper](https://doi.org/10.1109/mgrs.2024.3483459) | [Source](docs/literature-sources.md#r22) |

<a id="resources"></a>
## 🔗 Awesome Lists and Resources

The following are workflow or supporting-context resources, not standalone image generators.

| Year | Venue | Role | Name | Paper | More |
| :---: | :---: | --- | --- | :---: | :---: |
| 2026 | arXiv | SAR augmentation workflow | A Task-Driven and Quality-Assured Agent Framework for SAR Data Generation | [Paper](https://arxiv.org/abs/2606.28896) | [Source](docs/literature-sources.md#r2) |
| 2026 | IEEE GRSM (accepted; TechRxiv) | Remote sensing vision-language data guide; context | GeoChef: A Data-Centric Guide to Tailoring Vision-Language Models for Remote Sensing | [Paper](https://doi.org/10.36227/techrxiv.176978652.29736845/v1) | [Source](docs/literature-sources.md#r4) |
| 2026 | arXiv | Reflectance time-series reconstruction; context | HLS-GPT: A Generative Pretrained Transformer for Continental-Scale NASA Harmonized Landsat and Sentinel-2 Reflectance Reconstruction Across All Bands on Arbitrary Dates | [Paper](https://arxiv.org/abs/2606.18115) | [Source](docs/literature-sources.md#r5) |

- [VisionXLab/Awesome-RS-VL-Data](https://github.com/VisionXLab/Awesome-RS-VL-Data): reference repository and remote-sensing vision-language data resources.
- [Literature Sources and Import Notes](docs/literature-sources.md): provenance, import criteria, and deferred records.

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
