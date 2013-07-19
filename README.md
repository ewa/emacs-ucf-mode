emacs-ucf-mode
==============

Emacs major mode for editing Xilinx UCF (User Constraint File) files

This program is released under the terms of the GNU GPL v.3 or later.

To enable UCF mode, save `ucf-mode.el` somewhere in your search path (e.g. `~/emacs/` and add the following lines to your `.emacs` file:

```
(autoload 'ucf-mode "ucf-mode" "Xilinx UCF mode" t)
(add-to-list 'auto-mode-alist '("\\.ucf\\'" . ucf-mode))
```

The results look about like this:
<pre>
<font color="#b22222">#</font><font color="#b22222">GTX Reference clock pin -- used directly inside GTX transciever block
</font><font color="#b22222">#</font><font color="#b22222">NET doesn't appear as a top-level I/O -- causes translation warning
</font><font color="#a020f0">NET</font> "<font color="#a0522d">GT&#95;REF_CLK_P1</font>" <font color="#228b22">TNM_NET</font> = GT_REF_CLK_P1;
<font color="#a020f0">TIMESPEC</font> <font color="#a0522d">TS&#95;GT_REF_CLK_P1</font> = <font color="#228b22">PERIOD</font> "GT_REF_CLK_P1" 200 <font color="#008b8b">MHz</font> <font color="#008b8b">HIGH</font> 50%;

<font color="#b22222">#</font><font color="#b22222">Data clock from ADC0.  Driven by ADC&#95;CLK_{P/N}_1 direct from AD9510 chip.
</font><font color="#a020f0">NET</font> "<font color="#a0522d">AD0&#95;P_CLK</font>" <font color="#228b22">TNM_NET</font> = AD0_P_CLK;
<font color="#a020f0">TIMESPEC</font> <font color="#a0522d">TS&#95;AD0_P_CLK</font> = <font color="#228b22">PERIOD</font> "AD0_P_CLK" 200 <font color="#008b8b">MHz</font> <font color="#008b8b">HIGH</font> 50%;
<font color="#228b22">OFFSET</font> = <font color="#008b8b">IN</font> -0.12 <font color="#008b8b">ns</font> <font color="#228b22">VALID</font> 2.22 <font color="#008b8b">ns</font> <font color="#228b22">BEFORE</font> "AD0&#95;P_CLK" <font color="#008b8b">RISING</font>;
<font color="#228b22">OFFSET</font> = <font color="#008b8b">IN</font> -0.23 <font color="#008b8b">ns</font> <font color="#228b22">VALID</font> 2.01 <font color="#008b8b">ns</font> <font color="#228b22">BEFORE</font> "AD0&#95;P_CLK" <font color="#008b8b">FALLING</font>;
</pre>
