# DS-4002-Project3

Identifying our photos among celebrity photos. Class project #3

## H2 
This repository has 5 folders. The README.md file contains all of the information someone would need to replicate our project. The LICENSE file talks about the licensing and how to cite our project. The Scripts folder contains the code to show how we got our results. The Data file tells you about the data and how to retrieve it (it was too large to store on GitHub). Lastly, the Output file shows the output of our logistic regression model.

# Section 1
  We used Google Colab (Python) for this project. The packages that were installed to use our code were pandas, matplotlib, google.colab, os, PIL, collections, pillow_heif, shutil, pathlib, torch, torch.nn, torch.utils.data, torchvision, sklearn.metrics, matplotlib.pyplot, and torch.nn.functional. Our project was performed on Windows laptops.

 
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
│   ├── Facial Recognition.ipynb
```
  
  # Section 3
1) You will fully replicate the experiment by downloading from the original sources and then adding your own files. To access the data, go to this website: https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html. For the dataset, scroll down until you see a zip file that is named "Align&Cropped Images". You will then want to use some pictures that you have taken of yourself or a particular individual/group of individuals. You will need to run your selected photos through an indicated chunk of code to make them the same size as the photos in the celebrity dataset. Add the data to your Google Drive. These files should be put into My Drive. 
   
2) For the attributes we used in the EDA, scroll until you see the txt file that is named "Attributes Annotations". Once it directs you to a Google Drive, click on the "Anno" folder and then click on the "list_attr_celeba.txt" file to download.

3) Navigate to the Facial Recognition.ipynb file in the Scripts folder. Open your notebook in Google Colab. Follow the steps to read the data in from your Google Drive.

4) Run the notebook: execute initial cells in order for preliminary data processing. The only thing we did was change the -1s to be 0s. Therefore, if the attribute was present in the photo, it reported a 1; else, a 0.

5) Reproduce the exploratory data analysis by running the EDA cells. These will produce a stacked bar chart that shows the number of young/old people and whether they have blonde hair. Our other plot shows the number of blurry photos. 

6) After EDA, we performed more thorough data cleaning. We removed the blurry photos from our dataset. We also took a sample of 500 images to account for class imbalance.

7) The next step is to train and evaluate the model. We then split the data into training and test sets (80/20, stratified). To make sure we had a specific number of our group photos we split them into training and testing before combining them together. Subsequently, we built a CNN that we trained to select our photos. Finally, we then trained the model and evaluated using a confusion matrix, classification report (precision, recall, F1), and ROC-AUC. The notebook also outputs the top predictive words for each class.

8) Model performance should be close to: Accuracy = _________________, ROC-AUC ≈ _______________, F1 (Good) ≈ ______________, F1 (Not Good) ≈ ________________. Small variation may occur due to randomness in the train/test splitting and due to the specific sample. 
  
  # References
[1] 	D. Gargaro, “The pros and cons of facial recognition technology,” ITPro., July 23, 2023. 
		[Online], Available: https://www.itpro.com/security/privacy/356882/the-pros-and-cons-of-facial-recognition-technology. [Accessed Nov. 5, 2025].

[2] 	C. Ranjeeth Kumar, Saranya N, M. Priyadharshini, Derrick Gilchrist E, Kaleel Rahman 
		M, “Face recognition using CNN and siamese network,” ScienceDirect, vol. 27, June 2023. [Abstract], Available: https://www.sciencedirect.com/science/article/pii/S2665917423001368 [Accessed Nov. 		5, 2025]

[3] 	Z. Liu, P. Luo, X. Wang, “Large-scale CelebFaces Attributes (CelebA) Dataset” CUHK Multimedia 
		Lab., July 29, 2016. [Online], Available: https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html [Accessed Nov. 5, 2025]

[4]		K. Rafalski, “CNN Optimization: Strategies for Enhancing Deep Learning Performance” netguru, 
		Sept. 12, 2025. [Online], Available: https://www.netguru.com/blog/cnn-optimization
		[Accessed Nov. 5, 2025]

[5]		T. Tang, “Class Imbalance Strategies — A Visual Guide with Code” Medium, April 24, 2023. 
		[Online], Available: https://medium.com/data-science/class-imbalance-strategies-a-visual-guide-with-code-8bc8fae71e1a  [Accessed Nov. 14, 2025]

