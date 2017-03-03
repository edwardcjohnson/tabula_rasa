# tabula_rasa
A blank slate or template to initialize data science projects.


#### Python Environment Creation
This is an adaptation of [tdhopper.com's environment workflow](http://tdhopper.com/blog/2015/Nov/24/my-python-environment-workflow-with-conda/)

1. Create a project folder in the ~/work/repos/ directory on my computer.
2. Create an environment.yml file in the directory. 
   * The environment name should be the same as the folder name.
   * At minimum, it will specify the version of Python I want to use; it will often include anaconda as a dependency.
   * If you want to save your current environment instead of creating a new one, enter `conda env export > environment.yml`
3. Create the conda environment with `conda env create -f environment.yml`.
4. Activate the conda environment with `source activate ENV_NAME`.
5. Create a .env file containing the line `source activate ENV_NAME`.
   * autoenv should be installed, so that this file will be run every time I navigate to the project folder in the Terminal.
   * Therefore, my conda environment will be activated as soon as I navigate to the folder.
6. Run `git init` to make the folder a Git repository. 
   * Then run `git add environment.yml` and `git commit -m 'initial commit'` to add the YAML file to the repository.
7. If I want to push the repository to Github, I use `git create` using Github's hub commands.
   * I then push the master branch with `git push -u origin master`.
