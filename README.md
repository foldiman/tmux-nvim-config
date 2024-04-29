Instructions: 

From a fresh install of Ubuntu:

sudo apt update
sudo apt install build-essential
sudo apt install tmux
sudo apt install neovim
sudo apt install fd-find
sudo apt-get install ripgrep
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/JetBrainsMono.zip
unzip JetBrainsMono.zip
sudo mkdir ~/.fonts
sudo mv *.ttf ~/.fonts
rm JetBrainsMono.zip
fc-cache -fv
git clone https://github.com/foldiman/tmux-nvim-config ~/.config && nvim
(Type ":MasonInstallAll" and hit enter) to install nvim plugins
(Type "Lazy sync" and hit enter) to sync nvim plugins
(Type "TSInstallInfo" and hit enter) to see availible treesitter libraries
(Type "TSInstall <langA> <langB> .." and hit enter) to install desired libraries 
(Exit neovim)
alias vim=nvim
echo 'alias vim=nvim' >> .zshrc
nvim source ~/.config/tmux/tmux.conf
(Type <<leader> + I>) to install tmux plugins
