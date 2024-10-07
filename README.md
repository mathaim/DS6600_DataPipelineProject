# DS6600_DataPipelineProject: Salary Ttransparency UVA Board of Visitors and UVIMCO Leadership Dashboard

#### Introduction (6 points): describes the general topic and purpose for collecting and working with the proposed data.

![image](https://github.com/user-attachments/assets/ef782aa3-de8e-4f55-a9fb-cdde6c62c793)

While there was a long history of violence happening in Israel, Palestine, and surrounding territories, the situation culminated to become a point of international discourse in the past year. In February of 2024, UVA students passed a [referendum](https://studentelections.virginia.edu/form/uva-apartheid-divest-2024) calling on the school to disclose its financial ties to Israel and divest.n The referendum passed with 68% of the vote. Ultimately, the vote itself had no real power because the managing of the school's investments is up to the UVA Investment Management Company (UVIMCO) who creates the portfolio and the Board of Visitors who approve it. 

Later in the spring of 2024, students created encampments in colleges across America to prompt school administration to disclose and divest financing Israel in the context of the human rights violations it committed. The University of Virginia was no exception. The encampment itself was forcibly cleared out by Virginia state police, with the approval of President Jim Ryan. 

Jason Armesto publised a [story](https://dailyprogress.com/news/local/education/uva-will-not-be-divesting-from-israel/article_ccb031dc-721b-11ef-bfc3-db148d7affbc.html) with The Daily Progress on the state of affairs. On Friday, September 9, 2024 the Board of Visitors gathered and made it clear they would not be divesting from asset managers and companies that invest in Israel. The Chief Operating Officer of UVIMCO, Kristina Alimard, stated “Our primary objective is to generate strong adjusted returns for the University of Virginia. We do not utilize divestment or negative screens for nonfinancial reasons.” CEO of UVIMCO Robert Durdern cited a combination of difficulty and unwillingness as the reasons for not divesting. 

It seems like a slap in the face of UVA's mission of doing both great and good, if we are profitting off of an ongoing genocide. UVIMCO's [Investor Responsibility Framework](https://uvimco.org/wp-content/uploads/2022/03/Investor-Responsibility-Framework.pdf) addresses the global issue of climate change but nothing else. 

#### Background (6 points): reviews existing related work including published articles and public datasets, with citations for both.
I don't know if a dashboard exists that is comparable to what I want to do. I would imagine if there is it isn't very well-known. The closest thing is probably articles about politicians or other people in power, exposing their salaries and any other relevant info.

This [Forbes list of rich celebrities](https://www.forbes.com/celebrities/list/#tab:overall) relates to the salary transparency component.
- Citation: “The World’s Highest-Paid Celebrities.” Forbes, Forbes Magazine, www.forbes.com/celebrities/list/#tab:overall. Accessed 7 Oct. 2024. 

#### Data (6 points): lists potential sources for raw data, with citations, along with descriptions of the mechanism through which each data source shares data (through an API, web-scraping, a CSV file, etc.). Also, find and describe the licensing information for each data source to determine whether and under what restrictions you are allowed to use the data.
The dataset that this dashboard relies on will be novel and from on the following sources: 
- [Compensation of UVIMCO Members and other Tax Information](https://projects.propublica.org/nonprofits/organizations/562462804) via ProPublica
    - Mechanism: Nonprofit Explorer API
    - Citation:
    - Licesning Information:TBD
    - Restrictions: N/A
- [Compensation of UVA Board of Visitors from their public companies](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) via US Securities and Exchange Committees
    - Mechanism: EDGAR API 
    - Citation: 
    - Licesning Information:TBD
    - Restrictions:Agencies are required to give the public notice of their systems of records by publication in the Federal Register. You may click here to see a list of the SEC's systems of records. The Act also provides individuals with a means by which to seek access to and amendment of their records, although such requests are subject to exemptions as set forth in the Privacy Act. In addition, the Act allows individuals to bring suit against an agency for violating the Privacy Act.
- [News media](https://newsapi.org/docs/get-started) via newsapi.org
    - Mechanism: News API 
    - Citation: 
    - Licesning Information:[MIT License](https://github.com/News-API-gh?tab=repositories) because all of the repos on the official github have an MIT License?
    - Restrictions: N/A    
- [UVA's Board of Visitors Members](https://bov.virginia.edu/people) and [UVIMCO members](https://uvimco.org/leadership-team/)
    - Purpose: Obtain current occupation and photo
    - Mechanism: webscraping
    - Citation:
    - Licesning Information: N/A
    - Restrictions:
      
Sources I wanted to include but cannot for various reasons:
- Voting history via [The Virginia Department of Elections](https://www.elections.virginia.gov/candidatepac-info/client-services/)
    - Mechanism: comma delimited text file
    - Citation: Virginia Dept. of Elections: Client Services, www.elections.virginia.gov/candidatepac-info/client-services/. Accessed 6 Oct. 2024. 
    - Licesning Information:Information within a list of registered voters provided by the Department of Elections may not be posted, or provided to a third party for posting, on the internet as a list, database, or other similar searchable format.
    - Restrictions: The website lists 7 entities who can request this information. Two that I could potentially fall under are (1) Non-profit organizations which promote voter participation and voter registration or (2) Members of the public seeking to promote voter participation and registration by means of a communication or mailing without intimidation or pressure exerted on the recipient (are only eligible to receive a List of Those Who Voted (LTWV). Along with all other goals for this dashboard. I plan to promote voter participation.
- Criminal records via [Virginia State Police](https://vsp.virginia.gov/services/criminal-background/)
    - Mechanism: webscraping
    - Restrictions: Person you are requesting background search on must consent.
 
Sources I may include but need to learn more about if I can share findings:
- Court records via [Public Records Maintained by the Office of the Executive Secretary] 
    - Mechanism: requested from the Director of Legislative and Public Relations, Office of the Executive Secretary, Supreme Court of Virginia, 100 North 9th Street, Richmond, Va. 23219; Tel. 804-786-6455.
    - Citation:
    - Licesning Information:
    - Restrictions:
- Business records via [Department of Professional and Occupation Regulation](https://www.dpor.virginia.gov/RecordsandDocuments) 
    - Mechanism: emailing PublicRecords@dpor.virginia.gov, they likely send a csv file
    - Citation: “Records & Documents.” Virginia Department of Professional and Occupational Regulation, www.dpor.virginia.gov/RecordsandDocuments. Accessed 6 Oct. 2024. 
    - Licesning Information:
    - Restrictions: Unclear yet, but the  State Corporation Commission had the following terms:
      
          - Authorized uses of the CIS include:
      
              - File or submit business entity documents for new and existing businesses
              - Pay business entity annual registration fees
              - Reinstate business entities
              - File Uniform Commercial Code (UCC) and federal lien documents
              - Serve process on the Clerk as statutory agent.
      It is possible the Department of Professional and Occupation Regulation has similar terms in place.

#### Potential analyses (6 points): identifies the key features/variables in the data sources listed in the previous section and provides some thoughts on the kinds of analyses that you would like to include on a public-facing dashboard. (Note: when I say “analysis”, I don’t necessarily mean machine learning. You are free to use ML or other heavy models, if you have the background and desire to do so, but these analyses can be simple, exploratory, and descriptive like cross-tabs, histograms, and correlation tables as these simple analyses usually are very effective at communicating key ideas.)

1. **Gather information on who the members of the Board of Visitors:** The dashboard should serve as a resource in better understanding the people in these positions of power. The links on the [UVA's Board of Visitors Members](https://bov.virginia.edu/people) and [UVIMCO members](https://uvimco.org/leadership-team/) on the websites highlights career accomplishments and paints them in a very positive light, but I hope to go beyond that with this dashboard. What is their annual salary? What have they done in their careers? Do they hold any public political views? What is their voting history? Have they ever been sued? In essence, what is their digital footprint? I want to frame the salary visuation on a scale with what the average professor at UVA makes.
   
2. **Provide people who use my dashboard with the opportunity to express disappointment to these members:** My primary motivation for this project is not related to data wrangling. I hope to build a tool that prompts users' names and email addresses and automates an email to the 12 members. This email would express disappointment in their actions and highlight how their decision to not divest goes against UVA's mission of doing both great and good. 


#### Challenges (6 points): discusses what some of the biggest challenges may be as you proceed through the rest of the project. If you are not sure that something within your plan will work out, describe an alternative plan to quickly turn to in case the original plan doesn’t succeed.
I anticipate a number of logistical challenges beyond the controversial subject matter. Gathering data from these outdated government systems may prove to be a pain with not much benefit if I am not allowed to publish my findings. If that is the case, I will rely primarily on the News API to gather data that I put in the dashboard.
