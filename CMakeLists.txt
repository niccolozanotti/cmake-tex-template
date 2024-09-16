cmake_minimum_required(VERSION 3.20)

set (LATEX DEFAULT BUILD pdflatex)
project(MyDoc NONE)
  include(UseLATEX.cmake)
  add_latex_document(MyDoc.tex TARGET_NAME MyDoc
  INPUTS chapters
  BIBFILES MyDoc.bib
  USE_BIBLATEX
  IMAGE_DIRS assets/images assets/icons
#  USE_INDEX
  EXCLUDE_FROM_ALL
  )
