# openmp-offloading-with-HIP

This is a simple demo project on how to build an executable with cmake that runs HIP kernels and OpenMP offloading kernels.
Since the ROCm compiler refuses to build (or link) code with OpenMP target regions when in HIP mode, both types of kernels
are built into separate (static) libraries and then linked in CXX mode.


## References

- https://rocm.docs.amd.com/projects/llvm-project/en/latest/conceptual/openmp.html (ROCm OpenMP support, including offloading)
- https://github.com/ROCm/ROCm/discussions/2137 (Discussion regarding incompatibility between OpenMP offloading and HIP)
- https://github.com/ROCm/aomp/tree/aomp-dev/test/hip-openmp/matrixmul_omp_target_multifile (Similar example project for the AOMP compiler)
