# NewVPSInstance
contains tools and files to help u to install a stuff into a new VPS instance


# commands

### fresh ubuntu install (some parts requires user input)

```bash
sudo apt update
sudo apt upgrade
sudo apt install ufw

sudo ufw enable
sudo ufw allow 22

mkdir Documents

sudo apt-get install git
sudo apt-get install htop
echo "done"
```


### install conda ( instructions from [here](https://docs.conda.io/projects/miniconda/en/latest/index.html) )

``` bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh

~/miniconda3/bin/conda init bash
echo "done"
```

### install java (todo)

```bash
mkdir ~/downloads
cd ~/downloads
wget https://github.com/alexpvpmindustry/NewVPSInstance/raw/main/large_files/jdk-16.0.2_linux-x64_bin.tar.gz
tar -xvzf jdk-16.0.2_linux-x64_bin.tar.gz
cd ~/
echo 'export JAVA_HOME="/root/downloads/jdk-16.0.2/"' >> .bashrc
echo 'export PATH=$PATH:$JAVA_HOME/bin' >> .bashrc
source ~/.bashrc
echo "done"
```

- unzip tar.gz,
- add java to javahome
