---
layout: default
title: Git Setup
---

# Git Setup

{% raw %}
```bash
git init

# Create .gitignore
cat > .gitignore << EOL
*.pyc
__pycache__/
.env
.venv/
data/
wandb/
model.pth
.gcloud/
credentials.json
EOL

# Initial commit
git add .
git commit -m "Initial project setup"
```
{% endraw %}