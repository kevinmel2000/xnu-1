export MakeInc_cmd=${SRCROOT}/makedefs/MakeInc.cmd
export MakeInc_def=${SRCROOT}/makedefs/MakeInc.def
export MakeInc_rule=${SRCROOT}/makedefs/MakeInc.rule
export MakeInc_dir=${SRCROOT}/makedefs/MakeInc.dir

IOKIT_FRAMEDIR = $(FRAMEDIR)/IOKit.framework/Versions/A
export INCDIR = $(IOKIT_FRAMEDIR)/Headers
export LCLDIR = $(IOKIT_FRAMEDIR)/PrivateHeaders

include $(MakeInc_cmd)
include $(MakeInc_def)

MD_DIR = ata
NOT_EXPORT_HEADERS = IOATADevice_Reference.h IOATACommand_Reference.h	\
		  IOATAController_Reference.h IOATADriver_Reference.h	\
		  IOATAStandardInterface.h

INSTINC_SUBDIRS =
INSTINC_SUBDIRS_PPC =
INSTINC_SUBDIRS_I386 = ata-device

EXPINC_SUBDIRS = ${INSTINC_SUBDIRS}
EXPINC_SUBDIRS_PPC = ${INSTINC_SUBDIRS_PPC}
EXPINC_SUBDIRS_I386 = ${INSTINC_SUBDIRS_I386}

ALL_HEADERS = $(shell (cd $(SOURCE); echo *.h))

INSTALL_MD_LIST	= 
INSTALL_MD_LCL_LIST = ""
INSTALL_MD_DIR = $(MD_DIR)

EXPORT_MD_LIST	= $(filter-out $(NOT_EXPORT_HEADERS), $(ALL_HEADERS))
EXPORT_MD_DIR = IOKit/$(MD_DIR)

include $(MakeInc_rule)
include $(MakeInc_dir)
