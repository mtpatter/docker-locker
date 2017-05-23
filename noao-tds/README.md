# noao-tds

[![Docker Automated buil](https://img.shields.io/docker/automated/mtpatter/noao-tds.svg)](https://hub.docker.com/r/mtpatter/noao-tds/)

From noao lsst-tds pre-workshop emails

docker run -i -t -p 8888:8888 -v $PWD:/opt/notebooks noao-tds /bin/bash -c "/opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks/ --ip='*' --port=8888 --no-browser"
