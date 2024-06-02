all: pdf html

syl: syllabus.md
	pandoc -o syllabus.pdf syllabus.md

pdf: handout.md
	pandoc -o chatgpt.pdf handout.md

html: handout.md
	pandoc -s -o chatgpt.html handout.md

clean: handout.pdf
	rm *.pdf
