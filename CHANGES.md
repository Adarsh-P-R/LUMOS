# Changes

## 1.0.0 (2026-11-08)

First public release.

- 2D optical table with M6 holes on a 25 mm grid (or ¼"-20 on 1 inch), per-part snapping to holes, half-holes or anywhere.
- Gaussian beam tracing with q-parameters and M², Jones-vector polarisation, clipping on apertures, and AOM/AOD diffraction and frequency shifts, including double passes.
- More than 35 part types: lasers (with extra output ports), tapered amplifiers, lenses, mirrors, dichroics, windows, beam samplers, D-mirrors, flip mirrors, retroreflectors, PBS and nPBS cubes, wave plates, polarisers, isolators, Faraday rotators, AOMs, AODs, EOMs, fibre links, irises, ND filters, power meters, photodiodes, beam profilers, beam dumps, vapour cells, shutters, custom optics and translation stages.
- Fibre coupling efficiency from the overlap with the fibre mode, with Thorlabs collimators and fibres to choose from.
- Damage thresholds for every part, using quoted Thorlabs values where available, with warnings.
- Catalogue parts from Thorlabs, Gooch & Housego and Isomet, with their specifications.
- Mounting: recommended or chosen Thorlabs mounts, or custom mounts, with posts, post holders and bases picked for the beam height, a mounting view with footprints to scale, and overlap checks.
- Control tab for laser powers, wave plate angles, AOMs, shutters, flip mirrors and stages on one screen.
- Shop tab with part matches, live search links (Thorlabs, Elliot Scientific, G&H, Isomet) and CSV export.
- Locking, undo, saved setups, and setup import/export as JSON.
- Fibre splitters (e.g. 2×6), fibre couplers with light only going in, fibre outputs with light only coming out, and named fibres that link one table to another.
- Example setups: a Rb MOT laser table (cooling TA pro and repump DL pro with saturated-absorption locks, double-pass AOM, into fibres) and the matching six-beam MOT table.
- Desktop builds for Windows, macOS and Linux, and a web version.
- User manual as a PDF in `docs/`.
