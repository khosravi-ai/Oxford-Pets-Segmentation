Oxford Pets Segmentation with U-Net

This project implements a simple semantic segmentation model on the Oxford-IIIT Pet Dataset
.
The goal is to train a U-Net model to segment pets (cats and dogs) from the background.

📂 Project Pipeline

Download Dataset

Images (images.tar.gz)

Masks (annotations.tar.gz)

Preprocessing

Remove corrupted/extra files

Resize images and masks to 224×224

Normalize pixel values

Build U-Net Model

Encoder: Conv2D + MaxPooling

Decoder: Conv2DTranspose + Concatenation

Output: 3 classes (cat, dog, background)

Training

Loss: SparseCategoricalCrossentropy

Optimizer: Adam

Metrics: Accuracy + IoU

Callbacks: ModelCheckpoint, EarlyStopping

Results

Mean IoU on test set: 0.94

Mean Pixel Accuracy on test set: 0.94

📊 Sample Output
Input Image	Ground Truth Mask	Predicted Mask

	
	
🚀 How to Run
# Create virtual environment
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate

# Install dependencies
pip install tensorflow opencv-python matplotlib

# Run notebook
jupyter notebook Oxford_Pets_Segmentation.ipynb

📌 Notes

The trained model was saved as .h5 on Google Drive.

It is recommended to use the new .keras format for future projects.

This project was purely for practice to learn the basics of U-Net for image segmentation.