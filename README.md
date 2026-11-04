# UK Rent & Landlord Obligations Index 2026

A compact, source-linked comparison of 20 UK areas: private rent levels from official statistics, council tax Band D, local property-licensing schemes, and national rules for landlords (registration, deposits, energy rating, tenancy law).

- Version: 1.0
- Data date: private rents for September 2026 (ONS release of 21 October 2026); council tax for 2026-27; licensing and rules checked on 3 November 2026
- Author: Leonid Gorok
- Project site: [izirento.com](https://izirento.com)
- Used on: [UK Rent & Landlord Obligations Index 2026 on izirento.com](https://izirento.com/en-gb/research/data/uk-rents-and-landlord-duties-index)
- Last checked: 3 November 2026
- Licence: CC BY 4.0 for the compilation (see [`LICENSE`](LICENSE) and [`LICENSE.md`](LICENSE.md); underlying official data remain under the Open Government Licence v3.0)

## Files

| File | Content |
| --- | --- |
| [`uk_rent_obligations_index_2026.csv`](uk_rent_obligations_index_2026.csv) | One row per area (20 rows). Rent, council tax, additional and selective licensing, with a source URL for each field group |
| [`nation_rules_2026.csv`](nation_rules_2026.csv) | One row per nation (4 rows). National averages and rules that apply to every area in that nation, with source URLs |
| [`sources.md`](sources.md) | Every field, its publisher, URL, licence and as-of date |
| `LICENSE` | Creative Commons Attribution 4.0 International legal code |
| `LICENSE.md` | Why CC BY 4.0 fits the sources, and required attribution statements |

Join the two CSV files on `nation`.

## The 20 areas

- England (13): Birmingham, Manchester, Liverpool, Leeds, Sheffield, Bristol, Nottingham, Newham, Camden, Oxford, Brighton and Hove, Newcastle upon Tyne, Leicester
- Wales (3): Cardiff, Swansea, Newport
- Scotland (3): City of Edinburgh, Glasgow City, Aberdeen City
- Northern Ireland (1): Belfast

Selection: England and Wales areas are local authorities with official local rent figures, chosen to mix large cities with different licensing set-ups (city-wide, partial, none). Scotland and Northern Ireland are included to show how the rules differ, with the data caveats below.

## Official sources

- Office for National Statistics: [Price Index of Private Rents, UK: monthly price statistics (21 October 2026 edition)](https://www.ons.gov.uk/economy/inflationandpriceindices/datasets/priceindexofprivaterentsukmonthlypricestatistics/21october2026)
- Office for National Statistics: [Private rent and house prices, UK: October 2026](https://www.ons.gov.uk/economy/inflationandpriceindices/bulletins/privaterentandhousepricesuk/october2026)
- MHCLG: [Council Tax levels set by local authorities in England 2026 to 2027](https://www.gov.uk/government/statistics/council-tax-levels-set-by-local-authorities-in-england-2026-to-2027)
- Welsh Government: [Council Tax levels: April 2026 to March 2027](https://www.gov.wales/council-tax-levels-april-2026-march-2027)
- Scottish Government: [Council Tax datasets](https://www.gov.scot/publications/council-tax-datasets/)
- MHCLG: [Register your rental property service: guidance for landlords](https://www.gov.uk/guidance/register-your-rental-property-service-guidance-for-landlords)
- GOV.UK: [Renters' Rights Act: an overview for landlords](https://www.gov.uk/guidance/renters-rights-act-an-overview-for-landlords)

Council pages and every other URL, field by field, are in [`sources.md`](sources.md) and in the `*_source_url` columns of the CSV files.

## Methodology

1. **Rents.** Taken as published from ONS "Price Index of Private Rents, UK: monthly price statistics" (Table 1, month September 2026). The figure is the average monthly rent across new and existing tenancies, for all homes and by number of bedrooms. Annual change is the 12-month change, rounded to one decimal place. The latest two months are provisional and ONS revises them.
2. **Council tax.** Band D for 2026-27 as published by MHCLG (England, area average including parish precepts and, in London, the GLA precept), the Welsh Government (billing authority average including police and community council elements) and the Scottish Government (council Band D, excluding water and sewerage). Values are rounded to pence.
3. **Licensing.** For each council, the council's own pages or formal designation notices were read on 3 November 2026. Council facts are written in our own words, with the source URL and check date; no council text, logos or maps are copied. "No scheme found" means the council's licensing pages list no such scheme; it is not proof that none exists. Mandatory HMO licensing applies everywhere (thresholds differ by nation, see `nation_rules_2026.csv`).
4. **National rules.** Taken from GOV.UK, Welsh Government and Rent Smart Wales, Scottish Government and mygov.scot, and nidirect / Department for Communities pages.
5. **Blanks.** A cell is left empty when no verifiable public figure was found. No value is estimated or filled by calculation.

## Field dictionary: `uk_rent_obligations_index_2026.csv`

| Field | Meaning |
| --- | --- |
| `area_id` | Short identifier |
| `area_name` | Area name |
| `nation` | England, Wales, Scotland or Northern Ireland |
| `ons_area_code_used` | ONS code of the geography the rent figure comes from (a Broad Rental Market Area for Scotland) |
| `rent_geography` | Local authority, or Broad Rental Market Area (BRMA) |
| `rent_geography_note` | Caveat about the geography |
| `pipr_period` | Month of the rent figure (YYYY-MM) |
| `avg_monthly_private_rent_gbp` | Average monthly private rent, GBP, all homes |
| `rent_annual_change_pct` | 12-month change in that rent, percent |
| `avg_rent_1_bed_gbp`, `avg_rent_2_bed_gbp`, `avg_rent_3_bed_gbp` | Average monthly rent by bedrooms, GBP |
| `rent_source_url` | ONS dataset page |
| `council_tax_band_d_2026_27_gbp` | Band D council tax for 2026-27, GBP per year |
| `council_tax_source_url` | Publisher page |
| `additional_hmo_licensing` | Whether an additional (small HMO) licensing scheme is in force, and its reach |
| `additional_hmo_licensing_detail` | Scope, dates, qualifying rule |
| `additional_hmo_licensing_source_url` | Council page or designation notice |
| `selective_licensing` | Whether a selective (whole-rented-home) licensing scheme is in force, and its reach |
| `selective_licensing_detail` | Scope and dates |
| `selective_licensing_source_url` | Council page or designation notice |
| `licensing_checked_on` | Date the council pages were read |
| `england_landlord_register_window` | England only: region and legal registration window of the national landlord register |
| `england_landlord_register_source_url` | GOV.UK guidance |
| `row_notes` | Row-level caveats |

`nation_rules_2026.csv` fields: national average rent and council tax; mandatory HMO rule; landlord registration or licensing; deposit protection and cap; minimum EPC in force and planned; whether the Renters' Rights Act 2025 applies; main tenancy framework; rent-increase rule where verified; each with a `*_source_url` field.

## Limitations

- **Scotland.** ONS publishes Broad Rental Market Areas, not councils. Edinburgh uses Lothian, Glasgow uses Greater Glasgow, Aberdeen uses Aberdeen and Shire; these cover wider areas than the councils. Scottish rents are mainly advertised new lets, so do not compare them directly with England and Wales.
- **Northern Ireland.** The ONS table has national figures only, and the latest month is July 2026. Belfast rent and council tax cells are blank (Northern Ireland uses domestic rates). National NI rent is in `nation_rules_2026.csv`.
- **Council tax** is not comparable across nations: bands are valued on different dates and have different ratios. Compare within a nation.
- **Rent figures** are averages that can move sharply month to month at local level; ONS advises reading longer trends.
- **Licensing** schemes change often. The `licensing_checked_on` date applies. Swansea's council page could not be opened, so its scheme details were taken from the council policy listing and the Rent Smart Wales notice. Brighton and Hove's planned extension (Central Hove and Regency) is paused.
- **Rules not yet in force.** England's national landlord register starts regionally from 15 December 2026; England's EPC C target for 2030 is a stated plan, not yet law.
- **Blank by design:** Wales planned EPC standard; Scotland and Northern Ireland current minimum EPC (no in-force standard confirmed from an official page); Wales and Northern Ireland rent-increase rules; Belfast rent and council tax.
- This dataset is information, not legal advice.

## Citation

Gorok, L. (2026). *UK Rent & Landlord Obligations Index 2026* (Version 1.0) [Data set]. IziRento. [https://izirento.com](https://izirento.com)

## Attribution

Contains public sector information licensed under the Open Government Licence v3.0. Source: Office for National Statistics, Price Index of Private Rents. Crown copyright. Source: nidirect / Department for Communities (NI). Crown copyright. Third-party OGL data remain under [OGL v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). See [`LICENSE.md`](LICENSE.md) for the full statements.

## Licence and credit

The compilation is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (full text in [`LICENSE`](LICENSE)). When you reuse it, credit IziRento with a link, for example: "UK Rent & Landlord Obligations Index 2026 by IziRento ([izirento.com](https://izirento.com/en-gb/research/data/uk-rents-and-landlord-duties-index)), CC BY 4.0", and keep the attribution statements above.
