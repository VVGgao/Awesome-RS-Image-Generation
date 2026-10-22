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
| Condition-Driven Image Generation | [Text, Caption, and Foundation Generation](../README.md#text-to-image) | `text_caption_foundation_generation` | 19 | 19 |
| Condition-Driven Image Generation | [Layout, Mask, Object, and Semantic Control](../README.md#layout-conditioned) | `layout_mask_object_semantic_control` | 23 | 23 |
| Condition-Driven Image Generation | [Map, Vector, and Geospatial Metadata Control](../README.md#map-metadata) | `map_vector_geospatial_metadata_control` | 12 | 12 |
| Condition-Driven Image Generation | [Task-Oriented Synthesis](../README.md#data-synthesis) | `task_oriented_synthesis` | 10 | 10 |
| Observation-Driven Image Generation | [Cross-Modal and Cross-Sensor Translation](../README.md#cross-modal) | `cross_modal_cross_sensor_translation` | 71 | 22 |
| Observation-Driven Image Generation | [Image Editing, Restoration, and Completion](../README.md#reference-guided) | `image_editing_restoration_completion` | 46 | 14 |
| Observation-Driven Image Generation | [Spatial-Spectral Resolution Enhancement](../README.md#spatial-spectral) | `spatial_spectral_resolution_enhancement` | 66 | 34 |
| Observation-Driven Image Generation | [Temporal, Change, and Future Generation](../README.md#temporal) | `temporal_change_future_generation` | 23 | 11 |
| Image-Formation-Driven Generation | [Differentiable Rendering and Simulation](../README.md#rendering) | `differentiable_rendering_simulation` | 12 | 12 |
| Image-Formation-Driven Generation | [Geometry, View, and Acquisition Control](../README.md#geometry) | `geometry_view_acquisition_control` | 9 | 9 |
| Image-Formation-Driven Generation | [Scattering, Polarimetric, and Sensor Priors](../README.md#scattering) | `scattering_polarimetric_sensor_priors` | 12 | 12 |
| Image-Formation-Driven Generation | [Radiative, Atmospheric, and Spectral Physics](../README.md#spectral-physics) | `radiative_atmospheric_spectral_physics` | 6 | 6 |

## Counts, Retention, and Evidence Limits

- The retained collection has **341 unique source records**, with **218 current README table entries** and **125 archived observation-driven entries** (343 total displays across the two files). Text2Earth/Git-10M and ChangeAnywhere/ChangeAnywhere-100K each appear in both method and dataset views.
- **309 records** retain one of the original twelve subclass assignments: **64 condition-driven**, **206 observation-driven**, and **39 image-formation-driven**. The current README lists **64 / 81 / 39** respectively: only the observation-driven family was venue-filtered, leaving 119 supplementary and 6 pending records in its [archive](observation-supplementary.md). The [screening record](observation-screening.md) gives the policy and publication evidence. These are indexing counts, not a fresh full-text-verified generative-method census and not the manuscript's 262-method subset.
- **9 restoration/enhancement comparators** without a source generation subclass and **5 related 3D works** are listed separately. They are retained, not deleted or silently promoted to core generators. Other dataset, metric, benchmark, survey, and workflow records keep their separate roles.
- Primary assignments retain the recorded source subclass. Original bibliographic metadata remains in the source index and archive; the observation-driven core uses the checked publication title, year, venue and paper URL. Existing code/data links are unchanged. Later full-text audits may refine boundaries without losing provenance.
- The original Excel remains unchanged and is not published. No manuscript PDF, internal full text, author details, or local source paths are added by this reorganization.

## Maintenance Rules

- Preserve the [source row](literature-sources.md#source-rows), original subclass, and verified publication status when moving an entry.
- Put spatiotemporal fusion under spatial-spectral enhancement when it reconstructs an enhanced observation; use temporal/change/future generation when the generated product itself represents a transition, future, or sequence. Existing source assignments are retained until a documented review resolves a conflict.
- Do not infer a generative diffusion model from the word “diffusion” in a title or an attention module. Comparators and uncertain cases require explicit role labeling.
- Keep papers sorted by descending year within each subclass. Keep one primary method entry per source record; a linked dataset view is allowed when the same paper supplies a dataset.
- Keep the three-family and twelve-subclass anchors stable. Legacy anchors such as `restoration`, `other-tasks`, and `physics` remain aliases; source anchors `r<number>` are unchanged.

## Evaluation by Relation

Condition-driven outputs need appearance plus condition/object/topology checks. Observation-driven outputs need source, spatial-spectral, modality, or temporal consistency as appropriate. Formation-driven outputs need mechanism-aware diagnostics and real-transfer checks. Detection/segmentation scores measure downstream utility under a stated model, split, and real-synthetic protocol; they do not replace intrinsic validity tests.
