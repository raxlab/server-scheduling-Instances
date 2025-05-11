# Benchmark Instances for the Server Scheduling Problem

This repository hosts a collection of benchmark instances originally released by Rodrigo Carrasco. They are now updated and maintained here for broader accessibility and reproducibility.

The instances were initially made available through [Mendeley Data](https://doi.org/10.17632/PH95D337DJ.1) and have been used in various research projects related to scheduling jobs on servers with different constraint requirements.

## 📁 Repository Structure

```dir
server-scheduling-Instances/
├── release dates/ # instances that have precedence constraints and release dates
├── .gitignore
├── LICENSE
├── README.md
```

## 🧩 Data Description

The data is divided into 5 ZIP files. Each zip file contains a collection of text files, each containing the information of all jobs arriving at the server on a given day.

The text file structure is as follows:
```
<instance ID>
p
<list of CPU cycles required>
w
<list of priority weights>
r
<list of release dates>
pr
<list of precedence constraints in pairs of the form [parent, child]>
```

The information in p, w, and r follows the format of dictionaries in Python (job ID: information), whereas pr has the format of a Python list.

The "results.xls" file has 10 Excel sheets, with the best lower and upper bound (i.e., schedule value) known for that instance. There are two sheets for each set of instances, one with the results considering release dates (ends in "wr") and one with the results without considering release dates (ends in "nr"). 

In all cases, the schedule was evaluated as total completion time plus total energy consumption, as described in Carrasco, Iyengar, and Stein's "Resource Cost Aware Scheduling" [`DOI`](https://doi.org/10.1016/j.ejor.2018.02.059).


## 🚀 Getting Started

You can use the instances directly by cloning this repo.

## 📚 Citation
If you use these instances in your research, please cite the original article that used the dataset:

Carrasco, R.; Iyengar, G.; Stein, C. (2018), Resource cost aware scheduling, European Journal of Operational Research.
--------

```cite
@article{Carrasco2018:rcasEjor,
 annote = {url_dataset: "https://data.mendeley.com/datasets/ph95d337dj/1"},
 author = {Carrasco, Rodrigo A. and Iyengar, Garud and Stein, Cliff},
 doi = {10.1016/j.ejor.2018.02.059},
 issn = {03772217},
 journal = {European Journal of Operational Research},
 month = {sep},
 number = {2},
 pages = {621--632},
 title = {Resource cost aware scheduling},
 url = {https://www.researchgate.net/publication/323634007_Resource_Cost_Aware_Scheduling},
 volume = {269},
 year = {2018}
}
```

--------
## Acknowledgments

This research was partially supported by Conicyt Fondecyt grant 1151098 and Conicyt PIA Anillo grant ACT 1407.
