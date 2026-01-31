# SpectralResynth
一个从[hiirofox/Resys](https://github.com/hiirofox/Resys)获取想法的插件，还没有开工  

# TODO LIST
## feat
  - [ ] 制作最基础的测试
  - [ ] 复音/滑音
  - [ ] unison
  - [ ] Chorus/Wander/Graular(没错，ableton SpectralResonator)
  - [ ] 更多的波形?
## fix

# 克隆到本地
```bash
git clone --recurse-submodules https://github.com/ManasWorld/plugin-template.git
```
或者
```bash
git clone https://github.com/L-MODEL-TEST/l-model-plugin-template.git
cd l-model-plugin-template
git submodule update --init --recursive
```

## MacOS授权

```bash
sudo xattr -dr com.apple.quarantine /path/to/your/plugins/plugin_name.component
sudo xattr -dr com.apple.quarantine /path/to/your/plugins/plugin_name.vst3
sudo xattr -dr com.apple.quarantine /path/to/your/plugins/plugin_name.lv2
```
## 构建

```bash
git clone --recurse-submodules https://github.com/ManasWorld/plugin-template.git

# windows
cmake -G "Visual Studio 17 2022" -DCMAKE_BUILD_TYPE=Release -S . -B ./build

# linux
sudo apt update
sudo apt-get install libx11-dev libfreetype-dev libfontconfig1-dev libasound2-dev libxrandr-dev libxinerama-dev libxcursor-dev
cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -S . -B ./build
cmake --build ./build --config Release

# macOS
cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DCMAKE_OSX_ARCHITECTURES="x86_64;arm64" -S . -B ./build
cmake --build ./build --config Release
```
