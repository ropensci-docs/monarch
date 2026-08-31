# Fetch contact information from GitHub

Using a GitHub username fetch the contact information from their
profile.

## Usage

``` r
socials_gh(github, quiet = FALSE)
```

## Arguments

- github:

  Character. Github username

- quiet:

  Logical. Whether to suppress progress messages.

## Value

Data frame of social contact information. Three columns \`type\`,
\`value\` and \`github\` to indicate the type and value of the contact
information and the GitHub username identifying the individual.

## Examples

``` r
if (FALSE) { # local_eg()
socials_gh("steffilazerte")
}
```
