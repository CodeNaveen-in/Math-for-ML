# Conditional Probability
- It is the probability of an event occuring based on a given condition or prior knowledge of another event.
- In layman terms it's the likelihood of an event occuring *(given another one has already occured)*.

### Question
**What are the chances that its raining given that you carry an umbrella?**

**Given:** 

- It rains 30% of the time 
- You carry an umbrella 50% of the time 
- When it rains, you carry an umbrella 80% of the time 

**Implies (for 10 days scenario):**
- 3 out of 10 days are rainy. (since 30% of 10 = 3)
- 5 out of 10 days you carry an umbrella. (since 50% of 10 = 5)
- On rainy days, you carry it 2 out of 3 days (since 80% of 3 ~ 2)

**Total Umbrella Days:**
- Rainy days: 2 out of 3 
- Sunny days: 3 out of 7.
- Total umbrella days = 5 (matching the 50% probability).

**Conditional Probability:**
- Out of all umbrella days (5), only 2 days were rainy.
Thus, P(Rain | Carry Umbrella) = 2/5 = 40%.

## Formula
$$
P(A \mid B) = \frac{P(A \cap B)}{P(A)}
$$

- $P (A \cap B)$ : probability of both A and B occuring simultaneously.
- $P(A)$ : the probability of event A occuring

## Questions
To calculate the conditional probability, we can use the following step-by-step method:

- **Step 1**: Identify the Events. Let's call them Event A and Event B.
- **Step 2**: Determine the Probability of Event A i.e., P(A)
- **Step 3**: Determine the Probability of Event B i.e., P(B)
- **Step 4**: Determine the Probability of Event A and B i.e., P(A ∩ B).
- **Step 5**: Apply the Conditional Probability Formula and calculate the required probability.

## Examples
- **Tossing a coin (Independent Event)**
  - Let's consider two events in tossing two coins,
  - A: Getting a head on the first coin.
  - B: Getting a head on the second coin.Sample space for tossing two coins is:
  - S = {HH, HT, TH, TT}
  - The conditional probability of getting a head on the second coin (B) given that we got a head on the first coin (A) is = P(B|A).
  - Since the coins are independent (one coin's outcome does not affect the other), P(B|A) = P(B) = 0.5 (50%), which is the probability of getting a head on a single coin toss.
- **Drawing a card (Dependent Event)**
  - In a deck of 52 cards where two cards are being drawn, then let's consider the events be.
  - A: Drawing a red card on the first draw, and
  - B: Drawing a red card on the second draw.
  - The conditional probability of drawing a red card on the second draw (B) given that we drew a red card on the first draw (A) is = P(B|A) 
  - After drawing a red card on the first draw, there are 25 red cards and 51 cards remaining in the deck.
So, P(B|A) = 25/51 ≈ 0.49 (approximately 49%).

## Properties of Conditional Probabality
1. Let's consider an event A in any sample space S of an experiment. 
   
   $P(S|A) = P(A|A) = 1$
2. For any two events A and B of a sample space S, and an event X such that P(X) $\neq$ 0,
    
    $P((A \cap B)| X) = P (A | X) + P (B | X) - P ((A \cap B)| X)$
3. The order of sets or events is important in conditional probability i.e. 

    $P(B | A) \neq P (B | A)$
4. The complement formula for probability only holds conditional probability if it is given in the context for the fisrt argument i.e.
    $P(A' | B) \eq 1 - P(A | B)$
    $P(A | B') \neq 1 - P(A | B)$

5. For any of the two or three independent events, the intersection of events can be calculated using the following formula.
   - For events A and B intersection $P(A \cap B) = P (A) P(B)$
   - For the intersection of three events A, B, C, $P(A \cap B \cap C) = P(A) P(B) P(C)$

## For Indepdendent Events
- For independent events their conditional probability is the same as probability of the event individually.
- For independet events A and B, the conditional probability of A and B concerning each other is : 
  - P (B | A) = P(B)
  - P (A | B) = P(A)

## Conditional vs Joint vs Marginal Proability

| Parameter	| Conditional Probability	| Joint Probability	| Marginal Probability| 
| ---------- | ----------------- | ----------- | ---------- |
| Definition	| The probability of an event occurring is given. That another event has already occurred.	| The probability of two or more events occurring simultaneously.	| The probability of an event occurring without considering any other events.| 
| Calculation	| P (A | B)	| P (A ∩ B)	| P(A)
| Variables involved	| Two or more events	| Two or more events	| Single event.| 

## Multiplication Rule of the Probability 
- It helps us calculate the probability of the intersection of two events when the probability of one event depends on the occurance of other events.
- This rule is crucial in understanding the joint probability of events under specific conditions.

$$
P (A \cap B) = P(A) \times P(B / A)
$$

- $P (A \cap B)$ - This denotes the probability that both events A and B occur simultaneously.
- $P (A)$ - This represent the probability of event A happening.
- $P (B | A)$ - This is the conditional probability of event B occuring given that event A has already started.

## Applications
- Finance and Risk Management 
  - *(Assesing probability of a default for a borrower given certain financial indicators)*
- Healthcare Diagnostics
  - *(Determining probability of a patient having a specific disease given the result of the diagnostics)*

## Practice Question
### Question 
A bag contains 5 red balls and 7 blue balls. Two balls are drawn without replacement. What is the probability that the second ball drawn is red, given that the first ball drawn was red?

### Solution

- Let the events be,

- Event A: The first ball drawn is red.
- Event B: The second ball drawn is red.

P(A) = 5/12 and P(B) = 4/11 (as first ball drawn is already red, thus only 4 red balls remain in the bag)

Therefore, probability of the second ball drawn being red given that the first ball drawn was red is 4/11.