# Roteiro do Aluno: Instruções detalhadas da atividade

Siga todas as etapas abaixo utilizando o **VS Code** como ferramenta principal de trabalho.

---

## Passo 1: Reservar sua Tarefa (GitHub Issues)

1. Acesse o repositório oficial **`0012_uc3_tarefa09`** no GitHub e clique na aba **Issues**.
2. Escolha uma Issue que ainda não tenha comentários, abra-a e comente: **`Eu assumo esta tarefa`**.
3. Anote o **número da Issue** exibido ao lado do título (ex.: `#1`, `#2`, `#3`).

---

## Passo 2: Fork e Clone "ao Lado" pelo VS Code

1. No repositório do professor no GitHub, clique em **Fork** (canto superior direito) para criar uma cópia na sua conta.
2. **Atenção à organização das pastas:** O novo repositório **não pode** ser clonado dentro da pasta de outra atividade (`0012_uc3_base-conhecimento`). Ele deve ficar **ao lado**, em uma pasta raiz de projetos:

   ```text
   projetos-git/                        <-- Pasta raiz (NÃO tem .git aqui)
   ├── 0012_uc3_base-conhecimento/    <-- Repositório da Atividade 02
   └── 0012_uc3_tarefa09/  <-- Novo repositório da Atividade 03 (AO LADO)
   ```

3. **Clonando direto pelo VS Code:**
   * Abra uma **nova janela** do VS Code (`Ctrl + Shift + N`).
   * Pressione `Ctrl + Shift + P`, digite **`Git: Clone`** e pressione `Enter`.
   * Cole a URL HTTPS do **seu Fork** (`[https://github.com/SEU-USUARIO/0012_uc3_tarefa09.git](https://github.com/SEU-USUARIO/0012_uc3_tarefa09.git)`).
   * Selecione a pasta pai (`projetos-git/`) e, quando aparecer o aviso no canto inferior direito, clique em **Open** para abrir o projeto no VS Code.

---

## Passo 3: Configurar o `upstream` e Sincronizar (Conceito Novo)

Para manter seu *fork* conectado ao repositório oficial do professor e receber as atualizações aprovadas da turma:

1. Abra o **Terminal Integrado** do VS Code (`Ctrl + '`) e verifique se o caminho termina em `0012_uc3_tarefa09`.
2. Cadastre o repositório original do professor como **`upstream`**:

   ```bash
   git remote add upstream https://github.com/USUARIO-DO-PROFESSOR/0012_uc3_tarefa09.git
   ```

3. Confira se os dois remotos (`origin` = seu fork; `upstream` = repositório do professor) estão configurados:

   ```bash
   git remote -v
   ```

4. Puxe eventuais atualizações da branch de produção (`main`) do professor:

   ```bash
   git pull upstream main
   ```

---

## Passo 4: Criar a Branch de Homologação (Nunca use a `main`!)

A branch `main` representa o ambiente de **Produção**. Todo desenvolvimento deve ser feito em uma branch de **Homologação**:

1. No terminal do VS Code (ou clicando no nome `main` no canto inferior esquerdo da barra azul do VS Code > *Create new branch*), crie e mude para a sua branch de homologação (substitua `X` pelo número da sua Issue):

   ```bash
   git checkout -b homologacao/issue-X-tema
   ```

   *(Exemplo: `homologacao/issue-2-bips-bios`)*
2. Confirme no canto inferior esquerdo do VS Code se o nome exibido mudou de `main` para `homologacao/issue-X-tema`.

---

## Passo 5: Criar, Nomear e Salvar Corretamente o Arquivo `.md`

1. No Explorer do VS Code, clique com o botão direito sobre a pasta **`artigos`** > **New File...**
   * **Atenção:** **Não** abra nem edite o arquivo `.gitkeep`.
2. Digite o nome exato solicitado na Issue, conferindo:
   * Todas as letras **minúsculas**;
   * Sem acentos e sem espaços;
   * Palavras separadas por **hífen (`-`)** (não use `_`);
   * Extensão obrigatória **`.md`** no final (ex.: `artigos/diagnostico-bips-bios.md`).
3. Copie o conteúdo de `MODELO-ARTIGO.md`, cole no seu novo arquivo e preencha todas as seções:
   * Apague **todos os colchetes `[...]`** e textos de instrução do modelo.
   * Pressione `Ctrl + Shift + V` no VS Code para conferir a visualização formatada do Markdown.
   * Salve o arquivo (`Ctrl + S` — verifique se a bolinha branca na aba do arquivo desapareceu).

---

## Passo 6: Inspeção Visual no VS Code, Commit e Push

Antes de enviar, utilize as ferramentas visuais do VS Code para auditar sua entrega:

1. Clique no ícone **Source Control** na barra lateral esquerda (`Ctrl + Shift + G`).
2. Verifique na lista **Changes** se aparece **somente 1 arquivo novo** (`U` - *Untracked*) dentro de `artigos/` (se aparecer `.gitkeep` ou `README.md` modificados, clique na seta de desfazer *Discard Changes* neles).
3. Clique no sinal **`+`** (*Stage Changes*) ao lado do seu arquivo `.md` para enviá-lo à área de preparação.
4. Digite a mensagem de commit na caixa superior (ex.: `docs: adiciona guia de diagnostico de bips da bios (#2)`) e clique em **Commit**.
5. Confira o histórico gerado rodando no terminal:

   ```bash
   git log --oneline -n 3
   ```

6. Envie a branch de homologação para o seu Fork no GitHub clicando em **Publish Branch** no VS Code (ou via terminal):

   ```bash
   git push -u origin homologacao/issue-X-tema
   ```

---

## Passo 7: Abrir o Pull Request no GitHub

1. Acesse o seu Fork no navegador e clique no botão verde **Compare & pull request**.
2. Confira no topo da página se a comparação aponta:
   * **base repository:** `PROFESSOR/0012_uc3_tarefa09` (`base: main`)
   * **head repository:** `SEU-USUARIO/0012_uc3_tarefa09` (`compare: homologacao/issue-X-tema`)
3. Na descrição do Pull Request, escreva obrigatoriamente:

   ```markdown
   Closes #X
   ```

   *(Substitua `X` pelo número da sua Issue).*
4. Clique em **Create pull request**. Se o professor solicitar ajustes (*Request changes*), edite o mesmo arquivo na branch `homologacao/issue-X-tema`, faça um novo `commit` e `push`.
