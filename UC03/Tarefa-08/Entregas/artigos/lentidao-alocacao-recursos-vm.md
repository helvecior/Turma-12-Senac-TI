# VirtualBox/VMware: Lentidão extrema na VM e travamento do PC hospedeiro

> **Alerta de Segurança:** Desligue completamente a máquina virtual (não use o modo "Salvar Estado" ou "Pausar") e crie um ponto de restauração no sistema hospedeiro antes de alterar o dimensionamento de hardware virtual ou recursos de segurança do Windows.

## 1. Quando Aplicar (Sintoma)
Aplique este procedimento quando a máquina virtual apresentar resposta severamente atrasada (engasgos no mouse e demora para abrir programas) acompanhada de congelamentos no computador físico hospedeiro. O cenário indica contenção de recursos físicos (esgotamento de RAM, sobrecarga de vCPUs ou saturação de I/O de disco) ou conflito de hipervisores nativos.

## 2. Ferramentas/Componentes Necessários
* **Hardware / Físico:** Processador com suporte à virtualização (Intel VT-x ou AMD-V), Memória RAM física com folga mínima de 4 GB para o hospedeiro e unidade de armazenamento SSD/NVMe (com pelo menos 15% de espaço livre)
* **Software:** Oracle VirtualBox (com Extension Pack e Guest Additions) ou VMware Workstation Player/Pro (com VMware Tools), Gerenciador de Tarefas do Windows (ou htop/iotop no Linux) e painel de Segurança do Windows.

## 3. Passo a Passo Rápido
1. **Ajuste os recursos e aceleração da VM:** Com a VM desligada, limite a RAM e os núcleos (vCPU) a no máximo 50% do total físico, ative VT-x/AMD-V com Aceleração 3D e instale o Guest Additions (VirtualBox) ou VMware Tools (VMware).
2. **Otimize o disco e desative conflitos do hospedeiro:** Mova o arquivo da VM para um SSD, adicione a pasta às exclusões do antivírus e desative o Hyper-V do Windows via PowerShell (como Administrador), reiniciando o PC em seguida:
   ```bash
   # bcdedit /set hypervisorlaunchtype off
   ```
3. **Teste de Validação:** Inicie a VM, abra o Gerenciador de Tarefas do PC físico (aba Desempenho) e confirme se o uso total de Memória RAM permanece abaixo de 85% e o Tempo de atividade do Disco abaixo de 80% durante o uso normal.