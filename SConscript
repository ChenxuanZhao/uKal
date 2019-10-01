    
from building import *
import rtconfig

# get current directory
cwd     = GetCurrentDir()
# The set of source files associated with this SConscript file.

src     = Glob('src/*.c')
defines = []

# Examples
if GetDepend('UKAL_USING_EKAL'):
    defines += ['UKAL_MAX_STATE_VECTOR_SIZE=5']
    defines += ['UKAL_MAX_MEASUREMENT_VECTOR_SIZE=5']
    src    += Glob('examples/u_ekal.c')

path    = [cwd + '/']
path   += [cwd + '/src']

LOCAL_CCFLAGS = ''

group = DefineGroup('ulapack', src, depend = [''], CPPPATH = path, LOCAL_CCFLAGS = LOCAL_CCFLAGS, CPPDEFINES= defines)

Return('group')
