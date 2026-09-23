# Fetch contact information from social media

This is a wrapper around the three \`socials_xxx()\` functions.
\`socials_gh()\` starts (ideally) with a GitHub username to fetch
contact info from GitHub, followed by \`socials_ro()\` which checks
rOpenSci author pages and finally, if Mastodon handles have not been
found \`socials_masto()\`.

## Usage

``` r
socials_fetch(
  github = NULL,
  name = NULL,
  pkg = NULL,
  owner = "ropensci",
  which_cols = c("github", "name", "mastodon"),
  force_masto = FALSE,
  quiet = FALSE
)
```

## Arguments

- github:

  Character. Github username

- name:

  Character. Alternatively, a full name (can be slow if \`pkg\` not also
  provided).

- pkg:

  Character. Repository name for an rOpenSci package (in the
  \`ropensci\` organization)

- owner:

  Character. (Optional) Owner of the repository.

- which_cols:

  Character vector. Social handles to include defaults to "github",
  "name", "mastodon".

- force_masto:

  Logical. Whether to force a re-fetching of Mastodon handles.

- quiet:

  Logical. Whether to suppress progress messages.

## Value

Data frame of contact information

## Details

This workflow generally assumes that the person has a GitHub username.
You can supply name, which will trigger a search for the GitHub username
for you. This will search all of the rOpenSci organization for users
with that name which can take a while. However, if you supply a name and
a \`pkg\` (repository in rOpenSci), it can be much faster.

## Examples

``` r
if (FALSE) { # local_eg()
socials_fetch("steffilazerte")
socials_fetch(name = "Steffi LaZerte", pkg = "weathercan")
socials_fetch(name = "Bart Vanhoorne", pkg = "worrms")
socials_fetch(name = "Maelle Salmon", pkg = "babelquarto", owner = "ropensci-review-tools")
}
```
