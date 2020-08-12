# alternative-voting-methods
#### Redistricting Data Hub 2020

**************************************************************************************************

This project seeks to explore and compare the utilization of alternative voting modes (i.e. vote-by-mail, vote centers, absentee ballots, etc.) across states. 

<br> 
Project Questions:

- At what level (ex. aggregated county-wide) are election results of alternative modes reported
- What proportion of votes each type of mode makes up for recent elections 

<br> 
To begin to answer these questions, I created the following functions to output the vote total of these various modes at both the precinct and county levels for each state using the [MIT Election Data and Science Lab (MEDSL)](https://electionlab.mit.edu/data) precinct data from [2016](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LYWX3D) and [2018](https://github.com/MEDSL/2018-elections-official/blob/master/precinct_2018.zip).


The voting_modes_function files can be run with minimal modification. The only necessary thing to change is the value of "mystate" on Line 52. Enter the state abbrivation of the state you wish to learn more about its reporting of alternative voting modes.<sup>[1](#myfootnote1)</sup>

Due to slight differences in the data between 2016 and 2018, two seperate files were created for each election year, but the functions remain the same. Work is being done to integrate election year functions, but for now, to get the vote counts for a particular election year, run the file of that election year.



**************************************************************************************************

#### __county_tots__ - outputs vote totals by county
#### __modes_by_precinct__ - outputs vote total by mode in each precinct
#### __modes_by_county__ - outputs vote total by mode in each county
#### __modes_cand_by_county__ - outputs vote total by mode for every candidate in each county


<br> 

Function arguments:

- __state_abbrv__ - Abbreviation of the state you want the county vote totals of (i.e "WI").
- __df__ - Dataframe to be analyzed. Default is "df1," the name of the loaded MEDSL data.
- __csv__ - If csv="Y", the output will include a csv output of the results. Default is "Y". If csv="N", there will be no csv output of the results.
- __office_pos__ - Only applicable to 2018. The office you wish to receive vote total for. Defeault is U.S Congress for 2018. U.S Presidential election is the only seat option for 2016. 
- __prop__ - Only applies to __modes_by_county__. Default is "N". If prop="Y", rather than outputing vote total by mode in each county, the output will be the proportion of total vote each mode comprised in every county.


**************************************************************************************************

<a name="myfootnote1">1</a> Note: Every state reports alternative election mode results differently. In MEDSL data, not all states have alternative vote mode results.

MEDSL includes alternative mode results for:

_2016_

- Alabama, Alaska, Arizona, Arkansas, California, Delaware, Georgia, Hawaii, Idaho, Iowa, Kentucky, Maine, Maryland, Nebraska, New Jersey, New York, North Carolina, Oklahoma, Rhode Island, South Carolina, Washington 


_2018_

-  Alabama, Alaska, Arkansas, Delaware, Georgia, Hawaii, Idaho, Iowa, Louisiana, Maryland, Missouri, Nebraska, New Jersey, North Carolina, Oklahoma, Rhode Island, South Carolina, Virginia 


Additionally, Alaska should not be run, as the state does not have traditional counties so output is irregular.
