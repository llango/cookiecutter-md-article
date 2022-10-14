# Renders final PDF output file


LATEX_FORM_FILE=latex_formatter.yaml
OUT_DIR=out

.PHONY: format pdf

FILES=`cat toctree.txt`

pdf:
	@mkdir -p $(OUT_DIR)
	pandoc                        		\
	  --from         markdown     		\
	  --to           latex        		\
	  --out          $(OUT_DIR)/report.pdf 	\
	  --template     tex/template.tex 	\
	  --pdf-engine   xelatex      		\
	  --resource-path=.:fig			\
	  --bibliography bib/biblio.bib		\
	  --highlight-style highlight.theme	\
	  $(FILES)

format:
	@echo "格式化文件..."
	latexindent cover.tex -s -o cover.tex -y="defaultIndent: '  '"
	@echo "Deleting log file..."
	rm -f indent.log
	@echo "Done!"

clean:
	@echo "删除输出文件..."
	rm -rf $(OUT_DIR)
	@echo "Done!"

