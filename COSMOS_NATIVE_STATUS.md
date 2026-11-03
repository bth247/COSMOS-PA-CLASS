# Experimental COSMOS native SVT response

Base: official CLASS v3.4.1, 814ce59c380a5cccd0bed1747a384ff7bfc1f9cf.
This branch implements the solid background and scalar, vector and tensor
response equations, with metric coupling and state/stress diagnostics.
It is NOT a validated IRH-0 primordial gate prediction solver.

Vector updates include gauge-invariant normal velocity/strain/gate states,
a correction for duplicated upstream Newtonian initial velocity shifts,
a common gauge-invariant line-of-sight source representation, a massless
finite-time momentum-constraint projection, and consistent photon TCA stress.
Flat-space independent finite-time vector gate bases are available for
post-decoupling transfer/UETC controls. These are NOT reheating matching.

Independent inflationary gate mode preparation, thermal neutrino decoupling,
full IRH-0 matching, massive-neutrino vector constraint certification,
production convergence, and likelihood predictions remain incomplete.
Spatial curvature with the COSMOS vector species is explicitly rejected.

Code installers, derivations, tests, source pins, and numerical controls:
https://github.com/bth247/COSMOS-PA/tree/main/native
Current scientific status:
https://github.com/bth247/COSMOS-PA/blob/main/STATUS.md

No native likelihood fitting is enabled. Original CLASS attribution and
license remain intact.

Tensor Cauchy ingestion is now available for flat, tensor-only TAM runs
with massless ur and positive Omega_cosmos. Input supplies h,h_N,Q,Q_N
and neutrino Theta_2..Theta_lmax at one fixed scale factor. Strict log-k
interpolation rejects absent/out-of-range/malformed requested data; no
initial Taylor series or stock neutrino quadrupole replaces the supplied
state. A fixed-a time locator aligns the integration and source grids.

The associated project computes CONDITIONAL reheating-matched tensor
covariances through a conserved thermal join and weak decoupling. The
native adapter retains the inferred canonical r as a reference weight,
with the actual covariance carried by the initial basis data. Numerical
reference shape/amplitude are divided out, not fitted independently.

This does not complete scalar/vector decoupling transport, spectral/flavor
QKE evolution, all-k interpolation convergence, massive-neutrino handoff,
or production Einstein/Bianchi/gauge validation. Likelihoods remain disabled.
