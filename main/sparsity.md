* cuSPARSE
  * https://docs.nvidia.com/cuda/cusparse/index.html
  * https://developer.nvidia.com/cusparse
  * set of basic linear algebra subroutines for handling sparse matrices on NVIDIA GPUs
* cuSOLVER
  * https://docs.nvidia.com/cuda/cusolver/index.html
  * cuSolver library is a high-level package based on the cuBLAS and cuSPARSE libraries
  * CUDA sparse matix library
  * https://stackoverflow.com/questions/31840341/solving-general-sparse-linear-systems-in-cuda
    * Supports  solving general sparse linear systems in CUDA
* Tiramisu Compiler
  * http://tiramisu-compiler.org/
  * Polyhedral compiler for dense and sparse deep learning. Provides a simple C++ API for expressing algorithms and how these algorithms should be optimized by the compiler
  * Tiramisu uses the extended polyhedral model internally while TVM and Halide use intervals. This allows Tiramisu to naturally express many code patterns and transformations that are difficult to express in TVM and Halide. http://tiramisu-compiler.org/Comparison.html
  * White paper https://arxiv.org/pdf/2005.04091.pdf
* Sparse GPU Kernels for Deep Learning
  * https://arxiv.org/pdf/2006.10901.pdf
  * Seems much better than cuSPARSE. Fig 1
* Block-Sparse GPU Kernels
  * https://openai.com/blog/block-sparse-gpu-kernels/
  * https://github.com/openai/blocksparse
  * https://openai.com/blog/openai-pytorch/
  * can run orders of magnitude faster than cuBLAS or cuSPARSE
  * Supports TensorFlow and PyTorch
* CULA Sparse
  * http://www.culatools.com/cula_sparse_programmers_guide/
* Pytorch
  * https://github.com/traveller59/spconv
  * https://github.com/facebookresearch/SparseConvNet
  * https://towardsdatascience.com/sparse-matrices-in-pytorch-part-2-gpus-fd9cc0725b71  
* Presentations
  * Very good https://medium.com/huggingface/sparse-neural-networks-2-n-gpu-performance-b8bc9ce950fc
  * Sparse Matrix-Matrix Multiplication on the GPU. Nvidia GTC 2012 https://on-demand.gputechconf.com/gtc/2012/presentations/S0285-Optimization-of-Sparse-Matrix-Matrix-Multiplication-on-GPU.pdf
  * Sparse Matrices and Parallel Processing on GPUs http://www.netlib.org/utk/people/JackDongarra/WEB-PAGES/SPRING-2018/lect13-sparse.pdf
* Research Papers
  * Design Principles for Sparse Matrix Multiplication on the GPU https://people.eecs.berkeley.edu/~aydin/spmm_europar2018.pdf
* Examples
  * Blog post on running sparse algorithm on Nvidia Jetson https://hacarus.com/information/tech/sparse-modeling-with-the-jetson-nano-developer-kit/
    * Uses cuBLAS and cuSOLVER
* CUSP
  * https://developer.nvidia.com/cusp
  * https://cusplibrary.github.io/index.html
  * https://github.com/cusplibrary/cusplibrary
  * CUSP is an open source C++ library for sparse linear algebra based on Thrust
  * support for CUDA 7.0. Last release 2 years ago. Outdated/not maintained
* nsparse
  * https://github.com/EBD-CREST/nsparse
  * some 3d party it seems. support only CUDA: >=5.0 && < 9.0
