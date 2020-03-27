**You call 3 friends who live in Seattle and ask each of them independently whether Seattle is raining. Each of your friends has 2/3 chance telling you the truth while 1/3 chance mess with you by lying. You get 3 Yes from your friends. You also know that in any given day, there is 25% Seattle is raining. What is the probability that Seattle is actually raining?**
* Use Bayes' rule. P(rain | 3 Yes) = P(3 Yes| rain)* P(rain)/P(3 Yes) = P(3 Yes| rain)* P(rain) / (P(3 Yes| rain)* P(rain) + P(3 Yes| not rain)* P(not rain)) = (2/3)^3 * 1/4 / ((2/3)^3 * 1/4 + (1/3)^3 * 3/4)) = 8/11

**A new quantum message system has 0.8 probability of 0.8 of success in any attempt to send a message through. Calculate the of having 7 successes in 10 attempt?**
* Binomial distribution. <img src="https://latex.codecogs.com/gif.latex?P(X&space;=&space;7)&space;=&space;\binom{10}{7}&space;*&space;0.8^7&space;*&space;0.2^3&space;=&space;0.20133" title="P(X = 7) = \binom{10}{7} * 0.8^7 * 0.2^3 = 0.20133" />
