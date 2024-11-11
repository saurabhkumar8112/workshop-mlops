---
layout: default
title: Dependencies
---

# Dependencies

{% raw %}
```bash
# Install required packages
poetry add torch torchvision wandb gradio "dvc[gs]"

# Activate poetry shell
poetry shell

# Verify installations
python -c "import torch; import wandb; import gradio; import dvc; print('All packages installed successfully!')"
```
{% endraw %}