## MDFCL: Multi-modal data fusion based graph contrastive learning framework for molecular property prediction ##

This repository is dedicated to releasing the implementation of the models utilized in the paper named  ["MDFCL: Multi-modal data fusion based graph contrastive learning framework for molecular property prediction"](). 

In this work, we incorporate exhaustive information from dual molecular data modalities, namely graph and sequence structures. Subsequently, adaptive data augmentation strategies are designed based on the molecular backbones and side chains for multimodal data. Built upon these augmentation strategies, we develop a graph contrastive learning framework and pre-train it with unlabeled data ($\sim$ 10M molecules).

The paper is under review and the code will be available after the paper is accepted.

Please stay tuned for updates!

Thank you！



### Dataset

You can download the pre-training data and benchmarks used in the paper [here](https://drive.google.com/file/d/1aDtN6Qqddwwn2x612kWz9g0xQcuAtzDE/view?usp=sharing) and extract the zip file under `./data` folder. The data for pre-training can be found in `pubchem-10m-clean.txt`. All the databases for fine-tuning are saved in the folder under the benchmark name. You can also find the benchmarks from [MoleculeNet](https://moleculenet.org/).

### Pre-training

To train the MDFCL, where the configurations and detailed explaination for each variable can be found in `config.yaml`
```
$ python pretraining.py
```

### Fine-tuning 

To fine-tune the MDFCL pre-trained model on downstream molecular benchmarks, where the configurations and detailed explaination for each variable can be found in `config_finetune.yaml`
```
$ python finetune.py
```



## Acknowledgement



- PyTorch implementation of MolCLR: [https://github.com/yuyangw/MolCLR](https://github.com/yuyangw/MolCLR)

- PyTorch implementation of N-Gram: [https://github.com/chao1224/n_gram_graph](https://github.com/chao1224/n_gram_graph)

- PyTorch implementation of GraphDTA:[https://github.com/thinng/GraphDTA](https://github.com/thinng/GraphDTA)

- Strategies for Pre-training Graph Neural Networks: [https://github.com/snap-stanford/pretrain-gnns](https://github.com/snap-stanford/pretrain-gnns)

  

