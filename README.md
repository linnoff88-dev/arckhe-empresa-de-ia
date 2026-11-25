# Sua empresa de IA

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Sua empresa de IA](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

Este êÂ© um kit gratuito para o dono de pequena ou mêÂ©dia empresa sair do uso solto do ChatGPT e colocar um agente de IA para trabalhar num processo de verdade. SêÂ£o ferramentas que funcionam no navegador, sem cadastro: o Raio-X de Processos aponta por onde comeêÂ§ar, a calculadora mostra quanto custa e quanto devolve, o checklist diz se o agente estêÂ¡ seguro para ligar e o comparador da fêÂ¡brica mostra se vale mais a ferramenta pronta, a API ou uma mêÂ¡quina prêÂ³pria, com um teste de modelos abertos em portuguêÂªs. Quem faz consultoria tem o modelo para aplicar tudo isso num cliente. Depois, a trilha leva aos cursos e kits do ARCKHê para montar cada agente. VocêÂª sêÂ³ precisa do navegador; nada sai do seu computador.

## ê°Å¸ââ Guia de uso

Guia completo com as ferramentas interativas: **https://linnoff88-dev.github.io/

## De onde vem

Em Berlim (GTC, 21/10/2026), Jensen Huang disse que toda empresa vai virar empresa de IA e que êÂ© preciso produzir IA, nêÂ£o sêÂ³ consumir. Ele explicou com um bolo de cinco camadas: energia, computadores, fêÂ¡brica de IA, modelos e aplicaêÂ§êÂµes. Este kit traduz o bolo para a pequena empresa. VêÂ­deo: https://www.youtube.com/watch?v=t-mBC3kuhLM

| Camada | Na sua empresa | PeêÂ§a |
|---|---|---|
| AplicaêÂ§êÂµes | os processos do negêÂ³cio | Raio-X de Processos |
| Modelos | qual IA faz cada tarefa e quanto custa | Calculadora de custo |
| FêÂ¡brica de IA | ferramenta pronta, API ou mêÂ¡quina prêÂ³pria | Comparador da fêÂ¡brica + teste em portuguêÂªs |
| Computadores | agente isolado, acesso mêÂ­nimo | Checklist do agente seguro |
| Energia | pessoas, dados, contexto | trilha ARCKHê |

## O que tem no repositêÂ³rio

```
guia/index.html                 # pêÂ¡gina com as ferramentas (PT) + guia/en/ e guia/es/
kit/raio-x-processos.csv        # Raio-X em planilha (com fêÂ³rmulas)
kit/calculadora-custo.csv       # calculadora de custo por tarefa em planilha
# os CSV usam ";" e vêÂ­rgula decimal: abrem direto no Excel em portuguêÂªs; no Google Planilhas, Arquivo > Importar > separador ponto e vêÂ­rgula
kit/checklist-agente-seguro.md  # checklist de 10 itens em texto
kit/modelo-consultor.md         # modelo do consultor: 6 etapas, roteiro de 12 perguntas, proposta e relatêÂ³rio
kit/benchmark-pt.csv            # resultado do teste de modelos abertos em portuguêÂªs
bench/casos.json                # casos inventados das 4 tarefas (nota fiscal, contrato, classificar, atender)
bench/roda.py                   # roda o teste no Ollama local e dêÂ¡ a nota por regra fixa
bench/injeta.py                 # pêÂµe o resultado nos 3 guias
bench/resultados/               # respostas de cada modelo e resumo.json
```

## O processo, do inêÂ­cio ao fim

1. ê°Å¸Â§Â  **Raio-X**: o dono lista as tarefas que se repetem e recebe a fila dos 3 primeiros processos (guia, passo 1).
2. ê°Å¸Â§Â  **Custo**: calcula custo hoje êâ custo com agente e o custo por tarefa concluêÂ­da (guia, passo 2).
3. ê°Å¸Â§Â  **SeguranêÂ§a**: marca o checklist; abaixo de 6 itens nêÂ£o liga (guia, passo 3).
4. ê°Å¸Â§Â  **Piloto de 30 dias** com o kit ARCKHê indicado, anotando toda semana tarefas, retornos para pessoa, custo da IA e reclamaêÂ§êÂµes.
5. ê°Å¸Â§Â  **Medir**: refaz a calculadora com os nêÂºmeros reais; deu certo, passa para o prêÂ³ximo da fila.
6. ê°Å¸Â§Â  **FêÂ¡brica**: o comparador mostra o custo por mêÂªs da ferramenta pronta, da API e da mêÂ¡quina prêÂ³pria, e quantas tarefas a mêÂ¡quina dêÂ¡ conta (guia, seêÂ§êÂ£o FêÂ¡brica).
7. ê°Å¸Â§Â  **Consultoria**: quem atende clientes segue as 6 etapas de `kit/modelo-consultor.md`; o botêÂ£o "Montar o resumo para o cliente" gera a proposta com os nêÂºmeros das ferramentas.

Tudo isso roda no navegador (ê¢Å¡â¢ê¯Â¸Â JavaScript da pêÂ¡gina); nêÂ£o hêÂ¡ servidor nem agente automêÂ¡tico.

**Teste de modelos (mantenedor):**

1. ê¢Å¡â¢ê¯Â¸Â `python3 bench/roda.py rodar --modelos <m1,m2>` roda os casos no Ollama local, um modelo por vez (descarrega o anterior), e grava `bench/resultados/<modelo>.jsonl`. Caso jêÂ¡ feito êÂ© pulado.
2. ê¢Å¡â¢ê¯Â¸Â `python3 bench/roda.py resumo` dêÂ¡ a nota e gera `bench/resultados/resumo.json` e `kit/benchmark-pt.csv`.
3. ê¢Å¡â¢ê¯Â¸Â `python3 bench/injeta.py` pêÂµe o resultado na tabela dos 3 guias.
4. ê°Å¸Â§Â  Revisar as liêÂ§êÂµes da rodada no bloco `TF.licoes` dos guias e publicar (commit + push).

## Testar a sua tarefa

1. Abra `bench/casos.json` e copie um caso parecido com o seu (por exemplo, um de `atende`).
2. Troque o `id` por um nome novo e a `entrada` pela mensagem real do seu cliente (sem dado pessoal).
3. Em `requer`, ponha o que a resposta precisa conter (ex.: o preêÂ§o certo); em `proibe`, o que ela nêÂ£o pode dizer.
4. Para tarefas de ler documento, use as tarefas `nfe` ou `contrato` e preencha o `esperado` com os valores certos.
5. Rode `python3 bench/roda.py rodar --modelos llama3.2:latest --saida bench/minha-rodada` e abra `bench/minha-rodada/benchmark.csv`.

## Fontes dos nêÂºmeros do guia

- Cetic.br, TIC Empresas 2025 (17% das empresas usam IA; 80% compram pronto, 26% fazem prêÂ³pria).
- Serasa Experian, pesquisa com PMEs 2026 (41,3% citam falta de conhecimento; 31,2% custo).
- Gartner, previsêÂ£o de jun/2025 (mais de 40% dos projetos de agentes cancelados atêÂ© 2027).
- OWASP Top 10 for Agentic Applications 2026.
- Keynote de Jensen Huang, GTC Berlim 2026.

---
Parte do [ARCKHê AI](https://ARCKHê AI) ê¢â¬â conteêÂºdo aberto e gratuito.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>