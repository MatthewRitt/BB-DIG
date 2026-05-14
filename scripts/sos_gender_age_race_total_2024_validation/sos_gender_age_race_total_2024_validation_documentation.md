# SoS Gender, Age, Race, and Total 2024 Validation Documentation

## Overview
This script reads data from the 2024 general election broken down by gender, age, race, and total ballots
from the Secretary of State (SoS). The script joins the three demographic datasets and verifies that they
all contain the same values for the total ballots cast column. After that, it calculates the difference in
absolute values of total ballots cast, as well as the proportion of the difference,
between the merged demographic datasets and the total ballots dataset.

## Sources
Secretary of State (https://www.sos.alabama.gov/)
* ../../data_storage/raw_data/voter_data/2024_gender_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_age_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_race_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2024_total_gen_election.xlsx

## How to Use
The code outputs have already been generated for your convenience. The last output (the table)
is the most important piece of this script.
* `difference_percent` displays the proportion of the difference in absolute values of total ballots cast for the
  demographics table and the total table.
* `difference` displays the absolute value of the difference in total ballots cast for the demographics table
  and the total table.
