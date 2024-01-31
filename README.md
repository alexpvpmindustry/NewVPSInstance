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
sudo ufw allow 873

mkdir Documents

sudo apt-get install git
sudo apt-get install htop
sudo apt-get install screen
sudo apt-get install rsync
echo "done"
```

### install crontab to start servers on startup/reboot

put this file in the Documents folder `start_all.sh`
``` bash
#!/bin/bash 
cd /root/Documents/surv_eu/
./screen_server_start.sh
```

`chmod +x start_all.sh`

add this to `crontab -e`

`@reboot /root/Documents/start_all.sh`

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
ln -s /root/downloads/jdk-16.0.2/bin/java /usr/bin/java
cd ~/
echo 'export JAVA_HOME="/root/downloads/jdk-16.0.2"' >> .bashrc
echo 'export PATH=$PATH:$JAVA_HOME/bin' >> .bashrc
source ~/.bashrc
echo "done"
```

- unzip tar.gz,
- add java to javahome
