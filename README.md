# fMRI Basics

A growing collection of Jupyter notebooks for fMRI data analysis — aimed at students and collaborators getting started with neuroimaging in Python.

## Notebooks

| # | Notebook | What it covers |
|---|----------|----------------|
| 01 | `01_preprocessing_qc.ipynb` | Load a preprocessed NIfTI, print the header, extract Schaefer ROI timeseries, plot ROI×Time, ROI×ROI FC, and Time×Time correlation matrices; same inspection at the voxel level for one ROI |
| 02 | `02_atlas_surface_projection.ipynb` | Load the Schaefer atlas, project it onto the fsaverage surface, interactively highlight individual ROIs or whole networks |
| 03 | `03_nifti_surface_projection.ipynb` | Project any 3D NIfTI stat map onto the inflated brain surface |
| 04 | `04_glm_and_fir.ipynb` | GLM with canonical HRF (one beta per condition) and FIR (peri-event time course); single- and two-condition examples; runs on synthetic data — no files needed |

## Setup

```bash
pip install -r requirements.txt
jupyter lab
```

Or install dependencies individually:

```bash
pip install nilearn nibabel numpy scipy matplotlib ipywidgets tqdm
```

## Usage

Each notebook has a **Configuration** cell at the top — set your file paths there and run top-to-bottom.

Notebooks that require local data (01, 03) include clear `# <-- change this` markers.
Notebooks 02 and 04 need no local data (atlas downloaded automatically; 04 uses synthetic data).

## Requirements

- Python 3.9+
- See `requirements.txt`
