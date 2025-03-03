fgpoa
========================================================================

fgpoa (Foled graph partial order alignment) is designed to use a folded genome graph structure(the following figure) and improve both the sequence-to-graph scoring algorithm and the optimal alignment backtracking algorithm to develop a fast, memory-efficient, and highly accurate method for sequence-to-graph alignment tool.

<p align="center">
<img src="https://i.postimg.cc/jdZGGxwP/fig1-600dpi.png" height="250"/>
</p>

## Download and compile



```sh
git clone https://github.com/zzzerd/fgpoa.git
cd fgpoa && make
```



## Usage

* Produce help page
```sh
abpoa -h
```

* Align a set of query sequences against a reference DAG (in .gfa format):
```sh
abpoa -i graph.gfa -r 4 -b -1 -o outputfile.txt reads.fq
```


**Note:**  Currently only alignment is supported and sequence graph cannot be generated.

**Output file format:** The output is tab-delimited with each line consisting of the maximum score, path matching, and cigar. The path is represented as a tuple of segments and base offsets.

## <a name=“publication”></a>Publication

- **Yanfei Deng, Jinjun Kang, Zhuang Liu, Xiao Zhu, Wei Quan**. "[Fast sequence to graph alignment based on graph folding](10.1109/BIBM62325.2024.10822090)". *2024 IEEE International Conference on Bioinformatics and Biomedicine (BIBM). IEEE, 2024: 5194-5201*.