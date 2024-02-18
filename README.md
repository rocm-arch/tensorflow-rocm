#remove "set -e" from build_pip_package to avoid script erroring out when reruning makepkg
./tensorflow-2.15.0-opt-rocm/tensorflow-2.15.0/tensorflow/tools/pip_package/build_pip_package.sh

#fixes for PKGBUILD
Only create the required src folder
Only opt by default
Native march
Patch source code and scripts

#Code patch, add missing hip function in xla
tensorflow-2.15.0/third_party/xla/xla/stream_executor/rocm/rocm_driver.cc
tensorflow-2.15.0/third_party/xla/xla/stream_executor/rocm/rocm_driver_wrapper.h
