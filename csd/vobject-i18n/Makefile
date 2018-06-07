SRC  := $(wildcard csd-*.adoc)
XML  := $(patsubst %.adoc,%.xml,$(SRC))
HTML := $(patsubst %.adoc,%.html,$(SRC))
PDF  := $(patsubst %.adoc,%.pdf,$(SRC))

SHELL := /bin/bash

all: $(PDF) $(HTML) $(XML)

clean:
	rm -f $(PDF) $(HTML) $(XML)

%.html %.xml %.pdf: %.adoc
	bundle exec metanorma -t csd $^

open:
	open $(HTML)
