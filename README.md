# Handwritten digit workshop

**The problem**: Someone has to read handwritten digits on scanned forms and type them into a system. Handwriting varies, so writing a rule for every way people draw a digit would be difficult. Could we teach a model to recognize digits from examples instead?

In this workshop we use MNIST, a collection of small digit images with known answers, to try that approach. We inspect the images, prepare their pixel values, train a small neural network, and check which digits it gets wrong. An optional section compares it with a convolutional neural network (CNN). MNIST is practice data: real forms may look different, so a good score here would not be enough to use the model on actual forms.

## What's in this repository

- [mnist_workshop.ipynb](mnist_workshop.ipynb) contains the code, exercises, checks, and discussion stops. Work through its chapters in order.



## What you'll learn

- What the ML development cycle looks like.
- What a model's inputs, weights, outputs, and labels represent.
- Why training, validation, and test images have different jobs.
- How preprocessing and model architecture affect predictions.
- Why a single accuracy score misses useful information about errors.

## Run the notebook

No prior machine learning experience is needed; basic Python helps, and each exercise has a hint. Choose one setup option below. Run cells from top to bottom, chapter by chapter, and pause at each "Stop and discuss" prompt. For each `TODO`, replace only the `raise NotImplementedError(...)` line. Try your own approach first; each exercise has a collapsed hint and one solution if you get stuck. The checks in the cell give immediate feedback. Copilot may fill in the code for you, but it is more fun to try it yourself :).

### Local in VS Code

1. Clone this repository and open the folder in VS Code. Install the Python and Jupyter extensions if VS Code prompts you.
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/) if needed. Use it to install Python 3.11, then create a project environment and install the notebook packages from the repository root. `uv` manages this Python installation, so you do not need to install Python system-wide:

   ```powershell
   uv python install 3.11
   uv venv --python 3.11 .venv
   uv pip install --python .venv\Scripts\python.exe tensorflow-cpu matplotlib ipykernel
   ```

   On macOS or Linux, use `.venv/bin/python` in the `uv pip install` command instead.
3. Open [mnist_workshop.ipynb](mnist_workshop.ipynb) and select the `.venv` Python kernel in the top right.

### Google Colab

Open [Google Colab](https://colab.research.google.com/), choose **File > Upload notebook**, and upload [mnist_workshop.ipynb](mnist_workshop.ipynb). Use a CPU runtime. Colab provides Python, TensorFlow, NumPy, and Matplotlib; you do not need to install Python locally or use Colab Pro or Google Drive. The first run downloads MNIST, so internet access is required.
