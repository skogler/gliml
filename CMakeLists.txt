add_library(gliml INTERFACE
	include/gliml.h
	include/gliml.inl
	include/gliml_dds.h
	include/gliml_dds.inl
	include/gliml_ktx.h
	include/gliml_ktx.inl
	include/gliml_pvr.h
	include/gliml_pvr.inl
)
target_include_directories(gliml INTERFACE include)
if (MSVC)
else()
	target_compile_options(gliml PRIVATE -w)
endif()

