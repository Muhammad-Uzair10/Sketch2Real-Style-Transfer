
# Project Name: Sketch2Real: AI-Powered Artistic Style Transfer

## Description
This project implements an AI-powered artistic style transfer using TensorFlow and TensorFlow Hub, allowing users to transform content images with the artistic style of a sketch or other images. It leverages a pre-trained model for arbitrary image stylization and includes preprocessing and postprocessing steps to enhance the hand-drawn effect.

The project also features a Gradio interface for easy interaction, allowing users to upload content and style images and see the stylized output.

## Features
* **Style Transfer:** Applies the style of one image to the content of another.
* [cite_start]**Sketch Preprocessing:** Enhances hand-drawn features using edge detection (Canny) to prepare style images[cite: 8, 9, 10, 11, 15, 66, 67, 68, 69, 70, 71, 72, 73, 129, 130, 131, 132, 133].
* [cite_start]**Postprocessing:** Adds noise to the stylized output to simulate hand-drawn texture[cite: 30, 31, 32, 79, 80, 81, 141, 142, 143].
* [cite_start]**Gradio Interface:** Provides a user-friendly web interface for image upload and result display[cite: 35, 36, 37, 38, 39, 40, 41, 42, 101, 102, 103, 104, 105, 106, 107, 108, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179].
* [cite_start]**Style Mixing (Advanced Version):** Allows blending two different style images based on a user-defined percentage[cite: 148, 149, 160].

## Technologies Used
* Python
* [cite_start]TensorFlow [cite: 3]
* [cite_start]TensorFlow Hub [cite: 3]
* [cite_start]Gradio [cite: 3]
* [cite_start]OpenCV (`cv2`) [cite: 3]
* Numpy
* [cite_start]Matplotlib (for potential visualization, though not explicitly used in the Gradio interface part of the provided code) [cite: 3]

## Setup and Installation

To run this project locally or in a Colab environment, follow these steps:

### 1. Google Colab (Recommended for ease of use)

1.  Open the Colab notebook: `Style-Transfer.ipynb` (or the equivalent `.ipynb` file you uploaded).
2.  **Install Dependencies:** Run the first cell in the notebook to install the required libraries:
    ```bash
    !pip install tensorflow tensorflow-hub gradio opencv-python matplotlib
    ```
3.  **Upload Images:** You will need to upload your content and style images. The notebook includes a section for uploading files:
    ```python
    from google.colab import files
    uploaded = files.upload()
    ```
    Alternatively, you can place example images in your Google Drive and mount it to Colab.
4.  **Run all cells:** Execute all cells in the notebook sequentially.
5.  [cite_start]**Interact with Gradio:** Once the Gradio interface launches, a public URL will be provided (e.g., `https://xxxx.gradio.live`)[cite: 48, 111, 184]. Open this URL in your browser to interact with the style transfer application.

### 2. Local Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/YourRepositoryName.git](https://github.com/YourUsername/YourRepositoryName.git)
    cd YourRepositoryName
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: `venv\Scripts\activate`
    ```
3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    (You'll need to create a `requirements.txt` file manually if you plan to share this, see "Creating `requirements.txt`" below).
4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook Style-Transfer.ipynb
    ```
    Open the notebook in your browser and run the cells.

## Usage

1.  **Content Image:** Upload the image whose content you want to preserve (e.g., a photo).
2.  **Style Image(s):** Upload the image(s) whose artistic style you want to apply (e.g., a hand-drawn sketch, or two sketches for style mixing).
3.  **Style Mix Percentage (if applicable):** Adjust the slider to blend the styles from `Style Image 1` and `Style Image 2`.
4.  **View Result:** The stylized output will be displayed in the "Result" section.

## Model Used
[cite_start]The style transfer is powered by the "Arbitrary Image Stylization V1 256" model from TensorFlow Hub[cite: 22, 93, 147].

## Examples

* [cite_start]`photo.jpg` (Content Image) with `sketch_style.jpg` (Style Image)[cite: 40, 106].
* [cite_start]Content image: `/content/download (3) (1).jpeg`, Style Image 1: `/content/photo.jpg`, Style Image 2: `/content/download (1).jpeg`, Style Mix Percentage: 50[cite: 174].
* *(Add more examples if you have them, with descriptions and perhaps screenshots)*

## Troubleshooting (Optional Section)
* **Gradio Public URL Not Appearing:** Ensure you are running the notebook in an active Colab session. [cite_start]Gradio requires `share=True` to generate a public URL in Colab, which is automatically set in the provided code[cite: 47, 109, 184].
* [cite_start]**"No interface is running right now"**: This message appears if the Gradio `launch()` function hasn't been executed or has been stopped[cite: 51, 114]. Rerun the Gradio cell.

## License
[Choose your license, e.g., MIT License]

## Acknowledgements
* TensorFlow Hub for providing the pre-trained style transfer model.
* Gradio for simplifying the creation of web interfaces for machine learning models.