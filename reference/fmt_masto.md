# Convert a mastodon user link to handle

Convert a mastodon user link to handle

## Usage

``` r
fmt_masto(x)
```

## Arguments

- x:

  Character. Link to user's profile

## Value

Character user handle @user@instance

## Examples

``` r
if (FALSE) { # local_eg()
fmt_masto("https://fosstodon.org/@steffilazerte")
fmt_masto("steffi lazerte")
fmt_masto("@steffilazerte@fosstodon.org")
fmt_masto(NA)
fmt_masto(c("https://fosstodon.org/@steffilazerte", "https://hackyderm.io/@ropensci"))
fmt_masto("none")
}
```
