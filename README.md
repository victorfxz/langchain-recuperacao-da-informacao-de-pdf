# Visão Geral

Este repositório contem um aplicativo web completo que implementa o recurso "Bate-papo com PDF". Integrando a api do ChatGPT a um aplicativos no estilo de produção com o LangChain. Ele se utiliza de componentes do LangChain para construir pipelines de geração de texto complexos, aprimorando a saída do ChatGP.





![](D:\Git\estudos-e-projetos-de-ciencia-de-dados\aprendizado-de-maquina\app-preco-imovel-previsao\img\app.gif)

## Configurações iniciais

### Criar ambiente virtual.
```
python -m venv .venv
```
### No MacOS, WSL, Linux.
```
source .venv/bin/activate
```
### No Windows
```
.\.venv\Scripts\activate
```
### Instalar dependências.
```
pip install -r requirements.txt
```
### Inicializar o banco de dados - sqlite.db.
```
flask --app app.web init-db
```

## Executando o App

São necessários três processos distintos para garantir o funcionamento do aplicativo: o server, o worker e o Redis.

Caso algum desses processos seja interrompido, será necessário reiniciá-los. Abaixo, estão listados os comandos para iniciar cada um deles. Se houver a necessidade de interrompê-los, selecione a janela do terminal em que o processo está em execução e pressione Control-C.

## Para executar o servidor Python

```
inv dev
```

### Para executar o worker
```
inv devworker
```

### Para executar o Redis
```
redis-server
```

### Reset o banco de dados
```
flask --app app.web init-db
```
