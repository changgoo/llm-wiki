---
type: synthesis
status: active
created: 2026-05-14
updated: 2026-05-14
sources:
  - wiki/sources/mypapers-bibliography.md
tags:
  - astrophysics
  - ingest-plan
  - publications
---

# Publication Ingest Plan

## Strategy

Ingest the publication corpus in topic batches after PDF paths are provided. For each PDF, first create a `.txt` companion with `pdftotext -layout` in the same source directory, then ingest from text while consulting the PDF only for figures, tables, layout-sensitive material, and metadata.

Each batch should produce one batch synthesis page, update source pages for individual papers, and strengthen shared concept pages. Target 5-10 full papers per working pass; split larger batches if the individual papers are dense.

## Batch 0: Bibliography Map

Status: complete at metadata level.

Outputs:

- [[mypapers-bibliography]]
- [[publication-map]]
- this ingest plan

## Full-Text Batches

### Batch 1: Core ISM And TIGRESS Foundations

Papers: 12.
Purpose: establish the core pages for multiphase ISM dynamics, TIGRESS, vertical equilibrium, turbulence, and star formation regulation.

Initial source list:

- `2006ApJ...649L..13K` (2006) - Interstellar Turbulence Driving by Galactic Spiral Shocks
- `2008ApJ...681.1148K` (2008) - Galactic Spiral Shocks with Thermal Instability
- `2010ApJ...720.1454K` (2010) - Galactic Spiral Shocks with Thermal Instability in Vertically Stratified Galactic Disks
- `2011ApJ...743...25K` (2011) - Regulation of Star Formation Rates in Multiphase Galactic Disks: Numerical Tests of the Thermal/Dynamical Equilibrium Model
- `2013ApJ...776....1K` (2013) - Three-dimensional Hydrodynamic Simulations of Multiphase Galactic Disks with Star Formation Feedback. I. Regulation of Star Formation Rates
- `2013ApJ...778...88K` (2013) - Long-term Evolution of Decaying Magnetohydrodynamic Turbulence in the Multiphase Interstellar Medium
- `2015ApJ...815...67K` (2015) - Vertical Equilibrium, Energetics, and Star Formation Rates in Magnetized Galactic Disks Regulated by Momentum Feedback from Supernovae
- `2017ApJ...846..133K` (2017) - Three-phase Interstellar Medium in Galaxies Resolving Evolution with Star Formation and Supernova Feedback (TIGRESS): Algorithms, Fiducial Model, and Convergence
- `2018ApJ...853..173K` (2018) - Numerical Simulations of Multiphase Winds and Fountains from Star-forming Galactic Disks. I. Solar Neighborhood TIGRESS Model
- `2020ApJ...898...35K` (2020) - Local Simulations of Spiral Galaxies with the TIGRESS Framework. I. Star Formation and Arm Spurs/Feathers
- `2020ApJ...898...52M` (2020) - Cloud Properties and Correlations with Star Formation in Self-consistent Simulations of the Multiphase ISM
- `2024ApJ...975..113J` (2024) - Learning the Universe: GalactISM Simulations of Resolved Star Formation and Galactic Outflows across Main-sequence and Quenched Galactic Environments

### Batch 2: Supernovae, Bubbles, And Feedback Coupling

Papers: 12.
Purpose: build the feedback-coupling layer around supernova remnants, superbubbles, stellar wind bubbles, and momentum/energy injection.

Initial source list:

- `2015ApJ...802...99K` (2015) - Momentum Injection by Supernovae in the Interstellar Medium
- `2017ApJ...834...25K` (2017) - Superbubbles in the Multiphase ISM and the Loading of Galactic Winds
- `2019MNRAS.490.1961E` (2019) - Evolution of supernovae-driven superbubbles with conduction and cooling
- `2020ApJ...905...35K` (2020) - Radiative Supernova Remnants and Supernova Feedback
- `2021ApJ...914...89L` (2021) - Efficiently Cooled Stellar Wind Bubbles in Turbulent Clouds. I. Fractal Theory and Application to Star-forming Clouds
- `2021ApJ...914...90L` (2021) - Efficiently Cooled Stellar Wind Bubbles in Turbulent Clouds. II. Validation of Theory with Hydrodynamic Simulations
- `2021ApJ...922L...3L` (2021) - Star Formation Regulation and Self-pollution by Stellar Wind Feedback
- `2024ApJ...970...18L` (2024) - Geometry, Dissipation, Cooling, and the Dynamical Evolution of Wind-blown Bubbles
- `2025ApJ...989...42L` (2025) - The Coevolution of Stellar Wind-blown Bubbles and Photoionized Gas. I. Physical Principles and a Semianalytic Model
- `2025ApJ...989...43L` (2025) - The Coevolution of Stellar Wind-blown Bubbles and Photoionized Gas. II. 3D RMHD Simulations and Tests of Semianalytic Models
- `2025ApJ...990...49G` (2025) - Evolution of Supernova Remnants in a Cloudy Multiphase Interstellar Medium
- `2026ApJ..1000...70S` (2026) - Where Do Stars Explode in the ISM? - The Distribution of Dense Gas around Evolved Massive Stars in M33

