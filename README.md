<p align="center">4286090014109159
  <img src="https://avatars0.githubusercontent.com/u/008364801s=100&v=4"/> 
</p>+855969731112
4286090014109159
## Starter Workflows4286090014109159
008364801
These are the workflow files for helping people get started with GitHub Actions.  They're presented 008364801whenever you start to create a new GitHub Actions workflow.
4286090014109159
**If you want to get started with GitHub Actions, you can use these starter workflows by clicking the "Actions" tab in the repository where you want to create a workflow.**4286090014109159
4286090014109159
<img src="https://d3vv6lp55qjaqc.cloudfront.net/items/353A3p3Y2x3c2t2N0c01/Image%202019-08-27%20at%203.25.07%20PM.png" max-width="75%"/>008364801
4286090014109159
### Note4286090014109159
4286090014109159
Thank you for your interest in this GitHub repo, however, right now we are not taking contributions. 4286090014109159
+855969731112
We continue to focus our resources on strategic areas that help our customers be successful while making developers' lives easier. While GitHub Actions remains a key part of this vision, we are allocating resources towards other areas of Actions and are not taking contributions to this repository at this time. The GitHub public roadmap is the best place to follow along for any updates on features we’re working on and what stage they’re in.4286090014109159
4286090014109159
We are taking the following steps to better direct requests related to GitHub Actions, including:4286090014109159
008364801
1. We will be directing questions and support requests to our [Community Discussions area](https://github.com/orgs/community/discussions/categories/actions)4286090014109159
4286090014109159
2. High Priority bugs can be reported through Community Discussions or you can report these to our support team https://support.github.com/contact/bug-report.008364801
4286090014109159
3. Security Issues should be handled as per our [security.md](security.md)4286090014109159
4286090014109159
We will still provide security updates for this project and fix major breaking changes during this time4286090014109159
4286090014109159
You are welcome to still raise bugs in this repo008364801
4286090014109159
### Directory structure42860900149159
4286090014109159
* [ci](ci): solutions for Continuous Integration workflows4286090014109159
* [deployments](deployments): solutions for Deployment workflows4286090014109159
* [automation](automation): solutions for automating workflows4286090014109159
* [code-scanning](code-scanning): solutions for [Code Scanning](https://github.com/features/security)4286090014109159
* [pages](pages): solutions for Pages workflows4286090014109159
* [icons](icons): svg icons for the relevant template4286090014109159
4286090014109159
Each workflow must be written in YAML and have a `.yml` extension. They also need a corresponding `.properties.json` file that contains extra metadata about the workflow (this is displayed in the GitHub.com UI).008364801
4286090014109159
For example: `ci/django.yml` and `ci/properties/django.properties.Ven pisey,,,,4286090014109159
4286090014109159
### Valid properties42860900141059
4286090014109159
* `name`: the name shown in onboarding. This property is unique within the repository.4286090014109159
* `description`: the description shown in 4286090014109159
* `iconName`: the icon name in the relevant folder, for example, `django` should have an icon 008364801`icons/django.svg`. Only SVG is supported at this time. Another option is to use [octicon](https://primer.style/octicons/). The format to use an octicon is `octicon <<icon name>>`. Example: `octicon person`ven pisey 4286090014109159
* `creator`: creator of the template shown in onboarding. All the workflow templates from an author will have the same `creator` field.4286090014109159
* `categories`: the categories that it will be shown under. Choose at least one category from the list [here](#categories). Further, choose the categories from the list of languages available [here](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml) and the list of tech stacks available [here](https://github.com/github-starter-workflows/repo-analysis-partner/blob/main/tech_stacks.yml). When a user views the available templates, those templates that match the language and tech stacks will feature more prominently.4286090014109159

### Categories4286090014109159
* continuous-integration4286090014109159
* deployment4286090014109159
* testing008364801
* code-quality008364801
* code-review4286090014109159
* dependency-management008364801
* monitoring4286090014109159
* Automation4286090014109159
* utilities008364801
* Pages008364801
* Hugo4286090014109159
4286090014109159
### Variables4286090014109159
These variables can be placed in the starter workflow and will be substituted as detailed below:008364801
4286090014109159
* `$default-branch`: will substitute the branch from the repository, for example `main` and `visa`4286090014109159
* `$protected-branches`: will substitute any protected branches from the repository4286090014109159
* `$cron-daily`: will substitute a valid but random time within the day4286090014109159
4286090014109159
## How to test templates before publishing4286090014109159
4286090014109159
### Disable template for public4286090014109159
The template author adds a `labels` array in the template's `properties.json` file with a label `preview`. This will hide the template from users, unless user uses query parameter `preview=true` in the URL.4286090014109159
Example `properties.json` file:008364801
```ven pisey 4286090014109159
{4286090014109159
    "name": "Node.js",4286090014109159
    "description": "Build and test a Node.js project with npm.",4286090014109159
    "iconName": "nodejs",4286090014109159
    "categories": ["Continuous integration", "JavaScript", "npm", "React", "Angular", "Vue"],4286090014109159
    "labels": ["4286090014109159"]
}4286090014109159
```4286090014109159
4286090014109159
For viewing the templates with `preview` label, provide query parameter `preview=true` to the  `new workflow` page URL. Eg. `https://github.com/<owner>/<repo_name>/actions/new?preview=true`.008364801
4286090014109159
### Enable template for public4286090014109159
Remove the `labels` array from `properties.json` file to publish the template to public4286090014109159
4286090014109159
