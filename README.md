# Cross-species gray-matter atlas spanning rodents, nonhuman primates, and humans.

<img width="800" alt="image" src="https://github.com/user-attachments/assets/f301eaf9-6758-41d5-b551-4680049477c8" />


## Overview

The Common Hierarchical Atlas (CHA) provides a unified anatomical framework for cortical and subcortical gray-matter parcellation across multiple species. It was developed to support cross-species comparison in translational neuroscience by harmonizing homologous regions within a consistent hierarchical coordinate system. :contentReference[oaicite:1]{index=1}

The atlas is organized using species-specific minimal deformation templates (MDTs) and a common parcellation framework built on consistent tissue segmentation and literature-guided anatomical homologies. Primary species include:

- Human
- Rhesus macaque
- Marmoset
- Mouse

Rat coverage is also provided through atlas transfer from mouse using MRI-based alignment. 

## Key Features

- Population-based MDT reference spaces
- Cross-species consistent cortical and subcortical parcellation
- Hierarchical atlas design with multiple anatomical levels
- Harmonized regional definitions across rodents and primates
- Validation against species-specific atlases
- Freely available NIfTI atlas files for each species 

## Hierarchy

The CHA atlas is organized into three levels:

### Level 0: Tissue Compartments
Level 0 defines major tissue classes derived from automated MRI segmentation:

- Gray matter (GM)
- White matter (WM)
- Deep gray matter (DGM)
- Cerebellum (CBL)
- Cerebrospinal fluid (CSF)

These compartment maps form the anatomical foundation for higher-level parcellations. :contentReference[oaicite:4]{index=4}

### Level 1: Macro-Regions
Level 1 defines nine major cortical and subcortical divisions:

- Frontal (FRO)
- Parietal (PAR)
- Temporal (TEM)
- Occipital (OCC)
- Insular (INS)
- Cingulate (CIN)
- Olfactory (OLF)
- Basal ganglia (BG)
- Thalamic / hypothalamic system (THL)

These macro-regions are defined using consistent anatomical landmarks while allowing species-specific anatomical variation. :contentReference[oaicite:5]{index=5}

### Level 2: Subdivisions
Level 2 provides finer anatomical parcels. There are:

- 26 Level-2 regions in primates
- 21 Level-2 regions in rodents

Some regions remain undivided in rodents due to anatomical differences or MRI segmentation limitations, including:

- Parietal lobe (PAR)
- Caudoputamen (CPu)

## Included Level-2 Regions

### Frontal
- FRO_Precentral (PreC)
- FRO_Premotor (PreM)
- FRO_Prefrontal (PreF)

### Parietal
- PAR

### Temporal
- TEM_Superior (TemS)
- TEM_Inferior (TemI)
- TEM_Medial (TemM)
- TEM_Hippocampus (Hipp)
- TEM_Amygdala (Amyg)

### Occipital
- OCC_Lateral (OccL)
- OCC_Medial (OccM)

### Insula
- INS_Anterior (InsA)
- INS_Posterior (InsP)

### Cingulate
- CIN_Anterior (CingA)
- CIN_Posterior (CingP)

### Olfactory
- OLF_Anterior (OlfA)
- OLF_Piriform (Pir)

### Basal Ganglia
- BG_CaudoPutamen (CPu)
- BG_Accumbens (NAc)
- BG_Pallidum (Pal)

### Thalamic / Hypothalamic
- THL_Thalamus (Thal)
- THL_Hypothalamus (Hypo)



## Excluded Structures

The following structures were not included because reliable cross-species MRI segmentation was not feasible:

- Claustrum
- Substantia nigra
- Subthalamic nuclei

These exclusions reflect either MRI contrast limitations or lack of sufficiently consistent boundaries across species. 

## Coordinate Space and Templates

All atlas labels are defined in species-specific MDT spaces. Except for the human template, each MDT was generated specifically for this framework and aligned to the AC-PC axis with the origin set at the anterior commissure (AC). :contentReference[oaicite:9]{index=9}

### Species Templates
- **Human**: ICBM152 Nonlinear Asymmetrical 2009a template
- **Rhesus macaque**: MDT generated from PRIME-DE T1-weighted MRI
- **Marmoset**: Brain/MINDS / MBM-derived reference with AC-centered coordinate adjustment
- **Mouse**: High-resolution diffusion MRI MDT
- **Rat**: MDT generated from ex vivo diffusion MRI and aligned to the common framework

:contentReference[oaicite:10]{index=10}

## Construction Principles

Because cross-species homology is not always uniquely defined, the atlas prioritized three design principles:

1. Preserve regional definitions widely used in existing atlases
2. Maximize cross-species consistency where boundaries can be reasonably identified in MRI
3. Retain functional interpretability

In some cases, functionally meaningful groupings were favored over finer species-specific distinctions. For example:

- Superior and middle temporal gyri were grouped into a single superior temporal parcel for cross-species consistency
- Frontal subdivisions lacking clear homologues across species were not retained separately
- Olfactory parcels were preserved because of their importance in rodent and marmoset neurobiology

:contentReference[oaicite:11]{index=11}

## Source Atlases Used

Level-2 homologies were defined with support from one or more established atlases, including:

- FreeSurferSeg (human)
- Brodmann areas (human)
- Allen Brain Atlas (mouse)
- CIVM atlas (rhesus macaque)
- Inia19 / NeuroMaps (rhesus macaque)
- Brain/MINDS atlas (marmoset)
- MBM atlas (marmoset)
- Paxinos atlas (marmoset)

When multiple references were available, boundaries were cross-validated across atlases. 

## File Availability

Atlas files are available for each species as:

```text
<species>_CHA.nii.gz
