# NewVPSInstance
contains tools and files to help u to install a stuff into a new VPS instance


# commands

### fresh ubuntu install

```bash
sudo apt update
sudo apt upgrade
sudo apt install ufw

sudo ufw enable
sudo ufw allow 22
```


### install conda from [here](https://docs.conda.io/projects/miniconda/en/latest/index.html)

``` bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```
