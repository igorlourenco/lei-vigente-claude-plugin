---
name: legislacao-brasileira
description: Consulta o texto oficial vigente de leis federais brasileiras (Constituição, códigos, leis especiais) e de súmulas do STF e do STJ pelo servidor MCP Lei Vigente. Use sempre que for citar, explicar, resumir ou escrever sobre um artigo de lei, um dispositivo ou uma súmula do direito brasileiro, inclusive em pareceres, petições, contratos, e-mails a clientes, comentários de código ou regras de negócio baseadas em lei (prazos do CPC, CLT, CDC, LGPD, Código Civil, CTN etc.).
---

# Legislação brasileira com o Lei Vigente

O servidor MCP `lei-vigente` deste plugin traz o texto consolidado do Planalto e as súmulas do STF e do STJ.
Não cite de memória: a redação muda, artigos são revogados e números se confundem entre leis.

## Como consultar

1. Sabe o artigo: `consultar_artigo` (sigla + número) devolve o artigo inteiro, com parágrafos, incisos e alíneas.
   Para um único dispositivo, `consultar_dispositivo` com o `ref_key` (ex.: `CF.5.LXXVIII`, `CPC.1003.5`, `CC.12.unico`).
2. Não sabe o artigo: `buscar` com termos em português (aspas para frase exata), depois leia o resultado com
   `consultar_artigo` antes de afirmar qualquer coisa.
3. Súmula: `consultar_sumula` (tribunal, número e se é vinculante).
4. Não sabe a sigla do diploma: `listar_diplomas`. Diploma fora da lista não está na base: diga isso em vez de
   citar de memória.
5. Mudanças na lei: `alteracoes_recentes`; redações anteriores de um dispositivo: `versoes_dispositivo`.

## Ao escrever

- Reproduza o `texto` devolvido sem alterar e cite o `ref_key` e a `hierarquia`.
- Dispositivo com `revogado: true` nunca é apresentado como vigente.
- A fonte é o texto consolidado do Planalto, que pode atrasar alguns dias em relação ao Diário Oficial.
- Depois de redigir um texto com citações, confira-o com a skill `verificar-citacoes` (ferramenta `verificar_texto`).
- É informação jurídica, não aconselhamento; não preveja resultado de causa.
