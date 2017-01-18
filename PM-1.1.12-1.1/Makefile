#
#
#

PROXY ?= $(shell echo ${http_proxy} | cut -d '/' -f 3 )

# make sure that you have correctly configured ~/.blogpost
BLOGPOST=blogpost.py
BLOGPOST_OPTS=--force -u --proxy=$(PROXY)
#BLOGPOST_OPTS=--force -U --proxy=$(PROXY)

ASCIIDOC_OPTS=-a toc -a icons -a iconsdir=/images/icons -a numbered

SRCFILE=PM-1.1.12-1.1.txt

all:
	@echo make html
	@echo make post

html:
	asciidoc $(ASCIIDOC_OPTS) $(SRCFILE)

post:
	$(BLOGPOST) $(BLOGPOST_OPTS) $(ASCIIDOC_OPTS) post $(SRCFILE)
#	$(BLOGPOST) $(BLOGPOST_OPTS) --asciidoc-opt="$(ASCIIDOC_OPTS)" post $(SRCFILE)
