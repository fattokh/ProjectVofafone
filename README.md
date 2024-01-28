Exam project in Scientific Computing With Python A.Y. 2023/2024

Course number: INQ2100742

Professor: Alberto Zucchetta

Assistant: Dr. Rocco Ardino

Group members:

- Andrea Sandbu Numme (student ID: 2099720)
- Anna Matzen (student ID: 2099629)
- Antonin Zeman (student ID: 2100168)
- Fattokh Bakhtiyor Ugli Sadriddinov (student ID: 2085453)

The following text is part of the given project description:
Analysis of Vodafone users' fluxes

The study of the flux of people inside urban areas is of paramount importance to achieve an optimal understanding of emerging critical issues in the local mobility, and to explore areas of potential improvements in the infrastructures and local transports.

The mobility of users within and toward Padova has been monitored using the data provided by the Vodafone mobile carrier, which provides the information based on the users' connections to the network cells. The data provided by the carrier encompasses the monitoring of the users connected to the Vodafone network in Padova in a four-month period from February to May of 2018.

To provide statistical insights on the number and the flow of users, the data is aggregated based on the origin and movements of the users by averaging the number of connections during the time of the monitoring.

To further avoid privacy violation issues, all observations with less than 30 units (e.g. day-areas for which <

30 users have contributed) have been discarded and/or merged into dedicated categories (indicated with "altro", or "other").
Datasets

The data is provided in .csv files.

    day_od.csv: table of the origins and destinations of the users averaged by the day of the week. The data is provided with details of the month, type of user (resident in Padova/Italian visitor/foreign visitor), country of provenance, together with the province and comune of the user (if available).
    distinct_users_day.csv: table of the number of distinct users by origin. The data is provided with details of the month, type of user (resident in Padova/Italian visitor/foreign visitor), country of provenance, together with the province and comune of the user (if available).

The information is stored in the fields according to the following scheme:

    MONTH: month analyzed
    DOW: day analyzed
    ORIGIN: users' origin area (do not consider this field)
    DESTINATION: users' destination area (do not consider this field)
    CUST_CLASS: user type (resident / Italian visitor / foreigner visitor)
    COD_COUNTRY: users' country code (e.g. 222=Italy)
    COD_PRO: users' province code (e.g. 12=Varese)
    PRO_COM: users' comune code (e.g. 12026=Busto Arsizio)
    FLOW: number of movements for given date-time (with a minimum of 30 users)
    VISITORS: overall number of users

Together with the data files, three lookup-tables are provided to allow matching the Italian institute of STATistics (ISTAT) country, province and comune codes to the actual names.

    codici_istat_comune.csv: lookup file containing the mapping between comune ISTAT code-names
    codici_istat_provincia.csv: lookup file containing the mapping between province ISTAT code-names
    codici_nazioni.csv: lookup file containing mapping the country code to its name
