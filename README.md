# Algorithm Comparison on Simulated Mental Health and Remote Work Data

This repository contains the implementation and analysis of various causal discovery algorithms (PC, FCI, and GES) applied to simulated data examining the relationship between remote work and mental health outcomes.

## Project Structure

The project consists of three main Jupyter notebooks:

1. `data_simulation_and_eda.ipynb`: Contains the data simulation logic and exploratory data analysis
2. `algorithm_test.ipynb`: Implements and tests PC, FCI, and GES algorithms on the simulated data
3. `model_evaluation.ipynb`: Evaluates the performance of all algorithms using various metrics

## Dependencies

### Required Packages

The following packages are required to run the analysis:

```bash
pip install causal-learn  # Must be installed first
pip install --upgrade matplotlib
```

### Python Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import io
from causallearn.search.ConstraintBased.PC import pc
from causallearn.search.ScoreBased.GES import ges
import matplotlib.image as mpimg
import networkx as nx
from causallearn.search.ConstraintBased.FCI import fci
from causallearn.utils.GraphUtils import GraphUtils
from causallearn.search.FCMBased.ANM.ANM import ANM
from sklearn.linear_model import LinearRegression
from causallearn.utils.TXT2GeneralGraph import txt2generalgraph
from causallearn.graph.ArrowConfusion import ArrowConfusion
from causallearn.graph.AdjacencyConfusion import AdjacencyConfusion
from causallearn.graph.SHD import SHD
```

## Setup Instructions

1. Clone this repository:
```bash
git clone https://github.com/VivianZhao12/CAPSTONE-Causal-Inference-between-Remote-Work-and-Mental-Health
cd CAPSTONE-Causal-Inference-between-Remote-Work-and-Mental-Health
```

2. Create and activate a new Python environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

3. Install the required packages:
```bash
pip install -r requirements.txt
```

## Running the Analysis

Execute the notebooks in the following order:

1. First, run the data simulation and EDA:
```bash
jupyter notebook data_simulation_and_eda.ipynb
```

2. Then run the algorithm tests:
```bash
jupyter notebook algorithm_test.ipynb
```

3. Finally, run the model evaluation:
```bash
jupyter notebook model_evaluation.ipynb
```

## Attribution
The FASTKCI.py implementation used in this project is from:
- Original repository: [causal-learn](https://github.com/py-why/causal-learn/tree/main)
- Specific file: [FASTKCI.py](https://github.com/py-why/causal-learn/blob/main/causallearn/utils/FastKCI/FastKCI.py)
- Original authors: Mingming Gong, Erdun Gao, Aoqi Zuo (KCI implementation team)

This implementation is part of the larger causal-learn project developed by:
- Team Leaders: Kun Zhang, Joseph Ramsey, Mingming Gong, Ruichu Cai, Shohei Shimizu, Peter Spirtes, Clark Glymour
- Coordinators: Yujia Zheng, Biwei Huang, Wei Chen
