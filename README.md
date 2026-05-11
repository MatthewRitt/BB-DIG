## BB-DIG: Alabama Black Belt Voter Data Integration & Governance

This repository contains standardized voter participation datasets for the 17 Alabama Black Belt counties, produced for the Southern Poverty Law Center (SPLC) as part of INST490 at the University of Maryland.

## Project Overview

The BB-DIG project produces three types of cleaned datasets across two election years (2020 and 2024 General Elections) covering civic participation in the Alabama Black Belt. The goal is to give SPLC a consistent, well-documented foundation for voting rights research, policy work, and community outreach in the region.

## The 17 Black Belt Counties

Barbour, Bullock, Butler, Choctaw, Crenshaw, Dallas, Greene, Hale, Lowndes, Macon, Marengo, Montgomery, Perry, Pike, Russell, Sumter, Wilcox

## Datasets

This repository contains six cleaned CSV datasets in the clean_data folder.

The eligible_population files for 2020 and 2024 measure voter participation against the CVAP eligible population. They answer the question of everyone who could vote, how many did.
The voter_registration files for 2024 (with 2020 in progress) measure registration access and purge risk using ALVR active and inactive counts. They answer who registered and who is at risk of being removed from the rolls.
The voter_turnout files for 2020 and 2024 measure voter turnout against ALVR total registered voters. They answer of registered voters, how many showed up.

Each dataset uses a different denominator because each answers a different question. They should be used together for the complete picture of civic participation.

## How to Use This Repository
Start with the standardization document to understand the project's methodology. Then read the data dictionary for the specific dataset you want to use. Open the cleaned CSV in the clean_data folder for your analysis. Reference the cleaning scripts if you need to understand how the data was processed. You can reference the verification scripts to see how source consistency was checked.

## Important Documents

All standardization can be found in our Standardization document located in the repository.

Each dataset has a data dictionary with two parts. There is a xlsx file showing the columns and descriptions. There is also a documentation pdf providing more information specific to that dataset.

## Team

BB-DIG Team 1, INST490 Spring 2026, University of Maryland
Matthew Ritter 
Bao Nguyen
Maggie Hermanto
Asmita Brahme
Arnav Patel
Xuan Zhang

## License and Attribution

The code, cleaning scripts, data dictionaries, and standardization documentation in this repository are released under the MIT License. See LICENSE.md for details.

Raw and processed data files remain subject to their original publishers' terms of use. This project uses data from the Alabama Secretary of State, the U.S. Census Bureau, and the Redistricting Data Hub. This data was obtained from the Redistricting Data Hub. This analysis was conducted using data from the Redistricting Data Hub. See DATA_SOURCES.md for full attribution and terms.

## Acknowledgments

This project was done in partnership with the Southern Poverty Law Center (SPLC) as part of INST490 at the University of Maryland. The team is thankful to the SPLC for their partnership and to the Alabama Secretary of State, the U.S. Census Bureau, and the Redistricting Data Hub for making this data publicly available.