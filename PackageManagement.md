[comment]: <> (SPDX-License-Identifier: AGPL-3.0)

[comment]: <> (----------------------------------------------------)
[comment]: <> (Copyright © 2024, 2025, 2026)
[comment]: <> (            Pellegrino Prevete)
[comment]: <> (All rights reserved)
[comment]: <> (----------------------------------------------------)

[comment]: <> (This program is free software: you can redistribute)
[comment]: <> (it and/or modify it under the terms of the)
[comment]: <> (GNU Affero General Public License as published)
[comment]: <> (by the Free Software Foundation, either version)
[comment]: <> (3 of the License.)

[comment]: <> (This program is distributed in the hope that it)
[comment]: <> (will be useful, but WITHOUT ANY WARRANTY;)
[comment]: <> (without even the implied warranty of)
[comment]: <> (MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.)
[comment]: <> (See the GNU Affero General Public License)
[comment]: <> (for more details.)

# Package management

Internally, the `ur` is written to be
modular, so that it can be easily adapted
to work with any pre-existing package maanger.
The default and main is for the `inteppacman`
package manager, which is a pacman extension
with support for handling Android applications,
targeting the
[pacman tree published and mantained](
  https://github.com/themartiancompany/pacman)
published and maintained by The Martian Company,
which includes cross-platform support and
user-level management.

Cross-platform support and user-level management
code comes from the Termux and MSYS2/MinGW projects.

## Namespacing

Differently than from on a classical system package
manager, on the Ur there is no unique correspondence
between a `pkgbase` (a packages group name) and
an Universal Recipe, as every publisher is allowed
to publish an Universal Recipe for any given `pkgbase`.

The main practical reason for this design has been
to allow plurality in collaborative projects (suppose
two maintainers disagree on the best way to package a
program) and for users to select what they deem the
best choice for their systems by themselves in an
easy way, without necessarily having to impose one
to everybody.

The main theoretical reason is words are used
to refer at concepts but at this time copyright
allows for its holders to keep using the same words
to refer to an ever different thing, so that in
practice we are literally allowing for private
groups to rent ownership of words' meaning,
which is something barbaric and dystopian.

It's normally expected from humans that
even when using the same words, they will
always mean something different, maybe
slightly different when one is lucky,
but always different.
At the same time thats not to be expected
from computers, which on the opposite are
supposed to always interpret the same symbol
the same way.
