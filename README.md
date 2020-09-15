# Labs wrapper for Yeoman

This wrapper of yeoman simply allows the use of `labs` in place of the common
use of `yo`

## Installation

> The project has not yet been deployed to <npmjs.com> yet.

`npm i -g labs-yo`

This will install the main cli wrapper along with all Labs generators as
dependancies.

## Usage

The `labs` cli command is just a wrapper to the [yeoman](https://yeoman.io/learning/index.html)
`yo` command.

## Examples

- Run the SPA generator (base single page app starter)
  - `labs spa`

## Generators

- [SPA React](https://github.com/Lambda-School-Labs/generator-spa)
- [Node API](https://github.com/Lambda-School-Labs/generator-api)

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