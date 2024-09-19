# HPS Jupyter Book

[![Deploy](https://github.com/SeisSCOPED/HPS-book/actions/workflows/deploy.yaml/badge.svg)](https://github.com/SeisSCOPED/HPS-book/actions/workflows/deploy.yaml)
[![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](https://SeisSCOPED/HPS-book)
<!-- [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/geo-smart/simple-template/HEAD?labpath=book%2Fchapters) -->
<!-- [![GeoSMART Use Case](./book/img/use_case_badge.svg)](https://geo-smart.github.io/usecases) -->


## Citation

If you use this book, please cite it as follows:

```{bibliography}
```

## HPS Book contributors.

We welcome contribution to this book. Because this is the draft of a textbook, we are still exploring ways to homogeneize the format of the books. We accept the following main threads of research:
1. **CyberInfrastructure** content (e.g., how to use HPC, how to use the Cloud, open science) that does not replicate content from other sources and that is relevant to seismological research.
2. **Core Software** content: how to use a core package such as SPECFEM, noisepy, seisbench etc. The tutorials should be described as simple, boiler-plate example on how to use these packages that are the core of a research workflow.
3. **Research Workflow**: these are fullstack notebooks that leverage CI and core software for specific research question. We will welcome a few to exemplify current research practices.

## How to contribute.
We welcome contributions to this book! Follow the steps below to set up your environment, add your content, and ensure it appears correctly in the book.

### Step 1: Set Up Your Environment
1. **Clone the repository**
```
git clone https://github.com/SeisSCOPED/HPS-book.git
cd HPS-book
```
2. **Create and Activate a Conda Environment**: Ensure you have Conda installed. We recommend miniconda or mamba.
```
conda env create -f environment.yml
conda activate hps-book
```
### Step 2: Add Your Content
1. **Add Rendered Notebooks**: Place your rendered Jupyter notebooks (``.ipynb`` files) or markdown files (``.md`` files) in the appropriate directory within the ``book`` directory. For example, if you are adding a new tutorial, you might place it in ``book/tutorials``.

2. **Modify the Table of Contents (TOC)**: Update the ``_toc.yml`` file to include your new content. This file controls the structure of the book and how the chapters appear in the sidebar.

Open ``_toc.yml`` and add an entry for your new content. For example:
```
- file: intro
- part: Tutorials
  chapters:
    - file: tutorials/your_new_tutorial
```
Ensure the path to your file is correct and relative to the ``book`` directory.


### Step 3: Format Your Notebooks or Markdown Files
1. **Notebook Formatting:**
    * Ensure your notebooks are clean and free of unnecessary output. You can clear the output by going to ``Kernel -> Restart & Clear Output`` in Jupyter Notebook.
    * Use headings (``#``,``##``, ``###``, etc.) to structure your content.
    * Add markdown cells to explain your code and results.
2. **Markdown File Formatting:**
    * Use proper markdown syntax for headings, lists, links, images, etc.
    * Ensure your markdown files have a title at the top using a level 1 heading (``#``).

### Step 4: Build the Jupyter Book Locally
1. **Build the book**
In the repository main directory, type 
```
jb build book/
```
2. **Preview the book**
You can preview the book by opening the ``_build/html/index.html`` file in your web browser.


### Step 5: Submit Your Contribution
1. **Commit Your Changes:**
```
git add .
git commit -m "Add new tutorial on [topic]"
```
2. **Push Your Changes:**
```
git push origin your-branch-name
```
3. **Create a Pull Request:** Go to the repository on GitHub and create a pull request. Provide a clear description of your changes and the content you have added.

### Example of a Well-Formatted Notebook
Here’s an example of how to format a Jupyter notebook to ensure it appears nicely in the book:
```
# Title of Your Tutorial

## Introduction

Provide an introduction to your tutorial. Explain what the reader will learn and any prerequisites.

## Step 1: Setup

Explain the setup process. Include any necessary code.

```python
# Example setup code
import numpy as np
import matplotlib.pyplot as plt
```

::notes::
To improve pedagogy, we recommend that notebooks are designed to include student-led activities with empty cells, and provide avenues to change parameters in the workflows.

### Step 2: Main Content
Provide the main content of your tutorial. Use markdown cells to explain each step.
```
# Example code
x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.title("Sine Wave")
plt.show()
```
### Conclusion
Summarize what the reader has learned and provide any additional resources or next steps.
```

### Example of a Well-Formatted Markdown File

Here’s an example of how to format a markdown file to ensure it appears nicely in the book:

```markdown
# Title of Your Tutorial

## Introduction

Provide an introduction to your tutorial. Explain what the reader will learn and any prerequisites.

## Step 1: Setup

Explain the setup process. Include any necessary code.

```python
# Example setup code
import numpy as np
import matplotlib.pyplot as plt
```



## Original Template
This repository was made by a GEOSMART template and has the skeleton of a GeoSMART use case book in chapter ML in Seismology. The original authors were Scott Henderson (UW) and other friends at the eScience Institute. Below is how to reuse the template<br>

1. Click "Use This Template" and name your repository

2. In your repository edit book/_config.yml

3. Under your repository Settings --> Pages --> Source = GitHub Actions

3. Edit environment.yml, modify notebooks, and your JupyterBook will be published for you! 
