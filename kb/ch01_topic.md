# Themenblock 1A — Nyquist-Stabilitätskriterium

## Source
- Official University of Stuttgart handout `H-1-Nyquist.pdf`, version 4572.3.4, **4 pages**; original located in ChatGPT Library `/Regelungstechnik/`.
- First teaching unit: **page 1**. Pages 2–4 have only been indexed, not yet taught/assessed.

## Page-by-page source map
| PDF page | Original content | Key items |
|---|---|---|
| 1 | Nyquist criterion, Fig. 1; auxiliary lemma | Open/closed loop; G=G0/(1+G0); rotation around (-1,0); m0, a0; polynomial phase change |
| 2 | Proof of auxiliary lemma, Fig. 2 | Left-half-plane roots positive rotation; right-half-plane roots negative rotation; complex-conjugate pairs |
| 3 | Fig. 3 and Nyquist proof | Translation from -1 to 0; characteristic polynomial Z0+N0; mg |
| 4 | Conclusion and remarks | Delta phi = m0*pi - mg*pi when a0=0; imaginary-axis pole detours; critical-point intersection excludes asymptotic stability |

## Chinese explanation — PDF page 1
### Fundamental problem
Nyquist tests asymptotic stability of the **closed loop** by inspecting the frequency-domain locus (Ortskurve) of the **open loop**, without explicitly solving closed-loop poles.

### Figure 1: open versus negative-feedback closed loop
`Offener Kreis`: input `r` goes through `G0(s)` to output `y`.
`Geschlossener Kreis`: return the output `y` to a negative summing junction before `G0(s)`.

For unity negative feedback:
- `e(s)=r(s)-y(s)`
- `y(s)=G0(s)*e(s)=G0(s)*(r(s)-y(s))`
- Rearrange: `G(s)=y(s)/r(s)=G0(s)/(1+G0(s))`.

Here (G_0) denotes the **open-loop** transfer function and (G) the **closed-loop** transfer function.

### Page 1 theorem (Satz 1)
Let `Delta phi {G0(j omega)}` denote net phase rotation **around (-1,0)** as `omega` increases from `0` to `+infinity`. Let
- `m0`: number of open-loop poles in the open right half-plane `Re(s)>0`;
- `a0`: number of open-loop poles on the imaginary axis `Re(s)=0`.

Professor's stated condition for asymptotic closed-loop stability:
`Delta phi {G0(j omega)} = m0*pi + a0*pi/2`.
The actual interpretation relies on its specified half-frequency traverse and treatment of imaginary-axis poles (comment on page 4). Do not silently replace it with a full-contour winding-count convention.

### Why (-1,0) is critical
`G(s)=G0(s)/(1+G0(s))`: the denominator is `1+G0`. When `G0(j omega*)=-1`, the characteristic expression `1+G0(j omega*)=0`. The handout on page 4 calls this the boundary between stability and instability (imaginary-axis closed-loop root). Note: the **phase rotation relative to -1** is not simply the ordinary phase `arg G0(j omega)` relative to the origin.

### Page 1 auxiliary lemma (Hilfssatz 1)
If `P(j omega)=a*product_i(j omega - s_i)` is a degree `n` polynomial with no roots on the imaginary axis, and `n_plus` of its roots lie in the right half-plane, the net positive-frequency phase rotation around the origin is
`Delta phi_(0,0) {P(j omega)} = (n-n_plus)*pi/2 - n_plus*pi/2 = (n-2*n_plus)*pi/2`.
This is a premise of the proof developed on page 2. Each real LHP factor contributes `+pi/2` and each real RHP factor contributes `-pi/2`; conjugate pairs together give `+pi` or `-pi`. See original figure 2 on page 2.

## Problems to recognize
| German wording | Recognition | First action |
|---|---|---|
| `Stabilität des geschlossenen Kreises` | Test closed-loop stability | Determine open-loop pole counts and Nyquist trajectory |
| `Phasendrehung um (-1,0)` | Net winding relative to critical point | Use vector `1+G0(j omega)`, not `G0` about origin |
| `Pole in der rechten Halbebene` | Count `m0` | Inspect roots of the open-loop denominator |
| `Pole auf der imaginären Achse` | Count `a0` | Include imaginary-axis-pole correction; consult page 4 |

## Understanding checks — pending user answer
1. In unity negative feedback, why is the closed-loop denominator `1+G0`?
2. What does `m0` count, and is `a0` the same thing?
3. Why should the Nyquist rotation be considered around `(-1,0)` rather than the origin?

## Status
**NOT_STARTED / teaching delivered, assessment pending**. No independent student response yet; do not upgrade to PASS.
