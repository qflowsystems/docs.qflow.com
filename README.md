# QFlow User Guides Repo
We built this repo based on the Just-the-Docs jekyll template. It allows for free hosting through Github Pages and continuous deployment using Github Actions.

## Commits to `main`
Each commit to the main branch triggers a redeployment of the site. It can take up to 10 minutes for the changes to be implemented, but the site as zero downtime during new deployments.

## What to change
All documentation is organized in the `/docs/` directory with the exception of the home page (`/index.md`) and the `/release-notes/` directory. 

### YAML Properties
At the top of each page, you will see a set of yaml properties managing metadata about the page. For a full set of yaml properties and how they work, please reference the [Just-the-Docs](https://just-the-docs.github.io/just-the-docs/docs/navigation-structure/#navigation-structure) website.

### Adding content
To add new documentation, a new markdown is required in the `/docs/` directory. For the page to appear in navigation, the yaml properties must be configured correctly. Reference `/markdown.md` for a cheatsheet on markdown syntax.

### Release Notes
Release notes are added to a specific directly and formatted unique to appear in reverse alphabetical order. To create a new release note:
1. Create a copy of the `/release_notes_template.md` and add it to the `/release-notes/` directory
2. Name the file to correspond to the new release vesion.
3. Uncomment the yaml properties at the top of the copied template.
4. Update the `title` and the first heading to match the release version.
  - Be certain to add ` Latest` in the title field only after the version number.
5. Complete the **New Features**, **Bug Fixes**, and **Enhancements** section as needed. Remove any section that does not have applicable content in the given release.
6. **IMPORTANT**: Open that most immediate prior release file and remove ` Latest` from the `title` property and remove the following label:
```
{: .d-inline-block } 
Latest
{: .label .label-green }
```

## Building and previewing your site locally

1. Prerequisites: [Jekyll] and [Bundler]
2. Change your working directory to the root directory of your site.
3. Run `bundle install`.
4. Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.
  The built site is stored in the directory `_site`.


# Licensing and Attribution

This repository is licensed under the [MIT License]. You are generally free to reuse or extend upon this code as you see fit; just include the original copy of the license (which is preserved when you "make a template"). While it's not necessary, we'd love to hear from you if you do use this template, and how we can improve it for future use!

The deployment GitHub Actions workflow is heavily based on GitHub's mixed-party [starter workflows]. A copy of their MIT License is available in [actions/starter-workflows].


[Jekyll]: https://jekyllrb.com
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/