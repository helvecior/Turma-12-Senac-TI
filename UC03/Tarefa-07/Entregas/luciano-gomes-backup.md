# Procedimento Técnico de Backup e Restore — UC 3

* **Aluno(a):** luciano martins gomes
* **Tema:** Backup e Restore

## 1. Objetivo
Garantir a integridade e a recuperação rápida de dados críticos e imagens de sistema em computadores antes de manutenções, atualizações ou falhas de armazenamento. Na rotina técnica, evita perda definitiva de arquivos e reduz o tempo de inatividade da estação de trabalho.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** HD externo ou pendrive com capacidade compatível, mídia bootável (Linux/Clonezilla ou utilitário de imagem), ferramentas nativas do sistema (como `rsync` ou utilitários de backup do SO) e cabo de dados/energia confiável.
* **Segurança / Boas Práticas:** Utilizar pulseira antiestática (ESD) ao manusear discos internos, verificar integridade da energia elétrica (evitar quedas de luz durante gravação/restauração), confirmar o disco de origem e o de destino antes de gravar e validar a leitura do destino antes de formatar qualquer unidade.

## 3. Passo a Passo
1. Identifique os diretórios críticos do usuário e/ou partições do sistema que devem ser preservados, verificando o espaço livre disponível na unidade de backup.
2. Conecte a unidade de destino externa e execute a cópia ou criação da imagem de backup, registrando logs ou mensagens de conclusão:
   ```bash
   rsync -avh --progress /caminho/origem/ /caminho/destino/backup/
   ```
3. Para o restore, conecte a mídia de backup, selecione o ponto/arquivo válido correspondente à data desejada e restaure os dados ou imagem para o diretório ou partição de destino:

## 4. Como Validar (Teste Final)
- [ ] Conferir se a estrutura de pastas, permissões e arquivos restaurados está completa e se os arquivos abrem sem corrupção.
- [ ] Verificar o tamanho total e a quantidade de itens entre origem e destino (ou validar o log/checksum do backup) para confirmar que não houve falhas durante a cópia ou restauração.
