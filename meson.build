project('cpp-template', 'c',
  version : '0.1',
  default_options : ['warning_level=3', 'cpp_std=c++14'])

exe = executable('cpp_template', 'cpp_template.c',
  install : true)
#subproject('gtest')
cmake = import('cmake')
opt_var = cmake.subproject_options()
opt_var.set_override_option('cpp_std', 'c++17')
#poco_base = cmake.subproject = cmake.subproject('cmake-base')
#poco_base = cmake.subproject('poco-base')
#poco_deps = [poco_base.dependency('Encodings'), poco_base.dependency('JSON'), poco_base.dependency('Util'), poco_base.dependency('Net')]
poco_all = cmake.subproject('poco-all', options: opt_var)
#poco_basic = subproject('poco-base')
#poco_dep = poco_basic.get_variable('poco_basic')
#poco_all = subproject('pocoall')
test('basic', exe)
