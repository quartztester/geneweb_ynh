GeneWeb is a genealogy software with a web interface, developed in France since 1998. It stores families in separate bases, displays ascendance, descendancy, nuptiality and consanguinity computations, and imports and exports GEDCOM files.

The app consists of two daemons: `gwd` (browse the bases) and `gwsetup` (create bases and import GEDCOM files). Both are proxied by nginx and gated by YunoHost permissions instead of in-app accounts.
