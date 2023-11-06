# Deep Learning Model Performance Report for Alphabet Soup
***Overview of the Analysis*** <br>
The purpose of this analysis is to evaluate the performance of two deep learning models created for Alphabet Soup, a non-profit organization. The goal is to predict whether applicants will be successful if funded, based on various features from their applications. This classification problem can help the organization allocate resources more effectively to increase the success rate of their funding initiatives.

# Results
***Data Preprocessing***<br>
*Target Variable:*
- The target variable for both models is "IS_SUCCESSFUL," which represents the success (1) or failure (0) of funding an applicant.<br>

*Features:*
- The features used for the models include all columns in the dataset except "EIN" and "NAME," which are non-beneficial ID columns. These features are used to predict the success of funding.<br>

*Removed Variables:*
- In the initial model, some categorical variables were transformed into dummy variables for model input. In the optimization model, the "EIN" column was dropped, and the "NAME" column was binned and replaced with a "Other" category.

***Compiling, Training, and Evaluating the Model***<br>

*Initial Model:*<br>
![image](https://github.com/RachaelCaldwell/deep-learning-challenge/assets/134207637/b3e9b7ea-35c7-42bb-bd56-17d60b5a182e)

- Number of Input Features: 43
- Number of Hidden Layers: 2
- Number of Neurons in Hidden Layers: 80 (Layer 1) and 30 (Layer 2)
- Activation Function: ReLU for hidden layers and Sigmoid for the output layer
- Loss Function: Binary Crossentropy
- Optimizer: Adam
- The initial model was trained with 100 epochs, achieving an accuracy of approximately 72.42%.
![image](https://github.com/RachaelCaldwell/deep-learning-challenge/assets/134207637/e098a36b-110c-4757-a1fa-a46cf4a177b6)

*Optimization Model:*

- Number of Input Features: 43
- Number of Hidden Layers: 3
- Number of Neurons in Hidden Layers: 7 (Layer 1), 14 (Layer 2), and 21 (Layer 3)
- Activation Function: ReLU for hidden layers and Sigmoid for the output layer
- Loss Function: Binary Crossentropy
- Optimizer: Adam
- The optimization model was trained with 100 epochs, achieving an accuracy of approximately 77.92%.

***Summary***<br>
The initial deep learning model achieved an accuracy of 72.42%, which falls short of the target model performance. Three optimization models were used to improve model performance. The final optimization model was created by increasing the number of hidden layers and neurons where the "EIN" column was dropped and the "NAME" column was binned. This optimization resulted in a higher accuracy of 77.92%.

***Recommendation for a Different Model***<br>
While the optimization model demonstrated an improvement in accuracy, an alternative approach that could potentially yield better results with more advanced neural network architectures or machine learning algorithms could be a Random Forest Classifier. A Random Forest Classifier can handle both numerical and categorical data. It can be trained on the same preprocessed dataset and may provide a more interpretable model with better predictive performance.
