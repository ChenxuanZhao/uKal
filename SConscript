    
from building import *
import rtconfig

# get current directory
cwd     = GetCurrentDir()
# The set of source files associated with this SConscript file.

src     = Glob('src/*.c')

# Examples
if GetDepend('ULAPACK_USE_STATIC_ALLOC'):

    if GetDepend('UKAL_USING_EKAL'):
        src    += Glob('examples/u_ekal_static.c')

elif GetDepend('ULAPACK_USE_DYNAMIC_ALLOC'):

    if GetDepend('UKAL_USING_EKAL'):
        src    += Glob('examples/u_ekal_dynamic.c')

path    = [cwd + '/']
path   += [cwd + '/src']

LOCAL_CCFLAGS = ''

group = DefineGroup('ulapack', src, depend = [''], CPPPATH = path, LOCAL_CCFLAGS = LOCAL_CCFLAGS)

Return('group')
