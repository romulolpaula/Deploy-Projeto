# Imersão Dev Back-End

## Objetivo
O objetivo da Imersão Dev Back-End, oferecida pela Alura, foi possibilitar o desenvolvimento de uma aplicação completa de upload de imagens, que não apenas armazena as imagens em um banco de dados, mas também gera descrições automaticamente utilizando a API do Google Gemini. Além disso, foi possível aprender a publicar a aplicação na Google Cloud, tornando-a acessível ao público.

## Tecnologias Utilizadas
- **Linguagens**: 
  - **JavaScript**: Utilizado no desenvolvimento do back-end com Node.js.
- **Banco de Dados**: 
  - **MongoDB**: Para armazenar informações sobre as imagens e seus respectivos IDs.
- **Framework**: 
  - **Express.js**: Para criar a API RESTful que gerencia as operações de upload e atualização de imagens.
- **Serviços**: 
  - **Google Cloud**: Utilizado para hospedar a aplicação através do serviço Cloud Run.
- **API**: 
  - **Google Gemini**: Para gerar descrições automáticas das imagens enviadas.

## O que foi Abordado
1. **Upload de Imagens**: 
   - Aprimoramento da lógica de upload, onde cada imagem é vinculada a um ID único no MongoDB. A pasta de uploads foi tornada publicamente acessível, permitindo que as imagens sejam acessadas via URL.

2. **Atualização de Posts**: 
   - Implementação de um método HTTP PUT e uma nova rota `/upload/:id` para atualizar registros existentes no banco de dados, ao invés de criar novos. A função `atualizarNovoPost` foi criada para lidar com as requisições de atualização.

3. **Integração com Google Gemini**: 
   - Criação de um serviço `geminiService.js` para interagir com a API do Gemini. A chave da API foi armazenada em uma variável de ambiente, e a função `gerarDescriçãoComGemini` foi implementada para gerar descrições a partir do buffer da imagem.

4. **Testes**: 
   - Utilização do Postman para testar o upload e a atualização de imagens, garantindo que as descrições geradas pelo Gemini fossem salvas corretamente no banco de dados.

5. **Integração com o Front-End**: 
   - Um projeto front-end pré-configurado (disponibilizada pela Alura), chamado "InstaByte", foi utilizado para consumir a API. O pacote `cors` foi instalado e configurado para permitir a comunicação entre o front-end e o back-end.

6. **Deploy na Google Cloud**: 
   - Preparação do projeto para o deploy, incluindo a instalação do pacote `dotenv` para gerenciar variáveis de ambiente. O deploy foi realizado utilizando o Cloud Run, permitindo que a API fosse acessível publicamente.

## Resultado Final

| Front-end consumindo a API e gerando legendas automaticamente | Deploy do projeto na Google Cloud |
|:--------------------------------------------------------------:|:----------------------------------:|
| <img src="https://drive.google.com/uc?id=1CT34AMlWvfFd99gTmZgmu68f56Q681Qo" alt="Resultado Final 1" width="600" /> | <img src="https://drive.google.com/uc?id=1G6lfLux75scoUHSK7qnwYl0sAZWulxju" alt="Resultado Final 2" width="600" /> |

## Acesse o projeto

Acesse o link do deploy abaixo para verificar o funcionamento do projeto:

[Link do Deploy](https://deploy-projeto-533233414234.southamerica-east1.run.app/posts)

