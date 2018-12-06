# gerp
If you ever do
```bash
grep -rn <search_term>
```
or
```bash
git grep -n <search_term>
```
... and then copy-pasting the file-name (and sometimes the line number) back into
```bash
vim +<linenum> <filename>
```
... then this script will make your copy-pasting easier and faster.


Usage might look like this
```bash
$ gerp -C1 foo
vim SomeFile.h +40 ;#     void bar();
vim SomeFile.h +41 ;#     void foo() const;
vim SomeFile.h +42 ;#     void baaz();
```

Triple-click with the mouse on an output line to mark the whole line, middle click your mouse to paste, and hit return to open the file on the right line with vim.

The flags `-A`, `-B`, and `-C` are supported.
