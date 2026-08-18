---
title: Low-Cost Digital Droplet LAMP for Field-Deployable Nucleic Acid Detection
summary: A field-deployable digital droplet LAMP platform for absolute nucleic acid quantification, built on simple physically-generated emulsions instead of costly microfluidic chips and fluorinated surfactants.
date: 2026-08-18
---

**Research area:** Synthetic biology · droplet microfluidics · molecular diagnostics

## Overview

We are building a digital droplet loop-mediated isothermal amplification (ddLAMP) platform that delivers absolute nucleic acid quantification without thermocyclers, microfluidic chips, or fluorinated surfactant chemistry.

Digital assays work by partitioning a reaction into thousands of tiny compartments, each containing either zero or one target molecules. After amplification, each compartment reads out as simply positive or negative, and the fraction of positives gives the starting target concentration directly from Poisson statistics — no standard curve required. Combining this with LAMP, which amplifies DNA at a single constant temperature (60–65 °C) and tolerates crude, inhibitor-rich samples far better than PCR, gives a route to quantitative diagnostics that could run on a heat block in the field.

The obstacle is cost and complexity. Most published ddLAMP systems depend on custom microfluidic droplet generators and expensive fluorinated oils and surfactants, which puts them out of reach for low-resource and field settings. Our approach asks whether emulsions made by simple physical agitation — vortexing or pipette mixing — can support quantitative digital amplification. These droplets are polydisperse rather than monodisperse, but volume-weighted Poisson models offer a path to accurate quantification regardless, and this has not been systematically evaluated.

## Aims

1. **Establish a baseline droplet LAMP system** and characterise droplet interfacial chemistry across multiple water-in-oil formulations.
2. **Validate compartmentalisation** by quantifying molecular leakage and droplet coalescence under amplification conditions.
3. **Demonstrate quantitative ddLAMP detection** using plasmid DNA targets, assessing amplification efficiency and system biocompatibility.
4. **Test robustness across sample complexity**, from plasmid DNA through genomic DNA to inhibitor-rich crude extracts.

## Approach

**Droplet generation and characterisation.** Water-in-oil emulsions are produced by vortexing or pipette agitation and screened across oil–stabiliser combinations spanning mineral oil with phospholipids, silicone oil with polymeric surfactants, and fluorinated oil with Krytox/Jeffamine systems. Size distributions and polydispersity are measured by fluorescence microscopy, with image processing in Fiji/ImageJ and custom Python analysis.

**Thermal stability and isolation.** Candidate systems are held at 65 °C for the duration of a LAMP reaction and compared before and after to quantify coalescence and evaporation. Leakage assays using fluorescent dyes and labelled nucleic acids establish whether compartments remain molecularly isolated during incubation — the requirement that ultimately sets the false-positive floor of any digital assay.

**Compartmentalised amplification and readout.** Optimised droplet systems host LAMP reactions read by fluorescent nucleic acid dyes. Droplets are segmented and classified positive or negative by intensity threshold, with measured diameters feeding volume-corrected Poisson models to recover target concentration. Bulk reactions, positive controls and no-template controls run alongside throughout.

**Assay specificity.** A parallel strand of the work addresses LAMP's well-documented tendency toward target-independent amplification from primer interactions — a problem that becomes acute in a digital format, where an empty droplet that lights up is indistinguishable from a true positive. We are evaluating primer set design, reaction conditions, and sequence-specific readout chemistries that keep non-specific product dark.

## Why it matters

If polydisperse, physically generated emulsions can support quantitative digital amplification, the entry cost of digital nucleic acid testing drops by orders of magnitude. That opens absolute quantification to environmental monitoring, agricultural biosecurity, and clinical settings where a microfluidics facility is not an option.

## People

- **Dr Alexander Mason** — DECRA Fellow, project lead
- **Dr Dezerae Cox** — co-supervisor
- **Jessica Prescott** — Honours student (2026)

## Facilities

Work is carried out in PC2 laboratories at the University of Wollongong, using confocal and THUNDER fluorescence microscopy for droplet imaging, with quantitative analysis in LAS X, Fiji/ImageJ and Python.

---

*Interested in collaborating or joining the group? [Get in touch.](/contact/)*
