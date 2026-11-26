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

Use o workflow **Criar pasta de tarefa** sempre que a turma precisar de uma nova pasta. A primeira tarefa de uma UC também cria a pasta da unidade. Para executar o workflow, entre no GitHub com uma conta que tenha permissão de escrita neste repositório.

### 1. Abrir o formulário

1. Abra a aba **Actions** no topo do repositório.
2. Na barra lateral esquerda, selecione **Criar pasta de tarefa**. Você também pode [abrir o workflow diretamente](https://github.com/helvecior/Turma-12-Senac-TI/actions/workflows/createUCdirectory.yml).
3. Acima da lista de execuções, clique em **Run workflow** (Executar fluxo de trabalho). Esse primeiro clique abre o formulário.

### 2. Escolher a UC e o número

| Campo | O que selecionar ou digitar | Exemplo |
| --- | --- | --- |
| **Branch** | Escolha `main` para publicar a pasta na branch principal da turma. | `main` |
| **Em qual UC deseja criar a tarefa?** | Selecione a unidade no menu, de `UC01` a `UC16`. Você pode escolher uma UC cuja pasta ainda será criada. | `UC06` |
| **Número da tarefa** | Digite o número previsto para a atividade, com dois dígitos, de `01` a `99`. | `03` |

Confira os três campos e clique no botão **Run workflow** dentro do formulário. Com os valores do exemplo, o GitHub cria `UC06/Tarefa-03/Materiais/` e `UC06/Tarefa-03/Entregas/`. Se a pasta `UC06/` já existir, a nova tarefa entra ao lado das anteriores. O próprio workflow faz o commit e o push.

### 3. Conferir a execução e usar a pasta

1. Na página do workflow, abra a execução que acabou de iniciar. Aguarde a marca verde de sucesso.
2. Volte à aba **Code**, selecione a mesma branch e abra a UC e a tarefa. No exemplo, o caminho é **UC06 → Tarefa-03**.
3. Coloque enunciados e arquivos de apoio em **Materiais**. Coloque os trabalhos dos alunos em **Entregas**. O arquivo oculto `.gitkeep` permite que o Git registre cada subpasta antes da chegada dos primeiros documentos.
4. Atualize o índice da UC com o nome e o link da tarefa. Se for a primeira atividade da unidade, crie o `README.md` da UC e vincule a nova unidade na tabela deste README. Os índices são mantidos pela turma.

### Se algo der errado

| O que você vê | Como proceder |
| --- | --- |
| O botão **Run workflow** não aparece | Confira se abriu o workflow **Criar pasta de tarefa** na lateral de **Actions** e se sua conta tem acesso de escrita. |
| A execução mostra um **× vermelho** | Abra a execução, clique em **criar-tarefa** e expanda a etapa marcada em vermelho para ler a mensagem. |
| A mensagem indica que a pasta já existe | Abra a pasta pela aba **Code** para acrescentar o material. Se pretendia cadastrar outra tarefa, execute o workflow com o número correspondente. |
| A mensagem pede um número com dois dígitos | Abra o formulário novamente e use, por exemplo, `03`. O intervalo aceito é de `01` a `99`. |

## Guia de Git e GitHub

### 1. Baixar o repositório uma vez

No GitHub, abra **Code → HTTPS** e copie o endereço. O último argumento cria a pasta local com o nome `curso-senac`.

```bash
git clone https://github.com/helvecior/Turma-12-Senac-TI.git curso-senac
cd curso-senac
```

Se o workflow criou a pasta depois que você clonou o repositório, atualize a sua `main` conforme o próximo passo.

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

Depois de adicionar os arquivos à pasta criada pelo workflow e atualizar o índice da UC, prepare apenas os caminhos dessa contribuição. O exemplo usa a tarefa 03 da UC03. Confira o resumo antes de registrar o commit.

```bash
git status
git add UC03/Tarefa-03/ UC03/README.md
git diff --cached --stat
git commit -m "Adiciona materiais à tarefa 03 da UC03"
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
