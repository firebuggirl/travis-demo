# Continuous Integration

https://blog.angularindepth.com/the-angular-devops-series-ct-ci-with-travis-ci-and-github-pages-3c02664f078


## Deploy

  - create a GitHub Personal Access Token

  https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line?source=post_page-----3c02664f078----------------------

  - `Using a token` on the command line:

  ` git clone https://github.com/username/repo.git Username: your_usernamePassword: your_token `


  - In `Travis CI Dashboard` go to your project => top right click on `More options : Settings` => Scroll down to `Environment Variables`

    - Add new env variable + value of token:

      ` GITHUB_TOKEN `

## Deploying to GitHub Pages

  - set up Travis CI to `deploy to GitHub Pages`

  - `Add a deploy section` to `.travis.yml`

    - tells Travis CI to use Env Var =>
      `$GITHUB_TOKEN`

    - specifies files to deploy come from dist folder => `dist/travis-demo`

### Commit and push to GitHub

  ` git commit -am "Deploy to GitHub pages" `

  ` git push origin master `


  - URL => https://github.com/firebuggirl/travis-demo
