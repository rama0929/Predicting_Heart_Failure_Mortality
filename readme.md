# Group 3 - Predicting_Heart_Failure_Mortality

## Final Project Part - 1 

## Team Members - Roles 

- Jean Carlo Valderrama - Repository Manager - Square
- Tanner Ormanoski - Machine learning and ETL  - Triangle
-  Arielle Baez - Additional ETL and Tableau Visialization Creator  - Circle
- Corina Taggart / Rafael Amaya - X - Project Contributors 

## Presentation
[![clickhere](https://user-images.githubusercontent.com/39811614/182038239-aedb39ee-12b7-4e14-b919-d4b9b007f1b1.png)](https://docs.google.com/presentation/d/1zz7a-C6wCRbzemPMWhQPOu5Y4kytbCtVtkEbUBhLkXk/edit?usp=sharing)

## Introdution

- Heart disease is the largest leading cause of death in the U.S. killing around 696,962 Americans in 2020. While heart disease is a large umbrella term encompassing many heart conditions, heart failure is a major proponent of it. With this being such a dire condition, it would be advantageous to analyze heart failure and shed light on some of the contributing factors that lead to a  fatal case.

## Project overview 

- University of Central Florida (UCF) Data Analytics Group 3 project analyzed a dataset of patients and 12 variables of causes to make heart failure predictions by using machine learning and visualizations to interpred this 12 features from our heart failure cardiovascular disease data collection from Chico and Jurman . Our project is looking to find factors from our dataset to inform the public in ways that we can help people in the USA by analyzing population, demographics, age, gender, and other factors to help reduce the rate of heart failure mortality caused Cardiovascular disease(CVD).



## Machine Learning Model 

- The purpose of our model is to use logistic regression to predict between two possibilities, either the patient will die between the time of initial contact and check up, or the patient will survive. The logistic regression model was implemented do the binary outcomes of 0 and 1 .A standard 0.25 split was used to train the data. The model initially used 12 variables to determine this. After initially training the model with the 12 variables and testing it the accuracy was at 77%. I then determined that narrowing the variables down would improve the data. Since our samples were limited and we had 12 variables, overfitting was a huge probability. An accuracy test was ran on the training set and the testing set, and the accuracy scores on each did not indicate overfitting. After calculating the importance of the features and sorting them I dropped a number of less important features. Surprisingly, the less important features were high blood pressure, diabetes, anaemia, and sex. Smoking also was not a strong factor in the model’s predictions. That is not to say that there is no information to be gleaned from these factors. As a matter of fact we did some visualizations on these factors. The top three features were time, serum creatinine, and ejection fraction. Creatinine is a chemical compound that is a by product of energy-producing processes in your muscles. High levels of this compound can indicate poor kidney function. Further looking into this matter, I found an issue in the Journal of Cardiac Failure in which the researchers reported findings that demonstrate increases in serum creatinine levels during heart failure hospitalizations are associated with worsened outcomes after discharge. Ejection fraction is a common measure of the hearts performance and pump function. It is the amount of blood the heart pumps with each beat. Hopefully you can now see why these would be important factors. The fourth most important factor is a bit more obvious which is age. 

<img width="197" alt="heart rate top ranking of factos" src="https://user-images.githubusercontent.com/39811614/182394032-bfdb4183-008e-47da-9b43-42575dc34df3.png">

- Through dropping the previously mentioned less important features and using the AdaBoost Classifier algorithm we were able to achieve a much better accuracy score of 82.1 %. In essence AdaBoost iterates and reiterates through the classification process adding more weight to incorrectly classified samples until all the classifications are correct or the max iterations has been reached. Weight is also added to classifiers based on their accuracy. This also gave us an average precision score of 78% and an average recall score of 82%. Since we are dealing with a life and death scenario, recall or sensitivity would hold more importance, because we want to capture all the people who will die due to heart failure. We might have a few that false positives, meaning people who will actually survive that we predicted would not, but this is preferable to missing a few true positives in the pursuit of making sure everyone we predicted as being in mortal peril is actually in mortal peril.   

<img width="222" alt="Screen Shot 2022-08-02 at 10 05 01 AM" src="https://user-images.githubusercontent.com/39811614/182394353-f6ea54ad-7aca-4ea2-8c74-a2344d6342c7.png">

- File source : Heart_Failure/Predicting_Heart_Failure_Mortality.ipynb

<img width="1118" alt="Screen Shot 2022-07-10 at 2 51 29 PM" src="https://user-images.githubusercontent.com/39811614/178158185-2f22bc53-3e70-4cc8-abc6-9e9e33b8638b.png">

<img width="727" alt="Screen Shot 2022-07-10 at 2 54 12 PM" src="https://user-images.githubusercontent.com/39811614/178158246-14828ed0-b507-4c20-99e0-430b0c451677.png">

## Database - Predicting Heart Failure Mortality

- File source : explore_heart_failure_data.ipynb

<img width="1094" alt="Screen Shot 2022-07-10 at 3 09 18 PM" src="https://user-images.githubusercontent.com/39811614/178158726-aa561b0c-91b6-43e4-a14a-011b0ace144e.png">

<img width="1118" alt="Screen Shot 2022-07-10 at 3 10 35 PM" src="https://user-images.githubusercontent.com/39811614/178158732-3acea034-2fdc-4abb-8cc9-0517ce050281.png">

<img width="497" alt="Screen Shot 2022-07-10 at 3 13 54 PM" src="https://user-images.githubusercontent.com/39811614/178158804-dda709ea-67b1-42b6-b018-6c6a249ea326.png">

<img width="1107" alt="Screen Shot 2022-07-10 at 3 12 55 PM" src="https://user-images.githubusercontent.com/39811614/178158809-1bb0cac5-06e7-43f3-a33d-cfe60119f57e.png">

- Total columns after data cleaning ETL.

<img width="734" alt="Screen Shot 2022-08-03 at 7 02 38 PM" src="https://user-images.githubusercontent.com/39811614/182727326-2bec7b05-3f29-4a87-a562-c91e34d478fc.png">


## Tableau Dashboard

- United States Map with the rates of heart failure rates of mortality. 

- Texas and Georgia are the two states with the hightest ratest of heart failure mortality caused by Cardiovascular disease(CVD).

<img width="631" alt="usa" src="https://user-images.githubusercontent.com/39811614/182397178-8b185187-e329-41ab-ba7e-1a365c2a97a9.png">

- Surprisingly, this dataset collection clearly identify time, serum creatine and ejection fraction as the top three relevant features that were found on patients with heart rate failures. In addition, the below gender graph identify that male participants were more affected with heart rate failures than the female participants.

<img width="838" alt="male and female rate findings" src="https://user-images.githubusercontent.com/39811614/182397830-9a9c480b-db62-4607-aa49-5ff471bbd157.png">

- Serum Sodium with either high (Hyponatremia) or low (Hypernatremia) levels of sodium clearly identify male participants as the most affected patients compared to the female participants.

<img width="852" alt="serum sodium findings" src="https://user-images.githubusercontent.com/39811614/182399509-4eeb96cf-dabd-47d0-9197-b767a0bd9cd8.png">


Resources:
Heart Failure Prediction					
https://public.tableau.com/shared/JPMJMC4HQ?:display_count=n&:origin=viz_share_link

Geographic Map 
https://public.tableau.com/views/HeartFailure_GeoData/Sheet4?:language=en-US&:display_count=n&:origin=viz_share_link

## Recommendation for future Analysis

- Due to the limits of our dataset and the public data we were able to find, we were left wanting on a few key points. Such as, what lifestyle habits contribute to heart failure? We more specifically would like to look into diet and activity level. Are sedentary individuals more likely to suffer from heart disease? Furthermore, does poverty play a major role? One would assume so! Healthy habits and eating often require money. The price of a gym membership and organic foods are unobtainable to those who are impoverished. Finally, is heart failure and heart disease detectable in someone’s genetics? If so, how much of a role do genetics play? If my father and grandfather had heart disease, am I bound to the same fate?

- In addition, we would like to find and incorporate other variables from heart failures in further investigations as well as to apply varios methods of machine learning. 


## Resources

- Data set topic:  Heart Failure Prediction

- Data File : heart_failure_clinical_records_dataset.csv

- Data Source: https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data?resource=download

- File source : Heart_Failure/Predicting_Heart_Failure_Mortality.ipynb

- https://dev.socrata.com/foundry/chronicdata.cdc.gov/i2vk-mgdh



