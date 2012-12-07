ido-complete-space-or-hyphen
============================

Make ido completes like built-in M-x does, useful when use smex or use ido to
complete other hyphen separated choises

## Example

Choises: "ido-foo-bar", "ido-space" "idotest"

After you type "ido", then SPACE key. HYPHEN is inserted for you.

Howver if the choises are "ido-foo-bar", "ido-space" and "ido test", HYPHEN
is not inserted, you have to decided press SPACE or HYPHEN

## Usage

    (require 'ido-complete-space-or-hyphen)
    (ido-mode t)
