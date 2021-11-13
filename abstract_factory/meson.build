main_source = files('main.cpp')

inc = include_directories('include')

subdir('source')
subdir('test')

#executable('example_task', main_source, include_directories : inc, link_with : source_lib)

#gtest_dep = meson.get_compiler('cpp').find_library('gtest')
gtest_dep = dependency('gtest', main : true, required : false)

if gtest_dep.found()
e = executable('testprog', sources : [test_sources, project_sources], dependencies : gtest_dep, include_directories : inc)
test('gtest test', e)
else
executable('example_task', sources : [project_sources, main_source], include_directories : inc)
endif

#e = executable('my_test', sources : [test_sources, project_sources], dependencies : gtest_dep, include_directories : inc)
#test('mytest', e)