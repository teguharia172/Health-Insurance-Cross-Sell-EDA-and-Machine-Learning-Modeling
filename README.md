# Health-Insurance-Cross-Sell-EDA-and-Machine-Learning-Modeling
This is a  note book of exploratory data analysis on cross selling of health insurance customers on  vehicle insurance product  and using machine learning to predict whether a customer is interested or not in vehicle insurancen



## Background Information :

- an Insurance company that provide Health Insurance to its customers, usually they offer other insurance product to the customers through diffirent kind of marketing channel. In this case we will build a model to predict   whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.


## Problem Statement:

- Un optimize customer reachout process, many insurance worker spend a lot of their time having meeting with prospective client without knowing the probabily of that customer to buy the insurance product


## Business Goals:

- Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue


## Business Question:

- How does age of a vehicle determing the response of vehicle insurance advertisment
- How to attract customers from different generation 
- what's the major factor that make a health insurance customer not intersted with vehicle insurance 
- What's the best machine Learning modeling for this Cross Sell case


## Workflow :

- Data Cleaning
  - Recategorize Data
  - Binning  
  
- Exploratory Data Analysis to Answer business Question

- Feature Engineering & Selection For Machine Learning Process 
  - Encoding all the categorical features 
  - Checking correlation between dependent and independet variable
  - Feature Selection
 
 
- Model Building :
  - Splitting data into Training and Testing
  - Apllying the **SMOTE** (Synthetic Minority Oversampling Technique) to the minority target since the data is imbalance 
  - Creating base model of classification algorithm ( Logistic Regression, KNN Classifier, Decision Tree Classifier, Random Forest Clasifier)
  - Check The Evaluation matrix for all the base model
  - HyperParameter tuning
  - Checking Evaluation Matrix for tuned Model
  - Choose which model has the best recall score for this case 


<details>
  <summary><h2> Click to see the conclusion and recommendation </h2></summary>
  
## Conclusion:
  
  
- From this dataset of health insurance customers almost **95%** of customers have a vehicle age that's less than 2 years. from our analysis, customers who has more than 2 years of vehicle age are more interested with vehicle insurance advertisment, while customers who has less then one year of vehicle age, only **4%** of them are actually interesred with vehicle insurance 


- We found out that customer who already have vehicle insurance are almost have no interest in another vehicle insurance. Our analysis shows that **99.9% of customers that have a vehicle insurance is not interested in another vehicle insurance**, while customer who doesn't have a vehicle insurance **22.5 %** of them are interested with vehicle insurance


- we also found out that a newer vehicle are more likely to have a vehicle insurance, with vehicle that's less than one year **66% of those are insured** , vehicle that's older than one year but less than 2 years are **33% insured**,  while less than **one percent** of vehicle that's older than 2 years are insured. This should explain why customer who owns a newer vehicle are less likely to be intersted with insurance promotion, because they probably alredy have one.


- **Customers who never had vehicle damaged** only 0.5 % of those customers are intersted with vehicle insurance, **87%** of customers who never had any vehicle damaged already have a vehicle insurance


- **Which Customer Generation are less likely to be intersted with vehicle insurance** the answer is **Millenials** (people in age group of 18 - 34) only **6% of millenials are actually interested with vehicle insurance**, and why is so? 
    1. almost **63% of millenials already have vehicle insurance**, from our analysis before owning vehicle insurance is a major factor why someone is not interested with another vehicle insurance
    
    2. **90% of millenials have a vehicle that's less than one year of age**, and from our analysis before that vehicle that's less than one year are **66% already insured**

This conculed that millenials are more likely to already have a vehicle insurance before our vehicle insurance team approached, and that's a major factor why millenials are least likely to be interested with our vehicle insurance, because they already have one


#### So who's actually interested with our vehicle insurance ? 

From the responses there are **12 % of our health insurance customers are interested with the vehicle insurance product** but who are those people?

