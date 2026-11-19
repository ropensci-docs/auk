# Package index

## EBD Objects

- [`auk_ebd()`](https://docs.ropensci.org/auk/reference/auk_ebd.md) :
  Reference to eBird data file
- [`auk_sampling()`](https://docs.ropensci.org/auk/reference/auk_sampling.md)
  : Reference to eBird sampling event file

## Process Text Files

- [`auk_clean()`](https://docs.ropensci.org/auk/reference/auk_clean.md)
  : Clean an eBird data file (Deprecated)
- [`auk_select()`](https://docs.ropensci.org/auk/reference/auk_select.md)
  : Select a subset of columns
- [`auk_split()`](https://docs.ropensci.org/auk/reference/auk_split.md)
  : Split an eBird data file by species

## Filter

- [`auk_bbox()`](https://docs.ropensci.org/auk/reference/auk_bbox.md) :
  Filter the eBird data by spatial bounding box
- [`auk_bcr()`](https://docs.ropensci.org/auk/reference/auk_bcr.md) :
  Filter the eBird data by Bird Conservation Region
- [`auk_breeding()`](https://docs.ropensci.org/auk/reference/auk_breeding.md)
  : Filter to only include observations with breeding codes
- [`auk_complete()`](https://docs.ropensci.org/auk/reference/auk_complete.md)
  : Filter out incomplete checklists from the eBird data
- [`auk_country()`](https://docs.ropensci.org/auk/reference/auk_country.md)
  : Filter the eBird data by country
- [`auk_county()`](https://docs.ropensci.org/auk/reference/auk_county.md)
  : Filter the eBird data by county
- [`auk_date()`](https://docs.ropensci.org/auk/reference/auk_date.md) :
  Filter the eBird data by date
- [`auk_distance()`](https://docs.ropensci.org/auk/reference/auk_distance.md)
  : Filter eBird data by distance travelled
- [`auk_duration()`](https://docs.ropensci.org/auk/reference/auk_duration.md)
  : Filter the eBird data by duration
- [`auk_exotic()`](https://docs.ropensci.org/auk/reference/auk_exotic.md)
  : Filter the eBird data by exotic code
- [`auk_extent()`](https://docs.ropensci.org/auk/reference/auk_extent.md)
  : Filter the eBird data by spatial extent
- [`auk_filter()`](https://docs.ropensci.org/auk/reference/auk_filter.md)
  : Filter the eBird file using AWK
- [`auk_last_edited()`](https://docs.ropensci.org/auk/reference/auk_last_edited.md)
  : Filter the eBird data by last edited date
- [`auk_observer()`](https://docs.ropensci.org/auk/reference/auk_observer.md)
  : Filter the eBird data by observer
- [`auk_project()`](https://docs.ropensci.org/auk/reference/auk_project.md)
  : Filter the eBird data by project code
- [`auk_protocol()`](https://docs.ropensci.org/auk/reference/auk_protocol.md)
  : Filter the eBird data by protocol
- [`auk_species()`](https://docs.ropensci.org/auk/reference/auk_species.md)
  : Filter the eBird data by species
- [`auk_state()`](https://docs.ropensci.org/auk/reference/auk_state.md)
  : Filter the eBird data by state
- [`auk_time()`](https://docs.ropensci.org/auk/reference/auk_time.md) :
  Filter the eBird data by checklist start time
- [`auk_year()`](https://docs.ropensci.org/auk/reference/auk_year.md) :
  Filter the eBird data to a set of years

## Pre-process

- [`auk_rollup()`](https://docs.ropensci.org/auk/reference/auk_rollup.md)
  : Roll up eBird taxonomy to species
- [`auk_unique()`](https://docs.ropensci.org/auk/reference/auk_unique.md)
  : Remove duplicate group checklists

## Import

- [`auk_zerofill()`](https://docs.ropensci.org/auk/reference/auk_zerofill.md)
  [`collapse_zerofill()`](https://docs.ropensci.org/auk/reference/auk_zerofill.md)
  : Read and zero-fill an eBird data file
- [`read_ebd()`](https://docs.ropensci.org/auk/reference/read_ebd.md)
  [`read_sampling()`](https://docs.ropensci.org/auk/reference/read_ebd.md)
  : Read an EBD file

## Modeling

- [`filter_repeat_visits()`](https://docs.ropensci.org/auk/reference/filter_repeat_visits.md)
  : Filter observations to repeat visits for hierarchical modeling

- [`format_unmarked_occu()`](https://docs.ropensci.org/auk/reference/format_unmarked_occu.md)
  :

  Format EBD data for occupancy modeling with `unmarked`

## Data

- [`bcr_codes`](https://docs.ropensci.org/auk/reference/bcr_codes.md) :
  BCR Codes
- [`ebird_states`](https://docs.ropensci.org/auk/reference/ebird_states.md)
  : eBird States
- [`ebird_taxonomy`](https://docs.ropensci.org/auk/reference/ebird_taxonomy.md)
  : eBird Taxonomy
- [`valid_protocols`](https://docs.ropensci.org/auk/reference/valid_protocols.md)
  : Valid Protocols

## Path Management

- [`auk_get_awk_path()`](https://docs.ropensci.org/auk/reference/auk_get_awk_path.md)
  : OS specific path to AWK executable
- [`auk_get_ebd_path()`](https://docs.ropensci.org/auk/reference/auk_get_ebd_path.md)
  : Return EBD data path
- [`auk_set_awk_path()`](https://docs.ropensci.org/auk/reference/auk_set_awk_path.md)
  : Set a custom path to AWK executable
- [`auk_set_ebd_path()`](https://docs.ropensci.org/auk/reference/auk_set_ebd_path.md)
  : Set the path to EBD text files

## Helpers

- [`auk_ebd_version()`](https://docs.ropensci.org/auk/reference/auk_ebd_version.md)
  : Get the EBD version and associated taxonomy version
- [`auk_version()`](https://docs.ropensci.org/auk/reference/auk_version.md)
  : Versions of auk, the EBD, and the eBird taxonomy
- [`ebird_species()`](https://docs.ropensci.org/auk/reference/ebird_species.md)
  : Lookup species in eBird taxonomy
- [`get_ebird_taxonomy()`](https://docs.ropensci.org/auk/reference/get_ebird_taxonomy.md)
  : Get eBird taxonomy via the eBird API
- [`process_barcharts()`](https://docs.ropensci.org/auk/reference/process_barcharts.md)
  : Process eBird bar chart data
