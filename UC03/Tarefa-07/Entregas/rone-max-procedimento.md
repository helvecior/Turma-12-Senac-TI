
# Procedimento Técnico — Backup e Restauração com Clonezilla

## 1. Objetivo

Este procedimento tem como objetivo orientar a realização de backup e restauração de computadores utilizando o Clonezilla. A ferramenta permite criar imagens de discos para proteger os dados e recuperar o sistema em caso de falhas.

## 2. Ferramentas e Cuidados Técnicos

- **Ferramentas / Softwares:** Clonezilla Live, pendrive bootável e HD externo ou dispositivo de armazenamento para salvar a imagem.
- **Segurança / Boas Práticas:** Verificar os discos antes de iniciar, manter o computador conectado à energia, conferir o espaço disponível no HD externo e garantir que o backup foi concluído corretamente.

## 3. Passo a Passo

1. **Preparação:** Baixar o Clonezilla Live, preparar um pendrive bootável e conectar o dispositivo externo que armazenará o backup.

2. **Realização do Backup:** Reiniciar o computador pelo pendrive do Clonezilla. Selecionar o idioma, escolher o modo padrão e acessar a opção `device-image`. Selecionar o dispositivo onde a imagem será armazenada e escolher `savedisk` para criar uma cópia completa do disco.

```bash
# Exemplo de identificação dos discos
lsblk
```

3. **Restauração do Backup:** Inicializar novamente pelo pendrive do Clonezilla, selecionar `device-image`, localizar a imagem salva e escolher `restoredisk`. Selecionar o disco de destino correto e confirmar a operação. Atenção: a restauração substitui os dados existentes no disco de destino.

## 4. Como Validar (Teste Final)

- [ ] Verificar se a imagem de backup foi criada e está armazenada corretamente.
- [ ] Conferir se a restauração foi concluída sem erros.
- [ ] Reiniciar o computador e verificar se o sistema operacional inicia normalmente.
- [ ] Conferir se os arquivos e programas necessários estão acessíveis.
