ido-complete-space-or-hyphen
============================

Make ido completes like built-in M-x does, useful when use smex or use ido to
complete other hyphen separated choices

## Example

`(ido-completing-read "test: " '("ido-foo-bar" "ido-space" "ido-test"))`

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido-" |

`(ido-completing-read "test: " '("ido foo-bar" "ido space" "ido test"))`

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido " |

`(ido-completing-read "test: " '("ido-foo-bar" "ido-space" "idotest"))`

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido"  |
    | SPACE        | "ido-" |

When HYPHEN can be inserted and SPACE cannot, insert HYPHEN when user enter SPACE.

`(ido-completing-read "test: " '("ido-foo-bar" "ido-space" "ido test"))`

    | Key Sequence | Result                           |
    |--------------+----------------------------------+
    | i            | "i"                              |
    | SPACE        | "ido"                            |
    | SPACE        | "ido"  Completion popup is shown |
    | SPACE        | "ido "                           |

If both HYPHEN and SPACE can be inserted, SPACE first brings the completion
popup window, if user types SPACE again, then SPACE itself is inserted.

## Usage

    (require 'ido-complete-space-or-hyphen)
    (ido-mode t)
