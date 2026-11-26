# Procedimento Técnico — Clonagem de Disco com Clonezilla

* **Aluno(a):**  Amanda Carolina Barbosa Silva
* **Tema:** Clonagem de Disco com Clonezilla

## 1. Objetivo
Realizar a clonagem completa de um disco rígido (HD/SSD) utilizando o Clonezilla, criando uma cópia idêntica do sistema operacional, programas, drivers e arquivos do usuário. O procedimento serve para trocar o HD por um SSD sem precisar formatar, ou para restaurar várias máquinas iguais de forma rápida em um laboratório ou escritório, economizando tempo de instalação.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** Clonezilla Live (em Pen Drive bootável de 8GB ou mais). HD de origem (com o sistema pronto) e HD de destino (vazio, com tamanho igual ou maior).Programa Rufus para criar o pen drive bootável e Cabo SATA / Adaptador USB-SATA para ligar o segundo HD.
* **Segurança / Boas Práticas:** Pulseira ESD: Usar para não danificar a placa-mãe e o HD com estática. Backup prévio: Antes de clonar, conferir se o HD de destino está vazio, pois a clonagem APAGA TUDO que estiver nele. Verificação de energia: Usar nobreak, não pode faltar luz no meio da clonagem senão os dois HDs corrompem. Tamanho do disco: O HD de destino tem que ser igual ou maior que o de origem. 

## 3. Passo a Passo
1. Preparar o pen drive: Baixar o Clonezilla Live e criar o pen drive bootável com o Rufus.
2. Ligar os dois HDs: Desligar o PC, colocar a pulseira ESD, ligar o HD de origem e o HD de destino na placa-mãe. 
3. Dar boot pelo Clonezilla: Ligar o PC apertando F12 / Del para entrar no Boot e escolher o pen drive do Clonezilla. Escolher idioma Português e modo Start Clonezilla. 
4. Escolher o tipo de clonagem: Escolher device-device (disco para disco) se for clonar direto, ou device-image se for salvar uma imagem do disco em um HD externo. 
5. Selecionar os discos: Selecionar o disco de origem (Source) com cuidado e depois o disco de destino (Target). Conferir 2 vezes para não inverter! 
6. Iniciar a clonagem: Confirmar com y e esperar o processo terminar (pode demorar 20 a 60 min). No final escolher -p poweroff para desligar. 
7. Testar o disco clonado: Desligar, tirar o HD antigo e deixar só o novo, ligar o PC e ver se o Windows inicia normal. 

## 4. Como Validar (Teste Final)
- Teste 1 para confirmar que deu certo: O PC ligou só com o HD clonado e entrou no Windows normalmente, sem pedir formatação. 
- Teste 2 para confirmar que deu certo: Abrir o Windows, conferir se os arquivos, programas (Word, navegador) e o papel de parede estão idênticos ao HD original e abrir o Gerenciamento de Disco para ver se as partições foram copiadas. 
