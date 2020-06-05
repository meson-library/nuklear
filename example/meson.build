
file_browser = executable('file_browser' 
                       ,sources : ['file_browser.c']
                       ,dependencies        : [glfw_dep, glew_dep, opengl_dep]
                       ,install : true)

extended = executable('extended' 
                       ,sources : ['extended.c']
                       ,dependencies        : [glfw_dep, glew_dep, opengl_dep]
                       ,install : true)

canvas = executable('canvas' 
                       ,sources : ['canvas.c']
                       ,dependencies        : [glfw_dep, glew_dep, opengl_dep]
                       ,install : true)

skinning = executable('skinning' 
                       ,sources : ['skinning.c']
                       ,dependencies        : [glfw_dep, glew_dep, opengl_dep]
                       ,install : true)




install_subdir('icon', install_dir : 'resources')
install_subdir('images', install_dir : 'resources')
install_subdir('skins', install_dir : 'resources')
install_subdir('../extra_font', install_dir : 'resources')