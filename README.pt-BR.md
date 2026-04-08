# AI Dev Toolkit

Toolkit reutilizavel para desenvolvimento assistido por IA: patterns, regras, skills portateis, configuracao multi-ferramenta e implementacoes de referencia para fazer agentes de codigo trabalharem com mais contexto, mais consistencia e menos supervisao manual.

## Comece Por Aqui

Se voce quer entender o repositório em um unico arquivo, leia primeiro:

- [Resumo do AI Dev Toolkit](./docs/AI_ASSISTED_DEVELOPMENT_SUMMARY.pt-BR.md)

Se voce quer usar o toolkit no seu projeto o mais rapido possivel:

1. copie um arquivo de `rules/` para a raiz do seu projeto
2. leia `patterns/context-building.md`
3. leia `patterns/task-orchestration.md`
4. adicione `patterns/code-review.md` e `patterns/testing.md`
5. instale `forge-kit` apenas quando precisar sincronizar tudo entre varias ferramentas

## O Que O Repo Entrega

- `rules/`: instrucoes prontas para Claude Code, Codex, GitHub Copilot, Gemini, Cursor, Windsurf e Antigravity
- `patterns/`: playbooks tool-agnostic para contexto, memoria, testes, revisao, routing, permissoes e orquestracao
- `best-practices/`: versao curta e operacional dos principios mais importantes
- `kit/`: `forge-kit`, o instalador/configurador do toolkit
- `kit/core/skills/`: 29 skills portateis
- `implementations/`: guias especificos por ferramenta, incluindo GitHub Copilot, Gemini e Antigravity
- `companies/`: organizacoes prontas de agentes especialistas
- `tools/`: stack recomendada de CLIs, plugins e utilitarios
- `training/`: captura e fine-tuning opcional

## Sobre o `ai-dev-toolkit-setup`

O repositório companheiro `ai-dev-toolkit-setup` existe para preparar uma maquina nova com shell, tmux, bootstrap de OpenCode, autenticacao guiada, helpers de release e ambiente base para agentes.

Use:

- `ai-dev-toolkit` para guidance reutilizavel dentro de projetos
- `ai-dev-toolkit-setup` para bootstrap da maquina

O setup consome uma release pinada do toolkit e instala os helpers canonicos quando esta online.

## Quando Este Repo Faz Mais Sentido

Use este repositório quando voce quer:

- reduzir improviso no uso de IA para desenvolvimento
- dar contexto consistente para agentes
- criar workflows repetiveis de planejamento, execucao, review e verificacao
- usar varias ferramentas de IA sem reescrever guidance toda hora
- melhorar seguranca, qualidade e continuidade entre sessoes

## Proximo Passo

Se quiser a versao em ingles, use o [README original](./README.md).
