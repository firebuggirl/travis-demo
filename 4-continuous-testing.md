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

      `npm run e2e`

### 3 => Run unit tests w/ Headless Chrome

https://blog.angularindepth.com/angular-testing-with-headless-chrome-d1343b349699

- `Run`:

 `npm run test-headless`

- add `npm run test-headless` to  `.travis.yml`

### 4 => Commit/push to Github

  `git commit -am "Added unit for Travis CI using Headless Chrome"`

  `git push`

  - switch to Travis CI Dashboard => watch project run Unit Tests + build
