# Recession-Indicator

###  As of 09-2022, the United States has a 0.087% chance of heading into a recession within the next month. 

---

The model looks at each month and gives a percentage represent the likelihood of the United States entering a recession for the next month. It's typically 0.00%, but it'll sometimes be 0.1% or 0.2%. Once it gets above 1.0%, it's time to take notice. 

The model tends to start rising from 0.0% when a recession is coming. 

| Visualizing The Model |
| :-------------: |
| The recession indicator model tends to start rising from 0 when a recession is coming, and equal 1 when a recession is in full swing. ![Preview](https://i.imgur.com/tY3HhZJ.jpg)      |
| A recession is occurring when the NBER value is 1. ![Preview](https://i.imgur.com/JecIIou.jpg)      | 
| Overlapping the indicator model graph and the actual recession graph. ![Preview](https://i.imgur.com/IAoGDmO.jpg) |


Overfitting possibility? Most definitely. But when the model was trained on recession data before the Great Recession, it was still able to predict the recession and subsequent market pull-backs in 2008 and 2020. 

---



### Python libraries needed can be installed using Anaconda on Windows. 
* numpy
* pandas
* keras (needs tensorflow and theano, with tensorflow being the backend to keras)



### Steps for running: 
1. Run compile_data.py once country data is properly renamed and placed in the folder. 
2. Run ANN_recession.py   
    * Percentage for current recession will be given, and percentages for all previous months will be output to US_recession_percentages.csv  
    * If you want to train the model yourself, delete "recession_indicator_model.h5", and run ANN_recession.py again. 
