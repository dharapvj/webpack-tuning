# webpack-tuning

> A Vue.js project (using webpack template) customized to showcase various tuning opportunities.

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production and view the bundle analyzer report
npm run build --report
```

## See the differences in webpack bundles

After cloning the repo, checkout the un-tuned version

    git checkout unoptimized
    # run the app & check network tab for file sizes
    npm run dev 
    # build the report
    npm run build --report

Then checkout the tuned version

    git checkout optimized
    # run the app & check network tab for file sizes
    npm run dev 
    # build the report
    npm run build --report
