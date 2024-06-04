# AI-Image-Classifier

## About
We have built an AI-Image classifier app .This app successfully classifies images as Real or AI-generated fake image. The app also shows the p-scores of the classification with respect to it being real. This feature not only retains the transparency of the result but also carries important information. Images with borderline p-scores around 0.5 signifies that the image maybe a blend. 

For example tests against real images edited using AI-features resulted in p-values in range 0.6-0.8 approximately which says that it is primarily real but has some synthetic features to it in contrast to purely real phtotgraphs where p-score is usually above 0.95. 

## Architecture used:
So we had looked through various architectures for this specific task and decided to use pretrained models to achieve state-of-art performance.
So we decided to take-up pretarined models built on the purpose of image classification like VCG-16 and InceptionV3. We froze the base CNN layers, added fully connected layers at the output side for binary classification. We also had some binary imbalance in our scrapped data so we implemented SMOTE to make the training unbiased. Finally we decided to go with InceptionV3.

### why InceptionV3 over VCG-16 and others?
One of the main reasons is the use of Inception modules which can perform convolutions with multiple filter-sizes simultaneously which provides for better generalizations. It also uses auxiliary classifiers which prevent overfitting. It also uses factorization to reduce the no. of parameters and hence improve computational costs.


<img width="696" alt="Screenshot 2024-01-03 121416" src="https://github.com/anishhello/home-doc-assistant/assets/133523672/98473ecf-2e6a-40df-b985-26a68080f04c">

