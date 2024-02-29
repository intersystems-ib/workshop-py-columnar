# workshop-py-columnar
Columnar and row storages comparation based on a Python project developed using Jupyter Notebook connected using the official library to IRIS.

You can find more in-depth information in https://learning.intersystems.com.


# What do you need to install? 
* [Git](https://git-scm.com/downloads) 
* [Docker](https://www.docker.com/products/docker-desktop) (if you are using Windows, make sure you set your Docker installation to use "Linux containers").
* [Docker Compose](https://docs.docker.com/compose/install/)
* [Visual Studio Code](https://code.visualstudio.com/download) + [InterSystems ObjectScript VSCode Extension](https://marketplace.visualstudio.com/items?itemName=daimor.vscode-objectscript)

# Setup
Build the image we will use during the workshop:

```console
$ git clone https://github.com/intersystems-ib/workshop-py-columnar
$ cd workshop-py-columnar
$ docker-compose build
```

# Configuration

The main purpose of this example is to test the performance of different storage types (columnar or row) that InterSystems IRIS provides connecting it using Python libraries from a Jupyter Notebook project.


## Test Production 
* Run the containers that we will use in the workshop:
```
docker-compose build

docker-compose up -d
```
Automatically an IRIS instance will be deployed, a Jupyter Notebook is deployed under (http://localhost:8888) too.


## IRIS database

* Open the [Management Portal](http://localhost:52774/csp/sys/UtilHome.csp).
* Login using the default `superuser`/ `SYS` account.
* Open System Explorer --> SQL
* Select NAMESPACE USER and Schema `Test`

# Testing with Jupyter Notebook

This project is devolped in Python using Jupyter Notebook, you can access to it from [here](http://localhost:8888) and open PerformanceTests.ipnyb file.
![alt text](/images/jupyter.png)

You can test the project step by step or execute it at one time, feel free.