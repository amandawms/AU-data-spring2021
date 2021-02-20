# Largest Landlords Disproportionately Concentrated in Wards 7, 8   

Despite only accounting for 4% of the DC apartment rental market, the city's top 11 largest landlords hold 12% of apartment rental properties in wards 7 and 8. This matters for a reason I will eventually figure out.  

## Questions for [this DC Residential Property Tax Dataset](https://github.com/amandawms/AU-data-spring2021/blob/main/Assignment5dataset.csv): 

### What is the distribution of 2+ unit apartment buildings by ward? 

The majority (52%) of 2+ unit buildings are residential conversions with less than 5 units. These are single family residences that have been converted to 2+ unit buildings. The next most common type of 2+ unit building is a Residential Flat, with is a building with less than 5 units but was built to be multi-family rather than converted.

Ward 6 has the most 2+ unit buildings with 4174 total, followed by Wards 1 and 5. Wards 3 and 4 have the least amount of 2+ unit buildings. Ward 6 also has more Residential Conversions with 3149 total, which is nearly as many as Wards 2, 3, 4, 5, 7, and 8 combined. 

Ward 8 has the highest number of 6+ unit apartment buildings with 866, followed closely by Ward 7 with 599. Together they account for 46% of the total 6+ unit apartment buildings in the city. But the most common type of 2+ unit building in each of these are the residential flats of 5 units or less. Ward 8's buildings are almost evenly split between 6+ unit walk ups and less than 5 unit residential flats.   


### Which ward has the highest concentration of large (12+ unit with elevator) apartment buildings?

Ward 1 has the highest number of large apartment buildings with 151, accounting for nearly 6% of its 2+ unit buildings. The other wards have considerably less, with Ward 8 having the least 12+ unit buildings with just 21. 


### Which landlords have the most properties and what is that distribution by ward? 

Government entities are by far the biggest landlords when it comes to 2+ unit buildings. The District of Columbia Housing Authority holds 277 properties, the majority of which are in Ward 8. The United States of America holds 105 properties, primarily concentrated in Ward 7. The District of Columbia holds 67 properties, most of which are also in Ward 8. 

Overall, the majority of landlords (12,511) only own one 2+ unit property.  

Looking at the 11 largest property owners, you can see that 62% of their properties are in Wards 7 (21%) and 8 (41%). This trend holds true even when discounting the government-owned properties. The highest concentration of the largest private landlords is still in Ward 8, followed distantly by Ward 7. The top 11 property owners hold 15% of all properties in Ward 8 and 9% in Ward 7. 

Two of these top 11 landlords have almost identical names - PARKLANDS MANOR ASSOCIATION and PARKLANDS MANOR ASSOC LP. Combined, they own 50 properties, which would put them at the top of non-government landlords for 2+ unit buildings. We will look into whether they are the same or not. 

The most common apartment type these largest 11 landlords own are Residential walkups with 6+ units. 


### Steps for Analyzing:

I created a pivot table with wards in the column field, property type in the row field and count of property type in the values to see the count of each type of apartment building by ward. 

Then I added another count of property type to the values field so I could get percentages of the overall total of each type of building per ward. This is how I answered my first two questions. 


For my third question about landlords, I created a new pivot table with the owner name in the row, a count of property type in the values and ward data in the column field. Then I sorted that into descending order to see which landlords had the most properties.
 
To look at the top ten property owners, I filtered the pivot table to the top ten owners by property count. Then I added the property type back into the rows field to see what kind of 2+ unit building each landlord owns. Because the 10th and 11th largest property owners hold 17 properties, I actually have a top 11. 


### Notes + Definitions for dataset: 

21	Residential-Apartment-Walk-Up	(Class 2) : Structure of 6 or more units; 1 owner; owner's motivation is to earn investment income; no units higher than 3rd floor; no elevator; may have accessory uses.

22	Residential-Apartment-Elevator	(Class 2) : Structure with 12 or more units; 1 owner; elevator; more than 3 floors; may have accessory uses (parking, laundry, etc.). Owner's motivation is investment income.

23	Residential Flats-Less than 5	(Class 1 or 2) : Structure with more than 1 single family unit, less than 5; usually self-contained, under 1 roof; few accessory uses; in some cases, owner occupies 1 unit; built for this use.

24	Residential-Conversions-Less than 5 	(Class 1 or 2) : Structure with more than 1 single family unit, less than 5; usually self-contained, under 1 roof; few accessory uses; in some cases, owner occupies 1 unit; original primary use not multi-family

