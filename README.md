## Prequisite
Go to dir `tmp`
### pip
```
wget https://bootstrap.pypa.io/get-pip.py . 
python3 get-pip.py
```
### nvim + vim plug + python
```
mkdir ~/.local/bin
wget https://github.com/neovim/neovim/releases/download/v0.6.1/nvim.appimage 
chmod +x nvim.appimage
sudo mv nvim.appimage /usr/bin/nvim

sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'

pip install pynvim
```

### build-essential
```
sudo apt install build-essential
```

### node
```
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
sudo apt-get install -y nodejs
```
### gvm + go
```
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)

gvm install go1.4 -B
gvm use go1.4
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.19
```
### lua5.3
```
sudo apt install lua5.3
```

### rg 
```
sudo apt-get install ripgrep
```

### fzf
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

### lazygit
```
go install github.com/jesseduffield/lazygit@latest
```

### lf
```
env CGO_ENABLED=0 go install -ldflags="-s -w" github.com/gokcehan/lf@latest
```
### .tmux 
```
git clone https://github.com/gpakosz/.tmux.git ~/github/tmux
ln ~/github/tmux/.tmux.conf ~/.tmux.conf
```

### z.lua
```
git clone https://github.com/skywind3000/z.lua.git ~/github/z.lua
```

## link settings
```
ln  .p10k.zsh ~/.p10k.zsh
ln  .zshrc ~/.zshrc
ln  .tmux.conf.local ~/.tmux.conf.local
ln  .zprofile ~/.zprofile

md ~/.config/lf
ln lfrc ~/.config/lf/lfrc

ln lfcd ~/.local/bin/lfcd.sh
```

git clone https://github.com/a45s67/nvim-note.git "~/.config/nvim"
