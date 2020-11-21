# Climate-Resilient-Agriculture-w-Machine-Learning
IWD


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
  --image_dir=./dataset
If you're using the provided dataset, it may take up to three hours.

Classifying
To test classification, use the following command:

python3 classify.py path/to/image.jpg
Using webcam (demo)
To use webcam, use the following command:

