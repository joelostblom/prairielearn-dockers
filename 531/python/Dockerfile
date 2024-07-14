# Use the base image provided by MDS
FROM zacwarham/ubc-mds-pl:base-python

# Define additional packages that are specific to this course
ENV PYTHON_PACKAGES="altair vega_datasets"

# Install the pre-defined Python packages
RUN pip install --no-cache-dir $PYTHON_PACKAGES

# Start JupyterLab by default
CMD ["jupyter", "lab"]

# End course image