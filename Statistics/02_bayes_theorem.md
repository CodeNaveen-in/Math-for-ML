# Bayes Therorem

- It is a mathemetical formula used to determine the conditional probability of an event based on prior knowledge and new evidence.
- It adjusts probabilities when new information comes in and helps making better decisions.
- Also called Bayes Rule or Bayes Law
- Statement wise 
  - The conditional probability of an event A, given the occurance of another event B, is equal to the product of the probability B, given A, and the probability of A divided by the probability of event B.

$$
P (A | B) = \frac {P (B | A) \times P(A)}{P (B)}
$$

- P (A) and P (B) are the probabilites of event A and B.
- P (A|B) is the probability of event A when event B happens.
- P (B|A) is the probability of event B when A happens.

## Statement 
Let E1, E2,…, En be a set of events associated with the sample space S, in which all the events E1, E2,…, En have a non-zero probability of occurrence. All the events E1, E2,…, E form a partition of S. 

Let A be an event in space S for which we have to find the probability, then according to Bayes theorem,

$$
P (E_i | A) = \frac {P(E_i) \cdot P(A | E_i)} {\sum^n_\text{k=1} P(E_k) \cdot P (A | E_k)}
$$

Also called formula for probability of causes.

## Terms 

### Hypotheses
- They are possible events or outcomes in the sample space.
- They are denoted as $E_1$, $E_2$, $E_3$,.... $E_n$.
- Each of hypotheses represents a disinct scenario that could explain an observed event.

### Priori Probability
- It is the initial probability of an event occuring before any new data is taken into account.
- Denoted as $P(E_i)$
- It reflects existing knowledge or assumptions about event.
- *(The probabilty of a person having a disease before taking a test)*

### Posterior Probability
- It is the updated probability of an event after considering new information.
- It is denoted with $P(E_i | A)$ is the updated probability of an event after considering new information.
- It is derived from Bayes Therorem.
- *(The probability of having a disease given a positive test result)*

### Conditional Probability 
- The Probability of an event A based on the occurance of another evnet B is termed as probability
- It is denoted by P(A|B)

### Joint Probability 
- Probability of the two or more event occuring together and at the same time.
- It is denoted by $(P (A \cap B))$

### Random Variables
- Real World variables when possible values are determined by random experiments are called random variables.
- Probability of finding such variables is the experimental probability.

## Applications of Bayes theorem
- AI and Machine learning *(Using Naive Bayes classifiers)*
- Medical Testing


## Bayes theorem vs Conditional Probability

| Bayes Theorem	| Conditional Probability| 
| ------------- | ----------------------- |
| Bayes's Theorem is derived using the definition of conditional probability. It is used to find the reverse probability.	| Conditional Probability is the probability of event A when event B has already occurred.| 
| Formula: P(A/B) = [P(B/A) × P(A)] / P(B) | Formula: P(A/B) = P(A ∩ B) / P(B) |
| Purpose: To update the probability of an event based on new evidence.|  Purpose: To find the probability of one event based on the occurrence of another.| 
| Focus: Uses prior knowledge and evidence to compute a revised probability.| Focus: Direct relationship between two events.| 

`Bayes' Theorem helps us update probabilities based on prior knowledge and new evidence`

## Example
### Question
A person has undertaken a job. The probabilities of completion of the job on time with and without rain are 0.44 and 0.9, and 5, respectively. If the probability that it will rain is 0.45, then determine the probability that the job will be completed on time.

### Solution

- Let E1 be the event that the mining job will be completed on time and E2 be the event that it rains. We have,

- P(A) = 0.45,
P(no rain) = P(B) = 1 − P(A) = 1 − 0.45 = 0.55

- By multiplication law of probability,
P(E1) = 0.44, and P(E2) = 0.95

- Since, events A and B form partitions of the sample space S, by total probability theorem, we have

- P(E) = P(A) P(E1) + P(B) P(E2)
- ⇒ P(E) = 0.45 × 0.44 + 0.55 × 0.95
- ⇒ P(E) = 0.198 + 0.5225 = 0.7205

So, the probability that the job will be completed on time is 0.7205

## Tools used
Probability in Data Science is implemented using libraries like 
- **NumPy** for numerical operations and random simulation. 
- **Pandas** for organizing data and SciPy for working with probability distributions and statistical tests. 
- **PyMC** or **Scikit-learn** (for Naive Bayes models) for Bayesian analysis are often used. 
- **Matplotlib** and **Seaborn** are used to make visualisations to make probabilistic insights easier to interpret.

| Task	| Probability Concept| 
| ------ | ------------------ |****
| Classifying outcomes	| Conditional probability| 
| Measuring uncertainty	| Probability distributions| 
| Making predictions	Naive Bayes, | Logistic Regression| 
| Decision-making under uncertainty	| Bayesian inference| 
| Simulating random events	| Monte Carlo simulations| 