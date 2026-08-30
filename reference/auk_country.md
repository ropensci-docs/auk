# Filter the eBird data by country

Define a filter for the eBird Basic Dataset (EBD) based on a set of
countries. This function only defines the filter and, once all filters
have been defined,
[`auk_filter()`](https://docs.ropensci.org/auk/reference/auk_filter.md)
should be used to call AWK and perform the filtering.

## Usage

``` r
auk_country(x, country, replace = FALSE)
```

## Arguments

- x:

  `auk_ebd` or `auk_sampling` object; reference to file created by
  [`auk_ebd()`](https://docs.ropensci.org/auk/reference/auk_ebd.md) or
  [`auk_sampling()`](https://docs.ropensci.org/auk/reference/auk_sampling.md).

- country:

  character; countries to filter by. Countries can either be expressed
  as English names or [ISO 2-letter country
  codes](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). English
  names are matched via regular expressions using
  [countrycode](https://rdrr.io/pkg/countrycode/man/countrycode.html),
  so there is some flexibility in names.

- replace:

  logical; multiple calls to `auk_country()` are additive, unless
  `replace = FALSE`, in which case the previous list of countries to
  filter by will be removed and replaced by that in the current call.

## Value

An `auk_ebd` object.

## Details

This function can also work with on an `auk_sampling` object if the user
only wishes to filter the sampling event data.

## See also

Other filter:
[`auk_bbox()`](https://docs.ropensci.org/auk/reference/auk_bbox.md),
[`auk_bcr()`](https://docs.ropensci.org/auk/reference/auk_bcr.md),
[`auk_breeding()`](https://docs.ropensci.org/auk/reference/auk_breeding.md),
[`auk_complete()`](https://docs.ropensci.org/auk/reference/auk_complete.md),
[`auk_county()`](https://docs.ropensci.org/auk/reference/auk_county.md),
[`auk_date()`](https://docs.ropensci.org/auk/reference/auk_date.md),
[`auk_distance()`](https://docs.ropensci.org/auk/reference/auk_distance.md),
[`auk_duration()`](https://docs.ropensci.org/auk/reference/auk_duration.md),
[`auk_exotic()`](https://docs.ropensci.org/auk/reference/auk_exotic.md),
[`auk_extent()`](https://docs.ropensci.org/auk/reference/auk_extent.md),
[`auk_filter()`](https://docs.ropensci.org/auk/reference/auk_filter.md),
[`auk_last_edited()`](https://docs.ropensci.org/auk/reference/auk_last_edited.md),
[`auk_observer()`](https://docs.ropensci.org/auk/reference/auk_observer.md),
[`auk_project()`](https://docs.ropensci.org/auk/reference/auk_project.md),
[`auk_protocol()`](https://docs.ropensci.org/auk/reference/auk_protocol.md),
[`auk_species()`](https://docs.ropensci.org/auk/reference/auk_species.md),
[`auk_state()`](https://docs.ropensci.org/auk/reference/auk_state.md),
[`auk_time()`](https://docs.ropensci.org/auk/reference/auk_time.md),
[`auk_year()`](https://docs.ropensci.org/auk/reference/auk_year.md)

## Examples

``` r
# country names and ISO2 codes can be mixed
# not case sensitive
country <- c("CA", "United States", "mexico")
system.file("extdata/ebd-sample.txt", package = "auk") |>
  auk_ebd() |>
  auk_country(country)
#> Input 
#>   EBD: /github/home/R/x86_64-pc-linux-gnu-library/4.6/auk/extdata/ebd-sample.txt 
#> 
#> Output 
#>   Filters not executed
#> 
#> Filters 
#>   Species: all
#>   Countries: CA, MX, US
#>   States: all
#>   Counties: all
#>   BCRs: all
#>   Bounding box: full extent
#>   Years: all
#>   Date: all
#>   Start time: all
#>   Last edited date: all
#>   Protocol: all
#>   Project code: all
#>   Duration: all
#>   Distance travelled: all
#>   Records with breeding codes only: no
#>   Exotic Codes: all
#>   Complete checklists only: no
  
# alternatively, without pipes
ebd <- auk_ebd(system.file("extdata/ebd-sample.txt", package = "auk"))
auk_country(ebd, country)
#> Input 
#>   EBD: /github/home/R/x86_64-pc-linux-gnu-library/4.6/auk/extdata/ebd-sample.txt 
#> 
#> Output 
#>   Filters not executed
#> 
#> Filters 
#>   Species: all
#>   Countries: CA, MX, US
#>   States: all
#>   Counties: all
#>   BCRs: all
#>   Bounding box: full extent
#>   Years: all
#>   Date: all
#>   Start time: all
#>   Last edited date: all
#>   Protocol: all
#>   Project code: all
#>   Duration: all
#>   Distance travelled: all
#>   Records with breeding codes only: no
#>   Exotic Codes: all
#>   Complete checklists only: no
```
