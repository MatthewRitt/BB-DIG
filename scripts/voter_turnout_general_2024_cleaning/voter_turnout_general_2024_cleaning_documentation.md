# Voter Turnout 2024 General Cleaning Documentation

## Overview
This script reads the Alabama Secretary of State (SoS) turnout files along with the Alabama Voter Registration (ALVR) October 2024 sheet and the Redistricting Data Hub (RDH) voter file to produce a cleaned voter turnout dataset for the 2024 General Election. The script merges total ballots cast with breakdowns by gender, age, and race, and calculates race-based turnout rates using ALVR total registered voters as the denominator. The script is narrowed down to the 17 Black Belt Counties detailed in the README file in this repository.

## Data Sources
Secretary of State (https://www.sos.alabama.gov/)
* ../../data_storage/raw_data/voter_data/2024_total_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_gender_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_age_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_race_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_votereg_data_AlSoS.xlsx

Redistricting Hub (https://redistrictingdatahub.org/)
* ../../data_storage/raw_data/voter_data/AL_l2_2024_gen_stats_2020county.csv

## How to Use
The code outputs have already been generated for your convenience. The script produces one CSV file in the clean_data folder.

* `turnout_rate` displays total ballots cast divided by registered voters
* `turnout_rate_black`, `turnout_rate_white`, `turnout_rate_latinx` displays race-based turnout rates calculated as ballots divided by total registered voters from ALVR (active plus inactive)