Step 1: Ensure Node and Bower are installed with 'node -v' & 'bower -v'
  Step 1.1: If they're not 'brew install node' & 'npm install -g bower', see the other setup walkthroughs in this repo for more info
            on these

Step 2: Make a new directory.
  Step 2.1: Run 'bower init' in the new directory to initialize Bower
  Step 2.2: Choosing defaults for each of the options works fine.

Step 3: Install your most basic packages (add them to your bower.json file):
  Step 3.1: 'bower install jquery --save', installs jquery for dynamic page changes.
  Step 3.2: 'bower install bootstrap --save', installs bootstrap for page styling.
  Step 3.3: 'bower install angular --save', installs angular in your project for the frontend framework.
  Step 3.4: 'bower install angular-resource --save', allows for the ability for angular to interact with RESTful server-side data
    N.B: The --save is simply saving to your bower.json file

Step 4: Add a .gitignore file
  Step 4.1: Add 'bower_componants' to the file.

Step 5: Add a HTML file to the project tree (convetion says it should be named 'views/index.html').

Step 6: Create the Angular module
  Step 6.1: Create a new file 'js/app.js'
  Step 6.2: In the new file, create a new application with 'var variableName = angular.module('applicationName', []);'
  Step 6.3: Include ngResource in the empty array, this pulls in 'angular-resource' from the bower.json file and allows for interaction
            with RESTful resources (HTTPS).
  Step 6.4: Include the app.js file a a source file in your html file with '<script src="js/app.js"></script>'.
  Step 6.5: Finally wire up the HTML file with the Angular app. This is done by adding to the end of the html opening tag <html lang="en"
            ng-app="GitUserSearch">

Step 7: Setting up the test environment
  Step 7.1: Boilerplate with 'bower install angular-mocks --save-dev' & 'bower install angular-route --save-dev'.
  Step 7.2: Setup package.json for your node packages with 'npm init', you can press return on each argument to default it.
  Step 7.3: Add 'node_modules to .gitignore'.
  Step 7.4: Install necessary Node packages with 'npm install Karma --save-dev', 'npm install karma-jasmine karma-chrome-launcher
            karma-phantomjs-launcher --save-dev', 'npm install jasmine-core phantomjs phantomjs-prebuilt --save-dev' & 'npm install
            -g karma-cli'. This adds the dependancies for the karma test suite to your package.json file.
  Step 7.5: Run either 'karma init' and answer the questions, or copy and paste the 'karma.config.js' file in this folder. This
            configures your karma.
  Step 7.6: Fire up your tests with 'karma start test/karma.conf.js' (Note: this will fail if you've not written any tests!).

Step 8: Writting your first test
  Step 8.1: Create a 'test' folder.
  Step 8.2: Add a file 'nameOfController.spec.js' to the folder.
  Step 8.3.1: Setup and add your first test.
    Step 8.3.2: See the example 'gitUserSearchController.spec.js' in this folder for a basic test setup.
