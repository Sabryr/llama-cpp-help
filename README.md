# How to on ml9

  - Load the modules
    -  `module load Python/3.11.3-GCCcore-12.3.0 `
    -  `module load Python CMake/3.26.3-GCCcore-12.3.0 protobuf/24.0-GCCcore-12.3.0 CUDA/12.3.0`
    -  `module load Python protobuf/24.0-GCCcore-12.3.0 CUDA/12.3.0`
    -  `module load Python CUDA/12.3.0`
       - Load all at once
         -  `module load Python/3.11.3-GCCcore-12.3.0 CMake/3.26.3-GCCcore-12.3.0 protobuf/24.0-GCCcore-12.3.0 CUDA/12.3.0`
  - Creat a virtual environment and activate it  
    - `python -m venv llama-cpp`
    - `source llama-cpp/bin/activate`

  - Install the requirments with GPU support
    - ` CMAKE_ARGS="-DGGML_CUDA=on" pip install -r requirements.txt`

  - Test libraries  

## install dependancies

## Use env
```
- source llm/bin/activate
- export HF_HOME=/itf-fi-ml/shared/ml-models/NoraLLm/  # set modeul location to prevent downloading to HOME
```
