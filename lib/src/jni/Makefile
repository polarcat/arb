cc = gcc
out = playground
src = main.c \
lib3d/gl.c \
lib3d/gm.c \
lib3d/bg.c \
lib3d/img.c \
lib3d/font.c \
lib3d/draw.c \
lib3d/pip.c \
lib3d/cv.c \
lib3d/sb.c \
lib3d/plotter.c \
lib3d/tools.c \
lib3d/icon.c \
lib3d/game.c \
lib3d/wfobj.c \
utils/image.c \
utils/asset.c \
utils/sensors.c \

game = game/sources.mk

ifneq ("$(wildcard $(game))","")
include $(game)
endif

flags = -I. -Ilib3d -DASSETS="\"../main/assets/\"" -DHAVE_ALGO
libs = -lxcb -lxcb-keysyms -lEGL -lGLESv2 -lm -lpng -ljpeg -lv4l2

.PHONY: FORCE all

all: FORCE
	$(cc) -o $(out) $(src) $(libs) $(flags) $(CFLAGS)
