# Update a socials data frame with new values

\`socials_update()\` takes an existing social data frame and adds or
updates new values. Only certain data types are permitted to have more
than one value (i.e. names and websites). In all other cases, if there
is more than one handle or id value, you will be asked to choose one to
keep.

## Usage

``` r
socials_update(socials, socials_new = NULL, type = NULL, value = NULL)
```

## Arguments

- socials:

  Data frame. Data frame of previously fetched/loaded social contact
  information. Data frame with three columns \`type\`, \`value\` and
  \`github\` to indicate the type and value of the contact information
  and the GitHub username identifying the individual.

- socials_new:

  Data frame. New data to add/update. If adding only a single value, use
  \`type\` and \`value\` instead.

- type:

  Character. Type of data to add (to add a single value, alternative to
  \`socials_new\`)

- value:

  Character. Value of data to add (to add a single value, alternative to
  \`socials_new\`).

## Value

Socials data frame with new values

## Examples

``` r
if (FALSE) { # local_eg()
socials_fetch("steffilazerte") |>
  socials_update(type = "name", value = "Stefanie LaZerte") # Add an alias
}
```
