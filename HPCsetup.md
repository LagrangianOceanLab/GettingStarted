# HPC Setup

These instructions were modified from [Jesse Cusack's scientific-workflow](https://github.com/jessecusack/scientific-workflow/blob/main/HPC_clusters.md).

## Setting up ssh keys

To make logging on easier, it can be useful to [set up ssh keys on the server](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-2). Best practice is to have a unique ssh key for each combination of local computer and server, so that they can be easily deactivated if computers or access are lost.

## Installing Miniconda on the server

Log into the HPC cluster. To download Miniconda, run:

```bash
cd ~
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

To install Miniconda, run:

```bash
bash Miniconda3-latest-Linux-x86_64.sh
```

And follow the prompts to install it in your home directory (this usually just means following the default options).

As part of the installation, you may be asked for permission to modify your terminal configuration (the `.bashrc` file that lives in your home directory). This is recommended, so that every time you log into the HPC, you will have access to the `conda` commands automatically.

Upon successful installation, I would recommend setting `conda-forge` as the default channel package searches. I find that it has a more complete list of packages than the standard conda channel. To do so, run the following in the terminal:

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

## Working with Jupyter Lab
[Add instructions after testing them.]