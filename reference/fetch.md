# Fetch a value

Fetches a single value from your local socials data frame.

## Usage

``` r
fetch(values, type = "mastodon", n = 1)
```

## Arguments

- values:

  Character. Values of social data to match by.

- type:

  Character. Type of social data to fetch.

- n:

  Numeric. Maximum number of matches per value to return.

## Value

Character string of the value of the type of data requested

## Examples

``` r
if (FALSE) { # local_eg()
fetch("Steffi LaZerte", type = "linkedin")
fetch(c("Steffi LaZerte", NA, "Yanina Bellini Saibene"))
fetch("steffilazerte")
fetch("Maëlle Salmon", type = "github")
}
```
