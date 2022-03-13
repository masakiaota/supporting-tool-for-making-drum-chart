
# FROM jupyter/datascience-notebook:lab-3.0.16 

# SHELL ["/bin/bash", "-l", "-c"]

# # passの回避
# USER root
# # apt-get系
# RUN apt-get update &&\
#     apt-get install -y fish htop
# USER jovyan

# RUN conda install --quiet --yes --freeze-installed -c conda-forge jupyterlab=3.1.1

# #passwordの無効化
# RUN echo "c.NotebookApp.token = '' ; c.NotebookApp.password = ''" >> /home/jovyan/.jupyter/jupyter_notebook_config.py

# # pip install系
# RUN pip install --upgrade japanize-matplotlib tabulate tqdm joblib autopep8 &&\
#     pip install streamlit &&\
#     pip install --upgrade protobuf


# # install dependencies using conda
# RUN conda install --quiet --yes -c conda-forge ffmpeg libsndfile
# # install spleeter with pip
# RUN pip install spleeter omnizart
# RUN pmnizart download-checkpoints
# # M1macで動かなくて発狂しちゃう


FROM mctlab/omnizart:latest

USER root
SHELL ["/bin/bash", "-c"]

# RUN mkdir /tmp &&\ chmod 777 /tmp
# RUN apt-get update &&\
#     apt-get install -y fish htop

RUN pip install --upgrade pip &&\
    pip install jupyterlab tqdm joblib autopep8

