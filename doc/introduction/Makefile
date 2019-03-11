# Proposal makefile

NAME=$(shell basename $(realpath .))
BUILD_DIR=build
FLAGS= -output-directory $(BUILD_DIR) -jobname $(NAME) -file-line-error

all: output

clean:
	-rm build/*

output: doc
	mv build/$(NAME).pdf .

doc:
	mkdir -p $(BUILD_DIR)
	pdflatex $(FLAGS) main.tex
	bibtex $(BUILD_DIR)/$(NAME)
	pdflatex $(FLAGS) main.tex
	pdflatex $(FLAGS) main.tex
