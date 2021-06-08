# perl Orb [![CircleCI Build Status](https://circleci.com/gh/CircleCI-Public/perl-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/CircleCI-Public/perl-orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/circleci/perl)](https://circleci.com/orbs/registry/orb/circleci/perl) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/CircleCI-Public/perl-orb/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

Orb for building and testing Perl distributions.

## Usage

Example use-cases are provided on the orb [registry page](https://circleci.com/orbs/registry/orb/circleci/perl#usage-examples). Source for these examples can be found within the `src/examples` directory.

## Prerequisites

Some of the jobs included in this orb have certain prerequisites:

- `perl/build` - This job assumes that your repository follows the `Dist::Zilla` pattern, where there is a `dist.ini` file which controls the build.
- `perl/test-linux` - This job assumes you have `Dist::Zilla` pattern, as well as a `cpanfile` for all dependencies.
- `perl/makefile-build` - This job assumes that you have a `Makefile.PL` build process, depending on `ExtUtils::MakeMaker`.

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/circleci/perl) - The official registry page of this orb for all versions, executors, commands, and jobs described.  
[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.

### How To Contribute

We welcome [issues](https://github.com/CircleCI-Public/perl-orb/issues) to and [pull requests](https://github.com/CircleCI-Public/perl-orb/pulls) against this repository!

To publish a new production version:

- Create a PR to the `Alpha` branch with your changes. This will act as a "staging" branch.
- When ready to publish a new production version, create a PR from `Alpha` to `master`. The Git Subject should include `[semver:patch|minor|release|skip]` to indicate the type of release.
- On merge, the release will be published to the orb registry automatically.

For further questions/comments about this or other orbs, visit the Orb Category of [CircleCI Discuss](https://discuss.circleci.com/c/orbs).
