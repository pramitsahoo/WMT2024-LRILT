# WMT2024-LRILT
# WMT2024-LRILT

![Owner Avatar](https://github.com/pramitsahoo/WMT2024-LRILT)

## Overview

Welcome to the **WMT2024-LRILT** repository! This project contains the system developed by the NLIP Lab at IIT Hyderabad for the **WMT 2024 Shared Task** on **Low-Resource Indic Language Translation**. Our work focuses on advancing the translation of English ↔ Assamese, Khasi, Mizo, and Manipuri language pairs through fine-tuning pre-trained models.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Results](#results)
- [How to Use](#how-to-use)
- [Installation](#installation)
- [Usage](#usage)
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

## Results

Our system achieved the following results on the public test set:

| Language Pair   | BLEU Score | chrF2 Score |
|-----------------|------------|-------------|
| English → Assamese | 20.1      | 50.6        |
| English → Khasi    | 19.1      | 42.3        |
| English → Mizo     | 30.0      | 54.9        |
| English → Manipuri | 35.6      | 66.3        |

## How to Use

### Installation

To get started, clone this repository to your local machine:

```bash
git clone https://github.com/pramitsahoo/WMT2024-LRILT.git
cd WMT2024-LRILT
```

### Usage

To fine-tune the models on the provided datasets, follow these steps:

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the training script:
   ```bash
   python train.py --model <model_name> --data <dataset_path> --config <config_file>
   ```

3. Evaluate the model using the test set:
   ```bash
   python evaluate.py --model <model_name> --data <test_dataset_path>
   ```

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
