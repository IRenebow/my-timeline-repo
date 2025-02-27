# Compensation Timeline Notebook

This repository provides a Jupyter Notebook (`timeline.ipynb`) for visualizing compensation timelines (absolute and relative performance periods) based on CSV data. It uses:

- **pandas** for data loading and filtering  
- **matplotlib** and **seaborn** for plotting  
- **ipywidgets** for an interactive UI (entering CIK and participant IDs)  
- **Voila** to serve the notebook as a simple web app

## Repository Structure
my-timeline-repo/
├─ data/
│    ├─ GpbaAbs_vest.csv
│    └─ GpbaRel_vest.csv
├─ timeline.ipynb
├─ requirements.txt
└─ README.md

## Usage

1. **Launch as a Web App** (Binder + Voila):
   - Click the Binder badge below to launch the notebook in a cloud environment, served by Voila. No local installation needed!
   
   [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/IRenebow/my-timeline-repo/HEAD?urlpath=%2Fdoc%2Ftree%2Fvoila%2Frender%2Ftimeline.ipynb)

2. **Local Use** (Jupyter Lab/Notebook):
   1. Clone this repository:  
      ```bash
      git clone https://github.com/IRenebow/my-timeline-repo.git
      cd my-timeline-repo
      ```
   2. Install the dependencies (via pip):  
      ```bash
      pip install -r requirements.txt
      ```
      or, if you use conda:  
      ```bash
      conda create -n timeline-env python=3.9
      conda activate timeline-env
      pip install -r requirements.txt
      ```
   3. Launch Jupyter:
      ```bash
      jupyter lab
      ```
   4. Open `timeline.ipynb`. Run all cells to explore or generate plots.

3. **Notebook Description**:
   - **`timeline.ipynb`** has an interactive UI (two integer fields and a button).  
   - You can enter a **CIK** and **Participant ID**.  
   - It filters data from `GpbaAbs_vest.csv` and `GpbaRel_vest.csv`, then plots a timeline of grants.  
   - The plot is color-coded for absolute vs. relative performance periods, with a marker for grant dates.

## Data Details

- **GpbaAbs_vest.csv**: Holds absolute performance data, including columns for `CIK`, `participantid`, `grantDate`, `vestLow`, `vestHigh`, etc.
- **GpbaRel_vest.csv**: Holds relative performance data with similar columns.