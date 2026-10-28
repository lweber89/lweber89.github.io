# St. Louis Crime Data Explorer

## Overview

The St. Louis Crime Data Explorer is an interactive web dashboard that maps reported offenses in St. Louis at several spatial scales, from wards and neighborhoods down to a search radius around any address, so people can see the data at the point of need. It is built on monthly data prepared by the [geocrime-stl](geocrime-stl.md) ETL package.

**Study Area:** City of St. Louis, Missouri  
**Role:** Solo project (design, development, and documentation)  
**Status:** Live

---

## Methods & Tools

**Data Source**

- SLMPD crime data as posted by the City of St. Louis, typically published around the 5th of the following month.
- Offenses are grouped using the NIBRS "crimes against" classification: Person, Property, Society, plus Firearm and Other categories.

**Features**

1. **Map views:** wards, neighborhoods, individual locations, and a heat layer.
2. **Address tools:** address search, drop-a-pin, and use-my-location, with a "see crime near this address" option.
3. **Search radius:** quarter-mile, half-mile, or one-mile.
4. **Filters:** ward, neighborhood, offense category, and date.
5. **Analysis pages:** Hotspots, Charts, and a Methodology page explaining how the data is prepared.
6. **Export:** download the current list as CSV.

**Tools Used**

| Tool | Purpose |
|------|---------|
| geocrime-stl | Monthly ETL: fetch, clean, standardize, clip to city boundaries |
| City of St. Louis, OpenStreetMap, and U.S. Census geocoders | Address search |
| GitHub Pages | Hosting |
| Agentic, AI-assisted workflows | Used to build and document the dashboard |

---

## Highlights

- **Multi-scale view:** the same data can be read at the ward, neighborhood, or address-radius level.
- **Honest about limits:** the site states plainly that these are reported offenses, not a measure of how safe a place is, and notes the limits of the data: block-level locations, per-victim counting, and reporting bias.
- **Privacy-minded:** pins and device location stay in the browser; typed addresses go only to the geocoding services and are not stored.

The page layout was adapted from a crash-map project by Reddit user u/autosoap, used with permission.

---

## Links

[Open the Explorer](https://lweber89.github.io/geocrime-stl/dashboard/){ .md-button .md-button--primary }
[View the ETL package on GitHub](https://github.com/lweber89/geocrime-stl){ .md-button }
