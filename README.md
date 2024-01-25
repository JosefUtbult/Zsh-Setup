# Zsh Setup

Begin with installing the following fonts

- [MesloLGS NF Regular.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf)
- [MesloLGS NF Bold.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf)
- [MesloLGS NF Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf)
- [MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf)

Install ZSH

```bash
sudo apt install zsh
```

Execute ZSH for the first time

```bash
exec zsh
```

Make ZSH your default shell

```bash
chsh -s $(which zsh)
```

## Install oh-my-zsh

Run the following command

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

It will guide you through setup.

Select yes for `Do you want to change your default shell to zsh`

Install two plugins

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Edit your `~/.zshrc` file and find the line `plugin=(git)`. Change it to

```
plugins=(
	git
	zsh-autosuggestions
	zsh-syntax-highlighting
)
```

Then, find the line `ZSH_THEME` and change it to

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Now, try to close and reopen the terminal. It should give you a configuration menu.

Make sure all fonts work, by checking the different symbols in the wizard.

Select the `Rainbow` prompt style.

Select the `Unicode` character set

Skip showing the time

Select the `Angled` separator

Select the `Sharp` head

Select the `Flat` tail

Select the `One line` prompt height

Select the `Sparse` prompt spacing

Select `Many icons` for the icons

Select `Concise` prompt flow

Enable `Transiend prompt`

Select the `Verbose` instant prompt mode

Apply the changes to `~/.zshrc`
