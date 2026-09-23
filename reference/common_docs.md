# Common arguments and documentation for various functions

Common arguments and documentation for various functions

## Arguments

- socials:

  Data frame. Data frame of previously fetched/loaded social contact
  information. Data frame with three columns \`type\`, \`value\` and
  \`github\` to indicate the type and value of the contact information
  and the GitHub username identifying the individual.

- github:

  Character. Github username

- names:

  Character. Names to fetch by.

- value:

  Character. Value to search by

- type:

  Character. Type of \`value\` (e.g., "github" for github handle)

- pkg:

  Character. (Optional) Repository name (package name).

- owner:

  Character. (Optional) Owner of the repository.

- force_masto:

  Logical. Whether to force a re-fetching of Mastodon handles.

- open_browser:

  Logical. Whether to open the profile page in a browser for
  confirmation.

- quiet:

  Logical. Whether to suppress progress messages.

## Details

Use \`@inheritParams common_docs\` to include the above in any function
documentation with a matching argument (will only include matching args)
