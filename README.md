# FINAL_PROJECT

Machine Learning Individual Report (ReadMe)
Before constructing my Random Forest Classification model for this project, I began by doing some individual research online to see which machine learning models were common when working with medical record data. In this research I was able to determine that the Random Forest Algorithm is still widely used (as well as Naïve Bayes which I found surprising). Source: https://analyticsindiamag.com/top-6-ai-algorithms-in-healthcare/

With this in mind, I began to construct the Random Forest Model. To do this I began by looking back on our CA04 assignment which dealt with Ensemble methods. This assignment gave me the experience I needed to feel comfortable working with the Random Forest algorithm. I chose to search through a large number (about 60) different combinations of hyper-parameters to determine which one would give us optimal results.

In our business context, we determined the optimal performance metric to be recall. We decided this because we put a high amount of importance on avoiding false negatives (type two error). In our context a false negative would mean that we are telling a patient that they are low risk to develop cardiovascular disease when they are actually high risk. As you can imagine, this is a very dangerous outcome, and it is much safer to have more false positives. Ultimately, we decided on this Random Forest model due to it having the highest recall score (83%).

README for Notebook:
This notebook is broken up into sections using notes given in markdown text. The very first portion of the notebook is used to overlay our sleep dataset with the cardiovascular dataset. This first section can be skipped when using the “Combined_Data_Cleaned.csv”.  From here we begin by filling in any remaining null values in the dataset using an imputer method. Next we check the dataset for imbalance in the target variable. 

We then begin to split the data into the target variable and independent variables, dropping duplicative and unnecessary columns, and then finally splitting that data into training and testing subsets. I have then shown one instance of a Random Forest just as a baseline test to see base results and test the methods.

I then loop through a listed set of potential hyperparameters for the Random Forest. From this output I am able to determine the optimal hyperparameters to use in the final model. I then run the final model to get our desired results.

Lastly, we pull out the most important features of the final model. These features are then sorted by importance (based on entropy / impurity measure) and then graphed to display the most important ones. Finally, the model is saved using the pickle library so that we can import it into our DEMO notebook.
