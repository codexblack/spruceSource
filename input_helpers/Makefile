TARGET  = getevent sendevent joystickinput joypad setlcdbl devlogger setsharedmem
CROSS   = arm-linux-

WARMINGS = -pedantic -Wall -Wextra -Wcast-align -Wcast-qual -Wdisabled-optimization -Wformat=2 -Winit-self -Wlogical-op -Wmissing-include-dirs  -Wredundant-decls -Wshadow -Wsign-conversion -Wstrict-overflow=5 -Wundef
WARMINGS += -Wmissing-declarations 

export PATH=/opt/a30/bin:$(shell echo $$PATH)

all: $(TARGET)

setsharedmem: setsharedmem.c
	$(CROSS)gcc  setsharedmem.c -o setsharedmem -O3 $(WARMINGS)

devlogger: devlogger.c
	$(CROSS)gcc  devlogger.c -o devlogger -O3 $(WARMINGS)

setlcdbl: setlcdbl.c
	$(CROSS)gcc  setlcdbl.c -o setlcdbl -O3 $(WARMINGS)

joypad: joypad.c
	$(CROSS)gcc joypad.c -o joypad -O3 $(WARMINGS)

joystickinput: joystickinput.c
	$(CROSS)gcc joystickinput.c -o joystickinput -O3 $(WARMINGS)

getevent: getevent.c
	$(CROSS)gcc getevent.c -o getevent -O3 $(WARMINGS)

sendevent: sendevent.c
	$(CROSS)gcc sendevent.c -o sendevent -O3 $(WARMINGS)

clean:
	rm -rf $(TARGET) *.o
