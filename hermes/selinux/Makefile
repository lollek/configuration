PACKAGES = $(addsuffix .pp, $(basename $(wildcard *.te)))

all: $(PACKAGES)
.PHONY: all

%.mod: %.te
	checkmodule -M -m -o $*.mod $*.te

%.pp: %.mod
	semodule_package -o $*.pp -m $*.mod

clean:
	$(RM) $(PACKAGES)
