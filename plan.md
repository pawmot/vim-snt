# Vim Show&Tell ideas

1. Vim the editing philosophy vs Vim the editor
1. Vim the editing philosophy
    1. Modality
        1. What are modes any why are they valuable
        1. Normal
            1. default mode
            1. <esc> to go back to normal
            1. ZZ - save and quit :)
        1. Insert
            1. i - insert at cursor
            1. I - insert at the first non-whitespace char in line
            1. a - insert after cursor
            1. A - insert after the end of the line
            1. o - insert line after current one and Insert
            1. O - insert line before current one and Insert
            1. s - delete under cursor and Insert
            1. S - delete line and Insert
            1. C - delete to the end of line and Insert
            1. c operator (described later)
        1. Visual
            1. v - visual selection by char with wrapping lines (mouse-like) [Visual]
            1. V - visual selection by lines [V-Line]
            1. <C-v> - visual selection with a rectangular block [V-Block]
                1. usefull with pasting, or hitting I to go to Insert and edit multiple lines
        1. Command
            1. Usually enter with :
            1. Allows running commands, either built in or from plugins
                1. :q - quit
                1. :w - save
                1. :wa - save all
                1. :wq - save quit
                1. :q! - quit without saving
                1. :bn - go to next tab (*)
                1. :bp - go to previous tab (*)
        1. Replace
            1. r - replace the under cursor (not really Replace mode)
            1. R - go to Replace mode, replace multiple characters
        1. A lot more (e.g. Select, Operator Pending, ...), but those 3/4 are the main ones
    1. Motions
        1. Notes, chords, melodies
        1. hjkl
            1. h - left
            1. j - down
            1. k - up
            1. l - right
        1. Horizontal
            1. w, b, e, ge - words
            1. W, B, E, gE - WORDs
            1. f, F - find char, place cursor on it
            1. t, T - find char, place cursor before/after it
            1. ;, : - repeat search with f/F/t/T
            1. 0, ^, g_, $ - extremities
        1. Vertical
            1. {, } - move by paragraphs (separated by empty lines)
            1. <C-d>, <C-u> - move by half a page down and up
            1. /{pattern}, ?{pattern} - search down/up using a regex
            1. n, N - find next in the direction of search
            1. *, # - find word under the cursor, down/up, n/N to find next occurrence
            1. gg, G - beginning/end of file
            1. {number}G, :{number} - go to line
            1. % when on one of ({[<>]}) - jump to matching bracket
        1. Repetitions
            1. {number}{motion} will repeat it multiple times
                1. 5l - move 5 chars  to the right
                1. 2j - move 2 lines down
                1. 2{ - move 2 paragraphs up
            1. Relative line numbers
    1. Operators
        1. Kinds
            1. d - delete (cut)
            1. y - yank (copy)
            1. p - paste after cursor/line
            1. P - paste before cursor/line
            1. c - change (delete and go to Insert mode)
        1. Shorthand operator syntax
            1. yy - yank current line
            2. dd - delete current line
            3. cc - change current line
        1. Operators in Normal mode
            1. {op}{motion} will apply operator to the range described by motion
                1. y2l - yank 2 characters to the right
                1. dw - delete until the end of the word
                1. c$ - change until the end of the line
                1. d2j - delete three lines (current and two below)
                1. cf) - change everything to ')' (inclusive)
                1. ct) - change everything until ')' (exclusive)
            1. Text-object operators
                1. yiw - yank whole word
                1. diw - delete whole word
                1. diW - delete whole WORD
                1. ciw - change whole word
                1. yi} - yank the inside of a block delimited by {} (exclusive)
                1. da) - delete a block delimited by () (inclusive)
                1. block delimiting characters:
                    1. ()
                    1. {}
                    1. []
                    1. ""
                    1. ''
                    1. <>
                1. This is a simplified description, refer to docs for details
            1. . - repeat last run command at current cursor position
        1. Operators in Visual modes apply to the selected range
    1. Undo/redo
        1. u - undo
        1. <C-r> - redo
    1. Window scrolling
        1. zz - move current line to middle of the screen
        1. zt - move current line to top of the screen
        1. zb - move current line to bottom of the screen
        1. M - move cursor to the middle of the screen
        1. H - move cursor to the top of the screen
        1. L - move cursor to the bottom of the screen
        1. Usefull remaps - auto zz after searching and <C-d>/<C-u> results in a really fluid experience
    1. Advanced
        1. Easymotion and similar
            1. Allows for quick jumping to occurences of a character (demo)
1. Vim the editor
    1. Vim vs Neovim
    1. Configuration
    1. Plugins
    1. Making Neovim into an IDE-lite

