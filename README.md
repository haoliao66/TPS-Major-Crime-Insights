# TPS-Major-Crime-Insights
**Disclaimer**: The author is not affiliated with any law enforcement instituions nor claim to have any expertise or authority on the subject of policing and public safety. This project is adapted from a school project and **for educational purposes only**. 

The data used in the project is publicably available and can be accessed at the [TPS Open Data website](https://data.torontopolice.on.ca/datasets/TorontoPS::major-crime-indicators-open-data/about)(last updated Oct. 8th 2025).
## Executive Summary
This analysis examines major crime indicators in Toronto from 2014 to 2024, with a focus on recent trends (2021–2024). The project explores crime frequency by year, category, and neighborhood, and investigates reporting delays by crime type and location.
We begin by the framing the problem at hand- there is a clear significant increase in major crime occurences in the city throughout the years, with most of the increases attributed to auto thefts and assaults. We then perform geospatial analysis to identify crime hotspots. Furthermore, we identified crime types and analyzed how reporting time can create bottlenecks. At last, we zoom in by combining all of the features to identifying individual neighborhoods where future policing efforts should focus on and give tailored actionable recommendations: 
- Neighborhood with unusually **high rates of auto theft** (West Humber-Clairville(1)) could indicate targetting operations of organized crime groups, and require further investigation and close attention
- Neighborhood with **delayed report time for assaults** (Mimico-Queensway(160)) could indicate lack of public trust in policing, and require relation improvements with local residents and targeted awareness campaigns to encourage timely reports 
- Neighborhood with **high occurences of assaults** (Downtown Yonge East(168), Moss Park(73), and other Downtown neighborhoods) may require regular patroling for prevention.
- Possible **underreporting of Theft Over** may indicate lack of trust in effective solutions by the general public. This may require public awareness campaigns for individual legal rights, relation improvement to encourage reporting, and process improvement to make reporting occurences of theft easier. 

  
## Presentation
### Problem 

The total major crime cases within the city jurisdiction has shown a clear increasing trend from year to year, with the only exception being year 2020 due to COVID-related lockdown restrictions. Crime occurrences steadily increased until 2019, and peaked in 2023. This warrants closers examination into major crime occurences and efforts to come up with effective solutions to solve and prevent major crimes and ensure public safety. 

<img width="868" height="568" alt="cases per year" src="https://github.com/user-attachments/assets/9aba4cdb-023a-4487-bf57-e3f87898ef84" />

The plot below reveals that Assault consistently has the highest number of cases from 2014 to 2024, with a sharp increase in 2023. Auto Theft also shows notable steady increase and is becoming a major resident concern, while Robbery and Theft Over remain relatively stable and lower in frequency.

<img width="868" height="547" alt="categories" src="https://github.com/user-attachments/assets/90c688fe-8748-4f22-9471-108ed981543a" />

### Geospatial Analysis

The list of neighborhoods with high crime frequencies and city-wide major crime heatmap visual shows that major crime usually occurs at downtown areas with high population density. However, a notable exception is West Humber-Clairville(1), which stands out by as one of the few suburban neighborhoods on the list with both unusually high major crime occurences ranking at number one.   

<img width="853" height="455" alt="neighborhood" src="https://github.com/user-attachments/assets/30564cc9-c668-4e24-8fe2-43a4c48f0853" />
<img width="1918" height="1033" alt="heatmap" src="https://github.com/user-attachments/assets/1504d470-9f9b-4fad-b11d-41cad2d19099" />

### Crime type and reporting time Analysis
Next we look into a potential bottleneck for crime solving and prevention- the time it usually takes for the victim to report crimes. We accomplished this by aggregating the crime occurence and crime report columns to calculate reporting delay time and categorize them. The resulting table below shows that:
- Assault and Robbery are most likely to be reported immediately (<1 hour)
- Auto thefts are most likely reported within same day
- Theft Over has the highest rate of long delay(>1 week) in reporting. It is the least reported category, which possibly indicates significant underreporting due to low trust since it might be unlikely for them to receive effective help even if victim reports the crime

| Crime Type      | Immediate | Same Day | Within Week | Long Delay | Total   |
|-----------------|-----------|----------|-------------|------------|---------|
| Assault         | 57,253    | 13,996   | 7,539       | 10,858     | 89,646  |
|                 | (63.9%)   | (15.6%)  | (8.4%)      | (12.1%)    |         |
| Auto Theft      | 7,021     | 25,342   | 3,751       | 2,147      | 38,261  |
|                 | (18.3%)   | (66.2%)  | (9.8%)      | (5.6%)     |         |
| Break and Enter | 10,031    | 9,298    | 4,535       | 2,306      | 26,170  |
|                 | (38.3%)   | (35.5%)  | (17.3%)     | (8.8%)     |         |
| Robbery         | 8,641     | 1,807    | 517         | 330        | 11,295  |
|                 | (76.5%)   | (16.0%)  | (4.6%)      | (2.9%)     |         |
| Theft Over      | 1,009     | 1,665    | 1,755       | 1,629      | 6,058   |
|                 | (16.7%)   | (27.5%)  | (29.0%)     | (26.9%)    |         |

### Combined Analysis

Lastly, we combine all aforementioned aspects of analysis (geospacial/neighborhood, crime type, and reporting delay) to highlight some especially problematic neighborhoods and respectively the major crime category they suffer from, and recommend some tailored actionable solutions for each neighborhood according to their biggest safety needs:
- Neighborhood with unusually **high rates of auto theft** (West Humber-Clairville(1)) could indicate targetting operations of organized crime groups, and require further investigation and close attention
- Neighborhood with **delayed report time for assaults** (Mimico-Queensway(160)) could indicate lack of public trust in policing, and require relation improvements with local residents and targeted awareness campaigns  to encourage timely reports 
- Neighborhood with **high occurences of assaults** (Downtown Yonge East(168), Moss Park(73), and other Downtown neighborhoods) may require regular patroling for prevention.  


<img width="1504" height="989" alt="output" src="https://github.com/user-attachments/assets/a37381cd-ca69-4692-b0bf-61ea61ee23c6" />
