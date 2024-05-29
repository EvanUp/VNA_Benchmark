# VNA_Benchmark
Code and data for the paper "Multimodal LLMs Struggle with Basic Visual Network Analysis: a Visual Network Analysis Benchmark"

Code will be added shortly.
## Visual Network Analysis Benchmark

This repository contains the data and labels for “Multimodal LLMs Struggle with Basic Visual Network Analysis: a VNA Benchmark”

All graphs were generated using the networkx and netgraph python libraries

## Data

The repository contains 4 folders:

* degree
* structural_balance
* connected_components
* labels

the first three folders contain the graph images generated to evaluate GPT-4 and LLAVA and the final folder contains ground-truth labels for each of these graphs. Details on each evaluation are provided below

### Degree

Degree labels can be found in ‘labels/degree_labels.json’. This file is most easily read with `pd.read_json()`. It contains the following fields:

* `num_nodes`:  total number of nodes in the graph
* `max_degree`: maximum degree in the graph. Identical for letter and number graphs
* `nodes_with_max_degree`: a list of nodes with maximal degree.
* `letter_nodes_with_max_degree`: same as the previous column, but with integers mapped to letter IDs.
* `file`: name of the file in either degree/letter_nodeIDs or degree/number_nodeIDs the graph corresponds to.

### Structural Balance

Labels are present in both image and the folder names. All triads in ‘structural_balance/balanced_triads’ are balanced and all triads in ‘structural_balance/imbalanced_triads’ are imbalanced.

### Connected Components

‘connected_component_labels.csv’ contains 3 columns:

* `component_count`: number of components
* `isolate_count`: number of isolates
* `file`: name of the file the labels correspond to

### Citation

```
@article{williams2024multimodal,
  title={Multimodal LLMs Struggle with Basic Visual Network Analysis: a VNA Benchmark},
  author={Williams, Evan M and Carley, Kathleen M},
  booktitle={International Conference on Social Computing, Behavioral-Cultural Modeling and Prediction and Behavior Representation in Modeling and Simulation},
  year={2024},
  url = {https://arxiv.org/abs/2405.06634},
  organization={Springer}
}
```



