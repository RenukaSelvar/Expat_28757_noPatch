#
#                          __  __            _
#                       ___\ \/ /_ __   __ _| |_
#                      / _ \\  /| '_ \ / _` | __|
#                     |  __//  \| |_) | (_| | |_
#                      \___/_/\_\ .__/ \__,_|\__|
#                               |_| XML parser
#
# Copyright (c) 2017 Expat development team
# Licensed under the MIT license:
#
# Permission is  hereby granted,  free of charge,  to any  person obtaining
# a  copy  of  this  software   and  associated  documentation  files  (the
# "Software"),  to  deal in  the  Software  without restriction,  including
# without  limitation the  rights  to use,  copy,  modify, merge,  publish,
# distribute, sublicense, and/or sell copies of the Software, and to permit
# persons  to whom  the Software  is  furnished to  do so,  subject to  the
# following conditions:
#
# The above copyright  notice and this permission notice  shall be included
# in all copies or substantial portions of the Software.
#
# THE  SOFTWARE  IS  PROVIDED  "AS  IS",  WITHOUT  WARRANTY  OF  ANY  KIND,
# EXPRESS  OR IMPLIED,  INCLUDING  BUT  NOT LIMITED  TO  THE WARRANTIES  OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN
# NO EVENT SHALL THE AUTHORS OR  COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
# DAMAGES OR  OTHER LIABILITY, WHETHER  IN AN  ACTION OF CONTRACT,  TORT OR
# OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
# USE OR OTHER DEALINGS IN THE SOFTWARE.

SUBDIRS = . benchmark

AM_CPPFLAGS = -I$(srcdir)/../lib

noinst_LIBRARIES = libruntests.a

check_PROGRAMS = runtests runtestspp
TESTS = runtests runtestspp

# To support MinGW and Non-MinGW at the same time:
LOG_DRIVER = $(srcdir)/../test-driver-wrapper.sh

libruntests_a_SOURCES = \
    acc_tests.c \
    chardata.c \
    structdata.c \
    memcheck.c \
    minicheck.c

runtests_SOURCES = \
    runtests.c

runtestspp_SOURCES = \
    runtestspp.cpp

runtests_LDADD = libruntests.a ../lib/libexpat.la
runtestspp_LDADD = libruntests.a ../lib/libexpat.la

EXTRA_DIST = \
    acc_tests.h \
    chardata.h \
    structdata.h \
    minicheck.h \
    memcheck.h \
    README.txt \
    udiffer.py \
    xmltest.log.expected \
    xmltest.sh
