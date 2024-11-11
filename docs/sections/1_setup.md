# 1_setup.md
---
layout: default
title: Environment Setup
---

# Environment Setup

{% raw %}
```bash
# Create and enter project directory
mkdir ml_workshop
cd ml_workshop

# Set up Python with pyenv
pyenv install 3.12.0
pyenv local 3.12.0
python --version  # Verify 3.12.0

# Install Poetry
curl -sSL https://install.python-poetry.org | python3 -

# Initialize new project
poetry init
# Package name: ml-workshop
# Version: 0.1.0
# Description: MLOps Workshop
# Author: Saurabh Kumar
# Python requires: ^3.12
# No for interactive dependencies
```
{% endraw %}
