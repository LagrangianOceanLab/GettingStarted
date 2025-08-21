# HPC Setup

These instructions were modified from [Jesse Cusack's scientific-workflow](https://github.com/jessecusack/scientific-workflow/blob/main/HPC_clusters.md).

## Quick access to the server
To more quickly access the server, you can set up [ssh keys on your local machine, add login credentials to your config file, and create profiles in iTerm2 with different colors and shortcuts](https://github.com/LagrangianOceanLab/GettingStarted/tree/main?tab=readme-ov-file#setting-up-your-computer-for-easily-accessing-servers). 

## Working with GitHub on the server
To clone your project repository on the server, you will need to create an `ssh-key` on the server, following the [instruction on GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux). Make sure to select the `Linux` tab.

## Installing Miniconda on the server

Log into the HPC cluster. To download Miniconda, run:

```
cd ~
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

To install Miniconda, run:

```
bash Miniconda3-latest-Linux-x86_64.sh
```

And follow the prompts to install it in your home directory (this usually just means following the default options).

As part of the installation, you may be asked for permission to modify your terminal configuration (the `.bashrc` file that lives in your home directory). This is recommended, so that every time you log into the HPC, you will have access to the `conda` commands automatically.

Upon successful installation, I would recommend setting `conda-forge` as the default channel package searches. I find that it has a more complete list of packages than the standard conda channel. To do so, run the following in the terminal:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

If the `conda` command is not recognized when you try to use it, you might have to add the path to `~/miniconda3/bin/` to your `.bashrc` file.

1. Open `~/.bashrc` with your preferred editor. Note that the example uses `vi`.

```
vi ~/.bashrc
```

2. Add the path to your `miniconda3/bin` folder to your `.bashrc` by including the following line (replace `/path/to/miniconda3/bin` with the actual path, perhaps `~/miniconda3/bin`):

```
export PATH="/path/to/miniconda3/bin:$PATH"
```

3. Source the configuration or restart your Terminal session:

```
source ~/.bashrc
```

## Working with Jupyter Lab
[Add instructions after testing them.]