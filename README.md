# Essential Sparsity GLUE Benchmark

This repository contains a PyTorch and Hugging Face Transformers implementation for benchmarking **BERT-base** and **DistilBERT** on selected **GLUE benchmark tasks** using the experimental configuration described in the Essential Sparsity study.

---

## Experimental Configuration

| Parameter | Value |
|-----------|-------|
| Models | BERT-base, DistilBERT |
| Tasks | GLUE |
| Framework | PyTorch + Hugging Face Transformers |
| Random Seed | 42 |
| Optimizer | AdamW |
| Learning Rate | 2e-5 |
| Weight Decay | 0.01 |
| Batch Size | 16 |
| Warmup Ratio | 10% |
| LR Scheduler | Linear Decay |
| Epochs | 5 |
| Maximum Sequence Length | 128 |

---

## GLUE Tasks

The notebook supports the following GLUE datasets:

- SST-2
- QNLI
- QQP
- WNLI
- MNLI
- MRPC
- RTE

---

## Evaluation Metrics

The benchmark computes:

- Accuracy
- Precision
- Recall
- F1-Score
- GPU Memory Usage
- Inference Latency
- Throughput
- Energy Consumption (estimated)
- Training Time

---

## Project Structure

```
Essential-Sparsity-GLUE-Benchmark/
│
├── Essential_Sparsity_Benchmark.ipynb
├── README.md
└── results/
```

---

## Requirements

- Python 3.10+
- PyTorch
- Hugging Face Transformers
- Datasets
- Evaluate
- Scikit-learn
- NumPy
- Pandas
- NVIDIA GPU (recommended)

Install dependencies:

```bash
pip install transformers datasets evaluate torch scikit-learn pandas numpy pynvml
```

---

## Running the Notebook

1. Open the notebook in Kaggle or Jupyter Notebook.
2. Enable GPU acceleration.
3. Run all cells sequentially.
4. The notebook trains the selected model(s) on the specified GLUE task(s).
5. Results are displayed as a benchmark table after evaluation.

---

## Output Metrics

| Dataset | Model | Accuracy | Precision | Recall | F1 | Memory | Latency | Throughput | Energy |
|----------|--------|----------|-----------|--------|----|---------|----------|-------------|--------|

---

## Notes

- Models are trained using the official GLUE training split.
- Evaluation is performed on the corresponding GLUE validation split.
- Training follows the specified optimizer, scheduler, learning rate, and batch size configuration.
- GPU memory, latency, throughput, and energy are reported for benchmarking purposes.

---

## References

- Devlin et al., **BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding**
- Sanh et al., **DistilBERT**
- GLUE Benchmark
- Hugging Face Transformers
- Essential Sparsity

---

## Author

Rajiv Pradhan
