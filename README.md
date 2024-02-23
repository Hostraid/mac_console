Настройка терминала на MacOS
=========

# Установка Homebrew
- [документация](https://brew.sh/)

        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Установка терминала Warp.dev
- [документация](https://docs.warp.dev/getting-started/readme)
- [оф.сайт](https://www.warp.dev/)

        brew install --cask warp

# Установка шрифтов

        brew tap homebrew/cask-fonts
        brew install --cask font-hack-nerd-font
        brew install --cask font-meslo-lg-nerd-font

- полный список NERD шрифтов

        brew install --cask font-3270-nerd-font
        brew install --cask font-fira-mono-nerd-font
        brew install --cask font-inconsolata-go-nerd-font
        brew install --cask font-inconsolata-lgc-nerd-font
        brew install --cask font-inconsolata-nerd-font
        brew install --cask font-monofur-nerd-font
        brew install --cask font-overpass-nerd-font
        brew install --cask font-ubuntu-mono-nerd-font
        brew install --cask font-agave-nerd-font
        brew install --cask font-arimo-nerd-font
        brew install --cask font-anonymice-nerd-font
        brew install --cask font-aurulent-sans-mono-nerd-font
        brew install --cask font-bigblue-terminal-nerd-font
        brew install --cask font-bitstream-vera-sans-mono-nerd-font
        brew install --cask font-blex-mono-nerd-font
        brew install --cask font-caskaydia-cove-nerd-font
        brew install --cask font-code-new-roman-nerd-font
        brew install --cask font-cousine-nerd-font
        brew install --cask font-daddy-time-mono-nerd-font
        brew install --cask font-dejavu-sans-mono-nerd-font
        brew install --cask font-droid-sans-mono-nerd-font
        brew install --cask font-fantasque-sans-mono-nerd-font
        brew install --cask font-fira-code-nerd-font
        brew install --cask font-go-mono-nerd-font
        brew install --cask font-gohufont-nerd-font
        brew install --cask font-hack-nerd-font
        brew install --cask font-hasklug-nerd-font
        brew install --cask font-heavy-data-nerd-font
        brew install --cask font-hurmit-nerd-font
        brew install --cask font-im-writing-nerd-font
        brew install --cask font-iosevka-nerd-font
        brew install --cask font-jetbrains-mono-nerd-font
        brew install --cask font-lekton-nerd-font
        brew install --cask font-liberation-nerd-font
        brew install --cask font-meslo-lg-nerd-font
        brew install --cask font-monoid-nerd-font
        brew install --cask font-mononoki-nerd-font
        brew install --cask font-mplus-nerd-font
        brew install --cask font-noto-nerd-font
        brew install --cask font-open-dyslexic-nerd-font
        brew install --cask font-profont-nerd-font
        brew install --cask font-proggy-clean-tt-nerd-font
        brew install --cask font-roboto-mono-nerd-font
        brew install --cask font-sauce-code-pro-nerd-font
        brew install --cask font-shure-tech-mono-nerd-font
        brew install --cask font-space-mono-nerd-font
        brew install --cask font-terminess-ttf-nerd-font
        brew install --cask font-tinos-nerd-font
        brew install --cask font-ubuntu-nerd-font
        brew install --cask font-victor-mono-nerd-font

# Установка GIT
        brew install git

# Установка Oh My Zsh
- [документация](https://ohmyz.sh/)

        sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Установка темы PowerLevel10K Theme for Oh My Zsh
- [документация](https://github.com/romkatv/powerlevel10k)  

        git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
        sed -i '' 's/ZSH_THEME=.*/ZSH_THEME="powerlevel10k\/powerlevel10k"/' ~/.zshrc
        source ~/.zshrc

# Настройка темы

        p10k configure

# Изменить шрифт в VSCode и Warp.dev
- открыть settings.json (COMMAND+SHIFT+P) в VSCode
  
        "terminal.integrated.fontFamily": "MesloLGS NF"

- поменять шрифт в настройках Warp.dev - Appearence - Text
- выбрать тему в настройках Warp.dev - Appearence - Current Promt (Shell Promt1)

# Установка плагинов ZSH
- по умолчанию Warp уже их содержит (нужны для родной консоли MacOS)

        git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
        git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

- добавить в ~/.zshrc

        plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search)
        source ~/.zshrc

# Настройка консоли через StarShip
- [темы](https://starship.rs/presets/#nerd-font-symbols)  
  
        curl -sS https://starship.rs/install.sh | sh
        echo 'eval "$(starship init zsh)"' >> ~/.zshrc
        mkdir -p ~/.config && touch ~/.config/starship.toml
        nano ~/.config/starship.toml

# Создание темы Warp Coolnight
        mkdir -p ~/.warp/themes/
        nano ~/.warp/themes/coolnight.yaml

        accent: "#38ff9c"
        background: "#010b17"
        foreground: "#ebddf4"
        details: "darker"
        terminal_colors:
        normal:
            black: "#0b3b61"
            red: "#ff3a3a"
            green: "#52ffcf"
            yellow: "#fff383"
            blue: "#1376f8"
            magenta: "#c792ea"
            cyan: "#ff5dd4"
            white: "#15fca2"
        bright:
            black: "#62686c"
            red: "#ff54b0"
            green: "#73ffd8"
            yellow: "#fcf4ad"
            blue: "#378dfe"
            magenta: "#ae81ff"
            cyan: "#ff69d7"
            white: "#5ffbbe"


