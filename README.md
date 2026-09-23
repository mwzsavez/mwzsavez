# mwz

Automação, integrações e IA aplicada a rotinas contábeis e fiscais.
**Menos trabalho manual. Mais controle da operação.**

Construo sistemas que leem os documentos que a equipe já produz (PDF, Excel, CSV, TXT, XML), conectam
sistemas que não conversam entre si e conferem cada etapa. O trabalho repetitivo sai das mãos das pessoas
sem que se perca o controle do que foi feito.

Portfólio: **[savez-portfolio.vercel.app](https://savez-portfolio.vercel.app)**

---

## Em destaque: Painel de Obrigações Acessórias

Plataforma web que controla as obrigações fiscais de um escritório contábil e **dá baixa sozinha** ao ler
os documentos da equipe. Um agente reconhece cada arquivo pelo conteúdo (declaração, recibo, apuração,
guia, XML de nota) e o painel o amarra à obrigação certa, cruzando o que foi **declarado**, o que foi
**apurado** e o que foi **recolhido**.

- **545 empresas**, **45 obrigações** e **~30 mil competências** controladas num lugar só
- **34 mil documentos** lidos e classificados sem digitação por **15 leitores** de documento fiscal
  (DCTFWeb, eSocial, Reinf, SPED, GIA, PGDAS-D, apurações, PER/DCOMP…)
- **606 mil XML** de notas indexados e o ISS retido conferido nota a nota
- Integração com a API do eContador (Alterdata), com a Receita e com a Sefaz RS
- Cadastro de empresa nova automatizado: a empresa aparece no sistema contábil, a ficha abre sozinha,
  robôs consultam inscrição estadual e Simples Nacional, e a gerente aprova com a prova na tela
- Atrasadas de um mês **de 527 para 261** ao decidir as guias sindicais pela folha de pagamento
- **~1.250 testes automatizados** e trilha de auditoria de cada mudança

`Next.js` `React` `TypeScript` `Prisma` `PostgreSQL` `Node.js` `SQLite` `Python` `Playwright` `Vercel`

---

## Outros projetos

Todos em uso na rotina de um escritório contábil. Os repositórios são privados porque trabalham com dados
de clientes.

| Projeto | O que resolve | Stack |
|---|---|---|
| **Central e-CAC** | Rotinas em lote nos portais a partir de uma lista única de empresas: DCTFWeb com importação do MIT, transmissão e download dos documentos; consultas ao Simples Nacional/SIMEI e à inscrição estadual no RS, com comprovante por empresa | JavaScript · automação de navegador |
| **Apurações sem movimento** | Cruza a relação de empresas com os documentos de conferência antes de gerar as apurações de ICMS, ISSQN e PIS/COFINS sem movimento. Empresa com pendência é bloqueada com o motivo; arquivo existente nunca é sobrescrito | Python |
| **Faturamento consolidado** | Lê apurações, balancetes e DRE de layouts suportados e organiza o faturamento por competência, consolidando matriz e filiais e apontando divergência entre apuração e contabilidade | Python |
| **SPED Fiscal** | Cálculo do DIFAL e dos ajustes E111/E113 | Python |
| **Ressarcimento de IPI** | Gera os arquivos R11 e R12 para importação no PER/DCOMP Web | Python |
| **Dissídio no Alterdata** | Recalcula o reajuste e gera o arquivo de importação do dissídio | Python |
| **Folha → contabilidade** | Integra os relatórios de folha do Alterdata ao arquivo de importação contábil do Infor | Python |

---

## Como eu trabalho

- **Começo pelo processo real**, não pelo desenho: volume, exceções e onde a rotina trava.
- **Regra determinística onde uma regra resolve; IA só onde gera valor verificável**, com conferência
  humana na decisão final.
- **Meço contra os arquivos de produção** antes de dizer que funciona: reconhecer o documento não prova
  que os valores foram lidos.
- **Documento de cliente não entra no repositório**, nem como exemplo de teste.
- **Tudo idempotente e rastreável**: rodar duas vezes não duplica, e cada mudança registra quem, quando
  e por quê.

---

## Tecnologias

**Linguagens** · TypeScript · JavaScript · Python · SQL · PowerShell<br>
**Web** · Next.js · React · Tailwind CSS · APIs REST<br>
**Dados** · PostgreSQL · Prisma · SQLite · Excel<br>
**Automação e documentos** · Node.js · Playwright · pdf.js · OCR · XML<br>
**Entrega** · Git · GitHub · Vercel · Docker · Agendador de Tarefas do Windows

---

Tem uma rotina que se repete e trava? **[Conte qual é](https://savez-portfolio.vercel.app/contato)**.
