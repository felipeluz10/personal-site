---
title: "Automatizando a Estruturação de Dados com Python e LLMs"
date: 2023-10-20
description: "Como reduzi o tempo de processamento de dados despadronizados usando OpenAI e Pydantic."
hero: images/hero.svg # Vamos falar dessa imagem no passo 3
menu:
  sidebar:
    name: "Sanitizador com AI"
    identifier: "sanitizador-ai"
    weight: 10
tags: ["Python", "AI Engineering", "OpenAI", "Automação"]
categories: ["Engenharia de Dados"]
---

## O Problema
No dia a dia da operação, recebíamos um grande volume de e-mails e textos completamente despadronizados. O desafio era extrair campos críticos: **Nome**, **Data** e **Número do Pedido** para inserir no nosso banco de dados legado.

As abordagens tradicionais falharam:
* **Regex:** Não dava conta dos infinitos erros de digitação humanos.
* **Manual:** Inviável pelo volume (gargalo operacional).

## A Solução
Desenvolvi um script em Python que atua como um **"Sanitizador Inteligente"**. Em vez de tentar prever todos os erros possíveis com código, deleguei a interpretação semântica para um modelo de linguagem (LLM), garantindo a estrutura final com validação programática.

### Arquitetura da Solução
> *Aqui entrará o diagrama visual do fluxo (Input -> Script -> OpenAI -> JSON)*

## A Stack Tecnológica
Para garantir robustez e baixo custo, utilizei:

* **Python (Requests):** Para orquestração e chamadas de API.
* **OpenAI API (gpt-3.5-turbo):** O "cérebro" que entende o texto sujo. Escolhido pelo custo-benefício vs gpt-4.
* **Pydantic:** A camada de segurança. Garante que o JSON de saída siga estritamente o schema do banco de dados, rejeitando alucinações da IA.

## O Resultado
O que antes levava **2 minutos por e-mail** para triagem humana, agora é processado em **1.5 segundos** com 99% de precisão.

---
### Show me the code
O código fonte deste projeto (com dados sensíveis removidos) está disponível no meu GitHub:
[Link para o Repositório em Breve]