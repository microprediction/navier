# navier (view as [web page](https://navier.microprediction.org))

A reader's guide to the September 2026 forced blow-up construction for the
three-dimensional Navier–Stokes equations, and to the question of whether a
fast-fluctuating fluid would reach the singularity.

## The question

OpenAI's manuscript *Finite Time Blowup for Navier–Stokes* (8 September 2026)
constructs, for every viscosity, a smooth compactly supported force under which
the flow from rest has bounded energy and unbounded velocity at time one. That is
alternative (C) of Fefferman's Clay statement, and (D) follows by periodization.
The unforced alternatives (A) and (B) are untouched.

The site follows the paper's own order (core, annulus and pulses, correction
cycle, completion) and then asks: if the equations are given thermal noise, a
molecular scale, transport noise, or a fast exogenous switch, does the constructed
singularity survive? In one case (transport noise, Agresti 2026) there is a
theorem and it does not. In the others the answer is open, and the site says why.

## Map

- **Guide**: the problem, the residual trick, scales and exponents, the core, the
  annulus and the pulses, corrections and completion, what is settled.
- **Fluctuations**: can fluctuations break it, the molecular limit (calculator),
  seeds and noise (amplification arithmetic).
- **Literature**: papers, annotated bibliography, interactive map, timeline.

## Layout

```
docs/          the site, served by GitHub Pages from main
literature/    working notes distilled from the manuscript
```

Styling is the schur/homogenization chassis, unchanged. Math via KaTeX, the map
via D3 v7, demos in plain canvas.

## Cite

```
@misc{openai2026navierstokes,
  title  = {Finite Time Blowup for Navier--Stokes},
  author = {{OpenAI}},
  year   = {2026},
  note   = {Manuscript, 166 pp., released 8 September 2026},
  url    = {https://openai.com/index/navier-stokes-solution/}
}
```

Comments and corrections welcome as issues.
