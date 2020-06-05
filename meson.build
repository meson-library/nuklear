project('nuklear', ['c'], 
         version         : '4.02.5',  
         license         : ['MIT', 'PD'],
         default_options : 'c_std=c99',
         meson_version   : '>= 0.49.0')




name = 'nuklear'




system     = build_machine.system()
cpu        = build_machine.cpu()
cpu_family = build_machine.cpu_family()

cc    = meson.get_compiler('c')
cc_id = cc.get_id() 

lib_type    = get_option('default_library')

includes  = []
sources   = []
c_args    = []
link_args = []

root_include = include_directories('.')




if system not in ['windows']
    error('Script (meson.build) not prepared for your platform yet.')
endif

if system == 'windows' and cc_id not in ['msvc']
    error('Script (meson.build) not prepared for your compiler yet.')
endif




glew_project = subproject('glew')
glew_dep     = glew_project.get_variable('glew_dep')

glfw_project = subproject('glfw')
glfw_dep     = glfw_project.get_variable('glfw_dep')

opengl_dep = cc.find_library('opengl32', required: true)




subdir('src')




if get_option('build_docs')
    subdir('doc')
endif

if get_option('build_examples')
    if not meson.is_subproject()
        subdir('example')
    else
        warning('The option ' + name + ':' + 'build_examples' + ' not work in subproject.')
    endif
endif

if get_option('build_demos')
    if not meson.is_subproject()
        subdir('demo')
    else
        warning('The option ' + name + ':' + 'build_demos' + ' not work in subproject.')
    endif 
endif