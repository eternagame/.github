# Contributing to Eterna

We're excited to hear that you're interesting in contributing to Eterna! This document contains
guidance for you and information about our expectations in order to make the process as smooth
as possible and help you create high-quality contributions that will be faster for us to incorporate.
There's a lot here, so feel free to focus on the sections most applicable to you!

Thanks for lending us your time and talent! ❤️

- [Questions and Community](#questions-and-community)
- [Feature Requests and Bug Reports](#feature-requests-and-bug-reports)
- [Getting Started](#getting-started)
- [Pull Request Workflow](#pull-request-workflow)
- [Considerations for High-Quality Contributions](#considerations-for-high-quality-contributions)
  - [Code Style and Readability](#code-style-and-readability)
  - [Code Quality, Reliability, and Maintainability](#code-quality-reliability-and-maintainability)
  - [Design, Visuals, and Interactions](#design-visuals-and-interactions)
- [Financial Contributions](#financial-contributions)

## Questions and Community

Have questions about contributing or want to get in touch with us to talk shop (or anything else)?
Join the Eterna Discord: [![Eterna Discord](https://discord.com/api/guilds/702618517589065758/widget.png?style=banner2)](https://discord.gg/KYeTwux).

## Feature Requests and Bug Reports

Have an idea or ran into an issue? We want to hear about it!

If you're an Eterna player, the best way to submit feedback is usually through the
[Eterna Forum](https://forum.eternagame.org/c/feedback/24). This allows us to troubleshoot and discuss with you
and other players and ensure that it is recorded in the correct place with all the information we need for development.

For others (particularly developers), please submit an issue to the relevant GitHub repository. We have issue templates
set up to help ensure you are providing the information needed to help resolve it efficiently. If you can, we'd also
be happy for you to submit a PR with a resolution!

Either way, please take a moment to do a search wherever you are submitting your issue to ensure that it
hasn't already been reported. If you do submit a report, please provide as much detail and context as possible.
In particular, if submitting a bug report please be sure to provide specific steps that we can use to reproduce
the issue reliably (please provide a minimal reproduction for library usage bugs!) as well as any
relevant system information.

### Triaging

New issues submitted to our repositories will automatically be given the "pending triage" label. We will then assign it
a priority based on the following system:
* p1/urgent: Product is unusable for majority of users 
* p2/important: A large number of users have a significant pain point or a significant use case is prevented 
* p3/standard: Enhancement with nominal value or bug with nominal impact
* p4/minor: There is a reasonable workaround or this is a nice to have with limited impact
* p5/chore: A cleanup with no end-user impact 

## Getting Started

If you're not familiar with Git and GitHub, [GitHub's Quickstart](https://docs.github.com/en/get-started/quickstart) is
a great place to start.

If you came here from another repository, that repository should have information in its README
about how to get your development environment set up. New to our GitHub and don't know what projects
you might want to contribute to? Take a look at the following:

- Our current game/RNA design interface: https://github.com/eternagame/EternaJS
- Our current website frontend: https://github.com/eternagame/eternagame.org
- Our current mobile app: https://github.com/eternagame/eterna-mobile
- Our next-generation website: https://github.com/eternagame/eternagame.org-next
- Our next-generation RNA design interface and RNA design libraries: https://github.com/eternagame/eternajs-next
- Automated tooling and core configurations for our "next-gen" repositories: https://github.com/eternagame/workspace-helpers

## Contributor License Agreement

Please be aware that before any contributions are merged into our repositories, you will need
to sign our [Contributor License Agreement](https://cla-assistant.io/eternagame/.github).

## Pull Request Workflow

1. Find something to work on! If you already have something in mind, awesome. Otherwise, take a look
   at the GitHub issues in a repository that interests you, especially issues with the "good first issue" label
   if you're just getting started. If it seems useful, you may want to start out by discussing design decisions
   in a relevant GitHub issue.
2. [Fork the repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo) (if you're a member of our
   GitHub organization, no need to do that - you can make a branch on the main repository itself).
3. In your fork, [create a branch](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository)
   based on the default branch of the repository (for newer repositories this will be `main`) to contain the updates you
   will be making. We suggest using the branch name format `<type>/<kebab-case-short-description>`. For example, if
   you are working on a feature to add a page to search puzzles, it might be `feat/puzzle-search`. Adding a new author filter?
   `feat/puzzles-author-filter`. Fixing a bug preventing said filter from working? `fix/puzzles-author-filter` And so forth.
4. Clone your fork of the repository and check out your new branch locally. Make any changes you want, test them, commit, and push.
5. [Create a pull request (PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).
   Fill out the pull request template. Make a note if there's anything that needs to be done before
   the PR is merged (you may want to make it a draft in that case) or if there's any advice you could
   use from us to help get it over the finish line (also feel free to get in touch via Discord!). Note that pull request
   titles should comply with the [conventional commit](https://www.conventionalcommits.org) format - see below for more info.
6. Ensure that the CI status checks (which verify everything builds, linting and tests pass, etc) all succeed. If not,
   resolve the issues.
7. Once all status checks pass, we'll review your PR and provide any feedback we feel is needed.
8. Once all feedback is addressed, we'll merge your PR (most likely via a "squash commit").
9. Congrats, and thank you! Your code has been accepted and will be deployed with the next release. At this point,
   you can delete the branch you were working on (if you move on to another task, you'll create a fresh branch).

### Conventional Commits

We ask that when submitting a PR, you provide a title that follows the conventional commits standard.
Some of our repositories will verify this in continuous integration.

The general format is: `<type>(<scope>): <description>`. If a breaking change is introduced,
you will also need to add a `!` before the `:`.

Examples:
* `fix(core): Fixes a problem with the core module`
* `feat(secondary)!: A breaking change adding a new feature in the secondary module`

Valid types are feat (feature/enhancement), fix (bugfix), perf (performance), revert (reverting a prior commit),
deps (dependencies), docs (documentation), refactor (refactoring), test (updating automated tests), or
chore (formatting changes, build/tooling/ci updates, other configuration updates, etc)

To find a list of valid scopes, take a look at the `scope:` issue labels in the repository you are
submitting this PR to. If there are no scope labels, you may omit the `(<scope>)` portion of the title.
Note that if you are adding a new scope to the CI configuration and you use that scope in the same PR,
the CI will fail. That is expected, as that GitHub action needs to base its configuration on
the master branch - the PR will be merged ignoring the check in that case.

For additional details on the conventional commits format, see: https://www.conventionalcommits.org

### Additional Advice

Some advice to help ensure things go smoothly:
- Limit the scope of a PR. The smaller the change and the less code there is to review, the faster we can review it
  and we'll be able to provide higher-quality feedback.
- Commit liberally, within reason. In general, [atomic commits](https://dev.to/paulinevos/atomic-commits-will-help-you-git-legit-35i7)
  are ideal. This allows your commit history to be useful documentation when seeing why changes were made (either during the
  PR process or far in the future). Make your commit messages as descriptive as possible!
- Make sure to fill out the PR template with as much detail as you can - this will help us review your PR faster
  and ensure we have high-quality context we can reference down the line if needed.
- If reasonable, add automated tests! This helps make us (and you) confident that your change works as intended, and
  helps us ensure our code continues to work as we continue to change it into the future. That said, don't go crazy - we're
  not aiming for 100% code coverage (that is more likely to cause friction as tests are more likely to break, and there's
  a good chance the tests wouldn't be particularly high quality), but we want enough tests to verify that we can update
  dependencies and other areas of the code and feel reasonably secure that nothing breaks. It's also a good way to make
  sure you're handling edge cases in logic and understanding desired behavior.
- In some situations, we may not approve of adding a feature you may have written. Especially if it's a more complex feature
  or there is likelihood of disagreement, it may be a good idea to open a feature request for the issue first to allow for
  discussion.
- If a change affects an API or user-facing functionality, be sure to update any relevant documentation.

## Considerations for High-Quality Contributions

Here's some things we look for when reviewing contributions.

### Code Style and Readability

* Does the code follow existing conventions in the codebase? Have any automatic formatting tools been run?
* If any exclusions for lint rules were added, is it clear why it must be disabled? Are there alternate
  implementations that would allow for the exclusion to be removed?
* Are names (variables, functions, classes, etc) simple and meaningful? Is it clear from the name
  what the item is or does?
* Are docstrings added to functions, classes, and attributes? Do they clearly summarize what it is,
  what it does, and how it works?
* Does the code clearly convey intent? Is it written such that by reading the code, it reads as much
  as possible like a natural language description of what it does?
* Does code maintain an appropriate balance of being explicit without being verbose, and being terse
  without being difficult to understand at a glance?
* Are classes and functions relatively small? (As a rule of thumb, it should have/do
  [at most seven "things"](https://www.youtube.com/watch?v=t3rSCpcJzm0))
* Are functional programming practices used where appropriate, limiting mutation?
* Is code relatively "flat" (limiting nested if statements, loops, etc)?
* Are there any potential "gotchas" or subtleties in the way the code is written that could be eliminated?
* If for some reason code cannot be written to be obvious or remove gotchas, or additional context is needed
  to understand why a piece of code exists, is it properly commented?
* Are there any formatting changes that could improve readability?

### Code Quality, Reliability, and Maintainability

* Have all automated tests passed? Have any appropriate new automated tests been added?
* Does the code take advantage of type safety as much as possible?
* Are new functions, classes, and other modules properly encapsulated and loosely coupled?
  * Do they have a clear scope of responsibility?
  * Do they have small, clear interfaces so that they can act as a "black box"?
  * Is there a minimal need to coordinate multiple operations when using either an internal or external
    API surface (eg, are setters and getters used instead of needing to manually call an update function)?
  * Are functional programming practices used where appropriate, limiting state and ensuring pure functions?
* Is code duplication avoided in situations where code is large, complex, or needs to change together?
* Does architecture follow existing conventions where appropriate?

### Design, Visuals, and Interactions
* Do any new visual elements/interactions follow conventions in the existing application's design/structure
  as well as any style guides?
* Have alternative implementations been considered to find an optimal approach, and have decisions been documented?
* Have any additions and changes been vetted with users?
  * Do changes have the potential to break existing user workflows?
  * Are operations efficient for real user workflows, including advanced users?
* Is usability ensured for users with small screens and touchscreens (eg, mobile)?
* Are operations intuitive and understandable?
  * Are there visual alternatives for all operations?
  * Do interfaces follow standard conventions?
  * Are operations discoverable, including necessary visual cues?
  * Is there appropriate feedback to user actions?
  * Is there appropriate error validation? Are there understandable error messages? Are there ways error
    states can be avoided entirely (namely by preventing user error through forcing functions rather than
    eg ignoring user input which could be unclear)?
* Are there any accessibility concerns?
  * Is there sufficient contrast?
  * Does it work for users who are colorblind?
  * Does it work for users with visual impairments?
  * Does it work for users with screenreaders? Is semantic markup used?
  * Does it work for users with hearing impairments?
  * Does it work for users with cognitive processing limitations?
  * Are all copy and visuals acceptable across cultures?
* Are there any internationalization or localization concerns?
  * Are all strings localized?
  * Do numbers, dates, times, currencies, etc use proper formatting utilities for alternate locales?
  * Do interfaces work properly with RTL locales?


## Financial Contributions

If you want to make a financial contribution, you can support Eterna's work by making a donation.
- To make a personal, tax-deductible donation to the Eterna research fund, administered by Stanford University,
  visit https://give.stanford.edu/med/fund/?kwoDCFilter=KDC-3G8MQ45&kwoDCPreselect=KDC-3G8MQ45&olc=14209
- If you wish to support our longer-term projects through through a large gift,
  please contact [Eterna's principal investigator](mailto:rhiju@stanford.edu) or the
  [Stanford development office](mailto:medicalgiving@stanford.edu).
