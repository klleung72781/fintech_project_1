# FinTech Bootcamp Project 1 *Real Estate vs Security*
### Group 2
##### Members
* Aaron Sechler
* Franklin Bueno
* George Cruz
* King Leung
---

### Data Gathering and Preparation:

1. **Demand**: finding the most densely populated counties in the US, since population density is not a readily available stat, we used 2 datapoints to yield the desired results.
    - Since 2019 is not a census year, we decided to use the 2019 population estimate available on Census.gov:\
        https://www.census.gov/programs-surveys/popest/technical-documentation/file-layouts.html
    - Population density = Population / Land Area (this was obtained from Census TIGER/Line shapefiles):
        https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html\
        The county `shp` file also contains latitudes and longitudes of each county, useful for plotting on a map.
        ![Population Density](Images/population_density_bubble_map.png)
        **Top 10**
        | County Name | Population Density<br>(*People per Sq. Mile*) | 
        | ----------- | ----------- |
        | **New York County**<br>New York | 71874 |
        | **Kings County**<br>New York | 36901 |
        | **Bronx County**<br>New York | 33727 |
        | **Queens County**<br>New York | 20720 |
        | **San Francisco County**<br>California | 18795 |
        | **Hudson County**<br>New Jersey | 14556 |
        | **Suffolk County**<br>Massachusetts | 13801 |
        | **Philadelphia County**<br>Pennsylvania | 11797 |
        | **District of Columbia** | 11544 |
        | **Alexandria city** (Census County) <br>Virginia | 10675 |

2. **Market Value**:  finding the counties with the highest median income
    - CensusData python library provides easy access to the data\
        https://pypi.org/project/CensusData/
    - Combining the data with TIGER/Line shapefiles to create a bubble map visualization
        ![Household Income](Images/household_income.png)
        **Top 10**
        | County Name | Median Household Income (*USD*) | 
        | ----------- | ----------- |
        | **Los Angeles County**<br>California | 1514629.0 |
        | **Cook County**<br>Illinois | 1116759.0 |
        | **Maricopa County**<br>Arizona | 933112.0 |
        | **Harris County**<br>Texas | 865645.0 |
        | **San Diego County**<br>California | 593890.0 |
        | **Orange County**<br>California | 592269.0 |
        | **King County**<br>Washington | 494443.0 |
        | **Riverside County**<br>California | 472401.0 |
        | **Dallas County**<br>Texas | 459974.0 |
        | **Miami-Dade County**<br>Florida | 449056.0 |

3. **Other deciding factors**: gather additional dataset of counties that are both top 100 in population density and income in an attempt to locate a hidden gem...
    - Capital Gain (*Median Home Value per Sq. Foot*)
    - Potential Income (*Price to Rent Ratio*)
    - Operating Costs (*Real Estate Tax Rate*)
    ![Other Deciding Factors](Images/other_deciding_factors.JPG)
    - With an assumed investment of $1 million, identify the 10 best-performing counties
        **Top 10**
        | County Name | Total Proceeds (*USD*) | 
        | ----------- | ----------- |
        | **Wayne County**<br>Michigan | 3169917 |
        | **Macomb County**<br>Michigan | 2553876 |
        | **DeKalb County**<br>Georgia | 2522056 |
        | **Alameda County**<br>California | 2500199 |
        | **Broward County**<br>Florida | 2489344 |
        | **Sacramento County**<br>California | 2479974 |
        | **Pinellas County**<br>Florida | 2470103 |
        | **Dallas County**<br>Texas | 2449903 |
        | **San Mateo County**<br>California | 2434183 |
        | **Contra Costa County**<br>California | 2421439 |

    