#:notebook: Node Package Manager (npm) :notebook:

**npm is a package manager, designed to allow you to add further functionality to your project.**
**Similar to 'ruby gems', files are added to your 'package.json' file that add 'dependencies' to**
**your project. In short, the functionality is added through code written elsewhere, your project**
**then requires it (or becomes dependent on it), in order to run. The npm file defines that code**
**and pulls it into your project.**

**npm manages you BACKEND dependencies**

---

**npm (node package manager), comes as part of your installation of node. Installing node will also**
**install npm for you.**

**WARNING: Installing node if can cause issues if you already have node version manager installed**
**(n, nvm or nodenv). Running any of those three names followed by -v will let you know if its already**
**installed.**

---

```
STEP 1: 'brew install node', (not always necessary, read the warning above!)
```

```
STEP 2: 'npm init', will create a package.json file in your project. This command will run you
        through a number of questions, it is possible to hit enter on all of these questions to
        get your project going quickly. See the package.json file in this folder for an example
        of what it should look like.
```

```
STEP 3: The first bit of understanding for this file is what goes on under the 'scripts' heading,
        this section defines a collection of scripts that can be run with the npm command. Currently
        it should just contain the line:


            "test": "echo \"Error: no test specified\" && exit 1"


        This defines what happens when you run the command 'npm test', run it now and see what it
        outputs.


            > npm-setup@1.0.0 test /Users/Joe/Projects/setups/npm
            > echo "Error: no test specified" && exit 1

            Error: no test specified
            npm ERR! Test failed.  See above for more details.
            npm WARN Local package.json exists, but node_modules missing, did you mean to install?


        As testing is added, this will be updated.
```

```
STEP 4.1: Being a 'package manager', you will need to be able to install packages. To do this,
          find the package you want (hapi has been used in this example), and run 'npm install
          hapi --save'. This tells npm to install the package hapi into your project, save (--save)
          it inside a folder called 'node_modules' and update your package.json file.

    STEP 4.2: If you need to install a package that will only be required by developers of your app
              (and not needed to run the actual application), you can run 'npm install jasmine-node
              --save-dev', this nows becomes a development only package and updates the dependencies
              in the 'package.json' file appropriately.

    STEP 4.3: As a general rule, you can also use 'npm install [a package] -g' in order to install it
              globally on your machine. This will allow you to run it from elsewhere. It's important you
              still use the '--save' or '--save-dev' to make sure it is included in your 'package.json'.
              Other developers cloning your repo will now be able to see the necessary dependancies they
              need.
```

```
STEP 5: Finally, adding your node_modules file to your .gitignore file is good practice and convention.
        This stops you from clogging up a git repo with these files.
```
