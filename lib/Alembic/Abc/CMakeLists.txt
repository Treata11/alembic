##-*****************************************************************************
##
## Copyright (c) 2009-2015,
##  Sony Pictures Imageworks Inc. and
##  Industrial Light & Magic, a division of Lucasfilm Entertainment Company Ltd.
##
## All rights reserved.
##
## Redistribution and use in source and binary forms, with or without
## modification, are permitted provided that the following conditions are
## met:
## *       Redistributions of source code must retain the above copyright
## notice, this list of conditions and the following disclaimer.
## *       Redistributions in binary form must reproduce the above
## copyright notice, this list of conditions and the following disclaimer
## in the documentation and/or other materials provided with the
## distribution.
## *       Neither the name of Industrial Light & Magic nor the names of
## its contributors may be used to endorse or promote products derived
## from this software without specific prior written permission.
##
## THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
## "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
## LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
## A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
## OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
## SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
## LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
## DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
## THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
## (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
## OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
##
##-*****************************************************************************

LIST(APPEND CXX_FILES
    Abc/ArchiveInfo.cpp
    Abc/ErrorHandler.cpp
    Abc/IArchive.cpp
    Abc/IArrayProperty.cpp
    Abc/ICompoundProperty.cpp
    Abc/IObject.cpp
    Abc/ISampleSelector.cpp
    Abc/IScalarProperty.cpp
    Abc/OArchive.cpp
    Abc/OArrayProperty.cpp
    Abc/OCompoundProperty.cpp
    Abc/OObject.cpp
    Abc/OScalarProperty.cpp
    Abc/Reference.cpp
    Abc/SourceName.cpp
)
SET(CXX_FILES "${CXX_FILES}" PARENT_SCOPE)

SET(ABC_HEADERS
    All.h
    Base.h
    ErrorHandler.h
    Foundation.h
    Argument.h
    ArchiveInfo.h
    IArchive.h
    IArrayProperty.h
    IBaseProperty.h
    ICompoundProperty.h
    IObject.h
    ISampleSelector.h
    IScalarProperty.h
    ISchema.h
    ISchemaObject.h
    ITypedArrayProperty.h
    ITypedScalarProperty.h
    OArchive.h
    OArrayProperty.h
    OBaseProperty.h
    OCompoundProperty.h
    OObject.h
    OScalarProperty.h
    OSchema.h
    OSchemaObject.h
    OTypedArrayProperty.h
    OTypedScalarProperty.h
    Reference.h
    SourceName.h
    TypedArraySample.h
    TypedPropertyTraits.h
)

INSTALL(FILES
   ${ABC_HEADERS}
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/Alembic/Abc
)

IF (USE_TESTS)
    ADD_SUBDIRECTORY(Tests)
ENDIF()
