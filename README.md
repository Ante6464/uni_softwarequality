# Comparison of Large Language Model Prompting Techniques
Project by Justin Reichert and Fynn Aldenkirchs

## Project Overview

This project, conducted as part of the Software Quality course, aims to investigate and compare various prompting techniques for Large Language Models (LLMs). 
By systematically evaluating different prompting strategies, we seek to understand how subtle variations in prompt design 
can significantly impact the quality and relevance of generated text.

Note that this project uses code from the [MetricX Github repository](https://github.com/google-research/metricx), which is 
distributed under the Apache License 2.0. For more information,
see the LICENSE file in this repository. 
The code from MetricX included in this project can be found in the `metricx24` folder, and consists of the following files: `__init__.py`, `evaluate.py`, `evaluate_wmt24.py`, `models.py`, and `predict.py`.

## Project Structure
* `metricx24`: Code from the [MetricX repository](https://github.com/google-research/metricx) used for evaluation.
* `few_shot_prompts.ipynb`:  Prompt templates we created and ran through the pipeline.
* `zero_shot_prompts.ipynb`:  Prompt templates we created and ran through the pipeline.
* `ProjectNotebook.ipynb`:  The pipeline we developed for this project.
* `mlruns`: MLflow experiments and runs we logged through the pipeline.
* `mlartifacts`: MLflow artifacts and outputs that were produced by the pipeline.
* `machine_translation.csv/pkl`: Datasets used.


## Setup

1.  **Environment Creation:** In the root directory of the project, you'll find an environment.yml file. You can use this file to create a conda environment named `softwarequality` with the following command:

    ```bash
    conda env create --file environment.yml
    ```

2.  **Environment Activation:** Activate the newly created environment with:

    ```bash
    conda activate softwarequality
    ```
    
3.  **IDE Integration (Optional):** Set the `softwarequality` environment as the project's interpreter in your preferred IDE (e.g., PyCharm) to run the Jupyter Notebook.

4.  **macOS Specific Modification:** On macOS, due to differences in PyTorch's device handling, line 142 of `metricx24/predict.py` may need to be adjusted. Specifically, change the line 137 depending on your system, as determined in the preceding lines (137-141). This ensures proper device allocation for the MetricX evaluation.


