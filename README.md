# Blind Spot — BS-PJ-01

Plataforma de inteligência estratégica. Um arquivo único e autônomo.

## Subir

Suba a pasta inteira na raiz do repositório. Não precisa de build.

```
index.html
brand-bradesco.png
brand-bradesco-white.png
brand-oracle.png
brand-safra.svg
brand-safra-white.svg
vercel.json
```

## Rotas

- `/` — Blind Spot sem co-marca
- `/bradesco` — co-marca Bradesco
- `/oracle` — co-marca Oracle
- `/safra` — co-marca Safra

O `vercel.json` faz o reescrita das rotas para o `index.html`.

## Chave da API

A análise real é gerada ao vivo pelo cérebro do Blind Spot via API da Anthropic.
Na primeira vez, a tela pede a chave e ela fica guardada no navegador do usuário
(nada é enviado para servidor nosso). Sem chave, o sistema mostra os três exemplos
offline (Magazine Luiza, Natura e Localiza) já identificados como demonstração.

## O que roda ao vivo

- **Análise de empresa** — quatro chamadas em paralelo (A, B, C e cadeia), com busca
  na web. O relógio é o da chamada mais longa, não a soma.
- **Cruzamento** — árvore de implicações, aberta em duas fases.
- **Varredura** — sinais do mercado da empresa analisada, disparada em paralelo com
  a análise.
- **Futuros** — mapa de futuros possíveis e prováveis.
- **Decisões** e **Work in Progress** — derivados da análise.
- **Exportar Relatório** — relatório executivo em PDF, pela impressão do navegador.

## Observação

Os três exemplos offline foram escritos à mão para demonstração. A análise que
importa é a gerada pelo motor com a chave configurada — é ela que aplica o cérebro,
faz busca real na web e monta os achados sobre a empresa pedida.
