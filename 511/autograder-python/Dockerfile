# Use the prairielearn r autograder
FROM prairielearn/grader-python:latest

# Define additional packages not included in Python that are required for all courses
# eg.
ENV PYTHON_PACKAGES="scipy numpy pandas matplotlib"

# Install the pre-defined Python packages
# eg.
RUN pip install --no-cache-dir $PYTHON_PACKAGES

# End course image