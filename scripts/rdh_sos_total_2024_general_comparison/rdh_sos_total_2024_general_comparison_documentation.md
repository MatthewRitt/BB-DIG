# RDH & SoS Total 2024 General Comparison Documentation

## Overview
This script reads the 2024 total general election datasets from the Secretary of State (SoS) and Redistricting Hub (RDH)
and uses the absolute value of the total number of people who voted and registered from each dataset to compute the differences
in the values between the two datasets. The script is also narrowed down to only include the 17 Black Belt Counties. These county
names are detailed in our README file which you can find in this repository.

## Data Sources
Secretary of State (https://www.sos.alabama.gov/)
* ../../data_storage/raw_data/voter_data/2024_total_gen_election.xlsx

Redistricting Hub (https://redistrictingdatahub.org/) 

* ../../data_storage/raw_data/voter_data/AL_l2_2024_gen_stats_2020county.csv

## How to Use
The code outputs have already been generated for your convenience. The last output (the table)
is the most important piece of this script.
* `voted_difference_percent` displays the proportion of the difference in absolute values of total ballots cast for the SoS data and the RDH data.
* `voted_difference` displays the absolute value of the difference in total ballots cast for the SoS data and the RDH data.
* `reg_difference_percent` displays the proportion of the difference in absolute values of registration numbers for the SoS data and the RDH data.
* `reg_difference` displays the absolute value of the difference in registration numbers for the SoS data and the RDH data.
