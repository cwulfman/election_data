LDIR=../lib
SAXON=$(LDIR)/saxon-he-10.5.jar
XQ=$(LDIR)/electionReportFor.xq
XSL=$(LDIR)/cdf1-to-cdf2.xsl


%.v1.cdf.xml:
	java -cp $(SAXON) net.sf.saxon.Query -q:$(XQ) -s:$(SOURCE) municipality=$* -o:v1/$@

%.v2.cdf.xml: v1/%.v1.cdf.xml
	java -cp $(SAXON) net.sf.saxon.Transform -s:$< -xsl:$(XSL) -o:v2/$@
