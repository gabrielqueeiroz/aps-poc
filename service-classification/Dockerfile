FROM python:3.11-slim

WORKDIR /app

# Copia o arquivo de requisitos e instala as dependências
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante dos arquivos do seu projeto para o container
COPY . .

# Comando para rodar a aplicação quando o container iniciar
# Adapte esta linha para rodar seu script principal
CMD ["python", "seu_script_principal.py"]