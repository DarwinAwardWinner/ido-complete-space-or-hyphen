ido-complete-space-or-hyphen
============================

Make ido completes like built-in M-x does, useful when use smex or use ido to
complete other hyphen separated choices

## Example

Choices: "ido-foo-bar", "ido-space" "ido-test"

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido-" |

Choices: "ido-foo-bar", "ido-space" "ido-test"

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido " |

Choices: "ido-foo-bar", "ido-space" "idotest"

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido"  |
    | SPACE        | "ido-" |

When HYPHEN can be inserted and SPACE cannot, insert HYPHEN when user enter SPACE.

Choices: "ido-foo-bar", "ido-space" "ido test"

    | Key Sequence | Result |
    |--------------+--------|
    | i            | "i"    |
    | SPACE        | "ido"  |
    | SPACE        | "ido " |

If bot HYPHEN and SPACE can be inserted, SPACE just inserts itself.

## Usage

    (require 'ido-complete-space-or-hyphen)
    (ido-mode t)
