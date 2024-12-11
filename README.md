# Simple Tutorial for using the cippool gpus via the command line 📖

## 📖 Table of Contents <a href="#top">[Back to Top]</a>

- [Starting Point](#Starting-Point-)
- [Install Anaconda](#Install-Anaconda-)
- [Use Anaconda to create and use the environment](#Use-Anaconda-to-create-and-use-the-environment-)
- [Bonus](#Bonus-)

## 🚀 Starting Point <a name="Starting-Point-"></a> <a href="#top">[Back to Top]</a>
To start to use the cipool server via ssh, please run the following command __based on your operating system__.

### For windows:
please run the following command to install WSL via `cmd`

```bash
wsl --install
```

Then search and open the `wsl` and run the following command to link the cipool server via ssh

```bash
ssh YOUR_LRZ_ID@CIPOOL_SERVER_IP
```
For example, if your LRZ ID is `ra66ttt`, the cippool server ip is `10.153.53.10`, the command should be:

```bash
ssh ra66ttt@10.153.53.10
```

### For Linux/MacOS:
Please run the following command to link the cipool server via ssh

```bash
ssh YOUR_LRZ_ID@CIPOOL_SERVER_IP
```
For example, if your LRZ ID is `ra66ttt`, the cippool server ip is `10.153.53.10`, the command should be:

```bash
ssh ra66ttt@10.153.53.10
```

## ⚙️ Install Anaconda <a name="Install-Anaconda-"></a> <a href="#top">[Back to Top]</a>
To install Anaconda, please run the following command:

```bash
git clone https://github.com/YecanLee/cippool-server-guidance.git
cd cippool-server-guidance
bash env_setup.sh
```

## 📦 Use Anaconda to create and use the environment <a name="Use-Anaconda-"></a> <a href="#top">[Back to Top]</a>
To create an environment, please run the following command:

```bash
conda create -n YOUR_ENV_NAME python=YOUR_PYTHON_VERSION
```
For example, if your environment name is `cipool` and your python version is `3.10`, the command should be:

```bash
conda create -n cipool python=3.10
```

To activate the environment, please run the following command:

```bash
conda activate YOUR_ENV_NAME
```
For example, if your environment name is `cipool`, the command should be:

```bash
conda activate cipool
```

## 🎁 Bonus <a name="Bonus-"></a> <a href="#top">[Back to Top]</a>
To bypass the sudo limitation for installing cuda-toolkit, please run the following command:
```bash
# Activate the environment
conda activate YOUR_ENV_NAME
# Install cuda-toolkit
conda install nvidia/label/cuda-12.2.0::cuda-toolkit
```
