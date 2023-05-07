1. install 
```bash
# node(>=14.0)
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
# vim(>=8.2)
sudo apt install vim
# tmux
sudo apt install tmux
# zsh
sudo apt install zsh
```

2. git clone and copy to home
```bash
git clone https://github.com/Li-TianCheng/dep_config.git
cd dep_config
cp -rf ./.vim* .tmux* .*zsh* $HOME/
```

3. install coc.nvim dep on vim
```
:CocCommand clangd.install
:CocInstall coc-json coc-clangd coc-cmake coc-git coc-highlight coc-pyright coc-sh
```

* When compiling C++, add in `CMakeList.txt`:
```cmake
set (CMAKE_EXPORT_COMPILE_COMMANDS ON)
```