#
#
#

# make sure that you have correctly configured ~/.blogpost
BLOGPOST=blogpost.py
BLOGPOST_OPTS=--force -u --proxy=172.19.0.3:8080
#BLOGPOST_OPTS=--force -U --proxy=172.19.0.3:8080

ASCIIDOC_OPTS=-a toc -a icons -a iconsdir=/images/icons -a numbered

SRCFILE=PM-1.1.14-1.1.txt

all:
	@echo make html
	@echo make post

html:
	asciidoc $(ASCIIDOC_OPTS) $(SRCFILE)

post:
	$(BLOGPOST) $(BLOGPOST_OPTS) $(ASCIIDOC_OPTS) post $(SRCFILE)
#	$(BLOGPOST) $(BLOGPOST_OPTS) --asciidoc-opt="$(ASCIIDOC_OPTS)" post $(SRCFILE)
