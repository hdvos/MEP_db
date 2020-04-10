# MEP_db
A database of current and past Members of the European Parliament.

This database has been created by running queries in wikidata.org. 
This data was acquired on the 10th of april 2020 and contains the data as it was on this day on wikidata.

The data is in MEP_db.csv.
The queries, documentation and code to re-create the data are all in MEP_data_cleaner.ipynb.

The table contains the following columns
* **MEP_name**: The name of the member of parliament
* **national_party**: the national party the MEP represents.
* **EU_parliament_group**: The eu parliament group/fraction the MEP is part of.
* **EU_electoral_district**: The electoral district from which the MEP was chosen.
* **elected_in_country**: The country the electoral district is in.
* **start_date**: The date on which the MEP started in the EU parliament.
* **end_date**: The date on which the MEP left the EU parliament.
* **parliamentary_term**: the parliamentary term in which the MEP served. Note that the start date and end date of this term do not necessarily align with the start date and end date for an individual MEP since an MEP might leave earlier and be replaced by a different MEP.

Every column except the date columns also have an id column. This is constructed by concatenating \_id to the column name. So in the case of MEP_name this becomes MEP_name_id. These columns contain an unique URL to the objects entry in wikidata.

If an MEP served multiple terms, it has multiple rows in the table, each row representing one term.

If certain information was not in wikidata, the cell is left blank.

NOTE: this is only a selection of data from wikidata. So the limitations of wikidata are the same as the limitations for this data. I make no claims about the correctness and completeness of the data.
