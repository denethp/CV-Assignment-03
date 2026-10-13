# EN3160 – Assignment 03: Neural Networks

## Folder structure

```
CV-Assignment-03/
├── data/                      # Datasets (not uploaded to GitHub)
│   ├── cifar-10-batches-py/   # CIFAR-10   – Q1
│   ├── MNIST/                 # MNIST      – Q2
│   └── hymenoptera_data/      # Ants/bees  – Q3 (train / val)
├── .venv/                     # Python virtual environment (not uploaded)
├── 230502X_a03.ipynb          # Assignment notebook (Q1–Q3)
├── config.j2                  # LaTeX template for the PDF export
├── requirements.txt           # Python packages + setup commands
├── .gitignore                 # Keeps data/ and .venv/ out of Git
└── README.md
```

## Setup

```bat
python -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Exporting to PDF

```bat
jupyter nbconvert --to pdf --template-file config.j2 230502X_a03.ipynb
```

The template removes the default title block (the notebook has its own) and uses a smaller font for code.

## Datasets

Place each dataset inside `data/` as shown above.

| Dataset | Used in | Source |
|---|---|---|
| CIFAR-10 | Q1 | https://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz (extract into `data/`) |
| MNIST | Q2 | Downloaded from the course Moodle page (zip with `MNIST/raw/`), verified against the official torchvision MD5 checksums |
| Hymenoptera (ants/bees) | Q3 | https://download.pytorch.org/tutorial/hymenoptera_data.zip (extract into `data/`) |
| ResNet18 ImageNet1K weights | Q3 | Downloaded automatically by `torchvision.models.resnet18(weights="IMAGENET1K_V1")` |
