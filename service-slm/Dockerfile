FROM arm64v8/ubuntu:22.04

RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    wget \
    cmake \
    libopenblas-dev \
    libcurl4-openssl-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

RUN git clone https://github.com/ggerganov/llama.cpp.git

WORKDIR /app/llama.cpp

RUN cmake -B build && \
    cmake --build build --config Release -j$(nproc)

WORKDIR /app/llama.cpp/build/bin

CMD ["./llama-cli", "-m", "tinyllama-1.1b-chat-v1.0.Q4_K_M.gguf", "-p", "Qual capital do Brasil", "-n", "128", "--temp", "0.7"]