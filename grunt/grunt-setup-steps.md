#:notebook: Grunt :notebook:

**Grunt is a task runner, this means it automates a lot of the repetitive processes you may do.**

```
STEP 1: Install Grunt's command line tools globally with 'npm install -g grunt-cli'.
```

```
STEP 2: Install Grunt locally in your project with 'npm install --save-dev grunt'. This will add the
        necessary sheets of external code for grunt into your project in a file called 'node_modules'.
```

```
STEP 3: Setup 'Gruntfile', this will be where you define the tasks you wish Grunt to run. To do this,
        simply add a fille to your project root called 'Gruntfile.js'.
```

```
STEP 4: Now, we need to add a function to the Gruntfile that will tell Grunt what you would like run.
        For this example, we will use jsHint, See the Gruntfile in this repo for a completed example,
        or work through the following steps.

    STEP 4.1: setup the module with:

              'module.exports = function(grunt) {};'

    STEP 4.2: Add an 'initConfig' function with:

              grunt.initConfig({});

    STEP 4.3: Add the task you'd like to run to the function:

              (inside the init config)
              jshint: {
                all: ['Gruntfile.js', 'src/**/*.js', 'spec/**']
              }

    STEP 4.4: Add two further function to the end of the file to make sure it runs ok.

              grunt.loadNpmTasks('grunt-contrib-jshint');

              grunt.registerTask('default', ['jshint']);
              
