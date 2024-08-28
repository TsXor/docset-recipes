# conan-io/docs

## 安装doc2dash
```bash
pip install doc2dash
```

## 下载源码并选择版本
```bash
git clone https://github.com/conan-io/docs.git
# 按照具体情况在下面2条命令中选1条执行
git checkout release/1.65.0 # 最后一个conan-v1版本
git checkout release/2.6 # 目前最新的conan-v2版本
```

## 配置环境
首先创建一个`venv`，然后安装这里提供的`reqirements.txt`。
```bash
python -m venv .venv
# 按照具体情况在下面3条命令中选1条执行
.venv\Scripts\activate.bat # Windows cmd.exe
.venv\Scripts\Activate.ps1 # Windows PowerShell
source .venv/bin/activate # Linux/MacOS bash
pip install -r requirements.txt
```

## 构建与打包
```bash
sphinx-build -M html . build
# 按照具体情况在下面2条命令中选1条执行
doc2dash -n conan-v1 build/html # 之前选择的版本为conan-v1
doc2dash -n conan-v2 build/html # 之前选择的版本为conan-v2
```
