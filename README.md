# react-static_broken_hot_reloading

This example does not `hot-reload` as expected

# FIXED

Add `react-hot-loader/babel` to babel plugins via `.babelrc`

See below for the original problem

# Problem

This example does not `hot-reload` as expected

# What am i doing wrong?

## steps / reproduce

### Install/update react-static

    yarn global add react-static

### Create new app

    react-static create --name react-static-hmr-test --template basic

### Run app

    cd react-static-hmr-test

    yarn run start

## Change stuff

 * Change the text "_Home_" in [src/App.js](src/App.js)
   * This **_IS_** hot reloaded
 * Change the render of [src/containers/Home.js](src/containers/Home.js)
   * This **_IS NOT_** hot reloaded
