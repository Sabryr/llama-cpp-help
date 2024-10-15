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

## Test


```
#llama_cpp.py

from llama_cpp import Llama
  
llm = Llama(
      model_path="/itf-fi-ml/shared/ml-models/NoraLLm/normistral-7b-warm-instruct.Q8_0.gguf",
      # n_gpu_layers=-1, # Uncomment to use GPU acceleration
      # seed=1337, # Uncomment to set a specific seed
      # n_ctx=2048, # Uncomment to increase the context window
)
output = llm(
      "Q: Name the planets in the solar system? A: ", # Prompt
      max_tokens=32, # Generate up to 32 tokens, set to None to generate up to the end of the context window
      stop=["Q:", "\n"], # Stop generating just before the model would generate a new question
      echo=True # Echo the prompt back in the output
) # Generate a completion, can also call create_completion
print(output)


```
