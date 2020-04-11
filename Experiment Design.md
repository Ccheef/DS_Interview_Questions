**1. Google wants to add a new button to their main search page. How can they determine whether or not people enjoy this new button feature?**
* This type of question is essentially to test A/B testing
* First we decide on metrics to compare across the dual versions of the site we will serve.(Common metrics are DAU,MAU,CTR,Impressions, Engagement, etc...)
* Second step is to prepare two (or more) versions of your site/page. 
* Then serve the different versions of the page to the populations. Make sure the population is randomly splited. 
* Then define the statistical hypothsis test. For example, the metric chosen will be the same for both groups.
* For the hypothesis test you will pre-define your acceptable Type I Error (FPR or alpha) and also the power of the statistical test (1-power II error).
* In practice we will also want to consider factors such as how long to run the experiment (confidence intervals can be used for this). We will also need to decide on a protocol for outliers, such as truncation.
* A/B test is the very large topic, we can learn more through the [class](https://www.udacity.com/course/ab-testing--ud257) and [post](https://www.optimizely.com/optimization-glossary/ab-testing/)
