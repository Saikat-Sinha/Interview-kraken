# Contributing

When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method.

## Git - Branching

### Quick Legend

<table>
  <thead>
    <tr>
      <th>Instance</th>
      <th>Branch</th>
      <th>Description, Instructions, Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Working</td>
      <td>master</td>
      <td>Accepts merges from Features/Issues and Hotfixes</td>
    </tr>
    <tr>
      <td>Features/Issues</td>
      <td>topic-*</td>
      <td>Always branch off HEAD of Working</td>
    </tr>
  </tbody>
</table>


The `main` branch should be considered origin/master and will be the main branch where the source code of `HEAD` always reflects a state with the latest delivered development changes for the next release. As a contributor, you will you be branching and merging from `master`.


## Commit Messages

As a general rule, your commit message should start with a single line that's no more than about 50 characters and that describes the commit concisely. If you feel the need for more detailed explanations, create a blank line, followed by a more detailed explanation.

For consistency, try and use the imperative present tense when creating a message. Examples:

* Use "Add tests for" instead of "I added tests for"
* Use "Change x to y" instead of "Changed x to y"

In order to associate commits with Github Issue, the commit message might indicate one or more issue number and (optionally) a state change for the story. The commit message should start with square brackets containing a hash mark followed by the issue id wherever possible. For example:

    [Fixes Interview-kraken#14] Diverte power from warp drive to torpedoes

To automatically close an issue by using a commit message, include "Fix" in the square brackets in addition to the issue number. For example:

    [Fix Interview-kraken#12] Torpedoes now sufficiently powered






