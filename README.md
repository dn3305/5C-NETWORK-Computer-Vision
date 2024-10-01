Overview:
This project focuses on brain MRI image segmentation using two models: Attention U-Net and U-Net++. Both were trained and evaluated using PyTorch to segment tumor areas in brain MRIs.

Dependencies:
Python 3.7
PyTorch
Albumentations (for data augmentation)
OpenCV (for image processing)
Matplotlib (for visualization)
Data Preparation
The dataset (MRI images and masks) can be found here. The data is split into training, validation, and test sets, with augmentations applied.

Models:
Attention U-Net: Incorporates attention mechanisms for improved segmentation by focusing on relevant features.
U-Net++: Extends U-Net with nested skip connections to capture more fine-grained details.
Loss Function
We used Dice Loss to measure the similarity between the predicted and true masks.

Training:
The models were trained for multiple epochs using optimizers such as Adam and Adamax. The Dice Coefficient was used to track progress.

Visualization:
Both models' predictions were visualized and compared against the ground truth masks from the test dataset.

Saving Models:
You can save and load models using:

python:
torch.save(model.state_dict(), 'model.pth')
How to Run
Clone the repository.
Install dependencies using pip install -r requirements.txt.
Download and update the dataset paths in the notebook.
Run the training script to train the models.
Use the saved weights for inference.
