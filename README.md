# Sua empresa de IA

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Sua empresa de IA](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

Este Ã© um kit gratuito para o dono de pequena ou mÃ©dia empresa sair do uso solto do ChatGPT e colocar um agente de IA para trabalhar num processo de verdade. SÃ£o ferramentas que funcionam no navegador, sem cadastro: o Raio-X de Processos aponta por onde comeÃ§ar, a calculadora mostra quanto custa e quanto devolve, o checklist diz se o agente estÃ¡ seguro para ligar e o comparador da fÃ¡brica mostra se vale mais a ferramenta pronta, a API ou uma mÃ¡quina prÃ³pria, com um teste de modelos abertos em portuguÃªs. Quem faz consultoria tem o modelo para aplicar tudo isso num cliente. Depois, a trilha leva aos cursos e kits do ARCKHÉ para montar cada agente. VocÃª sÃ³ precisa do navegador; nada sai do seu computador.

## ðŸ“– Guia de uso

Guia completo com as ferramentas interativas: **https://linnoff88-dev.github.io/

## De onde vem

Em Berlim (GTC, 21/10/2026), Jensen Huang disse que toda empresa vai virar empresa de IA e que Ã© preciso produzir IA, nÃ£o sÃ³ consumir. Ele explicou com um bolo de cinco camadas: energia, computadores, fÃ¡brica de IA, modelos e aplicaÃ§Ãµes. Este kit traduz o bolo para a pequena empresa. VÃ­deo: https://www.youtube.com/watch?v=t-mBC3kuhLM

| Camada | Na sua empresa | PeÃ§a |
|---|---|---|
| AplicaÃ§Ãµes | os processos do negÃ³cio | Raio-X de Processos |
| Modelos | qual IA faz cada tarefa e quanto custa | Calculadora de custo |
| FÃ¡brica de IA | ferramenta pronta, API ou mÃ¡quina prÃ³pria | Comparador da fÃ¡brica + teste em portuguÃªs |
| Computadores | agente isolado, acesso mÃ­nimo | Checklist do agente seguro |
| Energia | pessoas, dados, contexto | trilha ARCKHÉ |

## O que tem no repositÃ³rio

```
guia/index.html                 # pÃ¡gina com as ferramentas (PT) + guia/en/ e guia/es/
kit/raio-x-processos.csv        # Raio-X em planilha (com fÃ³rmulas)
kit/calculadora-custo.csv       # calculadora de custo por tarefa em planilha
# os CSV usam ";" e vÃ­rgula decimal: abrem direto no Excel em portuguÃªs; no Google Planilhas, Arquivo > Importar > separador ponto e vÃ­rgula
kit/checklist-agente-seguro.md  # checklist de 10 itens em texto
kit/modelo-consultor.md         # modelo do consultor: 6 etapas, roteiro de 12 perguntas, proposta e relatÃ³rio
kit/benchmark-pt.csv            # resultado do teste de modelos abertos em portuguÃªs
bench/casos.json                # casos inventados das 4 tarefas (nota fiscal, contrato, classificar, atender)
bench/roda.py                   # roda o teste no Ollama local e dÃ¡ a nota por regra fixa
bench/injeta.py                 # pÃµe o resultado nos 3 guias
bench/resultados/               # respostas de cada modelo e resumo.json
```

## O processo, do inÃ­cio ao fim

1. ðŸ§  **Raio-X**: o dono lista as tarefas que se repetem e recebe a fila dos 3 primeiros processos (guia, passo 1).
2. ðŸ§  **Custo**: calcula custo hoje Ã— custo com agente e o custo por tarefa concluÃ­da (guia, passo 2).
3. ðŸ§  **SeguranÃ§a**: marca o checklist; abaixo de 6 itens nÃ£o liga (guia, passo 3).
4. ðŸ§  **Piloto de 30 dias** com o kit ARCKHÉ indicado, anotando toda semana tarefas, retornos para pessoa, custo da IA e reclamaÃ§Ãµes.
5. ðŸ§  **Medir**: refaz a calculadora com os nÃºmeros reais; deu certo, passa para o prÃ³ximo da fila.
6. ðŸ§  **FÃ¡brica**: o comparador mostra o custo por mÃªs da ferramenta pronta, da API e da mÃ¡quina prÃ³pria, e quantas tarefas a mÃ¡quina dÃ¡ conta (guia, seÃ§Ã£o FÃ¡brica).
7. ðŸ§  **Consultoria**: quem atende clientes segue as 6 etapas de `kit/modelo-consultor.md`; o botÃ£o "Montar o resumo para o cliente" gera a proposta com os nÃºmeros das ferramentas.

Tudo isso roda no navegador (âš™ï¸ JavaScript da pÃ¡gina); nÃ£o hÃ¡ servidor nem agente automÃ¡tico.

**Teste de modelos (mantenedor):**

1. âš™ï¸ `python3 bench/roda.py rodar --modelos <m1,m2>` roda os casos no Ollama local, um modelo por vez (descarrega o anterior), e grava `bench/resultados/<modelo>.jsonl`. Caso jÃ¡ feito Ã© pulado.
2. âš™ï¸ `python3 bench/roda.py resumo` dÃ¡ a nota e gera `bench/resultados/resumo.json` e `kit/benchmark-pt.csv`.
3. âš™ï¸ `python3 bench/injeta.py` pÃµe o resultado na tabela dos 3 guias.
4. ðŸ§  Revisar as liÃ§Ãµes da rodada no bloco `TF.licoes` dos guias e publicar (commit + push).

## Testar a sua tarefa

1. Abra `bench/casos.json` e copie um caso parecido com o seu (por exemplo, um de `atende`).
2. Troque o `id` por um nome novo e a `entrada` pela mensagem real do seu cliente (sem dado pessoal).
3. Em `requer`, ponha o que a resposta precisa conter (ex.: o preÃ§o certo); em `proibe`, o que ela nÃ£o pode dizer.
4. Para tarefas de ler documento, use as tarefas `nfe` ou `contrato` e preencha o `esperado` com os valores certos.
5. Rode `python3 bench/roda.py rodar --modelos llama3.2:latest --saida bench/minha-rodada` e abra `bench/minha-rodada/benchmark.csv`.

## Fontes dos nÃºmeros do guia

- Cetic.br, TIC Empresas 2025 (17% das empresas usam IA; 80% compram pronto, 26% fazem prÃ³pria).
- Serasa Experian, pesquisa com PMEs 2026 (41,3% citam falta de conhecimento; 31,2% custo).
- Gartner, previsÃ£o de jun/2025 (mais de 40% dos projetos de agentes cancelados atÃ© 2027).
- OWASP Top 10 for Agentic Applications 2026.
- Keynote de Jensen Huang, GTC Berlim 2026.

---
Parte do [ARCKHÉ AI](https://ARCKHÉ AI) â€” conteÃºdo aberto e gratuito.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>