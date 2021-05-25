<p align="center">
    <img width="300" src="https://github.com/withfig/fig/blob/main/static/FigBanner.png?raw=true"/>
</p>

---

![os](https://img.shields.io/badge/os-%20macOS-light)
[![Signup](https://img.shields.io/badge/signup-private%20beta-blueviolet)](https://fig.io?ref=github_autocomplete)
[![Documentation](https://img.shields.io/badge/documentation-black)](https://fig.io/docs/)
![Discord](https://img.shields.io/discord/837809111248535583?color=768ad4&label=discord)
[![Twitter](https://img.shields.io/twitter/follow/fig.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=fig)

# Autocompletion Boilerplate

This repository is a template for **individuals / teams looking to build autocomplete specs for private CLIs and scripts** (ie scripts that they do not want to make public).

This repo is almost exactly the same as [withfig/autocomplete](https://github.com/withfig/autocomplete) except the `dev/` and `specs/` folders are empty (they will appear after you run `npm run create-boilerplate`)

## Documentation

- Main docs: [fig.io/docs](https://fig.io/docs/)
- Autocomplete for personal shortcuts: [fig.io/docs/tutorials/visual-shortcuts](https://fig.io/docs/tutorials/visual-shortcuts)
- Autocomplete for teams: [fig.io/docs/tutorials/building-internal-clis](https://fig.io/docs/tutorials/building-internal-clis)

## Using this repo

Build your first spec in < 3 min: [fig.io/docs/getting-started](fig.io/docs/getting-started)

1. Click "**Use this Template**" above

2. Clone your forked repo and create an example spec

```bash
# Replace `YOUR_GITHUB_USERNAME` with your own github username
git clone https://github.com/YOUR_GITHUB_USERNAME/autocomplete.git fig-autocomplete
cd fig-autocomplete

# Add withfig/autocomplete as a remote
git remote add upstream https://github.com/withfig/autocomplete.git

# Install packages
npm install

# Create an example spec (call it "abc")
npm run create-example

# Turn on "dev mode"
npm run dev
```

3. Now go to your terminal and type `abc[space]`. Your example spec will appear. 😊

#### Other things to know

- Edit your spec in typescript in the `dev/` folder
- On save, specs are compiled to the `specs/` folder
- In **dev mode** specs are read from the `specs` folders. Otherwise they are read from `~/.fig/autocomplete`

<br/>

## Save My Spec Locally

Compile your spec then save it to your `~/.fig/autocomplete` folder

```bash
# Compile your spec(s) to the specs/ folder
npm run build

# Copy your spec from the specs/ folder to the ~/.fig/autocomplete folder
npm run copy <spec-name>
```

## Share with My Team

Compile your spec(s) to the `specs/` folder

```bash
npm run build
```

Now your spec has been compiled to the `specs/` folder, you can share the `.js` file with your team. Once they put it in their `~/.fig/autocomplete` folder, they will have full access to the completions you generated.

**Note**: alternatively, you could commit your spec to your repo, have your team clone the repo, then do the same as `Save My Spec Locally` above.

> Fig is working on providing a much better experience for this and is launching it very soon.

## Other available package.json commands

```bash

# Create a new spec from a boilerplate template
npm run create-boilerplate

# Typecheck all specs in the dev/ folder
npm test

# Compile typescripts specs from dev/ folder to specs/ folder
npm run build

# Copy all specs from the specs/ folder to the ~/.fig/autocomplete folder
npm run copy:all

# Copy an individual spec from the specs/ folder to the ~/.fig/autocomplete folder
npm run copy <spec-name>
```

## 😊 Need Help?

Email [hello@fig.io](mailto:hello@fig.io)

<p align="center">
    Join our community
<br/>
<a href="https://fig.io/community">
    <img src="http://fig.io/icons/discord-logo-square.png" width="80px" height="80px" /> 
</a>
</p>
