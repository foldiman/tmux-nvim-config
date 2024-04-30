Instructions:

_Update package registry_
sudo apt update

_Install dependencies and tools_
sudo apt install git
sudo apt install build-essential
sudo apt install unzip
sudo apt install fd-find
sudo apt-get install ripgrep

_Install tmux_
sudo apt install tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

_Install rust_
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

_Install Neovim_
sudo apt install neovim

_Install JetBrains NerdFont_
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/JetBrainsMono.zip
unzip JetBrainsMono.zip
sudo mkdir ~/.fonts
sudo mv *.ttf ~/.fonts
rm JetBrainsMono.zip
fc-cache -fv

_Install nvchad and tmux profile_

(Type ":MasonInstallAll" and hit enter) to install nvim plugins
(Type "Lazy sync" and hit enter) to sync nvim plugins
(Type "TSInstallInfo" and hit enter) to see availible treesitter libraries
(Type "TSInstall <langA> <langB> .." and hit enter) to install desired libraries 
(Exit neovim)
echo 'alias vim=nvim' >> .zshrc
nvim source ~/.config/tmux/tmux.conf
(Type <<leader> + I>) to install tmux plugins

If using WSL, its recommended to install Hyper for the shell. To do so:
git clone --filter=blob:none --sparse git@github.com:ryanoasis/nerd-fonts
cd nerd-fonts
install FiraCode
(Install Hyper) and modify the following preferences:
  fontSize: 18,
  fontFamily: '"JetBrainsMono NFM", Consolas, Menlo, "DejaVu Sans Mono", "Lucida Console", monospace',
  backgroundColor: '#052633',
  shell: 'C:\\Windows\\System32\\wsl.exe',
  shellArgs: ['-d', 'Ubuntu-24.04'], (Obviously replace Ubuntu-24.04 with your distribution)
