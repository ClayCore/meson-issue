project('example', 'c', version: '0.1.0', default_options: ['c_std=c17', 'warning_level=3'])

compiler = meson.get_compiler('c')

all_deps = []

common_includes = [
  include_directories('shared/include'),
  include_directories('src')
]

all_includes = [
    common_includes,
]

cc_flags = []
add_project_arguments(compiler.get_supported_arguments(cc_flags), language: 'c')

mainsources = [
  'src/main.c'
]

executable(
  'example', 
  mainsources, 
  include_directories: all_includes, 
  c_args: cc_flags, 
  dependencies:all_deps
)
