# Run cpuset tests
# Suite design taken from git which is Copyright (c) 2005 Junio C Hamano
#
# Copyright (C) 2007 Novell Inc.
# Author: Alex Tsariounov <tsariounov@gmail.com>
#

#CSET_TEST_OPTS=--verbose --debug
SHELL_PATH ?= $(SHELL)
TAR ?= $(TAR)

# Shell quote;
SHELL_PATH_SQ = $(subst ','\'',$(SHELL_PATH))

T = $(wildcard t[0-9][0-9][0-9][0-9]-*.sh)

all: $(T) clean

$(T):
	@echo "*** $@ ***"; '$(SHELL_PATH_SQ)' $@ $(GIT_TEST_OPTS)

clean:
	rm -fr trash

.PHONY: $(T) clean
.NOPARALLEL:

