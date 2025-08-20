### config
1. shell config
```bash
cd \
git clone https://github.com/Li-TianCheng/dev_config.git \
sudo apt install zsh -y \
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" \
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting \
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions \
git clone https://github.com/conda-incubator/conda-zsh-completion ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/conda-zsh-completion \
cp dev_config/.zshrc . \
sudo apt install tmux -y \
git clone --single-branch https://github.com/gpakosz/.tmux.git \
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm \
cp .tmux/.tmux.conf.local . \
cp dev_config/.tmux.conf . \
wget https://github.com/neovim/neovim/releases/download/v0.10.3/nvim-linux64.tar.gz \
tar -zxvf nvim-linux64.tar.gz \
cp -r nvim-linux64/* /usr/ \
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime \
sh ~/.vim_runtime/install_awesome_vimrc.sh \
curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim \
curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && sudo apt-get install -y nodejs \
cp dev_config/.vimrc . \
mkdir -p .config/nvim/ \
ln -s ~/.vimrc ~/.config/nvim/init.vim
cp dev_config/coc-settings.json ~/.config/nvim/ \
sudo apt install ack -y \
conda init zsh
```
2. vim-plugs config
```bash
# install vim plugs
:PlugInstall
# install clangd
# sudo apt install clangd
:CocCommand clangd.install
# install coc.nvim plugs
:CocInstall coc-json coc-clangd coc-cmake coc-git coc-pyright coc-sh coc-highlight coc-yaml
```

3. tmux plugs config
```bash
# install tmux plugs
ctrl+b+I
# save
ctrl+b+ctrl+s
# load
ctrl+b+ctrl+r
# win sync
ctrl+b+i
```

* when compiling C++, add in `CMakeList.txt`:
```cmake
set (CMAKE_EXPORT_COMPILE_COMMANDS ON)
```

* python format
```python
pip install autopep8
```
