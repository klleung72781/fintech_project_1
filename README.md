# FinTech Bootcamp Project Name TBD
### Group 2
##### Members
* Aaron Sechler
* Franklin Bueno
* George Cruz
* King Leung
---

### Data Gathering and Preparation:

1. **Demand**: finding the most densely populated counties in the US (*Unfortunately population density is not a readily available stat*)
    - Since 2019 is not a census year, we decided to use the 2019 population estimate available on Census.gov:
        https://www.census.gov/programs-surveys/popest/technical-documentation/file-layouts.html
    - Population density = Population / Land Area (this was obtained from Census TIGER/Line shapefiles):
        https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html
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

2. **Potential Income**:  finding the counties with the highest median income
    - CensusData python library provides easy access to the data
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

3. **Other deciding factors**: gather additional dataset of Counties in both Top 100 in Population Density and Income<br>The results have 51 counties.  Using the 
    - Costs (*Median Value per Sq. Foot* & *Property Tax Rate*)
    - Potential Income (*Price-to-rent Ratio*)

![Median Home Value](Images/median_home_value_line.png)

![Price to Rent Ratio](Images/price_to_rent_ratio.png)