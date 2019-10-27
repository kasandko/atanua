all: atanua

atanua-cpp-src = \
chip/7segchip.cpp \
chip/16segchip.cpp \
chip/and3chip.cpp \
chip/and8chip.cpp \
chip/andchip.cpp \
chip/audiochip.cpp \
chip/box.cpp \
chip/buttonchip.cpp \
chip/chip27xx.cpp \
chip/chip309.cpp \
chip/chip2051.cpp \
chip/chip7400.cpp \
chip/chip7402.cpp \
chip/chip7404.cpp \
chip/chip7408.cpp \
chip/chip7410.cpp \
chip/chip7420.cpp \
chip/chip7432.cpp \
chip/chip7447.cpp \
chip/chip7473.cpp \
chip/chip7474.cpp \
chip/chip7485.cpp \
chip/chip7486.cpp \
chip/chip7489.cpp \
chip/chip7490.cpp \
chip/chip74138.cpp \
chip/chip74139.cpp \
chip/chip74151.cpp \
chip/chip74154.cpp \
chip/chip74163.cpp \
chip/chip74164.cpp \
chip/chip74165.cpp \
chip/chip74181.cpp \
chip/chip74191.cpp \
chip/chip74192.cpp \
chip/chip74193.cpp \
chip/chip74195.cpp \
chip/chip74240.cpp \
chip/chip74241.cpp \
chip/chip74244.cpp \
chip/chip74245.cpp \
chip/chip74283.cpp \
chip/chip74574.cpp \
chip/clockchip.cpp \
chip/dchip.cpp \
chip/dflipflop.cpp \
chip/dxchip.cpp \
chip/extpin.cpp \
chip/extrapin.cpp \
chip/jkchip.cpp \
chip/jkflipflop.cpp \
chip/label.cpp \
chip/ledchip.cpp \
chip/ledgrid.cpp \
chip/logicprobe.cpp \
chip/muxchip.cpp \
chip/nand3chip.cpp \
chip/nand8chip.cpp \
chip/nandchip.cpp \
chip/nor3chip.cpp \
chip/nor8chip.cpp \
chip/norchip.cpp \
chip/notchip.cpp \
chip/or3chip.cpp \
chip/or8chip.cpp \
chip/orchip.cpp \
chip/sedchip.cpp \
chip/serchip.cpp \
chip/srchip.cpp \
chip/srflipflop.cpp \
chip/srnegchip.cpp \
chip/staticlevelchip.cpp \
chip/stepper.cpp \
chip/switchchip.cpp \
chip/tchip.cpp \
chip/tflipflop.cpp \
chip/xorchip.cpp \
core/AtanuaConfig.cpp \
core/basechipfactory.cpp \
core/BoxStitchingInformation.cpp \
core/chip.cpp \
core/fileio.cpp \
core/fileutils.cpp \
core/main.cpp \
core/nativefunctions.cpp \
core/net.cpp \
core/pin.cpp \
core/pluginchip.cpp \
core/pluginchipfactory.cpp \
core/simutils.cpp \
core/slidingaverage.cpp \
core/wire.cpp \
tinyxml/tinystr.cpp \
tinyxml/tinyxml.cpp \
tinyxml/tinyxmlerror.cpp \
tinyxml/tinyxmlparser.cpp \
basecode/angelcodefont.cpp \
basecode/mersennetwister.cpp \
basecode/toolkit.cpp \

atanua-c-src = \
8051/core.c \
8051/disasm.c \
8051/opcodes.c \
stb/stb_image.c \
stb/stb_image_write.c

atanua-obj = $(atanua-cpp-src:.cpp=.o) $(atanua-c-src:.c=.o)

CXX = clang
CC = clang

CXXFLAGS = \
-O3 \
-I/usr/include/c++/4.5 \
-I/usr/include/c++/4.5/i686-linux-gnu \
-I/usr/X11R6/include \
-Itinyxml \
-I/usr/include/gtk-3.0 \
-I/usr/include/cairo \
-I/usr/include/glib-2.0 \
-I/usr/lib/glib-2.0/include \
-I/usr/include/pango-1.0 \
-I/usr/lib/gtk-3.0/include \
-I/usr/include/atk-1.0 \
-I/usr/lib/i386-linux-gnu/glib-2.0/include \
-I/usr/lib/x86_64-linux-gnu/glib-2.0/include \
-I/usr/include/gdk-pixbuf-2.0 \
-I/usr/include/harfbuzz/ \
-Iinclude \
-Itinyxml \
-I./



atanua: $(atanua-obj)
	$(CXX) `pkg-config --cflags gtk+-3.0` `pkg-config --cflags glib-2.0` -o $@ $(atanua-obj) -L. -lSDLmain -lSDL -lGL -lGLU -lGLee -lm -ldl -lstdc++ `pkg-config --libs gtk+-3.0` `pkg-config --libs glib-2.0` -O3 $(CXXFLAGS)

clean:
	rm $(atanua-obj) atanua

