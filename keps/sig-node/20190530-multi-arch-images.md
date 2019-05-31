---
title: Multi-arch container image support
authors:
  - "lachie83@"
owning-sig: sig-node
participating-sigs:
  - TBD
reviewers:
  - TBD
approvers:
  - TBD
editor: TBD
creation-date: 2019-05-30
last-updated: 2019-05-30
status: provisional

---

# Multi-arch container image support

## Table of Contents

A table of contents is helpful for quickly jumping to sections of a KEP and for highlighting any additional information provided beyond the standard KEP template.
[Tools for generating][] a table of contents from markdown are available.

- [Title](#title)
  - [Table of Contents](#table-of-contents)
  - [Release Signoff Checklist](#release-signoff-checklist)
  - [Summary](#summary)
  - [Motivation](#motivation)
    - [Goals](#goals)
    - [Non-Goals](#non-goals)
  - [Proposal](#proposal)
    - [Risks and Mitigations](#risks-and-mitigations)
  - [Design Details](#design-details)
    - [Test Plan](#test-plan)
    - [Graduation Criteria](#graduation-criteria)

[Tools for generating]: https://github.com/ekalinin/github-markdown-toc

## Release Signoff Checklist

- [ ] kubernetes/enhancements issue in release milestone, which links to KEP (this should be a link to the KEP location in kubernetes/enhancements, not the initial KEP PR)
- [ ] KEP approvers have set the KEP status to `implementable`
- [ ] Design details are appropriately documented
- [ ] Test plan is in place, giving consideration to SIG Architecture and SIG Testing input
- [ ] Graduation criteria is in place
- [ ] "Implementation History" section is up-to-date for milestone
- [ ] User-facing documentation has been created in [kubernetes/website], for publication to [kubernetes.io]
- [ ] Supporting documentation e.g., additional design documents, links to mailing list discussions/SIG meetings, relevant PRs/issues, release notes

## Summary

This proposal adds multi-arch container image support to Kubernetes clusters which allows workloads to reference container images by a single name (assuming the container image has multi-arch support) regardless of the underlying platform of the Kubernetes node.

## Motivation

As Kubernetes is supported by more and more underlying operating systems and platforms, it's becoming increasingly difficult to keep track of what container images can run on specific nodes. This results in single-arch container images being referenced by name for a specific platform which creates a cumbersome user experience that is often error prone. The introduction of this feature would allow multi-arch containers images to be referenced by a single name and the container runtime along with the registry (if supported) would serve the correct container for that platofrm. Additionally, this feature would also encourage image packagers to build and package images that support multiple platforms.

Current experience
```
```

Experience after the introduction of this feature
```
```

### Goals

### Non-Goals

## Proposal

### Risks and Mitigations

## Design Details

### Test Plan

### Graduation Criterias
