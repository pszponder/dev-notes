# Oh My ZSH

## Themes
zsh-multiline
https://github.com/jan-auer/zsh-multiline

### Powerline
When installing Powerline fonts, use the following commands in command line:
```
git clone https://github.com/powerline/fonts.git # Clone the github repo
cd fonts    # Change to the cloned repos directory
./install.sh    # Run the install script
sudo fc-cache -fv    # Refresh the font cache, saves logging out and back in

```

Then make sure to enable the powerline specific fonts (such as "Fira Mono for Powerline" {may need to install}) under the linux settings for fonts

Need to also enable Fira Mono for Powerline seperately in VSCode so that everything shows up correctly in the VSCode terminal

In the Linux Terminal, make sure to remove the check on Custom Font cehckbox under Preferences of the Gnome Terminal app

### Fira Code
If you want to use Fira Code, make sure to download the powerline compatable font so that you can use powerline correctly

## Plugins
autojump
autocomplete
syntax highlighting