# AWS ML Pipeline – MNIST Classifier

## Overview
This project demonstrates a complete ML workflow using Python and PyTorch. 
It trains a simple neural network to classify handwritten digits from the MNIST dataset. 
The project is structured for cloud-ready deployment using AWS.

## Tech Stack
- Python 3.10
- PyTorch
- NumPy & Pandas
- Matplotlib
- AWS S3 / SageMaker (optional)
- Jupyter Notebook

## Project Structure
aws-ml-pipeline/
```
├─ data/ # MNIST dataset (ignored in Git)
├─ models/ # Saved PyTorch models (ignored in Git)
├─ notebooks/ # Jupyter notebooks
│ └─ mnist_training.ipynb
├─ src/ # Source code modules
├─ requirements.txt
├─ README.md
├─ LICENSE
```

## Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/hibaalavi3/aws-ml-pipeline.git
cd aws-ml-pipeline
```

2. Create conda environment:
```bash

cd aws-ml-pipeline 
```


## 2. Create conda environment:
```bash 

conda create -n awsml python=3.10
conda activate awsml
pip install -r requirements.txt
```


3. Run the notebook:

Open notebooks/mnist_training.ipynb in Jupyter or VS Code
Train and evaluate the model

AWS S3 Integration (Optional)
import boto3
s3 = boto3.client('s3')
s3.upload_file("../models/simple_mnist.pth", "your-bucket-name", "models/simple_mnist.pth")