1. **First, Customer who does not have a a vehicle insurance**, out of all customers who does not have a vehicle insurance  **22.5 %** of them says that they're interested with vehicle insurance product


2. **customers who has vehicle that's older than 2 years** our analysis before mentioned that only less than **one percent** of car that's older than 2 years are previouly insured, by not having a vehicle insurance they're more likely to be intersted with our vehicle insurance, our data show's that customer who has car that's more than 2 years are **7 times** more likely to be intersted with vehicle insurance compared to customer who own a vehicle less than one year


3. **customers who have had a vehicle damaged in the past** from our analysis we found out that **97%** customers who actually intersted with vehicle insurance have had their vehicle damaged in the past
    1. **95 % of customers who have had vehicle damage in the past still doesn't have a vehicle insurance**
    

**Which Customer Generation that's most likely to be interested in Vehicle insurance ?**
   - **GEN X** (Age Gen X : 35 - 50)
       - our analysis shows that GEN X has the highest percentage to be intersteed with vehicle insurance, to be precise, **21 %** of GEN X are interested with vehicle insurance 
       
       - This might be because **72% GEN X** does not have a vehicle insurace, and GEN X has the highest percentage of vehicle damager the past **(67%)** among other generation



<b>Machine learning could predict whether a customer would be interested or not towards vehicle insurance product with recall 0.965 out of 1</b>

Using logiistic regression that has been tuned, we focus more on recall instead of accuracy here because of we want to reduce the false negative ( The customer who actually interested but the model predicted that customer is not intrested). Since this kind of problem could lead into lost of potential revenue


## Recommendation



### 1. Work with dealership to capture millenial market


as we know from the analysis that millenials are less likely to be intersted with vehicle insurance because of most of them have a vehicle that's less than one year of age, and vehicle with less then one year of age are most likely to be insured so in conclution they already have one, and so they're not interested. By working together with a dealership that sells a brand new car, we could tackle this problem, our insurance company could have a bundling product of brand new vehicle and a free promotional vehicle insurance for certain period of months. we hope that by working together with vehicle dealership we could target more millenials customers.

### 2. Target & Educate Customers Who had Vehicle Damage in the past

**95%** customers who have had a vehicle damaged in the past still does not have a vehicle insurance this is a gold mine for our vehicle insurance, since customers are more likely to be interested in vehicle insurance if they've a vehicle damage in the past. 


 we could to a targeted marketing to this customers, by showing the benefits of having a vehicle insurance and how it will protect you if you ever had a vehicle damaged in the future


### 3. Benfits for customer who has a vehicle that's more than 2 years

having an older vehicle means having more problem compared to newer vehicle, problems like overheating, radiator problem and, etc are common with older cars, fixing those kind of stuff could be costly or having problem like that in the middle of a road could be troublesome. **Since only less than one percent** of customer who's actually owned car that's older than 2 years and insured, we could focus more on the problems that car over two years might have and the pain point of customers that owned older car and we should construct the benefits on those pain points, since **customer with vehicle age over 2 years** are the most likely to be intersted with vehicle insurance



### 4. Use Machine Learning Algorith to have predict the response outcome of a customer

Using the Logistic regression machine learning that has recall of 96.5 % will speed up and find out which customer who actually intersted in vehicle insurance, and we could focus our resource just based on the customers that's interested
</details>



<details>
  <summary><h2> Click to see the the Analysis </h2></summary>

### How does an age of customers vehicle determine the response of vehicle insurance advertisement

![alt-text-2](https://user-images.githubusercontent.com/57277832/97105794-504b3400-16f0-11eb-80a8-c03317a22ea8.png)

-  95% of customers have vehicle that's less than 2 years, the table above it shows that, customers who has more than 2 years of vehicle age are more interested with vehicle insurance advertisment, while customers who has less then one year of vehicle age, only **4%** of them are actually interesred with vehicle insurance 

### Why does customer who have a newer car are less likely to be intersted with vechicle insurance

![image](https://user-images.githubusercontent.com/57277832/97105939-1a5a7f80-16f1-11eb-90bb-4567e10c1280.png)

- **66% Customer who has car for less than one year** are already insuring their vehicle, while customers who has a vehicle that's older than 2 years, **less than one percent of them are insuring their vehicle**   

## Major Factors that makes a customer not intersted with vehicle insurance product

### Customer who already owned a vehicle insurance product is not interested with another one 

![image](https://user-images.githubusercontent.com/57277832/97106036-e3d13480-16f1-11eb-977f-75e68bbe5a81.png)


- **Almost Every Customer who already have vehicle insurance is not interested with another one**

### Customer who never had a vehicle damage is also not interested  with vehicle insurance 
![image](https://user-images.githubusercontent.com/57277832/97106237-ebdda400-16f2-11eb-9299-73b59a72c77e.png)

![image](https://user-images.githubusercontent.com/57277832/97106249-0283fb00-16f3-11eb-9c59-ff8bdbac698c.png)


- as we can see from the table and the chart above that only **0.5 %** of customers that never had any vehicle damaged are intersted with vehicle insurance product 

### How to attract customers from different generation 

Before we start with the analysis of **how to attract customers from different generation** we are going to define the age group of each generation since we don't have generation columns at the begining 

#### Generation Group :
- Millenials : 18 - 34
- Gen X : 35 - 50
- Boomer : 51 - 69
- Silent : 70 and Above

### Generation and Response 

lets start by looking to the response of vehicle insurance advertisment towards every generation

![image](https://user-images.githubusercontent.com/57277832/97106509-a621db00-16f4-11eb-878b-358d42bb555f.png)

from the table above we see that millenials are the least likely to be interested with vehicle insurance, **only 6 % of millenials are actually interested with vehicle insurance**.


**While Gen X** seems to be the generation that's most likely to be interested **(21%)** with vehicle insurance, followed by boomer **(14%)**, and silent **(7%)** Generation

### Why do millenials are the least likely to be interested with vehicle insurance 

first we have to look at what generation that most likely already have a vehicle insurance before being approached by our vehicle insurace marketing team

**1.**


![image](https://user-images.githubusercontent.com/57277832/97106694-c4d4a180-16f5-11eb-9098-c41f5633bec1.png)

![image](https://user-images.githubusercontent.com/57277832/97106748-01080200-16f6-11eb-9de2-bce35e4f39e5.png)

this might be one of the reason why millenials are least likely to be interested with vehicle insurance from our company, because **63% of millenials already have vehicle insurace**, and this explain why Gen X has the highest interested response, **72% Gen X generation does not have a vehicle insurace**, and from our analysis before owning a vehicle insurance is a major factor why someone is not interested with another vehicle insurance 



**2**

![image](https://user-images.githubusercontent.com/57277832/97106932-1a5d7e00-16f7-11eb-898d-3fc6d13cce38.png)


![image](https://user-images.githubusercontent.com/57277832/97106947-39f4a680-16f7-11eb-80ae-4471abc3e830.png)


Second reason might be age of the vehicle, **90 % of millenials owned a vehicle that's less than one year** and from our analysis **66%** of vehicle tha's less than one year is already insured.

While for **Gen X** majority of the customers owned a vehicle that's 1 to 2 years old which have (**32%**) of being insured and gen X are more likely to have vehicle that's older than 2 years compared to millenials

### What Machine Algorithm that work the best when it comes to classfying customers response

![image](https://user-images.githubusercontent.com/57277832/97107105-52b18c00-16f8-11eb-9736-00678e84e0a6.png)


This table above is evaluation matrix on all the algorithm after hyperparameter tuning, **we are going to focus more on recall** instead of accuracy here because we want to reduce the false **negative ( The customer who actually interested but the model predicted that customer is not interested)** since those kind of problem will lead into lost of potential revenue

it clearly shows that **logistic Regression** has the best recall score with 0.965 recall score, please take a look at the machine learning modeling notebook for this classification cause if you need more details on the machine learning process, Thank you
