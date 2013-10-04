[
  { "make": {
    "name": "re2_make",
    "outs": [ "lib/libre2.so" ]
  } },

  { "cc_library": {
    "name": "re2",
    "cc_headers": [ "re2/filtered_re2.h",
                    "re2/re2.h", 
                    "re2/set.h",
                    "re2/stringpiece.h",
                    "re2/variadic_function.h"
    ],
    "cc_objects": [ "$GEN_DIR/lib/libre2.so" ],
    "dependencies": [ ":re2_make" ],
    "strict_file_mode": false,
    "header_compile_args" : [ "-I$SRC_DIR" ]
  } },

  { "cc_binary": {
    "name": "testinstall",
    "cc_sources": [ "testinstall.cc" ],
    "dependencies": [ ":re2" ]
  } }
]