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

  - fails => Travis CI using wrong version of Node.js
