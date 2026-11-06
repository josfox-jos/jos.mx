# jos.mx — the public landing page of the .jos open standard

This repository holds the static site that introduces `.jos` to people who have never heard of it: one page, one idea, one next step.

**The idea it has to land in ten seconds:** an AI agent should receive a contract, not a wish. A `.jos` document states the objective, the checks that prove it was met, and the limits it must stay within, in plain JSON that any tool can read and no tool can execute by accident.

**The next step it offers:** install the command line (`npm install -g @josfox/jos`), validate an example, and read the specification.

## What the page must always say (and where each claim comes from)

| Claim on the page | Source |
|---|---|
| `.jos` is an open JSON format for declaring an intention | Specification `README.md` |
| Media type `application/vnd.jos+json`, IANA ticket #1460136, pending | Specification `IANA.md` |
| Current version 2.0.0; 1.0.0 documents stay valid | Specification `README.md` and `CONFORMANCE.md` |
| Two reference kernels pass 279 of 279 conformance vectors | Specification `README.md`, measured 2026-10-22 |

The version shown on the page must match the latest tag of the specification. A page that shows any other version is a bug.

## Deploy

GitHub Pages serves the root of `main`; `CNAME` holds `jos.mx` and `.nojekyll` keeps the files as they are. There is no build step and no hosting account: a merge to `main` is the deploy.

| File | Role |
|---|---|
| `index.html` | the landing page |
| `releases.json` | the public source of truth of every published version (name, version, date, registry, url, sha256); a release hook appends to it and the page renders it |
| `run/index.html` | the no-account carrier page for `jos+open://` links: shows the proposal, never runs anything |
| `404.html` | not found |

The staged copy of these files lives in `site/` of the coordination repository until the owner applies it.

## Where the landing page sends people

**The open standard**
- [Start with the .jos community front door](https://github.com/josfox-jos/jos) — quick start, packages and paths for every kind of reader.
- [Read the 2.0.0 specification, schemas and test kit](https://github.com/josfox-jos/jos-spec) — everything the landing page promises, in normative form.
- [See the original 0.0.7 format draft](https://github.com/josfox-ai/jos-format-spec) — useful if you still hold early `.jos` files.
- [Follow `.jos` over the Agent2Agent protocol](https://github.com/josfox-ai/A2A.jos) — the transport side of the contract.
- [Explore the A2A JavaScript SDK fork](https://github.com/josfox-ai/.jos-a2a-js) — the code base for `.jos` ↔ A2A in JavaScript.

**Built by JOSFOX**
- [Open the JOSFOX AI app with one call](https://github.com/josfox-ai/josfoxai-deep-link) — the deep-link helper for JOSFOX web pages.
- [Deep-link name reserved under josfox-jos](https://github.com/josfox-jos/josfoxai-deep-link) — points to the helper above.

Site maintained by JOSFOX LLC for the `.jos` community. A LICENSE file (Apache-2.0, matching the specification code) ships together with this README; see `APPLY.md`.

## Public platform documentation — expanded ecosystem

For readers of `josfox-jos/jos.mx`, distribution status per platform is documented in one public hub; its existence does not imply a downloadable artifact or verified host compatibility.

- For readers of `josfox-jos/jos.mx`, [jos-omni](https://github.com/josfox-ai/jos-omni) provides distribution documentation hub.
