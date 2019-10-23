###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C51
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = C:\Windows\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  E:/博士后/教学/计组实验 教学改革/PROTEUS系列实验/SCUT版实验系列final/第三章 计算机体系结构实验系列 2017版/实验3.3 流水线版CPU/80C51/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     E:/博士后/教学/计组实验 教学改革/PROTEUS系列实验/SCUT版实验系列final/第三章 计算机体系结构实验系列 2017版/实验3.3 流水线版CPU/PROGRAMS/JS.ASM

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../../PROGRAMS/JS.ASM 
	$(ASM) "..\..\PROGRAMS\JS.ASM" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"C:\Program Files\Labcenter Electronics\Proteus 8 Professional\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI

