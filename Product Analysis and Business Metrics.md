These are open-ended questions. I just provide some ideas for solution. <h4> 
-----------------------------------------------------
**1. In 2011 Facebook launched Messenger as a stand alone app for mobile devices (it used to only be part of the Facebook App). How would you track the performance of this new application? What metrics would you use?**
* Daily Active Users(DAU) and Monthly Active Users(MAU): Very common metrics. We can use the metrics to compare before and after the App launched,
to see whether the users have moved to the app. We can also calculate the Stickiness Ratio = DAU / MAU
* Total Time Spent: Also very common metric, especially for the App heavily relies on the advertisement for revenues. 
We can use this metric before and after the launching of the stand alone App to check how users change their engagement
* Number of messages sent and response time for received message: We can use the these metrics to check whether users are more engaged with the App and easier for them to respond the messages as they don't have to login Facebook.
Also remember, having high number of messages sent not necessary a good thing as there might be some technical issues that users have to repeatedly send messages or etc.
* Refer the [link](https://savvyapps.com/blog/mobile-app-analytics) to learn more metrics used for App
  
**2. Google has released a new version of their search algorithm, for which they used A/B testing. During the testing process, engineers realized that the new algorithm was not implemented correctly and returned less relevant results.2 things happened during testing:People in the treatment group performed more queries than the control group, and Advertising revenue was higher in the treatment group as well. What may be the cause of people in the treatment group performing more searches than the control group??**
* We know the new algorithm produced less relevant search results.This means that users may have to make additional searches in order to clarify what they are searching for using the new algorithm.In order to test this hypothesis, we could study how close searches are to each other. If we notice additional searches are done very soon after, we could classify as them clarifying searches.For example, when people search "Apple" for the company, but Google keep showing the fruit, people may have to clarify the key words immediately.

**3. Same setup as question 2. What do you think caused the new algorithm to generate more advertising revenue, even though the results were less relevant?**
* We know that more searches are being conducted, since advertisements are served along with every new search, there are more opportunities for users to click on the advertisement. 
* Another possibility is that the search algorithm is different than the algorithm used to display ads. In this case, the ads themselves may be more relevant than the search results, causing more ad clicks.

**4. Same setup as question 2. Since the less relevant algorithm resulted in higher advertising revenue, should it be implemented anyways?**
* This is a bit of an opinion question, but we should probably not implement this new algorithm.The effects described are probably only short-term effects due to the problems with the algorithm.We shouldn’t sacrifice the long term potential of the site for a temporary increase in revenue and searches.Google is probably best positioned to win in the long term when it has the most relevant search algorithm. 

**5. A car company produces all the cars for a country, we’ll call them Car X and Car Y. 50% of the population drives Car X, the other 50% drives Car Y. Two potential technologies have just been discovered that help reduce gasoline usage. Technology A can increase the MPG of Car X from 50 MPG to 75 MPG, while Technology B can increase the MPG of Car Y from 10 MPG to 11 MPG. Which technology should be implemented to save the most gasoline for the country?**
* Let us assume that the average commute distance for a car in both population is D, then this question has a clear correct answer. 
* Total Gas Used Change with Policy A: (D/50)-(D/75) = D / 150
* Total Gas Used Change with Policy B: (D/10)-(D/11) = D / 110
* D/150 < D/110, so we should implement Technology B
* This is a bot counter intuitive since people at first sight may think 50 to 75 is much more than 10 to 11.

