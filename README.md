# Metro Schedule Optimization for Société de transport de Montréal

## Description
The Societe de transport de Montreal (STM) is a public transport agency that offers transit
services such as buses and metro in the city of Montreal, Quebec, Canada. Established in 1861, it has
grown a large service map comprising of 4 metro lines, 68 metro stations, and 209 bus routes. According
to the Activity Report 2019, the daily ridership of the busiest bus line is 31,209 while the busiest metro
station, Berri-UQAM with an interchange station for three lines, has around 34,630 people entering the
station on a daily basis. However, these numbers change drastically after COVID-19 hit the city of
Montreal. The STM reports that the total number of trips made in 2020 is around 171.7 million, a 54%
decrease from 2019.

STM has made some adjustments to react to the sudden decrease in ridership. For example, it
adjusts the frequency of train departures of orange and green lines from 3 to 4 minutes respectively, but the
blue and yellow lines remain unchanged. Continuing operating the pre-COVID schedule sent STM into
a serious financial crisis. Moreover, based on the survey of transit users conducted by Trajectoire Quebec,
about 25% of users said they would not use transit again, meaning that Montreal is doubling down on
public transport during the pandemic 2021. This information made our group wonder whether STM is
currently operating on a reasonable schedule.

In this project, we limit our scope on examining the operating schedule of the STM metro system.
By optimizing the frequency of departures among different time slots throughout a week, we obtained a
more reasonable operating schedule that meets the current transit demand in Montreal. We also examined
the yellow, orange, blue line’s expansion projects as an extension to our basic model. As the expansion
projects will bring more passengers to the metro service, we want to examine how STM can adjust its
current metro schedule to meet the new demand.

## Data
There are four main parts of data: Operation costs, demand matrix, capacity, and average waiting time. 
Details can be found in the final report. 

To manipulate the data import section in [Project Main Coding](https://github.com/angelach99/Metro_Schedule_Optimization_Montreal/blob/master/Code/MGSC662_Group_Project_Mainmodel_Final.ipynb),
```# Import demand data
demand_blue = pd.read_excel('Demand_estimation_Index_Dec1.xlsx', sheet_name='blue', index_col = 0)
demand_orange = pd.read_excel('Demand_estimation_Index_Dec1.xlsx', sheet_name='orange', index_col = 0)
demand_yellow = pd.read_excel('Demand_estimation_Index_Dec1.xlsx', sheet_name='yellow', index_col = 0)
demand_green = pd.read_excel('Demand_estimation_Index_Dec1.xlsx', sheet_name= 'green', index_col = 0)
```
Notice that the file path is subjected to change after downloading in different location. The demand data is [Here: Demand data](https://github.com/angelach99/Metro_Schedule_Optimization_Montreal/tree/master/Data).

## Reference
Rapport d’activit´e 2020. url: https://www.stm.info/fr/a-propos/informations-entrepriseet-
financieres/rapport-annuel-2020/rapport-dactivite-2020.

STM presents its 2020 Annual Report a year filled with challenges. url: https://www.stm.info/
en/press/press-releases/2021/stm-presents-its-2020-annual-report-a-year-filledwith-
challenges.

COVID-19 – Adjustments to the STM’s bus, m´etro and paratransit service. url: https://www.stm.
info/en/press/press-releases/2020/covid-19---adjustments-to-the-stm-s-bus--metroand-
paratransit-service.

Name. Montreal is doubling down on public transport during the pandemic. July 2021. url: https:
/ / citymonitor . ai / transport / mass - transit / montreal - is - doubling - down - on - public -
transport-during-the-pandemic.

Orange line. url: https://www.stm.info/en/info/networks/metro/orange.

Budgets and reports. url: https : / / www . stm . info / en / about / financial _ and _ corporate _
information/budgets-and-reports.

MR-73. Nov. 2021. url: https://en.wikipedia.org/wiki/MR-73.

MPM-10. Nov. 2021. url: https://en.wikipedia.org/wiki/MPM-10.

Green line. url: https://www.stm.info/en/info/networks/metro/green.

Montreal’s Blue line extension facing major cost overruns, putting project’s future in doubt — CBC
News. May 2021. url: https://www.cbc.ca/news/canada/montreal/montreal- metro- blueline-
1.6022980.
