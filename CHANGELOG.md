# FerriteViz.jl changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
 - Crincle clip in 3D [#56](github-56), which basically removes all elements above some surface,
   which can be described by a function, from visualization.
 - `ClipPlane` to describe planar surfaces in 3D [#56](github-56).
 - Docs and helper for gradient field visualization based on interpolation [#51][github-51].
   Currently only useful in 2D, because we have no clip plane feature to introspect the interior
   of 3D problems.
 - Manufactured heat problem to test correctness of gradient field computation and as a
   helper to generate scalar-valued solutions with different ansatz [#51][github-51].

### Modified
 - Incompressible elasticity solver now takes the Ansatz functions and the actual material
   parameters instead of the poisson number the Ansatz functions [#51][github-51].

### Fixed
 - An unknown bug has been fixed, which computes the colorbar `(min,max)` wrong. Now the `max` is
   set to be `1.01` of `min` guaranteeing that the value is larger than `min` if close to zero [#51][github-51].
 - Update Makie dependencies to fix some visualization bugs [#51][github-51].

## PRs
* [github-51](https://github.com/Ferrite-FEM/Ferrite.jl/pull/51)
* [github-56](https://github.com/Ferrite-FEM/Ferrite.jl/pull/56)