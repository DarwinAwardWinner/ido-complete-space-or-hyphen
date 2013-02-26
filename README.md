ido-complete-space-or-hyphen
============================

Make ido completes like built-in M-x does, useful when use smex or use ido to
complete other hyphen separated choises

## Example

Choises: "ido-foo-bar", "ido-space" "idotest"

After you type "i", then SPACE key. The input text is completed to "ido-" and
HYPHEN is inserted for you.

However if the choises are "ido-foo-bar", "ido-space" and "ido test", the input
text is completed to "ido", type SPACE again will insert SPACE.

## Usage

    (require 'ido-complete-space-or-hyphen)
    (ido-mode t)
