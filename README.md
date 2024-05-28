# Data Kit - County Quarterly Census of Employment and Wage Summarization
## Version

Current version: 2024-05-22

## Provider

  - Organization: [Mid-Ohio Regional Planning Commission](https://morpc.org)
  - Contact: 
    - Name: Oliver Gwynn
	- E-mail: ogwynn@morpc.org

## Disclaimer

This data kit is a work in progress.

## Introduction

Each quarter the U.S. Bureau of Labor Statistics Census of Employment and Wage produces count of employment and wages reported by employers for the prior quarter. This data set includes annual factors for each given year, average establishment counts and employment levels, total wages, taxable wages and annual contributions, average annual and weekly pay, along with over the year change by count and percentage for each previously mentioned factor. The location quotient for average establishment counts and employment levels, total wages, taxable wages and annual contributions are also included. The purpose of this data kit is to create regional summary data from county-based QCEW data, and output datasets containing both county-level and region wide QCEW data.

## Outputs
This data kit includes up to four summarized outputs derived from a trasformation of Quarterly Census of Employment and Wage data from the Bureau of Labor Statistics:

  - County level adn regional summary quarterly long-form table that could (hypothethically) be used to drive a dashboard on the MORPC Insights platform (`./assets/output_data/qcew_quarterly_long_summarized.csv`)
  - County level and regional summary annual long-form table that could (hypothethically) be used to drive a dashboard on the MORPC Insights platform (`./assets/output_data/qcew_annual_long_summarized.csv`)
  - County level and regional summary quarterly wide-form table that contains concatenated QCEW data from BLS (`./assets/output_data/qcew_quarterly_wide_summarized.csv`)
  - County level with regional summary annual wide-form table that contains concatenated QCEW data from BLS (`./assets/output_data/qcew_annual_wide_summarized.csv`)
  
Each output is accompanied by a [Frictionless Resource file](https://specs.frictionlessdata.io/data-resource/), which provides a high-level description of the data and a link to the associated table schema.  The Resource file also provides the [MD5 checksum](https://en.wikipedia.org/wiki/Md5sum) ("hash") and the file size ("bytes") of the data file to allow for integrity checking.

The table schema is described by a [Frictionless Schema file](https://specs.frictionlessdata.io/table-schema/), which describes each of the fields contained in the table, including its name and type, and sometimes provides additional metadata about the table.

## Processes

The outputs are produced by a process which complies and transforms the data:

  1. A fully-automated process implemented as a Jupyter notebook (`./assets/01-summarize_qcew_data.ipynb`) uses the standardized wide-form BLS QCEW data and produces annual and/or quarterly summarized long and wide-form tables (`./assets/output_data/qcew_quarterly_long.csv`, `./assets/output_data/qcew_annual_long.csv`, `./assets/output_data/qcew_quarterly_wide.csv`, `./assets/output_data/qcew_annual_wide.csv`).

## Inputs

The process requires standardized wide-form BLS QCEW '.csv' files from the user. These files can be obtained automatically using [qcew_data_kit](https://github.com/olivergwynn/qcew_data_kit/tree/main) to automate the standardiztion of individual QCEW files into a dataset.

  1. Files must come from [qcew_data_kit](https://github.com/olivergwynn/qcew_data_kit/tree/main), be in wide-form, and placed in input data directory (`./assets/input_data/`)


## Revision history

### 2024-05-28 Oliver Gwynn <ogwynn@morpc.org>

First revision version.

### 2024-05-22 Oliver Gwynn <ogwynn@morpc.org>

Initial WIP version. 
