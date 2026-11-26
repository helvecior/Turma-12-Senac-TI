
# Correção de tela pequena e falha ao copiar e colar em máquinas virtuais

> **Alerta de Segurança:** Salve seus arquivos e crie um snapshot da máquina virtual antes de realizar alterações.

## 1. Quando Aplicar (Sintoma)

Este procedimento deve ser aplicado quando a tela da máquina virtual apresenta resolução pequena ou não se ajusta ao tamanho da janela.

Também se aplica quando não é possível copiar e colar textos e arquivos entre o computador físico e a máquina virtual.

## 2. Ferramentas/Componentes Necessários

- **Hardware / Físico:** Computador com memória RAM e espaço disponível.
- **Software:** VirtualBox com Guest Additions ou VMware com VMware Tools.

## 3. Passo a Passo Rápido

1. Inicie a máquina virtual e verifique se o sistema operacional está funcionando corretamente.
2. No VirtualBox, acesse Dispositivos e selecione Inserir Imagem de CD dos Adicionais para Convidado. No VMware, utilize a opção de instalação do VMware Tools.
3. Execute o instalador dentro da máquina virtual e siga as instruções apresentadas.
4. Reinicie a máquina virtual após a instalação.
5. Verifique se a resolução da tela se ajusta corretamente e teste as funções de copiar e colar.

**Teste de Validação:** Redimensione a janela da máquina virtual e copie um pequeno texto do computador físico para a VM. Confirme se as duas funções estão funcionando.