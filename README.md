<h1>
  Star-galaxy classification using ensembled CNNs
</h1>


🌟 Classify stellar sources in images to stars or galaxies using CNNs
<br> 📈 Investigate the performance of different models: DenseNet121, EfficientNetV2B0, MobileNetV3Small, and ensemble architectures.

<img src="https://github.com/phanuphatsrisukhawasu/star-galaxy-image-classification/blob/main/banner-example-prediction.jpeg?raw=true" alt="Example Prediction of Ensembled CNNs">

[![Python](https://img.shields.io/static/v1?message=Python&logo=python&labelColor=5c5c5c&color=3776AB&logoColor=white&label=%20)](https://www.python.org/)
[![Jupyter](https://img.shields.io/static/v1?message=Jupyter&logo=jupyter&labelColor=5c5c5c&color=F37626&logoColor=white&label=%20)](https://jupyter.org/)
[![TensorFlow](https://img.shields.io/static/v1?message=TensorFlow&logo=tensorflow&labelColor=5c5c5c&color=FF6F00&logoColor=white&label=%20)](https://www.tensorflow.org/)

<u>Note</u>: I provided all codes used in this project on the Jupyter Notebook [here](https://github.com/phanuphatsrisukhawasu/star-galaxy-image-classification/blob/main/star-galaxy-classification.ipynb).

<h2>
  🔎 Motivation
</h2>

As you may see in the above pictures, distinguishing between stars and galaxies in unprocessed stellar sources captured from astronomical instruments is tremendously challenging, even for experts. However, identifying these sources could lead to significant discoveries in astrophysics, as stars with galaxy properties, or vice-versa, are rare. Studying them will help leverage our understanding of the universe by tons of degrees.

<h2>
  🛠️ Methods
</h2>

In this project, I investigate the performance of different CNN architectures in identifying the source type. First, I would like to extend my sincere gratitude to the author of the dataset utilized in this project, Divyansh Agrawal (the dataset is available on Kaggle [here](www.kaggle.com/datasets/divyansh22/dummy-astronomy-data)). I used this dataset for all experiments.

In brief, I train different architectures: DenseNet121, EfficientNetV2B0, and MobileNetV3Small by fine-tuning their layers from the pre-trained weights on the ImageNet dataset. The ensemble CNN predicts by averaging the output of all models, resulting in voted prediction.

<h2>
  📊 Summarized Results
</h2>
  
I evaluated the performance of each model based on the classification accuracy, precision, recall, F1 Score, and AUC Score. We presented the full results in the notebook. At a glance, the performance of our ensembled CNNs shows a higher AUC and precision than any others.

<image src="https://github.com/phanuphatsrisukhawasu/star-galaxy-image-classification/blob/main/roc-curve.png?raw=true" alt_text="ROC Curve">
  
**Figure 1**: ROC Curve of the ensembled model with the highest AUC Score.

<image src="https://github.com/phanuphatsrisukhawasu/star-galaxy-image-classification/blob/main/confusion-matrix.png?raw=true" alt_text="Confusion Matrix">
  
**Figure 2**: Confusion matrix of the ensembled model showing some misclassification due to the imbalanced dataset.

<h2>
  🧑🏻‍🏫 References
</h2>

Agrawal, Divyansh. “Star-Galaxy Classification Data.” *Kaggle*, 12 June 2021, www.kaggle.com/datasets/divyansh22/dummy-astronomy-data. 
