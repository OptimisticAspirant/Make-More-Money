首先，打开Anaconda Prompt，查看环境列表：
```
conda env list
```
激活你需要加入kernel选项的环境，比如py36:
```
conda activate py36
```
安装ipykernel：
```
conda install ipykernel
```
添加环境，比如py36：
```
python -m ipykernel install --name py36
```
查看kernel：
```
jupyter kernelspec list
```
以上没什么用，不如直接在base环境下安装nb_conda：
```
conda install nb_conda
```