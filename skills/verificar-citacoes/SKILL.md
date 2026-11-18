---
name: verificar-citacoes
description: Confere, no texto oficial vigente, todas as citações de lei e de súmula de um texto jurídico (parecer, petição, contrato, e-mail, minuta) com o servidor MCP Lei Vigente e aponta as revogadas, inexistentes, ambíguas ou fora da base. Use quando o usuário pedir para conferir, revisar ou validar citações legais de um arquivo ou trecho, ou antes de entregar um texto jurídico que você redigiu.
argument-hint: "[arquivo ou trecho]"
---

# Verificar citações

Alvo: $ARGUMENTS

1. Obtenha o texto: se o alvo for um caminho, leia o arquivo; se for um trecho, use-o; se estiver vazio, use o
   texto jurídico mais recente da conversa ou pergunte qual arquivo conferir. Textos longos podem ser enviados em
   partes (por seção).
2. Envie o texto, sem alterar, à ferramenta `verificar_texto` do servidor `lei-vigente`.
   Se ela responder que exige autenticação, explique que a verificação precisa da conta Lei Vigente: rode `/mcp`,
   escolha `plugin:lei-vigente:lei-vigente` e faça login no navegador (a conta é criada em
   https://api.leivigente.com.br/conta). Enquanto isso, as ferramentas de leitura (`consultar_artigo`, `buscar`)
   funcionam sem conta.
3. Relate o `resumo` (contagem por status) e, para cada citação que não for `verificado`, uma linha com: trecho
   citado, status, o que está errado e a redação oficial ou o dispositivo correto (`ref_key`).
   - `verificado`: confirmada. Não precisa listar uma a uma; basta o total.
   - `verificado_parcial`: o artigo existe, mas o parágrafo/inciso/alínea citado não. Trate como erro.
   - `revogado` / `cancelada`: não pode ser citada como vigente.
   - `nao_encontrado`: o dispositivo não existe; mostre as `sugestao` se houver.
   - `verificado_inferido` / `ambiguo`: o diploma não estava explícito; peça conferência humana.
   - `diploma_desconhecido` / `nao_suportado`: fora da base, não necessariamente errada.
4. Só altere o arquivo se o usuário pedir. Ao corrigir, use a redação oficial devolvida e confira de novo.
