# NASA data acquisition record

## Downloaded source

`raw/OSD-267_metadata_OSD-267-ISA.zip` and its unpacked contents are the official metadata archive for **NASA OSDR OSD-267 / VEG-01A**.

- Study: *Microbiological and nutritional analysis of lettuce crops grown on the ISS — VEG-01A*
- Crop: `Lactuca sativa` cv. `Outredgeous` red romaine lettuce
- Comparison: ISS spaceflight samples and ground-control samples
- Source: <https://osdr.nasa.gov/bio/repo/data/studies/OSD-267>
- DOI: `10.26030/0cpc-g985`
- Downloaded: 2026-08-19

The metadata gives real experimental context suitable for scenario presets, including: Veggie plant-pillow hardware, growth medium blend, LED source, 16:8 photoperiod, 200 µmol m⁻² s⁻¹ light intensity, 23.25 °C mean growth temperature, and 33-day harvest age.

## Important limitation

OSD-267 is a microbiome/nutrition dataset. Its 1.32 GB raw archive is primarily sequencing data; the downloaded metadata does **not** include per-plant fresh biomass or root geometry. It must not be used to claim that the simulator's yield values were fitted to NASA measurements.

`raw/OSD-780_files.json` records the file inventory for a second official NASA Veggie study, **OSD-780 / VEG-04A and VEG-04B**. Its study description reports weighed harvests, but its currently listed public analytical files are microbial plate-count data and metadata, not a public biomass table.

## Next valid calibration data

For a calibrated yield model, obtain a table containing per-plant or per-pillow fresh mass along with growth duration, gravity/flight condition, crop, and treatment. This may require extracting values from the associated peer-reviewed Veggie publications or contacting the OSDR study team. Until then, retain the app's `physics-inspired estimate` label.

## Usable calibration reference added

`processed/veg04a_mizuna_aggregate_biomass.csv` is a compact, citable dataset transcribed from the biomass-production results of Bunchek et al. (2024), DOI `10.1080/17429145.2023.2292220`. It contains the four published VEG-04A aggregate fresh-edible-biomass observations at 35 days after initiation:

| Condition | Light treatment | Surviving plants | Total fresh edible biomass |
| --- | --- | ---: | ---: |
| ISS flight | red-rich | 5 | 293 g |
| ISS flight | blue-rich | 3 | 97 g |
| Ground control | red-rich | 3 | 141 g |
| Ground control | blue-rich | 3 | 121 g |

This is real published experimental data. It is **mizuna**, contains only four aggregate observations, and has lighting/survival confounding; it is therefore a validation/reference set for an ISS-mizuna scenario, not enough data to train a general crop-yield model or replace the simulator's lettuce estimates.
