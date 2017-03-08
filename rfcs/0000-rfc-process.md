* Feature Name: rfc-process
* Start Date: 2017-02-12
* Author: zimbatm
* Co-Authors: teh, MoreTea
* RFC PR:
* Related Issue:

# Summary
[summary]: #summary

The "RFC" (request for comments) process is intended to provide a consistent
and controlled path for new features to enter the nix language, packages and
OS, so that all stakeholders can be confident about the direction the
ecosystem is evolving in.

This RFC is used as a bootstrap to the process. Further RFCs can be used to
refine the process.

# Motivation
[motivation]: #motivation

There are a number of changes that are significant enough that they could
benefit from wider community consensus before being implemented. Either
because they introduce new concepts, big changes or are controversial enough
that not everybody will agree on the direction to take.

# Detailed design
[design]: #detailed-design

Many changes, including bug fixes and documentation improvements can be
implemented and reviewed via the normal GitHub pull request workflow.

Some changes though are "substantial", and we ask that these be put through a
bit of a design process and produce a consensus among the Nix community.

This is the bulk of the RFC. Explain the design in enough detail for somebody
familiar with the ecosystem to understand, and implement.  This should get
into specifics and corner-cases, and include examples of how the feature is
used.

## When you need to follow this process

You need to follow this process if you intend to make "substantial" changes to
the Nix ecosystem. What constitutes a "substantial" change is evolving based
on community norms, but may include the following.

* Any semantic or syntactic change to the language that is not a bugfix
* Removing language features
* Big restructuring of nixpkgs
* Expansions to the scope of nixpkgs (new arch, major subprojects, ...)
* Introduction of new interfaces or functions
* A controversial change

Some changes do not require an RFC:

* Adding, updating and removing packages in nixpkgs
* Fixing security updates and bugs that don't break interfaces

If you submit a pull request to implement a new feature without going
through the RFC process, it may be closed with a polite request to
submit an RFC first.

## What the process is

In short, to get a major feature added to the Nix ecosystem, one should first
go throught the RFC process in order to improve the likelyhood of inclusion.
Here are roughly the steps that one would take:

* Fork the RFC repo https://github.com/NixOS/rfcs
* Copy `0000-template.md` to `rfcs/0000-my-feature.md` (where 'my-feature' is
  descriptive. don't assign an RFC number yet).
* Fill in the RFC
* Submit a pull request. Rename the rfcs with the PR number. (eg: PR #123 would
  be `rfcs/0123-my-feature.md`)
* Get initial feedback on the PR.

At this point, the person submitting the RFC should find at least one "co-author"
that will help them bring the RFC to completion. The goal is to improve the
chances that the RFC is both desired and likely to be implemented.

Whomever merges the RFC should do the following:

* Create a corresponding issue on the appropriate repo (NixOS/nix,
  NixOS/nixpkgs, ...).
* Fill in the remaining metadata in the RFC header, including links for the
  original pull request(s) and the newly created issue.
* Commit everything.

Once an RFC becomes active then authors may implement it and submit the
feature as a pull request to the nix or nixpkgs repo. An 'active' is not a
rubber stamp, and in particular still does not mean the feature will
ultimately be merged; it does mean that in principle all the major
stakeholders have agreed to the feature and are amenable to merging it.

## Role of the "co-author"

To goal for assigning a "co-author" is to help move the RFC along.

The co-author should:
* be available for discussion with the main author
* respond to inquiries in a timely manner
* help with fixing minor issues like typos so community discussion can stay
  on design issues

The co-author doesn't necessarily have to agree with all the points of the RFC
but should generally be satisfied that the proposed additions are a good thing
for the community.

# Drawbacks
[drawbacks]: #drawbacks

There is a danger that the additional process will hinder contribution more
than it would help. We should stay alert that the process is only a way to
help contribution, not an end in itself.

# Alternatives
[alternatives]: #alternatives

Retain the current informal RFC process. The newly proposed RFC process is
designed to improve over the informal process in the following ways:

* Discourage unactionable or vague RFCs
* Ensure that all serious RFCs are considered equally
* Give confidence to those with a stake in the Nix ecosystem that they
  understand why new features are being merged

As an alternative, we could adopt an even stricter RFC process than the one
proposed here. If desired, we should likely look to Python's [PEP] process for
inspiration.

# Unresolved questions
[unresolved]: #unresolved-questions

1. Does this RFC strike a favorable balance between formality and agility?
2. Does this RFC successfully address the aforementioned issues with the current
   informal RFC process?
3. Should we retain rejected RFCs in the archive?

[PEP]: http://legacy.python.org/dev/peps/pep-0001/