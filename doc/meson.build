
doc = executable('doc', 'stddoc.c')

input = '../nuklear.h'
output = 'documentation.html'
install_dir = 'share/docs/nuklear'

documentation = custom_target('documentation',
  input              : input,
  output             : output,
  command            : [doc, '@INPUT@'],
  capture            : true,
  install            : true,
  install_dir        : install_dir)
