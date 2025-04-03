# Machine Learning Docker images

Docker images based on Nvidia Cuda images with Python pre-installed alongside [uv](https://github.com/astral-sh/uv), a package and project manager.

Python version available :
- 3.10
- 3.11
- 3.12

Python packages preinstalled :
- torch
- torchvision
- transformers
- smolagents[transformers]
- matplotlib
- seaborn
- numpy
- pandas
- scikit-learn
- scipy
- datasets

## How to use

```dockerfile
FROM maxenceleguery/python-cuda-uv:3.10 # Choose your Python version

COPY requirements.txt . # Copy your own requirements.txt
RUN uv pip install -f requirements.txt

# Then copy your code
...

CMD ["uv", "run", "main.py"] # Use uv run command to eecute your script/project/application
```