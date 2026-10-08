# Orbital Grove — Microgravity Simulator

A self-contained interactive prototype for modelling seed growth in orbital and partial-gravity environments.

## Run it

Open `index.html` in any modern browser.

No install, build step, backend, or account is required.

## What works

- Crop, medium, moisture, nutrient-density, gravity, and growth-day controls
- Animated root architecture using a deterministic biased random-walk model
- Diffusion-field / nutrient-density visualisation
- Live viability, biomass, root surface area, nutrient-exposure, and Earth-control comparison
- Downloadable JSON study report
- Local access controls:
  - Viewer can explore
  - Researcher can run/export
  - Principal Investigator can configure
- Access configuration is stored only in browser local storage

## Model framing

This is an educational, physics-inspired parametric simulator — not a validated crop-yield predictor.

It models reduced gravity as a weaker downward directional bias and treats near-zero-gravity nutrient transport as diffusion-dominant, consistent with the project brief.

## Real NASA reference data

See `data/README.md` for the acquired NASA OSDR metadata and a citable, four-observation ISS/ground fresh-biomass reference dataset from the VEG-04A mizuna experiment.

The application is deliberately still labelled **physics-inspired** because those observations are not sufficient to train or validate its general yield estimate.
