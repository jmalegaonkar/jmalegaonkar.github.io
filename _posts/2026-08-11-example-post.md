---
layout: post
title: "Example post: writing in Markdown with math"
math: true
---

This is the post template — plain Markdown. Write prose in paragraphs,
use `**bold**`, `*italics*`, and [links](https://example.com) as usual.

One kramdown quirk: **inline math also uses double dollar signs**, like
$$\pi(a \mid s)$$ or $$\mathbb{E}[X] = \sum_x x\, p(x)$$ — kramdown tells
inline from display apart by context.

Display math is a `$$` block on its own lines:

$$
V^\pi(s) = \mathbb{E}_\pi \left[ \sum_{t=0}^{\infty} \gamma^t \, r(s_t, a_t) \,\middle|\, s_0 = s \right]
$$

## Sections

Use `##` for section headings. A Nash equilibrium is a strategy profile
$$\sigma^* = (\sigma_1^*, \ldots, \sigma_n^*)$$ such that for every player
$$i$$,

$$
u_i(\sigma_i^*, \sigma_{-i}^*) \ge u_i(\sigma_i, \sigma_{-i}^*) \quad \text{for all } \sigma_i.
$$

## References

1. Author, A. *Title of the work*. Venue, Year.
