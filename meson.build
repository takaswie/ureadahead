project('ureadahead', 'c',
  version: '0.2.0',
  license: 'GPL-2.0',
)

conf = configuration_data()
conf.set_quoted('PACKAGE_NAME', meson.project_name())
conf.set_quoted('PACKAGE_VERSION', meson.project_version())
conf.set_quoted('PACKAGE_BUGREPORT', 'hoge')

ureadahead_config_header = configure_file(
  input: 'config.h.template',
  output: 'config.h',
  configuration: conf,
)

ureadahead_config_header_directory = include_directories('.')

add_project_arguments('-DHAVE_CONFIG_H', language: 'c')

subdir('src')