### Batch 3: Radiation, Chemistry, And Star Formation Models

Papers: 13.
Purpose: connect radiation transfer, chemistry, heating/cooling, metallicity, and pressure-regulated star formation models.

Initial source list:

- `2017MNRAS.465..885S` (2017) - Chemistry and radiative shielding in star-forming galactic discs
- `2018ApJ...858...16G` (2018) - The X_CO Conversion Factor from Galactic Multiphase ISM Simulations
- `2020ApJ...897..143K` (2020) - Diffuse Ionized Gas in Simulations of Multiphase, Star-forming Galactic Disks
- `2020ApJ...903..142G` (2020) - The Environmental Dependence of the X_CO Conversion Factor
- `2020ApJS..250....9S` (2020) - Lyalpha Radiative Transfer: Monte Carlo Simulation of the Wouthuysen-Field Effect
- `2022ApJ...936..137O` (2022) - Pressure-regulated, Feedback-modulated Star Formation in Disk Galaxies
- `2023ApJ...946....3K` (2023) - Introducing TIGRESS-NCR. I. Coregulation of the Multiphase Interstellar Medium and Star Formation Rates
- `2023ApJS..264...10K` (2023) - Photochemistry and Heating/Cooling of the Multiphase Interstellar Medium with UV Radiative Transfer for Magnetohydrodynamic Simulations
- `2023ApJS..268...42G` (2023) - Implementation of Chemistry in the Athena++ Code
- `2024ApJ...972...67K` (2024) - Metallicity Dependence of Pressure-regulated Feedback-modulated Star Formation in the TIGRESS-NCR Simulation Suite
- `2024ApJ...975..151H` (2024) - Toward Implementation of the Pressure-regulated, Feedback-modulated Model of Star Formation in Cosmological Simulations: Methods and Application to TNG
- `2024ApJ...975..173L` (2024) - Ultraviolet Radiation Fields in Star-forming Disk Galaxies: Numerical Simulations with TIGRESS-NCR
- `2025MNRAS.544.1390B` (2025) - Applying a star formation model calibrated on high-resolution interstellar medium simulations to cosmological simulations of galaxy formation

### Batch 4: Galactic Winds, CGM, And Baryon Cycling

Papers: 12.
Purpose: connect local feedback physics to multiphase outflows, ARKENSTONE, SMAUG, CGM structure, and baryon cycling.

Initial source list:

- `2020ApJ...894...12V` (2020) - Kinematics and Dynamics of Multiphase Outflows in Simulations of the Star-forming Galactic Interstellar Medium
- `2020ApJ...900...61K` (2020) - First Results from SMAUG: Characterization of Multiphase Galactic Outflows from a Suite of Local Star-forming Galactic Disk Simulations
- `2020ApJ...903...32F` (2020) - First Results from SMAUG: Uncovering the Origin of the Multiphase Circumgalactic Medium with a Comparative Analysis of Idealized and Cosmological Simulations
- `2020ApJ...903L..34K` (2020) - A Framework for Multiphase Galactic Wind Launching Using TIGRESS
- `2020ApJ...905....4P` (2020) - First Results from SMAUG: The Need for Preventative Stellar Feedback and Improved Baryon Cycling in Semianalytic Models of Galaxy Formation
- `2021MNRAS.508.2979P` (2021) - Characterizing mass, momentum, energy, and metal outflow rates of multiphase galactic winds in the FIRE-2 cosmological simulations
- `2024ApJ...960..100S` (2024) - The Structure and Composition of Multiphase Galactic Winds in a Large Magellanic Cloud Mass Simulated Galaxy
- `2024MNRAS.527.1216S` (2024) - ARKENSTONE - I. A novel method for robustly capturing high specific energy outflows in cosmological simulations
- `2024MNRAS.535.3550S` (2024) - ARKENSTONE - II. A model for unresolved cool clouds entrained in galactic winds in cosmological simulations
- `2025ApJ...991...16S` (2025) - Pumping Iron: How Turbulent Metal Diffusion Impacts Multiphase Galactic Outflows
- `2025MNRAS.543.1456B` (2025) - Prevention is better than cure? Feedback from high specific energy winds in cosmological simulations with ARKENSTONE
- `2026MNRAS.547ag374B` (2026) - Correction to: Prevention is better than cure? Feedback from high specific energy winds in cosmological simulations with ARKENSTONE

