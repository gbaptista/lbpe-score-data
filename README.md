# LBPE Score Data

Supporting data for the LBPE Score and MMLU replication.

The content was intentionally compressed to prevent data leaks, thereby avoiding contamination of the models.

## Setup

This repository utilizes [Git Large File Storage](https://git-lfs.com):

```sh
git lfs install
```

## Check and Extraction

```sh
git clone https://github.com/gbaptista/lbpe-score-data.git

cd lbpe-score-data

# Ensure the integrity and reliability of the data:
md5sum -c data.md5
# data.tar.gz: OK

# Extract the content:
tar -xzvf data.tar.gz
```

Move the extracted folder to inside the `lbpe-score` folder:
```sh
git clone https://github.com/gbaptista/lbpe-score.git

cd lbpe-score

mv ~/lbpe-score-data/data data
```

## Development

```sh
git lfs track "*.tar.gz"

tar -czvf data.tar.gz data/

md5sum data.tar.gz > data.md5
```
