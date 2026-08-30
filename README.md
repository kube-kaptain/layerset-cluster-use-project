# Layerset Cluster Use Project

Kaptain layerset composing the quality and release configuration for projects
whose output is consumed into clusters rather than built against.

Composes these layers in order:

1. **layer-github-flow-strict**: strict GitHub flow quality enforcement (slash blocking, conventional commit blocking)
2. **layer-gh-release-how-to-use-full-only**: release notes show the fully qualified reference alone, with no org-local alternative

This layerset carries no `kind`, so it applies to any build type. Cluster-use
projects come in several shapes and none of them should be excluded by the
layerset that configures them.


## When to use this

Reach for this layerset on public packages intended for cluster consumption but
not generic build use. These types of packages are only ever consumed by other
orgs in `product-*` products, `run-*` environments, or in repackaging projects.
