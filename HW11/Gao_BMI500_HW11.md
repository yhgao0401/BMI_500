Author: Yuhe GAO, Email: yuhe.gao@emory.edu

Question 1 is selected in this HW.

Please refer Gao_BMI500_HW11.ipynb for codes details.

====SIR-model=====
Analysis and Interpretation:
Infection peak: the Infection reaches the peak at around 38-39 days, where the new infections equal recoveries, namely dI/dt=0, \beta*S=\gamma. Based on assigned \beta and \gamma, the critical threshold is \gamma/\beta=333 people in the Susceptible group. And our total population is 1000, S_initial is 999, once S decreases to 333, the infection peak is reached. And if with the same \beta and \gamma setting, but total_population less than 333, no peak will show.

Basic reproductive number: R_0=\beta/\gamma = 0.003. Given the S_initial=999, the number of people who may get infected by the initial infected person is 0.003*999=3, indicating the infection would spread out. Therefore, to lower \beta, the transmission rate (such as using face masks, keeping social distance), increase \gamma, the recovery rate (such as improving hospitalization, medications), and lower susceptible population (such as taking vaccines) are the main directions to control an infectious disease.

Pandemic Dynamics:
The Susceptible population only decreases over time, and falls faster before the infection peak than later. There were a few people who never got infected.
The Recovery population only increases over time, and grows faster around the infection peak, and then gradually flattens the trend. It reflects the cumulated population who get infected and recover.
The Infected population increases at the beginning, reaches its peak when new infections=recoveries, and decreases after the peak. It starts with 0 and ends with 0. 

====SEIR-model======
The infected population comes to its peak around 60 days (N of infections is around 180), and drops to a lower level (infection N = 30-40). And later, there is a small flat peak around 250 days (infection N around 60). When looking into the plot with a 1200-day range, after this small peak, the level of the infected population is steady around 50.

It can be seen that there is a latency for exposed people and the actual infected people. Unlike the SIR model categorizes the population directly into susceptible and infected, SEIR involves an intermediate group of exposed, which mimics the real-world scenario, and lower infected population than the SIR model.

Introducing birth/death rate into the pandemic model helps to simulate the changes in a more realistic long-term trend. It guarantees new population coming into the Susceptible group. In the SIR model, the population is fixed. When people get infected from susceptible and then finally recover, they will be immune, and no changes will happen. Involving birth/death rate, SEIR mimics the situation that allows the infectious disease to co-exist with people.


As dicussed before, implications for public health interventions can happens on \gamma or \beta. From the sensitivety analysis, to control the pandemic on ethier peak population or total infections, the lower transmission rate or higher recovery rate are expected. With \gamma represent the recovery rate, focusing on improving hospitalization, medication, good rest, etc. can help to increase the recovery rate, and limit the infection. With \beta represents the transmission rate, applying social distance, using face masks, contactless interaction will help to constrain the transmission and contril the spread.