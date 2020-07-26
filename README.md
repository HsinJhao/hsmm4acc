# 仓库介绍
- 原仓库[链接](https://github.com/wadpac/hsmm4acc)
- 项目来源:NLeSC与UCL合作项目，主要对青少年的运动传感器数据进行分析，即基于可佩戴运动设备内部的传感器数据进行行为检测(Behaiour Detection)
- 主要方法:隐半马尔科夫模型，即Hidden Semi Markov Models(HSMM).基于python第三方库[pyhsmm](https://github.com/mattjj/pyhsmm).

## Installation
Prerequisites:
*  Python 2.7
* pip

### Instalation with conda
Navigate to the root of this repository. Create a conda environment with the environment.yml file:
 
`conda env create -f environment.yml`

Activate the environment:

`source activate ucl`

Then install the package:

`pip install .`

### Installation with pip
Navigate to the root of this repository. To install, try:

`pip install .`

### Installation troubleshooting
#### ImportError: No module named hmm_messages_interface
The `pyhsmm` package needs the right gcc compiler (it seems to work with gcc 4.7).  You can clone the pyhsmm package and compile it:

`python setup.py build_ext`

Which should solve the issue.
See also https://github.com/mattjj/pyhsmm/issues/55. 

#### Intel MKL FATAL ERROR: Cannot load libmkl_avx.so or libmkl_def.so.
You can disable the use of mkl with:
`conda install nomkl`



### Running tests
To run tests:

`nosetests test/`


