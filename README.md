#  Readme <br/>
This data has been normalized and cleaned using two of the tools (Tabula and OpenRefine) provided to us this semester through the LIS 545 Data Curation I course at the University of Washington. The primary curator of this data is Maria Arteaga. The topic of this dataset is the homeless counts in the state of Washington for the year of 2016. The intended audience of the final product is the general public of the State. The goal of this curation project is to combine the main point in time counts of homelessness in Washington from two agencies' yearly reports, in order to better represent any variance in the data in one place. <br/>
<br/>
Tabula was used to extract the tables from the referenced PDFs. After the tables were extracted, OpenRefine was used to clean the data. During this process empty cells were removed by excluding facets. Cells with multiple data points were separated. To further normalize the data, spelling and punctuation within the string values was standardized. <br/>
<br/>
Due to the heterogeneous nature of this curation project, there are two sets of “raw” files in the .CSV format, and two sets of “normal” files in the .CSV format. The final product is a combination of both “normal” files in one .CSV format. <br/>
<br/>
# Naming <br/>
<br/>
The file naming convention uses PascalCase and is as follows:
<br/>
<br/>
<code>
  Agency_StateTitle_Year_Datasettype
</code>
<br/>
<br/>

Agency represents the agency from which the data was retrieved. Can be either Housing and Urban Development Data “HUD” or Department of Commerce “DOC”. <br/>
State represents the State of Washington. <br/>
Title represents the title of the dataset. <br/>
Year represents the year this data was reported. <br/>
Datasettype is meant to differentiate the raw, normalized, or combined data.<br/>

#  Data Dictionary <br/>
<br/>
      
| Variable  | Variable Label | Variable Type  | Allowed Values | Description |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Demographic Type  | Demographic  | String  | “Households” “Persons” “Persons Under 18” “Persons 18 to 24” “Persons Over 24”   | The demographic representative of the houseless person the data values represent. For example a value of “Persons Over 24” will only have data representing how many people over 24 years are houseless.|
| Emergency   | Emergency  | Integer  | Integers greater than 0  |The amount of houseless persons who live in emergency shelters  |
| Transitional  | Transitional  | Integer | Integers greater than 0  |The amount of houseless persons who live in transitional housing |
| Safe Haven | Safe Haven | Integer  | Integers greater than 0  |The amount of houseless persons who were housed under Safe Haven |
| Total Sheltered  | Total Sheltered  | Integer  | Integers greater than 0 |The total amount of houseless people when you combine emergency, transitional, and safe haven |
| Total Unsheltered  | Total Unsheltered  | Integer | Integers greater than 0  |The amount of houseless persons who are not sheltered in emergency transitional or safe haven housing. |
| Total  | Total  | Integer  | Integers greater than 0  | The total number of houseless persons when you combine emergency, transitional, safe haven, and unsheltered data counts |
| Department of Commerce Total | DOC Total  | Integer  | Integers greater than 0 |The data representative of the total number of houseless persons when you combine emergency, transitional, safe haven, and unsheltered data counts for the Department of Commerce Homelessness Point in Count |
| Housing and Urban Development Total | HUD Total | Integer  | Integers greater than 0  |The data representative of the total number of houseless persons when you combine emergency, transitional, safe haven, and unsheltered data counts for the Housing and Urban Development Point in Count data |
| Difference  | Difference  | Integer  | Integers greater than 0  |The difference calculated by subtracting the DOC total from the HUD total. This datapoint represents the variation between the two agencies' homeless data count for the year of 2016 |

# Metadata Schema <br/>
### Project Open Data <br/>
<br/>

| Attribute  | Value |
| ------------- | ------------- |
| title   | Homelessness_in_Washington_Curation_Protocol |
| description | The topic of this dataset is the homeless counts in The State of Washington for the year of 2016. The intended audience of the final product is the general public of the State. The goal of this curation project is to combine the main point in time counts of homelessness in Washington from two agencies' yearly reports, in order to better represent any variance in the data in one place.   |
| keyword| “Homelessness”, “Unhoused”, “HUD”, “DOC” , “Washington”, “Point in Count”, “2016”  |
| modified  | 03/09/2022  |
| publisher | Maria Arteaga|
| contactPoint  | arteamar@uw.edu |
| identifier | https://github.com/mariaarteaga/Homelessness_in_Washington_Curation_Protocol  |
| accessLevel  | public  |
| license  | public domain |
| rights  | public  |
| spatial | Washington, USA  |
| temporal  | 2016  |
| conformsTo | https://project-open-data.cio.gov/v1.1/schema/   |
| describedBy |https://github.com/mariaarteaga/Homelessness_in_Washington_Curation_Protocol#data-dictionary-  |
| language | english  |
| references  | http://www.commerce.wa.gov/wp-content/uploads/2015/08/Commerce-Homelessness-in-Washington-2016.pdf https://files.hudexchange.info/reports/published/CoC_PopSub_State_WA_2016.pdf|
