# Save/Update socials data to local file

Save/Update your local copy of the contact information.

## Usage

``` r
cocoon_update(socials, type = NULL, value = NULL)
```

## Arguments

- socials:

  Data frame. Data frame of previously fetched/loaded social contact
  information. Data frame with three columns \`type\`, \`value\` and
  \`github\` to indicate the type and value of the contact information
  and the GitHub username identifying the individual.

- type:

  Character. Type of \`value\` (e.g., "github" for github handle)

- value:

  Character. Value to search by

## Value

Nothing

## Examples

``` r
if (FALSE) { # local_eg()
socials_fetch("steffilazerte") |>
  cocoon_update()

# Or directly
cocoon_update("steffilazerte")

# Or add parts
cocoon_update("steffilazerte", type = "name", value = "Stefanie LaZerte")
}
```
