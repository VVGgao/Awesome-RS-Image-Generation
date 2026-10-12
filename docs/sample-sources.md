# Sample Sources

这 8 篇示例论文来自用户提供的 `all_investigated_literature.xlsx`，工作表为 `All Literature`。下表行号是 Excel 实际行号，第 1 行为字段名。

本次只选取原表中 `active_reference = true`、`representative_method = true` 的部分条目，不导入完整文献库，不上传原 Excel，也不修改原文件。

| Sample | Excel row | master_id | Original subclass |
| --- | :---: | --- | --- |
| <a id="text2earth"></a>Text2Earth | 89 | `paper:P00001` | `text_caption_foundation_generation` |
| <a id="aerogen"></a>AeroGen | 44 | `paper:P00003` | `layout_mask_object_semantic_control` |
| <a id="diffusionsat"></a>DiffusionSat | 68 | `paper:P00014` | `map_vector_geospatial_metadata_control` |
| <a id="changeanywhere"></a>ChangeAnywhere | 77 | `paper:P01119` | `task_oriented_synthesis` |
| <a id="terramind"></a>TerraMind | 155 | `paper:P01049` | `cross_modal_cross_sensor_translation` |
| <a id="s2o-npde"></a>SAR-to-Optical via Neural PDE | 186 | `paper:P00589` | `cross_modal_cross_sensor_translation` |
| <a id="hir-diff"></a>HIR-Diff | 277 | `paper:P00023` | `spatial_spectral_resolution_enhancement` |
| <a id="unmixdiff"></a>UnmixDiff | 118 | `paper:P03444` | `radiative_atmospheric_spectral_physics` |

## Field Mapping

- `year` → README 的 Year；会议论文使用正式会议年份，预印本使用所列预印本年份。
- `venue_name` → Venue，使用 IEEE GRSM、IEEE TGRS、CVPR、ICLR、ICCV、IJCAI 等简称。
- `title` → Name，去除 BibTeX 大括号等格式标记，不改变论文身份。
- `url` / `doi` → Paper，优先链接到具体论文页面而不是网站首页。
- Keywords 是根据原表分类及论文／作者页面整理的简短描述，不是原表的直接字段。
- Code 链接由论文或作者项目页面补充。未确认的链接用 `—`，不表示确定不存在代码。
- More 链接到本表的来源行，不创建占位 Issue。

## Checks and Corrections

- **DiffusionSat**：原表同时列出 `year = 2023` 和 `venue_name = ICLR`。2023 是预印本首次提交年份；README 使用正式会议年份 **ICLR 2024**。[论文页面](https://arxiv.org/abs/2312.03606)及[作者代码仓库](https://github.com/samar-khanna/DiffusionSat)均注明 ICLR 2024。
- **TerraMind**：原表链接为 CVF 首页。README 改用 [ICCV 2025 具体论文页面](https://openaccess.thecvf.com/content/ICCV2025/html/Jakubik_TerraMind_Large-Scale_Generative_Multimodality_for_Earth_Observation_ICCV_2025_paper.html)，代码对应 [IBM/terramind](https://github.com/IBM/terramind)。
- **AeroGen**：使用 [CVPR 2025 具体论文页面](https://openaccess.thecvf.com/content/CVPR2025/html/Tang_AeroGen_Enhancing_Remote_Sensing_Object_Detection_with_Diffusion-Driven_Data_Generation_CVPR_2025_paper.html)和[作者仓库](https://github.com/Sonettoo/AeroGen)，而非根据仓库预印本 BibTeX 把会议年份写成 2024。
- **Text2Earth**：2025 年和 IEEE GRSM 对应[作者项目仓库](https://github.com/Chen-Yang-Liu/Text2Earth)中的期刊信息；Paper 保留原表 DOI。
- **ChangeAnywhere**：按[所列论文版本](https://arxiv.org/abs/2404.08892)标为 arXiv 2024。[作者仓库](https://github.com/tangkai-RS/ChangeAnywhere)提供资源入口，但仍列有生成训练代码发布事项，故 README 使用 Repository 而不声称完整生成代码已发布。
- **SAR-to-Optical via Neural PDE**：论文链接对应 [IJCAI 2022 原始页面](https://www.ijcai.org/proceedings/2022/229)；未补入未经确认的代码地址。
- **HIR-Diff**：会议与方法描述对应 [CVPR 2024 论文页面](https://openaccess.thecvf.com/content/CVPR2024/html/Pang_HIR-Diff_Unsupervised_Hyperspectral_Image_Restoration_Via_Improved_Diffusion_Models_CVPR_2024_paper.html)及[作者仓库](https://github.com/LiPang/HIRDiff)。仅作为可选恢复分类的示例，不据此确定最终综述范围。
- **UnmixDiff**：题名及 DOI 对应[作者实现仓库](https://github.com/yuyang95/UnmixingDM)中的引用信息；暂放 Other Generation Tasks，保留原表的物理／光谱分类供后续细分。

这些示例不构成完整收录、排名或方法推荐。数据集、评测与参考引导生成等未填栏目继续保留原占位。
