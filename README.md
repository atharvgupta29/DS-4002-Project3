# DS-4002-Project3

Identifying our photos among celebrity photos. Class project #3

## H2 
This repository has 5 folders. The README.md file contains all of the information someone would need to replicate our project. The LICENSE file talks about the licensing and how to cite our project. The Scripts folder contains the code to show how we got our results. The Data file tells you about the data and how to retrieve it (it was too large to store on GitHub). Lastly, the Output file shows the output of our logistic regression model.

# Section 1
  We used Google Colab (Python) for this project. The packages that were installed to use our code were pandas, matplotlib, google.colab, os, PIL, collections, pillow_heif, _______________________________. Our project was performed on Windows laptops.

 
=======
# Section 2
```bash
├── Data
│   ├── Data.md
├── LICENSE
├── Output
│   ├── Output.md
├── README.md
├── Scripts
│   ├── DS_4002_MI3.ipynb
```
  
  # Section 3
1) There are two options for this project. You can either fully replicate the experiment by downloading from the original sources and then adding your own files. Alternatively, you can use the sample we have provided of 500 celeb images and 75 images of our group photos.
   
1a) To access the data, go to this website: https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html. For the dataset, scroll down until you see a zip file that is named "Align&Cropped Images". You will then want to use some pictures that you have taken of yourself or a particular individual/group of individuals. Add these folders to your Google Drive. You will need to run your selected photos through an indicated chunk of code to make them the same size as the photos in the celebrity dataset.

1b) Download the file from the Data folder. 

**Regardless of whichever path you choose**, for the attributes we used in the EDA, scroll until you see the txt file that is named "Attributes Annotations". Once it directs you to a Google Drive, click on the "Anno" folder and then click on the "list_attr_celeba.txt" file to download.

2) Navigate to the ____________________.ipynb file in the Scripts folder. Open our notebook in Google Colab. If you are using the GitHub subset, upload the downloaded data file to your Google Colab environment so it is available when running the notebook. Otherwise, follow the steps to read the data in from your Google Drive. The cells you should run will have comments depending on which path you chose. 

3) Run the notebook: execute initial cells in order for preliminary data processing. The only thing we did was change the -1s to be 0s. Therefore, if the attribute was present in the photo, it reported a 1; else, a 0.

4) Reproduce the exploratory data analysis by running the EDA cells. These will produce a stacked bar chart that shows the amount of young/old people and whether they have blonde har. Our other plot shows the number of blurry photos. 

5) After EDA, we performed more thorough data cleaning. We removed the blurry photos from our dataset. We also took a sample of 500 images to account for class imbalance.

6) The next step is to train and evaluate the model. We then split the data into training and test sets (80/20, stratified). To make sure we had a specific number of our group photos we split them into training and testing before combining them together. Subsequently, we built a CNN that we trained to select our photos. Finally, we then trained the model and evaluated using a confusion matrix, classification report (precision, recall, F1), and ROC-AUC. The notebook also outputs the top predictive words for each class.

7) Model performance should be close to: Accuracy = _________________, ROC-AUC ≈ _______________, F1 (Good) ≈ ______________, F1 (Not Good) ≈ ________________. Small variation may occur due to randomness in the train/test splitting and due to the specific sample. 
  
  # References
[1] “Cross Validation in Machine Learning” GeeksforGeeksI, August 4, 2025. [Online]. Available:
	https://www.geeksforgeeks.org/machine-learning/cross-validation-machine-learning/.
	 [Accessed: Sep. 19, 2025]
   
[2] Grullón-Paz, “Recalled Pet Food May Be Linked to 130 Dog Deaths, F.D.A. Says”
New York Times, para. 1-2, August 19, 2021. [Online], Available: https://www.nytimes.com/2021/08/19/business/midwestern-pet-food-fda.html [Accessed Sept. 11, 2025].

[3] J.. Ni, J. Li, and J. McAuley, “Justifying recommendations using distantly-labeled reviews and fine-grained   
aspects,” Empirical Methods in Natural Language Processing (EMNLP), 2019. [Online]. Available:      https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/. [Accessed: Sep. 12, 2025].

[4] S. Thixton, “45 Pet Food Recalls over the Past Five Years,” Truth About Pet Food, July 17, 2025. [Online],
	Available: https://truthaboutpetfood.com/45-pet-food-recalls-over-the-past-five-years/. [Accessed Sept. 11, 
	2025].

[5] “Text Classification using Logistic Regression,” GeeksforGeeks, Jul. 23, 2025. [Online]. Available: 
https://www.geeksforgeeks.org/machine-learning/text-classification-using-logistic-regression/.[Accessed: Sep. 12, 2025].

[6] “Understanding TF-IDF (Term Frequency-Inverse Document Frequency)”, GeeksforGeeks, August 13, 2025. 
