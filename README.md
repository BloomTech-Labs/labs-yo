# Labs wrapper for Yeoman

This wrapper of yeoman simply allows the use of `labs` in place of the common
use of `yo`

## Installation

> The project has not yet been deployed to <npmjs.com> yet.

`npm i -g @lambdalabs/labs`

This will install the main cli wrapper along with all Labs generators as
dependancies.

## Usage

The `labs` cli command is just a wrapper to the [yeoman](https://yeoman.io/learning/index.html)
`yo` command.

## Examples

- Run the SPA generator (base react single page app starter)
  
  `labs @lambdalabs/spa project-name`

- Run the Node API generator (base node express api starter)
  
  `labs @lambdalabs/api project-name`

## Generators

- [SPA React](https://www.npmjs.com/package/@lambdalabs/generator-spa)
- [Node API](https://www.npmjs.com/package/@lambdalabs/generator-api)

## publish npmjs package

- update package.json version
- add a git tag with the version number `git tag v0.9.30 -m "release note"`
- push repo and tags `git push && git push --tags`

## Development setup

To develop locally it will be easiest to link the `labs` command and any generators being developed using npm.

1. link the generator in the labs-yo project folder.

    1. Go to the cloned and npm-installed project folder
    2. `npm link`
    3. Cd back to this `labs-yo` folder
    4. `npm link "name-of-package"`
    5. Example: `npm link "generator-spa`

2. link this project to the global npm commands.

    `npm link`

    The `labs` command is now globally available.

    `labs --help` should render the `yo` command options.