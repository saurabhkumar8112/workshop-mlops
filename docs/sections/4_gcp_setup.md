# Install Google Cloud SDK (if needed)
brew install google-cloud-sdk  # for macOS

# Setup Google Cloud
gcloud auth login
gcloud auth application-default login

# Create new bucket (if needed)
gsutil mb gs://YOUR_BUCKET_NAME

# Initialize DVC with Google Cloud Storage
dvc init
dvc remote add -d storage gs://YOUR_BUCKET_NAME/dvc-store
git add .dvc/config
git commit -m "Configure DVC with GCS"

# Verify remote
dvc remote list