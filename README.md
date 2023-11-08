# SUSE Enceladus

## Introduction

The SUSE-Enceladus organization in GitHub was created to serve the needs of the SUSE Public Cloud DevOps team. We started out with a "collector" project named Enceladus within the SUSE organization. Over time the collector project grew unwieldy and we had various unrelated source bases intermingled in the Enceladus project. In addition some of our other projects, large an small were maintained in separate projects in separate orgs. SUSE-Enceladus was created to collect our efforts for original source code in one organization, help us be more organized, and provide a better overview of the projects we develop and maintain. The initial projects in this organization started as migrations from Enceladus or other projects we maintained in GitHub.

## Goals

We strive to provide a reasonably uniform experience for all projects within the SUSE-Enceladus organization. In an effort to achieve this uniform experience we strive to document our processes and procedures. Each project will have a LICENSE, a README.md, and a CONTRIBUTING.md file that provides information about the project. However, projects do have different needs and therefore some differences are to be expected.

Projects in the SUSE-Enceladus organization represent original work of the SUSE Public Cloud DevOps team. We hope our work is useful to you and we welcome any contribution. All projects in SUSE_Enceladus are in alignment with the [SUSE open source policy][1] and as such we do not have a contributor agreement.

The projects in the SUSE-Enceladus organization do not accept content generated with the assistance of artificial intelligence as contributions. By submitting a pull request for review and inclusion the submitter certifies that the contribution was not generated with the assistance of AI.

[1]: https://opensource.suse.com/suse-open-source-policy

# Contributing to this site

This site is a [Lektor](https://www.getlektor.com/) project published via github CI to [github pages](https://pages.github.com/).

Please see https://www.getlektor.com/docs/installation/ for instructions on setting up Lektor locally for development.

### Documents

Each document is represented as a _page_ object, stored in a `contents.lr` file, nested under [content](/content). Please see the [Lektor content docs](https://www.getlektor.com/docs/content/) for more details on how this works. In short, the structure of content is defined in the model (in the /models dir.), the content itself is defined in the lektor file (in /contents), and that is rendered into a template defined in /templates.


There is currently one document in this project: the home page. It's an instance of the [homepage model](/models/homepage.ini). This page also includes nested elements ([flow blocks](https://www.getlektor.com/docs/content/flow/) in Lektor terminology). Both the homepage model, and any nested blocks define attributes. Those attributes are then rendered into the [homepage template](/templates/homepage.html) (which is nested in the [layout template](/templates/layout.html)).

### Pull Requests

* Use the Lektor admin interface to make content changes, instead of attempting to directly edit the .lr files.
* Use the Lektor admin interface to preview changes before submitting a PR. All content, including CSS changes, template changes, model changes and content changes are rendered immediately to the admin interface.
* Please include a screenshot when submitting a PR.

---
All contents Copyright (c) 2023 SUSE LLC.
