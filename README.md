# Versions

Schemes have now been separated via length, for ease of use. So, the classic 400bp v5.0.0 scheme is now designated as v5.0.0_400 (See Versioning) and is found in the "400s" directory. The major and minor version refer the mask used in the scheme generation, so for example, all v5.2.0 schemes will cover the same variants regardless of Amplicon length.

## v5.0.0

(01-05-2021)

A mask for designed for prevalent subvariants<sup>\*1</sup> at time of creation.

<sup>\*1</sup> (AY.103, AY.122, AY.20, AY.25, AY.39.1, AY.39.1.1, AY.4, AY.4.2, AY.4.3, AY.9, B.1.1.318, B.1.1.529, B.1.1.7, B.1.617.1, B.1.351, P.1)

## v5.1.0

(02-10-2022)

An updated version of v5.0 to include variants; BA.2.3, BA.4.1, BA.5, BA.5.1, BA.5.2, BA.5.2.1, BA.5.6

## v5.2.0

(17-10-2022)

An updated mask version of v5.1 to include BQ.1

## v5.3.2

(09-12-2022)

A balanced, replacement version of the v5.2 scheme, including primers replacements to fix a gap region around Amplicon 7. This includes all variants covered in previous v5 schemes. Also includes pooling information for generating balanced Amplicon coverage.

## File Format

`MN908947.3.fasta`: The reference genome used in the bed file indexing

`nmask.fasta`: The nmask with positions of variation masked via an N

`<version>.primer.bed`: The bedfile that contains the primers of the current version

`pooling`: How to make up the pool from 100uM primer stocks.

### Optional Files

`add.primer.bed`: New primers added in a subversion increase (v5.1.0 to v5.2.0)

`total_add.primer.bed`: New primers needed to create a version from the base (v5.0.0)

### Pooling File

This is how to create a pool from primers stocks

Columns are in order;

`primer_name`: The name of each primer

`pool`: The pool each primer belongs to

`amplicon`: The amplicon each primer contributes to

`primer_number`: This allows multiple primers to contribute to the same amplicon. The base primer is numbered 0, with each new alt sequentially increasing

`weight`: The ratio between primer concentration within its pool, and its amplicon's coverage. When pooling this can stand in for uL of each primer.

`uL_to_make_100uL`: If X amount of each primer at 100uM is added to its corresponding pool, both pools stocks will will come to 100uL

delta_rebalance is how to create a minor version from the base version (create v5.2.0 from v5.0.0)

## Versioning

v(w).(x).(y)\_(z)

`w`: Major Version. (New scheme)

`x`: Minor Version. Used to include new alt primers to account for new lineages (Changes to the primers)

`y`: Misc version. Used to include changes to file format or change to primer re-balancing volumes (No primer changes)

`z`: The max length of the scheme in base pairs
