可能遇到的问题，“Isaac Gym”没有反应,运行以下两个指令
```
        sudo prime-select nvidia
        export VK_ICD_FILENAMES=/usr/share/vulkan/icd.d/nvidia_icd.json
```
# titi_rl

Python环境：python3.8
```
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```
依赖：
```
conda install matplotlib
pip install opencv-python
```

### 报错1
```
AttributeError: module 'numpy' has no attribute 'float'.
`np.float` was a deprecated alias for the builtin `float`. To avoid this error in existing code, use `float` by itself. Doing this will not modify any behavior and is safe. If you specifically wanted the numpy scalar type, use `np.float64` here.
```
解决：降低numpy版本
```
conda install numpy==1.23.5
```

### 报错2
```
 import tensorboard
ModuleNotFoundError: No module named 'tensorboard'
```
解决
```
pip install tensorboard
```
### 报错3
```
ModuleNotFoundError: No module named 'onnx'
```
```
pip install onnx
```

### 报错4
```
ModuleNotFoundError: No module named 'onnx'
```
```
pip uninstall setuptools
conda install setuptools==58.0.4
```