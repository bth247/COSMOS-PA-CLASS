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

Matched scalar/vector Cauchy entry (conditional sampled controls)
--------------------------------------------------------------

Scalar-only and vector-only fixed-a imports are now available with
massless neutrinos, photon tight coupling and the standard flat background.
Scalar rows retain CDM-comoving densities and the Newtonian clock; vector
rows carry normal velocities and TAM multipoles. The reader validates the
entire table and supplied Einstein/material constraints, rejects absent k
coverage, and preserves exact nodes. Inter-node constraint completion is
not a certification of physical transfer interpolation.

The associated project now transports six real scalar canonical columns
through IRH-0, a regular-gradient thermal bridge, conditional AD-M matter
initialization and EM-rest FD weak decoupling. Previously matched vector
columns also enter the native solver. All six scalar/four vector matched
pivot bases pass two-gauge controls. Native solid/gate UETC factors cover
the matched pivot through late evolution. Diagnostic k extensions used in
response spectra are not cosmological predictions.

The full-Limber radial-coordinate helper now receives the caller's selected
k, avoiding an out-of-bounds regular-grid access for Limber q indices.
Lensing remains enabled in scalar controls. See the versioned reports and
theory/REHEATING_SCALAR_CLASS.md in the associated repository for exact
constraints, covariance units, approximations and remaining validation.

Production k/time/multipole and vacuum coverage, coherent-flavor spectral
collisions, complete native gauge/Bianchi certification and likelihoods
remain incomplete. Earlier missing-feature statements above are historical.


Radiation hierarchy validation update
------------------------------------
Matched-state audits expose late-time gauge/constraint errors from the
default radiation streaming/fluid closures. Scalar/vector Cauchy imports
now require radiation_streaming_approximation=3 and ur_fluid_approximation=3.
An explicit cosmos_cauchy_radiation_control=yes override exists only to
replay unvalidated diagnostic controls. It does not certify those closures.

The main project retains the rejected controls and full-hierarchy finite
gauge/conservation refinement, including the hierarchy-cutoff comparison.
Full production all-k/flavor/Bianchi validation remains incomplete.
