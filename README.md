# LLM Course

Lecture slides and computer assignments from the Spring 2026 Large Language Models course.

## Repository layout

```text
.
├── assignments/
│   ├── ca1/
│   │   ├── starter/
│   │   └── submission/
│   ├── ca2/
│   │   ├── starter/
│   │   └── submission/
│   ├── ca3/
│   │   ├── starter/
│   │   └── submission/
│   ├── ca4/
│   │   ├── starter/
│   │   └── submission/
│   └── ca5/
│       ├── starter/
│       └── submission/
├── archives/
│   ├── ca1/
│   ├── ca2/
│   ├── ca4/
│   └── ca5/
└── lectures/
```

- [`assignments/`](assignments/) groups the materials by assignment. Each `starter/` contains the supplied assignment brief, notebooks, and supporting files available in the original repository. Each `submission/` contains the completed work and its accompanying files.
- [`archives/`](archives/) contains ZIP and RAR submission packages, grouped by assignment. The CA5 ZIP is stored in two numbered parts. Their extracted files are under `assignments/`.
- [`lectures/`](lectures/) contains all 17 slide decks in their original numbered order.

## Assignment index

| Assignment | Topics | Starter materials | Completed work |
| --- | --- | --- | --- |
| CA1 | Transformer implementation, training, and name generation | [Starter](assignments/ca1/starter/) | [Notebook](assignments/ca1/submission/ca1.ipynb), [report](assignments/ca1/submission/ca1_report.pdf) |
| CA2 | Prompt engineering, in-context learning, and PEFT/LoRA | [Starter](assignments/ca2/starter/) | [Notebook](assignments/ca2/submission/ca2.ipynb) |
| CA3 | Tokenization, preference alignment, and LLM judging | [Starter](assignments/ca3/starter/) | [Notebook](assignments/ca3/submission/ca3.ipynb) |
| CA4 | Research agents and retrieval-augmented question answering | [Starter](assignments/ca4/starter/) | [Q1](assignments/ca4/submission/ca4_q1.ipynb), [Q2](assignments/ca4/submission/ca4_q2.ipynb) |
| CA5 | Multilingual trustworthiness evaluation and vision-language models | [Starter (Rev1)](assignments/ca5/starter/) | [Q1](assignments/ca5/submission/ca5_q1.ipynb), [Q2](assignments/ca5/submission/ca5_q2.ipynb) |

## Lecture index

| Lecture | Slides |
| --- | --- |
| 01 | [Introduction](lectures/01_introduction.pdf) |
| 02 | [Basics](lectures/02_basics.pdf) |
| 03 | [Fine-tuning and in-context learning](lectures/03_fine_tuning_and_in_context_learning.pdf) |
| 04 | [Prompt engineering](lectures/04_prompt_engineering.pdf) |
| 05 | [Instruction tuning](lectures/05_instruction_tuning.pdf) |
| 06 | [Parameter-efficient fine-tuning](lectures/06_peft.pdf) |
| 07 | [Data and tokenization](lectures/07_data_and_tokenization.pdf) |
| 08 | [Alignment](lectures/08_alignment.pdf) |
| 09 | [Reasoning](lectures/09_reasoning.pdf) |
| 10 | [Scaling laws](lectures/10_scaling_laws.pdf) |
| 11 | [Estimating LLM resource requirements](lectures/11_estimating_llm_resource_requirements.pdf) |
| 12 | [Retrieval-augmented generation](lectures/12_retrieval_augmented_generation.pdf) |
| 13 | [Chatbots and AI agents](lectures/13_chatbots_and_ai_agents.pdf) |
| 14 | [Evaluation](lectures/14_evaluation.pdf) |
| 15 | [LLM security risks and detection](lectures/15_llm_security_risks_and_detection.pdf) |
| 16 | [Quantization](lectures/16_quantization.pdf) |
| 17 | [Understanding LLMs](lectures/17_understanding_llms.pdf) |
## Extracting packaged files

The IMDb review dataset is compressed to keep the GitHub upload small. From the repository root, restore the filename expected by the CA2 notebook with:

```sh
unzip assignments/ca2/submission/IMDb-Review-Analysis-master/IMDb_Reviews.csv.zip -d assignments/ca2/submission/IMDb-Review-Analysis-master/
```

The CA5 submission archive is split into two parts. Reassemble and extract it with:

```sh
cat archives/ca5/ca5_submission.zip.part01 archives/ca5/ca5_submission.zip.part02 > archives/ca5/ca5_submission.zip
unzip archives/ca5/ca5_submission.zip -d archives/ca5/ca5_submission/
```

The restored IMDb CSV and CA5 archive copies are ignored by Git. The CA3 notebook uses `huggingface_hub.login()` to request your own Hugging Face credentials when needed.
