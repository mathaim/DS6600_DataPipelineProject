# DS6600_DataPipelineProject: UVA Board of Visitors Dashboard

#### Introduction (6 points): describes the general topic and purpose for collecting and working with the proposed data.

![image](https://github.com/user-attachments/assets/ef782aa3-de8e-4f55-a9fb-cdde6c62c793)

In the spring of 2024, students created encampments in colleges across America to prompt school administration to disclose and divest financing Israel in the context of the human rights violations it committed. The University of Virginia was no exception. The encampment itself was forcibly cleared out by Virginia state police, with the approval of President Jim Ryan. It sparked a school wide conversation on UVA's role in the context of a genocide.  

On September 13, 2024, Jason Armesto publised a [story](https://dailyprogress.com/news/local/education/uva-will-not-be-divesting-from-israel/article_ccb031dc-721b-11ef-bfc3-db148d7affbc.html) with The Daily Progress on the state of affairs. 

#### Background (6 points): reviews existing related work including published articles and public datasets, with citations for both.


#### Data (6 points): lists potential sources for raw data, with citations, along with descriptions of the mechanism through which each data source shares data (through an API, web-scraping, a CSV file, etc.). Also, find and describe the licensing information for each data source to determine whether and under what restrictions you are allowed to use the data.
The dataset that this dashboard relies on will be novel. It will require webscraping of voting history, LinkedIn profiles, law enforcement records, business records, judicial records, as well as a general google/news media search. As we discussed in class, the legality of such webscraping seems to be a point of contention in the courts. 


#### Potential analyses (6 points): identifies the key features/variables in the data sources listed in the previous section and provides some thoughts on the kinds of analyses that you would like to include on a public-facing dashboard. (Note: when I say “analysis”, I don’t necessarily mean machine learning. You are free to use ML or other heavy models, if you have the background and desire to do so, but these analyses can be simple, exploratory, and descriptive like cross-tabs, histograms, and correlation tables as these simple analyses usually are very effective at communicating key ideas.)

1. **Gather information on who the members of the Board of Visitors:** The dashboard should serve as a resource in better understanding the people in these positions of power. The [link](https://bov.virginia.edu/people) on UVA's websites highlights career accomplishments and paints them in a very positive light, but I hope to go beyond that with this dashboard. What have they done in their careers? Do they hold any public political views? What is their voting history? Have they ever been sued? In essence, what is their digital footprint? I don't necessarily have expectations on what I will find because this is a very open ended question. I will probably end up using some type of NLP to synthesize text if I find anything particularly verbose. 
2. **Provide people who use my dashboard with the opportunity to express disappointment to these members:** My primary motivation for this project is not related to data wrangling. I hope to build a tool that prompts users' names and email addresses and automates an email to the 12 members. This email would express disappointment in their actions and highlight how their decision to not divest goes against UVA's mission of doing both great and good. 


#### Challenges (6 points): discusses what some of the biggest challenges may be as you proceed through the rest of the project. If you are not sure that something within your plan will work out, describe an alternative plan to quickly turn to in case the original plan doesn’t succeed.
