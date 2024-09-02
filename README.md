# Atividade-import-os-platform

import os
import platform

def verificar_arquivo():
    # Solicita o nome do arquivo ao usuário
    nome_arquivo = input("Digite o nome do arquivo (com extensão): ")

    # Verifica se o arquivo existe
    if not os.path.isfile(nome_arquivo):
        print(f"O arquivo '{nome_arquivo}' não existe.")
        return

    # Verifica se o arquivo não está vazio
    if os.path.getsize(nome_arquivo) == 0:
        print(f"O arquivo '{nome_arquivo}' está vazio.")
        return

    # Mostra o conteúdo do arquivo e conta as linhas
    with open(nome_arquivo, 'r', encoding='utf-8') as arquivo:
        linhas = arquivo.readlines()
        print(f"\nConteúdo do arquivo '{nome_arquivo}':\n")
        for linha in linhas:
            print(linha.strip()) # Mostra o conteúdo do arquivo linha por linha

        # Conta a quantidade de linhas do arquivo
        print(f"\nO arquivo '{nome_arquivo}' contém {len(linhas)} linhas.")

# usando a função verificar_arquivo()
verificar_arquivo()
