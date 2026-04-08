# Resumo do AI Dev Toolkit

Este repositório e um toolkit para desenvolvimento assistido por IA. Ele nao e um app e nao e um framework para ser importado no codigo de producao. O objetivo dele e ajudar agentes de programacao a trabalhar com mais contexto, defaults mais seguros, fluxos mais claros e resultados mais repetiveis.

## O Jeito Mais Rapido de Tirar Valor

Se voce esta chegando agora, comece com um arquivo de regras:

- `rules/CLAUDE.md` para Claude Code e ferramentas compativeis
- `rules/AGENTS.md` para Codex CLI
- `rules/COPILOT.md` para GitHub Copilot
- os arquivos especificos para Cursor e Windsurf

Copie o arquivo certo para a raiz do seu projeto. Isso ja entrega para o agente uma base de identidade, padroes de codigo, workflow, testes, seguranca e entrega antes do primeiro prompt.

Voce nao precisa instalar tudo para se beneficiar do repositório.

## O Que Existe Aqui Dentro

### 1. Regras

O diretorio `rules/` contem arquivos prontos para diferentes ferramentas de IA.

Use essas regras quando voce quiser que o agente respeite automaticamente:

- seus padroes de codigo
- workflow trunk-based
- gates de teste e verificacao
- regras de documentacao
- limites de seguranca
- expectativa de execucao duravel

Pense em regras como a camada de comportamento sempre carregada.

### 2. Patterns

O diretorio `patterns/` contem playbooks de workflow. Eles explicam como usar IA direito, nao apenas o que mandar para o modelo.

O conjunto cobre:

- construcao de contexto
- orquestracao de tarefas
- code review
- testes
- memoria
- roteamento de modelos
- gestao de sessao
- git worktrees
- limites de permissao
- observabilidade
- desenvolvimento guiado por especificacao
- trabalho em multiplos repositorios
- streaming orchestration
- prompt engineering
- design de tool registry
- falhas comuns de agentes

Pense em `patterns` como o manual conceitual do desenvolvimento assistido por IA.

### 3. Best Practices

O diretorio `best-practices/` e uma camada mais curta e operacional em cima dos `patterns`.

Ele reforca:

- desenvolvimento assistido por IA com seguranca
- higiene de contexto e controle de tokens
- branching, commits e fluxo de entrega

Pense em `best-practices` como a versao checklist do manual.

### 4. forge-kit

O diretorio `kit/` contem o `forge-kit`, que e o sistema de instalacao e configuracao do toolkit.

Ele inclui:

- `kit/install.sh` para instalar os assets do toolkit em ferramentas suportadas
- `kit/setup.sh` para setup interativo
- `kit/adapters/` com a logica de instalacao por ferramenta
- `kit/profiles/` com modos como standard, minimal, research e durable
- `kit/core/` com regras compartilhadas, registries de configuracao e skills portateis

O `forge-kit` existe para que a mesma orientacao de desenvolvimento com IA possa ser instalada em varias ferramentas sem reescrever tudo na mao.

### 5. Skills Portateis

O diretorio `kit/core/skills/` atualmente contem 29 skills portateis.

A forma mais simples de entender e por grupos:

- Planejamento e execucao: `plan`, `plan-change`, `orchestrate`, `loop`, `ship`, `verify`, `ship-check`
- Debug e qualidade: `debug`, `root-cause-debug`, `review`, `secure`, `tdd`, `release-flow`
- Sessao e contexto: `resume`, `memory`, `context`, `context-hygiene`, `worktree-flow`, `repo-intake`
- Roteamento, fallback e infraestrutura: `route`, `fallback`, `schedule`, `mcp-health`, `mcp-readiness`, `toolkit-sync`, `cost`, `learn`, `research`, `dispatch`

Pense em skills como micro-workflows reutilizaveis que ensinam o agente a executar tarefas recorrentes.

### 6. Implementacoes por Ferramenta

O diretorio `implementations/` mostra como as mesmas ideias se traduzem para ferramentas reais:

- Claude Code
- Codex CLI
- OpenCode
- Cursor
- GitHub Copilot
- Windsurf
- Antigravity
- Gemini

Use essas implementacoes quando voce quiser setup especifico de ferramenta. As ideias centrais continuam nas regras, nos patterns e no kit.

### 7. Organizacoes de Agentes

O diretorio `companies/` contem organizacoes prontas de agentes especialistas.

Aqui, "companies" significa estruturas reutilizaveis de time para agentes, nao estudos de caso de negocio. Elas definem papeis, roteamento, skills e handoff para tornar trabalho multiagente mais previsivel.

O repo inclui organizacoes menores e um exemplo grande:

