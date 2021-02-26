# ml101


[continuumio/miniconda3](https://hub.docker.com/r/continuumio/miniconda3) instructions for running a notebook on Windows:
 
```
docker run ^
-it ^
--rm ^
--name miniconda3container01 ^
-p 8888:8888  ^
-v %cd%:/cntmnt:rw ^
continuumio/miniconda3 ^
/bin/bash  -c "/opt/conda/bin/conda install jupyter -y --quiet && /opt/conda/bin/jupyter notebook --notebook-dir=/cntmnt --ip='*' --port=8888 --no-browser --allow-root"

```
  
Manual setup
```
docker run ^
-it ^
--rm ^
--name miniconda3container01 ^
-p 8888:8888  ^
-v %cd%:/cntmnt:rw ^
continuumio/miniconda3 ^
/bin/bash 
```
```
# pip install matplotlib
/opt/conda/bin/conda install -c conda-forge matplotlib -y 
/opt/conda/bin/conda install -c anaconda seaborn pandas scikit-learn -y 
/opt/conda/bin/conda install jupyter -y --quiet && /opt/conda/bin/jupyter notebook --notebook-dir=/cntmnt --ip='*' --port=8888 --no-browser --allow-root
```

