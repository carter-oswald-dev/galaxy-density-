# Galaxy Counter

> A web-based astronomy tool that estimates how many galaxies lie behind a small patch of sky.



# Project Overview

## What is Galaxy Counter?

Based on this [2022 XKCD comic](https://xkcd.com/2596/) where you can use your phone to show just how small of a patch of the sky you need to have for there to be roughly 50,000 galaxies inside the circle.

### Goal

- Update estimated galaxy counts based on newer surveys such as those from the [James Webb Space Telescope](https://science.nasa.gov/mission/webb/).
- Make astronomical scales easier to understand.
- Allow for more accurate and custom comparisons of galaxy density using user-input measurements of phone and arm length.

---

# The Core Idea

A user provides:

- Screen width
- Circle width
- Arm length

The application then calculates:

- Apparent angular size
- Area of sky covered
- Estimated number of galaxies based on different methods and models.

The result is intended to give a ballpark answer to:

> Roughly how many galaxies exist behind this patch of sky?

---

# How It Works

The user provides:

- Screen width: Physical width of the phone screen.
- Circle width: Physical width of the circle shown on-screen.
- Arm length: Distance from eyes to the phone.

The application then performs several calculations:

- Angular diameter: Converts the circle measurement into its apparent size in the sky.
- Sky area: Converts the angular diameter into an area measured in square degrees.
- Galaxy density: Applies the selected galaxy density model.
- Estimated galaxy count: Multiplies the sky area by the selected density value.

The final result provides a ballpark estimate of how many galaxies exist behind the selected patch of sky.

---

# Important Notes

- Results are estimates.
- Different density models produce different answers.
- The number shown is not an exact count due to likely changes in galaxy density estimates as newer data becomes available.
- Intended as a fun and educational visualization tool.

---

# Data Sources

Galaxy Counter is designed to support multiple galaxy-density models. Some models are based on published estimates of the total number of galaxies in the observable universe, while future versions may use density maps derived from astronomical surveys.

Potential data sources include:

- XKCD comic that inspired this project:
  - https://xkcd.com/2596/

- James Webb Space Telescope:
  - https://science.nasa.gov/mission/webb/

- 2MASS Extended Source Catalog (XSC):
  - https://irsa.ipac.caltech.edu/Missions/2mass.html

- WISE × SuperCOSMOS Photometric Redshift Catalog:
  - http://ssa.roe.ac.uk/WISExSCOS.html

Future versions may use one or more of these datasets to create pre-computed galaxy-density maps that operate entirely within the browser without requiring external APIs or backend services.

---

# Design Goals

- No backend required.
- No mandatory APIs, avoiding API management overhead and rate-limit concerns.
- Mobile-friendly.
- Fast loading.
- Open source.
- Support multiple galaxy-density models and assumptions.
- Allow users to compare historical estimates, modern estimates, and survey-derived estimates.
- Support future integration of pre-computed sky-density maps while remaining fully compatible with GitHub Pages.

---

