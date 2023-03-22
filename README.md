## VERY UNOFFICIAL/EXPERIMENTAL PORT OF golang TO SICORTEX - NOT INTENDED TO BE ANY PART OF OFFICIAL GOLANG RELEASES
## IF THIS VIOLATES ANY TERMS/AGREEMENTS WITH DISTRIBUTION PLEASE INFORM ME AND I WILL REMOVE

## Background

Back about 13 years or so ago a company Sicortex made mips based HPC supercomputers. They also had a deskside version the PDS-072.
It was a 64 bit Little Endian Gentoo based machine. The PDS-072 had 12 6-core cpus and between 48 - 96 GB or Ram.
Nothing about its performance was hugely exciting but it was based on a Kautz graph for node interconnectivity.
Also around golang 1.6 a mips 64 port was released. This is an attempt to try and port this to my little sicortex PDS-072.

For the most part the port does seem to work. I have only currently tested forwards to this version 1.8.7 (which in itself is quite an old version of goleng but it does incorporate an important GC change - stack scanning)

The actual details of code fixes can be found in the notes/readme.md file but they mostly are around the page size and pipe as the sicortex kernel uses an older kernel that does not support pipe2().

I generally build this on a linux machine with a go1.4 (even more ancient - but seems to build the bootstrap ok)

If you happen to have a socirtex machine then you can build a bootstrap version, copy that to a sca node and take it from there.

you will have to bear with my slow progress as I try to get this rolled forward to a more recent version of golang.


 
# The Go Programming Language

Go is an open source programming language that makes it easy to build simple,
reliable, and efficient software.

![Gopher image](doc/gopher/fiveyears.jpg)

Our canonical Git repository is located at https://go.googlesource.com/go.
There is a mirror of the repository at https://github.com/golang/go.

Unless otherwise noted, the Go source files are distributed under the
BSD-style license found in the LICENSE file.

### Download and Install

#### Binary Distributions

Official binary distributions are available at https://golang.org/dl/.

After downloading a binary release, visit https://golang.org/doc/install
or load doc/install.html in your web browser for installation
instructions.

#### Install From Source

If a binary distribution is not available for your combination of
operating system and architecture, visit
https://golang.org/doc/install/source or load doc/install-source.html
in your web browser for source installation instructions.

### Contributing

Go is the work of hundreds of contributors. We appreciate your help!

To contribute, please read the contribution guidelines:
	https://golang.org/doc/contribute.html

Note that the Go project does not use GitHub pull requests, and that
we use the issue tracker for bug reports and proposals only. See
https://golang.org/wiki/Questions for a list of places to ask
questions about the Go language.
