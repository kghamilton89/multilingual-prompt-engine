# Multilingual Prompt Engine 🤗

> Please note that this project has been permanenetly moved to the [DIBT repo](https://github.com/huggingface/data-is-better-together) and is no longer maintained at this location.

## Scope

Multilingual Prompt Engine (MPE) is a community-driven continuation of the [Multilingual Prompt Evaluation Project](https://github.com/huggingface/data-is-better-together/blob/main/community-efforts/prompt_translation/README.md) (MPEP) initiative of the [Data is Better Together](https://huggingface.co/DIBT) (DIBT) project.

The primary goal of MPE is to use [completed MPEP datasets](https://huggingface.co/datasets?search=MPEP) to prompt [top-performing multilingual LLMs](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard), for the community to evaluate.

Thus, new language-specific performance metrics may be created and assessed so non-English speaking communities can access the best performing LLMs for their language, and indeed, assess the performance of their own fine-tuned and fully trained LLMs against larger foundation models.

## Usage

MPE is a Jupyter Notebook which may be run by anyone with a valid [Hugging Face token](https://huggingface.co/settings/tokens).

This documentation presumes that the user is conceptually familiar with the creation and configuration of a [Conda](https://conda.io/projects/conda/en/latest/index.html) environment.

To build the requisite Conda environment:

```bash
# navigate to the MPE directory

$ cd ./multilingual-prompt-engine

# build the conda environment from environment.yml

$ conda env create -f environment.yml

# activate the conda environment

$ conda activate hf
```

To configure the list of models used and number of prompts sent by MPE:

```python
# locate the num_prompts variable to configure the number of prompts to process for each language

num_prompts = 500

# locate the models variable and configure the target models as desired according to the syntax shown

models = [
    "google/gemma-2-27b-it",
    "meta-llama/Meta-Llama-3-70B-Instruct",
    "Qwen/Qwen2-72B-Instruct",
    "mistralai/Mixtral-8x22B-Instruct-v0.1",
]
```

To review the output generated by each of the respective models:

1. Navigate to `./responses/{language}.md` where {language} is the English-language name of the language whose output you wish to review.
2. Responses are sorted according to model, and then each prompt/response pair.
3. Work with these documents as you wish to create your own multilingual benchmarks and metrics!
