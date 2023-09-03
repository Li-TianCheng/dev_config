### auto config

1. install 
```bash
# node(>=14.0)
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash - &&\
sudo apt-get install nodejs
# vim(>=8.2)
sudo apt install vim
# tmux
sudo apt install tmux
# zsh
sudo apt install zsh
```

2. git clone and copy to home
```bash
git clone https://github.com/Li-TianCheng/dev_config.git
cd dev_config
cp -rf `ls -a . | grep -w '\.[^g.].*' | xargs` $HOME/
```

3. install clangd by coc.nvim on vim
```
# sudo apt install clangd
:CocCommand clangd.install
```

* when compiling C++, add in `CMakeList.txt`:
```cmake
set (CMAKE_EXPORT_COMPILE_COMMANDS ON)
```

### manual config
1. zsh config
```bash
# install zsh
sudo apt install zsh
# install oh-my-zsh and plugs
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/conda-incubator/conda-zsh-completion ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/conda-zsh-completion
# copy .zshrc to $HOME
cp .zshrc $HOME
```
2. tmux config
```bash
# install tmux
sudo apt install tmux
# copy .tmux.conf to $HOME
cp .tmux.conf $HOME
```
3. vim config
```bash
# install vim
sudo apt install vim
# install vimrc
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
# install vim-plug
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
# install node
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
# copy .vimrc to $HOME
cp .vimrc $HOME
# copy coc-settings.json to $HOME/.vim
cp .vim/coc-settings.json $HOME/.vim
```
4. install plugs by vim
```bash
# install vim plugs
:PlugInstall
# install clangd
# sudo apt install clangd
:CocCommand clangd.install
# install coc.nvim plugs
:CocInstall coc-json coc-clangd coc-cmake coc-git coc-pyright coc-sh coc-hightlight coc-yaml
```
