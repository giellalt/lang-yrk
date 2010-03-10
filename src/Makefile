XFST = xfst


yrk-num.fst: ../bin/yrk-num.fst
../bin/yrk-num.fst: yrk-num.txt
	@echo
	@echo "*** Building $(notdir $@) ***" ;
	@echo
	$(XFST) -e "read lexc < $< " \
		-e "save stack   $@ " \
		-stop

