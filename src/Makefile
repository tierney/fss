SSOBJ=ss.o ssfilter.o
LNSTATOBJ=lnstat.o lnstat_util.o

TARGETS=ss

include ../Config

all: $(TARGETS)

ss: $(SSOBJ) $(LIBUTIL)

install: all
	install -m 0755 $(TARGETS) $(DESTDIR)$(SBINDIR)
	ln -sf lnstat $(DESTDIR)$(SBINDIR)/rtstat
	ln -sf lnstat $(DESTDIR)$(SBINDIR)/ctstat

clean:
	rm -f *.o $(TARGETS) ssfilter.c
