# ROCm利用メモ
## Ubuntu 24.04 LTS
- [ROCm installation(Linux)](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/index.html))
- 権限付加
```
sudo usermod -a -G video ${USER}
sudo usermod -a -G render ${USER}
```
## PyTorch on ROCm
- [PyTorch on ROCm](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/install/3rd-party/pytorch-install.html)
- 前準備
  - pthyon venv導入 
    `python3 -m venv .python3.xx_venv`
- 動作確認
