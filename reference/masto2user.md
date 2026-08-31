# Convert a mastodon user link to handle

Convert a mastodon user link to handle

## Usage

``` r
masto2user(x)
```

## Arguments

- x:

  Character. Link to user's profile

## Value

Character user handle @user@instance

## Examples

``` r
if (FALSE) { # local_eg()
masto2user("https://fosstodon.org/@steffilazerte")
masto2user("steffi")
masto2user("@steffilazerte@fosstodon.org")
masto2user(NA)
}
```