### Batch 5: Cosmic Rays And Nonthermal Processes

Papers: 3.
Purpose: deepen the cosmic ray and nonthermal branch seeded by the existing cosmic ray feedback review.

Initial source list:

- `2024ApJ...964...99A` (2024) - Cosmic-Ray Acceleration of Galactic Outflows in Multiphase Gas
- `2024ApJ...974..201D` (2024) - Nonthermal Signatures of Radiative Supernova Remnants
- `2025ApJ...994...45H` (2025) - Dynamically Controlled Transport of GeV Cosmic Rays in Diverse Galactic Environments

### Batch 6: Observational ISM Diagnostics And Surveys

Papers: 10.
Purpose: build the observation-facing layer for H I, CNM, CO, dust polarization, radio continuum, and Local Group surveys.

Initial source list:

- `2014ApJ...786...64K` (2014) - Three-dimensional Hydrodynamic Simulations of Multiphase Galactic Disks with Star Formation Feedback. II. Synthetic H I 21 cm Line Observations
- `2017ApJ...837...55M` (2017) - Recovering Interstellar Gas Properties with Hi Spectral Lines: A Comparison between Synthetic Spectra and 21-SPONGE
- `2018ApJS..238...14M` (2018) - The 21-SPONGE H I Absorption Line Survey. I. The Temperature of Galactic H I
- `2019ApJ...880..106K` (2019) - Dust Polarization Maps from TIGRESS: E/B Power Asymmetry and TE Correlation
- `2020ApJ...899...15M` (2020) - Extracting the Cold Neutral Medium from H I Emission with Deep Learning: Implications for Galactic Foregrounds at High Latitude
- `2021ApJ...919...53C` (2021) - The Origin of Parity Violation in Polarized Dust Emission and Implications for Cosmic Birefringence
- `2024ApJ...974...93P` (2024) - The Local Group L-band Survey: The First Measurements of Localized Cold Neutral Medium Properties in the Low-metallicity Dwarf Galaxy NGC 6822
- `2025ApJS..279...35K` (2025) - The Karl G. Jansky Very Large Array Local Group L-Band Survey (LGLBS)
- `2026ApJ...997...50P` (2026) - A High-resolution Study of the Cold Neutral Medium in and around 30 Doradus
- `2026ApJ...997..328S` (2026) - The Local Group L-band Survey: Probing Cold Atomic Gas in IC 10 with Neutral Hydrogen Absorption

### Batch 7: Galaxy Environments And Special Systems

Papers: 10.
Purpose: file system-specific applications such as ram pressure, nuclear rings, UDGs, disk potentials, and SMBH accretion without overloading the core theory pages.

Initial source list:

- `2021ApJ...914....9M` (2021) - Star Formation in Nuclear Rings with the TIGRESS Framework
- `2022ApJ...925...99M` (2022) - Effects of Varying Mass Inflows on Star Formation in Nuclear Rings of Barred Galaxies
- `2022ApJ...926..139M` (2022) - First Results from SMAUG: Insights into Star Formation Conditions from Spatially Resolved ISM Properties in TNG50
- `2022ApJ...936..133C` (2022) - Ram Pressure Stripping of the Multiphase ISM: A Detailed View from TIGRESS Simulations
- `2022ApJ...939..101K` (2022) - Ultra-diffuse Galaxies as Extreme Star-forming Environments. II. Star Formation and Pressure Balance in H I-rich UDGs
- `2023ApJ...946...26G` (2023) - Toward Horizon-scale Accretion onto Supermassive Black Holes in Elliptical Galaxies
- `2023ApJ...946..114M` (2023) - Effects of Magnetic Fields on Gas Dynamics and Star Formation in Nuclear Rings
- `2024ApJ...973..141G` (2024) - Magnetized Accretion onto and Feedback from Supermassive Black Holes in Elliptical Galaxies
- `2025ApJ...989...66V` (2025) - Modeling the Mass Distribution and Gravitational Potential of Nearby Disk Galaxies: Implications for the Interstellar Medium Dynamical Equilibrium
- `2026ApJ...999..116C` (2026) - The Impact of Ram Pressure on the Radio Spectral Index and Magnetic Field of NGC 4522: A High-resolution VLA Continuum Study

## Per-Batch Workflow

1. Confirm PDF paths for the batch.
2. Generate `.txt` companions with `pdftotext -layout`.
3. Create or update one source page per paper.
4. Update existing concept pages before creating new ones.
5. Create one batch synthesis page summarizing what the batch changes about the wiki.
6. Update [[publication-map]], [[index]], [[overview]], and [[log]].
7. Commit after each completed batch.

## Quality Bar

A batch is complete when its source pages are linked, core claims are source-backed, contradictions or tensions are explicit, and the relevant concept pages can answer a future query without rereading every raw paper.
