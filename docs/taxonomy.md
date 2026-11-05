# Taxonomy and Classification Notes

## Scope and Primary Assignment

The collection follows the survey's three-family, twelve-subclass input-output framework. The generated target is a remote-sensing-view or sensor-linked image product. Restoration and reconstruction remain normal in-scope tasks, not optional additions. A paper's backbone (GAN, diffusion, autoregressive, etc.) and downstream use do not determine its primary family.

1. **Condition-driven:** non-target-image controls specify scene content, arrangement, geography, or task-driven sampling.
2. **Observation-driven:** an existing measured observation anchors a translated, edited, restored, enhanced, or temporal image product.
3. **Image-formation-driven:** an operational renderer, simulator, acquisition variable, scattering, radiative, spectral, or sensor mechanism defines the principal generation relation.

For hybrids, record one primary source-to-target relation and retain other controls or mechanisms as secondary attributes. SAR-assisted optical cloud removal remains observation-driven restoration. Direct optical-to-SAR translation remains observation-driven when physics is auxiliary; a reconstruction-to-electromagnetic-simulation-to-SAR chain is formation-driven when the forward process defines the product. SAR output alone is not a formation criterion. Unconditional synthesis should be explicitly flagged as a boundary case rather than silently treated as text conditioning.

Detection, segmentation, change detection, mapping, disaster response, and augmentation are application tags. Task-oriented synthesis is a subclass only where task information enters generation, guidance, filtering, or sampling, not merely because generated images later train a detector.

## Twelve Subclasses

| Family | Subclass | Source field | Source-indexed records | README entries |
| --- | --- | --- | :---: | :---: |
| Condition-Driven Image Generation | [Text, Caption, and Foundation Generation](../README.md#text-to-image) | `text_caption_foundation_generation` | 24 | 24 |
| Condition-Driven Image Generation | [Layout, Mask, Object, and Semantic Control](../README.md#layout-conditioned) | `layout_mask_object_semantic_control` | 27 | 27 |
| Condition-Driven Image Generation | [Map, Vector, and Geospatial Metadata Control](../README.md#map-metadata) | `map_vector_geospatial_metadata_control` | 11 | 11 |
| Condition-Driven Image Generation | [Task-Oriented Synthesis](../README.md#data-synthesis) | `task_oriented_synthesis` | 9 | 9 |
| Observation-Driven Image Generation | [Cross-Modal and Cross-Sensor Translation](../README.md#cross-modal) | `cross_modal_cross_sensor_translation` | 83 | 31 |
| Observation-Driven Image Generation | [Image Editing, Restoration, and Completion](../README.md#reference-guided) | `image_editing_restoration_completion` | 49 | 20 |
| Observation-Driven Image Generation | [Spatial-Spectral Resolution Enhancement](../README.md#spatial-spectral) | `spatial_spectral_resolution_enhancement` | 66 | 43 |
| Observation-Driven Image Generation | [Temporal, Change, and Future Generation](../README.md#temporal) | `temporal_change_future_generation` | 28 | 12 |
| Image-Formation-Driven Generation | [Differentiable Rendering and Simulation](../README.md#rendering) | `differentiable_rendering_simulation` | 14 | 14 |
| Image-Formation-Driven Generation | [Geometry, View, and Acquisition Control](../README.md#geometry) | `geometry_view_acquisition_control` | 11 | 11 |
| Image-Formation-Driven Generation | [Scattering, Polarimetric, and Sensor Priors](../README.md#scattering) | `scattering_polarimetric_sensor_priors` | 13 | 13 |
| Image-Formation-Driven Generation | [Radiative, Atmospheric, and Spectral Physics](../README.md#spectral-physics) | `radiative_atmospheric_spectral_physics` | 7 | 7 |

## Counts and Source Records

Updated 2026-11-05. Counts below refer to the current listings. Removed and merged rows remain documented in the source index.

| Family | Main list | Supplementary / pending |
| --- | ---: | ---: |
| Condition-driven | 71 | 0 |
| Observation-driven | 106 | 120 |
| Image-formation-driven | 45 | 0 |

Source references distinguish the original workbook (`r`) from the supplementary workbook (`s2-r`). See [publication decisions](observation-screening.md) and [repository checks](observation-code-audit.md).

## Maintenance Rules

- Preserve the [source row](literature-sources.md#source-rows), original subclass, and verified publication status when moving an entry.
- Put spatiotemporal fusion under spatial-spectral enhancement when it reconstructs an enhanced observation; use temporal/change/future generation when the generated product itself represents a transition, future, or sequence. Existing source assignments are retained until a documented review resolves a conflict.
- Do not infer a generative diffusion model from the word “diffusion” in a title or an attention module. Comparators and uncertain cases require explicit role labeling.
- Keep papers sorted by descending year within each subclass. Keep one primary method entry per source record; a linked dataset view is allowed when the same paper supplies a dataset.
- Keep the three-family and twelve-subclass anchors stable. Legacy anchors such as `restoration`, `other-tasks`, and `physics` remain aliases; source anchors `r<number>` are unchanged.

## Evaluation by Relation

Condition-driven outputs need appearance plus condition/object/topology checks. Observation-driven outputs need source, spatial-spectral, modality, or temporal consistency as appropriate. Formation-driven outputs need mechanism-aware diagnostics and real-transfer checks. Detection/segmentation scores measure downstream utility under a stated model, split, and real-synthetic protocol; they do not replace intrinsic validity tests.
