# modulome_cgluta
iModulon structure of Corynebacterium glutamicum

## Create environment
```
conda create --name PyModulon  python=3.7
conda activate PyModulon
pip install pymodulon -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install meme -i https://pypi.tuna.tsinghua.edu.cn/simple
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
conda config --set show_channel_urls yes
conda install mpi4py
conda install blast
python -m ipykernel install --user --name PyModulon --display-name "PyModulon"
```

# Instructions
## Each Jupyter notebook contains usage instructions, and here we provide example and explanations for important files.
* 1_create_the_gene_table_zjx.ipynb
    * Download the FASTA and GFF files for your organism and its plasmids from NCBI.(e.g. `genome.gff3`) 
    * Download the annotation file for your organism from [EggNOG Mapper](http://eggnog-mapper.embl.de/).(e.g. `eggNOG_annotations.txt`)
    * Download the annotation file for your organism from [Biocyc.org](https://biocyc.org/).(e.g. `biocyc_annotations.txt`)
    * Download the annotation file for your organism from [AmiGO 2](http://amigo.geneontology.org/amigo/search/annotation).(e.g. `GO_annotations.txt`) 

* 2_iModulon_characterization_zjx.ipynb
    * M and A matrices(e.g. `M.csv`、`A.csv`)
    * Expression data (e.g. `log_tpm.csv`)
    * Gene table and KEGG/GO annotations (Generated in `create_the_gene_table_zjx.ipynb`)(e.g. `gene_info.csv`)
    * Sample table, with a column for `project` and `condition`(e.g. `sample.csv`)
    * TRN file(e.g. `trn_test.csv`)

* The remaining notebooks are all examples of analyzing iModulons using cgu.json.gz. You can change the icadata to use them.
* The results of our operation are stored in cgu_raw.json.gz and can be directly extracted and used.


