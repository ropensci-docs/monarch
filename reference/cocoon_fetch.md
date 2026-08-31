# Fetch all details on a social contact

Fetch all details on a social contact

## Usage

``` r
cocoon_fetch(value, type = "github")
```

## Arguments

- value:

  Character. Value to search by

- type:

  Character. Type of \`value\` (e.g., "github" for github handle)

## Value

Data frame of socials

## Examples

``` r
if (FALSE) { # local_eg()
cocoon_fetch("steffilazerte")
cocoon_fetch("steffi LaZerte", type = "name")
}
```
