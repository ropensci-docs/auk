# Filter to only include observations with breeding codes

eBird users have the option of specifying breeding bird atlas codes for
their observations, for example, if nesting building behaviour is
observed. Use this filter to select only those observations with an
associated breeding code. This function only defines the filter and,
once all filters have been defined,
[`auk_filter()`](https://docs.ropensci.org/auk/reference/auk_filter.md)
should be used to call AWK and perform the filtering.

## Usage

``` r
auk_breeding(x)
```

## Arguments

- x:

  `auk_ebd` object; reference to basic dataset file created by
  [`auk_ebd()`](https://docs.ropensci.org/auk/reference/auk_ebd.md).

## Value

An `auk_ebd` object.

## See also

Other filter:
[`auk_bbox()`](https://docs.ropensci.org/auk/reference/auk_bbox.md),
[`auk_bcr()`](https://docs.ropensci.org/auk/reference/auk_bcr.md),
[`auk_complete()`](https://docs.ropensci.org/auk/reference/auk_complete.md),
[`auk_country()`](https://docs.ropensci.org/auk/reference/auk_country.md),
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
system.file("extdata/ebd-sample.txt", package = "auk") |>
  auk_ebd() |>
  auk_breeding()
#> Input 
#>   EBD: /github/home/R/x86_64-pc-linux-gnu-library/4.6/auk/extdata/ebd-sample.txt 
#> 
#> Output 
#>   Filters not executed
#> 
#> Filters 
#>   Species: all
#>   Countries: all
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
#>   Records with breeding codes only: yes
#>   Exotic Codes: all
#>   Complete checklists only: no
```
