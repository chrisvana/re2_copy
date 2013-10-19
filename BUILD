[
  { "make": {
    "name": "re2_make",
    "pass_flags": "full",
    "outs": [ "$GEN_DIR/lib/libre2.a" ],
    "licenses": [ "http://opensource.org/licenses/BSD-3-Clause" ]
  } },

  { "cc_library": {
    "name": "re2",
    "cc_headers": [ "re2/filtered_re2.h",
                    "re2/re2.h", 
                    "re2/set.h",
                    "re2/stringpiece.h",
                    "re2/variadic_function.h"
    ],
    "cc_objects": [ "$GEN_DIR/lib/libre2.a" ],
    "dependencies": [ ":re2_make" ],
    "strict_file_mode": false,
    "cc_include_dirs": [ "." ]
  } },

  { "cc_test": {
    "name": "testinstall",
    "cc_sources": [ "testinstall.cc" ],
    "dependencies": [ ":re2" ]
  } }
]