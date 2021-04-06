<p align="center">
    <img width="300" src="https://github.com/withfig/fig/blob/main/static/FigBanner.png?raw=true"/>
</p>

---
## Autocompletion Boilerplate

### TL;DR
This repository is a starter for teams to get started quickly when creating completions for private CLIs and scripts which should not be public.

## Getting Started
This repo is a `template` which means you can create your own repo with just a click. Simply click the **Use this template** button at the top right of this repository to create a new repository.

```bash
# Install packages
npm install

# Go into testing mode
npm run dev
```

Edit your spec in the `dev/` folder. It will compile to the root folder on save. Start testing your spec immediately in your terminal.

**Note**: Fig usually looks for completion specs in your `~/.fig/autocomplete` folder.

## Commands
### dev
Running 
```bash
npm run dev
```
starts the developer mode which makes development of completion specs easy. It updates the completions in fig as soon as you save your files while `dev` is running.

### test
The test commands enables typechecking of your specs. It will check for `TypeErrors` using TypeScript


### copy (general)
When fig shows the suggestions it will look for `.js` files in your local `~/.fig/autcomplete` folder. Therefore you need to copy your changed spec(s) from this repo to that folder. We have to helper functions for that usecase in place:

### copy
*Example:* 
```bash
npm run copy git
```
This command will copy the `git.js` spec to `.fig/autcomplete` folder.

### copy:all
This command copies **all** specs from this repository to your local `.fig/autocomplete` folder.

### create-boilerplate
This commands starts a small helper CLI which creates a new spec in the `/dev` folder. It adds a new `<name>.ts` file with some boilerplate content.

### build
This command compiles all `.ts` files in the `/dev` folder to `.js`. 

**Note:**
This needs to be used before copying files using `npm run copy` or `npm run copy:all`


### lint
This command checks all files for formatting (e.g. spacing and quotes) and invalid code (e.g. `name` property including a `=`)

### lint:fix
This command does the same as `npm run lint` but also fixes all problems which can be fixed automatically (e.g. using the correct quotes).

### prepare
Internal command used to install git hooks.