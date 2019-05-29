# 资讯简介

A file named `angular.json` at the root level of an Angular [workspace](guide/glossary#workspace) provides workspace-wide and project-specific configuration defaults for build and development tools provided by the Angular CLI. 
Path values given in the configuration are relative to the root workspace folder. 

## 什么是资讯？

At the top level of `angular.json`, a few properties configure the workspace, and a `projects` section contains the remaining per-project configuration options. 

* `version`: The configuration-file version.
* `newProjectRoot`: Path where new projects are created. Absolute or relative to the workspace folder.
* `defaultProject`: Default project name to use in commands, where not provided as an argument. When you use `ng new` to create a new app in a new workspace, that app is the default project for the workspace until you change it here.
* `projects` : Contains a subsection for each project (library, app, e2e test app) in the workspace, with the per-project configuration options. 

The initial app that you create with `ng new app_name` is listed under "projects", along with its corresponding end-to-end test app: 

## 资讯的类型？

下面的表格中呈现了资讯的类型

| 类型 | 描述 |
| :-------------- | :---------------------------- |
| `二手房`          | 本类型介绍了二手房的资讯信息 |
| `新房`    | 本类型涵盖了新房的资讯信息. |
| `租赁`   | 本类型涵盖了租赁的资讯信息.|
| `招聘`        | 本类型涵盖了招聘的资讯信息. |
| `法务`     | 本类型涵盖了法务的资讯信息. |
| `其他`     | 本类型涵盖了其他内容的资讯信息. |

## 资讯的作用？

Architect is the tool that the CLI uses to perform complex tasks such as compilation and test running, according to provided configurations. The `architect` section contains a set of Architect *targets*. Many of the targets correspond to the CLI commands that run them. Some additional predefined targets can be run using the `ng run` command, and you can define your own targets.

* The `architect/build` section configures defaults for options of the `ng build` command. See [Build target](#build-target) below for more information.

* The `architect/serve` section overrides build defaults and supplies additional serve defaults for the `ng serve` command.  In addition to the options available for the `ng build` command, it adds options related to serving the app.

* The `architect/e2e` section overrides build-option defaults for building end-to-end testing apps using the `ng e2e` command.
