Primeiro, ative seu ambiente de desenvolvimento:

source env/bin/activate

No diretório desejado, instale o Flask:

pip install flask

Após isso, crie o arquivo do projeto:

touch app.py

Então, com o editor de texto desejado, cole este trecho de código:

from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
   return "<body style='background-color: #0d7963; font-family: Arial; color: white'>" \
          "<div style='display: flex; flex-direction: column; place-items: center'>" \
          "<h1 style='text-align: center;'>Parabéns, está funcionando!</h1>" \
          "<h2 style='text-align: center;'>Este é seu primeiro projeto com flask.</h2>" \
          "<img width='50%' src='https://cms-assets.tutsplus.com/uploads/users/30/posts/16037/preview_image/flask.png'>" \
          "</body" \


Após esta etapa, defina a variável do ambiente com o nome do seu arquivo:

export FLASK_APP=app

Por fim, execute o seu projeto:

flask run


