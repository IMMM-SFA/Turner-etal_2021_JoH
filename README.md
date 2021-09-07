**Water storage and release policies for all large reservoirs of
conterminous United States**

Sean Turner<sup>1\*</sup>, Jennie Steyaert <sup>2</sup>, Laura Condon
<sup>2</sup>, and Nathalie Voisin <sup>1,3</sup>

<sup>1 </sup> Pacific Northwest National Laboratory <sup>2 </sup>
University of Arizona <sup>3 </sup> University of Washington

\* corresponding author:
<a href="mailto:sean.turner@pnnl.gov" class="email">sean.turner@pnnl.gov</a>

**Journal Article:** [![Generic
badge](https://img.shields.io/badge/DOI-10.1016/j.jhydrol.2021.126843-orange.svg)](https://doi.org/10.1016/j.jhydrol.2021.126843)

**Reservoir Operating Policies Dataset:** Inferred Storage Targets and
Release Functions `ISTARF-CONUS`:
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4602277.svg)](https://doi.org/10.5281/zenodo.4602277)

### Contributing software

<table>
<thead>
<tr class="header">
<th>Model</th>
<th>Version</th>
<th>Repository</th>
<th>DOI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>starfit</code></td>
<td>0.1.0</td>
<td><a href="https://github.com/IMMM-SFA/starfit/" class="uri">https://github.com/IMMM-SFA/starfit/</a></td>
<td><a href="https://doi.org/10.5281/zenodo.4924634"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.4924634.svg" alt="DOI" /></a></td>
</tr>
</tbody>
</table>

### Data requirements

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 9%" />
<col style="width: 11%" />
<col style="width: 53%" />
</colgroup>
<thead>
<tr class="header">
<th>Dataset</th>
<th>Version</th>
<th>Link</th>
<th>Supporting article to cite</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Global Reservoir and Dam Database <code>GRanD</code></td>
<td>1.3</td>
<td><a href="http://globaldamwatch.org/grand/" class="uri">http://globaldamwatch.org/grand/</a></td>
<td><a href="https://doi.org/10.1890/100125"><img src="https://img.shields.io/badge/DOI-10.1890/100125-orange.svg" alt="Generic badge" /></a></td>
</tr>
<tr class="even">
<td>Reservoir Operations for CONUS <code>ResOpsUS</code></td>
<td>1.0</td>
<td><a href="https://doi.org/10.5281/zenodo.5367383"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.5367383.svg" alt="DOI" /></a></td>
<td>Steyaert et al., <em>In Review</em>, Nature Scientific Data.</td>
</tr>
</tbody>
</table>

Reproduce my experiment
-----------------------

In Turner et al., 2021, reservoir operations data from `ResOpsUS` are
used to infer the operating policies of different reservoirs. The policy
inference code is contained in the `starfit` package.

For this example, you will need to first load some libraries:

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

`ResOpsUS` can be downloaded in full and read into R using `starfit`
function `read_reservoir_data()`. Alternatively, the same function can
access `ResOpsUS` data directly from Zenodo, saving us the effort of
downloading the entire dataset.

    #read_reservoir_data(500)
