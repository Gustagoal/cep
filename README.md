# cep
Script que coleta os dados de uma API atraves do CEP fornecido pelo usuario

import requests
cep = input("Digite um cep : ")
try:
    requisicao = requests.get(f"https://cep.awesomeapi.com.br/json/{cep}")
    dados = requisicao.json()
except Exception as e:
    print("Erro ao tentar digitar o cep")
    print(f"Erro do tipo {e}")
print(dados)
