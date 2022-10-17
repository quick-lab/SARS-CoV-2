#[5.0.0](https://github.com/quick-lab/nCOV19)(01-05-2021)

A verified 400bp scheme for designed for prevalent subvariants<sup>*1</sup> at time of creation. 

#[5.1.0](https://github.com/quick-lab/nCOV19)(01-05-2021)

An updated version of v5.0 to include variants; BA.2.3, BA.4.1, BA.5, BA.5.1, BA.5.2, BA.5.2.1, BA.5.6

#[5.2.0](https://github.com/quick-lab/nCOV19)(01-05-2021)

An updated version of v5.1 to include BQ.1


<sup>*1</sup>
(AY.103, AY.122, AY.20, AY.25, AY.39.1, AY.39.1.1, AY.4, AY.4.2, AY.4.3, AY.9, B.1.1.318, B.1.1.529, B.1.1.7, B.1.617.1, B.1.351, P.1)

## File Format
```MN908947.3.fasta```: The referance genome which is used in the bed file indexing

```nmask.fasta```:  The nmask with positions of vairation masked via an N

```nCOV19_400.primer.bed```:  The bedfile that contains the primers of the current version

```add.primer.bed```: New primers added in a subversion increase (v5.1.0 to v5.2.0)

```total_add.primer.bed```: New primers needed to create a version from the base (v5.0.0)

