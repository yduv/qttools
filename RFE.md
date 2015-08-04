## Introduction ##
.pro File for the Resource File Editor. Copy to a file RFE.pro and call qmake to create a project file for your favourite IDE / programming enviornment.
The .pro File is now included in the repository.
```
TEMPLATE     = app
TARGET       = RFE
DEPENDPATH  += . RFE_ImagePreview RFE_MainWindow RFE_StandardItem RFE_Widget
INCLUDEPATH += . RFE_ImagePreview RFE_MainWindow RFE_StandardItem RFE_Widget
RESOURCES    = icons.qrc

HEADERS = RFE_ImagePreview/RFE_ImagePreview.h \
          RFE_MainWindow/RFE_MainWindow.h \
          RFE_StandardItem/RFE_StandardItem.h \
          RFE_Widget/RFE_Widget.h
SOURCES = main.cpp \
          RFE_ImagePreview/RFE_ImagePreview.cpp \
          RFE_MainWindow/RFE_MainWindow.cpp \
          RFE_StandardItem/RFE_StandardItem.cpp \
          RFE_Widget/RFE_Widget.cpp
TRANSLATIONS = translations/RFE_de.ts
```

The RFE has been compiled, linked and tested against Qt 4.3, 4.4 and 4.5

If you have the PFG you could use it for generating the project file instead of taking this one.

e.g.:

PFG --name RFE --output-file ~/qttools/RFE/RFE.pro --input-dir ~/qttools/RFE/