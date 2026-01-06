# GAM : ```G```enetic ```A```ssortative ```M```ating



This repo hosts the code use to estimate Genetic Assortative Mating from inferred parental haplotype data. The method is described in our manuscript:

[Hofmeister, R.J. et al. Parental haplotypes reconstruction in up to 440,209 individuals reveals recent assortative mating dynamics. BioRxiv 2025. https://doi.org/10.1101/2025.09.24.678243](https://www.biorxiv.org/content/10.1101/2025.09.24.678243v1)


## Rationale
Assortative mating, that is, the tendency for individuals to select partners with similar characteristics, leaves detectable imprints in an individual’s genome: when parents are genetically similar for a trait, the alleles they transmit tend to align more than expected under random mating, resulting in similar distributions of trait-associated alleles on the maternal and paternal haplotypes. Consequently, PGS computed from the two parental haplotypes of an individual are expected to correlate. Exploiting this phenomenon, we can estimate GAM by correlating maternal and paternal haplotype-based PGS across individuals.

## Pipeline overview
Instead of using two individual forming a mate-pair to estimate GAM by correlating their PGS, we use the two haplotypes of the same individual as proxy for paternal and maternal genomes. The mate-pair is then formed by the haplotype 1 and the haplotype 2 of the same individual. Practically, it means that, for each individual, we will use haplotype 1 and haplotype 2 as if these were two different individuals, effectively proxying half of each parental genomes.

- step 1 : inferring and separating parental haplotypes. This is performed using the [THORIN tool]()
- step 2: computing haplotype-based PGS
- step 3: estimating GAM by correlating haploid-PGS


A full tutorial is available at [https://rjhfmstr.github.io/THORIN/docs/tutorials/gam_pipeline.html](https://rjhfmstr.github.io/THORIN/docs/tutorials/gam_pipeline.html)





## Citation

- If you use ```THORIN``` in your research work, please cite the following papers:

	[Hofmeister, R.J. et al. Parent-of-Origin inference for biobanks. Nature Communication 2022. https://doi.org/10.1038/s41467-022-34383-6](https://www.nature.com/articles/s41467-022-34383-6)

	[Hofmeister, R.J. et al. Parent-of-origin effects on complex traits in up to 236,781 individuals. Nature 2025. https://doi.org/10.1038/s41586-025-09357-5](https://www.nature.com/articles/s41586-025-09357-5)


- If you use our ```GAM pipeline```, please cite in addition the following preprint:

	[Hofmeister, R.J. et al. Parental haplotypes reconstruction in up to 440,209 individuals reveals recent assortative mating dynamics. BioRxiv 2025. https://doi.org/10.1101/2025.09.24.678243](https://www.biorxiv.org/content/10.1101/2025.09.24.678243v1)




## Documentation

- Documentation, installation instructions and tutorials for ```THORIN``` can be found at:

	[https://rjhfmstr.github.io/THORIN/](https://rjhfmstr.github.io/THORIN/)


- A detailed pipeline for the haplotype-based GAM estimation is available at:
	[https://rjhfmstr.github.io/THORIN/docs/tutorials/gam_pipeline.html](https://rjhfmstr.github.io/THORIN/docs/tutorials/gam_pipeline.html)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details






