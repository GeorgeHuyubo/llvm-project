if(EXISTS ${CMAKE_CURRENT_SOURCE_DIR}/${LIBC_TARGET_OS})
  add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/${LIBC_TARGET_OS})
endif()

add_entrypoint_object(
  statvfs
  ALIAS
  DEPENDS
    .${LIBC_TARGET_OS}.statvfs
)

add_entrypoint_object(
  fstatvfs
  ALIAS
  DEPENDS
    .${LIBC_TARGET_OS}.fstatvfs
)
