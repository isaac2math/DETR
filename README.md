## Setup the conda env

```shell

brew install cmake pkg-config

conda env create -f env.yaml

conda activate detr

conda env config vars set TRANSFORMERS_OFFLINE=1
conda env config vars set HF_DATASETS_OFFLINE=1

python -c "from transformers import pipeline; print(pipeline('sentiment-analysis')('we love you'))"
```

## Setup the conda env

```shell
git init
dvc init

git status

git commit -m "Initialize DVC"

dvc add data/raw/data.csv
git add data/raw/data.csv.dvc data/.gitignore
git commit -m "Add raw data"
dvc remote add --default drive gdrive://1_gQ-hEi5MXw1tg57v2lvm4HQWAM394fv
dvc push

```