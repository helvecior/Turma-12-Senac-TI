# Técnico em Informática · Senac

Este acervo reúne os enunciados, os modelos e os materiais de estudo da Turma 12 de Técnico em Informática do Senac. Escolha a unidade curricular na tabela para abrir o índice de tarefas.

**Materiais da turma** · [UC01 — 23 atividades](./UC01/README.md) · [UC02 — 14 atividades](./UC02/README.md) · [UC03 — 11 atividades](./UC03/README.md) · [UC04 — 2 atividades](./UC04/README.md)

[Unidades curriculares](#unidades-curriculares) · [Avisos e links importantes](#avisos-e-links-importantes) · [Recurso didático complementar](#recurso-didático-complementar) · [Como criar uma tarefa](#como-criar-uma-tarefa) · [Guia de Git e GitHub](#guia-de-git-e-github) · [AVA da turma](https://ava.mg.senac.br/edu/course/view.php?id=18936)

## Unidades curriculares

| Pasta | Título da unidade curricular |
| --- | --- |
| [UC01](./UC01/) | Planejar e executar a montagem de computadores |
| [UC02](./UC02/) | Planejar e executar a instalação de hardware e software para computadores |
| [UC03](./UC03/) | Planejar e executar a manutenção de computadores |
| [UC04](./UC04/) | Projeto Integrador Assistente de Suporte em Manutenção de Computadores |
| [UC05](./UC05/) | Planejar e executar a instalação de redes locais de computadores |
| UC06 | Planejar e executar a manutenção de redes locais de computadores |
| UC07 | Planejar e executar a instalação, a configuração e o monitoramento de sistemas operacionais de redes locais (servidores) |
| UC08 | Projeto Integrador Assistente de Operação de Redes de Computadores |
| UC09 | Desenvolver algoritmos |
| UC10 | Desenvolver banco de dados |
| UC11 | Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para desktop |
| UC12 | Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para internet |
| UC13 | Executar os processos de codificação, manutenção e documentação de aplicativos computacionais para mobile |
| UC14 | Elaborar design de interação para aplicações web |
| UC15 | Desenvolver e organizar elementos estruturais de sites |
| UC16 | Projeto Integrador Assistente de Desenvolvimento de Aplicativos Computacionais |

## Avisos e links importantes

[Abrir esta seção no AVA](https://ava.mg.senac.br/edu/course/view.php?id=18936#section-0)

| Recurso | Acesso |
| --- | --- |
| TEAMS - Classe: 031.2026.0012 - Técnico em Informática | [Abrir no AVA](https://ava.mg.senac.br/edu/mod/url/view.php?id=609017) · [Acesso direto](https://teams.cloud.microsoft/l/team/19%3AHsC5D20CFmb6_6I8G2WrIaLoUByOkLjSyn6LW9KGnxo1%40thread.tacv2/conversations?groupId=42484a1a-923b-45ae-a7ed-92e2013def8d&tenantId=a5e904b4-70f1-4f44-a1cc-3663c33b6d8a) |
| ORANGO - Língua Portuguesa e Matemática para o mundo do trabalho | [Abrir no AVA](https://ava.mg.senac.br/edu/mod/url/view.php?id=608967) · [Acesso direto](https://orango.senac.br/paravoce/) |
| CACHOLA | [Abrir no AVA](https://ava.mg.senac.br/edu/mod/url/view.php?id=608971) · [Acesso direto](https://cachola.senac.br/) |

## Recurso didático complementar

[Abrir esta seção no AVA](https://ava.mg.senac.br/edu/course/view.php?id=18936#section-6)

| Recurso | Acesso |
| --- | --- |
| Aprendendo a aprender: ferramentas mentais poderosas para ajudá-lo a dominar assuntos difíceis (em Português) | [Abrir no AVA](https://ava.mg.senac.br/edu/mod/url/view.php?id=615665) · [Acesso direto](https://www.coursera.org/learn/aprender) |
| Diferença entre GB e GiB | [Abrir no AVA](https://ava.mg.senac.br/edu/mod/resource/view.php?id=601918) |

## Organização do repositório

O curso tem 16 unidades. As UCs com pasta publicada têm um link no índice. O [repositório da turma](https://github.com/helvecior/Turma-12-Senac-TI) também pode ser consultado online. Cada unidade pode receber várias tarefas. A pasta [Modelo-Tarefa](./Configuracoes/Modelo-Tarefa/) serve de modelo para todas elas.

| Dentro de cada tarefa | O que guardar | Exemplo |
| --- | --- | --- |
| [Entregas](./Configuracoes/Modelo-Tarefa/Entregas/) | O que o aluno ou grupo produziu. Quando houver várias entregas, use uma subpasta por autor ou equipe. | `Entregas/Grupo-02/Relatorio.pdf` |
| [Materiais](./Configuracoes/Modelo-Tarefa/Materiais/) | Enunciados, materiais de apoio, instruções, regras, modelos e licenças. | Manual de apoio ou `links.md` com o repositório de exemplo. |

Se a própria **entrega** estiver no GitHub, registre o link em `Entregas/`, junto com o nome do trabalho. A finalidade do arquivo determina a pasta.

## Como criar uma tarefa

Em **Actions → Criar pasta de tarefa → Run workflow**, escolha a UC e informe o número da tarefa com dois dígitos. O workflow cria a pasta da UC quando necessário, copia o modelo e registra a tarefa na branch selecionada. Ao inaugurar uma UC, acrescente o link para ela no índice.

Para criar a estrutura manualmente:

1. Na raiz do repositório, copie a pasta `Configuracoes/Modelo-Tarefa/` para dentro da UC correspondente.
2. Dê à cópia um nome com o número da tarefa e um tema curto. Por exemplo, para uma nova tarefa de revisão na UC03, use `UC03/Tarefa-XX-Revisao/`, substituindo `XX` pelo número da nova tarefa.
3. Coloque cada arquivo na subpasta correspondente. No `README.md` da UC, acrescente um link como `[Tarefa XX — Revisão](./Tarefa-XX-Revisao/)`.

No Linux ou no Git Bash, o comando abaixo executa os dois primeiros passos do exemplo. Rode-o na raiz, ao criar essa tarefa pela primeira vez.

```bash
cp -r Configuracoes/Modelo-Tarefa UC03/Tarefa-XX-Revisao
```

Os arquivos ocultos `.gitkeep` permitem que o Git inclua as duas subpastas mesmo enquanto estão vazias.

## Guia de Git e GitHub

### 1. Baixar o repositório uma vez

No GitHub, abra **Code → HTTPS** e copie o endereço. O último argumento cria a pasta local com o nome `curso-senac`.

```bash
git clone https://github.com/helvecior/Turma-12-Senac-TI.git curso-senac
cd curso-senac
```

Se estiver usando este ZIP no clone da turma pela primeira vez, extraia-o em uma pasta separada. Copie o modelo `Configuracoes/Modelo-Tarefa/` e os arquivos da UC que você quer adicionar para o clone. Confira os arquivos existentes antes de substituí-los.

### 2. Atualizar a main e criar uma branch

Comece com `git status` para conferir se há trabalho local em andamento. Com suas alterações anteriores já registradas, atualize a `main` e crie uma branch para a nova contribuição.

```bash
git status
git switch main
git pull --ff-only
git switch -c docs/uc03-revisao
```

O `pull --ff-only` atualiza a branch quando o histórico local pode avançar diretamente até o remoto. O `switch -c` cria uma branch e já muda para ela. Para retomar uma branch existente, use `git switch docs/uc03-revisao`.

### 3. Registrar os arquivos e publicar a branch

Depois de copiar o modelo, adicionar os arquivos e atualizar o índice da UC, prepare apenas os caminhos dessa contribuição. Confira o resumo antes de registrar o commit.

```bash
git status
git add UC03/Tarefa-XX-Revisao/ UC03/README.md
git diff --cached --stat
git commit -m "Adiciona a tarefa de revisão à UC03"
git push -u origin docs/uc03-revisao
```

O **commit** registra a mudança no seu computador. O **push** envia os commits ao GitHub. No primeiro push, `-u` vincula a branch local à branch de mesmo nome em `origin`, o remoto criado pelo clone. Nos próximos envios dessa branch, basta `git push`.

### 4. Abrir e acompanhar um pull request

1. No GitHub, abra **Pull requests → New pull request**.
2. Em **base**, escolha `main`. Em **compare**, escolha `docs/uc03-revisao`.
3. Confira as mudanças, clique em **Create pull request** e descreva a tarefa e a UC.
4. Para atender a uma revisão, faça outro commit na mesma branch e use `git push`. O pull request recebe a atualização automaticamente.
5. Depois que a pessoa responsável fizer o **merge**, volte à principal no seu computador com `git switch main` e atualize com `git pull --ff-only`.

O **pull request** propõe integrar sua contribuição à branch principal. Já o comando **git pull** traz as atualizações do remoto para a branch local.

### 5. Sincronizar pelo VS Code

No painel **Controle do Código-Fonte** (`Ctrl+Shift+G`), confira a branch ativa e registre as alterações que deseja enviar. **Sincronizar Alterações** (*Sync Changes*) executa um pull e depois um push na branch atual. Se ela for nova, use **Publicar Branch** primeiro. A sincronização envia os commits já criados, por isso os arquivos apenas editados ainda precisam de um commit.

### Consulta rápida

| Quero… | Comando | O que observar |
| --- | --- | --- |
| Saber em qual branch estou | `git branch` | O asterisco identifica a branch ativa. |
| Listar também as branches remotas conhecidas | `git branch -a` | Atualize a lista com `git fetch origin`. |
| Conferir o que mudou | `git status` | Mostra arquivos novos, modificados e preparados. |
| Ver as alterações de texto em um arquivo rastreado | `git diff` | Mostra mudanças ainda fora da área de preparação. |
| Revisar o que vai entrar no commit | `git diff --cached` | Mostra as alterações preparadas com `git add`. |
| Tirar um arquivo da preparação | `git restore --staged UC03/README.md` | Mantém suas edições no arquivo. |
| Consultar o histórico de uma UC | `git log --oneline -- UC03/` | Lista commits que alteraram arquivos daquela pasta. |
| Ver o endereço do remoto | `git remote -v` | Mostra as URLs usadas para buscar e enviar commits. |

**Documentação:** [Referência do Git](https://git-scm.com/docs) · [Pull requests no GitHub](https://docs.github.com/pt/pull-requests/reference/pull-requests) · [Sincronização no VS Code](https://code.visualstudio.com/docs/sourcecontrol/repos-remotes)
