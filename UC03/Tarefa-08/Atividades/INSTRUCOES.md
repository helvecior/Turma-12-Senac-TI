# Roteiro do Aluno: Passo a Passo no Laboratório

Bem-vindo(a) ao repositório **`0012_uc3_base-conhecimento`**!  
Neste guia você encontrará todas as etapas para escolher uma tarefa, estruturar seu artigo técnico em Markdown (`.md`) sobre máquinas virtuais (VMware Workstation Pro / Oracle VirtualBox) e submetê-lo via **Pull Request**.

---

## Passo 1: Escolher uma Issue no GitHub

1. Acesse o repositório oficial **`0012_uc3_base-conhecimento`** no GitHub do professor e clique na aba **Issues**.
2. Escolha uma Issue aberta que ainda não tenha comentários de outros colegas.
3. Abra a Issue escolhida e deixe o seguinte comentário para indicar sua preferência:
   ```text
   Aluno: Seu nome
   ```
4. Anote o **número da Issue** que aparece ao lado do título (exemplo: **`#1`**, **`#2`**, **`#3`**) e o **nome exato do arquivo** solicitado na descrição.

---

## Passo 2: Fork, Clone e Criação da Branch

1. No repositório oficial do professor, clique no botão **Fork** (canto superior direito) para criar uma cópia na sua conta do GitHub.
2. No **seu** perfil do GitHub, abra o repositório forkado, clique no botão verde **Code** e copie o link **HTTPS**.
3. Abra o **VS Code**, acesse o **Terminal Integrado** (`Ctrl + '`) e clone o **seu fork** para a máquina do laboratório:
   ```bash
   git clone https://github.com/SEU-USUARIO/0012_uc3_base-conhecimento.git
   cd 0012_uc3_base-conhecimento
   ```
4. Crie e mude para uma **branch exclusiva** para a sua tarefa (substitua `X` pelo número da sua Issue e `nome-do-tema` pelo assunto escolhido). **Nunca trabalhe diretamente na branch `main`**:
   ```bash
   git checkout -b docs/issue-X-seu-nome
   ```
5. Confirme com `git branch` se o asterisco (`*`) está apontando para a nova branch criada.

---

## Passo 3: Criar o Arquivo `.md` Pequeno e Estruturado

1. No Explorer do VS Code, abra a pasta `artigos/` e crie **apenas 1 arquivo `.md`** com o nome exato indicado na sua Issue (exemplo: `artigos/erro-vtx-amdv-hyperv.md`).
   > ⚠️ **Atenção:** Use apenas letras minúsculas, sem espaços e sem acentos (`kebab-case`). Não altere nenhum outro arquivo do repositório.
2. Copie a estrutura do arquivo [`TEMPLATE.md`](../Materiais/TEMPLATE.md) e cole dentro do seu novo arquivo.
3. Preencha as seções com informações técnicas objetivas, mantendo o artigo enxuto (**entre 20 e 30 linhas**) e utilizando os 5 recursos essenciais do Markdown:
   * `# Título` — Título principal do procedimento (apenas um por arquivo).
   * `## Subtítulo` — Divisão das seções (`1. Quando Aplicar`, `2. Ferramentas Necessárias`, `3. Passo a Passo Rápido`).
   * `> **Alerta de Segurança:**` — Destaque para riscos de perda de dados, configuração de rede ou hardware.
   * `-` ou `1.` — Listas com marcadores para ferramentas e listas numeradas para etapas sequenciais.
   * `` `comando` `` ou blocos ```` ```bash ```` — Destaque para comandos de terminal, caminhos ou teclas de atalho.
4. Pressione **`Ctrl + Shift + V`** no VS Code para abrir a pré-visualização e conferir se toda a formatação renderizou corretamente.

---

## Passo 4: Treinar Inspeção e Restauração (`git diff` e `git restore`)

Antes de enviar sua entrega, pratique como inspecionar alterações e desfazer edições indesejadas no Git:

1. Com o seu artigo finalizado e salvo, digite uma linha de teste qualquer no final do arquivo (exemplo: `linha de teste com erro`) e salve (`Ctrl + S`).
2. No terminal do VS Code, execute os comandos abaixo para inspecionar o que mudou:
   ```bash
   git status
   git diff
   ```
   Observe que o `git diff` exibe em verde (`+`) exatamente a linha adicionada.
3. Agora, desfaça essa alteração indesejada restaurando o arquivo para o estado limpo anterior:
   ```bash
   git restore artigos/seu-arquivo.md
   ```
4. Rode `git status` novamente e confirme que o arquivo voltou ao normal.

---

## Passo 5: Commit, Push e Pull Request

1. No terminal do VS Code, adicione seu arquivo à área de preparação, registre o *commit* e envie sua branch para o seu Fork no GitHub:
   ```bash
   git add artigos/
   git commit -m "docs: adiciona artigo sobre [tema] (#X)"
   git push -u origin docs/issue-X-nome-do-tema
   ```
2. Acesse o seu repositório no **GitHub** (navegador) e clique no botão verde **Compare & pull request**.
3. Confira se o destino do Pull Request aponta da **sua branch** (`docs/issue-X-seu-nome`) para a branch **`main` do repositório original do professor**.
4. Na caixa de descrição do Pull Request, escreva obrigatoriamente a palavra-chave abaixo com o número da sua Issue para vinculá-la:
   ```markdown
   Closes #X
   ```
   *(Substitua `X` pelo número da sua Issue).*
5. Clique em **Create pull request** e aguarde a avaliação do professor.

---

## Passo 6: Correções após Revisão (Se solicitado)

Caso o professor revise seu Pull Request e solicite ajustes (*Request Changes*):

1. Abra o mesmo arquivo no VS Code, certificando-se de estar na mesma branch (`docs/issue-X-seu-nome`).
2. Realize as correções pedidas e salve (`Ctrl + S`).
3. Envie a atualização para o GitHub:
   ```bash
   git add artigos/
   git commit -m "fix: ajusta artigo conforme revisao (#X)"
   git push
   ```
4. O Pull Request aberto será atualizado automaticamente para nova avaliação.
