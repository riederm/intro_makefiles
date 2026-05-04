# intro_makefiles

Small example project showing how a Makefile for a tiny C "firmware" (main + uart + led) evolves from explicit rules to pattern rules.

## 01_simple_firmware
Minimal Makefile with one explicit rule per object file. Every `.c -> .o` step and the final link are written out by hand. Good starting point to see what `make` is actually doing before any abstractions.

## 02_pattern_rule
Same sources, same output, but the Makefile is rewritten using variables (`CC`, `CFLAGS`, `SRCS`, `OBJS`), a pattern rule (`build/%.o: %.c`) and automatic variables (`$@`, `$^`, `$<`). Adding a new source file now only requires extending `SRCS`.
