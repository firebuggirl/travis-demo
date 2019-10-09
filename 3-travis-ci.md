# Travis CI

- Register w/ Travis CI using your GitHub account

- find `travis-demo` in list of repos => activate sync capabilities

## Add Travis CI Configuration

- in `./` create `.travis.yml`

  - `--base-ref` => use my GitHub id

  - tells Travis CI:

    - use Node.js

    - Only watch the master branch for changes

    - Before running any of the scripts install Angular CLI

    - Make sure the app passes linting rules w/ ng lint

    - Build app => ng build


  ` git add .travis.yml `

  ` git commit -am "Travis CI configuration" `

  ` git push origin master `

  - watch the Travis CI log via dashboard as it builds app

  - fails => Travis CI using wrong version of Node.js => forgot to update node version .travis.yml file

  - icon in dashboard turns green when script has completed successfully


## Continuous Testing

- have Travis CI run Unit Tests whenever we push a new commit

### 1 => Steps for setting up Headless Chrome for Unit Testing

https://blog.angularindepth.com/angular-testing-with-headless-chrome-d1343b349699

- `Headless Chrome` => tool for running automated tests in environments where it isn’t practical to actually launch a browser

- configure Angular CLI to run Unit and E2E Tests using Headless Chrome

- Angular CLI adds karma-chrome-launcher by default via package.json => don’t need to install anything


### 2 => `Unit Tests`:

https://blog.angularindepth.com/angular-testing-with-headless-chrome-d1343b349699

  - configure a `new npm script` to run our unit tests `only once` using Headless Chrome and then exit

  - `package.json` => add `test-headless` script

  - `Run`:

    ` npm run test-headless `

- `E2E Tests`:

  - configure E2E tests to run using Headless Chrome

  - leverage the `Protractor configuration file` => via `e2e/protractor.conf.js`:

    - `modify the capabilities entry` in our protractor.conf.js file to `include a chromeOptions object`

    - Run:

      ` npm run e2e `

### 3 => Run unit tests w/ Headless Chrome

https://blog.angularindepth.com/angular-testing-with-headless-chrome-d1343b349699

- `Run`:

 ` npm run test-headless `

- add `npm run test-headless` to  `.travis.yml` 
