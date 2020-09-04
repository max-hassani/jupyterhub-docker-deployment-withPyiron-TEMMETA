FROM jupyter/minimal-notebook:latest
USER root
RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get install -y libgl1-mesa-glx
RUN /opt/conda/bin/conda install jupyterhub && \
    /opt/conda/bin/conda install -c conda-forge pyiron && \
    /opt/conda/bin/conda install -c conda-forge lammps && \
    /opt/conda/bin/conda install -c conda-forge nodejs nglview && \
    /opt/conda/bin/conda install -c conda-forge temmeta && \
    jupyter labextension install @jupyter-widgets/jupyterlab-manager --no-build && \
    jupyter labextension install nglview-js-widgets
