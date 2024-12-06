# Python-Data-Visualization
Python exercise covering Data Visualization

# Exercise 1: (Score : 4)
# Create a line plot using matplotlib pyplot that displays the population of four different cities over time. Each city should have its own line, 
# and the x-axis should represent years (e.g. 2010, 2011, 2012, etc.) while the y-axis should represent the population.
# The data for the four cities is provided below:
# City A: [500000, 550000, 600000, 650000, 700000, 750000, 800000]
# City B: [800000, 850000, 900000, 950000, 1000000, 1050000, 1100000]
# City C: [1000000, 1050000, 1100000, 1150000, 1200000, 1250000, 1300000]
# City D: [1200000, 1250000, 1300000, 1350000, 1400000, 1450000, 1500000]

import matplotlib.pyplot as plt

years = [2011,2012,2013,2014,2015,2016,2017]
city_a_pop = [500000, 550000, 600000, 650000, 700000, 750000, 800000]
city_b_pop = [800000, 850000, 900000, 950000, 1000000, 1050000, 1100000]
city_c_pop = [1000000, 1050000, 1100000, 1150000, 1200000, 1250000, 1300000]
city_d_pop = [1200000, 1250000, 1300000, 1350000, 1400000, 1450000, 1500000]

plt.plot(years, city_a_pop, color = 'red', label = 'City A', linewidth = 2, marker = '*', linestyle = 'dotted', markersize = 9)
plt.plot(years, city_b_pop, color = 'blue', label = 'City B', linewidth = 2, marker = '*', linestyle = 'dotted', markersize = 9)
plt.plot(years, city_c_pop, color = 'green', label = 'City C', linewidth = 2, marker = '*', linestyle = 'dotted', markersize = 9)
plt.plot(years, city_d_pop, color = 'purple', label = 'City D', linewidth = 2, marker = '*', linestyle = 'dotted', markersize = 9)

plt.title('CITY POPULATION', fontdict={'fontname': 'Arial', 'fontsize': 20})
plt.xlabel('YEARS')
plt.ylabel('POPULATION (millions)')
plt.legend()
plt.grid(True)
plt.figure(figsize=(8, 5), dpi=100)
plt.show()
# plt.savefig('Q1.png', dpi=300)


![DV1](https://github.com/user-attachments/assets/900a6378-93a2-4c16-80f1-bfd6db64a553)


# Exercise 2: (Score : 3)
# Create a scatter plot using seaborn that shows the relationship between the number of hours studied and the test scores obtained by a group of students. Use the following data:
# Hours Studied: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
# Test Scores: [93, 57, 61, 54, 51, 53, 87, 81, 83, 85]

import seaborn as sns
import pandas as pd

hours_studied = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
test_scores = [93, 57, 61, 54, 51, 53, 87, 81, 83, 85]

data = pd.DataFrame({ 
    'Hours Studied': hours_studied, 
    'Test Scores': test_scores 
})

sns.scatterplot(data = data, x = 'Hours Studied', y = 'Test Scores', color = 'blue', marker = 'o')

plt.xlabel('Hours Studied')
plt.ylabel('Test Scores')
plt.title('HRS vs TEST SCORES')
plt.figure(figsize=(8, 5), dpi=100)
plt.show()
# plt.savefig('Q2.png', dpi=300)


![DV2](https://github.com/user-attachments/assets/b7c1a05d-a13c-4de1-9583-95e5b4a3661c)


# Exercise 3: (Score : 3)
# Create a bar chart using matplotlib pyplot that shows the total sales for each month of the year. Use the following data:
# Month: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
# Sales: [11860, 10480, 4997, 5523, 13965, 6011, 13158, 9533, 5158, 9058, 11346, 6675]

# import matplotlib.pyplot as plt

months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
sales = [11860, 10480, 4997, 5523, 13965, 6011, 13158, 9533, 5158, 9058, 11346, 6675]

plt.bar(months,sales,color = 'pink')
plt.xlabel('Month')
plt.ylabel('Sales ($)')
plt.xticks(rotation=60)
plt.title('SALES DATA')
plt.figure(figsize=(8, 5), dpi=100)
plt.show()
# plt.savefig('Q3.png', dpi=300)


![DV3](https://github.com/user-attachments/assets/ef7d49d9-1849-4c88-a373-c7f834d20796)

