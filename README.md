### WGAN Project for Whole Slide Image Generation in Digital Pathology

I aimed to train a DCGAN using the Wasserstein loss function with a gradient penalty to generate WSIs of different glomerular structures. 

Please note that my GAN generated some clear images, but it did not successfully fit the complex distribution of the training dataset. So please feel free to share any improvements you make to this code :)

#### Getting Started

##### Prerequisites

Ensure you have the following installed:

- Python 3.7+
- PyTorch
- torchvision
- matplotlib
- PIL (Pillow)

##### Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/Annette29/whole_slide_image_generation_DCGAN-with-WL.git
   cd WGAN_Project
   ```

2. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

##### Usage

1. **Prepare the dataset:**

   Please find and download the kidney images dataset used from here: https://data.mendeley.com/datasets/k7nvtgn2x6/3

   Organize your training images in a directory, for example, `data/train`.

3. **Train the model:**

   Run the `main.py` script to start training the WGAN model:

   ```bash
   python main.py
   ```

4. **Generate images:**

   Use the `generate_images.py` script to generate new images using the trained model:

   ```bash
   python generate_images.py --model_path path/to/checkpoint.pth.tar --num_images 10 --output_dir generated_images
   ```

## Citation

If you use this code or find our work helpful, please consider citing this paper:

```bibtex
@inproceedings{sice23,
  author = {{Annette Waithira Irungu} and {Kotaro Sonoda} and {Kris Lami} and {Junya Fukuoka} and {Senya Kiyasu}},
  title = {Leveraging GANs for Whole Slide Image Generation in Digital Pathology},
  booktitle = {the 42nd Society of Instrument and Control Engineers (SICE) Kyushu Branch Conference},
  year = {2023},
  month = {dec},
  pages = {78–81}
}
```
