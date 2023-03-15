libnih_dependency = dependency('libnih',
  version: '>= 1.0.0',
)

blkid_dependency = dependency('blkid',
  version: '>= 2.16',
)

ext2fs_dependency = dependency('ext2fs',
  version: '>= 1.41',
)

ureadahead_dependencies = [
  libnih_dependency,
  blkid_dependency,
  ext2fs_dependency,
]

ureadahead_sources = [
  'ureadahead.c',
  'trace.c',
  'pack.c',
  'values.c',
  'file.c',
]

ureadahead_headers = [
  'trace.h',
  'pack.h',
  'values.h',
  'file.h',
  'errors.h',
]

ureadahead_executale = executable('ureadahead',
  sources: ureadahead_sources + ureadahead_headers + ureadahead_config_header,
  dependencies: ureadahead_dependencies,
  include_directories: ureadahead_config_header_directory,
  install: true,
)
