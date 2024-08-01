FROM quay.io/jupyter/base-notebook:python-3.11

# Install from the requirements.txt file
COPY --chown=${NB_UID}:${NB_GID} requirements.txt /tmp/
RUN pip install --no-cache-dir --requirement /tmp/requirements.txt && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

WORKDIR /home/jovyan/work

CMD ["start-notebook.py", "--no-browser", "--IdentityProvider.token=''"]