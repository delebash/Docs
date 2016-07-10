## How to Debug Webpack loaders in Webstorm ##

[Npm install instructions](https://www.npmjs.com/package/webpack-webstorm-debugger-script)

npm i webpack-webstorm-debugger-script

Usage (version 2):

    npm install webpack-webstorm-debugger-script

### Add run/debug configuration in WebStorm ###

Add new debug configuration(click + button to add new) of type Node.js and Node parameters: ./node_modules/webpack-webstorm-debugger-script

Put you break points in the css-loader index.ts file

Run debug button

## Compile css-load ts files on change ##

First make sure typescript 2.0 is install

    npm install typescript@next

install typings

    typings install

## Use manual tsc compiler ##
open second jetbrains terminal or run in cmder

    tsc --p "F:\Development\GitHub\delebash\Webpack-debug\skeleton-esnext-webpack\node_modules\@easy-webpack\config-sass"
    
src and out put files are set in tsconfig.json so all you need to do for running tsc is point to the root folder were tsconfig.json is located by using the  --p parameter


## Doesn't work ##
In Webstorm typescript settings set to Typescript version to custom and navigate to your npm global typescript lib folder

    C:\Users\Daniel\AppData\Roaming\npm\node_modules\typescript\lib

Add custom scope for the css-loader folder in you npm directory
Slider scroll bar over until you see elipse for Scope:

Click on the blue show included button or you will not see any folders listed. Navigate to your css-loader folder under node_modules and select.  Name your scope css-loader. Save

This loader should now be set for your Scope: option