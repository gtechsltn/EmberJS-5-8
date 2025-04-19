# Ember.js 5.8
* Ember is an open-source JavaScript web framework for building modern web applications.
* [LTS](https://emberjs.com/releases/lts/) 
* [Node.js](https://github.com/ember-cli/ember-cli/blob/master/docs/node-support.md)
* [NVM](https://github.com/coreybutler/nvm-windows)
* [Ember.js](https://endoflife.date/emberjs)

```
C:\Users\ADMIN>D:
D:\>md D:\gtechsltn\EmberJS-5-8
D:\>cd D:\gtechsltn
D:\gtechsltn>git clone https://github.com/gtechsltn/EmberJS-5-8
D:\gtechsltn>cd EmberJS-5-8
D:\gtechsltn\EmberJS-5-8>nvm use 22
Now using node v22.11.0 (64-bit)
D:\gtechsltn\EmberJS-5-8>
```

As of today, Sunday, April 20, 2025, the latest Long Term Support (LTS) version of Ember.js is 5.8. It was promoted to LTS on November 20, 2024.

## Recommended Node.js Versions:
As of April 2025, the currently supported Active LTS versions of Node.js are v18, v20, and v22.

It is highly recommended to use the most recent Active LTS version of Node.js for the best compatibility and to avoid potential issues.

## Specific Compatibility with Ember CLI:

Looking at the compatibility matrix for ember-cli, it indicates the following support as of the latest information:

* Node.js v18: Supported by ember-cli versions 4.6.0 and later.
* Node.js v20: Supported by ember-cli versions 5.4.0 and later.
* Node.js v22: Supported by ember-cli versions 6.2.0 and later.

Since Ember.js 5.8 was released around April 2024, it is expected to work well with the ember-cli versions that support the active Node.js LTS releases at that time and the subsequent ones.

Therefore, for Ember.js 5.8, you should aim to use either Node.js v18, v20, or v22. Using the latest LTS version (currently v22) is generally advisable for new projects as it will have the longest support window.

## NVM
```
D:\gtechsltn\EmberJS-5-8>node -v
D:\gtechsltn\EmberJS-5-8>npm -v
D:\gtechsltn\EmberJS-5-8>nvm install 22
D:\gtechsltn\EmberJS-5-8>nvm use 22
Now using node v22.11.0 (64-bit)
```

## Install Ember CLI 5.8 globally
```
D:\gtechsltn\EmberJS-5-8>npm install -g ember-cli@5.8.0
D:\gtechsltn\EmberJS-5-8>ember --version
```

## Install Ember CLI 5.8 locally as a development dependency
```
D:\gtechsltn\EmberJS-5-8>npm init -y
D:\gtechsltn\EmberJS-5-8>npm install --save-dev ember-cli@5.8.0
```

* **npm install**: The command to install packages.
* **--save-dev**: This flag tells npm to install the package as a development dependency, meaning it's primarily needed during development (building, testing) but not necessarily when the final application is deployed. The information about this dependency will be added to your package.json file under devDependencies.
* **ember-cli@5.8.0**: Specifies the exact version of Ember CLI you want to install.

### How to Use the Locally Installed Ember CLI:

Using npx: npx is a package runner tool that comes with npm (version 5.2+). It allows you to execute locally installed package executables without specifying the full path. Simply run Ember CLI commands like this from within your project directory:

```
npx ember --version
npx ember new my-addon  # Example: creating an addon within the project
npx ember serve
```

Using npm scripts: You can define scripts in your package.json file that run Ember CLI commands. Open your package.json and add a "scripts" section (or modify it if it already exists):

```
{
  "name": "my-special-project",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "ember serve",
    "build": "ember build",
    "test": "ember test"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "ember-cli": "5.8.0"
  }
}
```

Now, you can run these scripts using npm run:
```
npm run start   # Runs 'ember serve'
npm run build   # Runs 'ember build'
npm run test    # Runs 'ember test'
```

Then, use npx or npm scripts to run Ember CLI commands. Happy coding from Vietnam!

## Error
```
You cannot use the new command inside an ember-cli project.
```

## Solution
```
D:\gtechsltn\EmberJS-5-8>npx ember-cli@5.8.0 new modern-portal
Need to install the following packages:
ember-cli@5.8.0
Ok to proceed? (y) y

Ember CLI v5.8.0

Creating a new Ember app in D:\gtechsltn\EmberJS-5-8\modern-portal:
  create .editorconfig
  create .ember-cli
  create ...

Installing packages... This might take a couple of minutes.
npm: Installed dependencies

Initializing git repository.
Git: successfully initialized.

Successfully created project modern-portal.
Get started by typing:

  $ cd modern-portal
  $ npm start

Happy coding!

D:\gtechsltn\EmberJS-5-8>cd modern-portal
D:\gtechsltn\EmberJS-5-8\modern-portal> npm start

> modern-portal@0.0.0 start
> ember serve
> ...
```
