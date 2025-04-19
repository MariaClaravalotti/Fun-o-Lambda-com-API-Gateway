 # Lab: Criar uma função Lambda com API Gateway (Free Tier)
🎯 Objetivo
Criar uma função Lambda que retorna uma mensagem personalizada quando acessada por um link público via API Gateway.

## 🧰 Recursos usados (Free Tier)
AWS Lambda (1 milhão de invocações/mês grátis)

Amazon API Gateway (1 milhão de chamadas/mês grátis)

## 🚀 Passo a passo
1. Criar a função Lambda
Acesse o Console AWS > procure por Lambda

Clique em "Create function"

Name: minhaFuncaoHello

Runtime: Python 3.12 (ou Node.js, se preferir)

Permissions: Use a permissão padrão criada automaticamente

Clique em Create function

## 2. Código da função
Substitua o código da aba "Code source" por:

Python (exemplo):

python
Copiar
Editar
def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'headers': { 'Content-Type': 'application/json' },
        'body': '🚀 Olá, Clara! Sua função Lambda está funcionando!'
    }
Clique em Deploy para salvar.

## 3. Criar um endpoint com o API Gateway
Na tela da função Lambda, clique em "Adicionar gatilho"

Selecione API Gateway

Tipo: HTTP API

Segurança: Open (sem autenticação, público)

Clique em "Add"

A AWS vai criar e conectar a API automaticamente.

## 4. Testar sua API pública
Após a criação, você verá um link como este:


https://abc123xyz.execute-api.us-east-1.amazonaws.com/default/minhaFuncaoHello
Acesse esse link no navegador — vai ver sua mensagem retornada pela função Lambda! 🎉

![print1](https://github.com/user-attachments/assets/e3b57099-2151-400c-bb59-a2a6b536a63e)

![print2](https://github.com/user-attachments/assets/3a65e089-a53b-4f8f-937c-512b497cc442)


