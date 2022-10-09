# Telco Customer Churn Prediction
**Customer Churn**: Customer attrition, also known as customer churn, customer turnover, or customer defection, is the loss of clients or customers.<br/>
**Dataset**: [Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)<br/>
Used **Pandas Library** to load the data frame.<br/>
- **Data Cleaning**:
  - Dropping the Customer ID because we don't need that for our model.<br/>
  - Changing the strings into integers and floats.<br/>
  - Data Visualization - 1:
    - understanding the relationship between data and your company is one of the most important parts. This histogram tells us about the relation between the Tenure of each customer and the number of customers in each tenure value.<br/>
    ![image](https://user-images.githubusercontent.com/96788451/194772951-cf4b14e5-8ee3-4f48-800a-a23534be13d6.png)<br/><br/>
  - Data Visualization - 2:
    - Another good insight would be to check the relation between the number of customers and their monthly charges.<br/>
    ![image](https://user-images.githubusercontent.com/96788451/194773052-dfeb81b5-20e5-4016-9374-f68053acd841.png)<br/>
  - Replacing some random strings with integer value of 0 and 1 like ```Male = 1, Female = 0 or Yes = 1, No = 0```. <br/>
  - One Hot Encoding for some columns because their values (strings) variation is high.<br/>
  - Using ```MinMaxScaler()```  to scale the columns with continuous values between 0-1.<br/>
  - Splitting the dataset into two different sets, Training set and Testing set.<br/>
- **Model**:
    ```
    model = Sequential([
    Dense(units= 26, input_shape = (26,), activation = 'relu'),
    #Dense(units= 10, activation = 'relu'),
    Dense(units= 1, activation = 'sigmoid')])
    
    ```<br/>
- **Compilation**:
  
  ```
      model.compile(
      optimizer = 'adam',
      loss = 'binary_crossentropy', 
      metrics = ['accuracy'])
  
  ```
- Trained the model with the** 50 epochs**<br/>
- **Training Results**:
  - After training, the Accuracy of the model is ``` 82.03%```.<br/>
- **Testing Results**:
  - After testing on the testing dataset, the accuracy of the model is ```78.67%```.<br/>
- Created a **Classification Report** to get a complete insight into the model's working during training and testing.<br/>
  ![image](https://user-images.githubusercontent.com/96788451/194773485-508b934a-b736-43e3-b184-5a009b1e8673.png)<br/>
- **Confusion Matrix**: <br/>
    ![image](https://user-images.githubusercontent.com/96788451/194773502-90071e2c-2ac2-4795-a6b5-806a45c4696d.png)



