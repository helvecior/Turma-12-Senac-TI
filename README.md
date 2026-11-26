# Turma 0012 - Tecnico em Informática - Senac

## Comandos usados para criar as 16 branches para as UC's no GitHubs

### Versão que com o intuito do 16 ser o mais antigo (16 é o primeiro)

``` bash
for i in {16..01}; do git checkout -b "UC$i"; git push -u origin "UC$i"; done
```

### Versão que com o intuito do 16 ser o mais novo (16 é o último)

``` bash
for i in {01..16}; do git checkout -b "UC$i"; git push -u origin "UC$i"; done
```

> **Nota:** Apesar de ambos comandos criarem as branches corretamente, nenhum dos dois comandos conseguiu fazer com que as branches ficassem na ordem do menor para o maior na lista de seleção de branches do GitHub.

## Comando usado para apagar todas as branches locais e remotas caso dê algum erro

``` bash
{
git checkout main
for i in {01..16}; do
  git push origin --delete "UC$i" ||  git push origin --delete "UC0$i";
  git branch -d "UC$i" || git branch -d "UC$i"; done
git checkout main
git branch
}
```
