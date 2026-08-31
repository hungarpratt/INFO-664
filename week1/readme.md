# Background
For my final project, I will be demonstrating my skills in scraping, analyzing and presenting data using Python. I'm still trying to figure out ~~the perfect project~~ what to work on, but I have several topics I'm considering, as follows:

1. [Soviet Jewish Emigration 1970-2000](#soviet=jewish-emigration)
2. [Correlation between lung cancer and air pollution](#cancer-and-pollution)
3. [Prevalance of Hot Flashes During Perimenopause](#menopause)


## Concept 1: Soviet Jewish Emigration 1970-2000<a name="soviet-jewish-emigration"></a>
<img align="right" width="120" src="icon_russia.png" alt="Russian emigration icon">

**Background**<br/>
I have an acquaintance who runs a non-profit focused on the history of the Soviet Jewish refusenik movement, and we've been talking about how to represent the enormous migration of individuals (2 million people between 1970 and 2000) from the former Soviet Union to the United States and Israel. Inspired by the extraordinary timelapse representation of the trans-Atlantic slave trade found at [slavevogages.org](https://www.slavevoyages.org/voyage/trans-atlantic#timelapse), I would like to depict the migration pattern of this population over time. In order to do this, I'd need to obtain a dataset with the following fields for each individual:
- Year of emigration
- Departure location (ideally the specific city/town, but at minimum the Republic, e.g. Russia, Latvia, Georgia)
- Arrival location  (ideally the specific city and town in the U.S. and Israel, but at minimum the country)

**Data Source**<br/>
So far, I've been able to source this for the U.S. - bound immigrants at [this website](https://www.refugeeresettlementdata.com/data.html). Here's how the website is described by its authors:

>​This website is the result of a collaboration between the Universities of Göttingen, Heidelberg and Western Australia. It has been created as a platform to share digitised individual refugee data (1975-2008) obtained from publicly held records as originally recorded by the Office of Refugee Resettlement.

I am still trying to find a comparable dataset for arrivals in Israel. If I can't find anything, I can restrict my analysis to Soviet --> U.S. emigration.

## Concept 2: Correlation Between Lung Cancer and Pollution in the U.S.<a name="cancer-and-pollution"></a>
<img align="right" width="120" src="icon_cancer.png" alt="Cancer icon">

**Background**<br/>
Both my parents (non-smokers) developed lung cancer in the last 10 years; my dad passed away from his cancer this past summer. My parents have a number of friends, also non-smokers, who were diagnosed with lung cancer in their 80's. All of these people grew up in Pittsburgh, Pennsylvania, a city with a long industrial history in the coal and steel industries.

I have heard anecdotally that there's a connection between lung cancer and air pollution, and I'm curious if there is indeed a clear and quantifiable correlation. To do this analysis, I would need to find data on a region's air quality and it's rate of lung cancer (and factor in lag time for the disease to actually develop). Specifically, I would need the following fields of data:

- Year
- County code
- Pollution rate
- Lung cancer rate
- Smoker rate (to remove that bias from the analysis)

**Data Source**<br/>
I've found two data sources that I think might work for this purpose:

- [The CDC's WONDER cancer incidence](https://wonder.cdc.gov/cancer.html). The CDC only began tracking this data in 1999, so I'd be using data from 2000 - 2020.  According to some preliminary research I've done, there is a 20-30 year latency period between exposure to carcinogens and diagnosis of lung cancer. Consequently, if I wanted to use air pollution data from 1970 = 2000.

- [EPA Air Qualtiy Data](https://www.epa.gov/outdoor-air-quality-data). I can use this dataset to find emissions of SO2, which is released when fossil fules containing sulphur are burned; this includes coal-fired power plants, steel mills, and oil refineries. I'm speculating that these particular emmissions are related to cancer rates.


## Concept 3: Prevalance of Hot Flashes During Perimenopause<a name="menopause"></a>
<img align="right" width="120" src="icon_menopause.png" alt="CMenopause icon">

**Background**<br/>
Over the past few years, menopause has gone from a "hush-hush" theme to a hot topic, with a number of mainstream media outlets publishing featured stories about menopause and Hormone Replacement Therapy. For many of my female friends in their early 50's, menopause (or more specifically peri=menopause, which is the transition period leading up to menopause) is a dominant theme. Many women in this demographic are now seeking out Hormone Replacement Therapy to treat symptoms such as brain fog, sleeplessness and hot flashes. However, I'm curious how pervasive these symptoms truly are. I would love to know if there are any patterns or correlations, particularly when it comes to hot flashes. When do they typically occur? How frequently do they occur? Are they related to stress or other factors?

I suspect that robust datasets concerning menopause symptoms will emerge with the rise of wearable technologies (e.g. the Oura ring), but for now, data seems to be relatively scarce. However, I was able to find one dataset -- the [Swan Study](https://www.swanstudy.org/) -- that may provide some answers.

**Data Source**<br/>

The Study of Women's Health Across the Nation (SWAN) is co-sponsored by *The National Institutes of Health*,*The National Institute on Aging*, *The National Institute of Nursing Research*, *The Office of Research on Women's Health*, and *The National Center for Complementary and Alternative Medicine*. Between 1994 and 1997, the intiative tracked 3,302 participants affiliated with 7 research centers. 

One of the limitations of the dataset is that the original survey does not query for number of hot flashes for day. What it *does* ask is the following question: *"How many days in the past 2 weeks have you had a hot flash?*, with ansswers following into 4 buckets:

- 1-5 days
- 6-8 days
- 9-13 days
- Every day

Using responses to this question, I could build an analysis on an ordinal scale of ranges rather than daily frequency. I could also disaggregate and analyze the data by race, exercise levels, and stress levels.

