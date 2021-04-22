FROM rocker/binder:4.0.2
LABEL maintainer='Anna Elisabeth Furtjes'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/AnnaFurtjes/OpenMR_Hackathon/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2021-04-22/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
