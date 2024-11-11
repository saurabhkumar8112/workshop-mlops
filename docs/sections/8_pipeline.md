# Start fresh
rm -rf data/ model.pth wandb/
git checkout .

# Step 1: Get Data
dvc pull

# Step 2: Train Model
python train.py
# Show W&B dashboard during training

# Step 3: Deploy
python demo.py
# Show predictions working

# Step 4: Version Control Demo
# Modify data
rm -rf data/MNIST/raw/train-images-idx3-ubyte.gz
dvc add data/
git add data.dvc
git commit -m "Remove training data"
dvc push

# Restore original data
git checkout HEAD~1 data.dvc
dvc checkout