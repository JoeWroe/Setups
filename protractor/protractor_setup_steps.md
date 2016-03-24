#:notebook: Protractor :notebook:

**Protractor is an 'End 2 End' testing (Feature testing) tool for use with AngularJS**
**To begin with Protractor, you will need 'Node' and the 'Node Package Manager' installed on your system.**
**If they are not already, head to the 'npm' walkthrough found in this repo.**

```
STEP 1: Run 'npm install protractor -g'.
```

**You will also need Selenium installed on your system. Protractor install comes with Selenium so...**

```
STEP 2: Run 'webdriver-manager update', you will see the Selenium Standalone Server is now installed on your system
        as well as the Chromedriver.
```

```
STEP 3: Run 'npm init' to setup your package.json (Protractor is testing Angular, so is Frontend), then run 'npm
        install protractor --save' to add your required node modules.
```

```
STEP 4.1: Add a 'test' folder, and 'e2e' folder and a 'protractor.config.js' file to your project tree.

    STEP 4.2: Inside 'protractor.config.js' ad the following:

        exports.config = {

          specs: [
            './e2e/**/*.spec.js'
          ],

          baseUrl: 'http://localhost:3333'
        };

    This tells protractor two things. Under the specs, it says where to find the tests and the baseUrl will be
    the url to look at for the page that will be tested.

    STEP 4.3: With Protractor configured, we can now run Protractor from the command line with 'protractor
              test/protractor.conf.js'. Obviously running this will throw an error since we have no tests written!
