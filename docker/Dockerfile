FROM hysds/pge-base:latest
MAINTAINER jlinick "Justin.P.Linick@jpl.nasa.gov"
LABEL description="EONET scraper"

USER ops
# copy packages
COPY . /home/ops/verdi/ops/eonet

WORKDIR /home/ops
CMD ["/bin/bash", "--login"]
