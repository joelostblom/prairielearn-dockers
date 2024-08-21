# Use the prairielearn r autograder
FROM prairielearn/grader-r:latest

# Define additional packages that are specific to this course
ENV R_PACKAGES="rlang tidyverse dplyr infer"

# Install the pre-defined R packages
RUN install2.r -e $R_PACKAGES

# Ensure the rlang package is up-to-date
RUN R -e "install.packages('rlang', repos='https://cloud.r-project.org/')"
RUN R -e "install.packages(c('tidyverse', 'dplyr', 'infer'), repos='https://cloud.r-project.org/')"

# End course image