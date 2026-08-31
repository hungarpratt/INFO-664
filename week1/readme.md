# Background
For my final project, I will be demonstrating my skills in scraping, analyzing and presenting data using Python. I'm still trying to figure out ~~the perfect project~~ what to work on, but I have several topics I'm considering, as follows:

1. Soviet Jewish Emigration 1970-2000
2. Correlation between lung cancer and air pollution
3. Concept 3


## Concept 1: Soviet Jewish Emigration 1970-2000

**Background**
I have an acquaintance who runs a non-profit focused on the history of the Soviet Jewish refusenik movement, and we've been talking about how to best represent the enormous migration of individuals (2 million individuals between 1970 and 2000) from the former Soviet Union to the United States and Israel. Inspired by the extraordinary timelapse representation of the trans-Atlantic slave trade found at [slavevogages.org](https://www.slavevoyages.org/voyage/trans-atlantic#timelapse), I would like to depict the migration pattern of this population over time. In order to do this, I'd need to obtain a dataset with the following fields for each individual:
- Year of emigration
- Departure location (ideally the specific city/town, but at minimum the Republic, e.g. Russia, Latvia, Georgia)
- Arrival location  (ideally the specific city and town in the U.S. and Israel, but at minimum the country)

**Data**
So far, I've been able to source this for the U.S. - bound immigrants at [this website](https://www.refugeeresettlementdata.com/data.html). Here's how the website is described by its authors:

>​This website is the result of a collaboration between the Universities of Göttingen, Heidelberg and Western Australia. It has been created as a platform to share digitised individual refugee data (1975-2008) obtained from publicly held records as originally recorded by the Office of Refugee Resettlement.

## Concept 2: Correlation Between Lung Cancer and Pollution in the U.S.

**Background**
Both my parents (non-smokers) developed lung cancer in the last 10 years; my dad passed away from his cancer this past summer. My parents have a number of friends, also non-smokers, who were diagnosed with lung cancer in their 80's. All of these people grew up in Pittsburgh, Pennsylvania, a city with a long industrial history in the coal and steel industries.

I have heard anecdotally that there's a connection between lung cancer and air pollution, and I'm curious if there is a clear and quantifiable correlation. To do this analysis, I would need to find data on a region's air quality and it's rate of lung cancer (and factor in lag time for the disease to actually develop). 

**Data**
I've found two data sources that I think might work for this purpose:

- [The CDC's WONDER cancer incidence](https://wonder.cdc.gov/cancer.html). The CDC only began tracking this data in 1999, so I'd be using data from 2000 - 2020.  According to some preliminary research I've done, there is a 20-30 year latency period between exposure to carcinogens and diagnosis of lung cancer. Consequently, if I wanted to use air pollution data from 1970 = 2000.

- [EPA Air Data](https://www.epa.gov/outdoor-air-quality-data)

I would need to merge the two data sets and focus on the following fields of data:
- Year
- County code
- Pollution rate
- Lung cancer rate
- Smoker rate (to remove that bias from the analysis)

## Concept 3: YYY