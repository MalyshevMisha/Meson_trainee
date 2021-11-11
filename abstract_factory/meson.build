main_source = files('main.cpp')
project_sources += main_source

inc = include_directories('include')

subdir('source')

executable('example_task', main_source, include_directories : inc, link_with : source_lib)