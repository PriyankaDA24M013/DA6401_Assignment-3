# DA6401_Assignment-3





##  Project Structure

```
.
├── dl_agn_3.py                  # Main script for loading data, EDA, and future model development
├── dakshina_dataset_v1.0/      # Dataset directory from Kaggle
│   └── te/
│       └── lexicons/
│           ├── te.translit.sampled.train.tsv
│           ├── te.translit.sampled.dev.tsv
│           └── te.translit.sampled.test.tsv
```

##  Functional Overview

- **Data Loading**:
  - Parses the train/dev/test `.tsv` files containing Roman → Telugu transliterations.
  - Structure: each line contains a Roman script word and its native script equivalent separated by a tab.

- **EDA (Exploratory Data Analysis)**:
  - Displays dataset samples.
  - Checks for null values.
  - Visualizes character length distributions of Roman and Telugu words.
  - Lists unique characters in Roman and Telugu alphabets.

- **WandB Integration**:
  - Uses `wandb` to track experiments.
  - Requires WANDB API key (stored securely with Kaggle secrets integration).

##  How to Run

###  Prerequisites

- Python 3.7+
- Install required libraries:

```bash
pip install torch pandas matplotlib seaborn wandb
```

If using Kaggle:
- Enable GPU.
- Upload `dakshina_dataset_v1.0` to `/kaggle/input`.
- Add your WANDB API Key to "Secrets" as `WANDB_API_KEY`.

### Running the Script

1. Upload `dl_agn_3.py` and dataset to your working directory or Kaggle Notebook.
2. Execute the script cell by cell or run all at once.
3. Visualizations and printed outputs will provide insights into the dataset.

##  Sample Output

- Roman and Telugu character distribution plots
- Data sample previews
- Count of unique characters
- Null checks and dataset sizes

##  Experiment Tracking

- This project uses [Weights & Biases](https://wandb.ai/) to log metrics.
- The script logs in using your `WANDB_API_KEY` from Kaggle secrets.

##  Dataset

- **Name**: Dakshina Dataset (Google Research)
- **Subset Used**: Telugu
- **Files**:
  - `te.translit.sampled.train.tsv`
  - `te.translit.sampled.dev.tsv`
  - `te.translit.sampled.test.tsv`


