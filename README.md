Slides
======

A simple [AXEL](https://github.com/ssire/axel) and XSLT application to edit slides to give lectures by S. Sire (courtesy of [www.oppidoc.fr](http://www.oppidoc.fr))

To create some slides open the `course.xhtml` template inside the AXEL sample document editor, then start editing. You MUST of course install the AXEL repository first somewhere on your computer. Then you can save your document as a `sample.xml` file and apply the `course.xsl` XSLT transformation to generate a slideshow, for instance you can use the Saxon XSLT engine at [http://sourceforge.net/projects/saxon/](http://sourceforge.net/projects/saxon/).


## Sample command to generate slides

    java -cp {SAXON-HOME}/saxon9.jar net.sf.saxon.Transform -s:sample1.xml -xsl:course.xsl -o:sample1.xhtml timestamp="`date '+ (generated on %m/%d/%Y)'`"
    
where `{SAXON-HOME}` is the directory where you have installed Saxon.
