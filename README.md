# GettingStarted
Resources to get started with research in our group

## Creating a GitHub Account
Our group uses GitHub to share code, documentation, and for version control. If you do not already have an account, you should create one. If you want to refine your git skills, the OSU library offers git workshops, and the Ecampus Career Hub s a link to a thorough [video introductions](https://careers.ecampus.oregonstate.edu/classes/learning-github/).

1. Create a GitHub account.
2. Request a [PRO account](https://education.github.com/discount_requests/application) for students, which will allow you to have private repositories.
3. Let us know your username so we can add you to the **LagrangianOceanLab** team.
4. Together, we will identify or create a private repository best suited for your work.

## Working on the Jupyter Hub
Our group works on a shared Jupyter Hub for data visualization and analyses that do not require HPC resources. To better help each other, share data and model output, and facilitate project transitions, our team works out of a shared directory (`./hpc/lol_scratch/`). By default, only members of the `lol_group` can access the files in this directory, but you can change permissions as needed. 
1. Access the Jupyter Hub at `https://jupyter.ceoas.oregonstate.edu/`, and log in with your OSU credentials.
2. Set up your [GitHub SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) on the server. Your SSH keys should be saved in a subdirectory (typically `./.ssh/`) of your home folder, so that they remain private and not accessible to members of our group.
3. Navigate to our group's directory `./hpc/lol_scratch/` and create a directory with your name or onid.
4. Clone the relevant GitHub project repository for your work under your new directory.

**Important:** `./hpc/lol_scratch/` is not backed up, so you should regularly push your work to GitHub.

## Setting up your project GitHub repository
In general, we limit the files we upload to GitHub to code, text documentation, and figures to include in our documentation. To avoid having to select which files we push individually every time, it is good practice to include a `.gitignore` file in each of our project repositories. A `.gitignore` file with several examples of file that could be ignored is [included in this repository](https://github.com/LagrangianOceanLab/GettingStarted/blob/main/.gitignore).

## Using conda
#### 1. Install [Miniconda](https://docs.conda.io/projects/miniconda/en/latest/miniconda-install.html). 
Installing Miniconda is preferable to installing Anaconda because its packages include only conda and Python, which limits the storage it requires. Instead, users install only the package they need. 

#### 2. Create a conda environment for your project
One of the advantages of conda is that you can [create conda environments](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands), which keeps modules for different projects separate, avoiding potential conflicts. It is also possible for people to recreate someone else's conda environment, ensuring reproducibility. I like to have an environment named `sandbox` for data exploration, etc. It is completely fine if that environment breaks.

From now on, when you want to work on a project or install python modules, activate the conda environment you created:

```
conda activate nameoftheenvironment
```

## Installing Jupyter Lab and other Python modules locally
Once you have conda installed, open Terminal, activate the relevant conda environment (if applicable) and [install Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html):

```
conda install -c conda-forge jupyterlab
```

Using the same command, you can install Python modules commonly used in oceanography: 
- `xarray`
- `cartopy`
- `numpy`
- `pandas`
- `scipy` 
- `matplotlib`

## Setting up your computer for easily accessing servers
To easily access a remote server, you can set up `ssh-keys` on your local computer. It is best practice to create a new set of keys for each computer/server combination, so that you can easily deactivate a key if it becomes compromised. The instructions on [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server) and [GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) are two great resources for creating `ssh-keys`. 

Note that you should use the ed25519 signature system rather than the rsa system mentioned on DigitalOcean, and use an informative filename when saving them (e.g., I include the name of the server):

```
ssh-keygen -t ed25519
```

## Download useful tools
### Visual Studio Code
[VSCode](https://code.visualstudio.com/) is a versatile code editor. For instance, it offers markdown previews to help edit this `README.md` on your local computer. On a Mac, pressing `command + k` followed by pressing `v` will open a side-by-side markdown preview.

### iTerm2
iTerm2 is highly customizable Terminal application. One of my favorite features is to create profiles for each server that I access, which allows me to easily know *where* I am in a Terminal window. I detailed how to setup profiles across platform in the [scientific-workflow repository](https://github.com/jessecusack/scientific-workflow/blob/main/macOS_setup.md#step-4---customize-iterm2) maintained by Jesse Cusack.