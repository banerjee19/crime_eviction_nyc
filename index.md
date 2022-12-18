# Does crime and eviction share a significant association?  
### A tract level analysis for New York City, 2019
Debjit Banerjee, Commmand Line GIS, Fall 2022  
Bloustein School of Planning and Public Policy, Rutgers University

To understand this, I borrowed data from two sources. I used Crime and Eviction data from New York City's Open data portal. In addition, I used census variables that 
extant reserch has shown to have a positive association with eviction. 

The Crime data is from the [NYPD Historic Complaint](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)
dataset which I filtered to include data from only 2019. The data for eviction is from the [Eviction](https://data.cityofnewyork.us/City-Government/Evictions/6z8x-wfk4)
dataset that has records of every formal eviction in the city from 2017 till present day. I filtered the data for 2019 to be consistent with the complaint data. They are both updated every year. 
Both of these datasets contains lat-long values for the point locations. So, they had to be converted to geopandas geometries to be mappable.  

The total crimes and total evictions are point datasets. To create choropleth maps, first aggregated them to census tracts and then normalized them. The eviction counts 
were normalized by the total renter households in each census tract to estimate the 'eviction rate' for each. The total crimes were normalized by the total population 
and then multiplied by 100,000 to generate the crime rate per 100,000 population per census tract.


