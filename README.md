# Spec: Specification Repository v0.0.0

This repository contains the specification norming the structure, contents and versioning of Uqido Specification Repositories (yeah, a recursively defined spec :)!).

## Adoption Impact

The goal of any effective technical documentation—or any team-produced artifact, for that matter—is to create impact by influencing behavior in ways that lead to value creation.
To understand the impact of specifications, it's important to clarify the difference between a specification and a guideline document.

More specifically, in contrast to a guideline document, a specification:
- it's adoptable: you can *choose* to claim that a given software component *respects* a spec, whenever appropriate for *that* component, team, project, etc... .
- it's versionable: you can *evolve* a spec without impacting existing adopters.
- it's composable and extendable: you can create new specs by summing or extending existing specs (the usual caveats of composition and extension obviously apply!).
- it's reviewable: you can referer to clear normative content to check compliance and promote the spec, manually or via AI agents.
- it's measurable: you can measure the value of a spec by monitoring its adoption rate, assuming a virtuous team behaviour.
- it's AI friendly: you can use it as effective contexts for AI agents with reasoning capabilities.

Therefore, when clear, measurable, and repeatable patterns of impact emerge, you can create and adopt a specification to operate more effectively 
within that domain or project scope.

## Normative Content

A specification consists of a GitHub repository along with a standard set of documents and optional support material—such as support toolchain, 
recipes, etc...—following the conventions specified in this section.

Specification rules used in this document are borrowed from a well-regarded, best practice coding guideline from our good ol' buddy Bjarne Stroustrup
(https://www.stroustrup.com/JSF-AV-rules.pdf FYI, always worth a reading BTW :)):

There are three types of rules: **should**, **will**, and **shall** rules.

Each rule contains either a “should”, “will” or a “shall” in bold letters indicating its type.
- Should rules are advisory rules. They strongly suggest the recommended way of doing things.
- Will rules are intended to be mandatory requirements. It is expected that they will be followed, but they do not require verification. They are limited to
non-safety-critical requirements that cannot be easily verified (e.g., naming conventions).
- Shall rules are mandatory requirements. They must be followed and they require verification (either automatic or manual).

### Naming Conventions

The repo name **will** have the form "spec-some-recognizable-sensible-name".
Documentation material **shall** be written in `md` format with snake_case naming convention.
Non-mandatory, technology specific material may have different naming conventions.

### Versioning and Distribution

Specs **shall** follow semver 2.0 versioning; each version **shall** have a tag of the form v`semver`, any semver format is allowed (see https://semver.org/).
Specs are distributed via *links* to their tags, hence the version reported in this README and throughout the spec documentation **will** be consistent with the tag it lives in.

### Spec Repository Structure

A spec **shall** contain at least:
- a README.md
- a Apache License Version 2.0 LICENSE file

It may also contain directories with support material used to ease spec adoption, including scripts, recipes, examples etc... .
In any case, such support material is *not* intended as a mean for hosting libraries or other reusable code components; these
should live in dedicated repos: spec repositories **should** be dependency free and lightweight to link and clone.

The README.md **shall** follow the structure in the spec_template.md file.
