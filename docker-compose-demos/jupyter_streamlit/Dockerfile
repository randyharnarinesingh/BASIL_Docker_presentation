FROM jupyter/datascience-notebook
ENV GRANT_SUDO=yes 
ENV JUPYTER_ENABLE_LAB=yes
USER root
RUN sudo apt-get update && sudo apt-get -y upgrade  # update system
COPY ./jupyter_notebook_config.py /home/jovyan/.jupyter/
COPY ./requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
RUN rm requirements.txt
RUN rm -r /home/jovyan/work
