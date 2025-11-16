# Julia Tips
## 既存Packageに修正,機能を追加する方法
1. packageをdevモードにすると,ソースコードをcloneしてくれる.
```
(@v1.12) pkg> dev ONNXNaiveNASflux
     Cloning git-repo `https://github.com/DrChainsaw/ONNXNaiveNASflux.jl.git`
   Resolving package versions...
    Updating `~/.julia/environments/v1.12/Project.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 ⇒ v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` [loaded: `/home/kaz/.julia/packages/ONNXNaiveNASflux/VvDdp/src/ONNXNaiveNASflux.jl` (v0.2.16) expected `/home/kaz/.julia/dev/ONNXNaiveNASflux/src/ONNXNaiveNASflux.jl` (v0.2.16)]
    Updating `~/.julia/environments/v1.12/Manifest.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 ⇒ v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` [loaded: `/home/kaz/.julia/packages/ONNXNaiveNASflux/VvDdp/src/ONNXNaiveNASflux.jl` (v0.2.16) expected `/home/kaz/.julia/dev/ONNXNaiveNASflux/src/ONNXNaiveNASflux.jl` (v0.2.16)]
```
2. 通常のモードに戻したければ,
```
(@v1.12) pkg> free ONNXNaiveNASflux
   Resolving package versions...
    Updating `~/.julia/environments/v1.12/Project.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` ⇒ v0.2.16
    Updating `~/.julia/environments/v1.12/Manifest.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` ⇒ v0.2.16
        Info We haven't cleaned this depot up for a bit, running Pkg.gc()...
      Active manifest files: 1 found
      Active artifact files: 77 found
      Active scratchspaces: 0 found
     Deleted no artifacts, repos, packages or scratchspaces
```
3. 開発モードのときのソースコードは,
```
~/.julia/dev/ONNXNaiveNASflux/
```
が参照される.  
4. Packageをforkして開発したい場合.
```
(@v1.12) pkg> dev git@github.com:seisyuu-hantatsushi/ONNXNaiveNASflux.jl.git
     Cloning git-repo `git@github.com:seisyuu-hantatsushi/ONNXNaiveNASflux.jl.git`
Path `/home/kaz/.julia/dev/ONNXNaiveNASflux` exists and looks like the correct repo. Using existing path.
   Resolving package versions...
    Updating `~/.julia/environments/v1.12/Project.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 ⇒ v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` [loaded: `/home/kaz/.julia/packages/ONNXNaiveNASflux/VvDdp/src/ONNXNaiveNASflux.jl` (v0.2.16) expected `/home/kaz/.julia/dev/ONNXNaiveNASflux/src/ONNXNaiveNASflux.jl` (v0.2.16)]
    Updating `~/.julia/environments/v1.12/Manifest.toml`
  [2e935253] ~ ONNXNaiveNASflux v0.2.16 ⇒ v0.2.16 `~/.julia/dev/ONNXNaiveNASflux` [loaded: `/home/kaz/.julia/packages/ONNXNaiveNASflux/VvDdp/src/ONNXNaiveNASflux.jl` (v0.2.16) expected `/home/kaz/.julia/dev/ONNXNaiveNASflux/src/ONNXNaiveNASflux.jl` (v0.2.16)]
```
