# Data Folder

Raw data is **not stored** in this repository.

To reproduce:
```bash
kaggle competitions download -c playground-series-s3e26 -p data/raw
unzip -o data/raw/*.zip -d data/raw
python3 -m src.data_prep --in data/raw --out data/processed
