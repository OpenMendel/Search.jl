# Search
This [Julia](http://julialang.org/) package performs function optimization. Search permits bounds and linear constraints to be imposed on parameters and, in statistical applications, computes asymptotic standard errors and correlations of parameter estimates. It is one component of the umbrella [OpenMendel](https://openmendel.github.io) project.

[![](https://img.shields.io/badge/docs-current-blue.svg)](https://OpenMendel.github.io/Search.jl)

## Installation

*Note: Three OpenMendel packages - [SnpArrays](https://github.com/OpenMendel/SnpArrays.jl), [Search](https://github.com/OpenMendel/Search.jl), and [MendelBase](https://github.com/OpenMendel/MendelBase.jl) must be installed before any Mendel analysis packages will run.*

Within Julia, use the package manager to install Search:

    Pkg.clone("https://github.com/OpenMendel/Search.jl.git")

This package supports Julia v0.4.

## Running the Analysis

To run this analysis package, first launch Julia. Then load the package with the command:

     julia> using Search

Next, if necessary, change to the directory containing your files, for example,

     julia> cd("~/path/to/data/files/")

Finally, To call Search, you should start with the code
include("search.jl")

	using ParameterData
	using Optimize
	keyword = Dict{ASCIIString, Any}()
	keyword = optimization_dictionary(keyword)
	outfile = "Search.out"
	io = open(outfile, "w")
	keyword["output_unit"] = io
	
## Citation

If you use this analysis package in your research, please cite the following reference in the resulting publications:

*Lange K, Papp JC, Sinsheimer JS, Sripracha R, Zhou H, Sobel EM (2013) Mendel: The Swiss army knife of genetic analysis programs. Bioinformatics 29:1568-1570.*

<!--- ## Contributing
We welcome contributions to this Open Source project. To contribute, follow this procedure ... --->

## Acknowledgments

This project is supported by the National Institutes of Health under NIGMS awards R01GM053275 and R25GM103774 and NHGRI award R01HG006139.
