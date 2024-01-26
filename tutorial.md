# Tutorial LLM com FastChat
Este tutorial tem como objetivo 
- Instalação do FastChat
- Instalação de uma LLM
- Execução em CLI, e por server


## Instalação do FastChat
Utilizar Python 3.9

Executar seguintes comandos:
```bash
git clone https://github.com/lm-sys/FastChat.git
```
```bash
cd FastChat
```
```bash
py -3.9 -m pip install .
py -3.9 -m pip install fastchat
py -3.9 -m  pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```
Necessário instalar também CUDA 12.1 https://developer.nvidia.com/cuda-12-1-0-download-archive?target_os=Windows&target_arch=x86_64&target_version=11&target_type=exe_local

## Instalação do LLM
git clone https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0
-- O hugging face possui diversos outros projetos de LLM para text generation, no entanto esse foi o menor encontrado que pode ser executado em qualquer máquina.

## Execução em CLI
```bash
py -3.9 -m fastchat.serve.cli --model-path ./models/TinyLlama-1.1B-Chat-v1.0
```
Após a execução é possível conversar com o modelo

## Execução com Server
Executar cada arquivo em um command prompt.
```bash
py -3.9 -m fastchat.serve.controller --host 0.0.0.0
py -3.9 -m fastchat.serve.model_worker --model-path ./models/TinyLlama-1.1B-Chat-v1.0 --host 0.0.0.0
py -3.9 -m fastchat.serve.openai_api_server --host 0.0.0.0
```

### Extras
Também é possível executar em integração com o Autogen para múltiplos agentes e realizar uma conversação entre os agentes, no entanto na máquina atual não foi possível realizar esse teste
Nome do dispositivo	DESKTOP-M7RS535
Processador	Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz   1.80 GHz
RAM instalada	16,0 GB (utilizável: 15,9 GB)
ID do dispositivo	6B7D94D5-DFD2-477C-9513-11E6EBC8385B
ID do Produto	00327-30737-89850-AAOEM
Tipo de sistema	Sistema operacional de 64 bits, processador baseado em x64
Caneta e toque	Nenhuma entrada à caneta ou por toque disponível para este vídeo



