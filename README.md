### jetson_nano

python3.8 tensorflow-1.15.0


PYTHON_BIN_PATH=$(which python3.8) PYTHON_LIB_PATH=$(python3.8 -c 'import site; print(site.getsitepackages()[0])') TF_CUDA_COMPUTE_CAPABILITIES=5.3 TF_CUDA_VERSION=10.0 TF_CUDA_CLANG=0 TF_CUDNN_VERSION=7 TF_TENSORRT_VERSION=6 CUDA_TOOLKIT_PATH=/usr/local/cuda CUDNN_INSTALL_PATH=/usr/lib/aarch64-linux-gnu TENSORRT_INSTALL_PATH=/usr/lib/aarch64-linux-gnu TF_NEED_IGNITE=0 TF_ENABLE_XLA=0 TF_NEED_OPENCL_SYCL=0 TF_NEED_COMPUTECPP=0 TF_NEED_ROCM=0 TF_NEED_CUDA=1 TF_NEED_TENSORRT=1 TF_NEED_OPENCL=0 TF_NEED_MPI=0 GCC_HOST_COMPILER_PATH=$(which gcc) CC_OPT_FLAGS="-march=native" TF_SET_ANDROID_WORKSPACE=0     ./configure


bazel build --config=opt --config=cuda --config=nonccl --config=noaws   --local_resources=2048.0,1.0,1.0     //tensorflow/tools/pip_package:build_pip_package



##### tensorflow-1.15.0-cp38-cp38-linux_aarch64.whl
https://drive.google.com/file/d/1WWXQ7ZpQx3jBFqXRE8GRTvHKUrzZ6tvR/view?usp=sharing

