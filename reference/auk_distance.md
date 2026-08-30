# Filter eBird data by distance travelled

Define a filter for the eBird Basic Dataset (EBD) based on the distance
travelled on the checklist. This function only defines the filter and,
once all filters have been defined,
[`auk_filter()`](https://docs.ropensci.org/auk/reference/auk_filter.md)
should be used to call AWK and perform the filtering. Note that
stationary checklists (i.e. point counts) have no distance associated
with them, however, since these checklists can be assumed to have 0
distance they will be kept if 0 is in the range defined by `distance`.

## Usage

``` r
auk_distance(x, distance, distance_units)
```

## Arguments

- x:

  `auk_ebd` or `auk_sampling` object; reference to file created by
  [`auk_ebd()`](https://docs.ropensci.org/auk/reference/auk_ebd.md) or
  [`auk_sampling()`](https://docs.ropensci.org/auk/reference/auk_sampling.md).

- distance:

  integer; 2 element vector specifying the range of distances to filter
  by. The default is to accept distances in kilometers, use
  `distance_units = "miles"` for miles.

- distance_units:

  character; whether distances are provided in kilometers (the default)
  or miles.

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
[`auk_country()`](https://docs.ropensci.org/auk/reference/auk_country.md),
[`auk_county()`](https://docs.ropensci.org/auk/reference/auk_county.md),
[`auk_date()`](https://docs.ropensci.org/auk/reference/auk_date.md),
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
# only keep checklists that are less than 10 km long
system.file("extdata/ebd-sample.txt", package = "auk") |>
  auk_ebd() |>
  auk_distance(distance = c(0, 10))
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
#>   Distance travelled: 0-10 km
#>   Records with breeding codes only: no
#>   Exotic Codes: all
#>   Complete checklists only: no
  
# alternatively, without pipes
ebd <- auk_ebd(system.file("extdata/ebd-sample.txt", package = "auk"))
auk_distance(ebd, distance = c(0, 10))
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
#>   Distance travelled: 0-10 km
#>   Records with breeding codes only: no
#>   Exotic Codes: all
#>   Complete checklists only: no
```
