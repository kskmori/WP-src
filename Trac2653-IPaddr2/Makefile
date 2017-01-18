#
#
#

PROXY ?= $(shell echo ${http_proxy} | cut -d '/' -f 3 )

# make sure that you have correctly configured ~/.blogpost
BLOGPOST=blogpost.py
#BLOGPOST_OPTS=-u --proxy=$(PROXY)
BLOGPOST_OPTS=--force -U --proxy=$(PROXY)

ASCIIDOC_OPTS=-a toc -a icons -a iconsdir=/images/icons -a numbered

SRCFILE=Trac2653-IPaddr2-community.txt

all:
	@echo make html
	@echo make post

html:
	asciidoc $(ASCIIDOC_OPTS) $(SRCFILE)

post:
	$(BLOGPOST) $(BLOGPOST_OPTS) --asciidoc-opt="$(ASCIIDOC_OPTS)" post $(SRCFILE)
