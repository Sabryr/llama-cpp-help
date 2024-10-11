# How to on ml9

## install dependancies
```
- module load Python/3.11.3-GCCcore-12.3.0 CMake/3.26.3-GCCcore-12.3.0 protobuf/24.0-GCCcore-12.3.0 CUDA/12.3.0
- python -m venv llm
- source llm/bin/activate
- CMAKE_ARGS="-DGGML_CUDA=on" pip install -r requirements.txt
```

## Use env
```
- source llm/bin/activate
- export HF_HOME=/itf-fi-ml/shared/ml-models/NoraLLm/  # set modeul location to prevent downloading to HOME
```
