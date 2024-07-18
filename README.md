Add as a first buildpack in the chain. Make sure you have `yarn socket` and `yarn migrate` command in package.json.

# How to use:
1. `heroku buildpacks:clear` if necessary
2. `heroku buildpacks:set https://github.com/timanovsky/subdir-heroku-buildpack`
3. `heroku buildpacks:add heroku/nodejs` or whatever buildpack you need for your application
4. Deploy your project to Heroku.

# How it works
The buildpack overwrites procfile with
```
web: yarn socket
release: yarn migrate
```
