# Changelog 

Earlier changes were not versioned. Therefore dates of change are used instead there.

For new releases see [Github Release page](https://github.com/AuHau/toggl-cli)

## [2.5.0](https://www.github.com/hugovk/toggl-cli/compare/v2.4.3...v2.5.0) (2022-05-20)


### Features

* date-format config support ([176c8cf](https://www.github.com/hugovk/toggl-cli/commit/176c8cf7d157915cdc8ab1fb0c73e09c7eb4af95))
* python 3.8 support ([d7bb33e](https://www.github.com/hugovk/toggl-cli/commit/d7bb33e6ade596bfca328d517bc2e6c9104aeb55))
* rework of goal and sum commands ([72f10d7](https://www.github.com/hugovk/toggl-cli/commit/72f10d780f6828292afadbc68d95f17cee0506d1))
* sum and day command functions ([#136](https://www.github.com/hugovk/toggl-cli/issues/136)) ([8e874bf](https://www.github.com/hugovk/toggl-cli/commit/8e874bf586392045cf5458d97d57c1a811dfcbce))
* support for billable ([2cf0861](https://www.github.com/hugovk/toggl-cli/commit/2cf08617f2da722821d4134ed94687421c17105b))
* task for start command ([#211](https://www.github.com/hugovk/toggl-cli/issues/211)) ([6bff185](https://www.github.com/hugovk/toggl-cli/commit/6bff185291c72a1c38101579531b3b3bf700f9f2))
* theme support ([8fcf165](https://www.github.com/hugovk/toggl-cli/commit/8fcf165c4a6e50d65c72f753a22ea004531598cd))
* use new api url ([#185](https://www.github.com/hugovk/toggl-cli/issues/185)) ([9f659f8](https://www.github.com/hugovk/toggl-cli/commit/9f659f81dafa385d799cd3f95de58e980817d70f))


### Bug Fixes

* circular import ([#141](https://www.github.com/hugovk/toggl-cli/issues/141)) ([2b9a634](https://www.github.com/hugovk/toggl-cli/commit/2b9a6343767da116738dacf0cc903a43b4bd61cb))
* start cmd and billable in non-premium workspace ([c714ea2](https://www.github.com/hugovk/toggl-cli/commit/c714ea234fa767ecbbfb8084e888a20560b40050))
* sum command respects configured timezone ([#205](https://www.github.com/hugovk/toggl-cli/issues/205)) ([c2b4875](https://www.github.com/hugovk/toggl-cli/commit/c2b48756bce1be6a9e21fed52170ae33a5cbe21a))
* tests ([ad0b6da](https://www.github.com/hugovk/toggl-cli/commit/ad0b6da1f58ba078c92ef2d51e02bf09a4e9ee5a))
* where default workspace was always set, and uid was never set ([#156](https://www.github.com/hugovk/toggl-cli/issues/156)) ([988f461](https://www.github.com/hugovk/toggl-cli/commit/988f46101adeca1082b0e37209d7f57947ec25d2))
* wrong config mapping of values ([#163](https://www.github.com/hugovk/toggl-cli/issues/163)) ([12b48bf](https://www.github.com/hugovk/toggl-cli/commit/12b48bf8ed5a9308193fa6901e4beed05ee74b71))


### Documentation

* fix typo ([#162](https://www.github.com/hugovk/toggl-cli/issues/162)) ([d5f697f](https://www.github.com/hugovk/toggl-cli/commit/d5f697f5d097bf70131ebb649b24c79562002760))
* update ([cbdd2d2](https://www.github.com/hugovk/toggl-cli/commit/cbdd2d23d119a2a1b69fcb8d1e8fdd4bd7a8d036))

## v2.2.0

Features:
 * Python 3.8 support
 * new `toggl sum` command that displays sums of time grouped by days
 * new `toggl goal` command that waits until you reach your defined goal for the day and the send notification
 * new theming support
 * `--today` flag for `ls` and `sum` command  

## v2.1.0

Features:
 * New Tag model with CLI commands
 * 'me' command to display current user's info
 
Fixes:
 * Correct retrieval of package's version 
 * Properly working Premium/Non-premium tests

## v2.0.2

Fixes for python_required and calculation of duration

## v2.0.1

Fix for required python version

## v2.0.0

Full rewrite of the tool by [AuHau](https://github.com/AuHau), which implements most of the toggl's API capabilities. 
Entities which is now possible to fully manage (eq. CRUD operations):
 *  Time entries
 *  Clients
 *  Projects
 *  Project users
 *  Tasks (only for premium workspaces)
 *  Workspaces
 *  Workspace users
 
Main new features of the tool:
 *  Possibility to use environment variables to specify some of the input parameters
 *  Possibility to specify different config to be used for the command's execution
 *  Django ORM's like API Classes

## v2.0.0.0b3

 * Fixing bootstrap failures
 * Dropping relative imports
 * Minor improvements

## v2.0.0.0b2

 * Adding support for Time entries Report API which enables fetching all time entries ( `api.TimeEntry.objects.all_from_reports()` / `toggl ls --use-reports`)
 * Adding support to register specific Config object as default one

## v2.0.0.0b1

First Beta release of full rewrite

## 15 Dec 2014 
Thanks to [FedericoVaga](https://github.com/FedericoVaga)
`.togglrc` now supports API token authentication. You will need to add
`api_token` to the `auth` section, and `prefer_token` to the `options` section.

## 11 Nov 2014
Major refactoring into a more MVC OO structure.

## 30 Oct 2014
Added a feature that starting, stopping, and continuing an
entry prints out the time it started or stopped. This requires a new option in
~/.togglrc: `time_format = %I:%M%p` is the default.  See
[strftime()](https://docs.python.org/2/library/datetime.html#strftime-and-strptime-behavior)
for more options.
