**1.You are given a fair coin. On average, how many flips would you need to get two of the same flip in a row (either 2 heads in a row or 2 tails in a row)?**
* Expected Flips = 2 * 1/2 + 3 * 1/4 + 4 * 1/8 + .... = 3. Refer [the post](https://math.stackexchange.com/questions/112726/tossing-a-fair-coin-until-two-consecutive-tosses-are-the-same) for detailed explanation.

**2.What is the probability of rolling a total of sum 4 with two dice?**
* There are total 36 ways to throw. 3 ways can sum to 4: (1,3),(2,2),(3,1). So 3/36 = 1/12

**3.What is the probability of rolling at least one 4 with two dice?**
* We have 10 ways to have only one dice to be 4. 1 way to have both dice to be 4. so, p = 11/36

**4.You have two jars, 50 red marbles, 50 blue marbles. You need to place all marbles into the jars so that when you blindly pick a marble out of one jar, you maximize the chances of selecting a red marble. How would you distribute the marbles into two jars?**
* Place only one red marble into jar 1, and place the remaining marbles into jar 2. So, p = 1/2 * 1 + 1/2 * 49/99 = 0.7475

**5.If the probability of seeing a car on the highway in 30 minutes is 0.95, what is the probability of seeing a car on highway in 10 minutes?(Assume a constant default probability)**
* "constant default probability" means "the probability of observing a car in any given non-overlapping time interval of equal length are equal and independent". Let's assume the probability of seeing no car in 10 minutes is P. So, observing at least one car in 30 minutes is 1-P^3 = 0.95. That is, P = 0.37 and observing at least one car in 10 minutes is 1-P=0.67
* Or, cars arriving in a highway can be modeled by a Poisson process. For details, please refer to the [post](https://www.quora.com/If-the-probability-of-observing-a-car-in-30-minutes-on-a-highway-is-0-95-what-is-the-probability-of-observing-a-car-in-10-minutes-assuming-constant-default-probability)
