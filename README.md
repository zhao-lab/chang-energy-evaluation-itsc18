# Fuel Economy and Emission Testing for Connected and Automated Vehicles Using Real-world Driving Datasets

Developed the new evaluation method and standard which could evaluate the impacts on energy consumption and environmental pollution of CAV fairly, especially under the various traffic conditions. In this project, we proposed a new method to evaluate the fuel economy and emission level of the evaluated vehicle based on the unsupervised learning of the real-world driving data of the evaluated vehicle and typical driving primitive analysis of the naturalistic driving dataset of a large number of different vehicles. For more information see our paper "Fuel Economy and Emission Testing for Connected and Automated Vehicles Using Real-world Driving Datasets" [https://arxiv.org/abs/1805.07643v1]

## Getting Started

These instructions will get you a copy of the project up and running on your machine for development and testing purposes. 

### Prerequisites

these packages are needed:

```
numpy
matplotlib
os
scipy
csv
copy
time
sqlalchemy
sklearn
pyhsmm
```

For training purpose, we suggest that runing the code on Google Cloud Computing or other servers. We also used Jupyter Notebook for debuging and these tools all are highly recommented. 

### Installing

Install python packages:


For most packages you can use this easy way to install

```
pip install packagename
```

But installing package pyhsmm is a little bit triky. [pyhsmm github repository](https://github.com/mattjj/pyhsmm.git) 

An usefull summaries as follows:
1.download pyhsmm from pyhsmm github repository](https://github.com/mattjj/pyhsmm.git)    
2. install "future" and  "pybasicbayes" first. Because we found that it won't work without package "future" and "pybasicbayes".
```
pip install future
pip install pybasicbayes
```
   
3.change to the pyhsmm-master directory and install setup.py
```
cd /…/pyhsmm-master
python setup.py install
```
Congradulations! You have installed all the packages on your machine.

## Running the code

Basically, there are six parts of the code:   
1)data query   
2)posteriorl model    
3)real data process    
4)statis and results    
5)constrained K means clustering    
6)KL divergence   
How the code arranged and worked, see comments in the ipynb files.

### Data Query

Query data from server of UMICH TRI. If this sever are not avalibel for you, you can use the data published by federal government. 

```
http://
```

### Posterial Model

trained data by using pyhsmm package.
For more introduction about how to use pyhsmm. See:

```
https://github.com/mattjj/pyhsmm
```

### Real Data Process
data with fuel consumption for the validate vehicle 

### Statis and Results
Extracted the training results from the posteriol model


### constrained K means clustering 
Combined with package "conclust" in R to get the clusters with background knowledge.

### KL divergence
Calculated the cluster distribution distance between valicate vehicle and big data models.

## Authors

* **Weiqing Yang**  - [Weiqing Yang](https://github.com/VinchinYang)
* **Yan Chang** - [Yan Chang](https://github.com/yanyanlucky)
* **Ding Zhao**

See also the list of [contributors](https://github.com/zhao-lab/chang-energy-evaluation-itsc18/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

