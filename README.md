# Welcome to the Yet Another Wavelet toolbox.

![YAWTb](doc/images/yawtb_logo.jpg)

## Introduction

This archive contains the code of the YAWtb toolbox. This toolbox was under active development till about 2010. It is no longer developed and the purpose of this GitHub repository is only to keep an accessible archive for possible analysis.  

## Warnings

This is the version 0.1.0 of the YAWtb, the initial release.
It is still an unstable version and a lot of work has to be done 
especially on the documentation (use YAWtb at your own, rather limited, risk).
Any comments are welcome on our mailing lists (see the YAWtb website)

### Requirements

The YAWtb works for Matlab versions greater than 5 and was developped onto the 6th.
If you have some bugs, all emails are welcome at <yawtb-devel@lists.sourceforge.net>.
See the YAWtb homepage (http://www.fyma.ucl.ac.be/projects/yawtb) if you desire more 
information about this mailing list.

### Installation

In the sequel, the `>>` symbols represents the Matlab prompt.

Follow these steps to install the YAWtb Matlab toolbox,

1. Unpack YAWtb where you want (say the `<YAWTBDIR>` directory for simplicity);

2. Compile all the YAWtb mexfiles (provided that your `mex` matlab script is well configured) with the  `yamake` utility:
   `>> cd <YAWTBDIR>`
   `>> yamake`
(and for a more explicit compilation `>> yamake debug`)

**Remark**: If you have Microsoft Windows (9x, 2000, XP, ...), it seems that the native Matlab compiler, and also this of Windows, are not
able to compile correctly the yawtb C code (e.g. cwtsph stuff). Use instead the free compiler of Borland available at http://www.borland.com (need a simple registration) and configure Matlab in function (run 'mex -setup' and read the Borland compiler FAQ and doc).

3. Run `yaload` in Matlab to load the whole YAWtb path:

   >> cd <YAWTBDIR>
   >> yaload
    
4. Add the following lines to a matlab startup file, either the general one (matlabrc.m) located in MATLABDIR/toolbox/local, or the local startup file (startup.m) somewhere in your home dir (see matlab doc):

   %% YAWtb installation
   olddir=pwd;
   cd <YAWTBDIR>
   yaload;
   cd(olddir);
   clear olddir;

5. Enjoy of YAWtb !

