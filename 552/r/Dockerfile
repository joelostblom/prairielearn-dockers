# Use the base image provided by MDS
FROM ubcmds/base-r:fc31fb0

# Define additional packages that are specific to this course
ENV R_PACKAGES="rlang tidyverse dplyr infer"

# Install the pre-defined R packages
RUN install2.r -e $R_PACKAGES

# Ensure the rlang package is up-to-date
RUN R -e "install.packages('rlang', repos='https://cloud.r-project.org/')"
RUN R -e "install.packages(c('tidyverse', 'dplyr', 'infer'), repos='https://cloud.r-project.org/')"

# End course image