---
layout: default
title: DVC Setup
---

# DVC Setup

{% raw %}
```bash
# Download MNIST dataset
python download_mnist.py

# Initial data versioning
dvc init
dvc add data/
git add data.dvc .gitignore
git commit -m "Add complete MNIST dataset"
dvc push

# Demonstrate versioning by modifying data
rm -rf data/MNIST/raw/train-images-idx3-ubyte.gz
rm -rf data/MNIST/raw/train-labels-idx1-ubyte.gz

# Track modified dataset
dvc add data/
git add data.dvc
git commit -m "Keep only test dataset"
dvc push

# Show version switching
git checkout HEAD~1 data.dvc
dvc checkout
ls data/MNIST/raw/  # Shows all files

# Return to test-only version
git checkout main data.dvc
dvc checkout

# Complete removal and restore demo
rm -rf data/
dvc pull  # Restores current version
```
{% endraw %}