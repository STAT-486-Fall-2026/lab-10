# Lab 10: CNN Classification and Learned Representations

<!-- STAT 486 · Fall 2026 -->

## Objective

Implement and train a convolutional neural network in PyTorch on Fashion-MNIST, compare it with a random forest baseline, and investigate what the CNN gets right and wrong. Use softmax confidence to inspect individual predictions, then use PCA and t-SNE to visualize the CNN's learned representations.

## Before you begin

You need Git, a GitHub account, and [uv](https://docs.astral.sh/uv/getting-started/installation/) installed on your computer.

Plan for **3–4 hours** of coding and interpretation. The required work supports a local CPU; a GPU is not required. Allow extra time for the first environment installation and dataset download. The supplied setup downloads approximately 31 MB of compressed Fashion-MNIST data from a pinned revision of the official dataset repository and caches it locally. Both projection plots use all 10,000 validation examples, so allow the t-SNE fit to finish before running it again.

In a CPU reference check, the eight CNN training epochs took about four minutes and full-validation t-SNE took about one minute. These are execution times; the lab estimate includes implementation and interpretation. Runtime will vary with hardware and background activity.

## Set up your submission repository

### 1. Create your private submission repository

On [`STAT-486-Fall-2026/lab-10`](https://github.com/STAT-486-Fall-2026/lab-10), select **Use this template** and then **Create a new repository**. Set the owner to the `STAT-486-Fall-2026-Labs` organization, name the repository exactly:

```text
lab-10-<netid>
```

For example, a student whose NetID is `jdoe42` must create `lab-10-jdoe42`. Use your institutional NetID even if it differs from your GitHub username. Make the repository **private**, then create it. Do not fork the starter repository.

### 2. Clone your repository

Copy the HTTPS URL for **your repository**, then run the following commands. Replace the NetID placeholder.

```bash
git clone https://github.com/STAT-486-Fall-2026-Labs/lab-10-<netid>.git
cd lab-10-<netid>
```

### 3. Create and lock your environment

The starter repository includes a lab-specific `pyproject.toml` and `.python-version`. From the repository directory, run:

```bash
uv sync
```

This creates your local `.venv` with Python 3.11.5 and generates `uv.lock`. Keep the supplied `pyproject.toml` unchanged unless the lab directions explicitly say otherwise. Commit the generated `uv.lock` with your work, but never commit `.venv`.

### 4. Complete the lab

Open `lab-10.ipynb` in your preferred editor and configure it to use the Python interpreter or notebook kernel in this repository's `.venv`.

Complete the code tasks and written responses in the notebook. Use the supplied training/validation split for both models and select the CNN checkpoint using validation loss. Evaluate the fixed models on the test set in Section 4, then complete the confidence analysis and embedding plots in Sections 5 and 6 using the full validation set. Keep both models unchanged after test evaluation.

Before submitting, restart the kernel and run your completed notebook from beginning to end. Save the notebook with its tables, loss curves, image panels, and scatterplots visible. Your written interpretations belong in the provided Markdown cells. Do not commit downloaded data, model checkpoints, or environment directories; these are reproducible from the notebook and ignored by the starter.

### 5. Commit and push your work

```bash
git add lab-10.ipynb pyproject.toml .python-version uv.lock
git commit -m "Complete Lab 10"
git push
```

## Submission

Paste the root URL of your repository into the Canvas Lab 10 submission textbox:

```text
https://github.com/STAT-486-Fall-2026-Labs/lab-10-<netid>
```

Do not open a pull request and do not upload the notebook file to Canvas.
