# ROCm利用メモ
## Ubuntu 24.04 LTS
- [ROCm installation(Linux)](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/index.html))
- 権限付加
```
sudo usermod -a -G video ${USER}
sudo usermod -a -G render ${USER}
```
## PyTorch on ROCm
- 前準備
  - pthyon venv導入 
    `python3 -m venv .python3.xx_venv`
  - 仮想環境に移行
    `soruce ./.python3.xx_venv/bin/activate`
- [PyTorch on ROCm](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/install/3rd-party/pytorch-install.html)
- 動作確認
```
(.python3_env) $ python3 -c 'import torch' 2> /dev/null && echo 'Success' || echo 'Failure'
Success
(.python3_env) $ python3 -c 'import torch; print(torch.cuda.is_available())'
True
```
- gfx1103で利用するには...
```
export PYTORCH_ROCM_ARCH=gfx1100
export HSA_OVERRIDE_GFX_VERSION=11.0.0

```