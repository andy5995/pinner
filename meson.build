project(
  'pinner',
  ['c'],
  version: '0.1.1',
  meson_version : '>= 0.50.0',
  default_options: [
    'warning_level=2',
    ]
  )

# Setup compiler.
cc = meson.get_compiler('c')
extra_flags = [
  '-fno-common',
  '-fstack-protector-strong',
  '-Wformat-security',
  '-Wformat-overflow=3',
  '-Wshadow',
  '-Wstrict-overflow=5'
# '-Wconversion'
  ]

host_sys = host_machine.system()
platform_is_windows = (host_sys == 'windows')

add_project_arguments(cc.get_supported_arguments(extra_flags), language: 'c')

conf = configuration_data()
conf.set_quoted('PINNER_VERSION', meson.project_version())
config_h = configure_file(output : 'config.h', configuration : conf)

geany_dep = dependency('geany')

shared_module(
  meson.project_name(),
  'pinner.c',
  dependencies: [geany_dep],
  install: true,
  name_prefix: '',
  install_dir : join_paths(get_option('prefix'), 'lib', 'geany')
  )
