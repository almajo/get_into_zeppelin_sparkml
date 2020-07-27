# Get into Scala/Spark/Zepplin

I wanted to get to know some new technologies, apart from the Python Stack, that are typically used for Data Exploration, Machine Learning, ...

In this zeppelin notebook I did some (light) EDA work, followed by typical binary classifiers on a public version of the famous Titanic dataset.

The notebook is self-contained, i.e. the data is downloaded inside.

## Usage

### Requirements:

- Podman or Docker

### Getting Started

As I am working on a Fedora 31 workstation, I used Podman over Docker because it does not need sudo accesses and it is preinstalled.

The zeppelin notebook can be started with:

'''sh
podman run -p 8080:8080 --rm --name zeppelin apach/zeppelin:0.9.0
'''

or to directly load the notebook inside:

'''sh
podman run -p 8080:8080 --rm -v $PWD/notebook:/notebook -e ZEPPELIN_NOTEBOOK_DIR=/notebook --name zeppelin apach/zeppelin:0.9.0
'''

However sometimes there are permission errors when mounting a volume into the container. Then you could choose the first version and simply import the notebook file via the gui.
