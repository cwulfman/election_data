LDIR=../lib
SAXON=$(LDIR)/saxon-he-10.5.jar
XQ=$(LDIR)/electionReportFor.xq


%.v1.cdf.xml:
	java -cp $(SAXON) net.sf.saxon.Query -q:$(XQ) -s:$(SOURCE) municipality=$* -o:v1/$@
