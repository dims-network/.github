# DIMS-network

**Open tools for exploring dynamic interaction and multimodal signals in
social-interaction research.**

A DIMS dashboard puts video, time series, transcripts and annotations in one
place, against one shared clock, so that qualitative and quantitative readings
of an interaction can sit beside each other — recurrence quantification,
cross-recurrence, cross-wavelet coherence, a cross-effector network and ELAN
annotations included. Coherence is read against a chance level estimated by
simulation: two unrelated signals score about 0.25, not 0, so a number without
that comparison cannot be interpreted.

---

## How it is organised

One repository holds all the code. Each study is a small repository of its own,
holding its configuration, its data, and a **pinned copy** of that code —
verified against the release in CI, so a study can never quietly fork.

| | | |
|---|---|---|
| [**dims**](https://github.com/dims-network/dims) | the core — dashboard, tabs, Python analyses, no-code builder | everything else pins a release of this |
| [**case-demo**](https://github.com/dims-network/case-demo) | the reference study, with real data — rebuilt on each release | [live](https://dims-network.github.io/case-demo/) |
| [**dims-dashboard-demo**](https://github.com/dims-network/dims-dashboard-demo) | the same study, frozen at 1.0.0 and self-contained: it opens with no network and does not move | [live](https://dims-network.github.io/dims-dashboard-demo/) |
| [**case-ortho**](https://github.com/dims-network/case-ortho) | ORTHO — a two-person tabletop game | [live](https://dims-network.github.io/case-ortho/) |
| **case-karnatak** | Karnatak music lessons | private: the recordings are identifiable |
| [**dims-network.github.io**](https://github.com/dims-network/dims-network.github.io) | the site, generated from the core's markdown | |




## Working with human-subject data

Much of this data is video of identifiable people. A study declares its
visibility once, in `dims-case.json`, and the declaration is enforced by
machinery rather than by memory: a commit hook, a push hook, and a CI check that
fails if restricted data is tracked — or if a study declaring itself private is
in a public repository. See
[public and private data](https://dims-network.github.io/docs/data-visibility.html).

## Contributing

Issues labelled **`ready`** name the files, link the contract and state the
acceptance check, so one can be picked up without any other context. Start from
[the core's README](https://github.com/dims-network/dims#working-on-dims), a map
telling you which single document to read for the task you have.

## Reference

Miao, G. Q., Trujillo, J., Bulls, L. S., Thornton, M. A., Dale, R., & Pouw, W.
(2025). *DIMS Dashboard for Exploring Dynamic Interactions and Multimodal
Signals.* Proceedings of the 47th Annual Meeting of the Cognitive Science
Society (CogSci 2025).
