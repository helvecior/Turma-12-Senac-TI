# Procedimento Técnico de Backup e Restore com Clonezilla — UC 3

* **Aluno(a):** Laíz Flávia Moreira da Costa
* **Tema:** Backup e Restauração de Dados com Clonezilla

## 1. Objetivo
Este procedimento tem como objetivo orientar a realização de backup e restauração de dados utilizando o Clonezilla. O processo permite criar uma imagem de segurança do disco, garantindo a recuperação das informações em caso de falhas, problemas no sistema ou perda de dados.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** Computador ou máquina virtual.

Software Clonezilla.

Pendrive inicializável com Clonezilla.

HD externo ou disco secundário para armazenar a imagem de backup.

Computador com espaço suficiente para armazenar os arquivos.
* **Segurança / Boas Práticas:** Verificar se o equipamento está conectado à energia.

Conferir se o disco de destino possui espaço suficiente.

Identificar corretamente o disco de origem e o disco de destino.

Realizar o backup antes de qualquer manutenção que possa comprometer os dados.

Evitar interrupções durante o processo.

Conferir se a imagem de backup foi criada corretamente.

Não realizar restaurações sem confirmar o disco de destino, pois os dados existentes nele podem ser sobrescritos.

## 3. Passo a Passo
## 3. Passo a Passo

1. Iniciar o computador pelo pendrive com Clonezilla.
2. Selecionar idioma e configurar o teclado.
3. Escolher a opção `device-image`.
4. Selecionar o disco onde o backup será salvo.
5. Escolher `savedisk` para criar a imagem.
6. Nomear o backup e selecionar o disco de origem.
7. Confirmar e aguardar a conclusão do backup.
8. Para restaurar, selecionar `device-image` e depois `restoredisk`.
9. Escolher a imagem e o disco de destino correto.
10. Confirmar a restauração e aguardar a conclusão.
11. Reiniciar o computador e verificar se o sistema está funcionando.

## 4. Como Validar (Teste Final)
[ ] Confirmar se a imagem de backup foi criada e está disponível no local de armazenamento.


[ ] Verificar se o Clonezilla finalizou o processo sem apresentar erros.


[ ] Confirmar se a restauração foi concluída corretamente.


[ ] Verificar se os arquivos e pastas estão acessíveis após a restauração.


[ ] Testar a inicialização e o funcionamento do sistema operacional.
