#
# %CopyrightBegin%
#
# Copyright Ericsson AB 1997-2023. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# %CopyrightEnd%
#
include $(ERL_TOP)/make/target.mk
include $(ERL_TOP)/make/$(TARGET)/otp.mk

# ----------------------------------------------------
# Application version
# ----------------------------------------------------
include ../../vsn.mk
VSN=$(TOOLS_VSN)
APPLICATION=tools

# ----------------------------------------------------
# Target Specs
# ----------------------------------------------------
XML_APPLICATION_FILES = ref_man.xml

XML_REF3_FILES = \
	cover.xml \
	eprof.xml \
	hprof.xml \
	fprof.xml \
	cprof.xml \
	lcnt.xml \
	make.xml \
	tags.xml \
	xref.xml \
	erlang_mode.xml

XML_PART_FILES = part.xml

XML_CHAPTER_FILES = \
	cover_chapter.xml \
	fprof_chapter.xml \
	cprof_chapter.xml \
	lcnt_chapter.xml \
	erlang_mode_chapter.xml \
	xref_chapter.xml \
	notes.xml

BOOK_FILES = book.xml

XML_FILES = \
	$(BOOK_FILES) $(XML_CHAPTER_FILES) \
	$(XML_PART_FILES) $(XML_REF3_FILES) $(XML_APPLICATION_FILES)

IMAGE_FILES = \
	venn1.gif \
	venn2.gif

TOP_SPECS_FILE = specs.xml

NO_CHUNKS = erlang_mode.xml

# ----------------------------------------------------

# erlang_mode doesn't have erlang source so we generate a dummy file for it.
$(SPECDIR)/specs_erlang_mode.xml:
	$(gen_verbose)echo '<module name="erlang_mode"/>' > $(SPECDIR)/specs_erlang_mode.xml

# ----------------------------------------------------
include $(ERL_TOP)/make/doc.mk
