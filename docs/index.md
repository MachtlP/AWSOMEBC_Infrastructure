# I. Home

<p class="updated">Last updated: 25 Nov 2026</p>

Technical documentation of the **snowpackbc** tool chain: AWSOME (Avalanche Warning Service Operational Model
Environment) set up for four western Canadian operations, run daily in AWS and published on
[snowpackbc.com](https://snowpackbc.com).

This site is for modellers and developers: what data comes in, which script does what, how SNOWPACK is configured,
and how the output is post-processed and checked against observations. To **read the dashboard**, see the
[AWSOME BC User Guide](https://machtlp.github.io/AWSOME_BC_Docs/).

## Pages

| Page | Content |
|---|---|
| [II. Tool Chain Overview](toolchain.md) | The whole chain on one flow chart, the infrastructure, the daily schedule |
| [III. Weather Input](weather-input.md) | HRDPS and station data: download, correction, SMET assembly, script by script |
| [IV. SNOWPACK](snowpack.md) | Model configuration: flavour, slopes, resume, output, indices |
| [V. xsnow](xsnow.md) | The xsnow dataset (`xsnowpack.zarr`): structure, variables, quirks |
| [VI. AvAPro](avapro.md) | Avalanche-problem detection from the simulated profiles (v2 method, v3 on xsnow) |
| [VII. Observations & Assessments](observations.md) | InfoEx assessments and observations, Avalanche Canada forecasts, validation design |

## Operations

| Operation | Bands (BTL · TL · ALP) | Semi-distributed | Fully gridded | Stations |
|---|---|---|---|---|
| Rogers Pass (Glacier NP) | 1500–2000 · 2000–2200 · 2200 m + | `rogers_hex` | `rogers_grid` (162 cells) | Fidelity |
| Mike Wiegele (MWHS) | 1500–2000 · 2000–2200 · 2200 m + | `mwhs_hex` | `mwhs_grid` (446 cells) | Mt St Anne |
| Whistler | 1300–1800 · 1800–2000 · 2000 m + | `whistler_hex` (7 hexagons) | `whistler_grid` (261 cells) | Whistler Rendezvous |
| Banff | 1700–2200 · 2200–2400 · 2400 m + | `banff_hex` | `banff_grid` (379 cells) | Bosworth lower, Bow Summit, Lookout |

## Links

- Dashboard: [snowpackbc.com](https://snowpackbc.com) · user guide: [AWSOME BC User Guide](https://machtlp.github.io/AWSOME_BC_Docs/)
- Earlier developments (ISSW 2026 point runs, HRDPS, AvAPro v1/v2): [Documentation_ISSW](https://machtlp.github.io/Documentation_ISSW/)
- AWSOME core code: [gitlab.com/avalanche-warning](https://gitlab.com/avalanche-warning)
- SNOWPACK: [SLF SNOWPACK](https://www.slf.ch/en/services-and-products/snowpack.html) · HRDPS: [MSC Datamart](https://eccc-msc.github.io/open-data/msc-datamart/readme_en/)

!!! note "Public site"
    This repository is public. Account ids, bucket names, host addresses, tokens and database credentials are left out
    on purpose; the pages name scripts and folders relative to the snowpackbc repository.
