# Use the prairielearn modified version of jupyter lab
FROM prairielearn/workspace-jupyterlab-python:92c4d45d172f248640753e49dd6e4557431e3495

# root required to install for ubuntu commands
USER root

# Install additional system dependencies if needed
RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# jovyan is the default user for jupyter lab
USER jovyan

# Define additional packages not included in Python that are required for all courses
# eg.
# ENV PYTHON_PACKAGES="scipy numpy pandas matplotlib"

# Install the pre-defined Python packages
# eg.
# RUN pip install --no-cache-dir $PYTHON_PACKAGES

# Create directories for user settings
RUN mkdir -p /tmp/jupyter_config/lab/user-settings/@jupyterlab/docmanager-extension/

# Copy the custom plugin.jupyterlab-settings file to the correct location to increase auto-save frequency
COPY plugin.jupyterlab-settings /tmp/jupyter_config/lab/user-settings/@jupyterlab/docmanager-extension/
