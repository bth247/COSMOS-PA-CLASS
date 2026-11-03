# COSMOS native CLASS prototype — experimental

Base: official CLASS v3.4.1, 814ce59c380a5cccd0bed1747a384ff7bfc1f9cf.
This branch adds a distinct solid/gate background and scalar response,
dynamical tensor gate response, tensor stress diagnostics, and a gate-frequency
initial-series start-time check. It is NOT the completed IRH-0 native model.

Vectors and independent stochastic gate primordial modes are NOT implemented.
Nonzero Omega_cosmos with vector modes is explicitly rejected. Scalar/tensor
runs only test responses to existing primordial metric modes. They must NOT
be used as native gate observational predictions or for likelihood fitting.

Reproducible installers, full patch, numerical controls, derivations, IRH-0
prescription, and validation boundaries live in:
https://github.com/bth247/COSMOS-PA/tree/main/native
https://github.com/bth247/COSMOS-PA/blob/main/STATUS.md

See native/tensor/README.md there for the tested controls and normalization.
The original CLASS license and attribution remain intact.
