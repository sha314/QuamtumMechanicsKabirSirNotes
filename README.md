# QuamtumMechanicsKabirSirNotes
Lecture notes on Quantum Mechanics by Dr. Khorshed Kabir, Dhaka University


# Packages required
following commands installs the required package

sudo apt-get install texlive-latex-extra
sudo apt-get install texlive-science


# link to the hand written pdf
https://drive.google.com/drive/folders/0B4yKhYnqwfLbOUdQOG15YUxVUXM


# .sty files
http://www.hss.caltech.edu/~kcb/TeX/kbordermatrix.sty

# TeX home directory and Custome .sty
You could create a folder below your TeX home directory and put your .sty file therein. Use this command at the command prompt to find out where:

$ kpsewhich -var-value=TEXMFHOME
On my computer it shows

C:/Users/stefan/texmf
but it might also be ~/texmf/ on a Linux or Unix computer.

Following the TeX directory structure, you should place your file in a subdirectory like ~/texmf/tex/latex/commonstuff/, according to Arthur's comment below. This has the advantage that it is not necessary to update the package database as TeX searches your personal texmf tree directly. If there is an ls-R file in your home texmf tree you can safely delete it as TeX will not use it anyway. (Note: this assumes your personal tree is on a local file system: users with remotely-mounted home folders may still need to hash.)

Regarding MiKTeX, have a look at the section "Installing sty or cls files" in the answer to the question How can I manually install a package on MikTex (Windows).

You can then verify what file will be used with:

$ kpsewhich filename.sty
This will show the path to the file picked up by the TeX implementation.


