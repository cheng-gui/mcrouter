BUILT_SOURCES = \
  gen-cpp2/carbon_result_types.cpp \
  gen-cpp2/carbon_result_types.h \
  gen-cpp2/carbon_result_types.tcc \
  gen-cpp2/carbon_result_data.cpp \
  gen-cpp2/carbon_result_data.h \
  gen-cpp2/carbon_types.cpp \
  gen-cpp2/carbon_types.h \
  gen-cpp2/carbon_types.tcc \
  gen-cpp2/carbon_data.cpp \
  gen-cpp2/carbon_data.h

gen-cpp2/carbon_result_types.cpp: gen-cpp2/carbon_result_types.h
gen-cpp2/carbon_result_types.h: gen-cpp2/carbon_result_types.tcc
gen-cpp2/carbon_result_types.tcc: gen-cpp2/carbon_result_data.cpp
gen-cpp2/carbon_result_data.cpp: gen-cpp2/carbon_result_data.h
gen-cpp2/carbon_result_data.h: carbon_result.thrift
	@FBTHRIFT@ -gen mstch_cpp2:include_prefix=mcrouter/lib/carbon/ carbon_result.thrift

gen-cpp2/carbon_types.cpp: gen-cpp2/carbon_types.h
gen-cpp2/carbon_types.h: gen-cpp2/carbon_types.tcc
gen-cpp2/carbon_types.tcc: gen-cpp2/carbon_data.cpp
gen-cpp2/carbon_data.cpp: gen-cpp2/carbon_data.h
gen-cpp2/carbon_data.h: carbon.thrift
	@FBTHRIFT@ -gen mstch_cpp2:include_prefix=mcrouter/lib/carbon/ carbon.thrift
