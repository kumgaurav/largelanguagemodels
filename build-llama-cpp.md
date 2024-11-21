#Steps to build

1. Run the make command inside llama.cpp
2. pip install -r requirements.txt
3. examples/convert_legacy_llama.py --outfile /Users/gaurav/workspace/chatgpt/llama2/llama2model/7b/ggml-model-f16.bin /Users/gaurav/workspace/chatgpt/llama2/llama/llama-2-7b
4. examples/convert_legacy_llama.py --outfile /Users/gaurav/workspace/chatgpt/llama2/llama2model/13b/ggml-model-f16.bin /Users/gaurav/workspace/chatgpt/llama2/llama/llama-2-13b
5. ./llama-quantize  /Users/gaurav/workspace/chatgpt/llama2/llama2model/13b/ggml-model-f16.bin /Users/gaurav/workspace/chatgpt/llama2/llama2model/13b/ggml-model-q4_0.bin q4_0
6. ./llama-quantize  /Users/gaurav/workspace/chatgpt/llama2/llama2model/7b/ggml-model-f16.bin /Users/gaurav/workspace/chatgpt/llama2/llama2model/7b/ggml-model-q4_0.bin q4_0

7. CMAKE_ARGS="-DLLAMA_METAL=on" pip install -U llama-cpp-python --no-cache-dir


#Steps to test

1. ./llama-cli -m /Users/gaurav/workspace/chatgpt/llama2/llama2model/7b/ggml-model-q4_0.bin -p "I believe the meaning of life is" -n 128
2. 
