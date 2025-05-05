FROM r-base:4.4.2
# FROM r-base:4.1.3

RUN apt-get update 
# RUN apt-get install -y r-base
# RUN apt-get install -y dirmngr gnupg apt-transport-https ca-certificates software-properties-common
# RUN apt-get remove -y r-base r-base-core

# RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
# RUN add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu focal-cran40/'

# RUN apt-get install -y r-base r-base-core r-recommended r-base-html r-doc-html 
RUN apt-get update -y
RUN apt-get install -y usrmerge
RUN apt-get install -y xml2 libxml2-dev libcurl4-openssl-dev libnode-dev libproj-dev libgdal-dev libfontconfig1-dev

RUN R -e "install.packages('RCurl',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('XML',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('foreach',dependencies=TRUE, repos='http://cran.rstudio.com/')" 
RUN R -e "install.packages('optparse',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('suncalc',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('flock',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('alphahull',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('rgdal',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('EMCluster',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN apt-get install -y libharfbuzz-dev libfribidi-dev
RUN R -e "install.packages('pkgdown',dependencies=TRUE, repos='http://cran.rstudio.com/')"
# RUN R -e "install.packages('RcppAlphahull',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('devtools',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "devtools::install_github('https://github.com/federicoairoldi/ProgettoPACS', subdir = 'RcppAlphahull')"
RUN R -e "install.packages('stringr',repos = c('http://cran.us.r-project.org'))"
RUN R -e "install.packages('rstan',repos = c('https://mc-stan.org/r-packages/', getOption('repos')))"
RUN R -e "install.packages('tripack',dependencies=TRUE, repos='http://cran.rstudio.com/')"

COPY . /code
WORKDIR /code/R
