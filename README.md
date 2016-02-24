## Curriculum Vitae for Luis Urrea
A CV written in LaTeX using the [moderncv](http://www.ctan.org/pkg/moderncv) class.

### Sample
Here's what it looks like with real data, using the "classic" style and blue color scheme:

![Image](/cv_sample.png?raw=true "Sample CV")

### Why
I decided to start keeping my CV in LaTeX because:

* I can never find my CV when I need it
* I have dozens of files named `resume.doc` on my computer
* LaTeX -> PDF ensures a consistent, beautiful layout
* Writing your CV in a source-based language means you can track it in git (w00t!)

### Usage
To "build" a PDF you simply type:

    $ make

To clean up all generated and intermediate content, type:

    $ make clean

### Pre-requistes for building
Depending on your GNU/Linux distribution the package names may be different. Basically, you need the `texlive` package, as well as whichever "extras" package contains the moderncv stuff.

__On Arch Linux:__

    $ sudo pacman -Sy texlive-core texlive-latexextra

__On Fedora:__

    $ sudo yum install texlive texlive-moderncv

__On Ubuntu:__

    $ sudo add-apt-repository ppa:texlive-backports
    $ sudo apt-get install texlive
    $ sudo apt-get --no-install-recommends install texlive-latex-extra

__Mac OS X:__ download and install [BasicTeX](https://www.tug.org/mactex/morepackages.html) (a minimal TeXLive distribution) and then:

    $ export PATH=$PATH:/usr/local/texlive/2015basic/bin/x86_64-darwin
    $ sudo tlmgr install collection-fontsrecommended
    $ wget https://launchpad.net/moderncv/trunk/1.5.1/+download/moderncv-1.5.1.zip
    $ unzip moderncv-1.5.1.zip
    $ sudo mkdir -p /usr/local/texlive/2015basic/texmf-local/tex/latex/moderncv
    $ sudo cp moderncv/*.sty moderncv/*.cls /usr/local/texlive/2015basic/texmf-local/tex/latex/moderncv
    $ sudo mktexlsr

__Others:__ send a pull request with instructions for your distro.
