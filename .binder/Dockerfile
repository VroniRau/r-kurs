FROM rocker/binder:4.3.2
LABEL maintainer='maintainer'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}

RUN wget https://raw.githubusercontent.com/VroniRau/r-kurs/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'https://packagemanager.posit.co/cran/2024-02-27/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
