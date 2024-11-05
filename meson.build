project('chipmunk', 'c', version: '7.0.3', license: 'MIT')

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required: false)

if get_option('doubles')
  add_project_arguments('-DCP_USE_DOUBLES=1', language: 'c')
else
  add_project_arguments('-DCP_USE_DOUBLES=0', language: 'c')
endif

inc = include_directories('include')
lib = library(
  'chipmunk',
  'src/chipmunk.c',
  'src/cpArbiter.c',
  'src/cpArray.c',
  'src/cpBBTree.c',
  'src/cpBody.c',
  'src/cpCollision.c',
  'src/cpConstraint.c',
  'src/cpDampedRotarySpring.c',
  'src/cpDampedSpring.c',
  'src/cpGearJoint.c',
  'src/cpGrooveJoint.c',
  'src/cpHashSet.c',
  'src/cpHastySpace.c',
  'src/cpMarch.c',
  'src/cpPinJoint.c',
  'src/cpPivotJoint.c',
  'src/cpPolyline.c',
  'src/cpPolyShape.c',
  'src/cpRatchetJoint.c',
  'src/cpRobust.c',
  'src/cpRotaryLimitJoint.c',
  'src/cpShape.c',
  'src/cpSimpleMotor.c',
  'src/cpSlideJoint.c',
  'src/cpSpace.c',
  'src/cpSpaceComponent.c',
  'src/cpSpaceHash.c',
  'src/cpSpaceQuery.c',
  'src/cpSpaceStep.c',
  'src/cpSpatialIndex.c',
  'src/cpSweep1D.c',
  include_directories: inc,
  dependencies: m_dep,
)

chipmunk_dep = declare_dependency(include_directories: inc, link_with: lib)
