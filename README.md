# Python-Notebook
## Content
- **Introduction to Python**
  - [Markdown](Introduction_to_Python.md)
  - [Jupyter Notebook](Introduction_to_Python.ipynb)
  
## Starting Jupyter Lab
**Local**
```bash
$ jupyter lab --core-mode
```

**Docker**
```bash
$ docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes -v "$PWD":/home/jovyan/work jupyter/datascience-notebook
```
  
  

