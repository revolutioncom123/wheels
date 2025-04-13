## Build Triton

1. Run the workflow 'Build Triton'. Set 'Git tag' (e.g. `v3.3.x-windows` as of now) and 'Triton wheel version suffix' (e.g. `.post18` for a regular release and `a0.post18` for a pre-release)
2. Download the artifacts
3. Do some sanity checks locally, e.g. diff with the last wheel, pip install the wheel, run it in ComfyUI
4. Upload the wheels to PyPI using [twine](https://packaging.python.org/en/latest/tutorials/packaging-projects/#uploading-the-distribution-archives)

The workflow 'Build and Test Triton' runs all unit tests. It requires a self-hosted runner with GPU. Due to the cost, we only turn on the VM when there is a significant release.

## Build SageAttention

1. Run the workflow 'Build SageAttention'. We support torch 2.5.1 + CUDA 12.4.1 and torch 2.6.0 + CUDA 12.6.3 as of now
2. Download the artifacts
3. Do some sanity checks locally
4. Upload the wheels to GitHub releases
