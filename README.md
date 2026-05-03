# RUL Prediction – CMAPSS (FD001)

This repository contains LSTM and TCN models for Remaining Useful Life (RUL) prediction using the NASA CMAPSS FD001 dataset.

## Setup

Install the required dependencies:

pip install numpy pandas scikit-learn matplotlib torch tqdm

Tested with:
- Python 3.10.19
- PyTorch 2.5.1 (CUDA 12.1)
- scikit-learn 1.7.2
- numpy 1.26.4
- pandas 2.3.3
- matplotlib 3.10.7
- tqdm 4.67.1

## Data

The FD001 subset used in this project is included in the CMAPSSData/ folder:
- train_FD001.txt
- test_FD001.txt
- RUL_FD001.txt

## Reproducing Results

Pretrained model checkpoints are provided:
- lstm_best.pt
- tcn_best.pt

To reproduce the reported results:
1. Open the notebook Project-dbarrien.ipynb
2. Run all cells except the training loops
3. Run the checkpoint loading, evaluation, and plotting sections

This will reproduce:
- Test RMSE
- PHM score
- Training curves

## Notes

Training was performed on an NVIDIA RTX 500 Ada GPU.
Reproduction can be done on CPU using the provided checkpoints.
Only the FD001 subset is used in this project.
