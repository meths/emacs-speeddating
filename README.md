# `speeddating.el` [![MELPA badge][melpa-badge]][melpa-link] [![Travis CI Build Status][travis-badge]][travis-link]

  [melpa-link]: https://melpa.org/#/speeddating
  [melpa-badge]: https://melpa.org/packages/speeddating-badge.svg
  [travis-link]: https://travis-ci.org/xuchunyang/emacs-speeddating
  [travis-badge]: https://travis-ci.org/xuchunyang/emacs-speeddating.svg?branch=master

Increase date and time at point.

For example, saying point is on `31`, `M-x speeddating-increase` will change

    Fri, 31 Dec 1999 15:00:00 +0800

into

    Sat, 01 Jan 2000 15:00:00 +0800

## Requirement

Emacs 25.1 or newer

## Date and time formats

`speeddating.el` supports date and time formats in the user option
`speeddating-formats`, the formats use a subset syntax of
[`format-time-string`](https://www.gnu.org/software/emacs/manual/html_node/elisp/Time-Parsing.html).
Currently, the following formats are supported out of box.

<!-- (dolist (s speeddating-formats) (insert (format "| `%s` | %s |\n" s (format-time-string s)))) -->
| Format                     | Example                         |
|----------------------------|---------------------------------|
| `%a, %d %b %Y %H:%M:%S %z` | Sat, 20 Jun 2026 17:42:23 +0100 |
| `%a %b %d %H:%M:%S %Y %z`  | Sat Jun 20 17:42:23 2026 +0100  |
| `%Y-%m-%dT%H:%M:%S%:z`     | 2026-06-20T17:42:23+01:00       |
| `%a %b %_d %H:%M:%S %Z %Y` | Sat Jun 20 17:42:23 BST 2026    |
| `%a %b %-d %H:%M:%S %Y %Z` | Sat Jun 20 17:42:23 2026 BST    |
| `%-d %B %Y, at %H:%M`      | 20 June 2026, at 17:42          |
| `%Y-%m-%d %H:%M:%S`        | 2026-06-20 17:42:23             |
| `%Y-%m-%d %H:%M`           | 2026-06-20 17:42                |
| `%A, %B %-d, %Y`           | Saturday, June 20, 2026         |
| `%d %B %Y`                 | 20 June 2026                    |
| `%d %b %Y`                 | 20 Jun 2026                     |
| `%B %-d, %Y`               | June 20, 2026                   |
| `%Y-%m-%d`                 | 2026-06-20                      |
| `%Y/%m/%d`                 | 2026/06/20                      |
| `%H:%M:%S`                 | 17:42:23                        |
| `%Y`                       | 2026                            |
| `%B`                       | June                            |
| `%b`                       | Jun                             |
| `%A`                       | Saturday                        |
| `%a`                       | Sat                             |
