# Ticketmaster Ticket Pricing Strategies

* Ticket pricing is a topic that is largely unexplored at Ticketmaster because it is generally not the one to set the price. The Data Science Division at Ticketmaster is very interested in insights into how to price tickets. Currently the ticket prices for a touring artist are roughly the same at every performance location, i.e. there is little to no optimization done on pricing tickets based on location. Ticketmaster is very interested in determining the popularity of certain geographic locations for certain types of events and for certain types of people so that it can use this information for ticket price optimization. In order to provide pricing strategies, we studied three factors that affected the amount of ticket sold: geological location of tickets sold, population density of where tickets sold, and time difference between the event date and date of tickets sold.
 

### Data Description

* All of the data presented are web-based statistics. While the files look quite different from each other, the data are generated through the same process. When customers visit a website and the website loads, several javascript scripts are run during the loading process. This collect of scripts (referred to internally as a pixel) records the user's actions on the website and sends the resulting data to an external database. 
 
* The dataset we were using is "Purchase Data". Each row in the purchase dataset represents a purchase from Ticketmaster. This dataset contains information on what event the purchase was for, the type and date of event, cost of tickets, etc. 

### Recommendations

We found that income and population of a state are important factors that are relevant to the total tickets sold and should be considered when constructing a pricing optimization model. Several states, such as California and New York, generally sell better than the other states, and raising ticket prices in these states could potentially bring up revenue. Moreover, tickets sold more close to the event date, suggesting another potential price optimization factor.


### Contributors

Rosy(Pu) Zhou

Jiayun Luo

Sylvia Pan

Cindy Zheng 

Samuel Chen

Yilin Ye
