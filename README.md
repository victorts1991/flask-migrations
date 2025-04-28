# flask-migrations

Após executar o git clone execute os comandos abaixo na raiz do projeto:

```
python3 -m venv venv

source venv/bin/activate  # Unix/macOS
# ou
venv\Scripts\activate  # Windows

pip install -r requirements.txt

python3 app.py
```

Documentação em Swagger:

```
http://127.0.0.1:5000/apidocs
```

Obs: Após instalar uma dependência nova, para atualizar o arquivo requirements.txt execute o comando abaixo:

```
pip freeze > requirements.txt
```

Ao alterar as classes do arquivo models.py, execute os comandos abaixo para que sejam criadas as migrations e alterações no seu banco de dados:

```
alembic revision --autogenerate  -m "Adicionar a coluna data_de_nascimento na tabela usuarios" 
alembic upgrade head
```