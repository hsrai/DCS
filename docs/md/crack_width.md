---
title: "Flowchart — Crack-width calculation (IS 456:2000 Annex F)"
---

<!-- Include Mermaid from CDN (works on GitHub Pages if you allow the script in your page layout) -->
<script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>

# Calculation of Crack Width — Flowchart (IS 456:2000, Annex F)

This page shows a step-by-step flowchart to calculate the **design surface crack width** for a flexural member using the method given in **IS 456:2000 — Annex F** (Clauses 35.3.2 and 43.1). The formulae used (and assumptions) are from IS 456:2000. See citation below. :contentReference[oaicite:0]{index=0}

```mermaid
flowchart TD
  A[Start — Inputs] --> B[Material properties\n• f<sub>ck</sub> (N/mm²)\n• E<sub>c</sub> = 5000·√f<sub>ck</sub> (N/mm²)\n• E<sub>s</sub> = 200000 N/mm²]
  B --> C[Section and reinforcement\n• b, h, d (mm)\n• As (area of tension steel)\n• a<sub>sc</sub> = distance from point to nearest longitudinal bar\n• C<sub>min</sub> (min cover)\n• bar centroid position (to get b at centroid)\n• applied service moment M<sub>ser</sub> or forces]
  C --> D[Compute transformed/cracked properties\n• Compute neutral axis depth x (cracked section) — use cracked-section equilibrium / IS procedure]
  D --> E[Compute curvature/strain\n• Find ε₁ = strain at level considered (ignoring tension stiffening)\n  — from cracked section: ε₁ = curvature × distance (or from M / (E<sub>c</sub>·I<sub>cr</sub>) × (d - a) ) ]
  E --> F[Compute average steel strain ε<sub>m</sub>\n(using Annex F approximation)]
  F --> G[Compute design surface crack width w<sub>s</sub>\n(using Annex F equation)]
  G --> H[Compare w<sub>s</sub> with allowable limits (Clause 35.3.2)\n• Mild: 0.3 mm\n• Moderate: 0.2 mm\n• Severe/aggressive: 0.1 mm]
  H --> I{w<sub>s</sub> ≤ allowable?}
  I -->|Yes| J[Accept design\n— record w<sub>s</sub>, location, inputs]
  I -->|No| K[Modify design\n— increase reinforcement / reduce spacing\n— increase cover or change detailing\n— re-check]
  J --> L[End]
  K --> L
