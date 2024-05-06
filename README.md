# Multi-Armed Bandit Reinforcement Learning Project
## Overview
This project focuses on implementing and comparing three different algorithms for solving the Multi-Armed Bandit problem. The goal is to determine the most optimal advertisement type out of ten available options (Ad1 to Ad10). The algorithms we’ll compare are:

- Algoritma A/B Testing: A classic approach where we randomly assign users to different ads and measure their performance.
- Epsilon Greedy: An exploration-exploitation strategy that balances between trying new ads (exploration) and exploiting the best-performing ad (exploitation).
- Adaptive Epsilon Greedy: Similar to Epsilon Greedy, but with a dynamically adjusted exploration rate.

## Project Structure
```
├── data/
│   ├── Ads_CTR_Optimisation.csv                       # CSV file containing ad performance data
├── notebooks/
│   ├── Jupyter File.ipynb                             # Algorithm comparison and evaluation
├── TA
│   ├── Paulinus A. S. Jamlu 193114033.pdf             # Tugas Akhir
├── README.md                                          # Project documentation
```
## Getting Started
Clone this repository to your local machine.
Install the required libraries using pip install -r requirements.txt.
Explore the data in Ads_CTR_Optimisation.csv to understand the ad performance metrics.
Run the notebooks in the notebooks/ directory to analyze the data and compare the algorithms.
## Usage
Modify the parameters (e.g., epsilon, l,f, number of iteration/loop) in Jupyter File.ipynb as needed.
Run the bandit algorithms using the provided data.
Evaluate the performance of each algorithm using relevant metrics (e.g., click-through rate, conversion rate).
## Determining Optimal Ad Type
To evaluate the performance of each algorithm, consider the following metrics:

1. Total Click-Through Rate (CTR):
    - Calculate the total CTR for each ad type over multiple iterations.
    - Choose the ad type with the highest total CTR as the most optimal.
2. Regret:
   - Regret measures how much potential reward is lost by not selecting the best-performing ad at each step.
   - Minimize regret by selecting the ad type that maximizes cumulative rewards over time.
## Results
After conducting experiments and analyzing the performance of different algorithms, we observed the following:

1. Adaptive Epsilon Greedy:
   * This algorithm adapts its exploration rate dynamically based on the observed rewards. It aims to strike a balance between exploration (trying out different ads) and exploitation (choosing the best-performing ad).
   * Optimal Ad Type: The adaptive epsilon greedy algorithm identified the most optimal ad type with a high degree of confidence.
   * Complexity: However, it is worth noting that the adaptive epsilon greedy algorithm is more complex to implement and tune compared to other methods.
2. Algoritma A/B Testing:
   * A classic approach where users are randomly assigned to different ads, and their performance is measured.
   * Optimal Ad Type: While A/B testing provides a straightforward way to compare ads, it may not always identify the optimal ad type with high certainty.
   * Simplicity: A/B testing is simpler to set up and understand, making it a good choice for scenarios where complexity is a concern.
3. Epsilon Greedy:
   * This algorithm balances exploration and exploitation by randomly selecting an ad with a certain probability (epsilon) and choosing the best-performing ad otherwise.
   * Optimal Ad Type: Epsilon Greedy falls between the other two algorithms in terms of both performance and complexity.
   *  Intermediate Difficulty: It offers a moderate level of complexity, making it a suitable choice for scenarios where a balance between simplicity and sophistication is desired.
In summary, if you prefer a simpler approach and are willing to accept some uncertainty, A/B testing is a suitable choice. However, if you want a more sophisticated solution that adapts over time, Adaptive Epsilon Greedy is the way to go.

* Compares the Average Total CTR
  
![image](https://github.com/Alanjamlu34/Multi-Armed-Bandit-TA/assets/142156489/bea42ffa-6e8a-46bb-859c-e0e343553f05)

* Compares the Average Total Regret
  
![image](https://github.com/Alanjamlu34/Multi-Armed-Bandit-TA/assets/142156489/ce9a45bf-8dc0-43b3-988f-b1504ed10a1f)

Remember to adjust the parameters and evaluate the algorithms based on relevant metrics.
> [!TIP] 
> While all algorithms consistently identified Ad5 as the optimal ad type, it’s essential to consider the impact of randomness. Since the algorithms operate based on random exploration, we recommend running them for a large number of iterations (e.g., 500 iterations) and then averaging the results. By doing so, we can reduce the influence of occasional variations due to randomness.

> [!IMPORTANT]
> In some cases, the algorithms may yield slightly different results (e.g., identifying Ad8 as optimal a few times), but these differences are not statistically significant (occurring less than 5 times). Therefore, we can confidently eliminate such outliers.

## Acknowledgments
Special thanks to the open-source community and the authors of relevant research papers.

Good luck with your project! 🚀🤖
