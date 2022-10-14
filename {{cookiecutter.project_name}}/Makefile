# 呈现最终的PDF输出文件


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
	  --citeproc  \
	  --bibliography bib/biblio.bib		\
	  -M reference-section-title="参考文献"		\
	  --highlight-style highlight.theme	\
	  $(FILES)

format:
	@echo "格式化文件..."
	latexindent cover.tex -s -o cover.tex -y="defaultIndent: '  '"
	@echo "删除日志文件..."
	rm -f indent.log
	@echo "已完成!"

clean:
	@echo "删除输出文件..."
	rm -rf $(OUT_DIR)
	@echo "已完成!"

