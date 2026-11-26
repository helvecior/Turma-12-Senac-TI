# Tarefa 11 · Inventário dos adaptadores de rede pelo PowerShell

[Índice da UC02](../../README.md) · [Atividade no AVA](https://ava.mg.senac.br/edu/mod/assign/view.php?id=624365)

## Orientações da turma

Copie e cole o comando abaixo em um terminal do Windows na máquina física e pressione Enter.

Copie e cole a saída completa do comando nesta tarefa.

```powershell
Get-NetAdapter | ForEach-Object {
 $ip = Get-NetIPAddress -InterfaceIndex $_.InterfaceIndex -AddressFamily IPv4 -ErrorAction SilentlyContinue
 [PSCustomObject]@{
 InterfaceDescription = $_.InterfaceDescription
 MacAddress = $_.MacAddress
 IPAddress = $ip.IPAddress -join ', '
 }
} | Format-Table -AutoSize
```
