# Courier-Selection-Optimization

Problem: The problem arises in the supply chain for an e-commerce company where company which delivers to different part of the country have different delivery partners. All these deliver partner have different TATs, Prices, Sources, Destinations and strength in different part of countries. The idea was to select the delivery partner for particular region related to the warehouse of the company so that the TAT could be reduced in optimum price and hence the customer gets the product as early as possible.

Such supply chain problems are simply solved by three stage procedure as follows:

1. Data Segregation: First I took the raw data, from the company and the order with pincode and sourcewarehouse. I matched it with the couriers. The way couriers divide the region are in five categories mainly A,B,C,D and E which depends upon the reachability, accessibilty and distance from the source warehouse. The based on the price list weight and sizewise I created a column to categories the price and region code for making it easy to understand and train for model. I tried to refined and expand data as much as possible.

Note: I did first tested the efficacy of this solution using a sample code for code generated dataset. It is uploaded as well. For real code and I have upload the sample columns which you can generate digital the dataset for training, for privacy reason, I can't upload the real dataset.

2. Model: After the data is ready i trained a model, for test model I just used simple regression but for real data different models were used to train different parameters. But mainly parameters were TAT and price. Over that I even used region codes defined by delivery partner and grouped it by each delivery partner. So at the end of trained model we had values for each delivery partner from each warehouse to all the region with specified TAT and price based upon order weight.

3. Optimization and generation: The model is base for optimization. Based on value the minimization of TAT and price. Hence I used the PULP library to get optimization functions and hence using that I printed the out at top four delivery partners based upon their trained values from the model for specific source-destination pair. The destination can be a state or if we want to map can be pincode too.

Real Data Sample:

![image](https://github.com/user-attachments/assets/f18df4e2-ed8f-4a47-9e93-e831fdbece8d)

