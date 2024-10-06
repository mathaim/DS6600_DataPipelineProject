# DS6600_DataPipelineProject: UVA Board of Visitors and UVIMCO Leadership Dashboard

#### Introduction (6 points): describes the general topic and purpose for collecting and working with the proposed data.

![image](https://github.com/user-attachments/assets/ef782aa3-de8e-4f55-a9fb-cdde6c62c793)

While there was a long history of violence happening in Israel, Palestine, and surrounding territories, the situation culminated to become a point of international discourse in the past year. In February of 2024, UVA students passed a [referendum](https://studentelections.virginia.edu/form/uva-apartheid-divest-2024) calling on the school to disclose its financial ties to Israel and divest.n The referendum passed with 68% of the vote. Ultimately, the vote itself had no real power because the managing of the school's investments is up to the UVA Investment Management Company (UVIMCO) who creates the portfolio and the Board of Visitors who approve it. 

Later in the spring of 2024, students created encampments in colleges across America to prompt school administration to disclose and divest financing Israel in the context of the human rights violations it committed. The University of Virginia was no exception. The encampment itself was forcibly cleared out by Virginia state police, with the approval of President Jim Ryan. 

Jason Armesto publised a [story](https://dailyprogress.com/news/local/education/uva-will-not-be-divesting-from-israel/article_ccb031dc-721b-11ef-bfc3-db148d7affbc.html) with The Daily Progress on the state of affairs. On Friday, September 9, 2024 the Board of Visitors gathered and made it clear they would not be divesting from asset managers and companies that invest in Israel. The Chief Operating Officer of UVIMCO, Kristina Alimard, stated “Our primary objective is to generate strong adjusted returns for the University of Virginia. We do not utilize divestment or negative screens for nonfinancial reasons.” CEO of UVIMCO Robert Durdern cited a combination of difficulty and unwillingness as the reasons for not divesting. 

It seems like a slap in the face of UVA's mission of doing both great and good, if we are profitting off of an ongoing genocide. UVIMCO's [Investor Responsibility Framework](https://uvimco.org/wp-content/uploads/2022/03/Investor-Responsibility-Framework.pdf) addresses the global issue of climate change but nothing else. 

#### Background (6 points): reviews existing related work including published articles and public datasets, with citations for both.
I don't know if a dashboard exists that is comparable to what I want to do. I would imagine if there is it isn't very well-known. The closest thing is probably articles about politicians or other people in power, exposing something about their past. 

#### Data (6 points): lists potential sources for raw data, with citations, along with descriptions of the mechanism through which each data source shares data (through an API, web-scraping, a CSV file, etc.). Also, find and describe the licensing information for each data source to determine whether and under what restrictions you are allowed to use the data.
The dataset that this dashboard relies on will be novel. It will require pulling from newsapi.org and webscraping of: 
- [voting history](https://www.elections.virginia.gov/candidatepac-info/client-services/)
- LinkedIn profiles
- [criminal records](https://vsp.virginia.gov/services/criminal-background/)
- publicly available business records via [Department of Professional and Occupation Regulation](https://www.dpor.virginia.gov/RecordsandDocuments) and [State Corporation Commission
Clerk's Information System](https://cis.scc.virginia.gov/)
- [court records](https://www.uscourts.gov/court-records/find-case-pacer#:~:text=Federal%20case%20files%20are%20maintained,Register%20for%20a%20PACER%20account.)
  
As we discussed in class, the legality of such webscraping seems to be a point of contention in the courts. 


#### Potential analyses (6 points): identifies the key features/variables in the data sources listed in the previous section and provides some thoughts on the kinds of analyses that you would like to include on a public-facing dashboard. (Note: when I say “analysis”, I don’t necessarily mean machine learning. You are free to use ML or other heavy models, if you have the background and desire to do so, but these analyses can be simple, exploratory, and descriptive like cross-tabs, histograms, and correlation tables as these simple analyses usually are very effective at communicating key ideas.)

1. **Gather information on who the members of the Board of Visitors:** The dashboard should serve as a resource in better understanding the people in these positions of power. The [link](https://bov.virginia.edu/people) on UVA's websites highlights career accomplishments and paints them in a very positive light, but I hope to go beyond that with this dashboard. What have they done in their careers? Do they hold any public political views? What is their voting history? Have they ever been sued? In essence, what is their digital footprint? I don't necessarily have expectations on what I will find because this is a very open ended question. I will probably end up using some type of NLP to synthesize text if I find anything particularly verbose. 
2. **Provide people who use my dashboard with the opportunity to express disappointment to these members:** My primary motivation for this project is not related to data wrangling. I hope to build a tool that prompts users' names and email addresses and automates an email to the 12 members. This email would express disappointment in their actions and highlight how their decision to not divest goes against UVA's mission of doing both great and good. 


#### Challenges (6 points): discusses what some of the biggest challenges may be as you proceed through the rest of the project. If you are not sure that something within your plan will work out, describe an alternative plan to quickly turn to in case the original plan doesn’t succeed.
