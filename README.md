# GettingStarted
Resources to get started with research in our group

## Creating a GitHub Account
Our group uses GitHub to share code, documentation, and for version control. If you do not already have an account, you should create one. 

1. Create a GitHub account.
2. Request a [PRO account](https://education.github.com/discount_requests/application) for students, which will allow you to have private repositories.
3. Let us know your username so we can add you to the **LagrangianOceanLab** team.
4. Together, we will identify or create a private repository best suited for your work.

## Working on the Jupyter Hub
Our group works on a shared Jupyter Hub for data visualization and analyses that do not require HPC resources. To better help each other, share data and model output, and facilitate project transitions, our team works out of a shared directory (`./hpc/lol_scratch/`). By default, only members of the `lol_group` can access the files in this directory, but you can change permissions as needed. 
1. Access the Jupyter Hub at `https://jupyter.ceoas.oregonstate.edu/`, and log in with your OSU credentials.
2. Set up your [GitHub SSH keys] (https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) on the server. Your SSH keys should be saved in a subdirectory (typically `./.ssh/`) of your home folder, so that they remain private and not accessible to members of our group.
3. Navigate to our group's directory `./hpc/lol_scratch/` and create a directory with your name or onid.
4. Clone the relevant GitHub project repository for your work under your new directory.

**Important:** `./hpc/lol_scratch/` is not backed up, so you should regularly push your work to GitHub.

## Setting up you project GitHub repository
In general, we limit the files we upload to GitHub to code, text documentation, and figures to include in our documentation. To avoid having to select which files we push individually every time, it is good practice to include a `.gitignore` file in each of our project repositories. A sample `.gitignore` file is included [!!! add link!!!]

