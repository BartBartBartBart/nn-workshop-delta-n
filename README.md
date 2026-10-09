# Handwritten digit workshop

Imagine a service that receives scans of handwritten digits from paper forms. Someone currently reads each digit and enters it by hand. Can a model predict the digit from its pixels, and how would we tell when its guesses are unreliable? We use MNIST's small grayscale images as a stand-in for this problem. Real forms may look different, so a good MNIST score alone would not justify deploying the model.

In [mnist_workshop.ipynb](mnist_workshop.ipynb), you will inspect examples, prepare pixels, train a small neural network, and examine its mistakes. An optional section compares it with a convolutional neural network (CNN). No GPU is required.

For the instructor, [handwritten_digit_workshop.pptx](handwritten_digit_workshop.pptx) is an editable eleven-slide presentation using the Delta-N template. The PowerPoint speaker notes and [WORKSHOP_SLIDES.md](WORKSHOP_SLIDES.md) provide talking points. Start with the handwritten-form problem, then show the development loop before the model theory and the chapter slides. Keep each notebook chapter to 10-15 minutes including its discussion stop; the optional CNN chapter takes another 10-15 minutes.

## What you'll learn

- What a model's inputs, weights, outputs, and labels represent.
- Why training, validation, and test images have different jobs.
- How preprocessing and model architecture affect predictions.
- Why a single accuracy score misses useful information about errors.

## Before the hands-on session

The slides introduce the model, training, and the three data sets. The notebook keeps the instructions short so participants can spend more time running cells and discussing results. No prior machine learning experience is assumed; basic Python helps, and each exercise has a hint.

## Run the notebook

Choose one option. Run cells from top to bottom, chapter by chapter. Pause at each "Stop and discuss" prompt before moving on. For each `TODO`, replace only the `raise NotImplementedError(...)` line. Try your own approach first; each exercise has a collapsed hint and one solution if you get stuck. The checks in the cell give immediate feedback. Copilot may suggest code, but an accepted suggestion is not an explanation: predict what the cell should do and check the output yourself.

### Local in VS Code

1. Clone this repository and open the folder in VS Code. Install the Python and Jupyter extensions if VS Code prompts you.
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/) if needed. From the repository root, create an environment and install the notebook packages:

   ```powershell
   uv venv --python 3.11 .venv
   uv pip install --python .venv\Scripts\python.exe tensorflow-cpu matplotlib ipykernel
   ```

   On macOS or Linux, use `.venv/bin/python` in the second command instead.
3. Open [mnist_workshop.ipynb](mnist_workshop.ipynb) and select the `.venv` Python kernel in the top right.

### Google Colab

Open [Google Colab](https://colab.research.google.com/), choose **File > Upload notebook**, and upload [mnist_workshop.ipynb](mnist_workshop.ipynb). Use a CPU runtime. Colab includes TensorFlow, NumPy, and Matplotlib; no Colab Pro or Google Drive is needed. The first run downloads MNIST, so internet access is required.
