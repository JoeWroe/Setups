#:notebook: Bower :notebook:

**Bower is a package manager, designed to allow you to add further functionality to your project.**
**Similar to 'npm' or 'ruby gems', files are added to your bower file that add 'dependencies' to your**
**project. In short, the functionality is added through code written elsewhere, your project then**
**requires it (or becomes dependent on it), in order to run. The bower file defines that code and pulls**
**it into your project.**

**Bower manages your _FRONTEND_ dependencies**

---

**To get Bower going, you will need to install node**

**WARNING: Installing node can cause issues if you already have node version manager installed**
**(n, nvm or nodenv). Running any of those three names followed by -v will let you know if its already**
**installed.**

---

```
STEP 1.1: Globally install Bower to your local machine with 'npm install -g bower'

    STEP 1.2: Ensure everything is installed properly with 'node -v' & 'bower -v'.
```

```
STEP 2: In your project (if you don't have one set up yet, add a new directory named after your planned
        project, to do this in, then work your way through the npm walkthrough found in this repo), add a
        dependency to your package.json for bower with 'npm install --save-dev bower'.
```

```
STEP 3: Initialize Bower in your project with 'bower init'. For basic projects, pressing return for each
        of the questions will complete the setup as required for now. This will generate a 'bower.json'
        file that will define the frontend dependencies for your project.
```

```
STEP 4: Adding dependencies is now done in a similar way to npm. For this example, we will use jQuery, so we
        would run 'bower install jquery --save'. See the other files in this repo for what is created, but
        in brief, a folder entitled 'bower_components' is added with the necessary files to include the
        dependency in the project. The '--save' will add the dependency to your 'bower.json', so when your
        repo is cloned in the future, it is possible to see which dependencies have been used.
```

```
STEP 5: Finally, adding your bower_components file to your .gitignore file is good practice and convention.
        This stops you from clogging up a git repo with these files.
```
