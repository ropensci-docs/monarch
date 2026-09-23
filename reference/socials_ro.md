# Fetch contact information from rOpenSci author pages

Once initial contact information has been sourced via \`socials_gh()\`,
we can add to this by looking for additional details on the rOpenSci
author pages (\<https://ropensci.org/author\>).

## Usage

``` r
socials_ro(socials = NULL, names = NULL, github = NULL, quiet = FALSE)
```

## Arguments

- socials:

  Data frame. Data frame of previously fetched/loaded social contact
  information. Data frame with three columns \`type\`, \`value\` and
  \`github\` to indicate the type and value of the contact information
  and the GitHub username identifying the individual.

- names:

  Character. Optional, supply the full name as on RO author pages.
  (Doesn't require the socials data frame)

- github:

  Character. Github username

- quiet:

  Logical. Whether to suppress progress messages.

## Value

Data frame of social contact information. Three columns \`type\`,
\`value\` and \`github\` to indicate the type and value of the contact
information and the GitHub username identifying the individual.

## Details

By default \`socials_ro()\` will use the \`name\` stored in the
\`socials\` data frame.

If you know this doesn't match exactly that on the rOpenSci author
pages, you can supply an alternative with \`name\`. Ideally however, you
would add an additional name to the socials data frame to keep track of
minor variations in names.

## Examples

``` r
if (FALSE) { # local_eg()
socials_gh("steffilazerte") |>
  socials_ro()

socials_ro(names = c("Stefanie LaZerte", "Steffi LaZerte"))
}
```
