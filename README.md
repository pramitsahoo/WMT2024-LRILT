# WMT2024-LRILT

![Owner Avatar](https://github.com/pramitsahoo/WMT2024-LRILT)

## Overview

Welcome to the **WMT2024-LRILT** repository! This project contains the system developed by the NLIP Lab at IIT Hyderabad for the **WMT 2024 Shared Task** on **Low-Resource Indic Language Translation**. Our work focuses on advancing the translation of English ↔ Assamese, Khasi, Mizo, and Manipuri language pairs through fine-tuning pre-trained models.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Models](#models)
- [Results](#results)
- [Datasets](#datasets)
- [Contributors](#contributors)
- [License](#license)

## Features

- **Language-Specific Fine-Tuning**: Fine-tuning on pre-trained models like IndicRASP and IndicRASP Seed for low-resource languages.
- **Multilingual Support**: Cross-lingual transfer learning using multilingual models with script-based language grouping.
- **Layer-Freezing Techniques**: Leveraging frozen layers to enhance the efficiency of transfer learning.
- **Alignment Augmentation**: Improving translation quality using alignment-based pre-training objectives.

## System Architecture

Our approach leverages the following models:

- **IndicRASP**: Pre-trained on 22 scheduled Indic languages, focused on alignment augmentation.
- **IndicRASP Seed**: A fine-tuned version of IndicRASP on high-quality, small-scale data, demonstrating improved translation results.

We experimented with **bilingual** and **multilingual** setups, using language grouping based on script similarity, and explored layer-freezing techniques to optimize performance.

## Models
This repository contains checkpoints for translation models trained on low-resource Indic languages as part of the WMT24 Shared Task. Below are the links to the available models for **En → Indic** and **Indic → En** directions.

## En → Indic

| **Language**   | **Script** | **Checkpoint Name**    | **Download Link**      |
|-----------------|------------|------------------------|-------------------------|
| Assamese        | Bengali    | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/EUcFO1SHmDRCicxB_9Ld2ncBTgRHFZHIyv23um5C2c6vtg?e=XVe6yl)          |
| Khasi           | Latin      | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/ETB5zM6ptDhGsc5IrpFM4w0BpjBJEJCB2PwbJOZsWLT4Kw?e=WbGB5n)          |
| Mizo            | Latin      | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/EVfa_BvcWmVDjOPiNTsBZegBc6iTYW0l9mknUHPxVhzGGg?e=gn3Sjg)          |
| Manipuri        | Bengali    | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/EQzhRVE7VZxCnzTeORKiNjsBUxUCfQ5rx8P5tJkZlTdy1A?e=1uqGK0)          |

## Indic → En

| **Language**   | **Script** | **Checkpoint Name**    | **Download Link**      |
|-----------------|------------|------------------------|-------------------------|
| Assamese        | Bengali    | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/ES2TnnjmxSZBvnmSExzLXMcBy31OE5S87jygg2K52c3tow?e=CEJKPn)          |
| Khasi           | Latin      | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/EZhoUBHM3aZIiAY4HDqJxIsBYbJURpprRRYqDnxn6ch6Kg?e=3jFzp8)          |
| Mizo            | Latin      | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/ERioM87UCkZKig0xecFgc78BtorlVaji3hiRIRzj0R0egQ?e=7iPEl6)          |
| Manipuri        | Bengali    | `checkpoint_best.pt`   | [Download](https://iith-my.sharepoint.com/:u:/g/personal/ai23mtech14004_iith_ac_in/Eb_TtoCElpBHguybk-wZCRsBoJ6QZJWIu0e-nrJ1c-Mbpg?e=dhzW0W)          |



## Results

Our system achieved the following results on the public test set:

| Language Pair   | BLEU Score | chrF2 Score |
|-----------------|------------|-------------|
| English → Assamese | 20.1      | 50.6        |
| English → Khasi    | 19.1      | 42.3        |
| English → Mizo     | 30.0      | 54.9        |
| English → Manipuri | 35.6      | 66.3        |


### Datasets

We used the **IndicNECorp1.0** dataset provided by the IndicMT shared task organizers. It includes parallel and monolingual data for Assamese, Khasi, Mizo, and Manipuri languages. For more details, refer to the [official WMT24 shared task page](https://www2.statmt.org/wmt24/indic-mt-task.html).

## Contributors

- **Pramit Sahoo** ([@pramitsahoo](https://github.com/pramitsahoo))
- **Maharaj Brahma**
- **Maunendra Sankar Desarkar**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

For more details on the system and our experiments, please refer to our [paper](https://arxiv.org/abs/2410.03215v1).

Happy translating! 🌐✨
