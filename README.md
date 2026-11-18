# Lei Vigente para Claude Code

Plugin do [Lei Vigente](https://leivigente.com.br) para o Claude Code: o Claude consulta o texto oficial vigente
das leis federais brasileiras e das súmulas do STF e do STJ e confere as citações de pareceres, petições e
contratos antes de você enviar.

## Instalar

```bash
claude plugin marketplace add igorlourenco/lei-vigente-claude-plugin
claude plugin install lei-vigente@lei-vigente
```

Ou, dentro do Claude Code: `/plugin install lei-vigente --marketplace igorlourenco/lei-vigente-claude-plugin`.

## Conectar a conta

A leitura dos textos funciona sem conta. A verificação de citações exige a conta Lei Vigente:
dentro do Claude Code, rode `/mcp`, escolha `plugin:lei-vigente:lei-vigente` e entre pelo navegador
(crie a conta em [api.leivigente.com.br/conta](https://api.leivigente.com.br/conta)).

## O que vem no plugin

- Servidor MCP `https://api.leivigente.com.br/mcp` (ferramentas `consultar_artigo`, `consultar_dispositivo`,
  `consultar_sumula`, `buscar`, `verificar_texto` e outras; ver a [documentação](https://leivigente.com.br/docs/mcp)).
- Skill `legislacao-brasileira`: o Claude lê o texto oficial antes de citar um artigo ou uma súmula.
- Skill `/lei-vigente:verificar-citacoes [arquivo]`: confere todas as citações de um arquivo ou trecho.

## Exemplos

- "O que diz o art. 5º, inciso LXXVIII, da Constituição?"
- "Qual artigo do CPC trata do prazo para recorrer?"
- `/lei-vigente:verificar-citacoes pareceres/2026-10-cliente.md`

Cobre legislação federal e súmulas do STF e do STJ que estão na base. É informação jurídica, não aconselhamento.

[Privacidade](https://leivigente.com.br/docs/privacidade) ·
[Termos de uso](https://leivigente.com.br/docs/termos-de-uso) ·
[Suporte](https://leivigente.com.br/docs/suporte)
