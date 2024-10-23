project('chipmunk2d', 'c')

include = include_directories('include')
src = [
  'chipmunk.c',
  'cpArbiter.c',
  'cpArray.c',
  'cpBBTree.c',
  'cpBody.c',
  'cpCollision.c',
  'cpConstraint.c',
  'cpDampedRotarySpring.c',
  'cpDampedSpring.c',
  'cpGearJoint.c',
  'cpGrooveJoint.c',
  'cpHashSet.c',
  'cpHastySpace.c',
  'cpMarch.c',
  'cpPinJoint.c',
  'cpPivotJoint.c',
  'cpPolyline.c',
  'cpPolyShape.c',
  'cpRatchetJoint.c',
  'cpRobust.c',
  'cpRotaryLimitJoint.c',
  'cpShape.c',
  'cpSimpleMotor.c',
  'cpSlideJoint.c',
  'cpSpace.c',
  'cpSpaceComponent.c',
  'cpSpaceDebug.c',
  'cpSpaceHash.c',
  'cpSpaceQuery.c',
  'cpSpaceStep.c',
  'cpSpatialIndex.c',
  'cpSweep1D.c'
]

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)

sources = []
foreach s : src
  sources += 'src' / s
endforeach
  
chipmunk_lib = library('chipmunk2d',
  sources,
  include_directories: include,
  dependencies: m_dep
)

chipmunk2d_dep = declare_dependency(
  link_with: chipmunk_lib,
  include_directories : include
)
