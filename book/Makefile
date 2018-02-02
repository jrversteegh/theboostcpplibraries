XML_SOURCE := *.xml


all: book.pdf


book.fo: $(XML_SOURCE)
	xsltproc /usr/share/xml/docbook/stylesheet/docbook-xsl/fo/docbook.xsl index.xml > book.fo


book.pdf: book.fo
	fop -r book.fo book.pdf


.PHONY: clean
clean:
	rm -f book.fo book.pdf
