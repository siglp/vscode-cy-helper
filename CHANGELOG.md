# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] - YYYY-MM-DD

## [3.0.0] - 2022-07-28
### Added
 - simple cache for reading files, listen to fs changes instead of reading them again
 - more early returns for cases when additional work is not needed
 - publish extension as single bundle instead of multiple files

### Changed
- moved description with gifs (for commands and other functionality) to separate files to avoid loading multiple gif files.
- documentation gif images size reduced from 63.9 Mb to 34.6 Mb thus in combination with separating docs to separate pages should improve experience with docs.

## [2.7.0] - 2022-07-27
### Added
- automatically detect spec argument for Cypress Open based on cypress version in package.json

## [2.6.0] - 2022-07-26
### Added
- support for multiple workspace folders

## [2.5.1] - 2022-07-08
### Fixed

- properly handle `CommandReferencesProvider.provideReferences` when no usage found, address #13
- cypress execution code lense provider, address #11
- trigger fixture completion provider on ' and ` characters

## [2.5.0] - 2022-06-21

### Added

-   support for `specify` mocha keyword for

## [2.4.1] - 2022-06-21

### Fixed

-   by [Dane Dukic](https://github.com/ddukic): lack of support for cypress v10 for "Open Cypress" command

## [2.4.0] - 2021-12-21

### Added

-   config options `ItSkip` and `ItOnly` for `menuItems` object which are responsible for code lenses visibility
-   code lense for adding and clearing `it.skip`, address #3

## [2.3.0] - 2021-09-17

### Added

-   autocomplete for `cy.task`
-   go to definition for `cy.task`

## [2.2.0] - 2021-08-19

### Added

-   Generate JSON schema for json files menu item, enable menu item by default

## [2.1.0] - 2021-08-18

### Added

-   Autocompletion provider in gherkin files for allure tms and issue links autocompletion with xray test cases or jira issues

## [2.0.1] - 2021-08-03

### Changed

-   improved snippets for allure cucumber tags and provided option to use single argument, due to cypress-allure-plugin v2.9.0

## [2.0.0] - 2021-07-27

### Changed

-   moved to forked repository, new version is available by name "Cypress Helper v2"
-   publishing a fix for https://github.com/90poe/vscode-cy-helper/issues/60 as additional config for code lenses, for example `"cypressHelper.cypressCodeLensePattern": "**/e2e/**/*.+(js|ts|feature)"` will add code lenses just for files inside e2e folder

## [1.2.5] - 2021-04-27

## [1.2.4] - 2021-04-18

### Fixed

-   #51, handle duplicated tests in open\run code lenses

### Added

-   cucumber allure tags autocomplete: link and parentSuite labels

## [1.2.2] - 2021-04-01

### Fixed

-   #48, address issue when errors are thrown for some commands on initialisation it blocks other functionality

## [1.2.1] - 2021-03-20

### Changed

-   now terminals in Cypress Helper are created with specific current directory. In case directory not matches current terminal it will spawn new one. By default workspace root is used.

### Fixed

-   #43, solved by checking if package.json exist in sub-folders. In case it exist we treat folder as root for new terminal to support Cypress Run and Cypress Open code lenses for nested projects and calculate corresponding relative path to spec or root path.

## [1.2.0] - 2021-03-19

### Added

-   #40, autocomplete for jquery locators

### Changed

-   previously alias autocomplete suggested only aliases from saved changes. now it also provides unsaved from current file.
-   use snippets for allure tags autocompletion
-   add AS_ID to allure tags

### Fixed

-   cy.type keypress events autocomplete usage in template literals

## [1.1.0] - 2021-03-15

### Added

-   #39, autocompletion for cy.type keyPress sequences

## [1.0.3] - 2021-02-15

### Fixed

-   #34, capitalize absolute windows path when lowercase used

## [1.0.2] - 2021-01-29

### Fixed

-   #34, handle path with spaces when passing file to open cypress command

### Added

-   #30, option to run spec in cypress

## [1.0.1] - 2020-12-02

### Fixed

-   #32, for fixture definition check if resulting file exists

## [1.0.0] - 2020-11-24

### Added

-   github action updated with deployment to Open VSX registry

## [0.9.0] - 2020-11-24

### Added

-   configuration option to allow user respawn terminal on each Cypress open

## [0.8.3] - 2020-10-12

### Added

-   90poe internal: option to generate json schemas via binary for all new fixtures parsed from HAR

## [0.8.2] - 2020-09-21

### Fixed

-   check optional flag when parsing typescript arguments, address #27

### Changed

-   show only one codelense (set or clear tag) for each test

## [0.8.1] - 2020-09-04

### Fixed

-   clearing tags for feature file when auto-formatting enabled

## [0.8.0] - 2020-08-31

### Added

-   option to trigger custom command types generation on save event

## [0.7.1] - 2020-08-30

### Fixed

-   clearing `@focus` tags on terminal closing

## [0.7.0] - 2020-08-30

### Changed

-   menu items `Cypress: Open Spec File` and `Cypress: Open Single Test` replaced with CodeLenses right in test files

## [0.6.4] - 2020-06-15

### Fixed

-   glob pattern should always use forward-slashes, fixes issue with OS Windows

## [0.6.3] - 2020-06-15

### Added

-   better error messages for custom commands detection and definition

### Fixed

-   handling of configuration paths to have same config working for different OS

## [0.6.2] - 2020-05-29

### Fixed

-   properly resolve path, caused issues with linux mint

## [0.6.1] - 2020-05-22

### Added

-   github action for extension publish

### Changed

-   extension logo, based on [comment](https://github.com/cypress-io/cypress-documentation/pull/2721#issuecomment-630977645) from Cypress team representative.

## [0.6.0] - 2020-05-10

### Added

-   support for typescript files
-   better handling of cucumber step definitions with regex

## [0.5.2] - 2020-04-27

### Added

-   autocomplete for aliases in same folder
-   go to definition for aliases in same folder

### Changed

-   impoved definition provider for fixture file paths

## [0.5.1] - 2020-04-26

### Added

-   go to definition for fixture files

## [0.5.0] - 2020-04-08

### Added

-   cucumber tags autocompletion
-   option for [cypress-allure-plugin](https://www.npmjs.com/package/@shelex/cypress-allure-plugin) cucumber tags autocompletion

### Fixed

-   fixture autocomplete for gherkin files only on `"` character
-   prompt to reload vs code only when cypressHelper configuration affected

## [0.4.3] - 2020-03-23

### Changed

-   bump dependencies

### Added

-   90poe internal autocomplete provider for graphql mock commands

## [0.4.2] - 2020-03-02

### Fixed

-   addressing [Custom command folder setting not working?](https://github.com/90poe/vscode-cy-helper/issues/16)

## [0.4.1] - 2020-02-10

### Fixed

-   autocomplete triggering for VS Code 1.42.0

### Changed

-   moved 90poe internal commands to separate directory

## [0.4.0] - 2020-02-04

### Added

-   90poe internal command to convert HAR file into fixtures
-   90poe internal command to execute json schema generator binary

## [0.3.9] - 2019-12-12

### Added

-   fixture autocomplete for feature files on `"` character

## [0.3.8] - 2019-12-11

### Changed

-   switch from klaw-sync to fast-glob to read fs

## [0.3.7] - 2019-12-10

### Added

-   Command to create tsconfig.json (addressing [issue#12](https://github.com/90poe/vscode-cy-helper/issues/12))
-   Prompt to create tsconfig.json if not found after generating type definitions

## [0.3.6] - 2019-12-09

### Added

-   Definition provider for custom commands (native `Go to Definition`, `Peek Definition` items)
-   References provider for custom commands (native `Find All References`, `Peek References` items)
-   References provider for step definitions
-   Configuration to disable Command References provider in case type definition file in workspace
-   More information in README.

### Fixed

-   opened blank file when no command definition found

## [0.3.5] - 2019-12-05

### Added

-   prompt to reload vscode when configuration changed

### Fixed

-   fixture autocomplete when several commands chained on same line

## [0.3.4] - 2019-12-05

### Added

-   ability to configure cypress commands that require fixture autocomplete

### Fixed

-   activation of fixture autocompletion for `.ts` files

## [0.3.3] - 2019-12-04

### Added

-   `cy.fixture` autocompletion

## [0.3.2] - 2019-11-27

### Fixed

-   issue with some globally installed dependencies causing failure to read workspace files.
-   message in case no type definitions found for custom commands

### Added

-   badge to readme with link to gitter chat

## [0.3.1] - 2019-11-11

### Fixed

-   filePaths for cucumber commands on windows.

## [0.3.0] - 2019-11-04

### Added

-   basic file watcher to reduce fs operations amount and increase performance

### Fixed

-   sometimes custom command was not recognized when there are several on single line
-   catch error when reading non existing file

## [0.2.9] - 2019-10-24

### Fixed

-   failed extension activation when step definition folder not exist

## [0.2.8] - 2019-09-23

### Added

-   possibility to add annotations for custom command type definitions

### Changed

-   codebase refactoring

## [0.2.7] - 2019-09-19

### Added

-   license

## [0.2.6] - 2019-09-16

### Added

-   menu items are now configurable
-   slight performance tweaks

## [0.2.5] - 2019-09-13

### Changed

-   codebase improvements

## [0.2.4] - 2019-09-09

### Added

-   extension logo and description

## [0.2.3] - 2019-09-09

### Fixed

-   issue with parsing function argument with `undefined` or `null` default value
    recognized as object

## [0.2.2] - 2019-09-06

### Changed

-   codebase improvements

## [0.2.1] - 2019-09-04

### Added

-   Support for regexp cucumber type definitions

## [0.2.0] - 2019-09-04

### Added

-   Support custom cucumber types created with `defineParameterType`

## [0.1.9] - 2019-09-04

### Changed

-   codebase improvements

## [0.1.8] - 2019-09-04

### Changed

-   improve Cypress custom command detection

## [0.1.7] - 2019-09-04

### Added

-   menu item to find Cypress custom command references across framework

## [0.1.6] - 2019-09-04

### Added

-   menu item to find Cucumber step definition references across framework

## [0.1.5] - 2019-09-02

### Added

-   command to search for unused cucumber step definitions

## [0.1.4] - 2019-09-01

### Added

-   search for unused cypress custom commands

## [0.1.3] - 2019-08-29

### Fixed

-   case when several custom commands are used in same row

### Changed

-   write type definition file even when some commands were failed to parse

## [0.1.2] - 2019-08-28

### Fixed

-   add assets folder to vscode ignore to keep extension size small

## [0.1.1] - 2019-08-28

### Changed

-   use glob pattern for excludes from custom commands search

## [0.1.0] - 2019-08-27

### Changed

-   codebase improvements

## [0.0.9] - 2019-08-23

### Added

-   remove `@focus` and `.only` after terminal closed

## [0.0.8] - 2019-08-23

### Changed

-   reuse same terminal instance for opening cypress

## [0.0.7] - 2019-08-22

### Changed

-   improve user messages

## [0.0.6] - 2019-08-22

### Changed

-   improve user messages

## [0.0.5] - 2019-08-22

### Added

-   command for generating ts types for cypress custom commands

## [0.0.4] - 2019-08-22

### Added

-   keybindings for opening cypress custom command definition
-   conditions for showing menu items for commands

## [0.0.3] - 2019-08-22

### Changed

-   codebase improvements

## [0.0.2] - 2019-08-21

### Changed

-   codebase improvements

## [0.0.1] - 2019-08-21

### Added

-   command to open cypress custom command definition
-   command to open cypress for single test
-   command to open cypress for file
-   initial extention setup
