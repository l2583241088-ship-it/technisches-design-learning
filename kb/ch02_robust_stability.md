# Themenblock 1B — Robustheit der Stabilität

## Source
University of Stuttgart handout `H-1-Robuste_Stabilitaet.pdf`, version 4572.7.2, **1 page**; original saved in ChatGPT Library `/Regelungstechnik/`. Indexed but **not yet taught**.

## Source-faithful map (PDF page 1)
- `Robuste Stabilität`: closed-loop stability persists despite deviations of the true open-loop transfer function from the model due to model uncertainty or disturbances.
- `Amplitudenreserve a_r` (gain margin): factor by which actual plant gain can differ from model before instability occurs; the handout normally expresses the margin as an interval.
- `Phasenreserve gamma_r` (phase margin): acceptable phase deviation before instability; generally report magnitude of the smaller interval bound.
- Figure 1 shows Nyquist locus `G0(j omega)`, unit circle, critical point `(-1,0)`, and margin geometry.
- The handout specifies phase margin as angular difference between -180° and the phase at unity-gain crossover: `|G0(j omega_D)|=1`. Easy to read from Bode diagram.

## Notes
No external margins, numerical examples, or exam requirements have been inserted. Return to this document after completing Nyquist page 1–4.
