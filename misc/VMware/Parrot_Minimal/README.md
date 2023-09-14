- #### Installing VMware Tools
> 1. Mount the Disk:
> 
> https://github.com/Azathothas/Arsenal/assets/58171889/33506985-7bc6-4463-9640-5ef348356358
>
> 2. Open Terminal
> ```bash
> !# Copy the tar to /tmp
> sudo cp "$(find -type f -name '*.gz')" /tmp/
> !# Extract
> cd /tmp && tar -xvf "$(find -type f -name '*.gz')"
> !# Install
> cd "/tmp/vmware-tools-distrib" && sudo "./vmware-install.pl" --default
> !# Restart the VM
> ```
---
- #### Setup
> - **Passwordless**
> ```bash
> echo -e "$USER ALL=(ALL) NOPASSWD:ALL" | sudo tee -a /etc/sudoers
> sudo apt-get update -y
> ```
> - **CoreUtils**
> ```bash
> sudo apt-get update -y ; sudo apt-get dist-upgrade -y ; sudo apt-get upgrade -y
> !# May need to run this Twice
> sudo apt install autoconf automake autopoint binutils bison build-essential ca-certificates coreutils curl dos2unix git gcc htop flex file jq moreutils wget -y
> ```
> - **Grub**
> ```bash
>  sudo sed -i 's/GRUB_TIMEOUT=5/GRUB_TIMEOUT=0/' "/etc/default/grub"
> !#Reboot
>  sudo update-grub ; reboot 
> ```
---
- #### Install Addons & Utils
- ##### [**Static-Bins**](https://github.com/Azathothas/Toolpacks) (Essential)
> ```bash
> sudo curl -qfsSL "https://raw.githubusercontent.com/Azathothas/Toolpacks/main/x86_64/eget" -o "/usr/local/bin/eget" && sudo chmod +xwr "/usr/local/bin/eget"
> sudo eget "Azathothas/Toolpacks" --asset "toolpack_x86_64.tar.bz2" --all --to "/usr/local/bin" && sudo chmod +xwr /usr/local/bin/*
> !# You may need to Remove | Symlink Certain things
> !# Example: sudo rm "/usr/local/bin/git" # (As git doesn't work)
> !# Reinstall git from apt: sudo apt-get install git
> ```
 - ##### [Python (**MiniConda**)](https://docs.conda.io/projects/miniconda/en/latest/) (Essential)
> ```bash
> curl -qfSL "https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh" -o /tmp/install_conda.sh && chmod +xwr "/tmp/install_conda.sh" && /tmp/install_conda.sh -b
> !# Check pip
> export PATH="$HOME/miniconda3/bin:$HOME/miniconda3/condabin:$PATH"
> pip install archey4 ; archey
> !# Edit your $HOME/.bashrc | $HOME/.zshrc and add:
> export PATH="$HOME/miniconda3/bin:$HOME/miniconda3/condabin:$PATH"
> ```
- ##### Install [**Crystal**](https://crystal-lang.org/install/on_ubuntu/) (Optional)
> ```bash
>  curl -qfsSL "https://crystal-lang.org/install.sh" | sudo bash
> ```
- ##### Install [**Golang**](https://github.com/kerolloz/go-installer) (Optional)
> ```bash
> !# Install
>  bash <(curl -qfsSL "https://git.io/go-installer")
> !# Delete Junk
>  rm $HOME/go*.gz
> !# Export PATH (Or simply relogin)
>  export PATH=$HOME/.go/bin:$PATH
>  export PATH=$HOME/go/bin:$PATH
> ```
- ##### Install [**Rust**](https://www.rust-lang.org/tools/install) (Optional)
> ```bash
> !# Install
>  bash <(curl -qfsSL "https://sh.rustup.rs") -y 
> !# Export PATH (Or simply relogin)
>  export PATH=$HOME/.cargo/bin:$PATH
>  export PATH=$HOME/.cargo/env:$PATH
> ```
- ##### Install [**Ziglang**](https://ziglang.org/learn/getting-started/) (Optional)
> ```bash
> !# Install
>  pushd "$(mktemp -d)" && curl -qfSLJO $(curl -qfsSL "https://ziglang.org/download/index.json" | jq -r '.master | ."x86_64-linux".tarball')
>  find . -type f -name '*.tar*' -exec tar -xvf {} \; && sudo mkdir -p "/usr/local/zig" && sudo mv "$(find . -maxdepth 1 -type d | grep -v '^.$')"/* "/usr/local/zig" ; popd
>  !# Add this to $HOME/.bashrc | $HOME/.zshrc
>  export PATH="/usr/local/zig:/usr/local/zig/lib:/usr/local/zig/lib/include:$PATH"
> ```
---
> ```bash
> !# Final PATH in $HOME/.bashrc || $HOME/.zshrc
> #PATHS (Only Required)
> export GOROOT="$HOME/.go"
> export GOPATH="$HOME/go"
> export PATH="$HOME/bin:$HOME/.cargo/bin:$HOME/.cargo/env:$GOROOT/bin:$GOPATH/bin:$HOME/miniconda3/bin:$HOME/miniconda3/condabin:/usr/local/zig:/usr/local/zig/lib:/usr/local/zig/lib/include:$PATH"
> ```
---
- #### **NerdFonts** & **QOL**
> ```bash
>  !# Fonts
>  pushd "$(mktemp -d)" && eget "ryanoasis/nerd-fonts" --asset "CascadiaCode.zip" --to "CascadiaCode.zip" --download-only
>  unzip -o "CascadiaCode.zip" -d "$HOME/.fonts" && fc-cache -f -v ; sudo unzip -o "CascadiaCode.zip" -d "/usr/local/share/fonts" && sudo fc-cache -f -v ; popd
>
>  !# Colors
>  bash -c "$(wget -qO- https://git.io/vQgMr)"
>  #Profile name: Ayu Dark
>  # bg: #282C34
>  #Profile name: Dracula
>  #bg: Solid Color
>  #Monospace Regular 12
> ```
---