
Font  list

``` bash
fc-list
```



This method downloads a specific font (e.g., _JetBrainsMono_) directly into your user's local font directory without needing root permissions

Create the fonts directory
``` bash
mkdir -p ~/.local/share/fonts
```

**Download and extract the font**:  
Change `JetBrainsMono.zip` in the command below if you prefer a different font from the Nerd Fonts Releases page.
``` shell
wget -P ~/.local/share/fonts https://raw.githubusercontent.com/JetBrains/JetBrainsMono/master/fonts/ttf/JetBrainsMono-Regular.ttf
cd ~/.local/share/fonts && unzip JetBrainsMono.zip && rm JetBrainsMono.zip
```

**Update your system font cache**:
``` bash
fc-cache -f -v
```

Install Firacode
``` bash
mkdir -p ~/.local/share/fonts && cd ~/.local/share/fonts && \
wget https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FiraCode.zip && \
unzip FiraCode.zip && rm FiraCode.zip && fc-cache -fv
```
