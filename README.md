# A3CNN
Reconhecimento de imagens com redes neurais convolucionais.

Como Testar o Projeto no Google Colab

Este projeto foi desenvolvido para rodar no ambiente do Google Colab. Para testar o modelo com a sua própria imagem de um número, siga os passos abaixo:

1. Fazer o Upload da Imagem
No menu lateral esquerdo do Google Colab, clique no ícone de Pasta (Arquivos).

Clique no ícone de Fazer upload para o armazenamento de sessão (ícone de uma folha com uma seta para cima).

Selecione a imagem do número que você deseja que o modelo classifique e copie o caminho (ex: image1.jpg).

2. Atualizar o Caminho no Código
Antes de executar a célula de teste, você precisa atualizar a chamada da função com o nome exato do arquivo que você enviou.

Procure pela última linha do código:
prever_numero('/content/image1.jpg')

Substitua o texto entre aspas pelo caminho da sua imagem. O caminho padrão será /content/ seguido do nome do seu arquivo (por exemplo: /content/foto_teste.png).
