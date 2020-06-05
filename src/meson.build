#
#   Inside build directory run 'ninja generate' to generate the 'nuklear.h' header in the parent directory.
#

script = 'paq'
if system == 'windows'
    script += '.bat'
endif




run_target('generate', command : script)




install_headers('../nuklear.h', 
                 subdir : 'nuklear')

install_data(['LICENSE'],
               rename      : ['LICENSE'],
               install_dir :  'share/licenses/nuklear')