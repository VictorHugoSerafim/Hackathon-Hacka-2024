# Usando imagem oficial do Python
FROM python:3.11-slim

# Definindo diretório de trabalho
WORKDIR /app

# Copiando o arquivo de dependências do Python
COPY requirements.txt .

# Instalando dependências
RUN pip install --no-cache-dir -r requirements.txt

# Copiando o código da aplicação
COPY . .

# Expondo a porta padrão do Django
EXPOSE 8000

# Comando para rodar o servidor Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]