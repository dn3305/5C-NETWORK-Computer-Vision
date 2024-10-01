Overview
This project focuses on brain MRI image segmentation using two deep learning models: Attention U-Net and U-Net++. Both models were trained and evaluated on a brain MRI dataset using PyTorch, aiming to achieve high accuracy in segmenting regions of interest (tumor areas).

Dependencies
To run the project, you need:

Python 3.7
PyTorch
Albumentations (for data augmentation)
OpenCV (for image processing)
Matplotlib (for visualization)
Data Preparation
The dataset consists of MRI images and their corresponding masks. We split the data into training, validation, and test sets, applying data augmentation techniques such as flipping, rotation, and scaling using Albumentations.
https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation/data can be found here

Models
Attention U-Net
Attention U-Net improves segmentation performance by applying attention mechanisms to focus on relevant image features during upsampling.

U-Net++
U-Net++ enhances U-Net by using nested dense skip connections, making it more capable of capturing fine-grained details.

Loss Function
We used Dice Loss, designed for segmentation tasks to minimize the difference between predicted masks and ground truth masks.

Training
Both models were trained for multiple epochs with optimizers like Adam and Adamax. Training progress is tracked using Dice Coefficient as a metric.

Visualization
Predictions were visualized using test data, comparing ground truth masks with predicted masks from both models.

Saving Models
Both models can be saved and loaded using:

torch.save(model.state_dict(), 'model.pth')

Results


How to Run
Clone the repository.
Install the dependencies using pip install -r requirements.txt.
Download the dataset and update the paths in the notebook.
Run the training script to train the models.
Use the saved weights to load the models for inference.
