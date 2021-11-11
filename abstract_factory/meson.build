main_source = files('main.cpp')
project_sources += main_source

inc = include_directories('include')

subdir('source')
subdir('test')

gtest_dep = meson.get_compiler('cpp').find_library('gtest')

e = executable('my_test', sources : test_sources, dependencies : gtest_dep, include_directories : inc)
test('test', e)

#executable('example_task', main_source, include_directories : inc, link_with : source_lib)
executable('example_task', sources : project_sources, include_directories : inc)