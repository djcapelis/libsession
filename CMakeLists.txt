# Project configuration for libsession
project(libsession)
cmake_minimum_required(VERSION 2.6) # Unclear whether this is actually the minimum, but it is a safe choice for now

# The libsession library 
add_library(session SHARED src/libsession.c)

# Library Versioning Information
set(LIBSESSION_VERSION_MAJOR 0)
set(LIBSESSION_VERSION_MINOR prerelease)
set(LIBSESSION_VERSION_PATCH unstable)
set(LIBSESSION_VERSION_STRING ${LIBSESSION_VERSION_MAJOR}.${LIBSESSION_VERSION_MINOR}.${LIBSESSION_VERSION_PATCH})

set_target_properties(session PROPERTIES VERSION ${LIBSESSION_VERSION_STRING} SOVERSION ${LIBSESSION_VERSION_MAJOR})
