# PeerEval: Estimating Informativeness in Peer Review through Paper-Review Interaction

## Overview

This repository contains the dataset, code, and supplementary materials for the paper "PeerEval: Estimating Informativeness in Peer Review through Paper-Review Interaction." This research introduces a novel metric to evaluate the informativeness of peer reviews.

## Repository Contents

- `dataset/`: Contains the dataset used and the informativeness score generation files used in the study.
- `model/`: Contains the scripts and models used for data processing, model training, and evaluation.

## Installation

To run the code, you need to set up the environment with the required dependencies. Use the following commands to set up the environment:

```bash
# Clone the repository
git clone https://github.com/your-repo/PeerEval.git
cd PeerEval

# Create a virtual environment
python3 -m venv env
source env/bin/activate

# Install the required packages
pip install -r requirements.txt

# Download the data from the following link. Use Webscraping.py and pdf.py to create the test set

# Run the dataset and informativeness score formation files from the dataset folder
cd datasets

# Run the files in the model folder on the dataset created to obtain the results
cd ..
cd model
```

### Informativeness Score Calculation

The informativeness score is computed using the following formula:

$$
R_{info} = \frac{e_{asp} + R_{sec} + 2 \times |R_{rec} - 0.5| + e_{Rstr}}{2 \times (e + 1) \times R_{hsc}}
$$

Where:

- R<sub>info</sub>: Informativeness score
- R<sub>sec</sub>: Section score
- e<sub>asp</sub>: Aspect score
- R<sub>rec</sub>: Recommendation score
- e<sub>str</sub>: Strength score
- R<sub>hsc</sub>: Hedge score
