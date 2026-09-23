# Find and insert missing social media handles

Find and insert missing social media handles

## Usage

``` r
add_handles(
  df,
  primary = "github",
  which_cols = c("github", "name", "mastodon", "bluesky", "linkedin"),
  pkg_col = "pkg",
  owner_col = "owner",
  prefix = "",
  force = FALSE
)
```

## Arguments

- df:

  Data frame with at least 1 column appended with \`\_name\` or
  \`\_github\`.

- primary:

  Character. Either "github" or "name", which ever column is the primary
  column by which social handles should be fetched.

- which_cols:

  Character vector. Social columns to return, any of "github", "name",
  "mastodon", "linkedin", "bluesky".

- pkg_col:

  Character. Name of the "pkg" column. Optional but recommended for
  fetching by name when \`primary = "name"\`.

- owner_col:

  Character. Name of the column containing repository owners for
  packages (\`pkg_col\`). Optional but recommended for fetching by name
  when \`primary = "name"\`.

- prefix:

  Character. Optional prefix on column names (e.g. "maintainer\_" for
  "maintainer_github", "maintainer_name", etc.)

- force:

  Logical. Whether to force an update of all handles (not just those
  missing).

## Value

Data frame with added names and social media handles.

## Examples

``` r
if (FALSE) { # local_eg()
d <- data.frame(author_name = "Steffi LaZerte")
add_handles(d, primary = "name", prefix = "author_")

d <- data.frame(
  author_name = "Steffi LaZerte",
  pkg = "weathercan",
  owner = "ropensci",
  author_github = "steffilazerte"
)

add_handles(
  d,
  primary = "name",
  prefix = "author_",
  pkg_col = "pkg",
  owner_col = "owner",
  which_cols = "github"
)
add_handles(
  d,
  primary = "name",
  prefix = "author_",
  pkg_col = "pkg",
  owner_col = "owner"
)

d <- data.frame(github = "steffilazerte")
add_handles(d)

# If all complete, do not overwrite unless force == TRUE
d <- data.frame(
  github = "steffilazerte",
  name = "test",
  mastodon = "test",
  linkedin = "test"
)
add_handles(d)
add_handles(d, force = TRUE)

# Use name for LinkedIn (always)
d <- data.frame(github = "steffilazerte", name = "test", mastodon = "test")
add_handles(d)

d <- data.frame(
  author_name = c("Steffi LaZerte", "Yanina Bellini Saibene"),
  author_github = c("steffilazerte2", NA)
)
# Keep original github
add_handles(d, primary = "name", prefix = "author_")
# Get stored github
add_handles(d, primary = "name", prefix = "author_", force = TRUE)
}
```
