
0X. Research on the data
- S&P Companies & their public price/sales/...
- Startup Companies Information: with web scrapping and scoring, ...
- Economic information: GDP, interest rates, ...
- 

Some data is stored in a database, and the other we simply keep requesting for that.
Each day we keep asking which are the 500 companies (comparing with the database):
- If there is a new one, we produce a new event: sp_company_update

1X. Data Preprocessing
- Which S&P Companies we choose
- Which startup companies we choose
- Which indicators we choose 

2X. Algorithms
- Developing algorithms to create indicators that are useful
- Public the results on KafKa