25	Residential-Conversion-5 units	(Class 1 or 2) : Structure with 5 units, usually not self-contained but under 1 roof; with few accessory uses; 1 unit may be owner-occupied; original primary use not multi-family.


### What I did: 
Downloaded from open source DC 
Deleted a lot of columns: 
ABTLOTCODE
ACCEPTCODE
AMTDUE1
AMTDUE2
AMTDUE3
ANNUALTAX
ARN
ASRNAME
ASSESSMENT
BIDBALANCE
BIDCOLLECTED
BIDNAME
BIDTOTALDUE
CAPCURR
CAPPROP
CY1BAL
CY1COLL
CY1CR
CY1FEE
CY1INT
CY1PEN
CY1TAX
CY1TOTDUE
CY1TXSALE
CY1YEAR
CY2BAL
CY2COLL
CY2CR
CY2FEE
CY2INT
CY2PEN
CY2TAX
CY2TOTDUE
CY2TXSALE
CY2YEAR
DUEDATE1
DUEDATE2
DUEDATE3
INST_NO
LASTPAYDT
MIX1BLDPCT
MIX1BLDVAL
MIX1CLASS
MIX1LNDPCT
MIX1LNDVAL
MIX1RATE
MIX1TXTYPE
MIX2BLDPCT
MIX2BLDVAL
MIX2CLASS
MIX2LNDPCT
MIX2LNDVAL
MIX2RATE
MIX2TXTYPE
MIXEDUSE
NEWIMPR
NEWLAND
NEWTOTAL
OLDIMPR
OLDLAND
OLDTOTAL
PACEBALANCE
PACECOLLECTED
PACETOTALDUE
PARTPART
PCHILDCODE
PHASEBUILD
PHASELAND
PIPARENTLOT
PREMISEADD
PRESSL
PY10BAL
PY10COLL
PY10CR
PY10FEE
PY10INT
PY10PEN
PY10TAX
PY10TOTDUE
PY10TXSALE
PY10YEAR
PY1BAL
PY1COLL
PY1CR
PY1FEE
PY1INT
PY1PEN
PY1TAX
PY1TOTDUE
PY1TXSALE
PY1YEAR
PY2BAL
PY2COLL
PY2CR
PY2FEE
PY2INT
PY2PEN
PY2TAX
PY2TOTDUE
PY2TXSALE
PY2YEAR
PY3BAL
PY3COLL
PY3CR
PY3FEE
PY3INT
PY3PEN
PY3TAX
PY3TOTDUE
PY3TXSALE
PY3YEAR
PY4BAL
PY4COLL
PY4CR
PY4FEE
PY4INT
PY4PEN
PY4TAX
PY4TOTDUE
PY4TXSALE
PY4YEAR
PY5BAL
PY5COLL
PY5CR
PY5FEE
PY5INT
PY5PEN
PY5TAX
PY5TOTDUE
PY5TXSALE
PY5YEAR
PY6BAL
PY6COLL
PY6CR
PY6FEE
PY6INT
PY6PEN
PY6TAX
PY6TOTDUE
PY6TXSALE
PY6YEAR
PY7BAL
PY7COLL
PY7CR
PY7FEE
PY7INT
PY7PEN
PY7TAX
PY7TOTDUE
PY7TXSALE
PY7YEAR
PY8BAL
PY8COLL
PY8CR
PY8FEE
PY8INT
PY8PEN
PY8TAX
PY8TOTDUE
PY8TXSALE
PY8YEAR
PY9BAL
PY9COLL
PY9CR
PY9FEE
PY9INT
PY9PEN
PY9TAX
PY9TOTDUE
PY9TXSALE
PY9YEAR
REASONCD
SALEPRICE
SALETYPE
SEWSBALANCE
SEWSCOLLECTED
SEWSTOTALDUE
SUBNBHD
SUFFIX
SWWSADBALANCE
SWWSADCOLLECTED
SWWSADTOTALDUE
TOTBALAMT
TOTCOLAMT
TOTDUEAMT

Then I filtered by Use Codes: 
21	Residential-Apartment-Walk-Up

22	Residential-Apartment-Elevator

23	Residential Flats-Less than 5

24	Residential-Conversions-Less than 5

25	Residential-Conversion-5 units

Then I replaced all blanks with n/a

Then I copied and pasted into a new CSV file so that I'd later be able to upload to GitHub.
