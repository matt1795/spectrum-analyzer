# Proposal makefile

CC=pdflatex
NAME=$(shell basename $(realpath .))
FLAGS= -output-directory build -jobname $(NAME) -file-line-error

all: doc

clean:
	-rm ../../output/$(NAME).pdf
	-rm build/*

output: doc
	mv build/$(NAME).pdf ../../output/

doc:
	-$(CC) $(FLAGS) main.tex
