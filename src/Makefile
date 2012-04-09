# This is a makefile that builds the Nenets morphological parser
# *****************************************************************


# This is a preliminary file that builds a Skolt Sami parser based upon
# xfst and not twolc.



XFST = xfst 
LEXC = lexc 
TWOLC = twolc

ifeq (victorio.uit.no, $(shell hostname))
XFST = /opt/sami/xerox/c-fsm/ix86-linux2.6-gcc3.4/bin/fst -utf8
LEXC = /opt/sami/xerox/bin/lexc -utf8
TWOLC = /opt/sami/xerox/bin/twolc -utf8
endif


SRC = yrk-lex.txt \
	noun-yrk-morph.txt \
	noun-yrk-lex.txt \
	adj-yrk-lex.txt \
	adv-yrk-lex.txt \
	verb-yrk-lex.txt \
	verb-yrk-morph.txt \
	num-yrk-lex.txt \
	num-yrk-morph.txt \
	pron-yrk-morph.txt \
#	punct-yrk-lex.txt \
	pp-yrk-lex.txt

# Here we build the final generator , an inverted transducer of the analyzer.
# It is dependent upon yrk.save

iyrk.fst: ../bin/iyrk.fst
../bin/iyrk.fst: ../bin/yrk.fst ../bin/yrk-num.fst
	@echo
	@echo "*** Building the inverse iyrk.fst ***"
	@echo
	@printf "load ../bin/yrk.save \n\
	invert net \n\
	save stack ../bin/iyrk.fst \n\
	quit \n" > ../../tmp/iyrk-fst-script
	$(XFST) < ../../tmp/iyrk-fst-script
	@rm -f ../../tmp/iyrk-fst-script


# This goal is to build the final analyser. It depends on all the files.

yrk.fst: ../bin/yrk.fst
../bin/yrk.fst: ../bin/yrk.save ../bin/caseconv.fst
	@echo
	@echo "*** Building yrk.fst ***" ;
	@echo
	@printf "read regex [[@\"../bin/yrk.save\"] .o. \
	[@\"../bin/caseconv.fst\"]] ; \n\
	save stack ../bin/yrk.fst \n\
	quit \n" > ../../tmp/yrk-fst-script
	$(XFST) < ../../tmp/yrk-fst-script
	@rm -f ../../tmp/yrk-fst-script


# The second goal is to build the caseconv.fst file
# This goal depends on case.regex

caseconv.fst: ../bin/caseconv.fst
../bin/caseconv.fst: case.regex
	@echo
	@echo "*** Building caseconv.fst ***" ;
	@echo
	@printf "read regex < case.regex \n\
	save stack ../bin/caseconv.fst \n\
	quit \n" > ../../tmp/caseconv-script
	$(XFST) < ../../tmp/caseconv-script
	@rm -f ../../tmp/caseconv-script





yrk.save: ../bin/yrk.save
../bin/yrk.save: ../bin/xfst-yrk.bin ../bin/yrk-lex.save
	@echo
	@echo "*** Building the parser yrk.save ***"
	@echo
	@printf "read regex [[@\"../bin/yrk-lex.save\"] .o. \
	[@\"../bin/xfst-yrk.bin\"]] ; \n\
	save stack ../bin/yrk.save \n\
	quit \n" > ../../tmp/yrk-save-script
	$(XFST) < ../../tmp/yrk-save-script
	@rm -f ../../tmp/yrk-save-script

# The first goal is to build yrk-lex.save
# This goal depends on a bunch of lexicon files

yrk-lex.save: ../bin/yrk-lex.save
../bin/yrk-lex.save: $(SRC)
	@echo
	@echo "*** Building yrk-lex.save ***" ;
	@echo
	printf "compile-source $(SRC) \n\
	save-source ../bin/yrk-lex.save \n\
	quit \n" > ../../tmp/yrk-lex-save-script
	$(LEXC) < ../../tmp/yrk-lex-save-script
	rm -f ../../tmp/yrk-lex-save-script

# The second goal is to build xfst-yrk.bin
# This goal depends on xfst-yrk.txt

xfst-yrk.bin: ../bin/xfst-yrk.bin
../bin/xfst-yrk.bin: xfst-yrk.txt
	@echo
	@echo "*** Building xfst-yrk.bin ***" ;
	@echo
	@printf "source xfst-yrk.txt \n\
	save stack ../bin/xfst-yrk.bin \n\
	quit \n" > ../../tmp/xfst-yrk-script
	$(XFST) < ../../tmp/xfst-yrk-script
	@rm -f ../../tmp/xfst-yrk-script


# And yes, the number generator.

yrk-num.fst: ../bin/yrk-num.fst
../bin/yrk-num.fst: yrk-num.txt
	@echo
	@echo "*** Building $(notdir $@) ***" ;
	@echo
	$(XFST) -e "read lexc < $< " \
		-e "save stack   $@ " \
		-stop



clean:
	@rm -f ../bin/*.bin ../bin/*.fst ../bin/*.save


