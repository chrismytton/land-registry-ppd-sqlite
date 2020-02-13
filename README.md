# Land Registry Price Paid Data sqlite importer

Import a CSV download of the Land Registry Price Paid Data (PPD) into sqlite3.

## Usage

First create the database for the complete Land Registry PPD:

    bin/land_registry_complete land_registry.sqlite

Then you can query it with sqlite3:

    sqlite3 -csv -header land_registry.sqlite 'select * from ppd where price < 200'

## Lower level

If you want to import one of the non-complete datasets into sqlite use the following:

    bin/land_registry_ppd_csv_to_sqlite land_registry_2019.sqlite < pp-2019.csv
