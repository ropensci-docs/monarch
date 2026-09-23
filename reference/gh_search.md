# Find GH username from repository and full name

Look up users of a repository and match to a name. Try with and without
initials.

## Usage

``` r
gh_search(name, pkg = NULL, owner = "ropensci", open_browser = interactive())
```

## Arguments

- name:

  Character. Full or partial name of the person for whom you want to
  fetch the GitHub username.

- pkg:

  Character. (Optional) Repository name (package name).

- owner:

  Character. (Optional) Owner of the repository.

- open_browser:

  Logical. Whether to open the profile page in a browser for
  confirmation.

## Value

Accepted user name

## Examples

``` r
if (FALSE) { # local_eg()
gh_search(name = "Steffi E. LaZerte", pkg = "weathercan")
gh_search(name = "Steffi", pkg = "weathercan")
}
```
