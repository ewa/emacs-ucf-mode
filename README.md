emacs-ucf-mode
==============

Emacs major mode for editing Xilinx UCF (User Constraint File) files

This program is released under the terms of the GNU GPL v.3 or later.

To enable UCF mode, save `ucf-mode.el` somewhere in your search path (e.g. `~/emacs/`) and add the following lines to your `.emacs` file:

```lisp
(autoload 'ucf-mode "ucf-mode" "Xilinx UCF mode" t)
(add-to-list 'auto-mode-alist '("\\.ucf\\'" . ucf-mode))
```

The results look about like this:

![preview](colorized-ucf-example.png)
