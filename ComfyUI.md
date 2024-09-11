# 前期工具准备草稿

1.安装miniconda

2.安装英特尔oneAPI 基础工具套件

3.安装[Visual Studio 2022](https://visualstudio.microsoft.com/zh-hans/vs) 社区版下载  并选择“[使用 C++ 进行桌面开发]([在 Visual Studio 中安装 C 和 C++ 支持 |Microsoft 学习](https://learn.microsoft.com/en-us/cpp/build/vscpp-step-0-installation?view=msvc-170#step-4---choose-workloads))”工作负载进行安装

### 1.[安装miniconda]([Miniconda — Anaconda 文档](https://docs.anaconda.com/miniconda/))

下载对应版本下载并安装

### 2.[安装英特尔oneAPI 基础工具套件]([Download the Intel® oneAPI Base Toolkit](https://www.intel.cn/content/www/cn/zh/developer/tools/oneapi/base-toolkit-download.html))

选择安装方式，两者都可以

### 3.安装[Visual Studio 2022](https://visualstudio.microsoft.com/zh-hans/vs)

## 2.克隆[ComfyUI]([comfyanonymous/ComfyUI: The most powerful and modular diffusion model GUI, api and backend with a graph/nodes interface. (github.com)](https://github.com/comfyanonymous/ComfyUI)) 并进入到该文件夹下

```
git clone https://github.com/comfyanonymous/ComfyUI.git
```

## 3.创建conda环境

1.创建环境

```
conda create -n comfyuienv python=3.11
```

comfyuienv是环境名，自己写一个容易记的即可

2.激活环境

```
conda activate comfyuienv
```

## 4.安装[IPEX]([Welcome to Intel® Extension for PyTorch* Documentation!](https://intel.github.io/intel-extension-for-pytorch/index.html#installation?platform=gpu))

```
conda install pkg-config libuv
```

```
python -m pip install torch==2.1.0.post3 torchvision==0.16.0.post3 torchaudio==2.1.0.post3 intel-extension-for-pytorch==2.1.40+xpu --extra-index-url https://pytorch-extension.intel.com/release-whl/stable/xpu/cn/
```

```
call "C:\Program Files (x86)\Intel\oneAPI\setvars.bat"
```

```
pip install -r requirements.txt
```

```
python main.py --use-pytorch-cross-attention
```

启动A-Start