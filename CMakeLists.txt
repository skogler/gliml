add_library(gliml INTERFACE)
target_sources(gliml INTERFACE
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml.h
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml.inl
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_dds.h
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_dds.inl
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_ktx.h
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_ktx.inl
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_pvr.h
${CMAKE_CURRENT_SOURCE_DIR}/include/gliml_pvr.inl
)
target_include_directories(gliml INTERFACE include)
if (MSVC)
else()
	target_compile_options(gliml PRIVATE -w)
endif()

