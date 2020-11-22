# Climate-Resilient-Agriculture-w-Machine-Learning
IWD

### CROP HEALTH
Using Docker

docker build -t hands-classifier .
docker run -it hands-classifier bash

Install using PIP
pip3 install -r requirements.txt

Training
To train the model, use the following command (see framework github link for more command options):

python3 train.py \
  --bottleneck_dir=logs/bottlenecks \
  --how_many_training_steps=2000 \
  --model_dir=inception \
  --summaries_dir=logs/training_summaries/basic \
  --output_graph=logs/trained_graph.pb \
  --output_labels=logs/trained_labels.txt \
  --image_dir=./datasets crophealth 
If you're using the provided dataset, it may take up to three hours.

Classifying
To test classification, use the following command:

python3 classify.py path/to/image.jpg
Using webcam (demo)
To use webcam, use the following command:

### seedsFeatureExtraction.ipynb
We will use the data to help classify breast tumors as benign or malign

We have 569 observations with 33 variables

Ten real-valued features are computed for each cell nucleus:

-radius (mean of distances from center to points on the perimeter)
-texture (standard deviation of gray-scale values)
-perimeter
-area
-smoothness (local variation in radius lengths)
-compactness (perimeter^2 / area - 1.0)
-concavity (severity of concave portions of the contour)
-concave points (number of concave portions of the contour)
-symmetry
-fractal dimension (“coastline approximation” - 1)
-SVM technique has been used to model the data
