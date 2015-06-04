# member-functions
originally by Ron Lawrence <ral@bit-net.com>

Pulled from:
http://www.emacswiki.org/emacs/ExpandMemberFunctions

Changes:
* Added handling for multiple character extensions of source files. 

How does it work:
Expands functions headers from header file into blank functions in source file.
Works with custom header/source file extensions.
Quick use with input file names guessing.


INSTALLATION:

1. Copy member-functions.el to desired folder [example: cp member-functions.el ~/.emacs.d/lisp]

2. Add following lines to your .emacs file [by default at ~/.emacs]:

   ;; load the member-function
   (load "PATH TO FILE") ;; [example: (load "~/.emacs.d/lisp/member-functions)], best not to include .el
   (require 'member-functions)
   ;; set your own file extensions, do not include dot (valid examples below)
   (setq mf--source-file-extension "cpp")
   (setq mf--header-file-extension "hh")

3. Add valid PATH TO FILE in above code, edit extensions for your fitting


USAGE:

1. Open desired header file for expansion (it is VITAL to work from header file, not source file - if you want file name autocomplete)

2. Activate with [M-x expand-member-functions]

3. Guessed input files names will appear, edit them or press [RET] [RET] if they are correct

4. SAVE SOURCE FILE BUFFER, [C-x s] (save all buffers) will do

5. Enjoy!