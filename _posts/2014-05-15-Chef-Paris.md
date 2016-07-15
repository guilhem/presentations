---
layout: reveal
title: Chef-Paris Infrastructure as open-source code
---

<section data-markdown data-separator="^\n---\n$" data-separator-vertical="^\n--\n$" data-notes="^Note:">

# Infrastructure as open source code

--

## How to use open source components in my infrastructure

--

### Mainly how to survive with community

---

## /me

* Ops
* CI Consultant
* Systems Architect
* DevOps


Us Chef for 2 years

--

## collaborator: ≏ 10 cookbooks

--

## owner: ≏ 30 cookbooks

--

# contributor

![over 9000](http://img3.wikia.nocookie.net/__cb20130708051812/cardfight/images/7/7b/It-s-over-9000-its-over-9000-29849302-496-370.jpg)

---

# Why Open source?

- You are using free software, why not free scripts
- Share work (and tests) across a large community
- Community go fast, you are in or it make you out

---

# Organization

## tl;dr

- think as library
- split your cookbooks
- don't reinvent wheel

--

## Your infrastructure

Look like any other.
You are using same software as anybody else.

Sorry... your are not special.

--

## Your software

Even if your code is unique, you are using more "public" code (database, HTTP server, framework...)

--

## Slip as much as possible

Identify actions specific to you and those your ex-coworker can also do in their new company.

--

## 3 types of cookbooks

- Installation:
  - Mysql
  - Apache
  - ...
- Tool:
  - hostname
  - htpasswd
  - ...
- Wrapper

Note: can be a mix of those

---

# How-to

## tl;dr

- community site (futur supermarket)
- dependencies (berkshelf!!)

--

## Community sites

Identify best cookbook:

- features
- testing
- openness
- contributions
- authority

Note: any other?

--

## Use Strong dependencies

- Berkshelf

Note: or librarian-puppet...

--

## Workflow

In your "root" cookbook:

- Identifies your dependencies (in `metadata.rb`)
- Create dependency tree
- Test

Note: redo. Use `kitchen` tool

---

![# Run like hell](http://nursestat.org/images/in%20case%20of%20energency%20Run.png)

## tl;dr

- Fork
- PR
- Pray

--

## Case of failure

- Exotic platform (openbsd? MacOS? Windows?..)
- Can't set featureIlove®
- Dependency refactored
- New incompatible version

Note: any other?

--

## Patch them all!

- Manage your fork with berkshelf
- patch
- add tests
  - and run tests...

--

## Contribute

- Do a PR
- Explain why you are doing this
  - And answer maintainer's questions
- Rebase often with master

--

## If doesn't work... you may have bad time

---

# To be maintainer (or not to be)

## TL;DR

- Know that you don't know

--

## Like any other own cookbook

plus:

- strong test
- Public CI integration
- Good documentation

--

## Try to do as modular as possible

It limit PR and review work.

Pro-tip: Don't match any option but try to auto-generate conf from attributes.

--

## try to create a community to help you

2 or 3 contributors is a good number.

--

## Community work belongs to community

Don't be afraid to leave a cookbook when you don't use it anymore.

Note: give it to someone before!

---

# Thank you

## Questions?

##### or hey I need some bastard names
