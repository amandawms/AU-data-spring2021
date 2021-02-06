# Cleaning APT_DATA 

1. First, I downloaded the full dataset of all DC Basic Business Licenses from OpenDataDC.gov/datasets/basic-business-licenses. 

2. Filtered that dataset by LICENSE_CATEGORY_TEXT to only include "Housing: Residential" and "Housing: Transient". (I ended up filtering out all of the transient options later.)

3. Filtered again by LICENSECATEGORY to remove Bed and Breakfast, Boarding House, Hotel, Inn and Motel, and Rooming House (aka the Housing: Transient category), also deleted columns AE through AI, AL, and AM 

4. Copied and Pasted that newly filtered data set to a new tab, called NEWLY FILTERED DATA SET

5. Created pivot table to count by CUSTOMER_NUMBER column using BBL_CITY_STATE_ZIP as the count field because it had ZERO blanks. Turns out customer IDs are not unique and won't work for sorting like we want. 

6. In the same Pivot Table, I replaced CUSTOMER_NUMBER column with BILLING_ADDRESS_CITY_STATE_ZIP column. To count the blank cells in that column and see if it would work for landlord counts, I filtered by (blank) and discovered there are only 4. I included that at the top of the Pivot Table tab called "Pivot Table for Landlord Size" 
7. Filtered pivot table to discover number of rows per address. There are 44,653. 

8. Copied the pivot table to new sheet called "Landlord Count by Bill Address" and renamed "Row Labels" to BILLING_ADDRESS_CITY_STATE_ZIP

9. Using BILLING_ADDRESS_CITY_STATE_ZIP as a key, I joined the Address Count (Count of BBL_CITY_STATE_ZIP) onto the FILTERED DATA SET tab in column AL labeled "Address Count". I did this by creating and labeling the AL column, clicking in  the box below and entering a VLOOKUP formula: VLOOKUP(B2,'Landlord Count by Bill Address'!A:B,2,FALSE). I told excel to match the data in each cell of the BILLING_ADDRESS_CITY_STATE_ZIP column in the FILTERED DATA SET tab to the data in the BILLING_ADDRESS_CITY_STATE_ZIP column of the LANDLORD COUNT BY ADDRESS tab, then to paste the data in the cell next to each match (from the  Address Count (Count of BBL_CITY_STATE_ZIP) column) into the new column AL in the FILTERED DATA SET. It did not work the first time, I had to add FALSE so that it would find the exact matches. 

10.	I hit save. Then I saved the FILTERED DATA SET tab as a csv to upload to Github.

11. Then I tried to upload to Github and it failed because the file was way too big. 

12. Then I deleted Columns Q (DCS_ADD_DATE) and U (LICENSE_CATEGORY_TEXT) to make the size less than 25 so I could upload to GITHUB. Still was too big. Then I filtered down to only the "Apartment" option in the LICENSE CATEGORY column. I copy and pasted that into a new excel workbook and saved that as a new CSV so it would upload. 

13. Then I replaced all the blank cells with n/a. I could not do it before with the entire data set because my computer would freeze every time I tried. 

14. Then to make the original data file also small enough to upload to Github, I filtered that by the "Apartment" option in the LICENSE CATEGORY column and left everything else as it. I copy and pasted it to a new excel workbook and save it as a new csv.
