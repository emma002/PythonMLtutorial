# 环境配置操作流程说明

## 1. 本地部署

### 1.1 安装 Conda
1. 下载并安装 [Miniconda](https://docs.conda.io/en/latest/miniconda.html) 或 [Anaconda](https://www.anaconda.com/products/distribution)。
2. 安装完成后，打开终端（Windows 用户可以使用 Anaconda Prompt）并运行以下命令以验证安装：
   ```bash
   conda --version

### 1.2 创建课程环境
1. 使用 Conda 创建一个新的环境，并指定 Python 版本：
    ```bash
    conda create -n course_env python=3.10

2. 激活环境：
    ```bash
    conda activate course_env

### 1.3 安装依赖包
1. 将 requirements.txt 文件放在项目目录下。
    使用 pip 安装依赖包，并指定清华源以加速下载：
    ```bash
    pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

### 1.4 配置 Jupyter Notebook 和 VSCode
1. 在激活的环境下安装 Jupyter Notebook：
    ```bash
    pip install jupyter notebook
2. 将 Jupyter Notebook 内核链接到课程环境：
    ```bash
    python -m ipykernel install --user --name=course_env --display-name "course_env"
3. 打开 Jupyter Notebook：
    ```bash
    jupyter notebook

4. 在 VSCode 中，选择 course_env 作为 Python 解释器：
    打开 VSCode，按下 Ctrl+Shift+P，输入 Python: Select Interpreter，然后选择 course_env。

### 1.5 准备代码
将课程代码克隆或下载到本地目录。
在 Jupyter Notebook 或 VSCode 中打开代码文件，开始编写和运行代码。

# 2. 集群部署
https://docs.hpc.sjtu.edu.cn/studio/jupyter.html 
