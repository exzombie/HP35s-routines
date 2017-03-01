# HP-35s routines

## Intro

Here are some of the routines that I wrote for my HP-35s calculator. I
wrote them mostly for fun, but I think they could be useful in
practice. Anything more complex is probably better solved on a real
computer, which nowadays might mean a phone if you want to keep it
portable. But a HP calculator still has a superior interface and
battery life, so I hope you find these routines useful. Also included
is a quick reference card for the routines and more advanced built-in
functions which can be printed and is dimensioned to fit into the
calculator's pouch.

## Code organization

Each routine is in it's own file named after the letter that labels
the routine. The file starts with the code so that your text editor
can provide meaningful line numbers. Each routine consists of
subroutines that also have meaningful labels in the form of text
equations. These are never executed, so the value of flag 10 doesn't
matter. They only aid the reader.

After the code comes the description of the routine, how it's meant to
be called and what the subroutines do. The "public" subroutines,
i.e. those that are meant to be called by the user directly, have GTO
statements at the begining of the main routine for easy access. For
example, the M routine, which contains matrix operations, is organized
such that you call M001 or M002 for storing a matrix, M003 recalls the
stored matrix, M004 multiplies a matrix with a vector, and so on.

Use of named variables is mostly avoided, except for I and J of
course. Unless too inconvenient, routines try to only use anonymous
memory for storage and stack for input and output. Anonymous memory is
organized into segments of ten addresses, each belonging to a
routine. The first two digits of an address are the number of the
routine's letter label. For example, routine S is assigned addresses
from 190 to 199 (although only three are actually used). This scheme
leaves the first 10 and the last 530 addresses free. If a routine uses
any other memory, it is documented.

## Authors

Unless otherwise noted in a particular file, the following applies.

Copyright 2017 Jure Varlec <jure@varlec.si>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
