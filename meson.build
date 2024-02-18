project(
  'pinner',
  ['c'],
  version: '0.1.0.999',
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

geany_dep = dependency('geany')

shared_module(
  meson.project_name(),
  'pinner.c',
  dependencies: [geany_dep],
  install: true,
  name_prefix: '',
  install_dir : join_paths(get_option('prefix'), 'lib', 'geany')
  )
