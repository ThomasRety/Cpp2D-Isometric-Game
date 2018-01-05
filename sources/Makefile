##
## TRISTAN PROJECT, 2018
## CPP 2D isometric Game
## File description:
## makefile for game engine
##

program_NAME := engine


SRC := main.cpp

SRC_DIR	:=	src
OBJ_DIR	:=	obj
INC_DIR	:=	inc

SRC	:=	$(addprefix $(SRC_DIR)/, $(SRC))
OBJ	:=	$(patsubst $(SRC_DIR)%.c, $(OBJ_DIR)%.o, $(SRC))


program_OBJS := $(OBJ)
program_INCLUDE_DIRS := /usr/include/SDL2
program_INCLUDE_DIRS += inc
program_LIBRARY_DIRS :=
program_LIBRARIES := SDL2

CPPFLAGS := -Wall -Wextra -Werror
CPPFLAGS += $(foreach includedir,$(program_INCLUDE_DIRS),-I$(includedir))
LDFLAGS += $(foreach librarydir,$(program_LIBRARY_DIRS),-L$(librarydir))

LDLIBS += $(foreach library,$(program_LIBRARIES),-l$(library))

.PHONY: all clean distclean

all: $(program_NAME)

$(program_NAME): $(program_OBJS)
	$(LINK.cc) $^ -o $@ $(LDLIBS)

clean:
	@- $(RM) $(program_NAME)
	@- $(RM) $(program_OBJS)

distclean: clean