- `solopreneur`
- `startup-mvp`
- `agency`
- `open-source-maintainer`
- `fullstack-forge`

Se voce esta comecando, trate essa parte como opcional e avancada.

### 8. Tools e Training

Existem duas areas de apoio uteis, mas opcionais:

- `tools/README.md` cataloga CLIs recomendadas, plugins, utilitarios ligados a MCP e helpers de shell para ambientes intensivos em IA
- `training/README.md` cobre captura de conversas e fine-tuning opcional

Nenhuma das duas e obrigatoria para usar bem o toolkit.

## O Modelo Mental Central

Este repositório fica muito mais simples quando voce separa bem as camadas:

- Regras dizem como o agente deve se comportar por padrao.
- Patterns explicam por que um workflow funciona e quando usar.
- Skills ensinam procedimentos reutilizaveis em nivel de tarefa.
- Implementacoes mostram como essas ideias se encaixam em uma ferramenta especifica.
- Organizacoes de agentes definem times especialistas reutilizaveis.
- forge-kit instala e sincroniza o sistema inteiro.

Se voce mantiver essas seis camadas separadas na cabeca, a navegacao pelo repo fica bem mais facil.

## Superficies de Instrucao por Ferramenta

Ferramentas diferentes leem arquivos diferentes para comportamento e guidance do repositorio:

- Claude Code: `CLAUDE.md`
- Codex CLI: `AGENTS.md`
- GitHub Copilot: `.github/copilot-instructions.md` e opcionalmente `.github/instructions/*.instructions.md`
- Gemini CLI: `GEMINI.md`
- Gemini Code Assist no GitHub: `.gemini/styleguide.md`
- Antigravity: `~/.antigravity/rules.md` como superficie principal de regras

Este repositorio agora inclui cobertura explicita de regras e implementacoes para GitHub Copilot, Antigravity e Gemini, para que o mesmo modelo de desenvolvimento assistido por IA possa ser reutilizado nessas ferramentas tambem.

## O Que o `ai-dev-toolkit-setup` Faz

O repositório companheiro `ai-dev-toolkit-setup` resolve outro problema.

Use `ai-dev-toolkit` quando voce quer guidance reutilizavel de desenvolvimento com IA dentro de um projeto.

Use `ai-dev-toolkit-setup` quando voce quer preparar uma maquina com:

- helpers de shell
- workflow de tmux
- bootstrap de OpenCode
- diretorios iniciais de skills
- scaffolding de ambiente local
- scripts guiados de autenticacao
- instalacao de pacotes para uma maquina nova

Em resumo:

- `ai-dev-toolkit` e o manual e a caixa de ferramentas reutilizavel
- `ai-dev-toolkit-setup` e a camada de bootstrap da maquina

Detalhes importantes:

- o setup consome uma release pinada do toolkit via `TOOLKIT_VERSION`
- o setup instala scripts canonicos do toolkit quando esta online
- o setup ainda mantem uma pequena camada offline de fallback
- o setup nao instala secrets nem conclui a autenticacao de provedores por voce

## Caminho Recomendado Para Iniciantes

Se voce quer a menor trilha util de adocao, siga esta ordem:

1. Copie um arquivo de regras para o seu projeto.
2. Leia `patterns/context-building.md`.
3. Leia `patterns/task-orchestration.md`.
4. Adicione `patterns/code-review.md` e `patterns/testing.md`.
5. Adicione memoria e disciplina de sessao com `patterns/memory-systems.md` e `best-practices/context-management.md`.
6. Instale `forge-kit` so depois que souber quais ferramentas realmente usa.
7. Explore organizacoes de agentes apenas quando o workflow com um agente so comecar a quebrar.

## O Que E Opcional e Avancado

Estas areas tem valor, mas iniciantes nao devem comecar por elas:

- organizacoes multiagente em `companies/`
- ecossistema avancado de plugins em `tools/README.md`
- captura de dados e fine-tuning em `training/README.md`
- overlays avancados de orquestracao no OpenCode
- configuracao completa de loops autonomos antes de consolidar habitos basicos de verificacao

## O Que Este Repo Otimiza

O repositório empurra sempre para os mesmos resultados:

- mais contexto antes de codar
- uso mais barato de modelos via roteamento
- menos falhas silenciosas
- permissoes mais seguras
- gates de qualidade repetiveis
- unidades menores e shipaveis de trabalho
- continuidade entre sessoes
- portabilidade entre ferramentas de IA

Se o seu workflow com IA sofre com pouco contexto, qualidade instavel, disciplina de entrega fraca ou repeticao manual demais, este repositório foi feito para atacar exatamente esses problemas.
