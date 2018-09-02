# lerna-playground

learn [lerna](https://lernajs.io/) *A tool for managing JavaScript projects with multiple packages*

## Prerequisites

install lerna 
`npm install --global lerna`

## Example Workflow

```sh
# init lerna repo
mkdir lerna-playground
cd lerna-playground
git init
lerna init

# create mathlib
cd packages
mkdir mathlib
cd mathlib
npm init -f
touch index.js # write mathlib code

# create client that depends on mathlib
cd ..
mkdir client
cd client
npm init -f

# add mathlib
lerna add mathlib

# create client code
touch index.js

# run client
node index.js
```