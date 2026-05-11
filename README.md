# ContourDepth

A depth estimation model based on scene-structure constraints.

## Setup

```bash
conda env create -f environment.yml
conda activate contourdepth
```

## Dataset Format

The dataset structure is as follows (depth stored in `.npy` format):

```
dataset/
  image/
    0001.jpg
    0002.jpg
  depth/
    0001.npy
    0002.npy
  train.txt
  val.txt
  test.txt
  demo.txt
```

Each line in the text files is a **file name (without extension)**.

## Training

Training entry: `train.py`. Modify the corresponding training parameters in `config.yaml`.

## Loss Functions Based on Scene-Structure Constraints

Composed of three parts: structural consistency, variance constraint, and ordering constraint. 

**(a) Struct Loss: Structural Consistency**

**(b) Var Loss: Intra-Contour Variance Suppression**

**(c) Order Loss: Inter-Contour Ordering/Spacing Constraint**

## Acknowledgements & Citation

Parts of this project are derived from DPT:

```
@article{Ranftl2020,
	author    = {Ren\'{e} Ranftl and Katrin Lasinger and David Hafner and Konrad Schindler and Vladlen Koltun},
	title     = {Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-shot Cross-dataset Transfer},
	journal   = {IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI)},
	year      = {2020},
}
@article{Ranftl2021,
	author    = {Ren\'{e} Ranftl and Alexey Bochkovskiy and Vladlen Koltun},
	title     = {Vision Transformers for Dense Prediction},
	journal   = {ArXiv preprint},
	year      = {2021},
}

```
