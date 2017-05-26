PYUIC = pyuic5
RCC = rcc
PYRCC = pyrcc5

GUI_CLASSES = gui.py
RCCS = icons.rcc
PYRCCS = icons_rc.py

all: $(GUI_CLASSES) $(RCCS) $(PYRCCS)

%.rcc: %.qrc
	$(RCC) $< -o $@

%_rc.py: %.qrc
	$(PYRCC) $< -o $@

%.py: %.ui
	$(PYUIC) $< -o $@

clean:
	rm -f $(GUI_CLASSES) $(RCCS) $(PYRCCS)
	rm -f *.pyc
