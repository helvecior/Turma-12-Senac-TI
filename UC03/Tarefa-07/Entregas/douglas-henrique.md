# Backup e Restauração de Arquivos no Windows

* **Aluno(a):** Douglas Henrique de Brito
* **Tema:** Backup e Restore de arquivos no Windows

## 1. Objetivo
Garantir a proteção, integridade e disponibilidade de arquivos e pastas importantes do sistema Windows por meio da criação de cópias de segurança periódicas (Backup) e da recuperação rápida (Restore) em caso de exclusão acidental, falhas de hardware ou ataques de malware.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** Sistema operacional Windows 10 ou 11 (ferramenta nativa **Backup e Restauração (Windows 7)** no painel de controle) e uma unidade de armazenamento externa (HD externo, pendrive ou pasta compartilhada na rede).
* **Segurança / Boas Práticas:** Utilizar uma conta com privilégios de Administrador, verificar se a unidade de destino possui espaço livre antes de iniciar, armazenar o dispositivo de backup em local físico seguro e desconectar após o término para evitar contaminação por ransoware.

## 3. Passo a Passo
1. Conecte o HD externo ou pendrive (ex: unidade `E:\`) ao computador, abra o **Painel de Controle** e acesse **Sistema e Segurança** > **Backup e Restauração (Windows 7)**.
2. No painel direito, clique em **Configurar backup**, selecione a unidade externa(`E:\`) como destino e clique em **Avançar**.
3. Escolha a opção **Deixar eu escolher** para selecionar manualmente as pastas críticas (como *Documentos*, *Imagens* e *Área de Trabalho*), desmarque a imagem do sistema caso queira apenas arquivos e clique em **Avançar**.
4. Revise o resumo das pastas selecionadas e clique em **Salvar configurações e executar backup**, aguardando a barra de progresso concluir a cópia.
5. Para realizar a **Restauração (Restore)**, acesse novamente **Backup e Restauração (Windows 7)** com a unidade externa conectada e clique no botão **Restaurar meus arquivos**.
6. Clique em **Procurar arquivos** ou **Procurar pastas**, selecione os itens que deseja recuperar, escolha se deseja restaurar **No local original** ou em uma nova pasta de destino e clique em **Restaurar**.

## 4. Como Validar (Teste Final)
- [ ] **Verificação de conclusão:** Confirmar na tela de *Backup e Restauração* se a data e o horário do "Último backup" foram atualizados sem nenhum alerta de falha ou arquivos ignorados.
- [ ] **Conferência de propriedades (Tamanho e Quantidade):** Clicar com o botão direito na pasta restaurada > *Propriedades* comparar se o tamanho total (em MB/GB) e a quantidade de arquivos e subpastas sao iguais aos da pasta original.
- [ ] **Teste de abertura e integridade** Abrir pelo alguns arquivos de extensões diferentes (ex: `.pdf`,`.docx`, `.xlsx` ou `.jpg`) na pasta restaurada para garantir que não estão corrompidos.
- [ ] **Simulação de perda (Teste de recuperação real)** Criar um arquivo de teste, realizar o backup, excluir o arquivo original da máquina (inclusive da Lixeira) e executar a restauração para comprovar que ele retorna intacto.